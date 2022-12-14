---
title: Nouveautés de novembre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour qualité disponibles dans la version de novembre 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831082"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de novembre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.58.0.119
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2781818 | Erreur de clé introuvable lors de la définition du prix par défaut pour le journal d’utilisation des matériaux. |
| Facturation et tarification | 2922373 | Impossible de lier la ligne de devis au projet qui a été fermé en tant que devis perdu. |
| Facturation et tarification | 2943206 | Le champ **Ligne de contrat** dans l’entité Projet doit être facultatif. |
| Facturation et tarification | 2953182 | Amélioration du message d’erreur pour les factures de correction.|
| Facturation et tarification | 2959500 | Impossible de lier la ligne de devis à une tâche de projet déjà associée à un devis perdu.|
| Facturation et tarification | 2959560 | Message « Ce client est déjà sur le contrat de projet » reçu lors de la clôture du devis comme gagné dans certaines régions. |
| Facturation et tarification | 3031727 | Les affectations de ressources échouent avec l’erreur Champ obligatoire « msdyn_Company » manquant. |
| Facturation et tarification | 3036905 | La société propriétaire n’est jamais initialisée sur le ProjectTeamMember. |
| Gestion des opportunités | 2763519 | Erreur de référence nulle dans EnsureProjectContractAllowsUpdates. |
| Gestion des opportunités | 2783798 | Lors de l’importation des estimations de projet sur la ligne de devis, les descriptions de tâches sont manquantes pour les estimations de dépenses et de matériel.|
| Gestion des opportunités | 2988635 | Améliorer la description du message d’erreur lors de la suppression d’un client sur devis. |
| Gestion des opportunités | 3001191 | Impossible de créer un devis à partir de l’opportunité où la méthode de facturation est spécifiée comme nulle. |
| Mettre à niveau | 3012324 | La conversion du projet a échoué sur un projet avec des caractères de contrôle comme Onglet dans son nom. || Planification et suivi de projets | 2790384 | Le délai d’attente OperationSet en attente est trop court. |
| Planification et suivi de projets | 3044275 | Localisation manquante pour : missingProjectSchedulerErrorMessage. |
| Planification et suivi de projets | 3044277 | La grille Project Recon ne se charge pas lorsque le planificateur est désactivé.|
| Gestion des ressources | 2943153 | Mettez à jour l’onglet Suivi pour afficher deux décimales pour la durée.|
| Sous-traitance | 2932774 | La lecture seule de la ligne de facture du fournisseur génère une erreur incorrecte. |
| Sous-traitance | 2939556 | Le statut de l’en-tête de facture fournisseur ne doit pas être défini sur Brouillon sur la ligne, supprimer si non actif. |
| Temps et dépenses | 2939998 | Adoption de la nouvelle version de TESA dans ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
