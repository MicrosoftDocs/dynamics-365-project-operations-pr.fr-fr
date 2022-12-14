---
title: Nouveautés de novembre 2022 - Déploiement simplifié de Project Operations
description: Cet article fournit des informations sur les mises à jour qualité disponibles dans la version de novembre 2022 du déploiement simplifié de Microsoft Dynamics 365 Project Operations.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831095"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Nouveautés de novembre 2022 - Déploiement simplifié de Project Operations

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.58.0.119


## <a name="quality-updates"></a>Mises à jour qualité

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
