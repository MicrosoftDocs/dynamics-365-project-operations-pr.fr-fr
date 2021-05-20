---
title: Modes de planification
description: Cette rubrique fournit des informations sur les modes de planification.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981432"
---
# <a name="scheduling-modes"></a><span data-ttu-id="147eb-103">Modes de planification</span><span class="sxs-lookup"><span data-stu-id="147eb-103">Scheduling modes</span></span>

<span data-ttu-id="147eb-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="147eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="147eb-105">Dynamics 365 Project Operations permet aux organisations de définir la manière dont elles gèrent les modifications apportées aux variables clés dans les tâches au sein de la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="147eb-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="147eb-106">En fonction des besoins spécifiques de l’organisation, les chefs de projet peuvent apporter des modifications au mode de planification lors de la création d’un projet.</span><span class="sxs-lookup"><span data-stu-id="147eb-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="147eb-107">Il existe trois modes de planification disponibles dans Project Operations :</span><span class="sxs-lookup"><span data-stu-id="147eb-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="147eb-108">Durée fixe (mode par défaut)</span><span class="sxs-lookup"><span data-stu-id="147eb-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="147eb-109">Travail fixe</span><span class="sxs-lookup"><span data-stu-id="147eb-109">Fixed work</span></span>
  - <span data-ttu-id="147eb-110">Unités fixes</span><span class="sxs-lookup"><span data-stu-id="147eb-110">Fixed units</span></span>

<span data-ttu-id="147eb-111">Les valeurs impactées par la définition d’un mode de planification spécifique sont déterminées par la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="147eb-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="147eb-112">Effort (*Travail*) = Durée x Unités</span><span class="sxs-lookup"><span data-stu-id="147eb-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="147eb-113">Lorsque vous définissez le mode de planification d’un projet, vous définissez l’une de ces valeurs, qui ne peut alors pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="147eb-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="147eb-114">Le fait de conserver cette valeur en tant que constante donne la priorité à cette valeur, ce qui avertit le système de ne pas la modifier lorsque les deux autres valeurs changent.</span><span class="sxs-lookup"><span data-stu-id="147eb-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="147eb-115">Le tableau suivant fournit des informations sur les impacts liés à la sélection d’un mode spécifique.</span><span class="sxs-lookup"><span data-stu-id="147eb-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="147eb-116">**Dans cette tâche**</span><span class="sxs-lookup"><span data-stu-id="147eb-116">**In this task**</span></span>             | <span data-ttu-id="147eb-117">**Si vous révisez les unités**</span><span class="sxs-lookup"><span data-stu-id="147eb-117">**If you revise units**</span></span>   | <span data-ttu-id="147eb-118">**Si vous révisez la durée**</span><span class="sxs-lookup"><span data-stu-id="147eb-118">**If you revise duration**</span></span> | <span data-ttu-id="147eb-119">**Si vous révisez l’effort**</span><span class="sxs-lookup"><span data-stu-id="147eb-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="147eb-120">Tâche avec unités fixes</span><span class="sxs-lookup"><span data-stu-id="147eb-120">Fixed units task</span></span>     | <span data-ttu-id="147eb-121">La durée est recalculée.</span><span class="sxs-lookup"><span data-stu-id="147eb-121">Duration is recalculated.</span></span> | <span data-ttu-id="147eb-122">L’effort est recalculé.</span><span class="sxs-lookup"><span data-stu-id="147eb-122">Effort is recalculated.</span></span>    | <span data-ttu-id="147eb-123">La durée est recalculée.</span><span class="sxs-lookup"><span data-stu-id="147eb-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="147eb-124">Tâche avec effort fixe</span><span class="sxs-lookup"><span data-stu-id="147eb-124">Fixed effort task</span></span>    | <span data-ttu-id="147eb-125">La durée est recalculée.</span><span class="sxs-lookup"><span data-stu-id="147eb-125">Duration is recalculated.</span></span> | <span data-ttu-id="147eb-126">Les unités sont recalculées.</span><span class="sxs-lookup"><span data-stu-id="147eb-126">Units are recalculated.</span></span>    | <span data-ttu-id="147eb-127">La durée est recalculée.</span><span class="sxs-lookup"><span data-stu-id="147eb-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="147eb-128">Tâche avec durée fixe</span><span class="sxs-lookup"><span data-stu-id="147eb-128">Fixed duration task</span></span>  | <span data-ttu-id="147eb-129">L’effort est recalculé.</span><span class="sxs-lookup"><span data-stu-id="147eb-129">Effort is recalculated.</span></span>   | <span data-ttu-id="147eb-130">L’effort est recalculé.</span><span class="sxs-lookup"><span data-stu-id="147eb-130">Effort is recalculated.</span></span>    | <span data-ttu-id="147eb-131">Les unités sont recalculées.</span><span class="sxs-lookup"><span data-stu-id="147eb-131">Units are recalculated.</span></span>   |

<span data-ttu-id="147eb-132">Pour plus d’informations sur les implications d’un mode donné, voir [Modifier le type de tâche pour obtenir une planification plus précise](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="147eb-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="147eb-133">Dans la rubrique, le terme **Travail** est utilisé à la place du terme **Effort**.</span><span class="sxs-lookup"><span data-stu-id="147eb-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="147eb-134">Changer le mode de planification de l’organisation</span><span class="sxs-lookup"><span data-stu-id="147eb-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="147eb-135">Procédez comme suit pour définir le mode de planification d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="147eb-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="147eb-136">Accédez à **Paramètres** \> **Général** \> **Paramètres**, puis sélectionnez le paramètre du projet.</span><span class="sxs-lookup"><span data-stu-id="147eb-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="147eb-137">Sur la page **Paramètres du projet**, sélectionnez le mode de planification par défaut pour l’organisation, puis définissez si le chef de projet peut remplacer le paramètre lors de la création d’un projet.</span><span class="sxs-lookup"><span data-stu-id="147eb-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="147eb-138">Modifier le paramètre du mode de planification sur un projet</span><span class="sxs-lookup"><span data-stu-id="147eb-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="147eb-139">Si une organisation autorise le chef de projet à remplacer le mode de planification par défaut, le chef de projet peut effectuer cette modification lorsqu’il crée un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="147eb-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="147eb-140">Cependant, une fois le projet enregistré, le mode de planification ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="147eb-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="147eb-141">Projets copiés</span><span class="sxs-lookup"><span data-stu-id="147eb-141">Copied projects</span></span>

<span data-ttu-id="147eb-142">Étant donné qu’un projet est créé lorsque l’action de copie de projet est effectuée, le chef de projet ne peut pas définir le mode de planification.</span><span class="sxs-lookup"><span data-stu-id="147eb-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="147eb-143">Le projet de destination utilisera toujours par défaut le mode défini au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="147eb-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="147eb-144">Tâches copiées</span><span class="sxs-lookup"><span data-stu-id="147eb-144">Copied tasks</span></span>

<span data-ttu-id="147eb-145">Lorsqu’une tâche est copiée d’un projet à un autre, la tâche hérite du mode de planification du projet de destination.</span><span class="sxs-lookup"><span data-stu-id="147eb-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
