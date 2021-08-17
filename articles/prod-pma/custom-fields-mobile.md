---
title: Implémenter des champs personnalisés pour l’application mobile Microsoft Dynamics 365 Project Timesheet sur iOS et Android
description: Cette rubrique offre des modèles courants pour utiliser les extensions en vue d’implémenter les champs personnalisés.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 9f19a6d069c4f825be8515a6d26739c50d3b064698fc1872ede07a4e74ee4dcb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005748"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implémenter des champs personnalisés pour l’application mobile Microsoft Dynamics 365 Project Timesheet sur iOS et Android

[!include [banner](../includes/banner.md)]

Cette rubrique offre des modèles courants pour utiliser les extensions en vue d’implémenter les champs personnalisés. Les rubriques suivantes sont abordées :

- Les différents types de données compatibles avec la structure de champs personnalisés
- Procédure d’affichage des champs en lecture seule ou modifiables sur les entrées de feuille de temps et d’enregistrement des valeurs fournies par l’utilisateur dans la base de données
- Procédure d’affichage des champs en lecture seule sur l’en-tête de la feuille de temps
- Procédure d’intégration d’une autre logique métier personnalisée pour saisir des valeurs par défaut dans les champs et de validation supplémentaire

## <a name="audience"></a>Audience

Cette rubrique est destinée aux développeurs qui intègrent leurs champs personnalisés dans l’application mobile Microsoft Dynamics 365 Project Timesheet disponible pour Apple iOS et Google Android. Supposons que les lecteurs connaissent bien le développement X++ et la fonctionnalité de feuille de temps de projet.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contrat de données - Classe TSTimesheetCustomField X++

La classe **TSTimesheetCustomField** correspond à la classe de contrat de données X++ qui représente des informations sur un champ personnalisé pour la fonctionnalité de feuille de temps. Les listes des objets de champ personnalisé sont transmises à la fois au contrat de données TSTimesheetDetails et au contrat de données TSTimesheetEntry pour afficher les champs personnalisés dans l’application mobile.

- **TSTimesheetDetails** : contrat d’en-tête de la feuille de temps.
- **TSTimesheetEntry**  contrat de transaction de la feuille de temps. Les groupes de ces objets, avec les mêmes informations de projet et la valeur **timesheetLineRecId**, constituent une ligne.

### <a name="fieldbasetype-types"></a>fieldBaseType (types)

La propriété **FieldBaseType** sur l’objet **TsTimesheetCustom** détermine le type de champ qui apparaît dans l’application. Les valeurs **Types** suivantes sont prises en charge.

| Valeur de types | Type              | Remarques |
|-------------|-------------------|-------|
| 0           | Chaîne (et énumération) | Le champ apparaît comme un champ de texte. |
| 1           | Integer           | La valeur est affichée sous forme d’un nombre sans décimales. |
| 2           | Réel              | La valeur est affichée sous forme de nombre avec des décimales.<p>Pour afficher la valeur réelle en tant que devise dans l’application, utilisez la propriété **fieldExtenededType**. Vous pouvez utiliser la propriété **numberOfDecimals** pour définir le nombre de décimales affichées.</p> |
| 3           | Date              | Les formats de date sont déterminés par le paramètre d’utilisateur **Format de date, d’heure et de nombre** précisé sous **Préférence de langue et pays/région** dans **Options d’utilisateur**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Si la propriété **stringOptions** n’est pas fournie sur l’objet **TSTimesheetCustomField**, un champ de texte libre est fourni à l’utilisateur.

    La propriété **stringLength** peut être utilisée pour définir la longueur de chaîne maximale que les utilisateurs peuvent saisir.

- Si la propriété **stringOptions** est fournie sur l’objet **TSTimesheetCustomField**, ces éléments de liste sont les seules valeurs que les utilisateurs peuvent sélectionner à l’aide des boutons d’option.

    Dans ce cas, le champ de chaîne peut agir comme une valeur d’énumération à des fins de saisie de l’utilisateur. Pour enregistrer la valeur dans la base de données en tant qu’énumération, mappez manuellement la valeur de chaîne vers la valeur d’énumération avant de procéder à l’enregistrement dans la base de données à l’aide d’une chaîne de commande (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application vers la base de données » ultérieurement dans cette rubrique pour un exemple).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Vous pouvez utiliser cette propriété pour mettre en forme des valeurs réelles en tant que devise. Cette approche n’est applicable que lorsque la valeur **fieldBaseType** est définie sur **Réel**.

- **TSCustomFieldExtendedType:None**: aucune mise en forme n’est appliquée.
- **TSCustomFieldExtendedType::Currency** : formater la valeur en tant que devise.

    Lorsque le formatage de la devise est actif, le champ **stringValue** peut être utilisé pour passer le code devise qui doit être affiché dans l’application. La valeur est une valeur en lecture seule.

    Le champ **realValue** contient la somme d’argent qui doit être enregistrée dans la base de données.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Vous pouvez utiliser cette propriété pour spécifier l’emplacement du champ personnalisé dans l’application.

- **TSCustomFieldSection ::Header** : le champ apparaît dans la section **Afficher plus de détails** dans l’application. Ces champs sont toujours en lecture seule.
- **TSCustomFieldSection::Line** : le champ apparaît après tous les champs de ligne prêts à l’emploi sur les entrées de feuille de temps. Ces champs peuvent être modifiables ou en lecture seule.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Cette propriété identifie le champ lorsque les valeurs fournies par l’application sont enregistrées dans la base de données.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Cette propriété identifie le champ lorsque les valeurs fournies par l’application sont enregistrées dans la base de données.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Définissez cette propriété sur **Oui** pour spécifier que le champ de la section d’entrée de la feuille de temps doit être modifiable par les utilisateurs. Définissez la propriété sur **Non** pour rendre le champ en lecture seule.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Définissez cette propriété sur **Oui** pour indiquer que le champ de la section d’entrée de la feuille de temps est obligatoire.

### <a name="label-str"></a>étiquette (chaîne)

Cette propriété spécifie l’étiquette affichée à côté du champ dans l’application.

### <a name="stringoptions-list-of-strings"></a>stringOptions (liste des chaînes)

Cette propriété est applicable uniquement lorsque **fieldBaseType** est réglé sur **Chaîne**. Si **stringOptions** est défini, les valeurs de chaîne disponibles pour la sélection via les boutons d’option sont spécifiées par les chaînes de la liste. Si aucune chaîne n’est fournie, l’entrée de texte libre dans le champ de chaîne est autorisée (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application dans la base de données » ultérieurement dans cette rubrique pour un exemple).

### <a name="stringlength-int"></a>stringLength (entier)

Cette propriété spécifie la longueur maximale d’un champ de chaîne. Elle est applicable uniquement lorsque **fieldBaseType** est réglé sur **Chaîne**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (entier)

Cette propriété spécifie le nombre de décimales affichées pour un champ réel. Elle est applicable uniquement lorsque le champ **fieldBaseType** est défini sur **Réel**.

### <a name="ordersequence-int"></a>orderSequence (entier)

Cette propriété contrôle l’ordre dans lequel les champs personnalisés sont affichés dans l’application lorsque plusieurs champs personnalisés sont spécifiés. Les champs avec des nombres inférieurs apparaissent en premier.

### <a name="booleanvalue-boolean"></a>booleanValue (booléen)

Pour les domaines de type **Booléen**, cette propriété transmet la valeur booléenne du champ entre le serveur et l’application.

### <a name="guidvalue-guid"></a>guidValue (guid)

Pour les domaines de type **GUID**, cette propriété transmet la valeur GUID (identificateur global unique) du champ entre le serveur et l’application.

### <a name="int64value-int64"></a>int64Value (int64)

Pour les domaines de type **Int64**, cette propriété transmet la valeur int64 du champ entre le serveur et l’application.

### <a name="intvalue-int"></a>intValue (entier)

Pour les champs de type **Entier**, cette propriété transmet la valeur entier du champ entre le serveur et l’application.

### <a name="realvalue-real"></a>realValue (réel)

Pour les champs de type **Réel**, cette propriété transmet la valeur réel du champ entre le serveur et l’application.

### <a name="stringvalue-str"></a>stringValue (chaîne)

Pour les champs de type **Chaîne**, cette propriété transmet la valeur chaîne du champ entre le serveur et l’application. Il est également utilisé pour les champs de type **Réel** qui est formaté comme devise. Pour ces champs, la propriété est utilisée pour transmettre le code de devise à l’application.

### <a name="datevalue-date"></a>dateValue (date)

Pour les champs de type **Date**, cette propriété transmet la valeur date du champ entre le serveur et l’application.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Afficher et enregistrer un champ personnalisé dans la section d’entrée de la feuille de temps

Vous trouverez ci-dessous une capture d’écran de l’application mobile d’une création d’entrée de feuille de temps. Elle présente les champs prêts à l’emploi et un champ personnalisé dans la section « Entrée de temps » appelée « Chaîne de test » avec une valeur d’énumération « Deuxième option » déjà définie.

![Champ personnalisé Chaîne de test dans l’application.](media/timesheet-entry.jpg)



Vous trouverez ci-dessous une capture d’écran de l’application mobile de l’utilisateur sélectionnant l’une des options d’énumération disponibles pour le champ personnalisé « Chaîne de test ».  Les deux options sont « Première option » et « Deuxième option » affichées sous forme de case d’option. La deuxième option est actuellement sélectionnée.

![Cases d’option pour le champ personnalisé Chaîne de test.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Développer la table TSTimesheetLine afin qu’elle ait un champ personnalisé

Dans les scénarios types, il est probable que les données d’un champ personnalisé dans la section d’entrée de feuille de temps soient enregistrées dans la table TSTimesheetLine. Cependant, d’autres tables peuvent être utilisées si les données peuvent être récupérées en fonction d’un enregistrement TSTimesheetTrans fourni, ou si elles n’ont pas de contexte d’enregistrement spécifique (par exemple, si le champ est défini en lecture seule dans les paramètres du projet).

Notez que les champs personnalisés n’ont pas besoin d’enregistrements de base de données de sauvegarde. Ils peuvent être générés dynamiquement en fonction de la logique X++. Cette approche peut être utile dans les scénarios en lecture seule (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetDetails, méthode buildCustomFieldListForHeader pour renseigner les détails de la feuille de temps » pour un exemple de valeurs de champ personnalisé générées dynamiquement.)

Ci-dessous, vous trouverez une capture d’écran de Visual Studio de l’arborescence d’objets d’application. Elle présente une extension de la table TSTimesheetLine avec le champ TestLineString ajouté en tant que champ personnalisé.

![Chaîne de ligne.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Utiliser la chaîne de commande sur la méthode buildCustomFieldList de la classe TSTimesheetSettings pour afficher un champ dans la section d’entrée de feuille de temps

Ce code contrôle les paramètres d’affichage du champ dans l’application. Par exemple, il contrôle le type de champ, l’étiquette, si le champ est obligatoire et dans quelle section le champ apparaît.

L’exemple suivant montre un champ de chaîne sur les entrées d’heure. Ce champ a deux options, **Première option** et **Deuxième option**, qui sont disponibles via les cases d’option. Le champ de l’application est associé au champ **TestLineString** qui est ajouté à la table TSTimesheetLine.

Notez l’utilisation de la méthode **TSTimesheetCustomField::newFromMetatdata()** pour simplifier l’initialisation des propriétés du champ personnalisé : **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** et **numberOfDecimals**. Vous pouvez également définir ces paramètres manuellement, selon vos préférences.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Utiliser la chaîne de commande sur la méthode buildCustomFieldListForEntry de la classe TSTimesheetEntry pour saisir des valeurs dans une entrée de feuille de temps

La méthode **buildCustomFieldListForEntry** est utilisée pour saisir des valeurs sur les lignes de feuille de temps enregistrées dans l’application mobile. Elle prend un enregistrement TSTimesheetTrans comme paramètre. Les champs de cet enregistrement peuvent être utilisés pour remplir la valeur du champ personnalisé dans l’application.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application dans la base de données

Pour enregistrer un champ personnalisé dans la base de données dans le cadre d’une utilisation normale, vous devez développer plusieurs méthodes :

- La méthode **timesheetLineNeedsUpdating** est utilisée pour déterminer si l’enregistrement de ligne a été modifié par l’utilisateur dans l’application et doit être enregistrée dans la base de données. Si les performances ne sont pas un problème, cette méthode peut être simplifiée afin de toujours renvoyer la valeur **true**.
- Les méthodes **populateTimesheetLineFromEntryDuringCreate** et **populateTimesheetLineFromEntryDuringUpdate** peuvent être développées afin de saisir des valeurs dans l’enregistrement de base de données TSTimesheetLine à partir de l’enregistrement de contrat de données TSTimesheetEntry fourni. Dans l’exemple suivant, notez comment le mappage entre le champ de base de données et le champ de saisie est effectué manuellement via le code X++.
- La méthode **populateTimesheetWeekFromEntry** peut être également développée si le champ personnalisé qui est mappé à l’objet **TSTimesheetEntry** doit répondre à la table de base de données TSTimesheetLineweek.

> [!NOTE]
> L’exemple suivant enregistre la valeur **firstOption** ou **secondOption** que l’utilisateur sélectionne dans la base de données en tant que valeur de chaîne brute. Si le champ de la base de données est un champ de type **Enum**, ces valeurs peuvent être mappées manuellement à une valeur d’énumération, puis enregistrées dans un champ d’énumération de la table de base de données.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Afficher un champ personnalisé dans la section d’en-tête de la feuille de temps

Vous trouverez ci-dessous une capture d’écran de l’application mobile d’un utilisateur affichant une feuille de temps. Le bouton « Autres informations » a été sélectionné dans l’angle supérieur droit pour afficher l’option « Afficher plus de détails ».  

![Commande Afficher plus de détails.](media/show-more.png)

Vous trouverez ci-dessous une capture d’écran de l’application mobile affichant la section « Plus » d’une feuille de temps. Un champ personnalisé appelé « Taux d’utilisation de cette feuille de temps (champ personnalisé calculé) » a été ajouté à la section d’en-tête de la feuille de temps. Une valeur en lecture seule de « 0,667 » est définie sur le champ personnalisé.

![Section Plus.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Développer la table TSTimesheetTable afin qu’elle ait un champ personnalisé

Dans les scénarios typiques, il est probable que les données d’un champ personnalisé dans la section d’entrée de feuille de temps soient enregistrées dans la table TSTimesheetHeader. Cependant, d’autres tables peuvent être utilisées si les données peuvent être récupérées en fonction d’un enregistrement TSTimesheetTable qui est fourni, ou s’il n’a pas de contexte d’enregistrement spécifique (par exemple, si le champ est défini en lecture seule dans les paramètres du projet).

Notez que les champs personnalisés n’ont pas besoin d’enregistrements de base de données de sauvegarde. Ils peuvent être générés dynamiquement en fonction de la logique X++. L’exemple qui suit montre cette approche.

Les champs de la section d’en-tête sont toujours en lecture seule dans l’application.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Utiliser la chaîne de commande sur la méthode buildCustomFieldList de la classe TSTimesheetSettings pour afficher un champ dans la section d’en-tête

Ce code contrôle les paramètres d’affichage du champ dans l’application. Par exemple, il contrôle le type de champ, l’étiquette, si le champ est obligatoire et dans quelle section le champ apparaît.

L’exemple suivant montre une valeur calculée dans la section d’en-tête de l’application.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Utiliser la chaîne de commande sur la méthode buildCustomFieldListForHeader de la classe TSTimesheetDetails pour renseigner les détails dans la feuille de temps

La méthode **buildCustomFieldListForHeader** est utilisée pour renseigner les détails de l’en-tête de la feuille de temps dans l’application mobile. Elle prend un enregistrement TSTimesheetTable comme paramètre. Les champs de cet enregistrement peuvent être utilisés pour remplir la valeur du champ personnalisé dans l’application. L’exemple suivant ne lit aucune valeur de la base de données. Il utilise plutôt la logique X++ pour générer une valeur calculée qui est ensuite affichée dans l’application.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Autres possibilités de configurabilité/extensibilité

### <a name="adding-additional-validation-for-the-app"></a>Ajout d’une validation supplémentaire pour l’application

La logique existante pour la fonctionnalité de feuille de temps au niveau de la base de données fonctionnera toujours comme prévu. Pour interrompre la fin des opérations d’enregistrement ou de soumission et afficher un message d’erreur spécifique, vous pouvez ajouter **throw error("message to user")** au code via une chaîne d’extension de commande. Voici trois exemples de méthodes extensibles utiles :

- Si **validateWrite** sur la table TSTimesheetLine renvoie **false** lors d’une opération de sauvegarde pour une ligne de feuille de temps, un message d’erreur s’affiche dans l’application mobile.
- Si **validateSubmit** sur la table TSTimesheetTable renvoie **false** lors de l’envoi d’une feuille de temps dans l’application, un message d’erreur s’affiche.
- La logique qui remplit les champs (par exemple, **Propriété de ligne**) pendant la méthode **insérer** sur la table TSTimesheetLine fonctionnera toujours.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Masquage et marquage des champs prêts à l’emploi en lecture seule via la configuration

À partir des paramètres du projet, vous pouvez rendre les champs prêts à l’emploi en lecture seule ou masqués dans l’application mobile. Définissez les options dans la section **Feuilles de temps mobiles** sur l’onglet **Feuille de temps** de la page **Paramètres de gestion de projets et de comptabilité**.

![Paramètres du projet.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Modifier les activités disponibles à la sélection via les extensions

Les activités pouvant être sélectionnées pour un projet sont renseignées via les méthodes **getActivitiesForProject()** et **getActivityQuery ()** dans la classe **TsTimesheetProjectService**. Vous pouvez utiliser la chaîne de commande pour modifier ce comportement afin qu’il corresponde à votre scénario d’entreprise pour les activités pouvant être sélectionnées pour un projet spécifique.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Saisie d’une catégorie de projet par défaut sur les entrées de feuille de temps

La saisie d’une catégorie de projet par défaut sur les entrées de feuille de temps se produit à trois niveaux. Vous pouvez utiliser la chaîne de commande pour étendre le comportement à l’un de ces niveaux ou à leur ensemble afin d’obtenir le comportement souhaité. La hiérarchie suivante est utilisée :

1. L’application tente de mettre la catégorie par défaut à partir de la ressource de projet. Cette catégorie par défaut est définie dans les méthodes **getCurrentUserResource** et **getDelegatedResourcesForCurrentUser** dans la classe **TSTimesheetSettingsService**.
2. Si la catégorie par défaut n’est pas fournie au niveau des ressources du projet, l’application essaie de l’extraire de l’activité du projet. Cette catégorie par défaut est définie dans la méthode **getActivitiesForProject** dans la classe **TSTimesheetProjectService**.
3. Si la catégorie par défaut n’est pas fournie au niveau des activités du projet, la catégorie par défaut est extraite des paramètres du projet. Cette catégorie par défaut est définie dans la méthode **getProjectDetailsbyRule** dans la classe **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]