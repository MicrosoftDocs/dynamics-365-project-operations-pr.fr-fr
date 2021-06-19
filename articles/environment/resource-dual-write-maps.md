---
title: Versions du mappage à double écriture Project Operations
description: Cette rubrique fournit la liste des mappages à double écriture requis pour Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b24a20d47eefa43b2e4e184a377decdb280d436d
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025771"
---
# <a name="project-operations-dual-write-map-versions"></a>Versions du mappage à double écriture Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

L’utilisation de Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés nécessite l’exécution d’un ensemble de mappages à double écriture dans l’environnement. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Mappages prérequis : solution d’orchestration à double écriture

Les mappages suivants sont des conditions préalables requises pour la solution Project Operations. Assurez-vous d’exécuter les mappages répertoriés dans le tableau suivant et tous les mappages de table associés dans votre environnement.

| Mappage de table | Synchronisation initiale |
| --- | --- |
| Registre (msdyn_ledgers) | Nécessite une synchronisation initiale pour le mappage de table et tous les prérequis. La sélection principale pour la synchronisation initiale est composée des applications Finance and Operations. |
| Entités juridiques (cdm_companies) | Non requis. Le système remplit automatiquement cette entité lorsque les environnements sont liés à l’aide de la double écriture. |
| Clients V3 (comptes) | Non requis pour l’approvisionnement. |
| Fournisseurs V2 (msdyn_vendors) | Non requis pour l’approvisionnement. |

1. Dans la liste des mappages, sélectionnez le mappage Registre **(msdyn\_ledgers)** avec tous les prérequis et cochez la case **Synchronisation initiale**. Dans le champ **Sélection principale pour la synchronisation initiale**, sélectionnez les applications **Finance and Operations** pour le mappage du registre et tous les mappages prérequis. Cliquez sur **Exécuter**.

![Synchronisation de la carte du registre](media/DW6.png)

2. Suivez les mêmes étapes pour tous les autres mappages de table répertoriés dans le tableau ci-dessus. Ne cochez pas la case **Synchronisation initiale** lors de l’exécution de ces mappages.

## <a name="project-operations-dual-write-maps"></a>Mappages à double écriture Project Operations

Les mappages suivants sont requis pour une solution Project Operations. Les versions des mappages en double écriture sont répertoriées à partir de la mise à jour de Project Operations de mai 2021, version 4.10.0.186.

| **Mappage d’entité** | **Version la plus récente** | **Synchronisation initiale** |
| --- | --- | --- |
| Entité d’intégration pour les relations de transaction du projet (msdyn\_transactionconnections) | 1.0.0.0 | Non requis pour l’approvisionnement. |
| En-têtes de contrat du projet (commandes client) | 1.0.0.1 | Non requis pour l’approvisionnement. |
| Lignes du contrat de projet (salesorderdetails) | 1.0.0.0 | Non requis pour l’approvisionnement. |
| Source de financement de projet (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Non requis pour l’approvisionnement. |
| Table Intégration de Project Operations pour les estimations de matériel (msdyn\_estimatelines) | 1.0.0.0 | Non requis pour l’approvisionnement. |
| Propositions de facture de projet V2 (factures) | 1.0.0.3 | Non requis pour l’approvisionnement. |
| Chiffres réels d’intégration Project Operations (msdyn_actuals) | 1.0.0.14 | Non requis pour l’approvisionnement. |
| Jalons de la ligne de contrat d’intégration de Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Non requis pour l’approvisionnement. |
| Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn_estimateslines) | 1.0.0.2 | Non requis pour l’approvisionnement. |
| Entité d’intégration de Project Operations pour les estimations d’heures (msdyn_resourceassignments) | 1.0.0.5 | Non requis pour l’approvisionnement. |
| Entité d’exportation des catégories de dépenses de projet d’intégration de Project Operations (msdyn_expensecategories) | 1.0.0.1 | Non requis pour l’approvisionnement. |
| Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn_expenses) | 1.0.0.2 | Non requis pour l’approvisionnement. |
| Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Non requis pour l’approvisionnement. |
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Non requis pour l’approvisionnement. |
| Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories) | 1.0.0.1 | Nécessite une synchronisation initiale afin que le mappage de table synchronise les rôles de ressources de gestionnaire de projet et de membre d’équipe qui sont renseignés dans l’environnement Dynamics 365 Dataverse pendant l’approvisionnement. Dataverse est la source principale de la synchronisation initiale. |
| Tâches du projet (msdyn_projecttasks) | 1.0.0.4 | Non requis pour l’approvisionnement. |
| Catégories de transactions du projet (msdyn_transactioncategories) | 1.0.0.0 | Non requis pour l’approvisionnement. |
| Projets V2 (msdyn_projects) | 1.0.0.2 | Non requis pour l’approvisionnement. |

Pour exécuter les mappages répertoriés, procédez comme suit.

1. Activez les rôles de ressources de projet pour le mappage de table **toutes les entreprises (bookableresourcecategories)** car ce mappage nécessite la synchronisation initiale. Dans le champ **Sélection principale pour la synchronisation initiale**, sélectionnez **Common Data Service**. 

 ![Synchronisation du mappage de table des rôles de ressources](media/6ResourceInitialSync.jpg)

 Attendez que l’état de la carte soit **En cours** avant de passer à l’étape suivante.

2. Sélectionnez tous les mappages requis restants. Vous pouvez les filtrer dans la liste des mappages à double écriture en indiquant le mot-clé **Projet** dans la zone de recherche située dans le coin supérieur droit. Vous pouvez sélectionner tous les mappages, puis exécuter. Pour plus d’informations, voir [Gérer plusieurs mappages de table](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Assurez-vous également d’activer et d’exécuter les mappages d’entités associés.

### <a name="project-operations-dual-write-map-versions"></a>Versions du mappage à double écriture Project Operations

Exécutez toujours la dernière version du mappage dans votre environnement. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si l’une des conditions suivantes existe :

- Un mappage n’est pas activé.
- La dernière version du mappage n’est pas activée. 
- Les mappages de table associés ne sont pas activés.

Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Vous pouvez activer une nouvelle version du mappage en sélectionnant **Versions du mappage de table**, en sélectionnant la dernière version, puis en enregistrant la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, vous devrez réappliquer les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
