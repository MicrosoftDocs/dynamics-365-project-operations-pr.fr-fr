---
title: Comment attribuer une ressource pouvant être réservée à une tâche dans l’application web
description: Vue d’ensemble des méthodes d’attribution des ressources pouvant être réservées.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286290"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="31e04-103">Comment attribuer une ressource réservable à une tâche dans l’application web (application Project Service v2.x) ?</span><span class="sxs-lookup"><span data-stu-id="31e04-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="31e04-104">Il existe deux méthodes pour attribuer une ressource à une tâche dans Project Service.</span><span class="sxs-lookup"><span data-stu-id="31e04-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="31e04-105">Vous pouvez réserver une ressource en tant que membre d’équipe et l’attribuer à une tâche.</span><span class="sxs-lookup"><span data-stu-id="31e04-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="31e04-106">Ou, vous pouvez créer un membre d’équipe générique via l’attribution de rôle sur les tâches, générer une équipe, puis satisfaire les conditions de sauvegarde avec une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="31e04-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="31e04-107">Notez que si vous souhaitez attribuer une ressource réservable à une tâche, le membre de l’équipe de la ressource réservable doit disposer de suffisamment de réservations disponibles.</span><span class="sxs-lookup"><span data-stu-id="31e04-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="31e04-108">Le statut de la réservation doit être de type de validation Réservation ferme et Statut validé.</span><span class="sxs-lookup"><span data-stu-id="31e04-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="31e04-109">S’il n’y a pas suffisamment de réservations pour la ressource, Project Service supprime l’attribution et affiche le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="31e04-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="31e04-110">*Impossible d’attribuer la ressource à la tâche - les ressources suivantes ne disposent pas de suffisamment d’heures réservées par rapport au projet*</span><span class="sxs-lookup"><span data-stu-id="31e04-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="31e04-111">Réserver une ressource en tant que membre d’équipe et l’attribuer à une tâche</span><span class="sxs-lookup"><span data-stu-id="31e04-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="31e04-112">Avec cette méthode vous ajoutez une ressource à l’équipe du projet puis attribuez des tâches à la ressource dans la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="31e04-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="31e04-113">Voici la méthode pour le faire :</span><span class="sxs-lookup"><span data-stu-id="31e04-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="31e04-114">Dans la grille de membre de l’équipe, ajoutez un nouveau membre de l’équipe en sélectionnant **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="31e04-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="31e04-115">Dans l’écran Création rapide de membre d’équipe, sélectionnez le nom de la ressource réservable et définissez un rôle.</span><span class="sxs-lookup"><span data-stu-id="31e04-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="31e04-116">Sélectionnez les dates **De** et **À**.</span><span class="sxs-lookup"><span data-stu-id="31e04-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="31e04-117">![Capture d’écran de l’ajout d’un membre de l’équipe](media/FAQ-Resources-to-Tasks2-1.png "Capture d’écran de l’ajout d’un membre de l’équipe")</span><span class="sxs-lookup"><span data-stu-id="31e04-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="31e04-118">Sélectionnez une des méthodes d’attribution suivantes pour réserver la ressource :</span><span class="sxs-lookup"><span data-stu-id="31e04-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="31e04-119">**Capacité maximale** réserve la capacité totale de la ressource pour les dates de début et de fin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="31e04-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="31e04-120">**Capacité du pourcentage** réserva la ressource pour un pourcentage de la capacité de la ressource aux dates de début et de fin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="31e04-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="31e04-121">**Par heure - Distribuer de manière homogène** réserve la ressource pour un nombre spécifique d’heures, la distribuant de manière homogène par jour pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="31e04-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="31e04-122">**Par heure - Chargement frontal** réserve la ressource pour un nombre spécifique d’heures, chargeant frontalement les heures par jour pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="31e04-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="31e04-123">Ne sélectionnez pas **Aucun** car cela ajoute la ressource à l’équipe mais ne crée aucune réservation qui absorbe la capacité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="31e04-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="31e04-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="31e04-124">Select **Save**.</span></span>

    <span data-ttu-id="31e04-125">Notez que les heures de la réservation doivent être suffisantes pour correspondre aux plages d’heures et de dates de travail auxquelles vous attribuez cette ressource.</span><span class="sxs-lookup"><span data-stu-id="31e04-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="31e04-126">Si elles ne sont pas alignées, vous ne pouvez pas attribuer la ressource à la tâche.</span><span class="sxs-lookup"><span data-stu-id="31e04-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="31e04-127">Dans la structure de répartition du travail (WBS) de la tâche, cliquez sur la liste déroulante des cellules de la ressource.</span><span class="sxs-lookup"><span data-stu-id="31e04-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="31e04-128">Puis :</span><span class="sxs-lookup"><span data-stu-id="31e04-128">Then:</span></span> 

    1. <span data-ttu-id="31e04-129">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="31e04-129">Select **Add**.</span></span>
    2. <span data-ttu-id="31e04-130">Sélectionnez le liste déroulante sous **Ressources** et sélectionnez le membre de l’équipe ajouté ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="31e04-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="31e04-131">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="31e04-131">Select **OK**.</span></span> <span data-ttu-id="31e04-132">Le membre de l’équipe est maintenant attribué à la tâche.</span><span class="sxs-lookup"><span data-stu-id="31e04-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="31e04-133">![Capture d’écran de l’ajout de ressources avec WBS](media/FAQ-Resources-to-Tasks2-2.png "Capture d’écran de l’ajout de ressources avec WBS")</span><span class="sxs-lookup"><span data-stu-id="31e04-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="31e04-134">Dans la grille du membre de l’équipe, vous verrez l’agrégat des heures attribuées de la ressource sous Heures attribuées.</span><span class="sxs-lookup"><span data-stu-id="31e04-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="31e04-135">Il est inférieur ou égal aux heures réservées pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="31e04-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="31e04-136">![Capture d’écran des heures attribuées pour une ressource](media/FAQ-Resources-to-Tasks2-3.png "Capture d’écran des heures attribuées pour une ressource")</span><span class="sxs-lookup"><span data-stu-id="31e04-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="31e04-137">Si la tâche que vous tentez d’attribuer à la ressource commence après la date de fin des réservations de ressources, la ressource n’apparaîtra pas dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="31e04-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="31e04-138">Notez que vous pouvez attribuer une ressource à plus d’heures que ses heures réservées si la ressource dispose d’une capacité non attribuée restante.</span><span class="sxs-lookup"><span data-stu-id="31e04-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="31e04-139">Dans ce cas la ressource sera uniquement partiellement attribuée jusqu’à leurs réservations.</span><span class="sxs-lookup"><span data-stu-id="31e04-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="31e04-140">Vous pouvez voir ces heures de tâche non attribuées restantes en ajoutant la colonne Heures non dotées à la structure de distribution de travail.</span><span class="sxs-lookup"><span data-stu-id="31e04-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="31e04-141">Si les ressources sont attribuées à leurs heures réservées (leurs heures réservées sont égales à leurs heures attribuées), le message d’erreur suivant s’affichera lorsque vous essayez de leur attribuer d’autres tâches :</span><span class="sxs-lookup"><span data-stu-id="31e04-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="31e04-142">*Impossible d’attribuer la ressource à la tâche - les ressources suivantes ne disposent pas de suffisamment d’heures réservées par rapport au projet.*</span><span class="sxs-lookup"><span data-stu-id="31e04-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="31e04-143">En outre, le membre de l’équipe du responsable de projet par défaut ajouté à l’équipe lors de la création du projet est ajouté sans aucune réservation et ne peut être attribué à aucune tâche.</span><span class="sxs-lookup"><span data-stu-id="31e04-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="31e04-144">Il n’apparaît pas dans la liste déroulante de la ressource pour les tâches.</span><span class="sxs-lookup"><span data-stu-id="31e04-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="31e04-145">Si vous voulez attribuer cette ressource, vous devez le supprimer de l’équipe puis l’ajouter à nouveau avec une méthode d’attribution autre que Aucune.</span><span class="sxs-lookup"><span data-stu-id="31e04-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="31e04-146">La raison pour laquelle il est ajouté à l’équipe lorsque le projet est créé est parce qu’un projet contient au moins un approbateur de projet par défaut.</span><span class="sxs-lookup"><span data-stu-id="31e04-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="31e04-147">Créer un membre de l’équipe générique via l’attribution de rôle sur les tâches</span><span class="sxs-lookup"><span data-stu-id="31e04-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="31e04-148">Cette méthode vous assurer que les ressources ont suffisamment de réservations pour les tâches.</span><span class="sxs-lookup"><span data-stu-id="31e04-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="31e04-149">Tout d’abord, créez un espace réservé ou une ressource générique qui décrit les caractéristiques de la ressource nommée que vous souhaitez travailler sur des tâches en générant une équipe après avoir attribué des rôles à des tâches.</span><span class="sxs-lookup"><span data-stu-id="31e04-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="31e04-150">Voici la méthode pour le faire :</span><span class="sxs-lookup"><span data-stu-id="31e04-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="31e04-151">Dans la structure de répartition du travail, sélectionnez une tâche.</span><span class="sxs-lookup"><span data-stu-id="31e04-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="31e04-152">Sélectionnez l’icône de menu déroulant **Rôle attribué** dans la cellule de ressource.</span><span class="sxs-lookup"><span data-stu-id="31e04-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="31e04-153">Sélectionnez le menu déroulant **Rôle** et sélectionnez le rôle pour la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="31e04-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="31e04-154">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="31e04-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="31e04-155">![Capture d’écran de l’utilisation de WBS pour ajouter une ressource](media/FAQ-Resources-to-Tasks2-4.png "Capture d’écran de l’utilisation de WBS pour ajouter une ressource")</span><span class="sxs-lookup"><span data-stu-id="31e04-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="31e04-156">Une fois que vous avez terminé d’attribuer des rôles aux tâches dans la WBS, sélectionnez **Générer une équipe de projet**.</span><span class="sxs-lookup"><span data-stu-id="31e04-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="31e04-157">Project Service crée le nombre minimal de membres d’équipe génériques selon les rôles, les unités d’organisation d’allocation des ressources, et le calendrier de projet en regroupant les attributions des tâches.</span><span class="sxs-lookup"><span data-stu-id="31e04-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="31e04-158">![Capture d’écran de la génération de l’équipe du projet](media/FAQ-Resources-to-Tasks2-5.png "Capture d’écran de la génération de l’équipe du projet")</span><span class="sxs-lookup"><span data-stu-id="31e04-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="31e04-159">Dans la grille du membre de l’équipe, vous verrez des ressources de type de ressource générique avec le nom de rôle et de poste.</span><span class="sxs-lookup"><span data-stu-id="31e04-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="31e04-160">Si deux ressources sont nécessaires pour qu’un rôle termine le travail, la fonctionnalité Générer une équipe crée deux membres d’équipe et utilise les noms de poste pour les distinguer.</span><span class="sxs-lookup"><span data-stu-id="31e04-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="31e04-161">![Capture d’écran de l’ajout de deux ressources génériques](media/FAQ-Resources-to-Tasks2-6.png "Capture d’écran de l’ajout de deux ressources génériques")</span><span class="sxs-lookup"><span data-stu-id="31e04-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="31e04-162">Vous pouvez ouvrir le besoin en ressources de sauvegarde pour le membre de l’équipe générique en sélectionnant le lien sous Besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="31e04-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="31e04-163">![Capture d’écran de l’ouverture des ressources de sauvegarde requises](media/FAQ-Resources-to-Tasks2-7.png "Capture d’écran de l’ouverture des ressources de sauvegarde requises")</span><span class="sxs-lookup"><span data-stu-id="31e04-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="31e04-164">Sélectionnez **Réserver** pour la ressource générique, puis utilisez le tableau de planification pour rechercher et réserver une ressource réelle.</span><span class="sxs-lookup"><span data-stu-id="31e04-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="31e04-165">Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources en sélectionnant **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="31e04-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="31e04-166">Lorsque la ressource générique est exécutée avec une ressource nommée, la ressource générique est supprimée de l’équipe et les attributions de tâches pour la ressource générique sont attribuées à la ressource nommée qui a renseigné le besoin en ressources de la ressource générique.</span><span class="sxs-lookup"><span data-stu-id="31e04-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]