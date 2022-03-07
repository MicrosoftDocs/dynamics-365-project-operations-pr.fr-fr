---
title: Intégration des estimations et des chiffres réels de projet
description: Cette rubrique fournit des informations sur l’intégration en double écriture de Project Operations pour les estimations et les chiffres réels de projet.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000028"
---
# <a name="project-estimates-and-actuals-integration"></a>Intégration des estimations et des chiffres réels de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique fournit des informations sur l’intégration en double écriture de Project Operations pour les estimations et les chiffres réels de projet.

## <a name="project-estimates"></a>Estimations de projets

Les estimations de main-d’œuvre, de dépenses et de matériel du projet sont créées et gérées dans Microsoft Dataverse, et synchronisées avec les applications Finance and Operations à des fins comptables. Les opérations de création, de mise à jour et de suppression ne sont pas prises en charge via les applications Finance and Operations.

La création d’estimations nécessite une configuration comptable valide pour le projet. Les projets associés à des lignes de contrat doivent avoir un profil de coût et de produit de projet valide, défini dans les règles de profil de coût et de produit du projet. Pour plus d’informations, consultez [Configurer la comptabilité des projets facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimations de main-d’œuvre

Les estimations de main-d’œuvre sont créées par le gestionnaire de projet ou le gestionnaire de ressources qui affecte également une ressource générique ou nommée à la tâche de projet. Les enregistrements d’affectations de ressources peuvent être consultés sur l’onglet **Affectations de ressources**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’affectations de ressources dans Dataverse créent des enregistrements de prévisions en heures dans les applications Finance and Operations à l’aide de l’**entité d’intégration Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**.

   ![Intégration des estimations de main-d’œuvre](./Media/DW4LaborEstimates.png)

La double écriture synchronise les enregistrements d’affectations de ressources avec la table intermédiaire (**ProjCDSEstimateHoursImport**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions en heures (**ProjForecastEmpl**).

Le comptable de projet examine les enregistrements d’heures prévues créés dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Planifier** > **Prévisions en heures**.

## <a name="expense-estimates"></a>Estimations de dépenses

Les estimations de dépenses sont créées par le gestionnaire de projet sur l’onglet **Estimations des dépenses**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’estimations des dépenses sont stockés dans l’entité **Ligne d’estimation** dans Dataverse. Ces enregistrements d’estimations ont une classe de transaction, **Dépense** et sont synchronisés avec les enregistrements de prévisions de dépenses dans les applications Finance and Operations à l’aide de l’**entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimatelines)**.

   ![Intégration des estimations de dépenses](./Media/DW4ExpenseEstimates.png)

La double écriture synchronise les enregistrements d’estimations des dépenses avec la table intermédiaire (**ProjCDSEstimateExpenseImport**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions des dépenses (**ProjForecastCost**). Les lignes d’estimations stockent les enregistrements d’estimation des ventes et d’estimation des coûts séparément. La logique métier dans les applications Finance and Operations remplit un seul enregistrement de prévisions des dépenses en utilisant ce détail dans la table intermédiaire.

Le comptable de projet peut examiner les enregistrements de prévisions des dépenses créés dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Planifier** > **Prévisions des dépenses**.

## <a name="material-estimates"></a>Estimations du matériel

Les estimations du matériel sont créées par le gestionnaire de projet sur l’onglet **Estimations du matériel**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’estimation du matériel sont stockés dans l’entité **Ligne d’estimation** dans Dataverse. Ces enregistrements d’estimation ont une classe de transaction, **Matériel** et sont synchronisés avec les enregistrements de prévisions d’articles dans les applications Finance and Operations à l’aide de la **table d’intégration de Project Operations pour les estimations du matériel (msdyn\_estimatelines)**.

   ![Intégration des estimations du matériel](./Media/DW4MaterialEstimates.png)

La double écriture synchronise les enregistrements d’estimations du matériel avec la table intermédiaire (**ProjForecastSalesImpor**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions d’articles (**ForecastSales**). Les lignes d’estimations stockent les enregistrements d’estimation des ventes et d’estimation des coûts séparément. La logique métier dans les applications Finance and Operations remplit un seul enregistrement de prévisions d’articles en utilisant ce détail dans la table intermédiaire.

Le comptable de projet peut examiner les enregistrements de prévisions d’articles créés dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Planifier** > **Prévisions d’articles**.

## <a name="project-actuals"></a>Chiffres réels du projet

Les chiffres réels du projet sont créés dans Dataverse, en fonction du temps, des dépenses, du matériel et de l’activité de facturation. Tous les attributs opérationnels de ces transactions, y compris la quantité, le prix de revient, le prix de vente et le projet, sont capturés dans cette entité Dataverse. Pour plus d’informations, voir [Chiffres réels](../actuals/actuals-overview.md). Les enregistrements des chiffres réels sont synchronisés avec les applications Finance and Operations à l’aide du mappage de table à double écriture **Chiffres réels d’intégration de Project Operations (msdyn\_actuals)** pour la comptabilité en aval.

   ![Intégration des chiffres réels](./Media/DW4Actuals.png)

Le mappage de table **Chiffres réels d’intégration de Project Operations** synchronise tous les enregistrements de l’entité **Chiffres réels** dans Dataverse, avec l’attribut **Ignorer la synchronisation (usage interne uniquement)** défini sur **Faux**. Cette valeur d’attribut est définie dans Dataverse automatiquement lors de la création de l’enregistrement. Voici des exemples où cet attribut est défini sur **Vrai** :

  - Chiffres réels du coût du projet pour les transactions intersociétés. Pour plus d’informations, voir [Créer des transactions intersociétés](../project-accounting/create-intercompany-transactions.md). Ces enregistrements sont ignorés car le système recrée les chiffres réels du coût du projet dans les applications Finance and Operations lorsque la facture fournisseur intersociétés est validée.
  - Enregistrements de ventes non facturées négatifs créés lors de la confirmation de la facture pro forma. Ces enregistrements sont ignorés car la comptabilité auxiliaire du projet dans les applications Finance and Operations n’inverse pas les enregistrements des ventes non facturées lors de la facturation, mais remplace le statut par entièrement facturé.

Le mappage de table à double écriture synchronise les enregistrements des chiffres réels avec la table intermédiaire, **ProjCDSActualsImport**. Ces enregistrements sont traités par le processus périodique **Importer depuis la table intermédiaire** lors de la création de lignes de journal d’intégration de Project Operations et de lignes de proposition de facture de projet. Pour plus d’informations, voir [Feuille intégration dans Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse capture également les liens entre les transactions réelles du projet dans l’entité **Connexion de la transaction**. Pour plus d’informations, voir [Lier les chiffres réels aux enregistrements originaux](../actuals/linkingactuals.md). Les liens entre les transactions réelles sont également synchronisés avec les applications Finance and Operations à l’aide du mappage de table à double écriture, **Entité d’intégration pour les relations des transactions du projet (msdyn\_transactionconnections)**. Ces enregistrements sont utilisés par le processus périodique, **Importer depuis la table intermédiaire** lors de la création de lignes de journal d’intégration de Project Operations et de lignes de proposition de facture de projet.

La validation d’une feuille intégration Project Operations et d’une proposition de facture de projet déclenche une mise à jour des enregistrements respectifs de la table intermédiaire, **ProjCDSActualsImport**. Le système capture et enregistre les attributs comptables suivants pour les transactions réelles :

- Montant dans la devise comptable
- Taux de change
- N° document
- Montant de taxe de vente

Le mappage de table **Chiffres réels d’intégration Project Operations** met à jour les enregistrements des chiffres réels respectifs dans Dataverse avec ces informations.
