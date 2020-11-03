---
title: Développer des modèles de projet avec Copier le projet
description: Cette rubrique fournit des informations sur la création de modèles de projet à l'aide de l'action personnalisée Copier le projet.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075680"
---
# <a name="develop-project-templates-with-copy-project"></a>Développer des modèles de projet avec Copier le projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations prend en charge la possibilité de copier un projet et de rétablir toutes les affectations aux ressources génériques qui représentent le rôle. Les clients peuvent utiliser cette fonctionnalité pour créer des modèles de projet de base.

Lorsque vous sélectionnez **Copier le projet** , le statut du projet cible est mis à jour. Utilisez la **raison du statut** pour déterminer quand l'action de copie est terminée. La sélection **Copier le projet** met également à jour la date de début du projet à la date de début actuelle si aucune date cible n'est détectée dans l'entité de projet cible.

## <a name="copy-project-custom-action"></a>Copier l'action personnalisée du projet 

### <a name="name"></a>Nom  

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Paramètres d’entrée
Il existe trois paramètres de saisie :

| Paramètre          | Type   | Valeurs                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Référence d’entité | Projet source |
| Cible              | Référence d’entité | Projet cible |


- **{"clearTeamsAndAssignments":true}**  : Trois comportements par défaut de Project pour le Web et suppression de toutes les affectations et des membres de l'équipe.
- **{"removeNamedResources":true}** Le comportement par défaut pour Project Operations et rétablira les affectations aux ressources génériques.

Pour plus de valeurs par défaut sur les actions, voir [Utiliser des actions API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Spécifier les champs à copier 
Lorsque l'action est appelée **Copier le projet** regardera la vue du projet **Copier les colonnes du projet** pour déterminer les champs à copier lorsque le projet est copié.
