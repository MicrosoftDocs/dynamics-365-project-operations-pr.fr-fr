---
title: Attribuer une ressource à une tâche
description: Cette rubrique fournit des informations sur la façon d’attribuer des ressources aux tâches.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149990"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="6d44c-103">Attribuer une ressource à une tâche</span><span class="sxs-lookup"><span data-stu-id="6d44c-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6d44c-104">Il existe trois méthodes pour attribuer une ressource à une tâche dans Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6d44c-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="6d44c-105">Réserver une ressource en tant que membre d’équipe, et l’attribuer à une tâche</span><span class="sxs-lookup"><span data-stu-id="6d44c-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="6d44c-106">Vous pouvez ajouter une ressource à l’équipe du projet, puis attribuez la ressource à des tâches dans la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="6d44c-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="6d44c-107">Dans l’onglet **Membre de l’équipe**, ajoutez un nouveau membre de l’équipe en sélectionnant **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6d44c-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="6d44c-108">Le volet **Création rapide de membre d’équipe** s’ouvre, où sélectionnez le nom de la ressource réservable et définissez un rôle.</span><span class="sxs-lookup"><span data-stu-id="6d44c-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="6d44c-109">Sélectionnez un des modes d’attribution suivants pour la réservation de la ressource :</span><span class="sxs-lookup"><span data-stu-id="6d44c-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="6d44c-110">**Capacité maximale** réserve la capacité totale de la ressource pour les dates de début et de fin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="6d44c-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6d44c-111">**Capacité du pourcentage** réserva la ressource pour un pourcentage de la capacité de la ressource aux dates de début et de fin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="6d44c-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="6d44c-112">**Par heure - Distribuer de manière homogène** réserve la ressource pour un nombre spécifique d’heures, la distribuant de manière homogène par jour pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d44c-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="6d44c-113">**Par heure - Chargement frontal** réserve la ressource pour un nombre spécifique d’heures, chargeant frontalement les heures par jour pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d44c-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="6d44c-114">**Aucune** ajoute la ressource à l’équipe mais ne crée aucune réservation qui absorbe la capacité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6d44c-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="6d44c-115">Dans la grille **Planification** d’une tâche, sélectionnez l’icône **Ressource** dans la cellule de la ressource, puis sous **Membres de l’équipe**, sélectionnez le membre de l’équipe que vous venez d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="6d44c-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="6d44c-116">Sous l’onglet **Membre de l’équipe** et l’onglet **Rapprochement**, la ressource affiche des heures réservées et attribuées.</span><span class="sxs-lookup"><span data-stu-id="6d44c-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="6d44c-117">Les heures doivent être identiques, mais ce n’est pas obligatoire, car les réservations et les attributions ne sont pas couplées étroitement.</span><span class="sxs-lookup"><span data-stu-id="6d44c-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="6d44c-118">L’onglet **Rapprochement** donne des détails lorsqu’elles sont différentes, comme lorsque vous attribuez à une ressource plus d’heures que vous en avez réservées.</span><span class="sxs-lookup"><span data-stu-id="6d44c-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="6d44c-119">Au besoin, vous pouvez corriger les informations en étendant les réservations de la ressource ou en modifiant l’attribution.</span><span class="sxs-lookup"><span data-stu-id="6d44c-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="6d44c-120">Créer un membre de l’équipe générique via l’attribution de tâche</span><span class="sxs-lookup"><span data-stu-id="6d44c-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="6d44c-121">Lorsque vous créez un membre de l’équipe générique via l’attribution de tâche, vous créez un espace réservé ou une ressource générique qui décrit les caractéristiques de la ressource nommée que vous souhaitez travailler sur des tâches.</span><span class="sxs-lookup"><span data-stu-id="6d44c-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="6d44c-122">Ensuite, vous générer un besoin (ou vous envoyez une demande à l’aide du besoin) utilisé pour rechercher et réserver la ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="6d44c-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="6d44c-123">Dans la grille **Planification** d’une tâche, sélectionnez l’icône **Ressource** dans la cellule de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6d44c-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6d44c-124">Tapez un nom qui servira de nom pour la ressource d’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="6d44c-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="6d44c-125">Par exemple, Responsable du programme.</span><span class="sxs-lookup"><span data-stu-id="6d44c-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="6d44c-126">Sélectionnez **Créer** et dans le champ **Création rapide de membre d’équipe du projet**, définissez le rôle de la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="6d44c-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="6d44c-127">Vous pouvez continuer d’attribuer des tâches à cette ressource d’espace réservé en sélectionnant la ressource dans le **Sélecteur de ressource** de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6d44c-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="6d44c-128">Elles sont répertoriées sous **Membres de l’équipe**.</span><span class="sxs-lookup"><span data-stu-id="6d44c-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="6d44c-129">Lorsque vous avez terminé d’attribuer la ressource générique, sélectionnez la ressource générique sur l’onglet **Équipe**, puis sélectionnez **Générer un besoin** pour créer un besoin en ressources pour la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="6d44c-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="6d44c-130">Sélectionnez **Réserver** pour la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="6d44c-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="6d44c-131">Vous pouvez ensuite les utiliser le tableau Planification pour rechercher et réserver une ressource réelle.</span><span class="sxs-lookup"><span data-stu-id="6d44c-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="6d44c-132">Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources.</span><span class="sxs-lookup"><span data-stu-id="6d44c-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="6d44c-133">Lorsque la ressource générique est exécutée avec une ressource nommée, la ressource générique est supprimée de l’équipe et les attributions de tâches pour la ressource générique sont attribuées à la ressource nommée qui a renseigné le besoin en ressources de la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="6d44c-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="6d44c-134">Attribuer une ressource nommée dans la liste de toutes les ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="6d44c-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="6d44c-135">Vous pouvez utiliser la zone de recherche dans le **Sélecteur de ressource** afin de rechercher toutes les ressources pouvant être réservées et les attribuer à une tâche.</span><span class="sxs-lookup"><span data-stu-id="6d44c-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="6d44c-136">Les ressources attribuées ainsi sont ajoutées à l’équipe sans aucune réservation.</span><span class="sxs-lookup"><span data-stu-id="6d44c-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="6d44c-137">C’est similaire à ajouter un membre de l’équipe et à sélectionner Aucune comme mode de répartition.</span><span class="sxs-lookup"><span data-stu-id="6d44c-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="6d44c-138">La ressource est affichée dans l’onglet **Équipe** et l’onglet **Rapprochement** en tant que ressources avec uniquement des attributions et un déficit de réservation.</span><span class="sxs-lookup"><span data-stu-id="6d44c-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="6d44c-139">Réservez-les si vous souhaitez utiliser leur disponibilité.</span><span class="sxs-lookup"><span data-stu-id="6d44c-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="6d44c-140">Dans la grille **Planification** d’une tâche, sélectionnez l’icône **Ressource** dans la cellule de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6d44c-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="6d44c-141">Commencez à entrer un nom.</span><span class="sxs-lookup"><span data-stu-id="6d44c-141">Start typing a name.</span></span> <span data-ttu-id="6d44c-142">Les résultats de la recherche sur le nom s’affichent dans le **Sélecteur de ressource** sous **Autres ressources**.</span><span class="sxs-lookup"><span data-stu-id="6d44c-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="6d44c-143">Sélectionnez la ressource que vous souhaitez attribuer à la tâche.</span><span class="sxs-lookup"><span data-stu-id="6d44c-143">Select the resource that you want to assign to the task.</span></span>

