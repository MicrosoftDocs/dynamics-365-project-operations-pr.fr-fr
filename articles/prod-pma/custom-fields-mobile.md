---
title: Implémenter des champs personnalisés pour l’application mobile Microsoft Dynamics 365 Project Timesheet sur iOS et Android
description: Cette rubrique offre des modèles courants pour utiliser les extensions en vue d’implémenter les champs personnalisés.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270990"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="aef7f-103">Implémenter des champs personnalisés pour l’application mobile Microsoft Dynamics 365 Project Timesheet sur iOS et Android</span><span class="sxs-lookup"><span data-stu-id="aef7f-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aef7f-104">Cette rubrique offre des modèles courants pour utiliser les extensions en vue d’implémenter les champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="aef7f-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="aef7f-105">Les rubriques suivantes sont abordées :</span><span class="sxs-lookup"><span data-stu-id="aef7f-105">The following topics are covered:</span></span>

- <span data-ttu-id="aef7f-106">Les différents types de données compatibles avec la structure de champs personnalisés</span><span class="sxs-lookup"><span data-stu-id="aef7f-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="aef7f-107">Procédure d’affichage des champs en lecture seule ou modifiables sur les entrées de feuille de temps et d’enregistrement des valeurs fournies par l’utilisateur dans la base de données</span><span class="sxs-lookup"><span data-stu-id="aef7f-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="aef7f-108">Procédure d’affichage des champs en lecture seule sur l’en-tête de la feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="aef7f-109">Procédure d’intégration d’une autre logique métier personnalisée pour saisir des valeurs par défaut dans les champs et de validation supplémentaire</span><span class="sxs-lookup"><span data-stu-id="aef7f-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="aef7f-110">Audience</span><span class="sxs-lookup"><span data-stu-id="aef7f-110">Audience</span></span>

<span data-ttu-id="aef7f-111">Cette rubrique est destinée aux développeurs qui intègrent leurs champs personnalisés dans l’application mobile Microsoft Dynamics 365 Project Timesheet disponible pour Apple iOS et Google Android.</span><span class="sxs-lookup"><span data-stu-id="aef7f-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="aef7f-112">Supposons que les lecteurs connaissent bien le développement X++ et la fonctionnalité de feuille de temps de projet.</span><span class="sxs-lookup"><span data-stu-id="aef7f-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="aef7f-113">Contrat de données - Classe TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="aef7f-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="aef7f-114">La classe **TSTimesheetCustomField** correspond à la classe de contrat de données X++ qui représente des informations sur un champ personnalisé pour la fonctionnalité de feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="aef7f-115">Les listes des objets de champ personnalisé sont transmises à la fois au contrat de données TSTimesheetDetails et au contrat de données TSTimesheetEntry pour afficher les champs personnalisés dans l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="aef7f-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="aef7f-116">**TSTimesheetDetails** : contrat d’en-tête de la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="aef7f-117">**TSTimesheetEntry**  contrat de transaction de la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="aef7f-118">Les groupes de ces objets, avec les mêmes informations de projet et la valeur **timesheetLineRecId**, constituent une ligne.</span><span class="sxs-lookup"><span data-stu-id="aef7f-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="aef7f-119">fieldBaseType (types)</span><span class="sxs-lookup"><span data-stu-id="aef7f-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="aef7f-120">La propriété **FieldBaseType** sur l’objet **TsTimesheetCustom** détermine le type de champ qui apparaît dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="aef7f-121">Les valeurs **Types** suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="aef7f-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="aef7f-122">Valeur de types</span><span class="sxs-lookup"><span data-stu-id="aef7f-122">Types value</span></span> | <span data-ttu-id="aef7f-123">Type</span><span class="sxs-lookup"><span data-stu-id="aef7f-123">Type</span></span>              | <span data-ttu-id="aef7f-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="aef7f-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="aef7f-125">0</span><span class="sxs-lookup"><span data-stu-id="aef7f-125">0</span></span>           | <span data-ttu-id="aef7f-126">Chaîne (et énumération)</span><span class="sxs-lookup"><span data-stu-id="aef7f-126">String (and Enum)</span></span> | <span data-ttu-id="aef7f-127">Le champ apparaît comme un champ de texte.</span><span class="sxs-lookup"><span data-stu-id="aef7f-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="aef7f-128">1</span><span class="sxs-lookup"><span data-stu-id="aef7f-128">1</span></span>           | <span data-ttu-id="aef7f-129">Integer</span><span class="sxs-lookup"><span data-stu-id="aef7f-129">Integer</span></span>           | <span data-ttu-id="aef7f-130">La valeur est affichée sous forme d’un nombre sans décimales.</span><span class="sxs-lookup"><span data-stu-id="aef7f-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="aef7f-131">2</span><span class="sxs-lookup"><span data-stu-id="aef7f-131">2</span></span>           | <span data-ttu-id="aef7f-132">Réel</span><span class="sxs-lookup"><span data-stu-id="aef7f-132">Real</span></span>              | <span data-ttu-id="aef7f-133">La valeur est affichée sous forme de nombre avec des décimales.</span><span class="sxs-lookup"><span data-stu-id="aef7f-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="aef7f-134">Pour afficher la valeur réelle en tant que devise dans l’application, utilisez la propriété **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="aef7f-135">Vous pouvez utiliser la propriété **numberOfDecimals** pour définir le nombre de décimales affichées.</span><span class="sxs-lookup"><span data-stu-id="aef7f-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="aef7f-136">3</span><span class="sxs-lookup"><span data-stu-id="aef7f-136">3</span></span>           | <span data-ttu-id="aef7f-137">Date</span><span class="sxs-lookup"><span data-stu-id="aef7f-137">Date</span></span>              | <span data-ttu-id="aef7f-138">Les formats de date sont déterminés par le paramètre d’utilisateur **Format de date, d’heure et de nombre** précisé sous **Préférence de langue et pays/région** dans **Options d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="aef7f-139">4</span><span class="sxs-lookup"><span data-stu-id="aef7f-139">4</span></span>           | <span data-ttu-id="aef7f-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="aef7f-140">Boolean</span></span>           | |
| <span data-ttu-id="aef7f-141">15</span><span class="sxs-lookup"><span data-stu-id="aef7f-141">15</span></span>          | <span data-ttu-id="aef7f-142">GUID</span><span class="sxs-lookup"><span data-stu-id="aef7f-142">GUID</span></span>              | |
| <span data-ttu-id="aef7f-143">16</span><span class="sxs-lookup"><span data-stu-id="aef7f-143">16</span></span>          | <span data-ttu-id="aef7f-144">Int64</span><span class="sxs-lookup"><span data-stu-id="aef7f-144">Int64</span></span>             | |

- <span data-ttu-id="aef7f-145">Si la propriété **stringOptions** n’est pas fournie sur l’objet **TSTimesheetCustomField**, un champ de texte libre est fourni à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aef7f-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="aef7f-146">La propriété **stringLength** peut être utilisée pour définir la longueur de chaîne maximale que les utilisateurs peuvent saisir.</span><span class="sxs-lookup"><span data-stu-id="aef7f-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="aef7f-147">Si la propriété **stringOptions** est fournie sur l’objet **TSTimesheetCustomField**, ces éléments de liste sont les seules valeurs que les utilisateurs peuvent sélectionner à l’aide des boutons d’option.</span><span class="sxs-lookup"><span data-stu-id="aef7f-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="aef7f-148">Dans ce cas, le champ de chaîne peut agir comme une valeur d’énumération à des fins de saisie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aef7f-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="aef7f-149">Pour enregistrer la valeur dans la base de données en tant qu’énumération, mappez manuellement la valeur de chaîne vers la valeur d’énumération avant de procéder à l’enregistrement dans la base de données à l’aide d’une chaîne de commande (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application vers la base de données » ultérieurement dans cette rubrique pour un exemple).</span><span class="sxs-lookup"><span data-stu-id="aef7f-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="aef7f-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="aef7f-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="aef7f-151">Vous pouvez utiliser cette propriété pour mettre en forme des valeurs réelles en tant que devise.</span><span class="sxs-lookup"><span data-stu-id="aef7f-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="aef7f-152">Cette approche n’est applicable que lorsque la valeur **fieldBaseType** est définie sur **Réel**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="aef7f-153">**TSCustomFieldExtendedType:None**: aucune mise en forme n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="aef7f-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="aef7f-154">**TSCustomFieldExtendedType::Currency** : formater la valeur en tant que devise.</span><span class="sxs-lookup"><span data-stu-id="aef7f-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="aef7f-155">Lorsque le formatage de la devise est actif, le champ **stringValue** peut être utilisé pour passer le code devise qui doit être affiché dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="aef7f-156">La valeur est une valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aef7f-156">The value is a read-only value.</span></span>

    <span data-ttu-id="aef7f-157">Le champ **realValue** contient la somme d’argent qui doit être enregistrée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="aef7f-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="aef7f-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="aef7f-159">Vous pouvez utiliser cette propriété pour spécifier l’emplacement du champ personnalisé dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="aef7f-160">**TSCustomFieldSection ::Header** : le champ apparaît dans la section **Afficher plus de détails** dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="aef7f-161">Ces champs sont toujours en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aef7f-161">These fields are always read-only.</span></span>
- <span data-ttu-id="aef7f-162">**TSCustomFieldSection::Line** : le champ apparaît après tous les champs de ligne prêts à l’emploi sur les entrées de feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="aef7f-163">Ces champs peuvent être modifiables ou en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aef7f-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="aef7f-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="aef7f-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="aef7f-165">Cette propriété identifie le champ lorsque les valeurs fournies par l’application sont enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="aef7f-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="aef7f-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="aef7f-167">Cette propriété identifie le champ lorsque les valeurs fournies par l’application sont enregistrées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="aef7f-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="aef7f-168">isEditable (NoYes)</span></span>

<span data-ttu-id="aef7f-169">Définissez cette propriété sur **Oui** pour spécifier que le champ de la section d’entrée de la feuille de temps doit être modifiable par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="aef7f-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="aef7f-170">Définissez la propriété sur **Non** pour rendre le champ en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aef7f-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="aef7f-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="aef7f-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="aef7f-172">Définissez cette propriété sur **Oui** pour indiquer que le champ de la section d’entrée de la feuille de temps est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="aef7f-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="aef7f-173">étiquette (chaîne)</span><span class="sxs-lookup"><span data-stu-id="aef7f-173">label (str)</span></span>

<span data-ttu-id="aef7f-174">Cette propriété spécifie l’étiquette affichée à côté du champ dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="aef7f-175">stringOptions (liste des chaînes)</span><span class="sxs-lookup"><span data-stu-id="aef7f-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="aef7f-176">Cette propriété est applicable uniquement lorsque **fieldBaseType** est réglé sur **Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="aef7f-177">Si **stringOptions** est défini, les valeurs de chaîne disponibles pour la sélection via les boutons d’option sont spécifiées par les chaînes de la liste.</span><span class="sxs-lookup"><span data-stu-id="aef7f-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="aef7f-178">Si aucune chaîne n’est fournie, l’entrée de texte libre dans le champ de chaîne est autorisée (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application dans la base de données » ultérieurement dans cette rubrique pour un exemple).</span><span class="sxs-lookup"><span data-stu-id="aef7f-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="aef7f-179">stringLength (entier)</span><span class="sxs-lookup"><span data-stu-id="aef7f-179">stringLength (int)</span></span>

<span data-ttu-id="aef7f-180">Cette propriété spécifie la longueur maximale d’un champ de chaîne.</span><span class="sxs-lookup"><span data-stu-id="aef7f-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="aef7f-181">Elle est applicable uniquement lorsque **fieldBaseType** est réglé sur **Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="aef7f-182">numberOfDecimals (entier)</span><span class="sxs-lookup"><span data-stu-id="aef7f-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="aef7f-183">Cette propriété spécifie le nombre de décimales affichées pour un champ réel.</span><span class="sxs-lookup"><span data-stu-id="aef7f-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="aef7f-184">Elle est applicable uniquement lorsque le champ **fieldBaseType** est défini sur **Réel**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="aef7f-185">orderSequence (entier)</span><span class="sxs-lookup"><span data-stu-id="aef7f-185">orderSequence (int)</span></span>

<span data-ttu-id="aef7f-186">Cette propriété contrôle l’ordre dans lequel les champs personnalisés sont affichés dans l’application lorsque plusieurs champs personnalisés sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="aef7f-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="aef7f-187">Les champs avec des nombres inférieurs apparaissent en premier.</span><span class="sxs-lookup"><span data-stu-id="aef7f-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="aef7f-188">booleanValue (booléen)</span><span class="sxs-lookup"><span data-stu-id="aef7f-188">booleanValue (boolean)</span></span>

<span data-ttu-id="aef7f-189">Pour les domaines de type **Booléen**, cette propriété transmet la valeur booléenne du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="aef7f-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="aef7f-190">guidValue (guid)</span></span>

<span data-ttu-id="aef7f-191">Pour les domaines de type **GUID**, cette propriété transmet la valeur GUID (identificateur global unique) du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="aef7f-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="aef7f-192">int64Value (int64)</span></span>

<span data-ttu-id="aef7f-193">Pour les domaines de type **Int64**, cette propriété transmet la valeur int64 du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="aef7f-194">intValue (entier)</span><span class="sxs-lookup"><span data-stu-id="aef7f-194">intValue (int)</span></span>

<span data-ttu-id="aef7f-195">Pour les champs de type **Entier**, cette propriété transmet la valeur entier du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="aef7f-196">realValue (réel)</span><span class="sxs-lookup"><span data-stu-id="aef7f-196">realValue (real)</span></span>

<span data-ttu-id="aef7f-197">Pour les champs de type **Réel**, cette propriété transmet la valeur réel du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="aef7f-198">stringValue (chaîne)</span><span class="sxs-lookup"><span data-stu-id="aef7f-198">stringValue (str)</span></span>

<span data-ttu-id="aef7f-199">Pour les champs de type **Chaîne**, cette propriété transmet la valeur chaîne du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="aef7f-200">Il est également utilisé pour les champs de type **Réel** qui est formaté comme devise.</span><span class="sxs-lookup"><span data-stu-id="aef7f-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="aef7f-201">Pour ces champs, la propriété est utilisée pour transmettre le code de devise à l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="aef7f-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="aef7f-202">dateValue (date)</span></span>

<span data-ttu-id="aef7f-203">Pour les champs de type **Date**, cette propriété transmet la valeur date du champ entre le serveur et l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="aef7f-204">Afficher et enregistrer un champ personnalisé dans la section d’entrée de la feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="aef7f-205">Vous trouverez ci-dessous une capture d’écran de l’application mobile d’une création d’entrée de feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="aef7f-206">Elle présente les champs prêts à l’emploi et un champ personnalisé dans la section « Entrée de temps » appelée « Chaîne de test » avec une valeur d’énumération « Deuxième option » déjà définie.</span><span class="sxs-lookup"><span data-stu-id="aef7f-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Champ personnalisé de la chaîne de test dans l’application](media/timesheet-entry.jpg)



<span data-ttu-id="aef7f-208">Vous trouverez ci-dessous une capture d’écran de l’application mobile de l’utilisateur sélectionnant l’une des options d’énumération disponibles pour le champ personnalisé « Chaîne de test ».</span><span class="sxs-lookup"><span data-stu-id="aef7f-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="aef7f-209">Les deux options sont « Première option » et « Deuxième option » affichées sous forme de case d’option.</span><span class="sxs-lookup"><span data-stu-id="aef7f-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="aef7f-210">La deuxième option est actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="aef7f-210">The second option is currently selected.</span></span>

![Cases d’option pour le champ personnalisé Chaîne de test](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="aef7f-212">Développer la table TSTimesheetLine afin qu’elle ait un champ personnalisé</span><span class="sxs-lookup"><span data-stu-id="aef7f-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="aef7f-213">Dans les scénarios types, il est probable que les données d’un champ personnalisé dans la section d’entrée de feuille de temps soient enregistrées dans la table TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="aef7f-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="aef7f-214">Cependant, d’autres tables peuvent être utilisées si les données peuvent être récupérées en fonction d’un enregistrement TSTimesheetTrans fourni, ou si elles n’ont pas de contexte d’enregistrement spécifique (par exemple, si le champ est défini en lecture seule dans les paramètres du projet).</span><span class="sxs-lookup"><span data-stu-id="aef7f-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="aef7f-215">Notez que les champs personnalisés n’ont pas besoin d’enregistrements de base de données de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="aef7f-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="aef7f-216">Ils peuvent être générés dynamiquement en fonction de la logique X++.</span><span class="sxs-lookup"><span data-stu-id="aef7f-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="aef7f-217">Cette approche peut être utile dans les scénarios en lecture seule (voir la section « Utiliser la chaîne de commande sur la classe TSTimesheetDetails, méthode buildCustomFieldListForHeader pour renseigner les détails de la feuille de temps » pour un exemple de valeurs de champ personnalisé générées dynamiquement.)</span><span class="sxs-lookup"><span data-stu-id="aef7f-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="aef7f-218">Ci-dessous, vous trouverez une capture d’écran de Visual Studio de l’arborescence d’objets d’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="aef7f-219">Elle présente une extension de la table TSTimesheetLine avec le champ TestLineString ajouté en tant que champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="aef7f-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Chaîne de ligne](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="aef7f-221">Utiliser la chaîne de commande sur la méthode buildCustomFieldList de la classe TSTimesheetSettings pour afficher un champ dans la section d’entrée de feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="aef7f-222">Ce code contrôle les paramètres d’affichage du champ dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="aef7f-223">Par exemple, il contrôle le type de champ, l’étiquette, si le champ est obligatoire et dans quelle section le champ apparaît.</span><span class="sxs-lookup"><span data-stu-id="aef7f-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="aef7f-224">L’exemple suivant montre un champ de chaîne sur les entrées d’heure.</span><span class="sxs-lookup"><span data-stu-id="aef7f-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="aef7f-225">Ce champ a deux options, **Première option** et **Deuxième option**, qui sont disponibles via les cases d’option.</span><span class="sxs-lookup"><span data-stu-id="aef7f-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="aef7f-226">Le champ de l’application est associé au champ **TestLineString** qui est ajouté à la table TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="aef7f-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="aef7f-227">Notez l’utilisation de la méthode **TSTimesheetCustomField::newFromMetatdata()** pour simplifier l’initialisation des propriétés du champ personnalisé : **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** et **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="aef7f-228">Vous pouvez également définir ces paramètres manuellement, selon vos préférences.</span><span class="sxs-lookup"><span data-stu-id="aef7f-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="aef7f-229">Utiliser la chaîne de commande sur la méthode buildCustomFieldListForEntry de la classe TSTimesheetEntry pour saisir des valeurs dans une entrée de feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="aef7f-230">La méthode **buildCustomFieldListForEntry** est utilisée pour saisir des valeurs sur les lignes de feuille de temps enregistrées dans l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="aef7f-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="aef7f-231">Elle prend un enregistrement TSTimesheetTrans comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="aef7f-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="aef7f-232">Les champs de cet enregistrement peuvent être utilisés pour remplir la valeur du champ personnalisé dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="aef7f-233">Utiliser la chaîne de commande sur la classe TSTimesheetEntryService pour enregistrer une entrée de feuille de temps de l’application dans la base de données</span><span class="sxs-lookup"><span data-stu-id="aef7f-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="aef7f-234">Pour enregistrer un champ personnalisé dans la base de données dans le cadre d’une utilisation normale, vous devez développer plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="aef7f-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="aef7f-235">La méthode **timesheetLineNeedsUpdating** est utilisée pour déterminer si l’enregistrement de ligne a été modifié par l’utilisateur dans l’application et doit être enregistrée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="aef7f-236">Si les performances ne sont pas un problème, cette méthode peut être simplifiée afin de toujours renvoyer la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="aef7f-237">Les méthodes **populateTimesheetLineFromEntryDuringCreate** et **populateTimesheetLineFromEntryDuringUpdate** peuvent être développées afin de saisir des valeurs dans l’enregistrement de base de données TSTimesheetLine à partir de l’enregistrement de contrat de données TSTimesheetEntry fourni.</span><span class="sxs-lookup"><span data-stu-id="aef7f-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="aef7f-238">Dans l’exemple suivant, notez comment le mappage entre le champ de base de données et le champ de saisie est effectué manuellement via le code X++.</span><span class="sxs-lookup"><span data-stu-id="aef7f-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="aef7f-239">La méthode **populateTimesheetWeekFromEntry** peut être également développée si le champ personnalisé qui est mappé à l’objet **TSTimesheetEntry** doit répondre à la table de base de données TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="aef7f-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="aef7f-240">L’exemple suivant enregistre la valeur **firstOption** ou **secondOption** que l’utilisateur sélectionne dans la base de données en tant que valeur de chaîne brute.</span><span class="sxs-lookup"><span data-stu-id="aef7f-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="aef7f-241">Si le champ de la base de données est un champ de type **Enum**, ces valeurs peuvent être mappées manuellement à une valeur d’énumération, puis enregistrées dans un champ d’énumération de la table de base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="aef7f-242">Afficher un champ personnalisé dans la section d’en-tête de la feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="aef7f-243">Vous trouverez ci-dessous une capture d’écran de l’application mobile d’un utilisateur affichant une feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="aef7f-244">Le bouton « Autres informations » a été sélectionné dans l’angle supérieur droit pour afficher l’option « Afficher plus de détails ».</span><span class="sxs-lookup"><span data-stu-id="aef7f-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Commande Afficher plus de détails](media/show-more.png)

<span data-ttu-id="aef7f-246">Vous trouverez ci-dessous une capture d’écran de l’application mobile affichant la section « Plus » d’une feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="aef7f-247">Un champ personnalisé appelé « Taux d’utilisation de cette feuille de temps (champ personnalisé calculé) » a été ajouté à la section d’en-tête de la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="aef7f-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="aef7f-248">Une valeur en lecture seule de « 0,667 » est définie sur le champ personnalisé.</span><span class="sxs-lookup"><span data-stu-id="aef7f-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Section Plus](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="aef7f-250">Développer la table TSTimesheetTable afin qu’elle ait un champ personnalisé</span><span class="sxs-lookup"><span data-stu-id="aef7f-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="aef7f-251">Dans les scénarios typiques, il est probable que les données d’un champ personnalisé dans la section d’entrée de feuille de temps soient enregistrées dans la table TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="aef7f-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="aef7f-252">Cependant, d’autres tables peuvent être utilisées si les données peuvent être récupérées en fonction d’un enregistrement TSTimesheetTable qui est fourni, ou s’il n’a pas de contexte d’enregistrement spécifique (par exemple, si le champ est défini en lecture seule dans les paramètres du projet).</span><span class="sxs-lookup"><span data-stu-id="aef7f-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="aef7f-253">Notez que les champs personnalisés n’ont pas besoin d’enregistrements de base de données de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="aef7f-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="aef7f-254">Ils peuvent être générés dynamiquement en fonction de la logique X++.</span><span class="sxs-lookup"><span data-stu-id="aef7f-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="aef7f-255">L’exemple qui suit montre cette approche.</span><span class="sxs-lookup"><span data-stu-id="aef7f-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="aef7f-256">Les champs de la section d’en-tête sont toujours en lecture seule dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="aef7f-257">Utiliser la chaîne de commande sur la méthode buildCustomFieldList de la classe TSTimesheetSettings pour afficher un champ dans la section d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aef7f-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="aef7f-258">Ce code contrôle les paramètres d’affichage du champ dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="aef7f-259">Par exemple, il contrôle le type de champ, l’étiquette, si le champ est obligatoire et dans quelle section le champ apparaît.</span><span class="sxs-lookup"><span data-stu-id="aef7f-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="aef7f-260">L’exemple suivant montre une valeur calculée dans la section d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="aef7f-261">Utiliser la chaîne de commande sur la méthode buildCustomFieldListForHeader de la classe TSTimesheetDetails pour renseigner les détails dans la feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="aef7f-262">La méthode **buildCustomFieldListForHeader** est utilisée pour renseigner les détails de l’en-tête de la feuille de temps dans l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="aef7f-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="aef7f-263">Elle prend un enregistrement TSTimesheetTable comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="aef7f-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="aef7f-264">Les champs de cet enregistrement peuvent être utilisés pour remplir la valeur du champ personnalisé dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="aef7f-265">L’exemple suivant ne lit aucune valeur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="aef7f-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="aef7f-266">Il utilise plutôt la logique X++ pour générer une valeur calculée qui est ensuite affichée dans l’application.</span><span class="sxs-lookup"><span data-stu-id="aef7f-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="aef7f-267">Autres possibilités de configurabilité/extensibilité</span><span class="sxs-lookup"><span data-stu-id="aef7f-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="aef7f-268">Ajout d’une validation supplémentaire pour l’application</span><span class="sxs-lookup"><span data-stu-id="aef7f-268">Adding additional validation for the app</span></span>

<span data-ttu-id="aef7f-269">La logique existante pour la fonctionnalité de feuille de temps au niveau de la base de données fonctionnera toujours comme prévu.</span><span class="sxs-lookup"><span data-stu-id="aef7f-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="aef7f-270">Pour interrompre la fin des opérations d’enregistrement ou de soumission et afficher un message d’erreur spécifique, vous pouvez ajouter **throw error("message to user")** au code via une chaîne d’extension de commande.</span><span class="sxs-lookup"><span data-stu-id="aef7f-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="aef7f-271">Voici trois exemples de méthodes extensibles utiles :</span><span class="sxs-lookup"><span data-stu-id="aef7f-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="aef7f-272">Si **validateWrite** sur la table TSTimesheetLine renvoie **false** lors d’une opération de sauvegarde pour une ligne de feuille de temps, un message d’erreur s’affiche dans l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="aef7f-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="aef7f-273">Si **validateSubmit** sur la table TSTimesheetTable renvoie **false** lors de l’envoi d’une feuille de temps dans l’application, un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="aef7f-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="aef7f-274">La logique qui remplit les champs (par exemple, **Propriété de ligne**) pendant la méthode **insérer** sur la table TSTimesheetLine fonctionnera toujours.</span><span class="sxs-lookup"><span data-stu-id="aef7f-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="aef7f-275">Masquage et marquage des champs prêts à l’emploi en lecture seule via la configuration</span><span class="sxs-lookup"><span data-stu-id="aef7f-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="aef7f-276">À partir des paramètres du projet, vous pouvez rendre les champs prêts à l’emploi en lecture seule ou masqués dans l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="aef7f-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="aef7f-277">Définissez les options dans la section **Feuilles de temps mobiles** sur l’onglet **Feuille de temps** de la page **Paramètres de gestion de projets et de comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Paramètres du projet](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="aef7f-279">Modifier les activités disponibles à la sélection via les extensions</span><span class="sxs-lookup"><span data-stu-id="aef7f-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="aef7f-280">Les activités pouvant être sélectionnées pour un projet sont renseignées via les méthodes **getActivitiesForProject()** et **getActivityQuery ()** dans la classe **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="aef7f-281">Vous pouvez utiliser la chaîne de commande pour modifier ce comportement afin qu’il corresponde à votre scénario d’entreprise pour les activités pouvant être sélectionnées pour un projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="aef7f-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="aef7f-282">Saisie d’une catégorie de projet par défaut sur les entrées de feuille de temps</span><span class="sxs-lookup"><span data-stu-id="aef7f-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="aef7f-283">La saisie d’une catégorie de projet par défaut sur les entrées de feuille de temps se produit à trois niveaux.</span><span class="sxs-lookup"><span data-stu-id="aef7f-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="aef7f-284">Vous pouvez utiliser la chaîne de commande pour étendre le comportement à l’un de ces niveaux ou à leur ensemble afin d’obtenir le comportement souhaité.</span><span class="sxs-lookup"><span data-stu-id="aef7f-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="aef7f-285">La hiérarchie suivante est utilisée :</span><span class="sxs-lookup"><span data-stu-id="aef7f-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="aef7f-286">L’application tente de mettre la catégorie par défaut à partir de la ressource de projet.</span><span class="sxs-lookup"><span data-stu-id="aef7f-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="aef7f-287">Cette catégorie par défaut est définie dans les méthodes **getCurrentUserResource** et **getDelegatedResourcesForCurrentUser** dans la classe **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="aef7f-288">Si la catégorie par défaut n’est pas fournie au niveau des ressources du projet, l’application essaie de l’extraire de l’activité du projet.</span><span class="sxs-lookup"><span data-stu-id="aef7f-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="aef7f-289">Cette catégorie par défaut est définie dans la méthode **getActivitiesForProject** dans la classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="aef7f-290">Si la catégorie par défaut n’est pas fournie au niveau des activités du projet, la catégorie par défaut est extraite des paramètres du projet.</span><span class="sxs-lookup"><span data-stu-id="aef7f-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="aef7f-291">Cette catégorie par défaut est définie dans la méthode **getProjectDetailsbyRule** dans la classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="aef7f-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]