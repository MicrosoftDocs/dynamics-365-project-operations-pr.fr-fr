---
title: Intégration des estimations et des chiffres réels de projet
description: Cet article fournit des informations sur l’intégration de la double écriture de Project Operations pour les estimations et les chiffres réels du projet.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914583"
---
# <a name="project-estimates-and-actuals-integration"></a>Intégration des estimations et des chiffres réels de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article fournit des informations sur l’intégration de la double écriture de Project Operations pour les estimations et les chiffres réels du projet.

## <a name="project-estimates"></a>Estimations de projets

Les estimations de main-d’œuvre, de dépenses et de matériaux du projet sont créées et conservées dans Microsoft Dataverse et synchronisées avec les applications de finances et d’opérations à des fins comptables. Les opérations de création, de mise à jour et de suppression ne sont pas prises en charge via les applications de finances et d’opérations.

La création d’estimations nécessite une configuration comptable valide pour le projet. Les projets associés à des lignes de contrat doivent avoir un profil de coût et de produit de projet valide, défini dans les règles de profil de coût et de produit du projet. Pour plus d’informations, consultez [Configurer la comptabilité des projets facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimations de main-d’œuvre

Les estimations de main-d’œuvre sont créées par le gestionnaire de projet ou le gestionnaire de ressources qui affecte également une ressource générique ou nommée à la tâche de projet. Les enregistrements d’affectations de ressources peuvent être consultés sur l’onglet **Affectations de ressources**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’affectation de ressources dans Dataverse créent des enregistrements de prévisions horaires dans les applications de finances et d’opérations via **Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**.

   ![Intégration des estimations de main-d’œuvre.](./Media/DW4LaborEstimates.png)

La double écriture synchronise les enregistrements d’affectations de ressources avec la table intermédiaire (**ProjCDSEstimateHoursImport**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions en heures (**ProjForecastEmpl**).

Le comptable du projet examine les enregistrements d’heures prévisionnelles créés dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Plan** > **Prévisions horaires**.

## <a name="expense-estimates"></a>Estimations de dépenses

Les estimations de dépenses sont créées par le gestionnaire de projet sur l’onglet **Estimations des dépenses**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’estimations des dépenses sont stockés dans l’entité **Ligne d’estimation** dans Dataverse. Ces enregistrements d’estimation ont une classe de transaction de type **Dépense** et sont synchronisés avec les enregistrements de prévisions de dépenses dans les applications de finances et d’opérations via **Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimatelines)**.

   ![Intégration des estimations de dépenses.](./Media/DW4ExpenseEstimates.png)

La double écriture synchronise les enregistrements d’estimations des dépenses avec la table intermédiaire (**ProjCDSEstimateExpenseImport**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions des dépenses (**ProjForecastCost**). Les lignes d’estimations stockent les enregistrements d’estimation des ventes et d’estimation des coûts séparément. La logique métier des applications de finances et d’opérations remplit un seul enregistrement de prévision de dépenses à l’aide de ce détail dans la table intermédiaire.

Le comptable du projet peut passer en revue les enregistrements de dépenses prévisionnelles créés dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Plan** > **Prévisions de dépenses**.

## <a name="material-estimates"></a>Estimations du matériel

Les estimations du matériel sont créées par le gestionnaire de projet sur l’onglet **Estimations du matériel**, sur la page **Détails du projet** dans Dataverse. Les enregistrements d’estimation du matériel sont stockés dans l’entité **Ligne d’estimation** dans Dataverse. Ces enregistrements d’estimation ont la classe de transaction de type **Matériel** et sont synchronisés avec les enregistrements de prévisions d’article dans les applications de finances et d’opérations via **Table d’intégration de Project pour les estimations de matériel (msdyn\_estimatelines)**.

   ![Intégration des estimations du matériel.](./Media/DW4MaterialEstimates.png)

La double écriture synchronise les enregistrements d’estimations du matériel avec la table intermédiaire (**ProjForecastSalesImpor**), puis utilise la logique métier pour créer et mettre à jour les enregistrements de prévisions d’articles (**ForecastSales**). Les lignes d’estimations stockent les enregistrements d’estimation des ventes et d’estimation des coûts séparément. La logique métier des applications de finances et d’opérations remplit un seul enregistrement de prévision d’article à l’aide de ce détail dans la table intermédiaire.

Le comptable du projet peut passer en revue les enregistrements d’articles prévisionnels créés dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Plan** > **Prévisions d’articles**.

## <a name="project-actuals"></a>Chiffres réels du projet

Les chiffres réels du projet sont créés dans Dataverse, en fonction du temps, des dépenses, du matériel et de l’activité de facturation. Tous les attributs opérationnels de ces transactions, y compris la quantité, le prix de revient, le prix de vente et le projet, sont capturés dans cette entité Dataverse. Pour plus d’informations, voir [Chiffres réels](../actuals/actuals-overview.md). Les enregistrements réels sont synchronisés avec les applications de finances et d’opérations à l’aide du mappage de table en double écriture **Chiffres réels d’intégration de Project Operations (msdyn\_actuals)** pour la comptabilité en aval.

   ![Intégration des chiffres réels.](./Media/DW4Actuals.png)

Le mappage de table **Chiffres réels d’intégration de Project Operations** synchronise tous les enregistrements de l’entité **Chiffres réels** dans Dataverse, avec l’attribut **Ignorer la synchronisation (usage interne uniquement)** défini sur **Faux**. Cette valeur d’attribut est définie dans Dataverse automatiquement lors de la création de l’enregistrement. Voici des exemples où cet attribut est défini sur **Vrai** :

  - Chiffres réels du coût du projet pour les transactions intersociétés. Pour plus d’informations, voir [Créer des transactions intersociétés](../project-accounting/create-intercompany-transactions.md). Ces enregistrements sont ignorés, car le système recrée le chiffre réel du coût de projet dans les applications de finances et d’opérations lorsque la facture fournisseur intersociétés est validée.
  - Enregistrements de ventes non facturées négatifs créés lors de la confirmation de la facture pro forma. Ces enregistrements sont ignorés, car la comptabilité auxiliaire du projet dans les applications de finances et d’opérations n’inverse pas l’enregistrement des ventes non facturées lors de la facturation, mais modifie le statut en entièrement facturé.

Le mappage de table à double écriture synchronise les enregistrements des chiffres réels avec la table intermédiaire, **ProjCDSActualsImport**. Ces enregistrements sont traités par le processus périodique **Importer depuis la table intermédiaire** lors de la création de lignes de journal d’intégration de Project Operations et de lignes de proposition de facture de projet. Pour plus d’informations, voir [Feuille intégration dans Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse capture également les liens entre les transactions réelles du projet dans l’entité **Connexion de la transaction**. Pour plus d’informations, voir [Lier les chiffres réels aux enregistrements originaux](../actuals/linkingactuals.md). Les liens entre les transactions réelles sont également synchronisés avec les applications de finances et d’opérations à l’aide du mappage de table en double écriture, **Entité d’intégration pour les relations de transaction de projet (msdyn\_transactionconnections)**. Ces enregistrements sont utilisés par le processus périodique, **Importer depuis la table intermédiaire** lors de la création de lignes de journal d’intégration de Project Operations et de lignes de proposition de facture de projet.

La validation d’une feuille intégration Project Operations et d’une proposition de facture de projet déclenche une mise à jour des enregistrements respectifs de la table intermédiaire, **ProjCDSActualsImport**. Le système capture et enregistre les attributs comptables suivants pour les transactions réelles :

- Montant dans la devise comptable
- Taux de change
- N° document
- Montant de taxe de vente

Le mappage de table **Chiffres réels d’intégration Project Operations** met à jour les enregistrements des chiffres réels respectifs dans Dataverse avec ces informations.
