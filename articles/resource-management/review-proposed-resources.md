---
title: Vérifier les ressources proposées
description: Cette rubrique explique comment proposer des ressources de projet.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897358"
---
# <a name="review-proposed-resources"></a>Vérifier les ressources proposées

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les gestionnaires de ressources peuvent proposer une ressource au chef de projet en utilisant une demande de ressource.

1. Dans la grille de demande ou la demande elle-même, sélectionnez **Rechercher des ressources**.
2. Dans la page **Assistant Planifier**, sélectionnez la ressource, puis, dans le volet **Créer une réservation de ressource**, dans le champ **Statut de la réservation**, sélectionnez **Réserver**.

Les mises à jour de statut suivantes se produisent :

- Dans la page **Assistant Planifier**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, mais pas réservée de manière ferme.
- Dans la demande de ressource, le statut passe à **Révision nécessaire**.
- Dans l'onglet **Équipe** du projet, la valeur **Statut de demande** du membre de l'équipe générique passe à **Révision nécessaire**.

Le chef du projet peut accepter ou rejeter la proposition.

Lorsque les gestionnaires de ressources gèrent les demandes de ressources, ils utilisent les méthodes suivantes :

- Proposer plusieurs ressources pour satisfaire la demande si aucune ressource n'est disponible pour satisfaire les heures obligatoires. Les heures proposées sont alors fractionnées entre plusieurs ressources qui peuvent satisfaire les heures obligatoires. Dans ce scénario, les heures ne peuvent pas se chevaucher.
- Proposer moins de ressources que requis. Dans ce scénario, la capacité en ressources est inférieure aux heures requises que le demandeur a spécifiées. Par conséquent, lorsque le demandeur accepte les ressources proposées, un besoin en ressources non atteint est créé pour capturer la demande restante.
- Réserver plusieurs ressources pour satisfaire la demande si aucune ressource n'est disponible pour terminer le travail.
- Réserver moins de ressources que requis. Dans ce scénario, les heures réservées sont inférieures aux heures requises. Le système vous guide pour proposer des ressources à la place de réservations, de sorte que le demandeur puisse vérifier et suivre la demande restante.

## <a name="billable-utilization"></a>Utilisation facturable

Les ressources peuvent avoir une utilisation facturable cible. Cette utilisation cible est définie comme un attribut dans le rôle par défaut d'une ressource ou sur l'enregistrement de la ressource réservable individuelle. Les calculs de l'utilisation sont basés sur les heures réelles que les ressources ont signalées à l'aide des entrées de temps approuvées.

Les formules suivantes sont utilisées pour calculer l'utilisation :

- Utilisation facturable = Heures réelles facturables ÷ Capacité ressource
- Utilisation non facturable = Temps réel avec ID type facturation = Capacité non facturable, gratuite ou non disponible ÷ Capacité ressource
- Interne = Temps réel sans contrat de vente ÷ Capacité ressource
- Capacité ressource = Heures de travail d'une ressource – Absence du bureau – Jours non ouvrables

Vous trouverez la vue **Utilisation des ressources** dans le volet **Ressources**.

Chaque cellule dans la grille représente le pourcentage total d'utilisation de la ressource à une période, par exemple un jour, une semaine ou un mois. Les formules suivantes sont utilisées pour colorer les cellules :

- **Vert :** Utilisation facturable \>= Utilisation cible de la ressource
- **Jaune :** Utilisation cible – 20 \<= Utilisation facturable \< Utilisation cible.
- **Rouge :** Utilisation facturable \< Utilisation cible - 20

Comme la vue **Utilisation des ressources** est basée sur le Tableau de planification, vous pouvez utiliser les fonctionnalités de filtrage du Tableau de planification pour filtrer vos résultats.

La grille nécessite que vous définissiez une utilisation cible du rôle ou de la ressource individuelle. Pour effectuer cette configuration, accédez à **Ressources** \> **Rôles des ressources**.

En outre, un rôle par défaut doit être affecté à chaque ressource réservable. Accédez à **Ressources** \> **Ressources**. Dans l'onglet **Project Service**, vérifiez qu'un rôle de ressource est défini, et que le champ **Est la valeur par défaut** est défini sur **Oui**. Vous pouvez ajouter des rôles supplémentaires où **Est la valeur par défaut = Non**. Le rôle où **Est la valeur par défaut = Oui** est utilisé pour évaluer l'utilisation de la ressource par rapport à la cible de ce rôle.

Dans l'onglet **Project Service**, vous pouvez également définir une utilisation cible individuelle pour la ressource. Le calcul de l'utilisation utilise ensuite cette utilisation cible pour évaluer la cible de la ressource au lieu de la cible du rôle par défaut de la ressource.

L'utilisation s'affiche pour une ressource uniquement si cette ressource est approuvée, temps facturable pendant la période affichée dans la grille.

## <a name="resource-availability"></a>La disponibilité des ressources

Il est donc impératif que les gestionnaires de ressources puissent afficher la disponibilité des ressources et mettre à jour les réservations. Dans certains cas, il n'existe aucune demande formelle (demande de ressource), mais un gestionnaire des ressources doit répondre à la demande non planifiée fournie par les canaux, par exemple le courrier électronique, l'appel téléphonique, ou un message instantané. Les gestionnaires de ressources utilisent le Tableau de planification pour mettre à jour les ressources et les réservations.

Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d'une ressource. Les réservations de ressource consomment la capacité des ressources.

Le Tableau de planification utilise des couleurs et de l'ombrage pour afficher les réservations, la disponibilité et les surréservations, ainsi que le statut des réservations. Un paramètre des paramètres du Tableau de planification vous permet d'afficher une légende.

Si une flèche pointant vers la droite apparaît en regard d'une ressource réservable individuelle sur le Tableau de planification, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.

Comme Dynamics 365 Project Operations utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.

Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte de ressource.

