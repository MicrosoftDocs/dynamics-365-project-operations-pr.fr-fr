---
title: Créer des attributions de ressources
description: Cet article fournit des informations sur la création d’affectations de ressources génériques et nommées.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811990"
---
# <a name="create-resource-assignments"></a>Créer des attributions de ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Une affectation de ressource est l’association directe d’un membre de l’équipe de projet à une tâche de nœud terminal. Cet article fournit des informations sur les différentes moyens d’affecter des ressources.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Créer un membre de l’équipe générique via l’attribution de tâche


Lorsque vous créez un membre d’équipe générique via l’affectation de tâches, vous créez un espace réservé ou une ressource générique. Cette ressource générique décrit les caractéristiques de la ressource nommée que vous souhaitez voir travailler sur des tâches. Ensuite, vous générer un besoin, ou vous envoyez une demande à l’aide du besoin utilisé pour rechercher et réserver la ressource nommée.

1. Dans la grille Planification d’une tâche, sélectionnez l’icône Ressource dans la cellule **Ressource**.
2. Tapez un nom qui servira de nom pour la ressource d’espace réservé. Par exemple, Responsable du programme.
3. Sélectionnez **Créer** et dans le champ **Création rapide de membre d’équipe du projet**, définissez le rôle de la ressource générique.
4. Attribuez des tâches au besoin à cette ressource d’espace réservé en sélectionnant la ressource dans le **Sélecteur de ressource** de la tâche. Les ressoures sont répertoriées sous **Membres de l’équipe**.
5. Lorsque vous avez terminé d’attribuer la ressource générique, sélectionnez la ressource générique sur l’onglet **Équipe**, sélectionnez la ressource générique, puis **Générer un besoin** pour créer un besoin en ressources pour la ressource générique.
6. Sélectionnez **Réserver** pour la ressource générique, puis utilisez le Tableau de planification pour rechercher et réserver une ressource réelle. Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources.
7. Une fois la ressource générique intégralement satisfaite avec une ressource nommée, la ressource générique est retirée de l’équipe. (La satisfaction partielle des besoins en ressources ne résultera pas en une affectation de ressource.) Les affectations de tâche pour la ressource générique sont affectées à la ressource nommée ayant satisfait le besoin en ressource de la ressource générique.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Attribuer une ressource nommée dans la liste de toutes les ressources pouvant être réservées

Vous pouvez utiliser la zone de recherche dans le **Sélecteur de ressource** afin de rechercher toutes les ressources pouvant être réservées actives et les attribuer à une tâche de nœud terminal. Les ressources attribuées ainsi sont ajoutées à l’équipe sans aucune réservation. C’est similaire à ajouter un membre de l’équipe et à sélectionner **Aucune** comme mode de répartition. La ressource est affichée dans les onglets **Équipe**, **Affectation de ressource** et **Rapprochement** en tant que ressources avec uniquement des attributions et un déficit de réservation. Réservez-les si vous souhaitez utiliser leur disponibilité.

1. À partir de la grille des tâches, du tableau ou de la chronologie, accédez à la cellule **Affecté à**.
2. Dans la zone de recherche, commencez à saisir un nom. Les résultats de la recherche sur le nom s’affichent dans le **Sélecteur de ressource** sous **Autres ressources**.
3. Sélectionnez la ressource que vous souhaitez affecter à la tâche ou sélectionnez le nom de la ressource sous **Autres ressources d’équipe**.

## <a name="editing-resource-assignment-contours"></a>Modification des contours d’affectation des ressources

Par défaut, lorsque des ressources sont affectées à une tâche dans la planification, leur effort est distribué de manière linéaire à chaque ressource, en fonction des heures de travail de cette ressource et du mode de planification du projet. Un chef de projet peut utiliser la grille d’affectation des ressources pour affiner les estimations d’effort de chaque ressource affectée à une ou plusieurs tâches sur les différentes échelles de temps. Cette fonctionnalité aide les chefs de projet à produire des estimations de coûts et de ventes plus précises, qui sont déterminées par les contours d’affectation des ressources générés lorsqu’une ressource est affectée à une tâche. En outre, les chefs de projet peuvent plus facilement refléter la demande de ressources nécessaire pour générer la demande dans un besoin en ressources.

### <a name="navigation"></a>Navigation

Pour accéder à la grille d’édition des contours, le chef de projet sélectionne d’abord l’onglet **Tâches** sur la page principale du projet, puis sélectionne l’onglet **Affectations**.

![Onglet Affectations dans l’onglet Tâches de la page principale du projet.](media/AssignmentGrid.png)

La grille prend en charge deux méthodes de regroupement : **regrouper par ressource** et **regrouper par tâche**. Contrairement à la vue de grille, les colonnes ne sont pas configurables. Les seules colonnes visibles sont **Affecté à**, **Nom de tâche**, **Début de l’affectation**, **Fin de l’affectation** et **Effort d’affectation**.

Lorsque la grille est initialement rendue, elle commence au premier contour d’affectation. Si votre planification ne contient aucune affectation nécessitant un effort, la grille reste vide et n’affiche rien.

![Grille d’affectation vierge.](media/emptyassignmentgrid.png)

Si vous souhaitez visualiser vos contours et différentes échelles de temps, la grille d’affectation des ressources et la grille de réconciliation des ressources en lecture seule sont également disponibles.

### <a name="resource-calendars"></a>Calendriers de la ressource

La possibilité de modifier un contour pour un jour spécifique est régie par les jours ouvrables de la ressource, comme indiqué dans son calendrier. Si une cellule est désactivée pour une ressource donnée, cette ressource n’a pas de jours ouvrables pendant cette période.

Les contours d’une ressource peuvent s’étendre au-delà des dates de début et de fin actuelles de la tâche affectée. Si un contour est mis à jour de sorte qu’il soit postérieur à la date de fin la plus tardive d’une tâche ou à la date de début la plus ancienne d’une tâche, la date de fin ou la date de début de la tâche est modifiée selon le cas. Toutefois, si un contour est mis à jour de sorte qu’il soit antérieur à la date de début d’une tâche liée à un prédécesseur, la mise à jour échoue, car l’affectation déclenche le démarrage de la tâche avant que son prédécesseur ne soit terminé, et ce comportement n’est actuellement pas pris en charge.

### <a name="co-authoring"></a>Co-création

Les modifications apportées à la grille d’affectation des ressources sont automatiquement reflétées dans toutes les vues associées, y compris les vues de graphique, de chronologie, de tableau et de grille. Si plusieurs utilisateurs révisent le projet en même temps, toutes les modifications apportées par un utilisateur sont indiquées dans la grille. À l’inverse, toutes les modifications apportées à la grille d’affectation des ressources sont présentées à tous les autres utilisateurs qui visualisent le projet dans la même session.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
