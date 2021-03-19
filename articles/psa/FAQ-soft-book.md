---
title: Réservation temporaire d’une ressource
description: Cette rubrique décrit comment planifier provisoirement ou réserver provisoirement les membres de l’équipe du projet.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 1d2044692d1c6d694a1365be76dd8e7ddafd376d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285975"
---
# <a name="soft-book-a-resource"></a>Réservation temporaire d’une ressource

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vous pouvez planifier provisoirement ou réserver temporairement une ressource dans une équipe de projet pour indiquer que vous prévoyez d’attribuer la ressource au projet. Les réservations temporaires ne consomment pas les capacités disponibles d’une ressource, et vous pouvez attribuer des membres d’équipe réservés temporairement aux tâches du projet. Toutefois, du fait que la réservation temporaire ne consomme pas la capacité d’une ressource, vous pouvez toujours réserver fermement la ressource pour d’autres tâches au cours de la même période. Les ressources génériques ne peuvent pas être réservées temporairement, et une réservation provisoire ne peut pas combler une demande de ressource générique.

Les membres de l’équipe du projet réservés temporairement sont répertoriés sous l’onglet **Équipe** de la page **Projet**, avec leurs heures réservées temporairement affichées dans la colonne **Heures réservées temporairement** dans la vue **Membres de l’équipe nommés**. Les membres de l’équipe réservés temporairement sont également répertoriés dans le Tableau de planification. Du fait qu’ils sont réservés temporairement, le Tableau de planification n’affiche aucune consommation de capacité pour ces ressources. L’horaire réservé temporairement n’apparaît pas dans l’onglet **Rapprochement**, ni dans le champ **Étendre les réservations** de l’onglet **Rapprochement** du Tableau de planification. 

Il existe deux méthodes de réservation temporaire d’un membre d’équipe dans un projet : directement depuis le Tableau de planification, ou en ajoutant le membre de l’équipe dans l’onglet de **Équipe**. 

## <a name="soft-book-from-the-schedule-board"></a>Réserver temporairement depuis le Tableau de planification
Effectuez les étapes suivantes pour réserver temporairement à partir du Tableau de planification. 

1. Ouvrez le Tableau de planification, puis dans le volet **Besoins en réservations**, sélectionnez l’onglet **Projet**.
2. Recherchez le projet pour lequel réserver temporairement une ressource. S’il existe un grand nombre de projets dans la liste, sélectionnez l’en-tête de colonne **Projet**, puis utilisez le filtre pour rechercher un ou plusieurs projets.
3. Sélectionnez le projet, puis faites-le glisser-déplacer sur la grille de temps de la ressource.
5. Dans le volet **Créer la réservation de la ressource**, ajustez les dates de début et de fin, définissez le **Statut de réservation** sur **Temporaire**, puis définissez les heures. 
6. Cliquez sur **Réserver**. La ressource s’affiche à présent sous l’onglet **Équipe** en tant que ressource du projet. Sur la vue **Membre de l’équipe nommé**, vous verrez les heures réservées temporairement dans la colonne **Heures de réservation temporaire**.

> [!NOTE]
> Vous pouvez maintenant attribuer la ressource réservée temporairement aux tâches sous l’onglet **Planification**. Sous l’onglet **Rapprochement**, la ressource affiche un déficit d’attribution par rapport à ses attributions de tâches car l’onglet **Rapprochement** considère uniquement les réservations fermes. Vous pouvez utiliser la fonction **Étendre les réservations** pour réserver fermement la ressource afin de supprimer le déficit en réservations fermes par rapport aux attributions de ressources. Vous devrez annuler manuellement la réservation temporaire pour la ressource à l’aide de **Gérer les réservations**.

## <a name="soft-book-on-the-team-tab"></a>Réservation temporaire sur l’onglet Équipe

Vous pouvez ajouter des membres d’équipe directement sur l’onglet **Équipe**, puis modifiez leur statut d’attribution de **Ferme** à **Temporaire** avec **Gérer les réservations**. Lorsque vous ajoutez un membre de l’équipe ainsi, cela entraînera toujours une réservation ferme sauf si vous avez sélectionné la méthode d’attribution **Aucune**.

Pour utiliser ce mode, procédez comme suit.

1. Dans la page **Projet**, dans l’onglet **Équipe**, cliquez sur **Nouveau**.
2. Sélectionnez la ressources réservable, le rôle et les dates de début et de fin.
3. Sélectionnez une méthode d’attribution autre que **Aucune**.
4. Sélectionnez **Enregistrer**. Vous verrez la ressource sur la grille et ses heures dans la colonne **Heures réservées fermement**.
5. Gérez les réservations de la ressource en sélectionnant **Gérer les réservations**.
6. Lorsque le Tableau de planification s’ouvre, développez la ressource pour afficher ses réservations. Vous verrez la réservation affichée comme **Ferme**.
7. Cliquez avec le bouton droit sur la réservation, sous **Modifier le statut**, sélectionnez **Réservation temporaire** \> **Temporaire**. Le statut de la réservation est à présent **Temporaire**.
8. Après avoir fermé le Tableau de planification, vous verrez que les heures de la ressource ont été déplacées de la colonne **Heures réservées fermement** à **Heures réservées temporairement** dans la grille de l’onglet **Équipe**, dans la vue **Membres de l’équipe nommés**.

> [!NOTE]
> Lorsque vous utilisez la fonctionnalité **Gérer les réservations** pour modifier le statut de **Ferme** à **Temporaire**, si vous réservez fermement une ressource dans l’équipe et que vous lui attribuez des tâches, cela conserve les attributions de tâches de cette ressource. Toutefois, sous l’onglet **Rapprochement**, la ressource aura une insuffisance en réservation car seules les réservations fermes sont considérées lors du rapprochement des réservations avec les attributions. Vous pouvez utiliser la fonction **Étendre les réservations** sous l’onglet **Rapprochement** pour réserver fermement la ressource afin de supprimer le déficit en réservations fermes par rapport aux attributions de ressources. Vous devrez annuler la réservation temporaire pour la ressource à l’aide de **Gérer les réservations**.

Lorsque vous êtes prêt à passer une ressource de membre d’équipe réservée temporairement en ressource de membre d’équipe réservée fermement, procédez comme suit :

1. Sur le Tableau de planification, développez la ressource pour afficher ses réservations. Vous verrez la réservation affichée comme **Temporaire**.
2. Cliquez avec le bouton droit sur la réservation et sous **Modifier le statut**, sélectionnez **Réservation ferme** \> **Ferme**. Le statut de la réservation est à présent **Ferme**.
3. Après avoir fermé le Tableau de planification, revenez au projet et ouvrez l’onglet **Équipe**, vous verrez que les heures de la ressource ont été déplacées de la colonne **Heures réservées temporairement** à la colonne **Heures réservées fermement** dans la grille de l’onglet **Équipe**, dans la vue **Membres de l’équipe nommés**. Si la ressource a été attribuée aux tâches, elles n’affichent plus de déficit d’attribution sous l’onglet **Rapprochement**, car leurs réservations sont désormais fermes.



[!INCLUDE[footer-include](../includes/footer-banner.md)]