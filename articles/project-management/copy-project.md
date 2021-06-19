---
title: Copier un projet
description: Cette rubrique donne des informations sur la copie de projets dans Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091251"
---
# <a name="copy-a-project"></a><span data-ttu-id="fc066-103">Copier un projet</span><span class="sxs-lookup"><span data-stu-id="fc066-103">Copy a project</span></span>

<span data-ttu-id="fc066-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="fc066-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc066-105">Avec Dynamics 365 Project Operations, vous pouvez rapidement créer de nouveaux projets en sélectionnant **Copier le projet** dans le formulaire **Projets**.</span><span class="sxs-lookup"><span data-stu-id="fc066-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="fc066-106">Pour copier un projet, ouvrez le projet que vous souhaitez copier, puis sélectionnez **Copier le projet**.</span><span class="sxs-lookup"><span data-stu-id="fc066-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="fc066-107">L’action copiera les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc066-107">The action will copy the following:</span></span>

- <span data-ttu-id="fc066-108">les propriétés du projet ;</span><span class="sxs-lookup"><span data-stu-id="fc066-108">Project properties</span></span> 
- <span data-ttu-id="fc066-109">Structure de répartition du travail</span><span class="sxs-lookup"><span data-stu-id="fc066-109">Work breakdown structure</span></span>
- <span data-ttu-id="fc066-110">Membres de l’équipe du projet</span><span class="sxs-lookup"><span data-stu-id="fc066-110">Project team members</span></span>
- <span data-ttu-id="fc066-111">Estimations de projets</span><span class="sxs-lookup"><span data-stu-id="fc066-111">Project estimates</span></span>
- <span data-ttu-id="fc066-112">les estimations de dépense du projet.</span><span class="sxs-lookup"><span data-stu-id="fc066-112">Project expense estimates</span></span>
- <span data-ttu-id="fc066-113">Estimations du matériel du projet</span><span class="sxs-lookup"><span data-stu-id="fc066-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="fc066-114">les propriétés du projet ;</span><span class="sxs-lookup"><span data-stu-id="fc066-114">Project properties</span></span>

<span data-ttu-id="fc066-115">Lorsque le projet est copié, les valeurs des champs suivants sont copiées :</span><span class="sxs-lookup"><span data-stu-id="fc066-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="fc066-116">Nom</span><span class="sxs-lookup"><span data-stu-id="fc066-116">Name</span></span>
- <span data-ttu-id="fc066-117">Description</span><span class="sxs-lookup"><span data-stu-id="fc066-117">Description</span></span>
- <span data-ttu-id="fc066-118">Client</span><span class="sxs-lookup"><span data-stu-id="fc066-118">Customer</span></span>
- <span data-ttu-id="fc066-119">Modèle de calendrier</span><span class="sxs-lookup"><span data-stu-id="fc066-119">Calendar Template</span></span>
- <span data-ttu-id="fc066-120">Devise</span><span class="sxs-lookup"><span data-stu-id="fc066-120">Currency</span></span>
- <span data-ttu-id="fc066-121">Unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="fc066-121">Contracting Unit</span></span>
- <span data-ttu-id="fc066-122">Manager du projet</span><span class="sxs-lookup"><span data-stu-id="fc066-122">Project Manager</span></span>
- <span data-ttu-id="fc066-123">Statut</span><span class="sxs-lookup"><span data-stu-id="fc066-123">Status</span></span>
- <span data-ttu-id="fc066-124">Statut du projet global</span><span class="sxs-lookup"><span data-stu-id="fc066-124">Overall Project Status</span></span>
- <span data-ttu-id="fc066-125">Commentaires</span><span class="sxs-lookup"><span data-stu-id="fc066-125">Comments</span></span>
- <span data-ttu-id="fc066-126">Estimations</span><span class="sxs-lookup"><span data-stu-id="fc066-126">Estimates</span></span>
- <span data-ttu-id="fc066-127">Date de début estimée : il s’agit de la date à laquelle le projet est créé à partir de la copie.</span><span class="sxs-lookup"><span data-stu-id="fc066-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="fc066-128">Date de fin estimée : cette date est ajustée en fonction de la date de début du nouveau projet créé à partir de la copie.</span><span class="sxs-lookup"><span data-stu-id="fc066-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="fc066-129">Effort (en heures)</span><span class="sxs-lookup"><span data-stu-id="fc066-129">Effort (Hours)</span></span>
- <span data-ttu-id="fc066-130">Coût de main d’œuvre estimé</span><span class="sxs-lookup"><span data-stu-id="fc066-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="fc066-131">Coût des dépenses estimé</span><span class="sxs-lookup"><span data-stu-id="fc066-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="fc066-132">Coût matière estimé</span><span class="sxs-lookup"><span data-stu-id="fc066-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="fc066-133">La copie d’un projet est une opération de longue haleine.</span><span class="sxs-lookup"><span data-stu-id="fc066-133">Copy project is a long running operation.</span></span> <span data-ttu-id="fc066-134">Les enregistrements de projet, leurs attributs pertinents et de nombreuses entités associées sont également copiés.</span><span class="sxs-lookup"><span data-stu-id="fc066-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="fc066-135">En raison de la longueur de l’opération, une fois la copie commencée, la page du projet cible est verrouillée pour modification jusqu’à ce que l’opération de copie soit terminée.</span><span class="sxs-lookup"><span data-stu-id="fc066-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="fc066-136">Structure de répartition du travail</span><span class="sxs-lookup"><span data-stu-id="fc066-136">Work breakdown structure</span></span>

<span data-ttu-id="fc066-137">Lorsque le projet est copié, toute la structure de répartition du travail chargée en ressources est copiée.</span><span class="sxs-lookup"><span data-stu-id="fc066-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="fc066-138">Les ressources nommées sont remplacées par des ressource génériques.</span><span class="sxs-lookup"><span data-stu-id="fc066-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="fc066-139">Si les ressources nommées n’ont pas les mêmes heures de travail que la ressource générique, la planification sera recalculée et la durée des tâches peut changer.</span><span class="sxs-lookup"><span data-stu-id="fc066-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="fc066-140">les membres de l’équipe du projet ;</span><span class="sxs-lookup"><span data-stu-id="fc066-140">Project team members</span></span>

<span data-ttu-id="fc066-141">Lorsqu’une équipe de projet est copiée à partir du projet source, les ressources génériques sont copiées.</span><span class="sxs-lookup"><span data-stu-id="fc066-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="fc066-142">Les affectations de ressources génériques sont également gérées comme elles l’étaient dans le projet source.</span><span class="sxs-lookup"><span data-stu-id="fc066-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="fc066-143">Les ressources nommées seront converties en membres génériques de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="fc066-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="fc066-144">Estimations</span><span class="sxs-lookup"><span data-stu-id="fc066-144">Estimates</span></span>

<span data-ttu-id="fc066-145">Lorsque le projet est copié, les lignes d’estimation des ressources, des dépenses et du matériel sont copiées à partir du projet source.</span><span class="sxs-lookup"><span data-stu-id="fc066-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="fc066-146">Pour plus d’informations sur l’accès par programme à Copier le projet, voir [Développer des modèles de projet avec Copier le projet](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="fc066-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
