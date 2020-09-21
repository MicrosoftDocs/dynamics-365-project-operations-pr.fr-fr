---
title: Progression d'un projet et consommation des coûts
description: Cette rubrique propose des informations sur comment suivre la progression d'un projet et de la consommation des coûts.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168111"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="eba36-103">Progression d'un projet et consommation des coûts</span><span class="sxs-lookup"><span data-stu-id="eba36-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eba36-104">La nécessité de suivre la progression par rapport à une planification varie par secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="eba36-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="eba36-105">Certains secteurs d'activité suivent à un niveau granulaire, pendant que d'autres secteurs d'activité suivent à un niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="eba36-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="eba36-106">Cette rubrique montre comment planifier afin de répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="eba36-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="eba36-107">Vue de suivi des efforts</span><span class="sxs-lookup"><span data-stu-id="eba36-107">Effort tracking view</span></span>

<span data-ttu-id="eba36-108">La vue **Suivi des efforts** suit la progression des tâches dans la planification.</span><span class="sxs-lookup"><span data-stu-id="eba36-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="eba36-109">Elle compare les heures d'effort réelles ayant été consacrées à une tâche aux heures d'effort prévues pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="eba36-110">PSA utilise les formules suivantes pour calculer les mesures de suivi :</span><span class="sxs-lookup"><span data-stu-id="eba36-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="eba36-111">Pourcentage de progression = Cumul des efforts réels consacrés ÷ Efforts planifiés pour la tâche</span><span class="sxs-lookup"><span data-stu-id="eba36-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="eba36-112">Estimation avant achèvement = Efforts planifiés – Cumul des efforts réels consacrés</span><span class="sxs-lookup"><span data-stu-id="eba36-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="eba36-113">Estimation à l'achèvement (EAA) = Efforts restants + Cumul des efforts réels consacrés</span><span class="sxs-lookup"><span data-stu-id="eba36-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="eba36-114">Écart d'efforts escomptés = Efforts planifiés – EAA</span><span class="sxs-lookup"><span data-stu-id="eba36-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="eba36-115">PSA affiche une projection de l'écart d'efforts de la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="eba36-116">Si l'EAA excède les efforts planifiés, la tâche est prévue de prendre plus de temps qu'initialement planifié.</span><span class="sxs-lookup"><span data-stu-id="eba36-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="eba36-117">Par conséquent, il est en retard.</span><span class="sxs-lookup"><span data-stu-id="eba36-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="eba36-118">Si l'EAA est inférieure aux efforts planifiés, la tâche est prévue de prendre moins de temps qu'initialement planifié.</span><span class="sxs-lookup"><span data-stu-id="eba36-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="eba36-119">Par conséquent, il est en avance.</span><span class="sxs-lookup"><span data-stu-id="eba36-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="eba36-120">Nouvelle projection des efforts</span><span class="sxs-lookup"><span data-stu-id="eba36-120">Re-projecting effort</span></span>

<span data-ttu-id="eba36-121">Il arrive souvent qu'un chef de projet modifie les estimations initiales d'une tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="eba36-122">Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l'état actuel de projet.</span><span class="sxs-lookup"><span data-stu-id="eba36-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="eba36-123">Toutefois, il n'est pas recommandé que les chefs de projet modifient les numéros de référence, car la ligne de référence du projet représente la source fiable établie pour les estimations de planning et de coût du projet convenue par toutes les parties prenantes au projet.</span><span class="sxs-lookup"><span data-stu-id="eba36-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="eba36-124">Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peut utiliser un chef de projet :</span><span class="sxs-lookup"><span data-stu-id="eba36-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="eba36-125">Remplacez l'Estimation avant achèvement par défaut par une nouvelle évaluation des efforts restants réels pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="eba36-126">Remplacez le pourcentage de progression par défaut par une nouvelle évaluation de la progression réelle pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="eba36-127">Chacune de ces méthode entraîne un nouveau calcul de l'Estimation avant achèvement, de l'EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l'écart d'efforts escomptés pour une tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="eba36-128">L'Estimation avant achèvement, l'EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l'écart d'efforts.</span><span class="sxs-lookup"><span data-stu-id="eba36-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="eba36-129">Nouvelle projection d'efforts sur les tâches récapitulatives</span><span class="sxs-lookup"><span data-stu-id="eba36-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="eba36-130">Efforts sur les tâches récapitulatives ou les tâches de conteneur peuvent être de nouveau projetés.</span><span class="sxs-lookup"><span data-stu-id="eba36-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="eba36-131">Que l'utilisateur refasse une projection à l'aide des efforts restants ou du pourcentage de progression sur les tâches récapitulatives, l'ensemble de calculs suivant commence :</span><span class="sxs-lookup"><span data-stu-id="eba36-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="eba36-132">L'Estimation avant achèvement, l'EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.</span><span class="sxs-lookup"><span data-stu-id="eba36-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="eba36-133">Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l'EAA d'origine sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="eba36-134">Le nouvel EAA sur chacune des tâches individuelles jusqu'aux tâches de nœud terminal est calculé.</span><span class="sxs-lookup"><span data-stu-id="eba36-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="eba36-135">Les tâches enfants affectées jusqu'aux nœuds terminaux ont leur Estimation avant achèvement et pourcentage de progression recalculés selon la valeur de l'EAA.</span><span class="sxs-lookup"><span data-stu-id="eba36-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="eba36-136">Cela entraîne une nouvelle projection pour l'écart d'efforts de la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="eba36-137">Les EAA des tâches récapitulatives entièrement jusqu'au nœud racine sont recalculés.</span><span class="sxs-lookup"><span data-stu-id="eba36-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="eba36-138">Vue Suivi du coût</span><span class="sxs-lookup"><span data-stu-id="eba36-138">Cost tracking view</span></span> 

<span data-ttu-id="eba36-139">La vue **Suivi du coût** compare le coût réel consacré à une tâche au coût planifié sur une tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="eba36-140">Cette vue affiche uniquement les coûts de main-d'œuvre et n'inclut pas les estimations des coûts des dépenses.</span><span class="sxs-lookup"><span data-stu-id="eba36-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="eba36-141">PSA utilise les formules suivantes pour calculer les mesures de suivi :</span><span class="sxs-lookup"><span data-stu-id="eba36-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="eba36-142">Pourcentage des coûts consommés = Cumul des coûts réels consacrés ÷ Coût planifié pour la tâche</span><span class="sxs-lookup"><span data-stu-id="eba36-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="eba36-143">Coût pour terminer = Coûts planifiés – Cumul des coûts réels consacrés</span><span class="sxs-lookup"><span data-stu-id="eba36-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="eba36-144">EAA = Coût pour terminer + Cumul des coûts réels consacrés</span><span class="sxs-lookup"><span data-stu-id="eba36-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="eba36-145">Écart de coûts projetés = Coûts planifiés – EAA</span><span class="sxs-lookup"><span data-stu-id="eba36-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="eba36-146">Une projection de l'écart de coûts est affiché sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="eba36-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="eba36-147">Si l'EAA excède les coûts planifiés, la tâche est prévue d'être plus coûteux qu'initialement planifié.</span><span class="sxs-lookup"><span data-stu-id="eba36-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="eba36-148">Par conséquent, sa tendance excède le budget.</span><span class="sxs-lookup"><span data-stu-id="eba36-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="eba36-149">Si l'EAA est inférieur aux coûts planifiés, la tâche est prévue d'être moins coûteuse qu'initialement planifié.</span><span class="sxs-lookup"><span data-stu-id="eba36-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="eba36-150">Par conséquent, sa tendance est inférieure au budget.</span><span class="sxs-lookup"><span data-stu-id="eba36-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="eba36-151">Nouvelle projection des coûts du chef de projet</span><span class="sxs-lookup"><span data-stu-id="eba36-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="eba36-152">Lorsque l'effort est de nouveau projeté, l'Estimation avant achèvement, l'EAA (Estimé à Achèvement), le pourcentage des coût consommés et l'écart de coûts projeté sont tous recalculés dans la vue **Suivi du coût**.</span><span class="sxs-lookup"><span data-stu-id="eba36-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="eba36-153">Résumé du statut du projet</span><span class="sxs-lookup"><span data-stu-id="eba36-153">Project status summary</span></span>

<span data-ttu-id="eba36-154">Le suivi des données dans les vues **Suivi d'effort** et **Suivi du coût** affiche la progression et la consommation des coûts au niveau du nœud racine du projet, des tâches récapitulatives et des tâches de nœud terminal.</span><span class="sxs-lookup"><span data-stu-id="eba36-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="eba36-155">La section **Statut** sur la page **Entité de projet** affiche un résumé du statut au niveau du projet.</span><span class="sxs-lookup"><span data-stu-id="eba36-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="eba36-156">Champs récapitulatifs du statut</span><span class="sxs-lookup"><span data-stu-id="eba36-156">Status summary fields</span></span>

<span data-ttu-id="eba36-157">Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global.</span><span class="sxs-lookup"><span data-stu-id="eba36-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="eba36-158">Il utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant.</span><span class="sxs-lookup"><span data-stu-id="eba36-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="eba36-159">Le champ **Commentaires** permet au chef de projet d'entrer des commentaires spécifiques relatifs au statut.</span><span class="sxs-lookup"><span data-stu-id="eba36-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="eba36-160">Le champ **Statut mis à jour le** n'est pas modifiable et la valeur est un horodatage qui indique quand le statut a été mis à jour en dernier.</span><span class="sxs-lookup"><span data-stu-id="eba36-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="eba36-161">Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la date de suivi.</span><span class="sxs-lookup"><span data-stu-id="eba36-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="eba36-162">Lorsque l'écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, vous pouvez définir ces champs sur **En avance**.</span><span class="sxs-lookup"><span data-stu-id="eba36-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="eba36-163">Lorsque l'écart de planification et des coûts du nœud racine est négatif, vous pouvez les définir sur **En retard**.</span><span class="sxs-lookup"><span data-stu-id="eba36-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
