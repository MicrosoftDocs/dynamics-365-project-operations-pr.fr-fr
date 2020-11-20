---
title: Comment puis-je réserver temporairement les ressources dans la version 2.x de l’application ?
description: Cet article décrit comment réserver temporairement des membres de l’équipe du projet avec Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122250"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Comment puis-je réserver temporairement des ressources dans l’application Web (application Project Service v2.x) ?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vous pouvez planifier provisoirement ou réserver temporairement une ressource dans une équipe de projet pour indiquer que vous prévoyez d’attribuer la ressource à un projet. Les réservations temporaires ne consomment pas la capacité disponible d’une ressource. Les membres de l’équipe réservés temporairement ne peuvent pas être attribués à des tâches de projet. Seules les ressources avec le statut Réservé fermement et un type de validation Validé peuvent être attribuées aux tâches (si elles disposent d’heures de réservation ferme disponibles suffisantes pour couvrir un effort d’attribution).

Les membres de l’équipe de projet réservés temporairement s’affichent dans la grille du membre de l’équipe avec leurs heures réservées temporairement affichées dans la colonne Réservation temporaire. Ils s’affichent également sur le tableau de planification. Ici aussi, ils n’indiquent pas de consommation de capacité car la réservation temporaire ne consomme pas la capacité d’une ressource.

Il existe trois façons de réserver temporairement un membre d’équipe sur un projet avec la version 2.x. de Project Service. Vous pouvez réserver temporairement avec le tableau de planification, utiliser la fonctionnalité Gérer les réservations, ou créer une ressource générique. Ces méthodes sont décrites ci-dessous.

## <a name="soft-book-with-the-schedule-board"></a>Réserver temporairement avec le tableau de planification

Pour réserver temporairement avec le tableau de planification, suivez la procédure décrite ci-dessous : 
1. Ouvrez le tableau de planification.
2. Sélectionnez l’onglet Projet dans le volet inférieur Besoins en réservations du tableau de planification.
3. Recherchez le projet souhaité pour lequel réserver temporairement une ressource. Si vous avez beaucoup de projets, cliquez sur l’en-tête de colonne Projet et utilisez ensuite le filtre pour trouver votre projet.
4. Cliquez sur le projet, puis faites-le glisser-déplacer sur la grille de temps de la ressource.
5. Cette action génère l’ouverture du volet Créer une réservation de ressource sur la droite. Ajustez les dates de début et de fin, sélectionnez le statut de réservation comme temporaire et définir les heures. 
6. Cliquez sur Réserver.
7. Revenez au projet, la ressource s’affiche maintenant en tant que membre de l’équipe avec des heures de réservation temporaire dans la colonne Réservation temporaire.

Sachez que vous ne pouvez pas l’attribuer à des tâches de la structure de répartition du travail (WBS) car les ressources doivent être réservées fermement dans l’équipe pour être attribuées.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Réservation temporaire à l’aide de la fonctionnalité Gérer les réservations

Pour réserver temporairement avec la fonctionnalité Gérer les réservations, suivez la procédure décrite ci-dessous :
1. Dans la grille du membre de l’équipe, cliquez sur Nouveau.
2. Sélectionnez la ressources réservable, le rôle, du/au.
3. Sélectionnez une méthode d’attribution autre que Aucune :
- Capacité maximale
- Capacité du pourcentage
- Par heure - Distribuer de manière homogène
- Par heure - Chargement frontal
4. Cliquez sur Enregistrer. Vous verrez la ressource sur la grille de l’équipe et ses heures indiquées comme Fermes.
5. Gérez les réservations de la ressource en cliquant sur Gérer les réservations.
6. Lorsque le tableau de planification s’ouvre, développez la ressource pour afficher ses réservations. Vous verrez la réservation indiquée comme Ferme.
7. Cliquez avec le bouton droit sur la réservation, sous Modifier le statut, sélectionnez Réservation temporaire, puis Temporaire. Le statut de la réservation est à présent Temporaire.
8. Après avoir fermé le tableau de planification, vous verrez que les heures de la ressource sont passées de Ferme à Temporaire dans la grille du membre de l’équipe.
Notez que si vous réservez fermement une ressource dans l’équipe et que vous lui attribuez des tâches dans la WBS, lorsque vous utilisez la fonctionnalité Gérer les réservations pour modifier le statut de Ferme à Temporaire, cela supprime les attributions de tâches de cette ressource, car seules des ressources réservées fermement peuvent être attribuées aux tâches.

## <a name="soft-book-by-creating-a-generic-resource"></a>Réservation temporaire en créant une ressource générique

Vous pouvez créer une réservation temporaire en générant un membre d’équipe de ressource générique, en renseignant le tableau de planification ou la demande de ressources et en modifiant le type pendant la réservation.
Pour cela, effectuez les opérations suivantes :

1. Sur la WBS du projet, attribuez des rôles aux tâches pour lesquelles vous souhaitez générer des membres d’équipe génériques.
2. Cliquez sur Générer une équipe de projet.
3. Sur la grille du membre de l’équipe du projet, sélectionnez la ressource générique et cliquez sur Réserver.
4. Dans le tableau de planification, sélectionnez la ressource à réserver.
5. Sur le volet Créer une réservation de ressource du tableau de planification, modifiez le statut de réservation sur Temporaire.
6. Cliquez sur Réserver ou Réserver et quitter.

Après avoir fermé le tableau de planification, vous verrez la ressource sélectionnée ajoutée à l’équipe avec des heures réservées temporairement ainsi que les heures attribuées. Vous verrez également que la ressource générique reste dans l’équipe comme indicateur que les tâches sont attribuées à un membre de l’équipe en réservation temporaire.

Lorsque vous êtes prêt à passer une ressource de membre d’équipe réservée temporairement en ressource de membre d’équipe réservée fermement afin de pouvoir l’attribuer à des tâches, procédez comme suit :

1. Sélectionnez cette ressource et cliquez sur Gérer les réservations.
2. Lorsque le tableau de planification s’ouvre, développez la ressource pour afficher ses réservations. Vous verrez la réservation marquée comme Temporaire.
3. Cliquez avec le bouton droit sur la réservation, sous Modifier le statut, sélectionnez Réservation ferme, puis Ferme. Le statut de la réservation est à présent Ferme.
4. Après avoir fermé le tableau de planification, vous verrez que les heures de la ressource sont passées de Temporaire à Ferme dans la grille du membre de l’équipe. Vous pouvez désormais attribuer la ressource aux tâches (si les heures de réservation ferme coïncident avec les heures de travail de la tâche à l’attribution). Notez que si vous avez suivi les étapes d’exécution de la ressource générique dans l’élément n° 3 ci-dessus, lorsque vous modifiez le statut de la ressources réservable réservée temporairement à fermement, le membre de l’équipe générique est supprimé de l’équipe.
