---
title: Créer des attributions de ressources
description: Cette rubrique fournit des informations sur la création d’affectations de ressources génériques et nommées.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075653"
---
# <a name="create-resource-assignments"></a>Créer des attributions de ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Une affectation de ressource est l’association directe d’un membre de l’équipe de projet à une tâche de nœud terminal. Cette rubrique fournit des informations sur les différentes façons d’attribuer des ressources.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Créer un membre de l’équipe générique via l’attribution de tâche


Lorsque vous créez un membre d’équipe générique via l’affectation de tâches, vous créez un espace réservé ou une ressource générique. Cette ressource générique décrit les caractéristiques de la ressource nommée que vous souhaitez voir travailler sur des tâches. Ensuite, vous générer un besoin, ou vous envoyez une demande à l’aide du besoin, utilisé pour rechercher et réserver la ressource nommée.

1. Dans la grille Planification d’une tâche, sélectionnez l’icône Ressource dans la cellule **Ressource**.
2. Tapez un nom qui servira de nom pour la ressource d’espace réservé. Par exemple, Responsable du programme.
3. Sélectionnez **Créer** et dans le champ **Création rapide de membre d’équipe du projet** , définissez le rôle de la ressource générique.
4. Attribuez des tâches au besoin à cette ressource d’espace réservé en sélectionnant la ressource dans le **Sélecteur de ressource** de la tâche. Les ressoures sont répertoriées sous **Membres de l’équipe**.
5. Lorsque vous avez terminé d’attribuer la ressource générique, sélectionnez la ressource générique sur l’onglet **Équipe** , sélectionnez la ressource générique, puis **Générer un besoin** pour créer un besoin en ressources pour la ressource générique.
6. Sélectionnez **Réserver** pour la ressource générique, puis utilisez le Tableau de planification pour rechercher et réserver une ressource réelle. Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources.
7. Lorsque la ressource générique est entièrement remplie (la satisfaction partielle des besoins en ressources ne résultera pas en une affectation de ressource) avec une ressource nommée, la ressource générique est supprimée de l’équipe. Les affectations de tâches pour la ressource générique sont affectées à la ressource nommée qui répond aux besoins en ressources de la ressource générique.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Attribuer une ressource nommée dans la liste de toutes les ressources pouvant être réservées

Vous pouvez utiliser la zone de recherche dans le **Sélecteur de ressource** afin de rechercher toutes les ressources pouvant être réservées actives et les attribuer à une tâche de nœud terminal. Les ressources attribuées ainsi sont ajoutées à l’équipe sans aucune réservation. C’est similaire à ajouter un membre de l’équipe et à sélectionner **Aucune** comme mode de répartition. La ressource est affichée dans les onglets **Équipe** , **Affectation de ressource** et **Rapprochement** en tant que ressources avec uniquement des attributions et un déficit de réservation. Réservez-les si vous souhaitez utiliser leur disponibilité.

1. À partir de la grille des tâches, du tableau ou de la chronologie, accédez à la cellule **Affecté à**.
2. Dans la zone de recherche, commencez à saisir un nom. Les résultats de la recherche sur le nom s’affichent dans le **Sélecteur de ressource** sous **Autres ressources**.
3. Sélectionnez la ressource que vous souhaitez affecter à la tâche ou sélectionnez le nom de la ressource sous **Autres ressources d’équipe**.
