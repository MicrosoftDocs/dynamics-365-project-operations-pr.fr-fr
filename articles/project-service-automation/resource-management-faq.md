---
title: FAQ sur la gestion des ressources.
description: Cette rubrique apporte des réponses aux questions les plus fréquemment posées sur la gestion des ressources.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168104"
---
# <a name="resource-management-faq"></a>FAQ sur la gestion des ressources.

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Quelle est la différence entre un membre de l'équipe et un besoin en ressources ?

Un membre de l'équipe du projet peut être attribué aux tâches, réservé ou surréservé, et défini comme approbateur. Un besoin en ressources peut exister sans membre de l'équipe du projet, comme brouillon de note de la demande. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Quelle est la différence entre les heures proposées et les heures réservées provisoirement ?

Les heures proposées et les heures réservées provisoirement peuvent différer dans la visibilité. Les heures proposées sont accessibles qu'aux gestionnaires de ressources et au chef de projet ayant initialisé la demande à l'aide d'une demande de ressource. Les heures réservées provisoirement sont visibles de toute personne qui a accès au Tableau de planification.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Comment afficher les heures réservées provisoirement pour les ressources d'une équipe ?

Les réservations provisoires peuvent être effectuées lorsque vous réservez un besoin en ressources. Les ressources réservées provisoirement sur une équipe du projet apparaissent comme membres de l'équipe avec des heures réservées provisoirement. Elles s'affichent également sur le Tableau de planification.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Comment modifier les heures requises, et les dates de début et de fin, pour une ressource (générique ou nommée) que j'ai réservée ?

Une fois les ressources réservées, sélectionnez **Gérer les réservations** et apportez les modifications nécessaires.

## <a name="what-resources-types-does-project-service-automation-support"></a>Quels types de ressources Project Service Automation prend en charge ?

**Utilisateur** et **Contact** sont les seuls types de ressources pris en charge dans Dynamics 365 Project Service Automation. Bien que vous puissiez créer d'autres types de ressources (par exemple, **Équipement** et **Groupe**), aucun cas d'utilisation de bout en bout n'est pris en charge pour ceux-ci.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Quelle est la différence entre une attribution et une réservation ?

Les attributions sont l'attribution de ressources aux tâches d'un projet dans la planification du projet. Les ressources peuvent être des ressources réelles ou des ressources génériques. Les réservations sont l'allocation ferme ou provisoire des ressources sur un projet. Les réservations fermes consomment la capacité d'une ressource. Idéalement, pour les ressources réelles, les réservations et les affectations doivent correspondre, car elles ne peuvent pas différer. Toutefois, PSA n'applique pas cette mise en correspondance. La vue Rapprochement affiche à un chef de projet des emplacements où les réservations et les affectations d'une ressource ne correspondent pas.