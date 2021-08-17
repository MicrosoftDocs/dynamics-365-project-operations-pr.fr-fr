---
title: Vue d’ensemble du rapprochement des ressources
description: Cette rubrique fournit des informations qui vous aideront à vous assurer que les réservations de ressources et les affectations pour les projets sont alignées.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1542e97955902486d22ca637514e4e121fae70e2b227cafc7020c031061b5f98
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994768"
---
# <a name="resource-reconciliation-overview"></a>Vue d’ensemble du rapprochement des ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Pour les membres de l’équipe, les réservations et les attributions sont légèrement couplées. En d’autres termes, les ressources peuvent avoir des attributions et aucune réservation, ou elles peuvent avoir des réservations et aucune attribution. Idéalement, certaines réservation et attributions doivent être alignées, de sorte que les ressources aient une capacité engagée à effectuer les affectations des tâches. Cependant, les réservations peuvent être basées sur la disponibilité et les calendriers des tâches peuvent changer à mesure que le projet se poursuit. Par conséquent, le couplage léger des réservations ou des attributions procurent de la flexibilité.

L’onglet **Rapprochement** sur la page **Projets** permet aux chefs de projet de rapprocher les réservations des membres de l’équipe et leurs attributions pour les équipes de projet.

L’onglet **Rapprochement** affiche des réservations et attributions jusqu’au niveau de l’affectation de tâches individuelles à chaque membre de l’équipe. Les heures sont indiquées dans cellules pouvant représenter des périodes allant des mois à des jours. L’onglet affiche également un total net général pour le projet, conjointement à une colonne **Totale**.

Pour chaque ressource, l’onglet **Rapprochement** calcule la distinction entre les réservations du membre de l’équipe et un report des affectations des tâches du membre de cette équipe. Idéalement, cette différence doit être de 0 (zéro). En d’autres termes, il ne doit exister aucune différence entre les réservations et les attributions. Les différences sont en couleur et grisées pour attirer l’attention sur deux conditions :

- **Pénurie de réservation** – Une pénurie de réservation se produit lorsque la ressource a plus d’attributions que de réservations. La capacité n’ayant pas été réservée, le chef de projet peut également corriger cette condition en étendant les réservations de la ressource pour compenser la pénurie.
- **Réservations en trop** - Une réservation excessive se produit lorsque la ressource a été réservée pour le projet, mais n’a pas été affectée à des tâches. Cette condition peut être acceptable dans les cas où la ressource a été réservée dans le projet avant que l’affectation de tâches se soit produite. Cependant, dans d’autres cas, où il n’est pas prévu d’affecter la ressource à des tâches, le chef de projet doit envisager d’annuler les réservations de la ressource. De cette manière, la capacité peut être utilisée pour un autre projet.

Dans certains cas, lorsque vous affichez le temps à un niveau supérieur que le niveau du jour (par exemple, le niveau de mois), vous pouvez voir une différence nette de zéro pour une ressource (en d’autres termes, réservations égale attributions). Toutefois, si vous affichez le temps au niveau de la semaine, vous pouvez voir des attributions de zéro heure et des réservations de 40 heures au cours de la première semaine, mais des attributions de 40 heures et des réservations de zéro heure dans la deuxième semaine. Globalement, les réservations et attributions sont rapprochées, mais elles ne correspondent pas d’une semaine à l’autre.

Lorsque vous affichez le temps à des niveaux plus élevés, les cellules sous l’onglet **Rapprochement** ont un indicateur pour vous informer qu’il existe des différences à des niveaux plus bas. En appuyant deux fois ou en double-cliquant sur une cellule, vous pouvez faire un zoom avant pour afficher la différence. Vous pouvez ensuite sélectionner et maintenir (ou cliquer avec le bouton droit) pour faire un zoom arrière. En sélectionnant une ressource puis en utilisant le contrôle **Différence suivante** dans la barre d’outils de la grille, vous pouvez passer à la prochaine différence entre les réservations et les affectations d’une ressource. Vous pouvez ensuite utiliser le contrôle **Différence précédente** pour revenir. Vous pouvez également désactiver l’indicateur de différence et le comportement de navigation sous **Paramètres**.

Si vous avez des affectations de tâches pour une ressource mais aucune réservation, sélectionnez la pénurie de réservation sur l’onglet **Rapprochement**, de la page **Projets**, puis sélectionnez **Étendre la réservation**. La boîte de dialogue **Étendre la réservation** qui s’affiche indique la réservation qui est obligatoire pour compenser la pénurie de la ressource. La boîte de dialogue présente également les réservations existantes de la ressource dans tous les projets ou d’autres entités planifiables. Si vous sélectionnez **OK** pour créer la réservation pour la ressource, indépendamment de la disponibilité de cette ressource, vous pouvez entraîner de la surréservation.

Les réservations créées via l’action **Prolonger la réservation** sont associées à l’exigence principale du projet. Lorsqu’une extension est lancée, l’exigence spécifique qui doit être étendue ne peut pas être déterminée, car la ressource peut être associée à plusieurs exigences pour le projet.

Le chef de projet ou le gestionnaire de ressources peut ensuite utiliser le Tableau de planification pour gérer tous les cas où une ressource est réservée en trop au-delà de sa capacité.


[!INCLUDE[footer-include](../includes/footer-banner.md)]