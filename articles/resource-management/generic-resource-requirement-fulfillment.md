---
title: Répondre aux besoins en ressources génériques
description: Cette rubrique fournit des informations sur le mode de réservation des ressources nommées pour un besoin en ressources générique.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130304"
---
# <a name="generic-resource-requirement-fulfillment"></a>Répondre aux besoins en ressources génériques

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez réserver une ressource nommée pour remplacer une ressource génériques qui a un besoin en ressources.

1. Sur la page **Projets**, sélectionnez l’onglet **Équipe**.
2. Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Réserver**. Ou, ouvrez le besoin en ressources puis cliquez sur **Réserver**.
3. Dans la page **Assistant Planifier**, sélectionnez une ressource nommée à réserver sur votre équipe du projet, puis cliquez sur **Réserver**.

Une fois la réservation effectuée et satisfaite par une ressource nommée, la ressource générique est remplacée par la ressource nommée.

Les attributions sur la planification sont également mises à jour avec la ressource nommée.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Exécuter une ressource générique avec plusieurs ressources nommées
La satisfaction d’un besoin en ressource générique avec plusieurs ressources nommées est similaire à l’attribution d’une ressource nommée unique. Par exemple, il existe une tâche avec une durée de cinq jours et de 120 heures d’effort. Cette tâche ne peut pas être effectuée que par une ressource qui fonctionne un jour de huit heures classique sur une semaine de cinq jours. 

Le besoin est de 120 heures d’ingénierie robotique sur de cinq jours, soit 24 heures par jour.

Il s’agit d’un exemple où plusieurs ressources nommées sont nécessaires pour répondre à une demande de ressource générique. Vous devez réserver plusieurs ressources pour satisfaire le besoin.

La principale différence dans ce scénario est que la ressource générique reste dans l’équipe attribuée à la tâche, et les membres de l’équipe de ressources nommés réservés ne sont pas attribués dans le cadre du poste. Le chef de projet peut affecter le travail si besoin aux ressources nommées. La vue **Rapprochement** peut aider un chef de projet à répartir les réservations entre plusieurs ressources à des affectations de tâche. Cela n’est pas effectué automatiquement, car dans les scénarios plus compliqués que l’exemple simple ci-dessus, comme celui où un groupe de tâches composent le besoin, la façon dont le chef de projet souhaite les affecter, doit être prise en compte par le système. Comme le système ne peut pas comprendre l’intention, les hypothèses seront sans doute différentes de celles prévues et un résultat incorrect ou imprévisible se produira. Le résultat prévisible est que la ressource générique reste affectée jusqu’à ce que le chef de projet crée délibérément des attributions à l’aide de la vue **Rapprochement**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]