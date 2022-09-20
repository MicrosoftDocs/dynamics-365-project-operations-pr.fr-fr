---
title: Modifications de la fonctionnalité de Project Service Automation vers Project Operations
description: Cet article offre une vue d’ensemble des changements de fonctionnalités de Project Service Automation vers Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459923"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Modifications de la fonctionnalité de Project Service Automation vers Project Operations

La mise à niveau de Dynamics 365 Project Service Automation vers Dynamics 365 Project Operations simplifié sera possible en trois phases. Cet article offre les informations relatives aux modifications principales auxquelles vous attendre pour avoir la mise à niveau complète.

| Livraison de la mise à niveau | Phase 1 <br>(Janvier 2022) | Phase 2 <br>(Novembre 2022) | Phase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Aucune dépendance vis-à-vis de la structure de répartition du travail (WBS) pour les projets. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La WBS est incluse dans les limites actuellement prises en charge par Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| La WBS en dehors des limites actuellement prises en charge par Project Operations, y compris la prise en charge de Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Gestion des projets

Les changements les plus importants dans l’expérience utilisateur se situeront dans le domaine de la planification de projet. Project Operations adopte une nouvelle expérience moderne pour gérer une structure de répartition du travail (WBS) en tirant parti des fonctionnalités de planification fournies par [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Différences dans l’expérience de planification

Le tableau suivant résume les différences de planification entre Project Service Automation et Project Operations.

|  Planification     |   Project Operations   |   Antigène prostatique spécifique (PSA)   |
|-----------------|------------------------|---------|
| Modèles de projet - Possibilité de définir et d’appliquer des modèles de projet lors de la création d’un projet  |  &nbsp;    | :heavy_check_mark: |
| Intégration de la structure de répartition du travail (WBS) du projet avec le client de bureau   |    &nbsp;  | :heavy_check_mark: |
| Contraintes - Commencer au plus tôt le, finir au plus tard le  | :heavy_check_mark: |   &nbsp;  |
| Jalons - Tâches sans durée   | :heavy_check_mark:  |  &nbsp;  |
| Les tâches axées sur les ressources respecteront la disponibilité des ressources affectées   | :heavy_check_mark: |  &nbsp;    |
| Modification par phases de temps - Modifier les plans et travailler au jour le jour   |   &nbsp;  | :heavy_check_mark: |
| Planification automatique/manuelle - Utiliser le moteur de planification de Project pour planifier automatiquement ou manuellement des tâches |  &nbsp; | :heavy_check_mark:  |
| Modifier de grands projets directement dans l’interface utilisateur : il n’y a pas de limite à la taille des plans modifiables  | Limite définie à 500 tâches  | :heavy_check_mark:       |
| Pourcentage achevé - Marquer la progression de la tâche   | :heavy_check_mark:  |  &nbsp;  |
| [Modes de planification de projet](../project-management/scheduling-modes.md) - Définir le projet en unités fixes, effort fixe ou durée fixe | :heavy_check_mark: | &nbsp; |
| Chronologie - Créer et personnaliser la vue de la chronologie pour visualiser les détails du calendrier et communiquer avec les parties prenantes. | :heavy_check_mark:  | &nbsp; |
| Tâches pilotées par l’effort - Prise en charge du moteur de planification pour la planification d’une tâche pilotée par l’effort  | :heavy_check_mark:  | &nbsp; |
| Boîte de dialogue **Informations sur la tâche** - Enregistrer les détails de la tâche à l’aide d’une boîte de dialogue | :heavy_check_mark:  |  &nbsp;  |
| Glisser-déposer - Sélectionner plusieurs tâches et modifier leur position sur le WBS | :heavy_check_mark: | &nbsp;  |
| Vues persistantes flexibles - Définir des vues plus granulaires des attributs de tâche   | :heavy_check_mark:  | &nbsp; |
| Trier et filtrer le WBS  | :heavy_check_mark:  | &nbsp; |
| Affichage des tableaux pour la livraison de projets sans cascade  | :heavy_check_mark:   | &nbsp; |
| Vue Chronologie - Diagramme de Gantt interactif utilisé pour visualiser et modifier le WBS   | :heavy_check_mark:  | &nbsp; |
| Raccourcis clavier - Utiliser des raccourcis clavier pour les opérations courantes, telles que l’indentation ou l’insertion  | :heavy_check_mark:  |  &nbsp; |
| Annulation à plusieurs niveaux - Effectuer une analyse de simulation pour comprendre pleinement l’impact des modifications en inversant et en réappliquant un ensemble complet d’opérations | :heavy_check_mark: | &nbsp; |
| Couper/Copier/Coller - Collaborer sur le développement des horaires en copiant et en collant les détails des horaires entre les applications  | :heavy_check_mark: | &nbsp; |
| Listes de contrôle des tâches - Ajouter jusqu’à 20 éléments de liste de contrôle à une tâche   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planification de projet

La page **Projet** dans Project Operations présente un nombre important de différences par rapport à la page **Projet** dans Project Service Automation.

Les actions suivantes ont été supprimées de la page **Projets** dans le cadre de la mise à niveau de la phase 1 :

  - **Ouvrir dans MS Project**
  - **Créer un modèle**
  - **Supprimer le lien de MS Project**

La page **Projet** de Project Operations comprend les nouveaux onglets suivants.

- **Estimations du matériel**
- **Configuration de la facturation de la tâche**

L’onglet **Statut** a été supprimé et le champ **Statut** est maintenant sur l’onglet **Résumé** avec le mode de planification du projet.

   ![Mises à jour de la page Projet.](media/projectform.png)

L’onglet **Programme** a été renommé en onglet **Tâche** et présente la nouvelle expérience de planification de projet avec Project for the Web.

   ![Nouvel onglet Tâches de projet.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modes de planification

Project Operations a introduit une nouvelle fonctionnalité, [Modes de planification](../project-management/scheduling-modes.md). Tous les projets Project Service Automation existants sont, par défaut, définis sur **Durée fixe** dans Project Operations. Cependant, la valeur par défaut pour les nouveaux projets peut être gérée en accédant à **Réglages** > **Paramètres** > **Paramètre** > **Mode Planification**.

   ![Réglages des paramètres du projet pour le mode Planification.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limites de planification de projet

Project Operations s’appuie sur Project for the Web pour toutes les opérations de planification de projet. Project for the Web gère la structure de répartition du travail à l’aide des limites du tableau suivant.

| **Champ**                                          | **Limite**             |
|----------------------------------------------------|-----------------------|
| Nombre total maximal de tâches pour un projet                  | 500                   |
| Durée totale maximale d’un projet               | 3 650 jours (10 ans)  |
| Nombre total maximal de ressources pour un projet              | 300                   |
| Nombre total maximal de liens (successeur uniquement) pour un projet | 600                   |
| Nombre total maximal de champs personnalisés pour un projet          | 10                    |
| Niveau hiérarchique maximal                            | 10 niveaux             |
| Nombre maximal de liens (successeur + prédécesseur)            | 20                    |
| Durée maximale d’une tâche feuille                      | Plus de 1250 jours             |
| Durée maximale d’une tâche récapitulative                 | 3 650 jours (10 ans)  |
| Nombre maximal de ressources affectées à une tâche               | 20 ressources          |
| Plage de dates prise en charge pour une tâche                    | 1/1/2000 - 31/12/2149 |
| Éléments de liste de vérification                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilité et développement de la planification du projet

Après la mise à niveau vers Project Operations, vous devez utiliser les API de planification de projet pour exécuter des opérations de création, de mise à jour et de suppression sur les entités suivantes :

|   Nom de l’entité           |   Nom logique de l’entité       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tâche du projet            | msdyn_projecttask           |
| Dépendance de la tâche du projet | msdyn_projecttaskdependency |
| Attribution de ressource     | msdyn_resourceassignment    |
| Compartiment du projet          | msdyn_projectbucket         |
| Membre de l’équipe du projet     | msdyn_projectteam           |

Si vous avez actuellement des personnalisations qui impliquent ces entités, consultez [Utiliser les API de planification de projet pour effectuer des opérations avec les entités de planification](../project-management/schedule-api-preview.md) pour des conseils de mise en œuvre.

## <a name="data-model-changes"></a>Modifications du modèle de données

Dans le cadre de la phase 1 de la mise à niveau, des modifications ont été apportées au modèle de données. Ces modifications sont principalement des modifications de champ apportées aux entités existantes. Dans la phase 1, les entités **msydn_project** et **msdyn_projectteam** sont une refactorisation des personnalisations. 

> [!IMPORTANT]
> Cette section sera mise à jour avec des entités supplémentaires au fur et à mesure que les futures phases de mise à niveau seront terminées.

Les champs suivants ont été remplacés par de nouveaux champs.

|   Entity          |   Ancien nom logique   |   Nouveau nom logique    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Les champs suivants ont été ajoutés.

|   Entity          |   Nom logique                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Affiche le cumul des ventes de frais réels sur le projet. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Affiche le cumul du coût réel des matériaux du projet. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Affiche le cumul des ventes de matières réelles sur le projet. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | La ligne de contrat associée à ce projet. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Il s’agit d’un champ système interne utilisé pour **Copier le projet** associé à l’identifiant de corrélation. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Il s’agit d’un champ système interne utilisé pour **Copier le projet** associé à l’identifiant de session. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Dernière synchronisation du jeton de révision global xRM à partir du service de planification de projet. |
| msdyn_project     | msdyn_msprojectdocument                      | Document Microsoft Project appartenant au projet. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Cumul du coût planifié des matériaux du projet. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Cumul des ventes planifiées des matériaux du projet. Réservé exclusivement à une utilisation dans Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programme auquel ce projet est associé. |
| msdyn_project     | msdyn_quotelineproject                       | La ligne de devis associée à ce projet. |
| msdyn_project     | msdyn_replaylogheader                        | En-tête des journaux de relecture. |
| msdyn_project     | msdyn_schedulemode                           | Mode de planification par défaut utilisé pour toutes les tâches du projet.  |
| msdyn_project     | msdyn_taskearlieststart                      | Date de début la plus proche d’une tâche du projet.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Membre de l’équipe du projet à partir duquel ce membre de l’équipe du projet a été copié. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indique si la ressource requise doit être créée pour un nouveau membre d’équipe générique créé.  |
| msdyn_projectteam | msdyn_deletestatus                           | Statut de suppression du membre de l’équipe pour savoir si une demande de suppression a bien été envoyée à Project Scheduling Service et si ce dernier a bien renvoyé une réponse et dans le délai attendu. |
| msdyn_projectteam | msdyn_effortcompleted                        | Effectue le suivi des efforts réalisés par le membre de l’équipe sur ses affectations. |
| msdyn_projectteam | msdyn_effortremaining                        | Suit les efforts restant à réaliser par le membre de l’équipe sur ses affectations. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Période d’attente à partir du moment où le membre de l’équipe envoie une demande de suppression au service de planification de projet jusqu’à ce que le membre de l’équipe soit effectivement supprimé de Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Horodatage à enregistrer lorsque la demande de suppression du membre de l’équipe est envoyée à Project Scheduling Service. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Affiche le membre de l’équipe du projet à partir duquel ce membre de l’équipe du projet a été copié.  |

## <a name="project-templates"></a>Modèles de projet

Project Operations ne prend pas en charge les modèles de projet. Cependant, vous pouvez répliquer une grande partie de la fonctionnalité de base avec l’utilisation de l’[API de copie de projet](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Prise en charge des compléments de bureau

La prise en charge du complément Microsoft Project Desktop ne sera pas disponible dans les 2 premières phases de la mise à niveau. Dans la phase 3, les clients dont les projets dépassent les limites actuellement prises en charge de Project for the Web pourront utiliser le complément de bureau.

## <a name="editing-resource-assignment-contours"></a>Modification des contours d’affectation des ressources

La possibilité de modifier les contours d’affectation des ressources sera disponible lorsque la phase 2 de la mise à niveau sera disponible.

## <a name="billing-and-pricing"></a>Facturation et tarification

Les nouvelles fonctionnalités suivantes ont été ajoutées dans Project Operations. Ces fonctionnalités sont de nature additive et n’ont aucune incidence sur le modèle de données de Project Service Automation.

- [Enregistrer l’utilisation du matériel sur les projets et les tâches du projet](../material/material-usage-log.md)
- [Gestion des sous-traitants](../pro/subcontracting/managing-subcontracts-overview.md)
- [Paiements anticipés et contrats basés sur un acompte](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statut et validations des limites à ne pas dépasser des contrats](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturation à la tâche](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Composants obsolètes

Les tableaux suivants documentent tous les champs obsolètes déplacés vers la solution de composants obsolètes après la mise à niveau. Pour plus d’informations et un lien vers la solution, voir [Dynamics 365 Project Service Automation 3x vers Project Operations 4x Composants obsolètes](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Champs                                                     |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

