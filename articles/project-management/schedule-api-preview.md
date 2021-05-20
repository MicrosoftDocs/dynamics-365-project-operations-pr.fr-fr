---
title: Utiliser les API de planification pour effectuer des opérations avec des entités de planification
description: Cette rubrique fournit des informations et des exemples d’utilisation des API de planification.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950801"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="4a64f-103">Utiliser les API de planification pour effectuer des opérations avec des entités de planification</span><span class="sxs-lookup"><span data-stu-id="4a64f-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="4a64f-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="4a64f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="4a64f-105">Certaines ou toutes les fonctionnalités mentionnées dans cette rubrique sont disponibles dans le cadre d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="4a64f-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="4a64f-106">Le contenu et les fonctionnalités sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="4a64f-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="4a64f-107">Entités de planification</span><span class="sxs-lookup"><span data-stu-id="4a64f-107">Scheduling entities</span></span>

<span data-ttu-id="4a64f-108">Les API de planification offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="4a64f-109">Ces entités sont gérées via le moteur de planification de l’application Project pour le Web.</span><span class="sxs-lookup"><span data-stu-id="4a64f-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="4a64f-110">Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4a64f-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="4a64f-111">Le tableau suivant fournit une liste complète des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="4a64f-112">Nom de l'entité</span><span class="sxs-lookup"><span data-stu-id="4a64f-112">Entity name</span></span>  | <span data-ttu-id="4a64f-113">Nom logique de l’entité</span><span class="sxs-lookup"><span data-stu-id="4a64f-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="4a64f-114">Project</span><span class="sxs-lookup"><span data-stu-id="4a64f-114">Project</span></span> | <span data-ttu-id="4a64f-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4a64f-115">msdyn_project</span></span> |
| <span data-ttu-id="4a64f-116">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-116">Project Task</span></span>  | <span data-ttu-id="4a64f-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="4a64f-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="4a64f-118">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-118">Project Task Dependency</span></span>  | <span data-ttu-id="4a64f-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="4a64f-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="4a64f-120">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="4a64f-120">Resource Assignment</span></span> | <span data-ttu-id="4a64f-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="4a64f-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="4a64f-122">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-122">Project Bucket</span></span>  | <span data-ttu-id="4a64f-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="4a64f-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="4a64f-124">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-124">Project Team Member</span></span> | <span data-ttu-id="4a64f-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="4a64f-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="4a64f-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="4a64f-126">OperationSet</span></span>

<span data-ttu-id="4a64f-127">OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="4a64f-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="4a64f-128">API de planification</span><span class="sxs-lookup"><span data-stu-id="4a64f-128">Schedule APIs</span></span>

<span data-ttu-id="4a64f-129">Voici une liste des API de planification actuelles.</span><span class="sxs-lookup"><span data-stu-id="4a64f-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="4a64f-130">**msdyn_CreateProjectV1** : Cette API peut être utilisée pour créer un projet.</span><span class="sxs-lookup"><span data-stu-id="4a64f-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="4a64f-131">Le projet et le compartiment de projet par défaut sont créés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4a64f-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="4a64f-132">**msdyn_CreateTeamMemberV1** : Cette API peut être utilisée pour créer un membre de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="4a64f-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="4a64f-133">L’enregistrement de membre de l’équipe est créé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4a64f-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="4a64f-134">**msdyn_CreateOperationSetV1** : Cette API peut être utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="4a64f-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="4a64f-135">**msdyn_PSSCreateV1** : Cette API peut être utilisée pour créer une entité.</span><span class="sxs-lookup"><span data-stu-id="4a64f-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="4a64f-136">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="4a64f-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="4a64f-137">**msdyn_PSSUpdateV1** : Cette API peut être utilisée pour mettre à jour une entité.</span><span class="sxs-lookup"><span data-stu-id="4a64f-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="4a64f-138">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4a64f-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="4a64f-139">**msdyn_PSSDeleteV1** : Cette API peut être utilisée pour supprimer une entité.</span><span class="sxs-lookup"><span data-stu-id="4a64f-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="4a64f-140">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="4a64f-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="4a64f-141">**msdyn_ExecuteOperationSetV1** : Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.</span><span class="sxs-lookup"><span data-stu-id="4a64f-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="4a64f-142">Utilisation des API de planification avec OperationSet</span><span class="sxs-lookup"><span data-stu-id="4a64f-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="4a64f-143">Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="4a64f-144">Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="4a64f-145">Opérations prises en charge</span><span class="sxs-lookup"><span data-stu-id="4a64f-145">Supported operations</span></span>

| <span data-ttu-id="4a64f-146">Entité de planification</span><span class="sxs-lookup"><span data-stu-id="4a64f-146">Scheduling entity</span></span> | <span data-ttu-id="4a64f-147">Créer</span><span class="sxs-lookup"><span data-stu-id="4a64f-147">Create</span></span> | <span data-ttu-id="4a64f-148">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="4a64f-148">Update</span></span> | <span data-ttu-id="4a64f-149">Suppr</span><span class="sxs-lookup"><span data-stu-id="4a64f-149">Delete</span></span> | <span data-ttu-id="4a64f-150">Remarques importantes</span><span class="sxs-lookup"><span data-stu-id="4a64f-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="4a64f-151">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-151">Project task</span></span> | <span data-ttu-id="4a64f-152">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-152">Yes</span></span> | <span data-ttu-id="4a64f-153">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-153">Yes</span></span> | <span data-ttu-id="4a64f-154">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-154">Yes</span></span> | <span data-ttu-id="4a64f-155">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="4a64f-155">None</span></span> |
| <span data-ttu-id="4a64f-156">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-156">Project task dependency</span></span> | <span data-ttu-id="4a64f-157">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-157">Yes</span></span> | <span data-ttu-id="4a64f-158">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-158">Yes</span></span> | | <span data-ttu-id="4a64f-159">Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4a64f-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="4a64f-160">Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="4a64f-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4a64f-161">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="4a64f-161">Resource assignment</span></span> | <span data-ttu-id="4a64f-162">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-162">Yes</span></span> | <span data-ttu-id="4a64f-163">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-163">Yes</span></span> | | <span data-ttu-id="4a64f-164">Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="4a64f-165">Les enregistrements d’attribution de ressource ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4a64f-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="4a64f-166">Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="4a64f-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4a64f-167">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-167">Project bucket</span></span> | <span data-ttu-id="4a64f-168">N/A</span><span class="sxs-lookup"><span data-stu-id="4a64f-168">N/A</span></span> | <span data-ttu-id="4a64f-169">N/A</span><span class="sxs-lookup"><span data-stu-id="4a64f-169">N/A</span></span> | <span data-ttu-id="4a64f-170">N/A</span><span class="sxs-lookup"><span data-stu-id="4a64f-170">N/A</span></span> | <span data-ttu-id="4a64f-171">Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="4a64f-172">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-172">Project team member</span></span> | <span data-ttu-id="4a64f-173">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-173">Yes</span></span> | <span data-ttu-id="4a64f-174">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-174">Yes</span></span> | <span data-ttu-id="4a64f-175">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-175">Yes</span></span> | <span data-ttu-id="4a64f-176">Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="4a64f-177">Project</span><span class="sxs-lookup"><span data-stu-id="4a64f-177">Project</span></span> | <span data-ttu-id="4a64f-178">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-178">Yes</span></span> | <span data-ttu-id="4a64f-179">Oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-179">Yes</span></span> | <span data-ttu-id="4a64f-180">N/A</span><span class="sxs-lookup"><span data-stu-id="4a64f-180">N/A</span></span> | <span data-ttu-id="4a64f-181">Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="4a64f-182">Ces API peuvent être appelées avec des objets d’entité qui incluent des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4a64f-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="4a64f-183">La propriété ID est facultative.</span><span class="sxs-lookup"><span data-stu-id="4a64f-183">The ID property is optional.</span></span> <span data-ttu-id="4a64f-184">Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="4a64f-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="4a64f-185">Si elle n’est pas fournie, le système la générera.</span><span class="sxs-lookup"><span data-stu-id="4a64f-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="4a64f-186">Champs interdits</span><span class="sxs-lookup"><span data-stu-id="4a64f-186">Restricted fields</span></span>

<span data-ttu-id="4a64f-187">Les tableaux suivants définissent les champs interdits pour **Créer** et **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="4a64f-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="4a64f-188">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-188">Project task</span></span>

| <span data-ttu-id="4a64f-189">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="4a64f-189">**Logical name**</span></span>                       | <span data-ttu-id="4a64f-190">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="4a64f-190">**Can create**</span></span> | <span data-ttu-id="4a64f-191">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="4a64f-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="4a64f-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="4a64f-193">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-193">no</span></span>             | <span data-ttu-id="4a64f-194">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-194">no</span></span>               |
| <span data-ttu-id="4a64f-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="4a64f-196">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-196">no</span></span>             | <span data-ttu-id="4a64f-197">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-197">no</span></span>               |
| <span data-ttu-id="4a64f-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="4a64f-198">msdyn_actualend</span></span>                        | <span data-ttu-id="4a64f-199">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-199">no</span></span>             | <span data-ttu-id="4a64f-200">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-200">no</span></span>               |
| <span data-ttu-id="4a64f-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="4a64f-202">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-202">no</span></span>             | <span data-ttu-id="4a64f-203">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-203">no</span></span>               |
| <span data-ttu-id="4a64f-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4a64f-205">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-205">no</span></span>             | <span data-ttu-id="4a64f-206">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-206">no</span></span>               |
| <span data-ttu-id="4a64f-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="4a64f-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="4a64f-208">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-208">no</span></span>             | <span data-ttu-id="4a64f-209">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-209">no</span></span>               |
| <span data-ttu-id="4a64f-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="4a64f-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="4a64f-211">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-211">no</span></span>             | <span data-ttu-id="4a64f-212">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-212">no</span></span>               |
| <span data-ttu-id="4a64f-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="4a64f-214">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-214">no</span></span>             | <span data-ttu-id="4a64f-215">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-215">no</span></span>               |
| <span data-ttu-id="4a64f-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4a64f-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="4a64f-217">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-217">no</span></span>             | <span data-ttu-id="4a64f-218">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-218">no</span></span>               |
| <span data-ttu-id="4a64f-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4a64f-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4a64f-220">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-220">no</span></span>             | <span data-ttu-id="4a64f-221">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-221">no</span></span>               |
| <span data-ttu-id="4a64f-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4a64f-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="4a64f-223">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-223">no</span></span>             | <span data-ttu-id="4a64f-224">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-224">no</span></span>               |
| <span data-ttu-id="4a64f-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="4a64f-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="4a64f-226">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-226">no</span></span>             | <span data-ttu-id="4a64f-227">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-227">no</span></span>               |
| <span data-ttu-id="4a64f-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="4a64f-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="4a64f-229">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-229">no</span></span>             | <span data-ttu-id="4a64f-230">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-230">no</span></span>               |
| <span data-ttu-id="4a64f-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="4a64f-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="4a64f-232">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-232">no</span></span>             | <span data-ttu-id="4a64f-233">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-233">no</span></span>               |
| <span data-ttu-id="4a64f-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="4a64f-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="4a64f-235">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-235">no</span></span>             | <span data-ttu-id="4a64f-236">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-236">no</span></span>               |
| <span data-ttu-id="4a64f-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="4a64f-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="4a64f-238">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-238">no</span></span>             | <span data-ttu-id="4a64f-239">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-239">no</span></span>               |
| <span data-ttu-id="4a64f-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="4a64f-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="4a64f-241">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-241">no</span></span>             | <span data-ttu-id="4a64f-242">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-242">no</span></span>               |
| <span data-ttu-id="4a64f-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="4a64f-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="4a64f-244">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-244">no</span></span>             | <span data-ttu-id="4a64f-245">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-245">no</span></span>               |
| <span data-ttu-id="4a64f-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="4a64f-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="4a64f-247">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-247">no</span></span>             | <span data-ttu-id="4a64f-248">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-248">no</span></span>               |
| <span data-ttu-id="4a64f-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4a64f-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="4a64f-250">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-250">no</span></span>             | <span data-ttu-id="4a64f-251">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-251">no</span></span>               |
| <span data-ttu-id="4a64f-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="4a64f-253">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-253">no</span></span>             | <span data-ttu-id="4a64f-254">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-254">no</span></span>               |
| <span data-ttu-id="4a64f-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="4a64f-256">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-256">no</span></span>             | <span data-ttu-id="4a64f-257">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-257">no</span></span>               |
| <span data-ttu-id="4a64f-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4a64f-259">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-259">no</span></span>             | <span data-ttu-id="4a64f-260">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-260">no</span></span>               |
| <span data-ttu-id="4a64f-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4a64f-262">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-262">no</span></span>             | <span data-ttu-id="4a64f-263">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-263">no</span></span>               |
| <span data-ttu-id="4a64f-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="4a64f-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="4a64f-265">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-265">no</span></span>             | <span data-ttu-id="4a64f-266">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-266">no</span></span>               |
| <span data-ttu-id="4a64f-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4a64f-267">msdyn_progress</span></span>                         | <span data-ttu-id="4a64f-268">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-268">no</span></span>             | <span data-ttu-id="4a64f-269">Non (oui pour P4W)</span><span class="sxs-lookup"><span data-stu-id="4a64f-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="4a64f-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4a64f-271">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-271">no</span></span>             | <span data-ttu-id="4a64f-272">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-272">no</span></span>               |
| <span data-ttu-id="4a64f-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4a64f-274">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-274">no</span></span>             | <span data-ttu-id="4a64f-275">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-275">no</span></span>               |
| <span data-ttu-id="4a64f-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4a64f-277">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-277">no</span></span>             | <span data-ttu-id="4a64f-278">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-278">no</span></span>               |
| <span data-ttu-id="4a64f-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4a64f-280">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-280">no</span></span>             | <span data-ttu-id="4a64f-281">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-281">no</span></span>               |
| <span data-ttu-id="4a64f-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="4a64f-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="4a64f-283">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-283">no</span></span>             | <span data-ttu-id="4a64f-284">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-284">no</span></span>               |
| <span data-ttu-id="4a64f-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4a64f-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="4a64f-286">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-286">no</span></span>             | <span data-ttu-id="4a64f-287">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-287">no</span></span>               |
| <span data-ttu-id="4a64f-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="4a64f-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="4a64f-289">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-289">no</span></span>             | <span data-ttu-id="4a64f-290">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-290">no</span></span>               |
| <span data-ttu-id="4a64f-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4a64f-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="4a64f-292">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-292">no</span></span>             | <span data-ttu-id="4a64f-293">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-293">no</span></span>               |
| <span data-ttu-id="4a64f-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="4a64f-295">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-295">no</span></span>             | <span data-ttu-id="4a64f-296">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-296">no</span></span>               |
| <span data-ttu-id="4a64f-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4a64f-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="4a64f-298">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-298">no</span></span>             | <span data-ttu-id="4a64f-299">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-299">no</span></span>               |
| <span data-ttu-id="4a64f-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4a64f-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="4a64f-301">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-301">no</span></span>             | <span data-ttu-id="4a64f-302">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-302">no</span></span>               |
| <span data-ttu-id="4a64f-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="4a64f-304">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-304">no</span></span>             | <span data-ttu-id="4a64f-305">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-305">no</span></span>               |
| <span data-ttu-id="4a64f-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4a64f-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4a64f-307">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-307">no</span></span>             | <span data-ttu-id="4a64f-308">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-308">no</span></span>               |
| <span data-ttu-id="4a64f-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4a64f-310">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-310">no</span></span>             | <span data-ttu-id="4a64f-311">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-311">no</span></span>               |
| <span data-ttu-id="4a64f-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="4a64f-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="4a64f-313">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-313">no</span></span>             | <span data-ttu-id="4a64f-314">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-314">no</span></span>               |
| <span data-ttu-id="4a64f-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="4a64f-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="4a64f-316">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-316">no</span></span>             | <span data-ttu-id="4a64f-317">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-317">no</span></span>               |
| <span data-ttu-id="4a64f-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="4a64f-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="4a64f-319">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-319">no</span></span>             | <span data-ttu-id="4a64f-320">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-320">no</span></span>               |
| <span data-ttu-id="4a64f-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4a64f-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4a64f-322">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-322">no</span></span>             | <span data-ttu-id="4a64f-323">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-323">no</span></span>               |
| <span data-ttu-id="4a64f-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="4a64f-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="4a64f-325">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-325">no</span></span>             | <span data-ttu-id="4a64f-326">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-326">no</span></span>               |
| <span data-ttu-id="4a64f-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="4a64f-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="4a64f-328">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-328">no</span></span>             | <span data-ttu-id="4a64f-329">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-329">no</span></span>               |
| <span data-ttu-id="4a64f-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="4a64f-330">msdyn_summary</span></span>                          | <span data-ttu-id="4a64f-331">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-331">no</span></span>             | <span data-ttu-id="4a64f-332">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-332">no</span></span>               |
| <span data-ttu-id="4a64f-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="4a64f-334">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-334">no</span></span>             | <span data-ttu-id="4a64f-335">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-335">no</span></span>               |
| <span data-ttu-id="4a64f-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="4a64f-337">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-337">no</span></span>             | <span data-ttu-id="4a64f-338">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="4a64f-339">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-339">Project task dependency</span></span>

| <span data-ttu-id="4a64f-340">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="4a64f-340">**Logical name**</span></span>              | <span data-ttu-id="4a64f-341">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="4a64f-341">**Can create**</span></span> | <span data-ttu-id="4a64f-342">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="4a64f-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="4a64f-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="4a64f-343">msdyn_linktype</span></span>                | <span data-ttu-id="4a64f-344">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-344">no</span></span>             | <span data-ttu-id="4a64f-345">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-345">no</span></span>           |
| <span data-ttu-id="4a64f-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="4a64f-346">msdyn_linktypename</span></span>            | <span data-ttu-id="4a64f-347">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-347">no</span></span>             | <span data-ttu-id="4a64f-348">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-348">no</span></span>           |
| <span data-ttu-id="4a64f-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="4a64f-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="4a64f-350">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-350">yes</span></span>            | <span data-ttu-id="4a64f-351">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-351">no</span></span>           |
| <span data-ttu-id="4a64f-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="4a64f-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="4a64f-353">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-353">yes</span></span>            | <span data-ttu-id="4a64f-354">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-354">no</span></span>           |
| <span data-ttu-id="4a64f-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4a64f-355">msdyn_project</span></span>                 | <span data-ttu-id="4a64f-356">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-356">yes</span></span>            | <span data-ttu-id="4a64f-357">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-357">no</span></span>           |
| <span data-ttu-id="4a64f-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="4a64f-358">msdyn_projectname</span></span>             | <span data-ttu-id="4a64f-359">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-359">yes</span></span>            | <span data-ttu-id="4a64f-360">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-360">no</span></span>           |
| <span data-ttu-id="4a64f-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="4a64f-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="4a64f-362">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-362">yes</span></span>            | <span data-ttu-id="4a64f-363">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-363">no</span></span>           |
| <span data-ttu-id="4a64f-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="4a64f-364">msdyn_successortask</span></span>           | <span data-ttu-id="4a64f-365">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-365">yes</span></span>            | <span data-ttu-id="4a64f-366">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-366">no</span></span>           |
| <span data-ttu-id="4a64f-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="4a64f-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="4a64f-368">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-368">yes</span></span>            | <span data-ttu-id="4a64f-369">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="4a64f-370">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="4a64f-370">Resource assignment</span></span>

| <span data-ttu-id="4a64f-371">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="4a64f-371">**Logical name**</span></span>             | <span data-ttu-id="4a64f-372">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="4a64f-372">**Can create**</span></span> | <span data-ttu-id="4a64f-373">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="4a64f-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="4a64f-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="4a64f-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="4a64f-375">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-375">yes</span></span>            | <span data-ttu-id="4a64f-376">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-376">no</span></span>           |
| <span data-ttu-id="4a64f-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="4a64f-378">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-378">yes</span></span>            | <span data-ttu-id="4a64f-379">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-379">no</span></span>           |
| <span data-ttu-id="4a64f-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="4a64f-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="4a64f-381">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-381">no</span></span>             | <span data-ttu-id="4a64f-382">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-382">no</span></span>           |
| <span data-ttu-id="4a64f-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="4a64f-384">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-384">no</span></span>             | <span data-ttu-id="4a64f-385">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-385">no</span></span>           |
| <span data-ttu-id="4a64f-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="4a64f-386">msdyn_committype</span></span>             | <span data-ttu-id="4a64f-387">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-387">no</span></span>             | <span data-ttu-id="4a64f-388">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-388">no</span></span>           |
| <span data-ttu-id="4a64f-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="4a64f-389">msdyn_committypename</span></span>         | <span data-ttu-id="4a64f-390">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-390">no</span></span>             | <span data-ttu-id="4a64f-391">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-391">no</span></span>           |
| <span data-ttu-id="4a64f-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4a64f-392">msdyn_effort</span></span>                 | <span data-ttu-id="4a64f-393">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-393">no</span></span>             | <span data-ttu-id="4a64f-394">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-394">no</span></span>           |
| <span data-ttu-id="4a64f-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4a64f-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="4a64f-396">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-396">no</span></span>             | <span data-ttu-id="4a64f-397">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-397">no</span></span>           |
| <span data-ttu-id="4a64f-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4a64f-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="4a64f-399">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-399">no</span></span>             | <span data-ttu-id="4a64f-400">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-400">no</span></span>           |
| <span data-ttu-id="4a64f-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4a64f-401">msdyn_finish</span></span>                 | <span data-ttu-id="4a64f-402">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-402">no</span></span>             | <span data-ttu-id="4a64f-403">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-403">no</span></span>           |
| <span data-ttu-id="4a64f-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="4a64f-405">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-405">no</span></span>             | <span data-ttu-id="4a64f-406">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-406">no</span></span>           |
| <span data-ttu-id="4a64f-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="4a64f-408">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-408">no</span></span>             | <span data-ttu-id="4a64f-409">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-409">no</span></span>           |
| <span data-ttu-id="4a64f-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="4a64f-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="4a64f-411">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-411">no</span></span>             | <span data-ttu-id="4a64f-412">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-412">no</span></span>           |
| <span data-ttu-id="4a64f-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="4a64f-414">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-414">no</span></span>             | <span data-ttu-id="4a64f-415">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-415">no</span></span>           |
| <span data-ttu-id="4a64f-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="4a64f-417">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-417">no</span></span>             | <span data-ttu-id="4a64f-418">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-418">no</span></span>           |
| <span data-ttu-id="4a64f-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="4a64f-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="4a64f-420">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-420">no</span></span>             | <span data-ttu-id="4a64f-421">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-421">no</span></span>           |
| <span data-ttu-id="4a64f-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="4a64f-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="4a64f-423">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-423">no</span></span>             | <span data-ttu-id="4a64f-424">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-424">no</span></span>           |
| <span data-ttu-id="4a64f-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="4a64f-425">msdyn_projectid</span></span>              | <span data-ttu-id="4a64f-426">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-426">yes</span></span>            | <span data-ttu-id="4a64f-427">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-427">no</span></span>           |
| <span data-ttu-id="4a64f-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-428">msdyn_projectidname</span></span>          | <span data-ttu-id="4a64f-429">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-429">no</span></span>             | <span data-ttu-id="4a64f-430">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-430">no</span></span>           |
| <span data-ttu-id="4a64f-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="4a64f-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="4a64f-432">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-432">no</span></span>             | <span data-ttu-id="4a64f-433">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-433">no</span></span>           |
| <span data-ttu-id="4a64f-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="4a64f-435">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-435">no</span></span>             | <span data-ttu-id="4a64f-436">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-436">no</span></span>           |
| <span data-ttu-id="4a64f-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4a64f-437">msdyn_start</span></span>                  | <span data-ttu-id="4a64f-438">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-438">no</span></span>             | <span data-ttu-id="4a64f-439">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-439">no</span></span>           |
| <span data-ttu-id="4a64f-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="4a64f-440">msdyn_taskid</span></span>                 | <span data-ttu-id="4a64f-441">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-441">no</span></span>             | <span data-ttu-id="4a64f-442">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-442">no</span></span>           |
| <span data-ttu-id="4a64f-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-443">msdyn_taskidname</span></span>             | <span data-ttu-id="4a64f-444">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-444">no</span></span>             | <span data-ttu-id="4a64f-445">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-445">no</span></span>           |
| <span data-ttu-id="4a64f-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="4a64f-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="4a64f-447">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-447">no</span></span>             | <span data-ttu-id="4a64f-448">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="4a64f-449">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="4a64f-449">Project team member</span></span>

| <span data-ttu-id="4a64f-450">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="4a64f-450">**Logical name**</span></span>                                 | <span data-ttu-id="4a64f-451">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="4a64f-451">**Can create**</span></span> | <span data-ttu-id="4a64f-452">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="4a64f-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="4a64f-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="4a64f-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="4a64f-454">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-454">no</span></span>             | <span data-ttu-id="4a64f-455">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-455">no</span></span>           |
| <span data-ttu-id="4a64f-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="4a64f-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="4a64f-457">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-457">no</span></span>             | <span data-ttu-id="4a64f-458">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-458">no</span></span>           |
| <span data-ttu-id="4a64f-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="4a64f-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="4a64f-460">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-460">no</span></span>             | <span data-ttu-id="4a64f-461">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-461">no</span></span>           |
| <span data-ttu-id="4a64f-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="4a64f-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="4a64f-463">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-463">no</span></span>             | <span data-ttu-id="4a64f-464">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-464">no</span></span>           |
| <span data-ttu-id="4a64f-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4a64f-465">msdyn_effort</span></span>                                     | <span data-ttu-id="4a64f-466">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-466">no</span></span>             | <span data-ttu-id="4a64f-467">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-467">no</span></span>           |
| <span data-ttu-id="4a64f-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4a64f-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="4a64f-469">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-469">no</span></span>             | <span data-ttu-id="4a64f-470">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-470">no</span></span>           |
| <span data-ttu-id="4a64f-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4a64f-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="4a64f-472">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-472">no</span></span>             | <span data-ttu-id="4a64f-473">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-473">no</span></span>           |
| <span data-ttu-id="4a64f-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4a64f-474">msdyn_finish</span></span>                                     | <span data-ttu-id="4a64f-475">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-475">no</span></span>             | <span data-ttu-id="4a64f-476">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-476">no</span></span>           |
| <span data-ttu-id="4a64f-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="4a64f-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="4a64f-478">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-478">no</span></span>             | <span data-ttu-id="4a64f-479">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-479">no</span></span>           |
| <span data-ttu-id="4a64f-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="4a64f-480">msdyn_hours</span></span>                                      | <span data-ttu-id="4a64f-481">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-481">no</span></span>             | <span data-ttu-id="4a64f-482">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-482">no</span></span>           |
| <span data-ttu-id="4a64f-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="4a64f-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="4a64f-484">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-484">no</span></span>             | <span data-ttu-id="4a64f-485">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-485">no</span></span>           |
| <span data-ttu-id="4a64f-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="4a64f-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="4a64f-487">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-487">no</span></span>             | <span data-ttu-id="4a64f-488">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-488">no</span></span>           |
| <span data-ttu-id="4a64f-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4a64f-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="4a64f-490">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-490">no</span></span>             | <span data-ttu-id="4a64f-491">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-491">no</span></span>           |
| <span data-ttu-id="4a64f-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="4a64f-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="4a64f-493">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-493">no</span></span>             | <span data-ttu-id="4a64f-494">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-494">no</span></span>           |
| <span data-ttu-id="4a64f-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="4a64f-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="4a64f-496">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-496">no</span></span>             | <span data-ttu-id="4a64f-497">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-497">no</span></span>           |
| <span data-ttu-id="4a64f-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="4a64f-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="4a64f-499">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-499">no</span></span>             | <span data-ttu-id="4a64f-500">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-500">no</span></span>           |
| <span data-ttu-id="4a64f-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4a64f-501">msdyn_start</span></span>                                      | <span data-ttu-id="4a64f-502">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-502">no</span></span>             | <span data-ttu-id="4a64f-503">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="4a64f-504">Project</span><span class="sxs-lookup"><span data-stu-id="4a64f-504">Project</span></span>

| <span data-ttu-id="4a64f-505">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="4a64f-505">**Logical name**</span></span>                       | <span data-ttu-id="4a64f-506">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="4a64f-506">**Can create**</span></span> | <span data-ttu-id="4a64f-507">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="4a64f-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="4a64f-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="4a64f-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="4a64f-509">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-509">no</span></span>             | <span data-ttu-id="4a64f-510">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-510">no</span></span>           |
| <span data-ttu-id="4a64f-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="4a64f-512">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-512">no</span></span>             | <span data-ttu-id="4a64f-513">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-513">no</span></span>           |
| <span data-ttu-id="4a64f-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="4a64f-515">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-515">no</span></span>             | <span data-ttu-id="4a64f-516">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-516">no</span></span>           |
| <span data-ttu-id="4a64f-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="4a64f-518">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-518">no</span></span>             | <span data-ttu-id="4a64f-519">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-519">no</span></span>           |
| <span data-ttu-id="4a64f-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="4a64f-521">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-521">no</span></span>             | <span data-ttu-id="4a64f-522">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-522">no</span></span>           |
| <span data-ttu-id="4a64f-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4a64f-524">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-524">no</span></span>             | <span data-ttu-id="4a64f-525">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-525">no</span></span>           |
| <span data-ttu-id="4a64f-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="4a64f-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="4a64f-527">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-527">yes</span></span>            | <span data-ttu-id="4a64f-528">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-528">no</span></span>           |
| <span data-ttu-id="4a64f-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4a64f-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="4a64f-530">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-530">yes</span></span>            | <span data-ttu-id="4a64f-531">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-531">no</span></span>           |
| <span data-ttu-id="4a64f-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4a64f-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="4a64f-533">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-533">yes</span></span>            | <span data-ttu-id="4a64f-534">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-534">no</span></span>           |
| <span data-ttu-id="4a64f-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="4a64f-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="4a64f-536">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-536">no</span></span>             | <span data-ttu-id="4a64f-537">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-537">no</span></span>           |
| <span data-ttu-id="4a64f-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4a64f-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="4a64f-539">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-539">no</span></span>             | <span data-ttu-id="4a64f-540">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-540">no</span></span>           |
| <span data-ttu-id="4a64f-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="4a64f-542">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-542">no</span></span>             | <span data-ttu-id="4a64f-543">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-543">no</span></span>           |
| <span data-ttu-id="4a64f-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="4a64f-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="4a64f-545">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-545">no</span></span>             | <span data-ttu-id="4a64f-546">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-546">no</span></span>           |
| <span data-ttu-id="4a64f-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="4a64f-548">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-548">no</span></span>             | <span data-ttu-id="4a64f-549">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-549">no</span></span>           |
| <span data-ttu-id="4a64f-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="4a64f-550">msdyn_duration</span></span>                         | <span data-ttu-id="4a64f-551">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-551">no</span></span>             | <span data-ttu-id="4a64f-552">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-552">no</span></span>           |
| <span data-ttu-id="4a64f-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4a64f-553">msdyn_effort</span></span>                           | <span data-ttu-id="4a64f-554">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-554">no</span></span>             | <span data-ttu-id="4a64f-555">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-555">no</span></span>           |
| <span data-ttu-id="4a64f-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4a64f-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4a64f-557">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-557">no</span></span>             | <span data-ttu-id="4a64f-558">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-558">no</span></span>           |
| <span data-ttu-id="4a64f-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4a64f-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="4a64f-560">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-560">no</span></span>             | <span data-ttu-id="4a64f-561">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-561">no</span></span>           |
| <span data-ttu-id="4a64f-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4a64f-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="4a64f-563">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-563">no</span></span>             | <span data-ttu-id="4a64f-564">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-564">no</span></span>           |
| <span data-ttu-id="4a64f-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4a64f-565">msdyn_finish</span></span>                           | <span data-ttu-id="4a64f-566">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-566">yes</span></span>            | <span data-ttu-id="4a64f-567">oui</span><span class="sxs-lookup"><span data-stu-id="4a64f-567">yes</span></span>          |
| <span data-ttu-id="4a64f-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="4a64f-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="4a64f-569">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-569">no</span></span>             | <span data-ttu-id="4a64f-570">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-570">no</span></span>           |
| <span data-ttu-id="4a64f-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="4a64f-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="4a64f-572">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-572">no</span></span>             | <span data-ttu-id="4a64f-573">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-573">no</span></span>           |
| <span data-ttu-id="4a64f-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="4a64f-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="4a64f-575">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-575">no</span></span>             | <span data-ttu-id="4a64f-576">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-576">no</span></span>           |
| <span data-ttu-id="4a64f-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="4a64f-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="4a64f-578">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-578">no</span></span>             | <span data-ttu-id="4a64f-579">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-579">no</span></span>           |
| <span data-ttu-id="4a64f-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="4a64f-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="4a64f-581">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-581">no</span></span>             | <span data-ttu-id="4a64f-582">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-582">no</span></span>           |
| <span data-ttu-id="4a64f-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="4a64f-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="4a64f-584">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-584">no</span></span>             | <span data-ttu-id="4a64f-585">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-585">no</span></span>           |
| <span data-ttu-id="4a64f-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="4a64f-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="4a64f-587">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-587">no</span></span>             | <span data-ttu-id="4a64f-588">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-588">no</span></span>           |
| <span data-ttu-id="4a64f-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="4a64f-590">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-590">no</span></span>             | <span data-ttu-id="4a64f-591">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-591">no</span></span>           |
| <span data-ttu-id="4a64f-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="4a64f-593">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-593">no</span></span>             | <span data-ttu-id="4a64f-594">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-594">no</span></span>           |
| <span data-ttu-id="4a64f-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="4a64f-596">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-596">no</span></span>             | <span data-ttu-id="4a64f-597">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-597">no</span></span>           |
| <span data-ttu-id="4a64f-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4a64f-599">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-599">no</span></span>             | <span data-ttu-id="4a64f-600">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-600">no</span></span>           |
| <span data-ttu-id="4a64f-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4a64f-602">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-602">no</span></span>             | <span data-ttu-id="4a64f-603">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-603">no</span></span>           |
| <span data-ttu-id="4a64f-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4a64f-604">msdyn_progress</span></span>                         | <span data-ttu-id="4a64f-605">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-605">no</span></span>             | <span data-ttu-id="4a64f-606">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-606">no</span></span>           |
| <span data-ttu-id="4a64f-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4a64f-608">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-608">no</span></span>             | <span data-ttu-id="4a64f-609">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-609">no</span></span>           |
| <span data-ttu-id="4a64f-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4a64f-611">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-611">no</span></span>             | <span data-ttu-id="4a64f-612">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-612">no</span></span>           |
| <span data-ttu-id="4a64f-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4a64f-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4a64f-614">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-614">no</span></span>             | <span data-ttu-id="4a64f-615">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-615">no</span></span>           |
| <span data-ttu-id="4a64f-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4a64f-617">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-617">no</span></span>             | <span data-ttu-id="4a64f-618">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-618">no</span></span>           |
| <span data-ttu-id="4a64f-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="4a64f-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="4a64f-620">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-620">no</span></span>             | <span data-ttu-id="4a64f-621">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-621">no</span></span>           |
| <span data-ttu-id="4a64f-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="4a64f-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="4a64f-623">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-623">no</span></span>             | <span data-ttu-id="4a64f-624">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-624">no</span></span>           |
| <span data-ttu-id="4a64f-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4a64f-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="4a64f-626">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-626">no</span></span>             | <span data-ttu-id="4a64f-627">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-627">no</span></span>           |
| <span data-ttu-id="4a64f-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="4a64f-629">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-629">no</span></span>             | <span data-ttu-id="4a64f-630">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-630">no</span></span>           |
| <span data-ttu-id="4a64f-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4a64f-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4a64f-632">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-632">no</span></span>             | <span data-ttu-id="4a64f-633">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-633">no</span></span>           |
| <span data-ttu-id="4a64f-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4a64f-635">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-635">no</span></span>             | <span data-ttu-id="4a64f-636">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-636">no</span></span>           |
| <span data-ttu-id="4a64f-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="4a64f-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="4a64f-638">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-638">no</span></span>             | <span data-ttu-id="4a64f-639">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-639">no</span></span>           |
| <span data-ttu-id="4a64f-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="4a64f-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="4a64f-641">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-641">no</span></span>             | <span data-ttu-id="4a64f-642">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-642">no</span></span>           |
| <span data-ttu-id="4a64f-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4a64f-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4a64f-644">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-644">no</span></span>             | <span data-ttu-id="4a64f-645">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-645">no</span></span>           |
| <span data-ttu-id="4a64f-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="4a64f-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="4a64f-647">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-647">no</span></span>             | <span data-ttu-id="4a64f-648">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-648">no</span></span>           |
| <span data-ttu-id="4a64f-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="4a64f-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="4a64f-650">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-650">no</span></span>             | <span data-ttu-id="4a64f-651">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-651">no</span></span>           |
| <span data-ttu-id="4a64f-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="4a64f-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="4a64f-653">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-653">no</span></span>             | <span data-ttu-id="4a64f-654">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-654">no</span></span>           |
| <span data-ttu-id="4a64f-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="4a64f-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="4a64f-656">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-656">no</span></span>             | <span data-ttu-id="4a64f-657">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-657">no</span></span>           |
| <span data-ttu-id="4a64f-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="4a64f-659">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-659">no</span></span>             | <span data-ttu-id="4a64f-660">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-660">no</span></span>           |
| <span data-ttu-id="4a64f-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="4a64f-662">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-662">no</span></span>             | <span data-ttu-id="4a64f-663">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-663">no</span></span>           |
| <span data-ttu-id="4a64f-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="4a64f-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="4a64f-665">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-665">no</span></span>             | <span data-ttu-id="4a64f-666">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-666">no</span></span>           |
| <span data-ttu-id="4a64f-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4a64f-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="4a64f-668">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-668">no</span></span>             | <span data-ttu-id="4a64f-669">non</span><span class="sxs-lookup"><span data-stu-id="4a64f-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="4a64f-670">Limitations et problèmes connus</span><span class="sxs-lookup"><span data-stu-id="4a64f-670">Limitations and known issues</span></span>
<span data-ttu-id="4a64f-671">Voici une liste des limitations et des problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="4a64f-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="4a64f-672">Les API de planification ne peuvent être utilisées que par les **utilisateurs disposant d’une licence Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="4a64f-673">Elles ne peuvent pas être utilisées par :</span><span class="sxs-lookup"><span data-stu-id="4a64f-673">They can't be used by:</span></span>
    - <span data-ttu-id="4a64f-674">Utilisateurs de l'application</span><span class="sxs-lookup"><span data-stu-id="4a64f-674">Application users</span></span>
    - <span data-ttu-id="4a64f-675">Utilisateurs du système</span><span class="sxs-lookup"><span data-stu-id="4a64f-675">System users</span></span>
    - <span data-ttu-id="4a64f-676">Utilisateurs de l’intégration</span><span class="sxs-lookup"><span data-stu-id="4a64f-676">Integration users</span></span>
    - <span data-ttu-id="4a64f-677">Autres utilisateurs ne disposant pas de la licence requise</span><span class="sxs-lookup"><span data-stu-id="4a64f-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="4a64f-678">Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.</span><span class="sxs-lookup"><span data-stu-id="4a64f-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="4a64f-679">Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.</span><span class="sxs-lookup"><span data-stu-id="4a64f-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="4a64f-680">Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.</span><span class="sxs-lookup"><span data-stu-id="4a64f-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="4a64f-681">Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="4a64f-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="4a64f-682">Les API de planification sont disponibles en version préliminaire publique.</span><span class="sxs-lookup"><span data-stu-id="4a64f-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="4a64f-683">L’utilisation de ces API dans un environnement de production n’est pas prise en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4a64f-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="4a64f-684">Limites des projets et des tâches</span><span class="sxs-lookup"><span data-stu-id="4a64f-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="4a64f-685">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="4a64f-685">Error handling</span></span>

   - <span data-ttu-id="4a64f-686">Pour consulter les erreurs générées par les ensembles d’opérations, accédez à **Paramètres** \> **Planifier l’intégration** \> **Ensembles d’opérations**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="4a64f-687">Pour consulter les erreurs générées par le service de planification de projet, accédez à **Paramètres** \> **Planifier l’intégration** \> **Journaux des erreurs de PSS**.</span><span class="sxs-lookup"><span data-stu-id="4a64f-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="4a64f-688">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="4a64f-688">Sample scenario</span></span>

<span data-ttu-id="4a64f-689">Dans ce scénario, vous allez créer un projet, un membre de l’équipe, quatre tâches et deux affectations de ressources.</span><span class="sxs-lookup"><span data-stu-id="4a64f-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="4a64f-690">Ensuite, vous allez mettre à jour une tâche, mettre à jour le projet, supprimer une tâche, supprimer une affectation de ressource et créer une dépendance de tâche.</span><span class="sxs-lookup"><span data-stu-id="4a64f-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="4a64f-691">Exemples supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4a64f-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
