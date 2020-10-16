---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896008"
---
# <a name="bookings-vs-assignments"></a>Réservations et Affectations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet. Les réservations fermes consomment la capacité d’une ressource. 

Les attributions sont l’attribution de ressources aux tâches d’un projet dans la planification du projet. Les ressources peuvent être réelles ou génériques. 

Idéalement, pour les ressources réelles, les réservations et les affectations doivent correspondre, car elles ne peuvent pas différer. Toutefois, Microsoft Dynamics Project Operations n’applique pas cette mise en correspondance. La vue **Rapprochement** affiche à un chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.
