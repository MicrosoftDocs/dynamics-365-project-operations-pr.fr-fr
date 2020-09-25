---
title: Proposer des ressources de projet
description: Cette rubrique explique comment proposer des ressource de projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168131"
---
# <a name="propose-project-resources"></a>Proposer des ressources de projet

Les gestionnaires de ressources peuvent proposer une ressource au chef de projet en utilisant une demande de ressource.

1. Dans la grille de demande ou la demande elle-même, sélectionnez **Rechercher des ressources**.
2. Dans la page **Assistant Planifier**, sélectionnez la ressource, puis, dans le volet **Créer une réservation de ressource**, dans le champ **Statut de la réservation**, sélectionnez **Réserver**.

    ![Ressource sélectionnée proposée](media/Resource-Management-image62.png)

Les mises à jour de statut suivantes se produisent :

- Dans la page **Assistant Planifier**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, mais pas réservée de manière ferme.

    ![Indicateurs de statut des réservations proposées sur la page Assistant Planifier](media/Resource-Management-image63.png)

- Dans la demande de ressource, le statut passe à **Révision nécessaire**.

    ![Statut de la demande de ressource passé à Révision nécessaire](media/Resource-Management-image64.png)

- Dans l'onglet **Équipe** du projet, la valeur **Statut de demande** du membre de l'équipe générique passe à **Révision nécessaire**.

    ![Statut de demande du membre de l'équipe générique passé à Révision nécessaire sous l'onglet Équipe](media/Resource-Management-image48.png)

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

![Vue Utilisation des ressources](media/Resource-Management-image65.png)

Chaque cellule dans la grille représente le pourcentage total d'utilisation de la ressource à une période, par exemple un jour, une semaine ou un mois. Les formules suivantes sont utilisées pour colorer les cellules :

- **Vert :** Utilisation facturable \>= Utilisation cible de la ressource
- **Jaune :** Utilisation cible – 20 \<= Utilisation facturable \< Utilisation cible.
- **Rouge :** Utilisation facturable \< Utilisation cible - 20

Comme la vue **Utilisation des ressources** est basée sur le Tableau de planification, vous pouvez utiliser les fonctionnalités de filtrage du Tableau de planification pour filtrer vos résultats.

La grille nécessite que vous définissiez une utilisation cible du rôle ou de la ressource individuelle. Pour effectuer cette configuration, accédez à **Ressources** \> **Rôles des ressources**.

En outre, un rôle par défaut doit être affecté à chaque ressource réservable. Accédez à **Ressources** \> **Ressources**. Dans l'onglet **Project Service**, vérifiez qu'un rôle de ressource est défini, et que le champ **Est la valeur par défaut** est défini sur **Oui**. Vous pouvez ajouter des rôles supplémentaires où **Est la valeur par défaut = Non**. Le rôle où **Est la valeur par défaut = Oui** est utilisé pour évaluer l'utilisation de la ressource par rapport à la cible de ce rôle.

![Rôle par défaut défini](media/Resource-Management-image67.png)

Dans l'onglet **Project Service**, vous pouvez également définir une utilisation cible individuelle pour la ressource. Le calcul de l'utilisation utilise ensuite cette utilisation cible pour évaluer la cible de la ressource au lieu de la cible du rôle par défaut de la ressource.

L'utilisation s'affiche pour une ressource uniquement si cette ressource est approuvée, temps facturable pendant la période affichée dans la grille.

## <a name="resource-availability"></a>La disponibilité des ressources

Il est donc impératif que les gestionnaires de ressources puissent afficher la disponibilité des ressources et mettre à jour les réservations. Dans certains cas, il n'existe aucune demande formelle (demande de ressource), mais un gestionnaire des ressources doit répondre à la demande non planifiée fournie par les canaux, par exemple le courrier électronique, l'appel téléphonique, ou un message instantané. Les gestionnaires de ressources utilisent le Tableau de planification pour mettre à jour les ressources et les réservations.

Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d'une ressource. Les réservations de ressource consomment la capacité des ressources.

![Tableau de planification](media/Resource-Management-image68.png)

Le Tableau de planification utilise des couleurs et de l'ombrage pour afficher les réservations,la disponibilité et les surréservations, ainsi que le statut des réservations. Un paramètre des paramètres du Tableau de planification vous permet d'afficher une légende.

Si une flèche pointant vers la droite apparaît en regard d'une ressource réservable individuelle sur le Tableau de planification, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.

![Ressource réservable développée sur le Tableau de planification](media/Resource-Management-image69.png)

Comme Dynamics 365 Project Service Automation utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.

![Détails des réservations de ressource pour les projets et les ordres de travail](media/Resource-Management-image70.png)

Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte de ressource.

![Carte de ressource](media/Resource-Management-image71.png)