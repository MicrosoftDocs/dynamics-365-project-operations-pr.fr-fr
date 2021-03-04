---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841169"
---
# <a name="bookings-vs-assignments"></a>Réservations et Affectations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet. Les réservations fixes consomment la capacité d’une ressource. Les réservations représentent des concepts organisationnels pour les équipes, afin qu’elles puissent comprendre comment les ressources seront impliquées dans divers projets. Dynamics 365 Project Operations prend en compte les réservations en tant que concept au niveau du projet. 

Contrairement aux réservations, les affectations désignent l’engagement de ressources sur des tâches de projet dans le calendrier de projet. Les ressources peuvent être nommées ou génériques.  Lorsqu'un besoin en ressources est dérivé des affectations de tâches de projet, Project Operations utilise les contours d'effort de l'affectation de ressources pour créer les contours des détails des besoins en ressources. Cependant, une référence aux affectations de ressources n'est pas conservée. Les mises à jour des réservations dérivées des besoins en ressources ne mettent pas à jour les affectations de ressources.

En règle générale, la somme des réservations pour une ressource est égale à la somme des affectations de la ressource sur une ou plusieurs tâches. Toutefois, Project Operations n’applique pas cette mise en correspondance. La vue **Rapprochement** affiche au chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.


