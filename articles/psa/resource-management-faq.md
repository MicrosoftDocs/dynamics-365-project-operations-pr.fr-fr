---
title: FAQ sur la gestion des ressources.
description: Cette rubrique apporte des réponses aux questions les plus fréquemment posées sur la gestion des ressources.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 20562b98ccc8451ab57dd42fb8c2f9f303811dbe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283140"
---
# <a name="resource-management-faq"></a><span data-ttu-id="94483-103">FAQ sur la gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="94483-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="94483-104">Quelle est la différence entre un membre de l’équipe et un besoin en ressources ?</span><span class="sxs-lookup"><span data-stu-id="94483-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="94483-105">Un membre de l’équipe du projet peut être attribué aux tâches, réservé ou surréservé, et défini comme approbateur.</span><span class="sxs-lookup"><span data-stu-id="94483-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="94483-106">Un besoin en ressources peut exister sans membre de l’équipe du projet, comme brouillon de note de la demande.</span><span class="sxs-lookup"><span data-stu-id="94483-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="94483-107">Quelle est la différence entre les heures proposées et les heures réservées provisoirement ?</span><span class="sxs-lookup"><span data-stu-id="94483-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="94483-108">Les heures proposées et les heures réservées provisoirement peuvent différer dans la visibilité.</span><span class="sxs-lookup"><span data-stu-id="94483-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="94483-109">Les heures proposées sont accessibles qu’aux gestionnaires de ressources et au chef de projet ayant initialisé la demande à l’aide d’une demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="94483-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="94483-110">Les heures réservées provisoirement sont visibles de toute personne qui a accès au Tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="94483-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="94483-111">Comment afficher les heures réservées provisoirement pour les ressources d’une équipe ?</span><span class="sxs-lookup"><span data-stu-id="94483-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="94483-112">Les réservations provisoires peuvent être effectuées lorsque vous réservez un besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="94483-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="94483-113">Les ressources réservées provisoirement sur une équipe du projet apparaissent comme membres de l’équipe avec des heures réservées provisoirement.</span><span class="sxs-lookup"><span data-stu-id="94483-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="94483-114">Elles s’affichent également sur le Tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="94483-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="94483-115">Comment modifier les heures requises, et les dates de début et de fin, pour une ressource (générique ou nommée) que j’ai réservée ?</span><span class="sxs-lookup"><span data-stu-id="94483-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="94483-116">Une fois les ressources réservées, sélectionnez **Gérer les réservations** et apportez les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="94483-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="94483-117">Quels types de ressources Project Service Automation prend en charge ?</span><span class="sxs-lookup"><span data-stu-id="94483-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="94483-118">**Utilisateur** et **Contact** sont les seuls types de ressources pris en charge dans Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="94483-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="94483-119">Bien que vous puissiez créer d’autres types de ressources (par exemple, **Équipement** et **Groupe**), aucun cas d’utilisation de bout en bout n’est pris en charge pour ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="94483-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="94483-120">Quelle est la différence entre une attribution et une réservation ?</span><span class="sxs-lookup"><span data-stu-id="94483-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="94483-121">Les attributions sont l’attribution de ressources aux tâches d’un projet dans la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="94483-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="94483-122">Les ressources peuvent être des ressources réelles ou des ressources génériques.</span><span class="sxs-lookup"><span data-stu-id="94483-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="94483-123">Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet.</span><span class="sxs-lookup"><span data-stu-id="94483-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="94483-124">Les réservations fermes consomment la capacité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="94483-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="94483-125">Idéalement, pour les ressources réelles, les réservations et les affectations doivent correspondre, car elles ne peuvent pas différer.</span><span class="sxs-lookup"><span data-stu-id="94483-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="94483-126">Toutefois, PSA n’applique pas cette mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="94483-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="94483-127">La vue Rapprochement affiche à un chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="94483-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]