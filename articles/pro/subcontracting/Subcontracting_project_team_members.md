---
title: Membres de l’équipe du projet en sous-traitance
description: Cette rubrique explique comment contractualiser des membres de l’équipe de projet dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902859"
---
# <a name="subcontracting-project-team-members"></a>Membres de l’équipe du projet en sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Microsoft Dynamics 365 Project Operations, vous pouvez choisir de sous-traiter des membres de l’équipe de projet avec ou sans dotation de personnel.

- Les membres de l’équipe de projet sans personnel se voient attribuer une ressource générique.
- Les membres de l’équipe avec dotation de personnel ont une ressource nommée affectée.

Lorsque vous liez un membre de l’équipe de projet à une ligne de contrat de sous-traitance, toutes les affectations à des tâches que possède le membre de l’équipe seront réévaluées en fonction de la liste de tarifs jointe au contrat de sous-traitance.  Dans l’onglet **Estimations** de la page **Détails du projet**, sélectionnez le bouton **Mettre à jour les prix** pour voir les tarifs et/ou les coûts mis à jour résultant de la décision de sous-traiter. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Sous-traitance d’un membre de l’équipe de projet sans dotation de personnel
La page **Détails des membres de l’équipe** comporte des champs de contrat et de ligne de sous-traitance qui permettent à un chef de projet d’exprimer comment il souhaite tirer la capacité requise d’un contrat de sous-traitance. Pour sous-traiter un membre de l’équipe de projet en tant que ressource générique, procédez comme suit :

1.  Choisissez un contrat de sous-traitance sur la page **Détails des membres de l’équipe**.

2.  Vous ne pouvez sélectionner que des sous-contrats ayant le statut **Brouillon** ou **Confirmé**. Les contrats de sous-traitance **Fermés** ou **Annulés** ne peuvent pas être sélectionnés. 

3.  Le champ **Ligne de sous-traitance** devient visible une fois que vous avez sélectionné un contrat de sous-traitance.

4.  Dans le champ **Ligne de sous-traitance**, vous ne pouvez sélectionner que des lignes de sous-traitance qui concernent le temps. Vous ne pouvez pas sélectionner de lignes de sous-traitance pour des dépenses ou du matériel.

5.  Le rôle de l’enregistrement du membre de l’équipe de projet doit correspondre au rôle sur la ligne de sous-traitance. Cela garantit que le temps estimé pour le rôle sur le projet est le même que celui acheté sur la ligne de sous-traitance. 

Lorsqu’un membre générique de l’équipe est associé à un contrat de sous-traitance et à une ligne de contrat de sous-traitance, le champ **Type de collaborateur** de la ligne du membre de l’équipe générique sera mis à jour en **Collaborateur sous contrat** et la **Validité du contrat de sous-traitance** sera fixée à **Valide**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Sous-traitance d’un membre de l’équipe de projet avec dotation de personnel
Comme les membres d’équipe génériques ou sans personnel, la capacité requise sur un projet d’un membre de l’équipe avec personnel peut également être liée à un contrat de sous-traitance. Pour sous-traiter un membre nommé de l’équipe de projet, procédez comme suit :

1.  Assurez-vous que la ressource nommée est configurée en tant que ressource réservable de type Collaborateur sous contrat. Assurez-vous également que le champ **Fournisseur** sur la ressource réservable correspond au fournisseur du sous-contrat que vous sélectionnez. 

2.  Vous ne pouvez sélectionner que des sous-contrats ayant le statut **Brouillon** ou **Confirmé**. Les contrats de sous-traitance **Fermés** ou **Annulés** ne peuvent pas être sélectionnés. 

3.  Le champ **Ligne de sous-traitance** devient visible une fois que vous avez sélectionné un contrat de sous-traitance.

4.  Dans le champ **Ligne de sous-traitance**, vous ne pouvez sélectionner que des lignes de sous-traitance qui concernent le temps. Vous ne pouvez pas sélectionner de lignes de sous-traitance pour des dépenses ou du matériel.

5.  Le rôle de l’enregistrement du membre de l’équipe de projet doit correspondre au rôle sur la ligne de sous-traitance. Cela garantit que le temps estimé pour le rôle sur le projet est le même que celui acheté sur la ligne de sous-traitance. 

Les membres de l’équipe de projet nommés qui sont configurés avec le type de collaborateur sous contrat **Ressource réservable** seront affichés avec un statut de validité de sous-traitance **Non valide** s’ils ne sont pas liés à un contrat de sous-traitance. Lorsqu’un membre nommé de l’équipe est associé à un contrat de sous-traitance et à une ligne de contrat de sous-traitance, le champ **Type de collaborateur** de la ligne du membre de l’équipe sera mis à jour en **Collaborateur sous contrat** et la **Validité du contrat de sous-traitance** sera fixée à **Valide**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
