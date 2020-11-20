---
title: Vérifier les ressources proposées
description: Cette rubrique explique comment proposer des ressources de projet.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401170"
---
# <a name="review-proposed-resources"></a>Vérifier les ressources proposées

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les gestionnaires de ressources peuvent proposer une ressource au chef de projet en utilisant une demande de ressource.

1. Dans la grille de demande ou la demande elle-même, sélectionnez **Rechercher des ressources**.
2. Dans la page **Assistant Planifier**, sélectionnez la ressource, puis, dans le volet **Créer une réservation de ressource**, dans le champ **Statut de la réservation**, sélectionnez **Réserver**.

Les mises à jour de statut suivantes se produisent :

- Dans la page **Assistant Planifier**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, mais pas réservée de manière ferme.
- Dans la demande de ressource, le statut passe à **Révision nécessaire**.
- Dans l’onglet **Équipe** du projet, la valeur **Statut de demande** du membre de l’équipe générique passe à **Révision nécessaire**.

Le chef du projet peut accepter ou rejeter la proposition.

Lorsque les gestionnaires de ressources gèrent les demandes de ressources, ils utilisent les méthodes suivantes :

- Proposer plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour satisfaire les heures obligatoires. Les heures proposées sont alors fractionnées entre plusieurs ressources qui peuvent satisfaire les heures obligatoires. Dans ce scénario, les heures ne peuvent pas se chevaucher.
- Proposer moins de ressources que requis. Dans ce scénario, la capacité en ressources est inférieure aux heures requises que le demandeur a spécifiées. Par conséquent, lorsque le demandeur accepte les ressources proposées, un besoin en ressources non atteint est créé pour capturer la demande restante.
- Réserver plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour terminer le travail.
- Réserver moins de ressources que requis. Dans ce scénario, les heures réservées sont inférieures aux heures requises. Le système vous guide pour proposer des ressources à la place de réservations, de sorte que le demandeur puisse vérifier et suivre la demande restante.

## <a name="resource-availability"></a>La disponibilité des ressources

Il est donc impératif que les gestionnaires de ressources puissent afficher la disponibilité des ressources et mettre à jour les réservations. Dans certains cas, il n’existe aucune demande formelle (demande de ressource), mais un gestionnaire des ressources doit répondre à la demande non planifiée fournie par les canaux, par exemple le courrier électronique, l’appel téléphonique, ou un message instantané. Les gestionnaires de ressources utilisent le Tableau de planification pour mettre à jour les ressources et les réservations.

Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d’une ressource. Les réservations de ressource consomment la capacité des ressources.

Le Tableau de planification utilise des couleurs et de l’ombrage pour afficher les réservations, la disponibilité et les surréservations, ainsi que le statut des réservations. Un paramètre des paramètres du Tableau de planification vous permet d’afficher une légende.

Si une flèche pointant vers la droite apparaît en regard d’une ressource réservable individuelle sur le Tableau de planification, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.

Comme Dynamics 365 Project Operations utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.

Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte de ressource.

