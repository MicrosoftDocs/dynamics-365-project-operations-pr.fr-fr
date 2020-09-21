---
title: Attribuer une ressource à une tâche
description: Cette rubrique fournit des informations sur la façon d'attribuer des ressources aux tâches.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168155"
---
# <a name="assign-a-resource-to-a-task"></a>Attribuer une ressource à une tâche

Il existe trois méthodes pour attribuer une ressource à une tâche dans Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Réserver une ressource en tant que membre d'équipe, et l'attribuer à une tâche

Vous pouvez ajouter une ressource à l'équipe du projet, puis attribuez la ressource à des tâches dans la planification du projet.

1. Dans l'onglet **Membre de l'équipe**, ajoutez un nouveau membre de l'équipe en sélectionnant **Nouveau**. 

2. Le volet **Création rapide de membre d'équipe** s'ouvre, où sélectionnez le nom de la ressource réservable et définissez un rôle. 

    Sélectionnez un des modes d'attribution suivants pour la réservation de la ressource :

    - **Capacité maximale** réserve la capacité totale de la ressource pour les dates de début et de fin spécifiées.
    - **Capacité du pourcentage** réserva la ressource pour un pourcentage de la capacité de la ressource aux dates de début et de fin spécifiées.
    - **Par heure - Distribuer de manière homogène** réserve la ressource pour un nombre spécifique d'heures, la distribuant de manière homogène par jour pendant la période spécifiée.
    - **Par heure - Chargement frontal** réserve la ressource pour un nombre spécifique d'heures, chargeant frontalement les heures par jour pendant la période spécifiée.
    - **Aucune** ajoute la ressource à l'équipe mais ne crée aucune réservation qui absorbe la capacité de la ressource.

3. Dans la grille **Planification** d'une tâche, sélectionnez l'icône **Ressource** dans la cellule de la ressource, puis sous **Membres de l'équipe**, sélectionnez le membre de l'équipe que vous venez d'ajouter. 

> [!NOTE]
> Sous l'onglet **Membre de l'équipe** et l'onglet **Rapprochement**, la ressource affiche des heures réservées et attribuées. Les heures doivent être identiques, mais ce n'est pas obligatoire, car les réservations et les attributions ne sont pas couplées étroitement. L'onglet **Rapprochement** donne des détails lorsqu'elles sont différentes, comme lorsque vous attribuez à une ressource plus d'heures que vous en avez réservées. Au besoin, vous pouvez corriger les informations en étendant les réservations de la ressource ou en modifiant l'attribution.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Créer un membre de l'équipe générique via l'attribution de tâche

Lorsque vous créez un membre de l'équipe générique via l'attribution de tâche, vous créez un espace réservé ou une ressource générique qui décrit les caractéristiques de la ressource nommée que vous souhaitez travailler sur des tâches. Ensuite, vous générer un besoin (ou vous envoyez une demande à l'aide du besoin) utilisé pour rechercher et réserver la ressource nommée.

1. Dans la grille **Planification** d'une tâche, sélectionnez l'icône **Ressource** dans la cellule de la ressource.

2. Tapez un nom qui servira de nom pour la ressource d'espace réservé. Par exemple, Responsable du programme.

3. Sélectionnez **Créer** et dans le champ **Création rapide de membre d'équipe du projet**, définissez le rôle de la ressource générique.

4. Vous pouvez continuer d'attribuer des tâches à cette ressource d'espace réservé en sélectionnant la ressource dans le **Sélecteur de ressource** de la tâche. Elles sont répertoriées sous **Membres de l'équipe**.

5. Lorsque vous avez terminé d'attribuer la ressource générique, sélectionnez la ressource générique sur l'onglet **Équipe**, puis sélectionnez **Générer un besoin** pour créer un besoin en ressources pour la ressource générique.

6. Sélectionnez **Réserver** pour la ressource générique. Vous pouvez ensuite les utiliser le tableau Planification pour rechercher et réserver une ressource réelle. Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources.

7. Lorsque la ressource générique est exécutée avec une ressource nommée, la ressource générique est supprimée de l'équipe et les attributions de tâches pour la ressource générique sont attribuées à la ressource nommée qui a renseigné le besoin en ressources de la ressource générique.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Attribuer une ressource nommée dans la liste de toutes les ressources pouvant être réservées

Vous pouvez utiliser la zone de recherche dans le **Sélecteur de ressource** afin de rechercher toutes les ressources pouvant être réservées et les attribuer à une tâche.

Les ressources attribuées ainsi sont ajoutées à l'équipe sans aucune réservation. C'est similaire à ajouter un membre de l'équipe et à sélectionner Aucune comme mode de répartition. La ressource est affichée dans l'onglet **Équipe** et l'onglet **Rapprochement** en tant que ressources avec uniquement des attributions et un déficit de réservation. Réservez-les si vous souhaitez utiliser leur disponibilité.

1. Dans la grille **Planification** d'une tâche, sélectionnez l'icône **Ressource** dans la cellule de la ressource.

2. Commencez à entrer un nom. Les résultats de la recherche sur le nom s'affichent dans le **Sélecteur de ressource** sous **Autres ressources**.

3. Sélectionnez la ressource que vous souhaitez attribuer à la tâche.

