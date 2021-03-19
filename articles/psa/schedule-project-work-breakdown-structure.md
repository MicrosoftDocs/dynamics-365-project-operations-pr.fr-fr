---
title: Planifier un projet avec une structure de répartition du travail
description: Procédure de planification d’un projet avec une structure de répartition du travail dans Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282690"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="64432-103">Planifier un projet avec une structure de répartition du travail (Project Service)</span><span class="sxs-lookup"><span data-stu-id="64432-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="64432-104">Un calendrier de projet communique le travail à effectuer, quelles ressources exécuteront le travail, et le délai dans lequel le travail doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="64432-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="64432-105">Le calendrier de projet reflète toutes les tâches associées à l’exécution du projet dans les temps.</span><span class="sxs-lookup"><span data-stu-id="64432-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="64432-106">L’une des premières étapes au cours de la phase d’initiation du projet est de proposer un calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="64432-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="64432-107">Pour créer un calendrier de projet, vous devez créer une structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="64432-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="64432-108">Créez une structure de projet avec une structure de répartition du travail, qui vous aide à :</span><span class="sxs-lookup"><span data-stu-id="64432-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="64432-109">Diviser le travail en tâches gérables</span><span class="sxs-lookup"><span data-stu-id="64432-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="64432-110">Évaluer le temps requis pour effectuer une tâche</span><span class="sxs-lookup"><span data-stu-id="64432-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="64432-111">Définir des dépendances de tâche et la durée des tâches</span><span class="sxs-lookup"><span data-stu-id="64432-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="64432-112">Déterminer les rôles requis pour effectuer chaque tâche</span><span class="sxs-lookup"><span data-stu-id="64432-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="64432-113">Le calendrier de projet dans la structure de répartition du travail semble familier, et est complété par un diagramme de Gantt interactif.</span><span class="sxs-lookup"><span data-stu-id="64432-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="64432-114">Créer une structure de répartition du travail pour un projet</span><span class="sxs-lookup"><span data-stu-id="64432-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="64432-115">Créez une structure de répartition du travail pour représenter la séquence des tâches dans un projet.</span><span class="sxs-lookup"><span data-stu-id="64432-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="64432-116">La structure de répartition du travail comprend des tâches, des exigences pour chaque tâche, et des informations sur le revenu et les coûts.</span><span class="sxs-lookup"><span data-stu-id="64432-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="64432-117">Dans la structure de répartition du travail, vous pouvez ajouter :</span><span class="sxs-lookup"><span data-stu-id="64432-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="64432-118">La séquence de tâches dans une hiérarchie</span><span class="sxs-lookup"><span data-stu-id="64432-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="64432-119">D’autres tâches, le cas échéant, qui doivent être effectuées avant de commencer une tâche</span><span class="sxs-lookup"><span data-stu-id="64432-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="64432-120">La date de début, la date de fin, et la durée d’une tâche</span><span class="sxs-lookup"><span data-stu-id="64432-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="64432-121">Le nombre d’heures requises pour une tâche</span><span class="sxs-lookup"><span data-stu-id="64432-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="64432-122">Toutes les compétences et formations requises des employés</span><span class="sxs-lookup"><span data-stu-id="64432-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="64432-123">Les employés qui sont assignés à une tâche</span><span class="sxs-lookup"><span data-stu-id="64432-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="64432-124">Le revenu et les coûts estimés</span><span class="sxs-lookup"><span data-stu-id="64432-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="64432-125">Types de tâche</span><span class="sxs-lookup"><span data-stu-id="64432-125">Task types</span></span>  
<span data-ttu-id="64432-126">Vous utiliserez les types de tâches suivantes lors de la création de votre structure de répartition du travail :</span><span class="sxs-lookup"><span data-stu-id="64432-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="64432-127">**Nœud racine du projet**.</span><span class="sxs-lookup"><span data-stu-id="64432-127">**Project root node**</span></span> | <span data-ttu-id="64432-128">La tâche récapitulative de niveau supérieur du projet.</span><span class="sxs-lookup"><span data-stu-id="64432-128">The top-level summary task for the project.</span></span> <span data-ttu-id="64432-129">Toutes les autres tâches du projet sont créées en dessous.</span><span class="sxs-lookup"><span data-stu-id="64432-129">All other project tasks are created under it.</span></span> <span data-ttu-id="64432-130">Le nom de la tâche racine est le nom du projet.</span><span class="sxs-lookup"><span data-stu-id="64432-130">The name of the root task is the project name.</span></span> <span data-ttu-id="64432-131">L’effort, les dates, et la durée du nœud racine sont basés sur les valeurs dans la hiérarchie en dessous.</span><span class="sxs-lookup"><span data-stu-id="64432-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="64432-132">Vous ne pouvez pas modifier les propriétés de nœud racine ou supprimer le nœud racine.</span><span class="sxs-lookup"><span data-stu-id="64432-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="64432-133">**Tâches récapitulatives ou de conteneur**</span><span class="sxs-lookup"><span data-stu-id="64432-133">**Summary or container tasks**</span></span> | <span data-ttu-id="64432-134">Une tâche récapitulative est une tâche qui a des sous-tâches.</span><span class="sxs-lookup"><span data-stu-id="64432-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="64432-135">Une tâche récapitulative n’a pas d’efforts ou coûts de travail qui lui sont propres.</span><span class="sxs-lookup"><span data-stu-id="64432-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="64432-136">Ses efforts et coûts de travail sont un cumul de ses sous-tâches.</span><span class="sxs-lookup"><span data-stu-id="64432-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="64432-137">Vous pouvez modifier le nom d’une tâche récapitulative, mais vous ne pouvez pas modifier l’effort, les dates, ou la durée, car ils sont automatiquement calculés.</span><span class="sxs-lookup"><span data-stu-id="64432-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="64432-138">La suppression d’une tâche récapitulative entraîne la suppression de la tâche et toutes ses sous-tâches.</span><span class="sxs-lookup"><span data-stu-id="64432-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="64432-139">**Tâches de nœud terminal**</span><span class="sxs-lookup"><span data-stu-id="64432-139">**Leaf node tasks**</span></span> | <span data-ttu-id="64432-140">Une tâche de nœud terminal représente le travail le plus détaillé du projet.</span><span class="sxs-lookup"><span data-stu-id="64432-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="64432-141">Elle possède un effort estimé, un nombre de ressources planifiées, des dates de début et de fin planifiées, et une durée.</span><span class="sxs-lookup"><span data-stu-id="64432-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="64432-142">Hiérarchie de tâche</span><span class="sxs-lookup"><span data-stu-id="64432-142">Task hierarchy</span></span>  
 <span data-ttu-id="64432-143">Vous avez les options suivantes lorsque vous créez une hiérarchie de tâche :</span><span class="sxs-lookup"><span data-stu-id="64432-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="64432-144">**Ajouter une tâche**.</span><span class="sxs-lookup"><span data-stu-id="64432-144">**Add task**.</span></span>   <span data-ttu-id="64432-145">Vous pouvez ajouter une tâche à un emplacement choisi dans la hiérarchie de tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="64432-146">Si vous ne sélectionnez pas d’emplacement, votre nouvelle tâche apparaît à la fin.</span><span class="sxs-lookup"><span data-stu-id="64432-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="64432-147">**Mettre une tâche en retrait**.</span><span class="sxs-lookup"><span data-stu-id="64432-147">**Indent task**.</span></span>   <span data-ttu-id="64432-148">Mettez une tâche en retrait pour en faire un enfant de la tâche directement au-dessus.</span><span class="sxs-lookup"><span data-stu-id="64432-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="64432-149">**Mettre une tâche en retrait négatif**.</span><span class="sxs-lookup"><span data-stu-id="64432-149">**Outdent task**.</span></span>   <span data-ttu-id="64432-150">Mettez une tâche en retrait négatif pour qu’elle ne soit plus une sous-tâche de sa tâche parente d’origine.</span><span class="sxs-lookup"><span data-stu-id="64432-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="64432-151">**Monter et descendre**.</span><span class="sxs-lookup"><span data-stu-id="64432-151">**Move up and Move down**.</span></span>   <span data-ttu-id="64432-152">Déplacez des tâches vers le haut et le bas dans la hiérarchie de sa tâche parente.</span><span class="sxs-lookup"><span data-stu-id="64432-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="64432-153">Le déplacement d’une tâche vers le haut ou le bas n’a aucun impact sur ses coûts, son effort, ses dates, ou sa durée.</span><span class="sxs-lookup"><span data-stu-id="64432-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="64432-154">Attributs de tâche</span><span class="sxs-lookup"><span data-stu-id="64432-154">Task attributes</span></span>  
 <span data-ttu-id="64432-155">Un nom de tâche décrit le travail devant être effectué.</span><span class="sxs-lookup"><span data-stu-id="64432-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="64432-156">Vous utilisez divers attributs de tâche pour décrire la planification et les exigences en dotation de personnel pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="64432-157">Attributs de planification</span><span class="sxs-lookup"><span data-stu-id="64432-157">Schedule attributes</span></span>

 - <span data-ttu-id="64432-158">Attribuez des valeurs à **Heures d’effort**, **Nombre de ressources**, **Date de début**, **Date de fin** et **Durée** pour déterminer la planification de la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="64432-159">**Effort** est une estimation des heures nécessaires pour terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="64432-160">**Nombre de ressources** est une estimation que le responsable de projet saisit dans la tâche pour fournir la meilleure planification.</span><span class="sxs-lookup"><span data-stu-id="64432-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="64432-161">**Durée** (en jours) affiche le nombre de jours de travail nécessaires pour terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="64432-162">Attributs de dotation de personnel</span><span class="sxs-lookup"><span data-stu-id="64432-162">Staffing attributes</span></span>

 - <span data-ttu-id="64432-163">**Rôle**, **Unité d’organisation de ressources**, **Nombre de ressources** et **Ressources** décrivent les exigences en dotation de personnel pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="64432-164">**Rôle** décrit le type de ressource nécessaire pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="64432-165">**Unité d’organisation de ressources** indique l’unité d’organisation dont les ressources doivent provenir pour cette tâche ; cela a également un impact sur les estimations de coûts et de ventes de la tâche, puisque c’est pris en compte pour déterminer le prix de vente unitaire de la ressource.</span><span class="sxs-lookup"><span data-stu-id="64432-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="64432-166">**Ressources** conserve une ressource générique ou une ressource nommée lorsqu’il en y a une.</span><span class="sxs-lookup"><span data-stu-id="64432-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="64432-167">Dépendances de tâche</span><span class="sxs-lookup"><span data-stu-id="64432-167">Task dependencies</span></span>  
 <span data-ttu-id="64432-168">Vous pouvez créer des relations de prédécesseur entre une ou plusieurs tâches dans la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="64432-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="64432-169">Vous pouvez définir une ou plusieurs valeurs pour le champ de prédécesseur sur les tâches pour afficher les tâches dont il sera dépendant.</span><span class="sxs-lookup"><span data-stu-id="64432-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="64432-170">Lorsque vous attribuez une valeur de prédécesseur à une tâche, la tâche peut uniquement démarrer lorsque toutes les tâches de prédécesseur sont terminées.</span><span class="sxs-lookup"><span data-stu-id="64432-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="64432-171">La définition de cette dépendance sur une tâche entraînera le recalcul de la date de début planifiée de la tâche comme la dernière date de fin de tous ses prédécesseurs.</span><span class="sxs-lookup"><span data-stu-id="64432-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="64432-172">Les impacts associés au prédécesseur sur un programme ne sont pas limités par le mode de tâche défini sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="64432-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="64432-173">Mode de tâche</span><span class="sxs-lookup"><span data-stu-id="64432-173">Task mode</span></span>  
 <span data-ttu-id="64432-174">Le mode de tâche est l’un des facteurs importants qui déterminent la planification des tâches de nœud terminal.</span><span class="sxs-lookup"><span data-stu-id="64432-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="64432-175">Il existe deux modes de tâche pour chaque tâche : le mode de planification automatique et le mode de planification manuelle.</span><span class="sxs-lookup"><span data-stu-id="64432-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="64432-176">**Planification automatique**</span><span class="sxs-lookup"><span data-stu-id="64432-176">**Auto scheduling**.</span></span>   <span data-ttu-id="64432-177">Lorsque vous définissez le mode de tâche sur Planifiée automatiquement, le moteur de planification de tâche s’appuie sur les règles de planification sur les attributs de tâche suivants pour déterminer la planification de la tâche :</span><span class="sxs-lookup"><span data-stu-id="64432-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="64432-178">Prédécesseurs</span><span class="sxs-lookup"><span data-stu-id="64432-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="64432-179">Effort</span><span class="sxs-lookup"><span data-stu-id="64432-179">Effort</span></span>  
  
    -   <span data-ttu-id="64432-180">Nombre de ressources</span><span class="sxs-lookup"><span data-stu-id="64432-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="64432-181">Les dates de début et de fin</span><span class="sxs-lookup"><span data-stu-id="64432-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="64432-182">**Mes règles de planification**.</span><span class="sxs-lookup"><span data-stu-id="64432-182">**Scheduling rules**.</span></span>   <span data-ttu-id="64432-183">La date de début d’une tâche de nœud terminal qui ne dispose pas de prédécesseurs par défaut à la date de début de planification du projet.</span><span class="sxs-lookup"><span data-stu-id="64432-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="64432-184">La durée d’une tâche de nœud terminal est toujours calculée comme le nombre de jours ouvrables entre ses dates de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="64432-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="64432-185">Lorsqu’une tâche est planifiée automatiquement, le moteur de planification suit les règles ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="64432-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="64432-186">Les dates de début et de fin d’une tâche doivent toujours être des jours ouvrables selon le calendrier de planification du projet</span><span class="sxs-lookup"><span data-stu-id="64432-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="64432-187">La date de début d’une tâche qui possède des prédécesseurs par défaut à la dernière date de fin de ses prédécesseurs</span><span class="sxs-lookup"><span data-stu-id="64432-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="64432-188">Effort = nombre de personnes \* durée \* heures dans un jour de travail standard du calendrier de projet</span><span class="sxs-lookup"><span data-stu-id="64432-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="64432-189">**Planification manuelle**.</span><span class="sxs-lookup"><span data-stu-id="64432-189">**Manual scheduling**.</span></span>   <span data-ttu-id="64432-190">Dans certains cas, vous pourriez vouloir dévier de ces règles.</span><span class="sxs-lookup"><span data-stu-id="64432-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="64432-191">Dans ces cas-là, vous pouvez définir le mode de tâche pour que la tâche soit planifiée manuellement.</span><span class="sxs-lookup"><span data-stu-id="64432-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="64432-192">Le moteur de planification arrête de calculer les valeurs pour d’autres attributs de planification.</span><span class="sxs-lookup"><span data-stu-id="64432-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="64432-193">La définition de prédécesseurs sur des tâches a un impact sur la date de début de la tâche dépendante.</span><span class="sxs-lookup"><span data-stu-id="64432-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="64432-194">Créer une structure de répartition du travail</span><span class="sxs-lookup"><span data-stu-id="64432-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="64432-195">Accédez à **Project Service > Projets**.</span><span class="sxs-lookup"><span data-stu-id="64432-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="64432-196">Cliquez sur le projet sur lequel vous souhaitez travailler.</span><span class="sxs-lookup"><span data-stu-id="64432-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="64432-197">Dans la barre dans toute la partie supérieure de l’écran, sélectionnez la flèche vers le bas en regard du nom de projet, puis cliquez sur Structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="64432-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="64432-198">Pour ajouter une tâche, cliquez sur **Ajouter une tâche**.</span><span class="sxs-lookup"><span data-stu-id="64432-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="64432-199">Renseignez les champs requis pour la tâche et cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="64432-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="64432-200">Continuez d’ajouter des tâches jusqu’à ce que votre structure de répartition du travail soit complète.</span><span class="sxs-lookup"><span data-stu-id="64432-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="64432-201">Lors de la création de votre structure de répartition du travail, vous pouvez procéder comme suit pour organiser les tâches :</span><span class="sxs-lookup"><span data-stu-id="64432-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="64432-202">Sélectionnez une tâche et cliquez sur **Retrait** pour la déplacer sous une autre tâche ou sur Retrait négatif pour la sortir d’un niveau.</span><span class="sxs-lookup"><span data-stu-id="64432-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="64432-203">Sélectionnez une tâche et cliquez sur **Monter** ou **Descendre** pour la déplacer vers le haut ou le bas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="64432-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="64432-204">Cliquez sur **Masquer le diagramme de Gantt** pour masquer le diagramme de Gantt, puis cliquez sur **Afficher le diagramme de Gantt** pour l’afficher de nouveau.</span><span class="sxs-lookup"><span data-stu-id="64432-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="64432-205">Sélectionnez une période autre pour le diagramme de Gantt dans **Échelle de temps**.</span><span class="sxs-lookup"><span data-stu-id="64432-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="64432-206">Pour ajouter les rôles spécifiés dans votre structure de répartition du travail aux membres de l’équipe de projet, cliquez sur **Générer une équipe de projet**.</span><span class="sxs-lookup"><span data-stu-id="64432-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="64432-207">Cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l’écran lorsque vous avez fini d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="64432-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="64432-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64432-208">See Also</span></span>  
 [<span data-ttu-id="64432-209">Guide du responsable de projet</span><span class="sxs-lookup"><span data-stu-id="64432-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]