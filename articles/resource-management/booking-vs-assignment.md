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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075589"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="ab6b1-103">Réservations et Affectations</span><span class="sxs-lookup"><span data-stu-id="ab6b1-103">Bookings vs assignments</span></span>

<span data-ttu-id="ab6b1-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="ab6b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab6b1-105">Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ab6b1-106">Les réservations fermes consomment la capacité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="ab6b1-107">Les attributions sont l’attribution de ressources aux tâches d’un projet dans la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ab6b1-108">Les ressources peuvent être réelles ou génériques.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="ab6b1-109">Idéalement, pour les ressources réelles, les réservations et les affectations doivent correspondre, car elles ne peuvent pas différer.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="ab6b1-110">Toutefois, Microsoft Dynamics Project Operations n’applique pas cette mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="ab6b1-111">La vue **Rapprochement** affiche à un chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="ab6b1-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
