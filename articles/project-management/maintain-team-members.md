---
title: Préserver les membres de l’équipe
description: Cette rubrique fournit des informations sur la réservation de ressources nommées dans les équipes de projet et leur attribution de tâches.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075606"
---
# <a name="maintain-team-members"></a>Préserver les membres de l’équipe

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez ajouter une ressource nommée à votre équipe de projet en les réservant directement dans l’équipe.

1. Dans Dynamics 365 Project Operations, accédez à **Projets** , puis sélectionnez pour ouvrir le projet que réservez.
2. Dans la page **Projet** , dans l’onglet **Équipe** , sélectionnez **Nouveau**. 
3. Dans la boîte de dialogue **Création rapide : Membre de l’équipe de projet** , sélectionnez la ressource réservable. Le champ **Rôle** se remplit avec le rôle par défaut de la ressource si elle en a un d’attribué. Vous pouvez changer de rôle. 
4. Sélectionnez les dates de début et de fin auxquelles la ressource sera nécessaire et sélectionnez la méthode d’allocation de la capacité de la ressource. 
5. Sélectionnez **Oui** dans le champ **Approbateur du projet** si vous voulez que le membre de l’équipe soit un approbateur de projet. Le membre de l’équipe peut approuver les entrées de temps et de dépenses envoyées pour ce projet. 
6. Sélectionnez **Enregistrer**.

Vous pouvez désormais attribuer la ressource réservée aux tâches sur le projet. Dans la page **Projet** , sur l’onglet **Planification** , attribuez des tâches à la nouvelle ressource. Le sélecteur de ressources lancé à partir du champ **Ressources** dans la grille de tâches affichera les membres de l’équipe que vous pouvez sélectionner.


Dans Project Operations, les réservations de ressources et les affectations de tâches ne sont pas étroitement liées. Si vous utilisez le sélecteur de ressources dans la planification, vous pouvez attribuer des tâches aux membres de l’équipe pour plus d’heures que leurs réservation n’en couvre.

Les différences entre les réservations et les affectations des membres de l’équipe sont indiquées sur les onglets **Équipe** et **Rapprochement des ressources**. Vous pouvez également rapprocher les différences entre les réservations et les affectations de ressources à un niveau plus détaillé.

Utilisez le sélecteur de ressources sur l’onglet **Planification** pour rechercher et sélectionner les ressources réservables qui ne font pas déjà partie de l’équipe du projet. Ces ressources sont affichées dans le sélecteur de ressources comme **Autres ressources**.

Une fois que vous effectuez une sélection, la ressource est ajoutée à l’équipe du projet et attribuée à la tâche, mais aucune réservation n’est générée.

Vous pouvez utiliser la capacité d’extension de réservation de l’onglet **Rapprochement** ou le **Tableau de planification** pour réserver la capacité de la ressource sur le projet.

Lorsqu’un membre de l’équipe est réservé sur votre projet, vous pouvez **Gérer les réservations** ou utiliser le **Tableau de planification** directement pour gérer ses réservations.
