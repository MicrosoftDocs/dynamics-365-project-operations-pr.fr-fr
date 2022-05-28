---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591263"
---
# <a name="bookings-vs-assignments"></a>Réservations et Affectations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet. Les réservations fixes consomment la capacité d’une ressource. Les réservations représentent des concepts organisationnels pour les équipes, afin qu’elles puissent comprendre comment les ressources seront impliquées dans divers projets. Dynamics 365 Project Operations prend en compte les réservations en tant que concept au niveau du projet. 

Contrairement aux réservations, les affectations désignent l’engagement de ressources sur des tâches de projet dans le calendrier de projet. Les ressources peuvent être nommées ou génériques.  Lorsqu’un besoin en ressources est dérivé des affectations de tâches de projet, Project Operations utilise les contours d’effort de l’affectation de ressources pour créer les contours des détails des besoins en ressources. Cependant, une référence aux affectations de ressources n’est pas conservée. Les mises à jour des réservations dérivées des besoins en ressources ne mettent pas à jour les affectations de ressources.

En règle générale, la somme des réservations pour une ressource est égale à la somme des affectations de la ressource sur une ou plusieurs tâches. Toutefois, Project Operations n’applique pas cette mise en correspondance. La vue **Rapprochement** affiche au chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.




[!INCLUDE[footer-include](../includes/footer-banner.md)]