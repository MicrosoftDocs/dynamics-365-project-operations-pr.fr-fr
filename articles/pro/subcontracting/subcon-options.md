---
title: Options de sous-traitance pour les membres de l’équipe du projet
description: Cette rubrique explique les options de sous-traitance pour les membres de l’équipe de projet dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903412"
---
# <a name="subcontracting-options-for-project-team-members"></a>Options de sous-traitance pour les membres de l’équipe du projet

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Microsoft Dynamics 365 Project Operations, vous pouvez évaluer les options de sous-traitance disponibles pour un ou plusieurs membres de l’équipe de projet. Les options de sous-traitance disponibles vous permettent de :

- Créer un nouveau contrat de sous-traitance et/ou créer de nouvelles lignes sur un contrat de sous-traitance existant pour les membres de l’équipe de projet sélectionnés. 
- Effectuer une réservation par rapport à un contrat de sous-traitance ou une ligne d’un tel contrat existant. 

Vous pouvez choisir parmi les options de sous-traitance disponibles pour les membres génériques de l’équipe de projet, ou choisir parmi les membres de l’équipe de projet qui ont été dotés d’une ressource nommée qui est un collaborateur sous contrat. 

Il n’existe aucune option de sous-traitance disponible pour ce qui suit :

- Les membres de l’équipe de projet qui ont été dotés d’un employé. 
- Les membres de l’équipe de projet qui sont déjà associés à un contrat de sous-traitance et une ligne de contrat de sous-traitance. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Sous-traitance d’un membre de l’équipe de projet sans dotation de personnel

Pour passer en revue et choisir parmi les options de sous-traitance disponibles pour un membre de l’équipe de projet générique ou sans dotation de personnel, procédez comme suit :

1. Sélectionnez un ou plusieurs enregistrements de membre de l’équipe de projet où la ressource est une ressource générique.
2. Assurez-vous qu’aucun des enregistrements des membres de l’équipe de projet sélectionnés n’est déjà en sous-traitance. 
3. Sélectionnez **Options de sous-traitance** dans la sous-grille des membres de l’équipe de projet. La boîte de dialogue **Options de sous-traitance** s’ouvre. 
4. Si vous n’avez sélectionné qu’un seul enregistrement de membre de l’équipe de projet à l’étape 1, les options suivantes seront disponibles :
    - Créer de nouvelles lignes de contrat de sous-traitance. 
    - Effectuer une réservation sur un contrat de sous-traitance existant. Si vous avez sélectionné plusieurs enregistrements de membres d’équipe de projet à l’étape 1, la seule option disponible est de créer de nouvelles lignes de contrat de sous-traitance.
5. L’option de réservation sur une ligne de contrat de sous-traitance existante vous permet de sélectionner un contrat de sous-traitance et une ligne de contrat de sous-traitance par rapport auxquels vous souhaitez effectuer une réservation. Lors de la sélection d’une ligne de contrat sous-traitance pour réserver de la capacité, vous devez vous assurer que la ligne de contrat de sous-traitance sélectionnée concerne le temps et que le rôle requis sur le membre de l’équipe de projet correspond au rôle qui a été acheté sur la ligne de contrat de sous-traitance.
6. Lorsque vous choisissez de créer de nouvelles lignes de contrat de sous-traitance pour les membres de l’équipe de projet, le système vous permettra de sélectionner le contrat de sous-traitance pour lequel vous souhaitez créer ces lignes. Le contrat de sous-traitance que vous sélectionnez pour créer de nouvelles lignes doit avoir le statut de **Brouillon**. Avec cette option de création de nouvelles lignes de contrat de sous-traitance pour les membres de l’équipe de projet sélectionnés, le système créera une ligne de contrat de sous-traitance pour le temps pour chaque membre de l’équipe de projet. Le rôle, les heures et les dates seront copiés du membre de l’équipe de projet vers chaque ligne de contrat de sous-traitance créée. 
7. Lorsqu’un membre générique de l’équipe est associé à un contrat de sous-traitance et à une ligne de contrat de sous-traitance, le champ **Type de collaborateur** de la ligne du membre de l’équipe générique sera mis à jour en **Collaborateur sous contrat** et la valeur **Validité du contrat de sous-traitance** sera fixée à **Valide**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Sous-traitance d’un membre de l’équipe de projet avec dotation de personnel

Comme les membres d’équipe génériques ou sans dotation de personnel, vous pouvez également afficher les options de sous-traitance pour un membre de l’équipe de projet doté de personnel, tant que le membre de l’équipe doté est un collaborateur sous contrat. Pour passer en revue et choisir parmi les options de sous-traitance disponibles pour un membre de l’équipe de projet nommé ou avec dotation de personnel, procédez comme suit :

1. Sélectionnez un ou plusieurs enregistrements de membre de l’équipe de projet où la ressource est un collaborateur sous contrat nommé.
2. Assurez-vous qu’aucun des enregistrements des membres de l’équipe de projet sélectionnés n’est déjà en sous-traitance. 
3. Sélectionnez **Options de sous-traitance** dans la sous-grille des membres de l’équipe de projet. La boîte de dialogue **Options de sous-traitance** s’ouvre. 
4. Si vous n’avez sélectionné qu’un seul enregistrement de membre de l’équipe de projet à l’étape 1, les options suivantes seront disponibles :
      - Créer de nouvelles lignes de contrat de sous-traitance.
      - Effectuer une réservation par rapport à un sous-contrat existant.
  Si vous avez sélectionné plusieurs enregistrements de membres d’équipe de projet à l’étape 1, la seule option disponible est de créer de nouvelles lignes de contrat de sous-traitance.
5. L’option de réservation sur une ligne de contrat de sous-traitance existante vous permet de sélectionner un contrat de sous-traitance et une ligne de contrat de sous-traitance par rapport auxquels vous souhaitez effectuer une réservation. Lors de la sélection d’une ligne de contrat de sous-traitance pour réserver de la capacité, vous devez vous assurer des points suivants :
      - La ligne de contrat de sous-traitance sélectionnée concerne le temps. 
      - Le rôle requis pour le membre de l’équipe de projet correspond au rôle qui a été acheté sur la ligne de sous-traitance. 
      - Le fournisseur auquel le collaborateur sous-traitant est associé est le même que le fournisseur du contrat de sous-traitance.
6. Lorsque vous choisissez de créer de nouvelles lignes de contrat de sous-traitance pour les membres de l’équipe de projet, le système vous permettra de sélectionner le contrat de sous-traitance pour lequel vous souhaitez créer ces lignes. Avec cette options, vous devez vous assurer que le fournisseur auquel appartient le collaborateur sous-traitant est le même que le fournisseur du sous-contrat. 
7. Le contrat de sous-traitance que vous sélectionnez pour créer de nouvelles lignes doit avoir le statut de **Brouillon**. Avec cette option de création de nouvelles lignes de contrat de sous-traitance pour les membres de l’équipe de projet sélectionnés, le système créera une ligne de contrat de sous-traitance pour le temps pour chaque membre de l’équipe de projet. Le rôle, les heures et les dates seront copiés du membre de l’équipe de projet vers chaque ligne de contrat de sous-traitance créée.  
8. Lorsqu’un membre nommé de l’équipe est associé à un contrat de sous-traitance et à une ligne de contrat de sous-traitance, le champ **Type de collaborateur** de la ligne du membre de l’équipe nommé sera mis à jour en **Collaborateur sous contrat** et la valeur **Validité du contrat de sous-traitance** sera fixée à **Valide**.

## <a name="re-costing-subcontractor-assignments"></a>Réévaluation du coût des affectations des sous-traitants

Lorsqu’un membre de l’équipe de projet (générique ou nommé) est lié à des lignes de contrat de sous-traitance à l’aide de la boîte de dialogue **Options de sous-traitance**, toutes les affectations à des tâches que possède le membre de l’équipe seront réévaluées en fonction de la liste de tarifs jointe au contrat de sous-traitance. Dans l’onglet **Estimations** de la page **Détails du projet**, sélectionnez le bouton **Mettre à jour les prix** pour voir les tarifs et/ou les coûts mis à jour résultant de la décision de sous-traiter.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
