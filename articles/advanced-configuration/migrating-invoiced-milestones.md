---
title: Migrer les jalons de facturation entièrement facturés lors du basculement
description: Cette rubrique explique comment migrer les jalons de facturation à prix fixe qui ont été facturés au client pour les contrats de projet ouverts avant la date de mise en service.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576267"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrer les jalons de facturation entièrement facturés lors du basculement

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

## <a name="scenario"></a>Scénario

Contoso est mis en ligne avec Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés. Dans le cadre des activités de basculement, l’équipe de mise en œuvre doit migrer les contrats de projet ouverts depuis l’ancien système. Certains des contrats de projet comportent des lignes de contrat qui utilisent le mode de facturation à prix fixe et qui ont déjà été partiellement facturées au client final. L’équipe de mise en œuvre doit migrer ces jalons de facturation en fonction de **Facture client validée**, car ils doivent être inclus dans la valeur totale du contrat à des fins de comptabilisation des produits. Cependant, les soldes des clients en comptabilité client et dans le grand livre ne doivent pas être affectés.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Conditions préalables

- Dynamics 365 Finance 10.0.24 ou version ultérieure doit être installé.
- L’environnement dans lequel les étapes de migration seront effectuées doit être en mode maintenance. Aucune autre activité ne doit être effectuée pendant la migration des jalons.
- Les étapes de migration doivent être suivies exactement comme décrit ici et ne peuvent être utilisées que pour l’activité de basculement. Microsoft ne prend en charge aucune autre utilisation de cette fonctionnalité.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Créer une version de basculement du mappage en double écriture des jalons de la ligne de contrat d’intégration de Project Operations 

1. Assurez-vous que le mappage cible pour l’entité **Jalons de la ligne de contrat d’intégration de Project Operations** est à jour. 

    1. Dans Finance, accédez à **Gestion de données** \> **Entités de données** et sélectionnez l’entité **Jalons de la ligne de contrat d’intégration de Project Operations**. 
    2. Sélectionnez **Modifier les mappages de la cible**. 
    3. Sur la page **Mettre en correspondance la phase intermédiaire avec la cible**, sélectionnez **Générer le mappage**, puis confirmez que vous souhaitez générer le mappage.

2. Arrêtez et actualisez le mappage en double écriture **Jalons de la ligne de contrat d’intégration de Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Accédez à **Gestion des données** \> **Double écriture**, sélectionnez le mappage et ouvrez ses détails. 
    2. Sélectionnez **Arrêter**, et attendez que le système arrête le mappage. 
    3. Sélectionnez **Actualiser les tables**.

3. Ajoutez un mappage pour le statut de la transaction.

    1. Sélectionnez **Ajouter un mappage**.
    2. Sur la nouvelle ligne, dans la colonne **Applications de finances et d’opérations**, sélectionnez le champ **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Dans la colonne **Microsoft Dataverse**, sélectionnez **msdyn\_invoicestatus\[Statut de la facture\]**.
    4. Dans la colonne **Type de mappage**, sélectionnez la flèche droite (**\>**).
    5. Dans la boîte de dialogue qui s’affiche, dans le champ **Sens de synchronisation**, sélectionnez **Dataverse vers les applications de finances et d’opérations**.
    6. Cliquez sur **Ajouter une transformation**.
    7. Dans le champ **Type de transformation**, sélectionnez **ValueMap**.
    8. Sélectionnez **Ajouter un mappage de valeurs**.
    9. Dans le champ de gauche, saisissez **4**. Dans le champ de droite, saisissez **192350001**. 
    10. Sélectionnez **Enregistrer**, puis fermez la boîte de dialogue.

4. Sélectionnez **Enregistrer sous** pour enregistrer la version du mappage en double écriture. 
5. Dans le volet **Ajouter une table**, dans le champ **Éditeur**, sélectionnez **Éditeur par défaut**.
6. Dans le champ **Version**, saisissez la version.
7. Dans le champ **Description**, saisissez une remarque sur cette version de basculement du mappage. 
8. Cliquez sur **Enregistrer**.
9. Démarrez le mappage.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrer les jalons facturés vers l’environnement Dataverse

1. Dans l’environnement Project Operations Dataverse, créez des jalons dont le statut de facture est **Prêt pour facturation**. À ce stade, ne migrez aucun jalon qui n’a pas été facturé.

    > [!NOTE]
    > Avant de migrer les jalons de facturation, assurez-vous que les dimensions financières associées à la ligne de contrat de projet sont définies comme prévu. Les dimensions financières ne peuvent pas être modifiées une fois la migration terminée.

2. Une fois tous les jalons migrés, arrêtez les mappages en double écriture suivants :

    - Jalons de la ligne de contrat d’intégration Project Operations (msdyn\_contractlinesscheduleofvalues)
    - Chiffres réels d’intégration Project Operations (msdyn\_actuals)
    - Proposition de facture de projet V2 (factures)

    Pour arrêter les mappages, procédez comme suit :

    1. Dans Finance, accédez à **Gestion des données** \> **Double écriture**, sélectionnez un mappage et ouvrez ses détails.
    2. Sélectionnez **Arrêter**, et attendez que le système arrête le mappage.

3. Dans l’environnement Project Operations Dataverse, créez et confirmez des factures pro forma pour les étapes de facturation. 

    1. Dans le plan du site, accédez aux contrats de projet, sélectionnez les contrats, puis **Créer des factures**.
    2. Une fois les factures créées, ouvrez-les à partir du menu **Factures** dans le plan du site, puis sélectionnez **Confirmer**.

    Cette étape crée les enregistrements requis dans l’environnement Dataverse. Cependant, cela n’affecte pas les finances et la comptabilité client, car les mappages en double écriture précédemment répertoriés ont été arrêtés.

4. Une fois toutes les factures pro forma confirmées, renvoyez tous les mappages en double écriture à leur état initial.

    1. Mettez à jour la version du mappage en double écriture **Jalons de la ligne de contrat d’intégration de Project Operations** (**msdyn\_contractlinescheduleofvalues**) avec sa version d’origine. 
    2. Sélectionnez le mappage en double écriture dans la liste des mappages, puis sélectionnez **Version du mappage de table**, et enfin sélectionnez la version d’origine du mappage de table.
    3. Cliquez sur **Enregistrer**.
    4. Redémarrez les mappages en double écriture suivants :

        - Jalons de la ligne de contrat d’intégration Project Operations (msdyn\_contractlinesscheduleofvalues)
        - Chiffres réels d’intégration Project Operations (msdyn\_actuals)
        - Proposition de facture de projet V2 (factures)

Les jalons sont maintenant migrés et le système est prêt pour les prochaines étapes de l’activité de basculement.
