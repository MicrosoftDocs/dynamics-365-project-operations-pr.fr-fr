---
title: Vérifier les ressources proposées
description: Cette rubrique explique comment proposer des ressources de projet.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279270"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="f9b25-103">Vérifier les ressources proposées</span><span class="sxs-lookup"><span data-stu-id="f9b25-103">Review proposed resources</span></span>

<span data-ttu-id="f9b25-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f9b25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9b25-105">Les gestionnaires de ressources peuvent proposer une ressource au chef de projet en utilisant une demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="f9b25-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="f9b25-106">Dans la grille de demande ou la demande elle-même, sélectionnez **Rechercher des ressources**.</span><span class="sxs-lookup"><span data-stu-id="f9b25-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="f9b25-107">Dans la page **Assistant Planifier**, sélectionnez la ressource, puis, dans le volet **Créer une réservation de ressource**, dans le champ **Statut de la réservation**, sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="f9b25-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="f9b25-108">Les mises à jour de statut suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="f9b25-108">The following status updates occur:</span></span>

- <span data-ttu-id="f9b25-109">Dans la page **Assistant Planifier**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, mais pas réservée de manière ferme.</span><span class="sxs-lookup"><span data-stu-id="f9b25-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="f9b25-110">Dans la demande de ressource, le statut passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="f9b25-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="f9b25-111">Dans l’onglet **Équipe** du projet, la valeur **Statut de demande** du membre de l’équipe générique passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="f9b25-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="f9b25-112">Le chef du projet peut accepter ou rejeter la proposition.</span><span class="sxs-lookup"><span data-stu-id="f9b25-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="f9b25-113">Lorsque les gestionnaires de ressources gèrent les demandes de ressources, ils utilisent les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9b25-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="f9b25-114">Proposer plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour accomplir les heures requises.</span><span class="sxs-lookup"><span data-stu-id="f9b25-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="f9b25-115">Les heures proposées sont alors fractionnées entre plusieurs ressources qui peuvent satisfaire les heures obligatoires.</span><span class="sxs-lookup"><span data-stu-id="f9b25-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="f9b25-116">Dans ce scénario, les heures ne peuvent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="f9b25-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="f9b25-117">Proposer moins de ressources que requis.</span><span class="sxs-lookup"><span data-stu-id="f9b25-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="f9b25-118">Dans ce scénario, la capacité en ressources est inférieure aux heures requises que le demandeur a spécifiées.</span><span class="sxs-lookup"><span data-stu-id="f9b25-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="f9b25-119">Par conséquent, lorsque le demandeur accepte les ressources proposées, un besoin en ressources non satisfait est créé pour capturer la demande restante.</span><span class="sxs-lookup"><span data-stu-id="f9b25-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="f9b25-120">Réserver plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour effectuer les tâches.</span><span class="sxs-lookup"><span data-stu-id="f9b25-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="f9b25-121">Réserver moins de ressources que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f9b25-121">Book fewer resources than are required.</span></span> <span data-ttu-id="f9b25-122">Dans ce scénario, les heures réservées sont inférieures aux heures requises.</span><span class="sxs-lookup"><span data-stu-id="f9b25-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="f9b25-123">Le système vous guide pour proposer des ressources à la place de réservations, de sorte que le demandeur puisse vérifier et suivre la demande restante.</span><span class="sxs-lookup"><span data-stu-id="f9b25-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="f9b25-124">La disponibilité des ressources</span><span class="sxs-lookup"><span data-stu-id="f9b25-124">Resource availability</span></span>

<span data-ttu-id="f9b25-125">Il est donc impératif que les gestionnaires de ressources puissent afficher la disponibilité des ressources et mettre à jour les réservations.</span><span class="sxs-lookup"><span data-stu-id="f9b25-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="f9b25-126">Dans certains cas, il n’existe aucune demande formelle (demande de ressource), mais un gestionnaire des ressources doit répondre à la demande non planifiée fournie par les canaux, par exemple le courrier électronique, l’appel téléphonique, ou un message instantané.</span><span class="sxs-lookup"><span data-stu-id="f9b25-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="f9b25-127">Les gestionnaires de ressources utilisent le Tableau de planification pour mettre à jour les ressources et les réservations.</span><span class="sxs-lookup"><span data-stu-id="f9b25-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="f9b25-128">Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="f9b25-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="f9b25-129">Les réservations de ressource consomment la capacité des ressources.</span><span class="sxs-lookup"><span data-stu-id="f9b25-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="f9b25-130">Le Tableau de planification utilise des couleurs et de l’ombrage pour afficher les réservations, la disponibilité et les surréservations, ainsi que le statut des réservations.</span><span class="sxs-lookup"><span data-stu-id="f9b25-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="f9b25-131">Un paramètre des paramètres du Tableau de planification vous permet d’afficher une légende.</span><span class="sxs-lookup"><span data-stu-id="f9b25-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="f9b25-132">Si une flèche pointant vers la droite apparaît en regard d’une ressource réservable individuelle sur le Tableau de planification, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.</span><span class="sxs-lookup"><span data-stu-id="f9b25-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="f9b25-133">Comme Dynamics 365 Project Operations utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.</span><span class="sxs-lookup"><span data-stu-id="f9b25-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="f9b25-134">Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte de ressource.</span><span class="sxs-lookup"><span data-stu-id="f9b25-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]