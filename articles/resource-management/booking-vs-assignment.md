---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130215"
---
# <a name="bookings-vs-assignments"></a>Réservations et Affectations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet. Les réservations fermes consomment la capacité d’une ressource. Les réservations représentent des concepts organisationnels pour les équipes afin qu’elles comprennent comment les ressources seront engagées dans divers projets. Dynamics 365 Project Operations considère les réservations comme un concept au niveau du projet. 

Contrairement aux réservations, les attributions sont l’engagement de ressources aux tâches d’un projet dans la planification du projet. Les ressources peuvent être nommées ou génériques. 

En règle générale, la somme des réservations d’une ressource sera égale à la somme des affectations de la ressource pour une ou plusieurs tâches. Toutefois, Project Operations n’applique pas cette mise en correspondance. La vue **Rapprochement** affiche au chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.
