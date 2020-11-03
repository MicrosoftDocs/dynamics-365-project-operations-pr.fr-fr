---
title: Considérations relatives à la mise à niveau de la structure de répartition du travail
description: Cette rubrique donne des informations sur la mise à niveau de la structure de répartition du travail de Project Service Automation version 2.x vers la version 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075822"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="cbfb5-103">Considérations relatives à la mise à niveau de la structure de répartition du travail</span><span class="sxs-lookup"><span data-stu-id="cbfb5-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="cbfb5-104">Cette rubrique donne des informations sur la mise à niveau de la structure de répartition du travail de Project Service Automation version 2.x vers la version 3.x.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="cbfb5-105">Cette rubrique définit l'état d'intégrité d'un projet dans Project Service Automation (PSA) qui est nécessaire pour une mise à niveau réussie.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="cbfb5-106">Elle fournit également des informations sur les situations de blocage courantes qui provoquent l'échec de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="cbfb5-107">Pour plus d'informations sur la définition de tâches de projet et leurs fonctions dans une planification de projet, consultez [Planifications de projets](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="cbfb5-108">Entités clés</span><span class="sxs-lookup"><span data-stu-id="cbfb5-108">Key entities</span></span>
<span data-ttu-id="cbfb5-109">Pour une structure de répartition du travail précise qui est déjà chargée avec des ressources, les entités suivantes sont nécessaires :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="cbfb5-110">Projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="cbfb5-111">Équipe du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="cbfb5-112">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="cbfb5-113">Affectations de ressources</span><span class="sxs-lookup"><span data-stu-id="cbfb5-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="cbfb5-114">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="cbfb5-115">Ressources réservables</span><span class="sxs-lookup"><span data-stu-id="cbfb5-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="cbfb5-116">Pour définir une structure de répartition du travail chargée avec des ressources, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="cbfb5-117">Créer un projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-117">Create a new project.</span></span> <span data-ttu-id="cbfb5-118">Pour plus d'informations sur la création d'un projet, consultez [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="cbfb5-119">Créer une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-119">Create one or more tasks.</span></span> <span data-ttu-id="cbfb5-120">Pour plus d'informations sur la création d'une tâche, consultez [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="cbfb5-121">Définir les dépendances de tâche.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-121">Define the task dependencies.</span></span> <span data-ttu-id="cbfb5-122">Pour plus d'informations, voir [Dépendance des tâches du projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="cbfb5-123">Affecter les membres de l'équipe du projet au projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-123">Assign project team members to the project.</span></span> <span data-ttu-id="cbfb5-124">Pour plus d'informations, consultez [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="cbfb5-125">Affecter les membres de l'équipe du projet aux tâches.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="cbfb5-126">Pour plus d'informations, consultez [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="cbfb5-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="cbfb5-127">Relations entre les membres de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-127">Project team relationships</span></span>

<span data-ttu-id="cbfb5-128">Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="cbfb5-129">Tous les membres de l'équipe du projet doivent être associés à une ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="cbfb5-130">Tous les membres de l'équipe du projet doivent être associés au même projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="cbfb5-131">Relations entre les tâches du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-131">Project task relationships</span></span>
<span data-ttu-id="cbfb5-132">Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="cbfb5-133">Les tâches connexes doivent être associées au même projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="cbfb5-134">Chaque tâche de ligne doit avoir une tâche parente.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="cbfb5-135">Chaque tâche doit avoir un projet parent.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="cbfb5-136">Conditions valides</span><span class="sxs-lookup"><span data-stu-id="cbfb5-136">Valid conditions</span></span>

- <span data-ttu-id="cbfb5-137">Toutes les durées de tâche doivent être supérieures ou égales à (>=) une heure et inférieures à 1 800 000 minutes (1 250 jours).\*</span><span class="sxs-lookup"><span data-stu-id="cbfb5-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="cbfb5-138">Toutes les tâches doivent avoir une date de début qui n'est pas antérieure au 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="cbfb5-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="cbfb5-139">Toutes les tâches doivent avoir une date de début qui ne dépasse pas 17 ans à compter de la date du jour.\*</span><span class="sxs-lookup"><span data-stu-id="cbfb5-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="cbfb5-140">Toutes les tâches doivent avoir une date de début antérieure ou égale à la date de fin.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="cbfb5-141">Tous les types de transaction dans les classifications (Dépenses, Matériel, Taxes et Temps) doivent avoir des valeurs pour **Unité par défaut** et **Groupe d'unités**.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="cbfb5-142">Les formats de date avec des lettres doivent être évités.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="cbfb5-143">Étapes d'atténuation potentielles</span><span class="sxs-lookup"><span data-stu-id="cbfb5-143">Potential mitigation steps</span></span>
- <span data-ttu-id="cbfb5-144">Utilisez la recherche avancée pour identifier les tâches du projet qui ne contiennent pas d'ID de projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="cbfb5-145">Utilisez la recherche avancée pour identifier les tâches du projet dont la durée planifiée est supérieure à > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="cbfb5-146">Avant d'apporter des modifications aux données, vous devez rechercher les personnalisations associées à l'entité qui ont pu aboutir à la génération des données dans un état incorrect.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="cbfb5-147">Ces personnalisations doivent être traitées avant de procéder à toute mise à jour des données.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="cbfb5-148">Pour les tâches identifiées qui sont devenues orphelines, pensez à supprimer ces tâches si elles sont inutiles ou si elles doivent être associées au projet parent correct.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="cbfb5-149">Pour les tâches dont la durée est supérieure à 1 250 jours, pensez à ajouter plusieurs tâches pour représenter la durée totale, si possible.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="cbfb5-150">Les éléments signalés par un astérisque (\*) ont des limites dues au fait que la gestion de la relation client (CRM) ne prend en charge que 7 320 extensions de périodicité.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="cbfb5-151">Vous devez rester en dessous de cette limite.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="cbfb5-152">Relations entre les affectations de ressources</span><span class="sxs-lookup"><span data-stu-id="cbfb5-152">Resource Assignment relationships</span></span>
<span data-ttu-id="cbfb5-153">Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="cbfb5-154">Toutes les affectations de ressources dans une structure de répartition du travail doivent être associées au même projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="cbfb5-155">Toutes les affectations de ressources dans une structure de répartition du travail doivent être associées aux membres de l'équipe du projet dans le même projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="cbfb5-156">Étapes d'atténuation potentielles</span><span class="sxs-lookup"><span data-stu-id="cbfb5-156">Potential mitigation steps</span></span>
- <span data-ttu-id="cbfb5-157">Identifiez toutes les tâches qui ne remplissent pas les conditions décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="cbfb5-158">Les affectations de ressources qui ne sont plus valides doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="cbfb5-159">Relations entre les dépendances de tâche du projet</span><span class="sxs-lookup"><span data-stu-id="cbfb5-159">Project task dependency relationships</span></span>
<span data-ttu-id="cbfb5-160">Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :</span><span class="sxs-lookup"><span data-stu-id="cbfb5-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="cbfb5-161">Toutes les dépendances de tâche du projet doivent être associées au même projet.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="cbfb5-162">Une tâche ne peut pas avoir la même dépendance référencée plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="cbfb5-162">A task can't have the same dependency referenced more than once.</span></span>
