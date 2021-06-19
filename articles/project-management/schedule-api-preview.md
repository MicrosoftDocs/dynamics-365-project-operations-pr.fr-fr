---
title: Utiliser les API de planification pour effectuer des opérations avec des entités de planification
description: Cette rubrique fournit des informations et des exemples d’utilisation des API de planification.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116794"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="fabba-103">Utiliser les API de planification pour effectuer des opérations avec des entités de planification</span><span class="sxs-lookup"><span data-stu-id="fabba-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="fabba-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="fabba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="fabba-105">Certaines ou toutes les fonctionnalités mentionnées dans cette rubrique sont disponibles dans le cadre d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="fabba-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="fabba-106">Le contenu et les fonctionnalités sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="fabba-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="fabba-107">Entités de planification</span><span class="sxs-lookup"><span data-stu-id="fabba-107">Scheduling entities</span></span>

<span data-ttu-id="fabba-108">Les API de planification offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="fabba-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="fabba-109">Ces entités sont gérées via le moteur de planification de l’application Project pour le Web.</span><span class="sxs-lookup"><span data-stu-id="fabba-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="fabba-110">Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fabba-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="fabba-111">Le tableau suivant fournit une liste complète des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="fabba-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="fabba-112">Nom de l’entité</span><span class="sxs-lookup"><span data-stu-id="fabba-112">Entity name</span></span>  | <span data-ttu-id="fabba-113">Nom logique de l’entité</span><span class="sxs-lookup"><span data-stu-id="fabba-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="fabba-114">Project</span><span class="sxs-lookup"><span data-stu-id="fabba-114">Project</span></span> | <span data-ttu-id="fabba-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="fabba-115">msdyn_project</span></span> |
| <span data-ttu-id="fabba-116">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-116">Project Task</span></span>  | <span data-ttu-id="fabba-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="fabba-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="fabba-118">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-118">Project Task Dependency</span></span>  | <span data-ttu-id="fabba-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="fabba-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="fabba-120">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="fabba-120">Resource Assignment</span></span> | <span data-ttu-id="fabba-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="fabba-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="fabba-122">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-122">Project Bucket</span></span>  | <span data-ttu-id="fabba-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="fabba-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="fabba-124">Membre de l’équipe du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-124">Project Team Member</span></span> | <span data-ttu-id="fabba-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="fabba-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="fabba-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="fabba-126">OperationSet</span></span>

<span data-ttu-id="fabba-127">OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="fabba-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="fabba-128">API de planification</span><span class="sxs-lookup"><span data-stu-id="fabba-128">Schedule APIs</span></span>

<span data-ttu-id="fabba-129">Voici une liste des API de planification actuelles.</span><span class="sxs-lookup"><span data-stu-id="fabba-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="fabba-130">**msdyn_CreateProjectV1** : Cette API peut être utilisée pour créer un projet.</span><span class="sxs-lookup"><span data-stu-id="fabba-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="fabba-131">Le projet et le compartiment de projet par défaut sont créés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fabba-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="fabba-132">**msdyn_CreateTeamMemberV1** : Cette API peut être utilisée pour créer un membre de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="fabba-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="fabba-133">L’enregistrement de membre de l’équipe est créé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fabba-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="fabba-134">**msdyn_CreateOperationSetV1** : Cette API peut être utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="fabba-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="fabba-135">**msdyn_PSSCreateV1** : Cette API peut être utilisée pour créer une entité.</span><span class="sxs-lookup"><span data-stu-id="fabba-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="fabba-136">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="fabba-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="fabba-137">**msdyn_PSSUpdateV1** : Cette API peut être utilisée pour mettre à jour une entité.</span><span class="sxs-lookup"><span data-stu-id="fabba-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="fabba-138">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fabba-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="fabba-139">**msdyn_PSSDeleteV1** : Cette API peut être utilisée pour supprimer une entité.</span><span class="sxs-lookup"><span data-stu-id="fabba-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="fabba-140">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="fabba-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="fabba-141">**msdyn_ExecuteOperationSetV1** : Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.</span><span class="sxs-lookup"><span data-stu-id="fabba-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="fabba-142">Utilisation des API de planification avec OperationSet</span><span class="sxs-lookup"><span data-stu-id="fabba-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="fabba-143">Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="fabba-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="fabba-144">Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="fabba-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="fabba-145">Opérations prises en charge</span><span class="sxs-lookup"><span data-stu-id="fabba-145">Supported operations</span></span>

| <span data-ttu-id="fabba-146">Entité de planification</span><span class="sxs-lookup"><span data-stu-id="fabba-146">Scheduling entity</span></span> | <span data-ttu-id="fabba-147">Créer</span><span class="sxs-lookup"><span data-stu-id="fabba-147">Create</span></span> | <span data-ttu-id="fabba-148">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="fabba-148">Update</span></span> | <span data-ttu-id="fabba-149">Suppr</span><span class="sxs-lookup"><span data-stu-id="fabba-149">Delete</span></span> | <span data-ttu-id="fabba-150">Remarques importantes</span><span class="sxs-lookup"><span data-stu-id="fabba-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="fabba-151">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-151">Project task</span></span> | <span data-ttu-id="fabba-152">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-152">Yes</span></span> | <span data-ttu-id="fabba-153">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-153">Yes</span></span> | <span data-ttu-id="fabba-154">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-154">Yes</span></span> | <span data-ttu-id="fabba-155">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="fabba-155">None</span></span> |
| <span data-ttu-id="fabba-156">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-156">Project task dependency</span></span> | <span data-ttu-id="fabba-157">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-157">Yes</span></span> | <span data-ttu-id="fabba-158">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-158">Yes</span></span> | | <span data-ttu-id="fabba-159">Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fabba-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="fabba-160">Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="fabba-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="fabba-161">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="fabba-161">Resource assignment</span></span> | <span data-ttu-id="fabba-162">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-162">Yes</span></span> | <span data-ttu-id="fabba-163">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-163">Yes</span></span> | | <span data-ttu-id="fabba-164">Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="fabba-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="fabba-165">Les enregistrements d’attribution de ressource ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fabba-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="fabba-166">Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="fabba-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="fabba-167">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-167">Project bucket</span></span> | <span data-ttu-id="fabba-168">N/A</span><span class="sxs-lookup"><span data-stu-id="fabba-168">N/A</span></span> | <span data-ttu-id="fabba-169">N/A</span><span class="sxs-lookup"><span data-stu-id="fabba-169">N/A</span></span> | <span data-ttu-id="fabba-170">N/A</span><span class="sxs-lookup"><span data-stu-id="fabba-170">N/A</span></span> | <span data-ttu-id="fabba-171">Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="fabba-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="fabba-172">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="fabba-172">Project team member</span></span> | <span data-ttu-id="fabba-173">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-173">Yes</span></span> | <span data-ttu-id="fabba-174">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-174">Yes</span></span> | <span data-ttu-id="fabba-175">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-175">Yes</span></span> | <span data-ttu-id="fabba-176">Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="fabba-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="fabba-177">Project</span><span class="sxs-lookup"><span data-stu-id="fabba-177">Project</span></span> | <span data-ttu-id="fabba-178">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-178">Yes</span></span> | <span data-ttu-id="fabba-179">Oui</span><span class="sxs-lookup"><span data-stu-id="fabba-179">Yes</span></span> | <span data-ttu-id="fabba-180">N/A</span><span class="sxs-lookup"><span data-stu-id="fabba-180">N/A</span></span> | <span data-ttu-id="fabba-181">Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**.</span><span class="sxs-lookup"><span data-stu-id="fabba-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="fabba-182">Ces API peuvent être appelées avec des objets d’entité qui incluent des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="fabba-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="fabba-183">La propriété ID est facultative.</span><span class="sxs-lookup"><span data-stu-id="fabba-183">The ID property is optional.</span></span> <span data-ttu-id="fabba-184">Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="fabba-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="fabba-185">Si elle n’est pas fournie, le système la générera.</span><span class="sxs-lookup"><span data-stu-id="fabba-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="fabba-186">Champs interdits</span><span class="sxs-lookup"><span data-stu-id="fabba-186">Restricted fields</span></span>

<span data-ttu-id="fabba-187">Les tableaux suivants définissent les champs interdits pour **Créer** et **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="fabba-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="fabba-188">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-188">Project task</span></span>

| <span data-ttu-id="fabba-189">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="fabba-189">**Logical name**</span></span>                       | <span data-ttu-id="fabba-190">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="fabba-190">**Can create**</span></span> | <span data-ttu-id="fabba-191">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="fabba-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="fabba-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="fabba-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="fabba-193">non</span><span class="sxs-lookup"><span data-stu-id="fabba-193">no</span></span>             | <span data-ttu-id="fabba-194">non</span><span class="sxs-lookup"><span data-stu-id="fabba-194">no</span></span>               |
| <span data-ttu-id="fabba-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="fabba-196">non</span><span class="sxs-lookup"><span data-stu-id="fabba-196">no</span></span>             | <span data-ttu-id="fabba-197">non</span><span class="sxs-lookup"><span data-stu-id="fabba-197">no</span></span>               |
| <span data-ttu-id="fabba-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="fabba-198">msdyn_actualend</span></span>                        | <span data-ttu-id="fabba-199">non</span><span class="sxs-lookup"><span data-stu-id="fabba-199">no</span></span>             | <span data-ttu-id="fabba-200">non</span><span class="sxs-lookup"><span data-stu-id="fabba-200">no</span></span>               |
| <span data-ttu-id="fabba-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="fabba-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="fabba-202">non</span><span class="sxs-lookup"><span data-stu-id="fabba-202">no</span></span>             | <span data-ttu-id="fabba-203">non</span><span class="sxs-lookup"><span data-stu-id="fabba-203">no</span></span>               |
| <span data-ttu-id="fabba-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="fabba-205">non</span><span class="sxs-lookup"><span data-stu-id="fabba-205">no</span></span>             | <span data-ttu-id="fabba-206">non</span><span class="sxs-lookup"><span data-stu-id="fabba-206">no</span></span>               |
| <span data-ttu-id="fabba-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="fabba-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="fabba-208">non</span><span class="sxs-lookup"><span data-stu-id="fabba-208">no</span></span>             | <span data-ttu-id="fabba-209">non</span><span class="sxs-lookup"><span data-stu-id="fabba-209">no</span></span>               |
| <span data-ttu-id="fabba-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="fabba-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="fabba-211">non</span><span class="sxs-lookup"><span data-stu-id="fabba-211">no</span></span>             | <span data-ttu-id="fabba-212">non</span><span class="sxs-lookup"><span data-stu-id="fabba-212">no</span></span>               |
| <span data-ttu-id="fabba-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="fabba-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="fabba-214">non</span><span class="sxs-lookup"><span data-stu-id="fabba-214">no</span></span>             | <span data-ttu-id="fabba-215">non</span><span class="sxs-lookup"><span data-stu-id="fabba-215">no</span></span>               |
| <span data-ttu-id="fabba-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="fabba-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="fabba-217">non</span><span class="sxs-lookup"><span data-stu-id="fabba-217">no</span></span>             | <span data-ttu-id="fabba-218">non</span><span class="sxs-lookup"><span data-stu-id="fabba-218">no</span></span>               |
| <span data-ttu-id="fabba-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fabba-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="fabba-220">non</span><span class="sxs-lookup"><span data-stu-id="fabba-220">no</span></span>             | <span data-ttu-id="fabba-221">non</span><span class="sxs-lookup"><span data-stu-id="fabba-221">no</span></span>               |
| <span data-ttu-id="fabba-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fabba-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="fabba-223">non</span><span class="sxs-lookup"><span data-stu-id="fabba-223">no</span></span>             | <span data-ttu-id="fabba-224">non</span><span class="sxs-lookup"><span data-stu-id="fabba-224">no</span></span>               |
| <span data-ttu-id="fabba-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="fabba-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="fabba-226">non</span><span class="sxs-lookup"><span data-stu-id="fabba-226">no</span></span>             | <span data-ttu-id="fabba-227">non</span><span class="sxs-lookup"><span data-stu-id="fabba-227">no</span></span>               |
| <span data-ttu-id="fabba-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="fabba-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="fabba-229">non</span><span class="sxs-lookup"><span data-stu-id="fabba-229">no</span></span>             | <span data-ttu-id="fabba-230">non</span><span class="sxs-lookup"><span data-stu-id="fabba-230">no</span></span>               |
| <span data-ttu-id="fabba-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="fabba-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="fabba-232">non</span><span class="sxs-lookup"><span data-stu-id="fabba-232">no</span></span>             | <span data-ttu-id="fabba-233">non</span><span class="sxs-lookup"><span data-stu-id="fabba-233">no</span></span>               |
| <span data-ttu-id="fabba-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="fabba-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="fabba-235">non</span><span class="sxs-lookup"><span data-stu-id="fabba-235">no</span></span>             | <span data-ttu-id="fabba-236">non</span><span class="sxs-lookup"><span data-stu-id="fabba-236">no</span></span>               |
| <span data-ttu-id="fabba-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="fabba-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="fabba-238">non</span><span class="sxs-lookup"><span data-stu-id="fabba-238">no</span></span>             | <span data-ttu-id="fabba-239">non</span><span class="sxs-lookup"><span data-stu-id="fabba-239">no</span></span>               |
| <span data-ttu-id="fabba-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="fabba-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="fabba-241">non</span><span class="sxs-lookup"><span data-stu-id="fabba-241">no</span></span>             | <span data-ttu-id="fabba-242">non</span><span class="sxs-lookup"><span data-stu-id="fabba-242">no</span></span>               |
| <span data-ttu-id="fabba-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="fabba-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="fabba-244">non</span><span class="sxs-lookup"><span data-stu-id="fabba-244">no</span></span>             | <span data-ttu-id="fabba-245">non</span><span class="sxs-lookup"><span data-stu-id="fabba-245">no</span></span>               |
| <span data-ttu-id="fabba-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="fabba-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="fabba-247">non</span><span class="sxs-lookup"><span data-stu-id="fabba-247">no</span></span>             | <span data-ttu-id="fabba-248">non</span><span class="sxs-lookup"><span data-stu-id="fabba-248">no</span></span>               |
| <span data-ttu-id="fabba-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="fabba-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="fabba-250">non</span><span class="sxs-lookup"><span data-stu-id="fabba-250">no</span></span>             | <span data-ttu-id="fabba-251">non</span><span class="sxs-lookup"><span data-stu-id="fabba-251">no</span></span>               |
| <span data-ttu-id="fabba-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="fabba-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="fabba-253">non</span><span class="sxs-lookup"><span data-stu-id="fabba-253">no</span></span>             | <span data-ttu-id="fabba-254">non</span><span class="sxs-lookup"><span data-stu-id="fabba-254">no</span></span>               |
| <span data-ttu-id="fabba-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="fabba-256">non</span><span class="sxs-lookup"><span data-stu-id="fabba-256">no</span></span>             | <span data-ttu-id="fabba-257">non</span><span class="sxs-lookup"><span data-stu-id="fabba-257">no</span></span>               |
| <span data-ttu-id="fabba-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fabba-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="fabba-259">non</span><span class="sxs-lookup"><span data-stu-id="fabba-259">no</span></span>             | <span data-ttu-id="fabba-260">non</span><span class="sxs-lookup"><span data-stu-id="fabba-260">no</span></span>               |
| <span data-ttu-id="fabba-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="fabba-262">non</span><span class="sxs-lookup"><span data-stu-id="fabba-262">no</span></span>             | <span data-ttu-id="fabba-263">non</span><span class="sxs-lookup"><span data-stu-id="fabba-263">no</span></span>               |
| <span data-ttu-id="fabba-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="fabba-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="fabba-265">non</span><span class="sxs-lookup"><span data-stu-id="fabba-265">no</span></span>             | <span data-ttu-id="fabba-266">non</span><span class="sxs-lookup"><span data-stu-id="fabba-266">no</span></span>               |
| <span data-ttu-id="fabba-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="fabba-267">msdyn_progress</span></span>                         | <span data-ttu-id="fabba-268">non</span><span class="sxs-lookup"><span data-stu-id="fabba-268">no</span></span>             | <span data-ttu-id="fabba-269">Non (oui pour P4W)</span><span class="sxs-lookup"><span data-stu-id="fabba-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="fabba-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="fabba-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="fabba-271">non</span><span class="sxs-lookup"><span data-stu-id="fabba-271">no</span></span>             | <span data-ttu-id="fabba-272">non</span><span class="sxs-lookup"><span data-stu-id="fabba-272">no</span></span>               |
| <span data-ttu-id="fabba-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="fabba-274">non</span><span class="sxs-lookup"><span data-stu-id="fabba-274">no</span></span>             | <span data-ttu-id="fabba-275">non</span><span class="sxs-lookup"><span data-stu-id="fabba-275">no</span></span>               |
| <span data-ttu-id="fabba-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="fabba-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="fabba-277">non</span><span class="sxs-lookup"><span data-stu-id="fabba-277">no</span></span>             | <span data-ttu-id="fabba-278">non</span><span class="sxs-lookup"><span data-stu-id="fabba-278">no</span></span>               |
| <span data-ttu-id="fabba-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="fabba-280">non</span><span class="sxs-lookup"><span data-stu-id="fabba-280">no</span></span>             | <span data-ttu-id="fabba-281">non</span><span class="sxs-lookup"><span data-stu-id="fabba-281">no</span></span>               |
| <span data-ttu-id="fabba-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="fabba-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="fabba-283">non</span><span class="sxs-lookup"><span data-stu-id="fabba-283">no</span></span>             | <span data-ttu-id="fabba-284">non</span><span class="sxs-lookup"><span data-stu-id="fabba-284">no</span></span>               |
| <span data-ttu-id="fabba-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="fabba-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="fabba-286">non</span><span class="sxs-lookup"><span data-stu-id="fabba-286">no</span></span>             | <span data-ttu-id="fabba-287">non</span><span class="sxs-lookup"><span data-stu-id="fabba-287">no</span></span>               |
| <span data-ttu-id="fabba-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="fabba-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="fabba-289">non</span><span class="sxs-lookup"><span data-stu-id="fabba-289">no</span></span>             | <span data-ttu-id="fabba-290">non</span><span class="sxs-lookup"><span data-stu-id="fabba-290">no</span></span>               |
| <span data-ttu-id="fabba-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="fabba-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="fabba-292">non</span><span class="sxs-lookup"><span data-stu-id="fabba-292">no</span></span>             | <span data-ttu-id="fabba-293">non</span><span class="sxs-lookup"><span data-stu-id="fabba-293">no</span></span>               |
| <span data-ttu-id="fabba-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="fabba-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="fabba-295">non</span><span class="sxs-lookup"><span data-stu-id="fabba-295">no</span></span>             | <span data-ttu-id="fabba-296">non</span><span class="sxs-lookup"><span data-stu-id="fabba-296">no</span></span>               |
| <span data-ttu-id="fabba-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="fabba-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="fabba-298">non</span><span class="sxs-lookup"><span data-stu-id="fabba-298">no</span></span>             | <span data-ttu-id="fabba-299">non</span><span class="sxs-lookup"><span data-stu-id="fabba-299">no</span></span>               |
| <span data-ttu-id="fabba-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fabba-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="fabba-301">non</span><span class="sxs-lookup"><span data-stu-id="fabba-301">no</span></span>             | <span data-ttu-id="fabba-302">non</span><span class="sxs-lookup"><span data-stu-id="fabba-302">no</span></span>               |
| <span data-ttu-id="fabba-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="fabba-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="fabba-304">non</span><span class="sxs-lookup"><span data-stu-id="fabba-304">no</span></span>             | <span data-ttu-id="fabba-305">non</span><span class="sxs-lookup"><span data-stu-id="fabba-305">no</span></span>               |
| <span data-ttu-id="fabba-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="fabba-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="fabba-307">non</span><span class="sxs-lookup"><span data-stu-id="fabba-307">no</span></span>             | <span data-ttu-id="fabba-308">non</span><span class="sxs-lookup"><span data-stu-id="fabba-308">no</span></span>               |
| <span data-ttu-id="fabba-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="fabba-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="fabba-310">non</span><span class="sxs-lookup"><span data-stu-id="fabba-310">no</span></span>             | <span data-ttu-id="fabba-311">non</span><span class="sxs-lookup"><span data-stu-id="fabba-311">no</span></span>               |
| <span data-ttu-id="fabba-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="fabba-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="fabba-313">non</span><span class="sxs-lookup"><span data-stu-id="fabba-313">no</span></span>             | <span data-ttu-id="fabba-314">non</span><span class="sxs-lookup"><span data-stu-id="fabba-314">no</span></span>               |
| <span data-ttu-id="fabba-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="fabba-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="fabba-316">non</span><span class="sxs-lookup"><span data-stu-id="fabba-316">no</span></span>             | <span data-ttu-id="fabba-317">non</span><span class="sxs-lookup"><span data-stu-id="fabba-317">no</span></span>               |
| <span data-ttu-id="fabba-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="fabba-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="fabba-319">non</span><span class="sxs-lookup"><span data-stu-id="fabba-319">no</span></span>             | <span data-ttu-id="fabba-320">non</span><span class="sxs-lookup"><span data-stu-id="fabba-320">no</span></span>               |
| <span data-ttu-id="fabba-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="fabba-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="fabba-322">non</span><span class="sxs-lookup"><span data-stu-id="fabba-322">no</span></span>             | <span data-ttu-id="fabba-323">non</span><span class="sxs-lookup"><span data-stu-id="fabba-323">no</span></span>               |
| <span data-ttu-id="fabba-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="fabba-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="fabba-325">non</span><span class="sxs-lookup"><span data-stu-id="fabba-325">no</span></span>             | <span data-ttu-id="fabba-326">non</span><span class="sxs-lookup"><span data-stu-id="fabba-326">no</span></span>               |
| <span data-ttu-id="fabba-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="fabba-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="fabba-328">non</span><span class="sxs-lookup"><span data-stu-id="fabba-328">no</span></span>             | <span data-ttu-id="fabba-329">non</span><span class="sxs-lookup"><span data-stu-id="fabba-329">no</span></span>               |
| <span data-ttu-id="fabba-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="fabba-330">msdyn_summary</span></span>                          | <span data-ttu-id="fabba-331">non</span><span class="sxs-lookup"><span data-stu-id="fabba-331">no</span></span>             | <span data-ttu-id="fabba-332">non</span><span class="sxs-lookup"><span data-stu-id="fabba-332">no</span></span>               |
| <span data-ttu-id="fabba-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="fabba-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="fabba-334">non</span><span class="sxs-lookup"><span data-stu-id="fabba-334">no</span></span>             | <span data-ttu-id="fabba-335">non</span><span class="sxs-lookup"><span data-stu-id="fabba-335">no</span></span>               |
| <span data-ttu-id="fabba-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="fabba-337">non</span><span class="sxs-lookup"><span data-stu-id="fabba-337">no</span></span>             | <span data-ttu-id="fabba-338">non</span><span class="sxs-lookup"><span data-stu-id="fabba-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="fabba-339">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="fabba-339">Project task dependency</span></span>

| <span data-ttu-id="fabba-340">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="fabba-340">**Logical name**</span></span>              | <span data-ttu-id="fabba-341">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="fabba-341">**Can create**</span></span> | <span data-ttu-id="fabba-342">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="fabba-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="fabba-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="fabba-343">msdyn_linktype</span></span>                | <span data-ttu-id="fabba-344">non</span><span class="sxs-lookup"><span data-stu-id="fabba-344">no</span></span>             | <span data-ttu-id="fabba-345">non</span><span class="sxs-lookup"><span data-stu-id="fabba-345">no</span></span>           |
| <span data-ttu-id="fabba-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="fabba-346">msdyn_linktypename</span></span>            | <span data-ttu-id="fabba-347">non</span><span class="sxs-lookup"><span data-stu-id="fabba-347">no</span></span>             | <span data-ttu-id="fabba-348">non</span><span class="sxs-lookup"><span data-stu-id="fabba-348">no</span></span>           |
| <span data-ttu-id="fabba-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="fabba-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="fabba-350">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-350">yes</span></span>            | <span data-ttu-id="fabba-351">non</span><span class="sxs-lookup"><span data-stu-id="fabba-351">no</span></span>           |
| <span data-ttu-id="fabba-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="fabba-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="fabba-353">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-353">yes</span></span>            | <span data-ttu-id="fabba-354">non</span><span class="sxs-lookup"><span data-stu-id="fabba-354">no</span></span>           |
| <span data-ttu-id="fabba-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="fabba-355">msdyn_project</span></span>                 | <span data-ttu-id="fabba-356">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-356">yes</span></span>            | <span data-ttu-id="fabba-357">non</span><span class="sxs-lookup"><span data-stu-id="fabba-357">no</span></span>           |
| <span data-ttu-id="fabba-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="fabba-358">msdyn_projectname</span></span>             | <span data-ttu-id="fabba-359">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-359">yes</span></span>            | <span data-ttu-id="fabba-360">non</span><span class="sxs-lookup"><span data-stu-id="fabba-360">no</span></span>           |
| <span data-ttu-id="fabba-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="fabba-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="fabba-362">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-362">yes</span></span>            | <span data-ttu-id="fabba-363">non</span><span class="sxs-lookup"><span data-stu-id="fabba-363">no</span></span>           |
| <span data-ttu-id="fabba-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="fabba-364">msdyn_successortask</span></span>           | <span data-ttu-id="fabba-365">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-365">yes</span></span>            | <span data-ttu-id="fabba-366">non</span><span class="sxs-lookup"><span data-stu-id="fabba-366">no</span></span>           |
| <span data-ttu-id="fabba-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="fabba-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="fabba-368">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-368">yes</span></span>            | <span data-ttu-id="fabba-369">non</span><span class="sxs-lookup"><span data-stu-id="fabba-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="fabba-370">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="fabba-370">Resource assignment</span></span>

| <span data-ttu-id="fabba-371">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="fabba-371">**Logical name**</span></span>             | <span data-ttu-id="fabba-372">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="fabba-372">**Can create**</span></span> | <span data-ttu-id="fabba-373">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="fabba-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="fabba-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="fabba-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="fabba-375">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-375">yes</span></span>            | <span data-ttu-id="fabba-376">non</span><span class="sxs-lookup"><span data-stu-id="fabba-376">no</span></span>           |
| <span data-ttu-id="fabba-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="fabba-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="fabba-378">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-378">yes</span></span>            | <span data-ttu-id="fabba-379">non</span><span class="sxs-lookup"><span data-stu-id="fabba-379">no</span></span>           |
| <span data-ttu-id="fabba-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="fabba-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="fabba-381">non</span><span class="sxs-lookup"><span data-stu-id="fabba-381">no</span></span>             | <span data-ttu-id="fabba-382">non</span><span class="sxs-lookup"><span data-stu-id="fabba-382">no</span></span>           |
| <span data-ttu-id="fabba-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="fabba-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="fabba-384">non</span><span class="sxs-lookup"><span data-stu-id="fabba-384">no</span></span>             | <span data-ttu-id="fabba-385">non</span><span class="sxs-lookup"><span data-stu-id="fabba-385">no</span></span>           |
| <span data-ttu-id="fabba-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="fabba-386">msdyn_committype</span></span>             | <span data-ttu-id="fabba-387">non</span><span class="sxs-lookup"><span data-stu-id="fabba-387">no</span></span>             | <span data-ttu-id="fabba-388">non</span><span class="sxs-lookup"><span data-stu-id="fabba-388">no</span></span>           |
| <span data-ttu-id="fabba-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="fabba-389">msdyn_committypename</span></span>         | <span data-ttu-id="fabba-390">non</span><span class="sxs-lookup"><span data-stu-id="fabba-390">no</span></span>             | <span data-ttu-id="fabba-391">non</span><span class="sxs-lookup"><span data-stu-id="fabba-391">no</span></span>           |
| <span data-ttu-id="fabba-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fabba-392">msdyn_effort</span></span>                 | <span data-ttu-id="fabba-393">non</span><span class="sxs-lookup"><span data-stu-id="fabba-393">no</span></span>             | <span data-ttu-id="fabba-394">non</span><span class="sxs-lookup"><span data-stu-id="fabba-394">no</span></span>           |
| <span data-ttu-id="fabba-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fabba-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="fabba-396">non</span><span class="sxs-lookup"><span data-stu-id="fabba-396">no</span></span>             | <span data-ttu-id="fabba-397">non</span><span class="sxs-lookup"><span data-stu-id="fabba-397">no</span></span>           |
| <span data-ttu-id="fabba-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fabba-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="fabba-399">non</span><span class="sxs-lookup"><span data-stu-id="fabba-399">no</span></span>             | <span data-ttu-id="fabba-400">non</span><span class="sxs-lookup"><span data-stu-id="fabba-400">no</span></span>           |
| <span data-ttu-id="fabba-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fabba-401">msdyn_finish</span></span>                 | <span data-ttu-id="fabba-402">non</span><span class="sxs-lookup"><span data-stu-id="fabba-402">no</span></span>             | <span data-ttu-id="fabba-403">non</span><span class="sxs-lookup"><span data-stu-id="fabba-403">no</span></span>           |
| <span data-ttu-id="fabba-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="fabba-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="fabba-405">non</span><span class="sxs-lookup"><span data-stu-id="fabba-405">no</span></span>             | <span data-ttu-id="fabba-406">non</span><span class="sxs-lookup"><span data-stu-id="fabba-406">no</span></span>           |
| <span data-ttu-id="fabba-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="fabba-408">non</span><span class="sxs-lookup"><span data-stu-id="fabba-408">no</span></span>             | <span data-ttu-id="fabba-409">non</span><span class="sxs-lookup"><span data-stu-id="fabba-409">no</span></span>           |
| <span data-ttu-id="fabba-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="fabba-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="fabba-411">non</span><span class="sxs-lookup"><span data-stu-id="fabba-411">no</span></span>             | <span data-ttu-id="fabba-412">non</span><span class="sxs-lookup"><span data-stu-id="fabba-412">no</span></span>           |
| <span data-ttu-id="fabba-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fabba-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="fabba-414">non</span><span class="sxs-lookup"><span data-stu-id="fabba-414">no</span></span>             | <span data-ttu-id="fabba-415">non</span><span class="sxs-lookup"><span data-stu-id="fabba-415">no</span></span>           |
| <span data-ttu-id="fabba-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="fabba-417">non</span><span class="sxs-lookup"><span data-stu-id="fabba-417">no</span></span>             | <span data-ttu-id="fabba-418">non</span><span class="sxs-lookup"><span data-stu-id="fabba-418">no</span></span>           |
| <span data-ttu-id="fabba-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="fabba-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="fabba-420">non</span><span class="sxs-lookup"><span data-stu-id="fabba-420">no</span></span>             | <span data-ttu-id="fabba-421">non</span><span class="sxs-lookup"><span data-stu-id="fabba-421">no</span></span>           |
| <span data-ttu-id="fabba-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="fabba-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="fabba-423">non</span><span class="sxs-lookup"><span data-stu-id="fabba-423">no</span></span>             | <span data-ttu-id="fabba-424">non</span><span class="sxs-lookup"><span data-stu-id="fabba-424">no</span></span>           |
| <span data-ttu-id="fabba-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="fabba-425">msdyn_projectid</span></span>              | <span data-ttu-id="fabba-426">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-426">yes</span></span>            | <span data-ttu-id="fabba-427">non</span><span class="sxs-lookup"><span data-stu-id="fabba-427">no</span></span>           |
| <span data-ttu-id="fabba-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="fabba-428">msdyn_projectidname</span></span>          | <span data-ttu-id="fabba-429">non</span><span class="sxs-lookup"><span data-stu-id="fabba-429">no</span></span>             | <span data-ttu-id="fabba-430">non</span><span class="sxs-lookup"><span data-stu-id="fabba-430">no</span></span>           |
| <span data-ttu-id="fabba-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="fabba-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="fabba-432">non</span><span class="sxs-lookup"><span data-stu-id="fabba-432">no</span></span>             | <span data-ttu-id="fabba-433">non</span><span class="sxs-lookup"><span data-stu-id="fabba-433">no</span></span>           |
| <span data-ttu-id="fabba-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="fabba-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="fabba-435">non</span><span class="sxs-lookup"><span data-stu-id="fabba-435">no</span></span>             | <span data-ttu-id="fabba-436">non</span><span class="sxs-lookup"><span data-stu-id="fabba-436">no</span></span>           |
| <span data-ttu-id="fabba-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="fabba-437">msdyn_start</span></span>                  | <span data-ttu-id="fabba-438">non</span><span class="sxs-lookup"><span data-stu-id="fabba-438">no</span></span>             | <span data-ttu-id="fabba-439">non</span><span class="sxs-lookup"><span data-stu-id="fabba-439">no</span></span>           |
| <span data-ttu-id="fabba-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="fabba-440">msdyn_taskid</span></span>                 | <span data-ttu-id="fabba-441">non</span><span class="sxs-lookup"><span data-stu-id="fabba-441">no</span></span>             | <span data-ttu-id="fabba-442">non</span><span class="sxs-lookup"><span data-stu-id="fabba-442">no</span></span>           |
| <span data-ttu-id="fabba-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="fabba-443">msdyn_taskidname</span></span>             | <span data-ttu-id="fabba-444">non</span><span class="sxs-lookup"><span data-stu-id="fabba-444">no</span></span>             | <span data-ttu-id="fabba-445">non</span><span class="sxs-lookup"><span data-stu-id="fabba-445">no</span></span>           |
| <span data-ttu-id="fabba-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="fabba-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="fabba-447">non</span><span class="sxs-lookup"><span data-stu-id="fabba-447">no</span></span>             | <span data-ttu-id="fabba-448">non</span><span class="sxs-lookup"><span data-stu-id="fabba-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="fabba-449">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="fabba-449">Project team member</span></span>

| <span data-ttu-id="fabba-450">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="fabba-450">**Logical name**</span></span>                                 | <span data-ttu-id="fabba-451">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="fabba-451">**Can create**</span></span> | <span data-ttu-id="fabba-452">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="fabba-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="fabba-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="fabba-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="fabba-454">non</span><span class="sxs-lookup"><span data-stu-id="fabba-454">no</span></span>             | <span data-ttu-id="fabba-455">non</span><span class="sxs-lookup"><span data-stu-id="fabba-455">no</span></span>           |
| <span data-ttu-id="fabba-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="fabba-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="fabba-457">non</span><span class="sxs-lookup"><span data-stu-id="fabba-457">no</span></span>             | <span data-ttu-id="fabba-458">non</span><span class="sxs-lookup"><span data-stu-id="fabba-458">no</span></span>           |
| <span data-ttu-id="fabba-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="fabba-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="fabba-460">non</span><span class="sxs-lookup"><span data-stu-id="fabba-460">no</span></span>             | <span data-ttu-id="fabba-461">non</span><span class="sxs-lookup"><span data-stu-id="fabba-461">no</span></span>           |
| <span data-ttu-id="fabba-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="fabba-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="fabba-463">non</span><span class="sxs-lookup"><span data-stu-id="fabba-463">no</span></span>             | <span data-ttu-id="fabba-464">non</span><span class="sxs-lookup"><span data-stu-id="fabba-464">no</span></span>           |
| <span data-ttu-id="fabba-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fabba-465">msdyn_effort</span></span>                                     | <span data-ttu-id="fabba-466">non</span><span class="sxs-lookup"><span data-stu-id="fabba-466">no</span></span>             | <span data-ttu-id="fabba-467">non</span><span class="sxs-lookup"><span data-stu-id="fabba-467">no</span></span>           |
| <span data-ttu-id="fabba-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fabba-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="fabba-469">non</span><span class="sxs-lookup"><span data-stu-id="fabba-469">no</span></span>             | <span data-ttu-id="fabba-470">non</span><span class="sxs-lookup"><span data-stu-id="fabba-470">no</span></span>           |
| <span data-ttu-id="fabba-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fabba-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="fabba-472">non</span><span class="sxs-lookup"><span data-stu-id="fabba-472">no</span></span>             | <span data-ttu-id="fabba-473">non</span><span class="sxs-lookup"><span data-stu-id="fabba-473">no</span></span>           |
| <span data-ttu-id="fabba-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fabba-474">msdyn_finish</span></span>                                     | <span data-ttu-id="fabba-475">non</span><span class="sxs-lookup"><span data-stu-id="fabba-475">no</span></span>             | <span data-ttu-id="fabba-476">non</span><span class="sxs-lookup"><span data-stu-id="fabba-476">no</span></span>           |
| <span data-ttu-id="fabba-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="fabba-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="fabba-478">non</span><span class="sxs-lookup"><span data-stu-id="fabba-478">no</span></span>             | <span data-ttu-id="fabba-479">non</span><span class="sxs-lookup"><span data-stu-id="fabba-479">no</span></span>           |
| <span data-ttu-id="fabba-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="fabba-480">msdyn_hours</span></span>                                      | <span data-ttu-id="fabba-481">non</span><span class="sxs-lookup"><span data-stu-id="fabba-481">no</span></span>             | <span data-ttu-id="fabba-482">non</span><span class="sxs-lookup"><span data-stu-id="fabba-482">no</span></span>           |
| <span data-ttu-id="fabba-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="fabba-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="fabba-484">non</span><span class="sxs-lookup"><span data-stu-id="fabba-484">no</span></span>             | <span data-ttu-id="fabba-485">non</span><span class="sxs-lookup"><span data-stu-id="fabba-485">no</span></span>           |
| <span data-ttu-id="fabba-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="fabba-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="fabba-487">non</span><span class="sxs-lookup"><span data-stu-id="fabba-487">no</span></span>             | <span data-ttu-id="fabba-488">non</span><span class="sxs-lookup"><span data-stu-id="fabba-488">no</span></span>           |
| <span data-ttu-id="fabba-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="fabba-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="fabba-490">non</span><span class="sxs-lookup"><span data-stu-id="fabba-490">no</span></span>             | <span data-ttu-id="fabba-491">non</span><span class="sxs-lookup"><span data-stu-id="fabba-491">no</span></span>           |
| <span data-ttu-id="fabba-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="fabba-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="fabba-493">non</span><span class="sxs-lookup"><span data-stu-id="fabba-493">no</span></span>             | <span data-ttu-id="fabba-494">non</span><span class="sxs-lookup"><span data-stu-id="fabba-494">no</span></span>           |
| <span data-ttu-id="fabba-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="fabba-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="fabba-496">non</span><span class="sxs-lookup"><span data-stu-id="fabba-496">no</span></span>             | <span data-ttu-id="fabba-497">non</span><span class="sxs-lookup"><span data-stu-id="fabba-497">no</span></span>           |
| <span data-ttu-id="fabba-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="fabba-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="fabba-499">non</span><span class="sxs-lookup"><span data-stu-id="fabba-499">no</span></span>             | <span data-ttu-id="fabba-500">non</span><span class="sxs-lookup"><span data-stu-id="fabba-500">no</span></span>           |
| <span data-ttu-id="fabba-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="fabba-501">msdyn_start</span></span>                                      | <span data-ttu-id="fabba-502">non</span><span class="sxs-lookup"><span data-stu-id="fabba-502">no</span></span>             | <span data-ttu-id="fabba-503">non</span><span class="sxs-lookup"><span data-stu-id="fabba-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="fabba-504">Project</span><span class="sxs-lookup"><span data-stu-id="fabba-504">Project</span></span>

| <span data-ttu-id="fabba-505">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="fabba-505">**Logical name**</span></span>                       | <span data-ttu-id="fabba-506">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="fabba-506">**Can create**</span></span> | <span data-ttu-id="fabba-507">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="fabba-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="fabba-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="fabba-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="fabba-509">non</span><span class="sxs-lookup"><span data-stu-id="fabba-509">no</span></span>             | <span data-ttu-id="fabba-510">non</span><span class="sxs-lookup"><span data-stu-id="fabba-510">no</span></span>           |
| <span data-ttu-id="fabba-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="fabba-512">non</span><span class="sxs-lookup"><span data-stu-id="fabba-512">no</span></span>             | <span data-ttu-id="fabba-513">non</span><span class="sxs-lookup"><span data-stu-id="fabba-513">no</span></span>           |
| <span data-ttu-id="fabba-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="fabba-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="fabba-515">non</span><span class="sxs-lookup"><span data-stu-id="fabba-515">no</span></span>             | <span data-ttu-id="fabba-516">non</span><span class="sxs-lookup"><span data-stu-id="fabba-516">no</span></span>           |
| <span data-ttu-id="fabba-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="fabba-518">non</span><span class="sxs-lookup"><span data-stu-id="fabba-518">no</span></span>             | <span data-ttu-id="fabba-519">non</span><span class="sxs-lookup"><span data-stu-id="fabba-519">no</span></span>           |
| <span data-ttu-id="fabba-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="fabba-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="fabba-521">non</span><span class="sxs-lookup"><span data-stu-id="fabba-521">no</span></span>             | <span data-ttu-id="fabba-522">non</span><span class="sxs-lookup"><span data-stu-id="fabba-522">no</span></span>           |
| <span data-ttu-id="fabba-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="fabba-524">non</span><span class="sxs-lookup"><span data-stu-id="fabba-524">no</span></span>             | <span data-ttu-id="fabba-525">non</span><span class="sxs-lookup"><span data-stu-id="fabba-525">no</span></span>           |
| <span data-ttu-id="fabba-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="fabba-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="fabba-527">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-527">yes</span></span>            | <span data-ttu-id="fabba-528">non</span><span class="sxs-lookup"><span data-stu-id="fabba-528">no</span></span>           |
| <span data-ttu-id="fabba-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="fabba-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="fabba-530">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-530">yes</span></span>            | <span data-ttu-id="fabba-531">non</span><span class="sxs-lookup"><span data-stu-id="fabba-531">no</span></span>           |
| <span data-ttu-id="fabba-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="fabba-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="fabba-533">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-533">yes</span></span>            | <span data-ttu-id="fabba-534">non</span><span class="sxs-lookup"><span data-stu-id="fabba-534">no</span></span>           |
| <span data-ttu-id="fabba-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="fabba-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="fabba-536">non</span><span class="sxs-lookup"><span data-stu-id="fabba-536">no</span></span>             | <span data-ttu-id="fabba-537">non</span><span class="sxs-lookup"><span data-stu-id="fabba-537">no</span></span>           |
| <span data-ttu-id="fabba-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fabba-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="fabba-539">non</span><span class="sxs-lookup"><span data-stu-id="fabba-539">no</span></span>             | <span data-ttu-id="fabba-540">non</span><span class="sxs-lookup"><span data-stu-id="fabba-540">no</span></span>           |
| <span data-ttu-id="fabba-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="fabba-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="fabba-542">non</span><span class="sxs-lookup"><span data-stu-id="fabba-542">no</span></span>             | <span data-ttu-id="fabba-543">non</span><span class="sxs-lookup"><span data-stu-id="fabba-543">no</span></span>           |
| <span data-ttu-id="fabba-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="fabba-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="fabba-545">non</span><span class="sxs-lookup"><span data-stu-id="fabba-545">no</span></span>             | <span data-ttu-id="fabba-546">non</span><span class="sxs-lookup"><span data-stu-id="fabba-546">no</span></span>           |
| <span data-ttu-id="fabba-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="fabba-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="fabba-548">non</span><span class="sxs-lookup"><span data-stu-id="fabba-548">no</span></span>             | <span data-ttu-id="fabba-549">non</span><span class="sxs-lookup"><span data-stu-id="fabba-549">no</span></span>           |
| <span data-ttu-id="fabba-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="fabba-550">msdyn_duration</span></span>                         | <span data-ttu-id="fabba-551">non</span><span class="sxs-lookup"><span data-stu-id="fabba-551">no</span></span>             | <span data-ttu-id="fabba-552">non</span><span class="sxs-lookup"><span data-stu-id="fabba-552">no</span></span>           |
| <span data-ttu-id="fabba-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fabba-553">msdyn_effort</span></span>                           | <span data-ttu-id="fabba-554">non</span><span class="sxs-lookup"><span data-stu-id="fabba-554">no</span></span>             | <span data-ttu-id="fabba-555">non</span><span class="sxs-lookup"><span data-stu-id="fabba-555">no</span></span>           |
| <span data-ttu-id="fabba-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fabba-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="fabba-557">non</span><span class="sxs-lookup"><span data-stu-id="fabba-557">no</span></span>             | <span data-ttu-id="fabba-558">non</span><span class="sxs-lookup"><span data-stu-id="fabba-558">no</span></span>           |
| <span data-ttu-id="fabba-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="fabba-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="fabba-560">non</span><span class="sxs-lookup"><span data-stu-id="fabba-560">no</span></span>             | <span data-ttu-id="fabba-561">non</span><span class="sxs-lookup"><span data-stu-id="fabba-561">no</span></span>           |
| <span data-ttu-id="fabba-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fabba-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="fabba-563">non</span><span class="sxs-lookup"><span data-stu-id="fabba-563">no</span></span>             | <span data-ttu-id="fabba-564">non</span><span class="sxs-lookup"><span data-stu-id="fabba-564">no</span></span>           |
| <span data-ttu-id="fabba-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fabba-565">msdyn_finish</span></span>                           | <span data-ttu-id="fabba-566">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-566">yes</span></span>            | <span data-ttu-id="fabba-567">oui</span><span class="sxs-lookup"><span data-stu-id="fabba-567">yes</span></span>          |
| <span data-ttu-id="fabba-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="fabba-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="fabba-569">non</span><span class="sxs-lookup"><span data-stu-id="fabba-569">no</span></span>             | <span data-ttu-id="fabba-570">non</span><span class="sxs-lookup"><span data-stu-id="fabba-570">no</span></span>           |
| <span data-ttu-id="fabba-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="fabba-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="fabba-572">non</span><span class="sxs-lookup"><span data-stu-id="fabba-572">no</span></span>             | <span data-ttu-id="fabba-573">non</span><span class="sxs-lookup"><span data-stu-id="fabba-573">no</span></span>           |
| <span data-ttu-id="fabba-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="fabba-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="fabba-575">non</span><span class="sxs-lookup"><span data-stu-id="fabba-575">no</span></span>             | <span data-ttu-id="fabba-576">non</span><span class="sxs-lookup"><span data-stu-id="fabba-576">no</span></span>           |
| <span data-ttu-id="fabba-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="fabba-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="fabba-578">non</span><span class="sxs-lookup"><span data-stu-id="fabba-578">no</span></span>             | <span data-ttu-id="fabba-579">non</span><span class="sxs-lookup"><span data-stu-id="fabba-579">no</span></span>           |
| <span data-ttu-id="fabba-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="fabba-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="fabba-581">non</span><span class="sxs-lookup"><span data-stu-id="fabba-581">no</span></span>             | <span data-ttu-id="fabba-582">non</span><span class="sxs-lookup"><span data-stu-id="fabba-582">no</span></span>           |
| <span data-ttu-id="fabba-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="fabba-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="fabba-584">non</span><span class="sxs-lookup"><span data-stu-id="fabba-584">no</span></span>             | <span data-ttu-id="fabba-585">non</span><span class="sxs-lookup"><span data-stu-id="fabba-585">no</span></span>           |
| <span data-ttu-id="fabba-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="fabba-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="fabba-587">non</span><span class="sxs-lookup"><span data-stu-id="fabba-587">no</span></span>             | <span data-ttu-id="fabba-588">non</span><span class="sxs-lookup"><span data-stu-id="fabba-588">no</span></span>           |
| <span data-ttu-id="fabba-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="fabba-590">non</span><span class="sxs-lookup"><span data-stu-id="fabba-590">no</span></span>             | <span data-ttu-id="fabba-591">non</span><span class="sxs-lookup"><span data-stu-id="fabba-591">no</span></span>           |
| <span data-ttu-id="fabba-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="fabba-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="fabba-593">non</span><span class="sxs-lookup"><span data-stu-id="fabba-593">no</span></span>             | <span data-ttu-id="fabba-594">non</span><span class="sxs-lookup"><span data-stu-id="fabba-594">no</span></span>           |
| <span data-ttu-id="fabba-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="fabba-596">non</span><span class="sxs-lookup"><span data-stu-id="fabba-596">no</span></span>             | <span data-ttu-id="fabba-597">non</span><span class="sxs-lookup"><span data-stu-id="fabba-597">no</span></span>           |
| <span data-ttu-id="fabba-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fabba-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="fabba-599">non</span><span class="sxs-lookup"><span data-stu-id="fabba-599">no</span></span>             | <span data-ttu-id="fabba-600">non</span><span class="sxs-lookup"><span data-stu-id="fabba-600">no</span></span>           |
| <span data-ttu-id="fabba-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="fabba-602">non</span><span class="sxs-lookup"><span data-stu-id="fabba-602">no</span></span>             | <span data-ttu-id="fabba-603">non</span><span class="sxs-lookup"><span data-stu-id="fabba-603">no</span></span>           |
| <span data-ttu-id="fabba-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="fabba-604">msdyn_progress</span></span>                         | <span data-ttu-id="fabba-605">non</span><span class="sxs-lookup"><span data-stu-id="fabba-605">no</span></span>             | <span data-ttu-id="fabba-606">non</span><span class="sxs-lookup"><span data-stu-id="fabba-606">no</span></span>           |
| <span data-ttu-id="fabba-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="fabba-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="fabba-608">non</span><span class="sxs-lookup"><span data-stu-id="fabba-608">no</span></span>             | <span data-ttu-id="fabba-609">non</span><span class="sxs-lookup"><span data-stu-id="fabba-609">no</span></span>           |
| <span data-ttu-id="fabba-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="fabba-611">non</span><span class="sxs-lookup"><span data-stu-id="fabba-611">no</span></span>             | <span data-ttu-id="fabba-612">non</span><span class="sxs-lookup"><span data-stu-id="fabba-612">no</span></span>           |
| <span data-ttu-id="fabba-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="fabba-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="fabba-614">non</span><span class="sxs-lookup"><span data-stu-id="fabba-614">no</span></span>             | <span data-ttu-id="fabba-615">non</span><span class="sxs-lookup"><span data-stu-id="fabba-615">no</span></span>           |
| <span data-ttu-id="fabba-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="fabba-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="fabba-617">non</span><span class="sxs-lookup"><span data-stu-id="fabba-617">no</span></span>             | <span data-ttu-id="fabba-618">non</span><span class="sxs-lookup"><span data-stu-id="fabba-618">no</span></span>           |
| <span data-ttu-id="fabba-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="fabba-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="fabba-620">non</span><span class="sxs-lookup"><span data-stu-id="fabba-620">no</span></span>             | <span data-ttu-id="fabba-621">non</span><span class="sxs-lookup"><span data-stu-id="fabba-621">no</span></span>           |
| <span data-ttu-id="fabba-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="fabba-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="fabba-623">non</span><span class="sxs-lookup"><span data-stu-id="fabba-623">no</span></span>             | <span data-ttu-id="fabba-624">non</span><span class="sxs-lookup"><span data-stu-id="fabba-624">no</span></span>           |
| <span data-ttu-id="fabba-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="fabba-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="fabba-626">non</span><span class="sxs-lookup"><span data-stu-id="fabba-626">no</span></span>             | <span data-ttu-id="fabba-627">non</span><span class="sxs-lookup"><span data-stu-id="fabba-627">no</span></span>           |
| <span data-ttu-id="fabba-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="fabba-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="fabba-629">non</span><span class="sxs-lookup"><span data-stu-id="fabba-629">no</span></span>             | <span data-ttu-id="fabba-630">non</span><span class="sxs-lookup"><span data-stu-id="fabba-630">no</span></span>           |
| <span data-ttu-id="fabba-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="fabba-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="fabba-632">non</span><span class="sxs-lookup"><span data-stu-id="fabba-632">no</span></span>             | <span data-ttu-id="fabba-633">non</span><span class="sxs-lookup"><span data-stu-id="fabba-633">no</span></span>           |
| <span data-ttu-id="fabba-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="fabba-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="fabba-635">non</span><span class="sxs-lookup"><span data-stu-id="fabba-635">no</span></span>             | <span data-ttu-id="fabba-636">non</span><span class="sxs-lookup"><span data-stu-id="fabba-636">no</span></span>           |
| <span data-ttu-id="fabba-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="fabba-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="fabba-638">non</span><span class="sxs-lookup"><span data-stu-id="fabba-638">no</span></span>             | <span data-ttu-id="fabba-639">non</span><span class="sxs-lookup"><span data-stu-id="fabba-639">no</span></span>           |
| <span data-ttu-id="fabba-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="fabba-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="fabba-641">non</span><span class="sxs-lookup"><span data-stu-id="fabba-641">no</span></span>             | <span data-ttu-id="fabba-642">non</span><span class="sxs-lookup"><span data-stu-id="fabba-642">no</span></span>           |
| <span data-ttu-id="fabba-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="fabba-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="fabba-644">non</span><span class="sxs-lookup"><span data-stu-id="fabba-644">no</span></span>             | <span data-ttu-id="fabba-645">non</span><span class="sxs-lookup"><span data-stu-id="fabba-645">no</span></span>           |
| <span data-ttu-id="fabba-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="fabba-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="fabba-647">non</span><span class="sxs-lookup"><span data-stu-id="fabba-647">no</span></span>             | <span data-ttu-id="fabba-648">non</span><span class="sxs-lookup"><span data-stu-id="fabba-648">no</span></span>           |
| <span data-ttu-id="fabba-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="fabba-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="fabba-650">non</span><span class="sxs-lookup"><span data-stu-id="fabba-650">no</span></span>             | <span data-ttu-id="fabba-651">non</span><span class="sxs-lookup"><span data-stu-id="fabba-651">no</span></span>           |
| <span data-ttu-id="fabba-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="fabba-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="fabba-653">non</span><span class="sxs-lookup"><span data-stu-id="fabba-653">no</span></span>             | <span data-ttu-id="fabba-654">non</span><span class="sxs-lookup"><span data-stu-id="fabba-654">no</span></span>           |
| <span data-ttu-id="fabba-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="fabba-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="fabba-656">non</span><span class="sxs-lookup"><span data-stu-id="fabba-656">no</span></span>             | <span data-ttu-id="fabba-657">non</span><span class="sxs-lookup"><span data-stu-id="fabba-657">no</span></span>           |
| <span data-ttu-id="fabba-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="fabba-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="fabba-659">non</span><span class="sxs-lookup"><span data-stu-id="fabba-659">no</span></span>             | <span data-ttu-id="fabba-660">non</span><span class="sxs-lookup"><span data-stu-id="fabba-660">no</span></span>           |
| <span data-ttu-id="fabba-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="fabba-662">non</span><span class="sxs-lookup"><span data-stu-id="fabba-662">no</span></span>             | <span data-ttu-id="fabba-663">non</span><span class="sxs-lookup"><span data-stu-id="fabba-663">no</span></span>           |
| <span data-ttu-id="fabba-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="fabba-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="fabba-665">non</span><span class="sxs-lookup"><span data-stu-id="fabba-665">no</span></span>             | <span data-ttu-id="fabba-666">non</span><span class="sxs-lookup"><span data-stu-id="fabba-666">no</span></span>           |
| <span data-ttu-id="fabba-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fabba-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="fabba-668">non</span><span class="sxs-lookup"><span data-stu-id="fabba-668">no</span></span>             | <span data-ttu-id="fabba-669">non</span><span class="sxs-lookup"><span data-stu-id="fabba-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="fabba-670">Limitations et problèmes connus</span><span class="sxs-lookup"><span data-stu-id="fabba-670">Limitations and known issues</span></span>
<span data-ttu-id="fabba-671">Voici une liste des limitations et des problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="fabba-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="fabba-672">Les API de planification ne peuvent être utilisées que par les **utilisateurs disposant d’une licence Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="fabba-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="fabba-673">Elles ne peuvent pas être utilisées par :</span><span class="sxs-lookup"><span data-stu-id="fabba-673">They can't be used by:</span></span>
    - <span data-ttu-id="fabba-674">Utilisateurs de l’application</span><span class="sxs-lookup"><span data-stu-id="fabba-674">Application users</span></span>
    - <span data-ttu-id="fabba-675">Utilisateurs du système</span><span class="sxs-lookup"><span data-stu-id="fabba-675">System users</span></span>
    - <span data-ttu-id="fabba-676">Utilisateurs de l’intégration</span><span class="sxs-lookup"><span data-stu-id="fabba-676">Integration users</span></span>
    - <span data-ttu-id="fabba-677">Autres utilisateurs ne disposant pas de la licence requise</span><span class="sxs-lookup"><span data-stu-id="fabba-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="fabba-678">Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.</span><span class="sxs-lookup"><span data-stu-id="fabba-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="fabba-679">Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.</span><span class="sxs-lookup"><span data-stu-id="fabba-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="fabba-680">Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.</span><span class="sxs-lookup"><span data-stu-id="fabba-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="fabba-681">Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="fabba-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="fabba-682">Limites des projets et des tâches</span><span class="sxs-lookup"><span data-stu-id="fabba-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="fabba-683">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="fabba-683">Error handling</span></span>

   - <span data-ttu-id="fabba-684">Pour consulter les erreurs générées par les ensembles d’opérations, accédez à **Paramètres** \> **Planifier l’intégration** \> **Ensembles d’opérations**.</span><span class="sxs-lookup"><span data-stu-id="fabba-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="fabba-685">Pour consulter les erreurs générées par le service de planification de projet, accédez à **Paramètres** \> **Planifier l’intégration** \> **Journaux des erreurs de PSS**.</span><span class="sxs-lookup"><span data-stu-id="fabba-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="fabba-686">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="fabba-686">Sample scenario</span></span>

<span data-ttu-id="fabba-687">Dans ce scénario, vous allez créer un projet, un membre de l’équipe, quatre tâches et deux affectations de ressources.</span><span class="sxs-lookup"><span data-stu-id="fabba-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="fabba-688">Ensuite, vous allez mettre à jour une tâche, mettre à jour le projet, supprimer une tâche, supprimer une affectation de ressource et créer une dépendance de tâche.</span><span class="sxs-lookup"><span data-stu-id="fabba-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="fabba-689">Exemples supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fabba-689">Additional samples</span></span>

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
