---
title: Dotation d’un projet en sous-traitants et capacité de sous-traitance
description: Cette rubrique explique comment les besoins du projet peuvent être satisfaits à l’aide de collaborateurs contractuels ou d’une capacité sous-traitée dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903414"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotation d’un projet en sous-traitants et capacité de sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les membres génériques de l’équipe de projet peuvent être dotés d’employés ou de collaborateurs contractuels. Lors de la dotation d’un projet avec des contractuels, vous pouvez limiter vos options de dotation à des contractuels spécifiques affectés à une ligne de contrat de sous-traitance. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Rechercher des besoins en ressources humaines avec des contractuels appartenant à une ligne de contrat sous-traitance spécifique

Pour rechercher des besoins en ressources humaines et les doter en contractuels appartenant à une ligne de contrat sous-traitance spécifique, procédez comme suit :

1. Créez un membre générique de l’équipe de projet qui fait référence à un contrat de sous-traitance et une ligne de contrat de sous-traitance.
2. Générez un besoin en ressources pour ce membre générique de l’équipe de projet en utilisant le bouton **Générer un besoin** dans la sous-grille des membres de l’équipe de projet.
3. Sélectionnez la ligne du membre de l’équipe, puis sélectionnez le bouton **Réserver** dans la sous-grille. 
4. Cela ouvre le tableau de planification avec le contexte du besoin. Outre d’autres attributs tels que les champs de dates, de rôle et d’unité d’organisation, les filtres du Tableau de planification sont également automatiquement renseignés avec les champs de fournisseur, de contrat de sous-traitance et de ligne du contrat sous-traitance issus du besoin en ressources.
5. Le système recherche les ressources qui répondent aux critères de filtrage et les répertorie. 
6. Sélectionnez l’une des ressources filtrées et réservez la ressource pour le besoin. 
7. Un membre de l’équipe de projet est créé et mis à jour avec les références au contrat de sous-traitance et à la ligne de contrat de sous-traitance. Accédez à **Estimations du projet** et sélectionnez **Mettre à jour les prix** pour voir le coût mis à jour de l’affectation de ressource. 

> [!NOTE]
> La mise à jour du membre de l’équipe de projet avec une référence à un contrat de sous-traitance et une ligne de contrat de sous-traitance n’est pas toujours possible lors de la réservation si la ressource est affectée à plusieurs lignes de contrat de sous-traitance. Si le système ne parvient pas à mettre à jour le membre de l’équipe de projet avec un contrat et une ligne de sous-traitance, ouvrez l’enregistrement du membre de l’équipe de projet et mettez à jour manuellement ces champs afin que l’estimation des coûts financiers reflète avec précision le coût du sous-traitant.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Rechercher et doter en personnel les besoins en ressources avec n’importe quel collaborateur contractuel

Pour rechercher et doter en personnel les besoins en ressources avec n’importe quel collaborateur contractuel, procédez comme suit :

1. Créez un membre de l’équipe de projet générique.
2. Générez un besoin en ressources pour ce membre générique de l’équipe de projet en utilisant le bouton **Générer un besoin** dans la sous-grille des membres de l’équipe de projet.
3. Sélectionnez la ligne du membre de l’équipe, puis sélectionnez le bouton **Réserver** dans la sous-grille. 
4. Cela ouvre le tableau de planification avec le contexte du besoin. Outre d’autres attributs tels que les champs de dates, de rôle et d’unité d’organisation, les filtres du Tableau de planification sont également automatiquement renseignés avec les champs de fournisseur, de contrat de sous-traitance et de ligne du contrat sous-traitance issus du besoin en ressources. Étant donné que le besoin ne comportait aucune valeur renseignée de contrat ou de ligne de sous-traitance, ces attributs seront vides dans le volet de filtre.
5. Le système recherche les ressources qui répondent aux critères de filtrage et les répertorie.
6. Mettez à jour le champ **Type de collaborateur** dans le volet de filtre en **Collaborateur sous contrat** pour limiter la recherche aux travailleurs contractuels. Mettez à jour le champ **Fournisseur** dans le volet de filtre pour sélectionner un fournisseur afin de limiter la recherche aux seuls collaborateurs contractuels qui appartiennent à une société fournisseur spécifique.
7. Sélectionnez un collaborateur contractuel dans la liste et réservez la ressource pour le besoin.
8. Un membre de l’équipe de projet est créé. Cependant, le membre de l’équipe de projet n’est mis à jour avec aucun contrat ou ligne de sous-traitance et, par conséquent, l’affectation des ressources ne sera pas chiffrée à l’aide de la tarification de sous-traitance. Mettez à jour manuellement le membre de l’équipe de projet avec une ligne de sous-traitance et accédez à **Estimations du projet**, puis sélectionnez **Mettre à jour les prix** pour voir le coût mis à jour de l’affectation de ressource.

> [!NOTE]
> Les membres de l’équipe de projet dont le **Type de collaborateur** est **Collaborateur sous contrat** mais n’ont pas de référence à un contrat de sous-traitance sont signalés comme **Non valide** dans la grille **Membres de l’équipe de projet**. S’il existe des membres de l’équipe de projet ayant ce statut, ouvrez l’enregistrement du membre de l’équipe de projet et mettez à jour manuellement les champs de contrat et de ligne de sous-traitance afin que l’estimation des coûts financiers reflète avec précision le coût du sous-traitant dans l’onglet **Estimations**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
