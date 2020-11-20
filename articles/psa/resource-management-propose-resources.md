---
title: Proposer des ressources de projet
description: Cette rubrique explique comment proposer des ressources de projet.
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120180"
---
# <a name="propose-project-resources"></a><span data-ttu-id="a8582-103">Proposer des ressources de projet</span><span class="sxs-lookup"><span data-stu-id="a8582-103">Propose project resources</span></span>

<span data-ttu-id="a8582-104">Les gestionnaires de ressources peuvent proposer une ressource au chef de projet en utilisant une demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="a8582-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a8582-105">Dans la grille de demande ou la demande elle-même, sélectionnez **Rechercher des ressources**.</span><span class="sxs-lookup"><span data-stu-id="a8582-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a8582-106">Dans la page **Assistant Planifier**, sélectionnez la ressource, puis, dans le volet **Créer une réservation de ressource**, dans le champ **Statut de la réservation**, sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="a8582-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Ressource sélectionnée proposée](media/Resource-Management-image62.png)

<span data-ttu-id="a8582-108">Les mises à jour de statut suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="a8582-108">The following status updates occur:</span></span>

- <span data-ttu-id="a8582-109">Dans la page **Assistant Planifier**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, mais pas réservée de manière ferme.</span><span class="sxs-lookup"><span data-stu-id="a8582-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicateurs de statut des réservations proposées sur la page Assistant Planifier](media/Resource-Management-image63.png)

- <span data-ttu-id="a8582-111">Dans la demande de ressource, le statut passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="a8582-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Statut de la demande de ressource passé à Révision nécessaire](media/Resource-Management-image64.png)

- <span data-ttu-id="a8582-113">Dans l’onglet **Équipe** du projet, la valeur **Statut de demande** du membre de l’équipe générique passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="a8582-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Statut de demande du membre de l’équipe générique passé à Révision nécessaire sous l’onglet Équipe](media/Resource-Management-image48.png)

<span data-ttu-id="a8582-115">Le chef du projet peut accepter ou rejeter la proposition.</span><span class="sxs-lookup"><span data-stu-id="a8582-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a8582-116">Lorsque les gestionnaires de ressources gèrent les demandes de ressources, ils utilisent les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8582-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a8582-117">Proposer plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour satisfaire les heures obligatoires.</span><span class="sxs-lookup"><span data-stu-id="a8582-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a8582-118">Les heures proposées sont alors fractionnées entre plusieurs ressources qui peuvent satisfaire les heures obligatoires.</span><span class="sxs-lookup"><span data-stu-id="a8582-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a8582-119">Dans ce scénario, les heures ne peuvent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="a8582-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a8582-120">Proposer moins de ressources que requis.</span><span class="sxs-lookup"><span data-stu-id="a8582-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="a8582-121">Dans ce scénario, la capacité en ressources est inférieure aux heures requises que le demandeur a spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a8582-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a8582-122">Par conséquent, lorsque le demandeur accepte les ressources proposées, un besoin en ressources non atteint est créé pour capturer la demande restante.</span><span class="sxs-lookup"><span data-stu-id="a8582-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a8582-123">Réserver plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour terminer le travail.</span><span class="sxs-lookup"><span data-stu-id="a8582-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a8582-124">Réserver moins de ressources que requis.</span><span class="sxs-lookup"><span data-stu-id="a8582-124">Book fewer resources than are required.</span></span> <span data-ttu-id="a8582-125">Dans ce scénario, les heures réservées sont inférieures aux heures requises.</span><span class="sxs-lookup"><span data-stu-id="a8582-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a8582-126">Le système vous guide pour proposer des ressources à la place de réservations, de sorte que le demandeur puisse vérifier et suivre la demande restante.</span><span class="sxs-lookup"><span data-stu-id="a8582-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="a8582-127">Utilisation facturable</span><span class="sxs-lookup"><span data-stu-id="a8582-127">Billable utilization</span></span>

<span data-ttu-id="a8582-128">Les ressources peuvent avoir une utilisation facturable cible.</span><span class="sxs-lookup"><span data-stu-id="a8582-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a8582-129">Cette utilisation cible est définie comme un attribut dans le rôle par défaut d’une ressource ou sur l’enregistrement de la ressource réservable individuelle.</span><span class="sxs-lookup"><span data-stu-id="a8582-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a8582-130">Les calculs de l’utilisation sont basés sur les heures réelles que les ressources ont signalées à l’aide des entrées de temps approuvées.</span><span class="sxs-lookup"><span data-stu-id="a8582-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a8582-131">Les formules suivantes sont utilisées pour calculer l’utilisation :</span><span class="sxs-lookup"><span data-stu-id="a8582-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="a8582-132">Utilisation facturable = Heures réelles facturables ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="a8582-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="a8582-133">Utilisation non facturable = Temps réel avec ID type facturation = Capacité non facturable, gratuite ou non disponible ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="a8582-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="a8582-134">Interne = Temps réel sans contrat de vente ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="a8582-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="a8582-135">Capacité ressource = Heures de travail d’une ressource – Absence du bureau – Jours non ouvrables</span><span class="sxs-lookup"><span data-stu-id="a8582-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a8582-136">Vous trouverez la vue **Utilisation des ressources** dans le volet **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="a8582-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vue Utilisation des ressources](media/Resource-Management-image65.png)

<span data-ttu-id="a8582-138">Chaque cellule dans la grille représente le pourcentage total d’utilisation de la ressource à une période, par exemple un jour, une semaine ou un mois.</span><span class="sxs-lookup"><span data-stu-id="a8582-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a8582-139">Les formules suivantes sont utilisées pour colorer les cellules :</span><span class="sxs-lookup"><span data-stu-id="a8582-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="a8582-140">**Vert :** Utilisation facturable \>= Utilisation cible de la ressource</span><span class="sxs-lookup"><span data-stu-id="a8582-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="a8582-141">**Jaune :** Utilisation cible – 20 \<= Utilisation facturable \< Utilisation cible.</span><span class="sxs-lookup"><span data-stu-id="a8582-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="a8582-142">**Rouge :** Utilisation facturable \< Utilisation cible - 20</span><span class="sxs-lookup"><span data-stu-id="a8582-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="a8582-143">Comme la vue **Utilisation des ressources** est basée sur le Tableau de planification, vous pouvez utiliser les fonctionnalités de filtrage du Tableau de planification pour filtrer vos résultats.</span><span class="sxs-lookup"><span data-stu-id="a8582-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a8582-144">La grille nécessite que vous définissiez une utilisation cible du rôle ou de la ressource individuelle.</span><span class="sxs-lookup"><span data-stu-id="a8582-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a8582-145">Pour effectuer cette configuration, accédez à **Ressources** \> **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="a8582-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="a8582-146">En outre, un rôle par défaut doit être affecté à chaque ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="a8582-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a8582-147">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="a8582-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="a8582-148">Dans l’onglet **Project Service**, vérifiez qu’un rôle de ressource est défini, et que le champ **Est la valeur par défaut** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="a8582-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="a8582-149">Vous pouvez ajouter des rôles supplémentaires où **Est la valeur par défaut = Non**.</span><span class="sxs-lookup"><span data-stu-id="a8582-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="a8582-150">Le rôle où **Est la valeur par défaut = Oui** est utilisé pour évaluer l’utilisation de la ressource par rapport à la cible de ce rôle.</span><span class="sxs-lookup"><span data-stu-id="a8582-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Rôle par défaut défini](media/Resource-Management-image67.png)

<span data-ttu-id="a8582-152">Dans l’onglet **Project Service**, vous pouvez également définir une utilisation cible individuelle pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="a8582-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a8582-153">Le calcul de l’utilisation utilise ensuite cette utilisation cible pour évaluer la cible de la ressource au lieu de la cible du rôle par défaut de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a8582-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a8582-154">L’utilisation s’affiche pour une ressource uniquement si cette ressource est approuvée, temps facturable pendant la période affichée dans la grille.</span><span class="sxs-lookup"><span data-stu-id="a8582-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a8582-155">La disponibilité des ressources</span><span class="sxs-lookup"><span data-stu-id="a8582-155">Resource availability</span></span>

<span data-ttu-id="a8582-156">Il est donc impératif que les gestionnaires de ressources puissent afficher la disponibilité des ressources et mettre à jour les réservations.</span><span class="sxs-lookup"><span data-stu-id="a8582-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a8582-157">Dans certains cas, il n’existe aucune demande formelle (demande de ressource), mais un gestionnaire des ressources doit répondre à la demande non planifiée fournie par les canaux, par exemple le courrier électronique, l’appel téléphonique, ou un message instantané.</span><span class="sxs-lookup"><span data-stu-id="a8582-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a8582-158">Les gestionnaires de ressources utilisent le Tableau de planification pour mettre à jour les ressources et les réservations.</span><span class="sxs-lookup"><span data-stu-id="a8582-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a8582-159">Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="a8582-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a8582-160">Les réservations de ressource consomment la capacité des ressources.</span><span class="sxs-lookup"><span data-stu-id="a8582-160">Resource bookings consume the capacity of the resources.</span></span>

![Tableau de planification](media/Resource-Management-image68.png)

<span data-ttu-id="a8582-162">Le Tableau de planification utilise des couleurs et de l’ombrage pour afficher les réservations,la disponibilité et les surréservations, ainsi que le statut des réservations.</span><span class="sxs-lookup"><span data-stu-id="a8582-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a8582-163">Un paramètre des paramètres du Tableau de planification vous permet d’afficher une légende.</span><span class="sxs-lookup"><span data-stu-id="a8582-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a8582-164">Si une flèche pointant vers la droite apparaît en regard d’une ressource réservable individuelle sur le Tableau de planification, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.</span><span class="sxs-lookup"><span data-stu-id="a8582-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Ressource réservable développée sur le Tableau de planification](media/Resource-Management-image69.png)

<span data-ttu-id="a8582-166">Comme Dynamics 365 Project Service Automation utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.</span><span class="sxs-lookup"><span data-stu-id="a8582-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Détails des réservations de ressource pour les projets et les ordres de travail](media/Resource-Management-image70.png)

<span data-ttu-id="a8582-168">Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte de ressource.</span><span class="sxs-lookup"><span data-stu-id="a8582-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Carte de ressource](media/Resource-Management-image71.png)
