---
title: Modifications de la gestion des ressources (Project Service Automation 3.x)
description: Cette rubrique fournit des informations sur les modifications du secteur de la gestion des ressources.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007813"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="a8284-103">Modifications de la gestion des ressources (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="a8284-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="a8284-104">Les sections de cette rubrique fournissent des informations sur les modifications apportées au secteur de la gestion des ressources de Dynamics 365 Project Service Automation version 3.x.</span><span class="sxs-lookup"><span data-stu-id="a8284-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="a8284-105">Estimations de projets</span><span class="sxs-lookup"><span data-stu-id="a8284-105">Project estimates</span></span>

<span data-ttu-id="a8284-106">Au lieu d’être basées sur l’entité **msdyn\_projecttask** (**Tâche du projet**), les estimations de projet sont basées sur l’entité **msdyn\_resourceassignment** (**Attribution de ressource**).</span><span class="sxs-lookup"><span data-stu-id="a8284-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="a8284-107">Les affectation de ressources sont devenues la « source fiable » pour la planification et la tarification d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="a8284-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="a8284-108">Tâches de ligne</span><span class="sxs-lookup"><span data-stu-id="a8284-108">Line tasks</span></span>

<span data-ttu-id="a8284-109">Dans PSA 3.x, les tâches de ligne sont obsolètes (déconseillées).</span><span class="sxs-lookup"><span data-stu-id="a8284-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="a8284-110">Les attributions indiquent maintenant la totalité de la tâche au lieu des tâches de ligne.</span><span class="sxs-lookup"><span data-stu-id="a8284-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="a8284-111">L’exemple suivant explique comment une tâche nommée « Tâche de ligne » est attribuée aux membres de l’équipe A et B dans les précédentes versions de PSA et dans PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a8284-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="a8284-112">**Avant PSA 3.x :**</span><span class="sxs-lookup"><span data-stu-id="a8284-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="a8284-113">Tâche de test</span><span class="sxs-lookup"><span data-stu-id="a8284-113">Test task</span></span>

        - <span data-ttu-id="a8284-114">Tâche de test – Tâche de ligne 1</span><span class="sxs-lookup"><span data-stu-id="a8284-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="a8284-115">Attribution à A</span><span class="sxs-lookup"><span data-stu-id="a8284-115">Assignment to A</span></span>

        - <span data-ttu-id="a8284-116">Tâche de test – Tâche de ligne 2</span><span class="sxs-lookup"><span data-stu-id="a8284-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="a8284-117">Attribution à B</span><span class="sxs-lookup"><span data-stu-id="a8284-117">Assignment to B</span></span>

- <span data-ttu-id="a8284-118">**PSA 3.x :**</span><span class="sxs-lookup"><span data-stu-id="a8284-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="a8284-119">Tâche de test</span><span class="sxs-lookup"><span data-stu-id="a8284-119">Test task</span></span>

        - <span data-ttu-id="a8284-120">Attribution à A</span><span class="sxs-lookup"><span data-stu-id="a8284-120">Assignment to A</span></span>
        - <span data-ttu-id="a8284-121">Attribution à B</span><span class="sxs-lookup"><span data-stu-id="a8284-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="a8284-122">Attribution non attribuée</span><span class="sxs-lookup"><span data-stu-id="a8284-122">Unassigned assignment</span></span>

<span data-ttu-id="a8284-123">Dans PSA 3.x, une attribution non attribuée est une attribution attribuée à un membre de l’équipe **NULL** et à une ressource **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a8284-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="a8284-124">Les attributions non attribuées peuvent se produire dans certains scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="a8284-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="a8284-125">Si une tâche a été créée, mais qu’elle n’a pas encore été attribuée à un membre de l’équipe, une attribution non attribuée est toujours créée.</span><span class="sxs-lookup"><span data-stu-id="a8284-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="a8284-126">Si tous les cessionnaires d’une tâche sont supprimés, une attribution non attribuée est recréée pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="a8284-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="a8284-127">Champs de planification de l’entité Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="a8284-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="a8284-128">Les champs de l’entité **msdyn\_projecttask** ont été rendus obsolètes ou migrés vers l’entité **msdyn\_resourceassignment**, ou ils sont maintenant référencés à partir de l’entité **msdyn\_projectteam** (**Membre de l’équipe du projet**).</span><span class="sxs-lookup"><span data-stu-id="a8284-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="a8284-129">Champ obsolète sur msdyn\_projecttask (Tâche du projet)</span><span class="sxs-lookup"><span data-stu-id="a8284-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8284-130">Nouveau champ sur msdyn\_resourceassignment (Attribution des ressources)</span><span class="sxs-lookup"><span data-stu-id="a8284-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="a8284-131">Commentaire</span><span class="sxs-lookup"><span data-stu-id="a8284-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="a8284-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="a8284-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="a8284-133">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8284-133">None</span></span> | |
| <span data-ttu-id="a8284-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="a8284-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="a8284-135">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8284-135">None</span></span> | |
| <span data-ttu-id="a8284-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="a8284-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="a8284-137">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8284-137">None</span></span> | |
| <span data-ttu-id="a8284-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="a8284-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="a8284-139">Aucune</span><span class="sxs-lookup"><span data-stu-id="a8284-139">None</span></span> | |
| <span data-ttu-id="a8284-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="a8284-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="a8284-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a8284-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="a8284-142">Le format de la structure de données JavaScript Object Notation (JSON) stockée dans le champ a été modifié.</span><span class="sxs-lookup"><span data-stu-id="a8284-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="a8284-143">Profil de la planification</span><span class="sxs-lookup"><span data-stu-id="a8284-143">Schedule contour</span></span>

<span data-ttu-id="a8284-144">Le profil de la planification est stockée dans le champ **Travail planifié** (**msdyn\_plannedwork**) de chaque entité **Attribution de ressource** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="a8284-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="a8284-145">Structure</span><span class="sxs-lookup"><span data-stu-id="a8284-145">Structure</span></span>

<span data-ttu-id="a8284-146">La nouvelle structure du profil de la planification est composée de secteurs de temps flexibles qui sont définis pour chaque jour de la planification.</span><span class="sxs-lookup"><span data-stu-id="a8284-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="a8284-147">Chaque secteurs de temps contient les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8284-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="a8284-148">**Début** : Le début des heures de travail du jour, selon le calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="a8284-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a8284-149">**Fin** : La fin des heures de travail du jour, selon le calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="a8284-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a8284-150">**Heures** : Le nombre d’heures qui sont attribuées ce jour-là.</span><span class="sxs-lookup"><span data-stu-id="a8284-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="a8284-151">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a8284-151">**Example**</span></span>

<span data-ttu-id="a8284-152">Cet exemple utilise un calendrier de projet où la journée de travail est de 9 h 00 à 17 h 00 dans le fuseau horaire UTC-8.</span><span class="sxs-lookup"><span data-stu-id="a8284-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="a8284-153">Planification automatique et planification manuelle</span><span class="sxs-lookup"><span data-stu-id="a8284-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="a8284-154">Si une tâche est planifiée automatiquement, les heures sont chargées à l’avance, et la durée de la tâche peut être réduite.</span><span class="sxs-lookup"><span data-stu-id="a8284-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="a8284-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a8284-155">**Example**</span></span>

<span data-ttu-id="a8284-156">La tâche suivante est programmée automatiquement pour 18 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).</span><span class="sxs-lookup"><span data-stu-id="a8284-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="a8284-157">Si une tâche est planifiée manuellement, les heures sont distribuées à part égales à toutes les dates.</span><span class="sxs-lookup"><span data-stu-id="a8284-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="a8284-158">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a8284-158">**Example**</span></span>

<span data-ttu-id="a8284-159">La tâche suivante est programmée manuellement pour 18 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).</span><span class="sxs-lookup"><span data-stu-id="a8284-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="a8284-160">Unité d’attribution</span><span class="sxs-lookup"><span data-stu-id="a8284-160">Assignment unit</span></span>

<span data-ttu-id="a8284-161">L’unité d’attribution a été rendue obsolète dans PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a8284-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="a8284-162">Les heures d’effort de tâche sont maintenant divisées à parts égales, par jour, parmi toutes les ressources affectées.</span><span class="sxs-lookup"><span data-stu-id="a8284-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="a8284-163">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a8284-163">**Example**</span></span>

<span data-ttu-id="a8284-164">Dans cet exemple, la tâche est attribué à deux ressources et est planifiée automatiquement pour 36 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).</span><span class="sxs-lookup"><span data-stu-id="a8284-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="a8284-165">Attribution 1 :</span><span class="sxs-lookup"><span data-stu-id="a8284-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="a8284-166">Attribution 2 :</span><span class="sxs-lookup"><span data-stu-id="a8284-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="a8284-167">Dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="a8284-167">Pricing dimensions</span></span>

<span data-ttu-id="a8284-168">Dans PSA 3.x, les champs de dimension de tarification spécifiques aux ressources (comme **Rôle** et **Unité d’organisation**) ont été supprimés de l’entité **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a8284-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a8284-169">Ces champs peuvent désormais être récupérés auprès du membre de l’équipe de projet correspondant (**msdyn\_projectteam**) de l’attribution de ressource (**msdyn\_resourceassignment**) lorsque des estimations de projet sont générées.</span><span class="sxs-lookup"><span data-stu-id="a8284-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="a8284-170">Un nouveau champ, **msdyn\_organizationalunit**, a été ajouté à l’entité **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="a8284-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="a8284-171">Champ obsolète sur msdyn\_projecttask (Tâche du projet)</span><span class="sxs-lookup"><span data-stu-id="a8284-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8284-172">Champ de msdyn\_projectteam (Membre de l’équipe de projet) qui est utilisé à la place</span><span class="sxs-lookup"><span data-stu-id="a8284-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="a8284-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a8284-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="a8284-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a8284-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="a8284-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a8284-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="a8284-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a8284-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="a8284-177">Profils</span><span class="sxs-lookup"><span data-stu-id="a8284-177">Contours</span></span>

<span data-ttu-id="a8284-178">Les champs de profil de tarification et d’estimation ont été rendus obsolètes dans l’entité **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a8284-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a8284-179">Ils ont été déplacés vers l’entité **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="a8284-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="a8284-180">Champ obsolète sur msdyn\_projecttask (Tâche du projet)</span><span class="sxs-lookup"><span data-stu-id="a8284-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8284-181">Nouveau champ sur msdyn\_resourceassignment (Attribution des ressources)</span><span class="sxs-lookup"><span data-stu-id="a8284-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="a8284-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a8284-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="a8284-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a8284-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="a8284-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a8284-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="a8284-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a8284-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="a8284-186">Les champs suivants ont été ajoutés à l’entité **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="a8284-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="a8284-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a8284-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a8284-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a8284-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="a8284-189">Les champs suivants des coûts et ventes planifiés, réels et restants sont inchangés sur l’entité **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="a8284-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="a8284-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a8284-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a8284-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a8284-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="a8284-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="a8284-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="a8284-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="a8284-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="a8284-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a8284-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="a8284-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a8284-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]