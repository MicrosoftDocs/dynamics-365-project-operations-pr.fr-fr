---
title: Créer une équipe de projet
description: Cette rubrique donne des informations sur la création et la gestion d'équipes de projet.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075905"
---
# <a name="create-a-project-team"></a>Créer une équipe de projet

[!include [banner](../includes/banner.md)]

Pour utiliser les rôles précédemment définis dans un projet, un chef de projet doit associer les rôles au projet. Plusieurs rôles peuvent être attribués à un projet. Pour éviter toute confusion, ces rôles sont automatiquement étiquetés lors de la réservation. Par exemple, si le chef de projet a besoin de trois ingénieurs en logiciel, trois rôles d’ingénieur en logiciel **ingénieur logiciel 1** , **ingénieur logiciel 2** et **ingénieur logiciel 3** , car leurs étiquettes sont automatiquement générées. Si des caractéristiques de rôle ont été précédemment définies pour le rôle, elles sont appliquées en tant que filtre lors des recherches d’une ressource. Des caractéristiques supplémentaires peuvent être ajoutées si nécessaire pour affiner davantage la recherche.

Les paramètres d’affichage peuvent également être personnalisés pour offrir une meilleure vue de la disponibilité des ressources. Il existe des options pour afficher la disponibilité horaire, quotidienne, hebdomadaire, mensuelle, trimestrielle et annuelle. Il existe également une option pour afficher la capacité disponible et restante sur les ressources. Cette option est utile pour la gestion du temps, lorsque vous estimez le temps disponible pour les activités ou la disponibilité des ressources.

Le chef de projet peut sélectionner un rôle sur la page, puis, s’il existe une ressource disponible qui répond à l’exigence, choisir de réserver une ressource pour remplir le rôle. Notez que les ressources ne doivent pas être réservées à ce stade de la phase de planification. Lorsque vous créez une structure de répartition du travail, vous pouvez remplacer les rôles par des ressources en personnel pour le projet. Si les rôles sont remplacés par des ressources dotées de personnel dans la structure de répartition du travail, la configuration des ressources met automatiquement à jour la liste et la planification de l’équipe de projet.

[![Liste des équipes de projet qui comprend à la fois les rôles et les ressources réelles](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Le chef de projet dispose de différentes options pour réserver une ressource pour un projet, telles que **Capacité restante** , **Capacité complète** , **Pourcentage de capacité** et **Préciser les heures**. Ces options de réservation peuvent être annulées à tout moment si les affectations de ressources changent. Deux types de réservation sont pris en charge :

- **Réservation ferme**  : la réservation de ressources a été approuvée et confirmée pour travailler sur l’engagement pour la durée spécifiée.
- **Réservation temporaire**  : les réservations de ressources était provisoirement défini pour travailler sur l’engagement pour la durée spécifiée.

La procédure suivante explique comment créer une équipe de projet.

## <a name="create-a-project-team"></a>Créer une équipe de projet

1. Sur la liste **Tous les projets** , sélectionnez un projet, puis **Modifier**.
2. Sur l’onglet **Équipe de projet et planification** , dans le champ **Date de fin de planification** , entrez la date de début de planification plus un mois. Par exemple, si la date de début de la planification est le 24 juin 2017 (24/06/2017), entrez **24/07/2017**.
3. Cliquez sur **Ajouter**.
4. Dans le volet **Ajouter des rôles au projet** , dans le champ **Rôle** , sélectionnez **Chef de projet senior**.
5. Sélectionnez **Compétences requises**.
6. Sur la page **Choisir les caractéristiques** , les caractéristiques que vous avez précédemment définies pour le rôle de chef de projet senior sont sélectionnées par défaut. Cliquez sur **OK**.
7. Sur la page **Ajouter des rôles au projet** , dans le champ **Nombre de ressources** , entrez **1**.
8. Dans le champ **Ressource** , la recherche affiche toutes les ressources possédant les compétences requises. Sélectionnez **Daniel Goldschmidt** , puis sélectionnez **Créer**.
9. Sélectionnez **Ajouter** sur la page **Projet**.
10. Dans le volet **Ajouter des rôles au projet** , dans le champ **Rôle** , sélectionnez **Membre de l’équipe**. Tapez **5** dans le champ **Nombre de ressources**.
11. Sélectionnez **Créer**.
12. Sur la page **Projets** , sélectionnez **Répondre à la ressource**.

## <a name="monitor-project-teams"></a>Surveiller les équipes de projet
1. Sur la page **Tous les projets** , sélectionnez l’ **ID de projet** pour le projet **Mise à niveau XYZ Phase 2**.
2. Sur le raccourci **Équipe de projet et planification** , vérifiez que les ressources de projet répertoriées sont correctes.
