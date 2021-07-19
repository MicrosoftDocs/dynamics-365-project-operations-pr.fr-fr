---
title: Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification
description: Cette rubrique fournit des informations et des exemples pour utiliser les API de planification de projets.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293224"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="7539b-103">Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification</span><span class="sxs-lookup"><span data-stu-id="7539b-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="7539b-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="7539b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="7539b-105">Certaines ou toutes les fonctionnalités mentionnées dans cette rubrique sont disponibles dans le cadre d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="7539b-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="7539b-106">Le contenu et les fonctionnalités sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="7539b-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="7539b-107">Entités de planification</span><span class="sxs-lookup"><span data-stu-id="7539b-107">Scheduling entities</span></span>

<span data-ttu-id="7539b-108">Les API de planification de projets offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec les **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="7539b-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="7539b-109">Ces entités sont gérées via le moteur de planification de l’application Project pour le Web.</span><span class="sxs-lookup"><span data-stu-id="7539b-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="7539b-110">Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7539b-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="7539b-111">Le tableau suivant fournit une liste complète des entités de planification de projets.</span><span class="sxs-lookup"><span data-stu-id="7539b-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="7539b-112">Nom de l'entité</span><span class="sxs-lookup"><span data-stu-id="7539b-112">Entity name</span></span>  | <span data-ttu-id="7539b-113">Nom logique de l’entité</span><span class="sxs-lookup"><span data-stu-id="7539b-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="7539b-114">Project</span><span class="sxs-lookup"><span data-stu-id="7539b-114">Project</span></span> | <span data-ttu-id="7539b-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7539b-115">msdyn_project</span></span> |
| <span data-ttu-id="7539b-116">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-116">Project Task</span></span>  | <span data-ttu-id="7539b-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="7539b-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="7539b-118">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-118">Project Task Dependency</span></span>  | <span data-ttu-id="7539b-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="7539b-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="7539b-120">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="7539b-120">Resource Assignment</span></span> | <span data-ttu-id="7539b-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="7539b-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="7539b-122">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-122">Project Bucket</span></span>  | <span data-ttu-id="7539b-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="7539b-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="7539b-124">Membre de l’équipe du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-124">Project Team Member</span></span> | <span data-ttu-id="7539b-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="7539b-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="7539b-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="7539b-126">OperationSet</span></span>

<span data-ttu-id="7539b-127">OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="7539b-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="7539b-128">API de planification de projets</span><span class="sxs-lookup"><span data-stu-id="7539b-128">Project schedule APIs</span></span>

<span data-ttu-id="7539b-129">Voici la liste des API de planification de projet actuelles.</span><span class="sxs-lookup"><span data-stu-id="7539b-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="7539b-130">**msdyn_CreateProjectV1** : Cette API peut être utilisée pour créer un projet.</span><span class="sxs-lookup"><span data-stu-id="7539b-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="7539b-131">Le projet et le compartiment de projet par défaut sont créés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7539b-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="7539b-132">**msdyn_CreateTeamMemberV1** : Cette API peut être utilisée pour créer un membre de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="7539b-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="7539b-133">L’enregistrement de membre de l’équipe est créé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7539b-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="7539b-134">**msdyn_CreateOperationSetV1** : Cette API peut être utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="7539b-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="7539b-135">**msdyn_PSSCreateV1** : Cette API peut être utilisée pour créer une entité.</span><span class="sxs-lookup"><span data-stu-id="7539b-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="7539b-136">L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="7539b-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="7539b-137">**msdyn_PSSUpdateV1** : Cette API peut être utilisée pour mettre à jour une entité.</span><span class="sxs-lookup"><span data-stu-id="7539b-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="7539b-138">L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7539b-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="7539b-139">**msdyn_PSSDeleteV1** : Cette API peut être utilisée pour supprimer une entité.</span><span class="sxs-lookup"><span data-stu-id="7539b-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="7539b-140">L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="7539b-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="7539b-141">**msdyn_ExecuteOperationSetV1** : Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.</span><span class="sxs-lookup"><span data-stu-id="7539b-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="7539b-142">Utilisation des API de planification de projets avec OperationSet</span><span class="sxs-lookup"><span data-stu-id="7539b-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="7539b-143">Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7539b-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="7539b-144">Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7539b-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="7539b-145">Opérations prises en charge</span><span class="sxs-lookup"><span data-stu-id="7539b-145">Supported operations</span></span>

| <span data-ttu-id="7539b-146">Entité de planification</span><span class="sxs-lookup"><span data-stu-id="7539b-146">Scheduling entity</span></span> | <span data-ttu-id="7539b-147">Créer</span><span class="sxs-lookup"><span data-stu-id="7539b-147">Create</span></span> | <span data-ttu-id="7539b-148">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="7539b-148">Update</span></span> | <span data-ttu-id="7539b-149">Suppr</span><span class="sxs-lookup"><span data-stu-id="7539b-149">Delete</span></span> | <span data-ttu-id="7539b-150">Remarques importantes</span><span class="sxs-lookup"><span data-stu-id="7539b-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="7539b-151">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-151">Project task</span></span> | <span data-ttu-id="7539b-152">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-152">Yes</span></span> | <span data-ttu-id="7539b-153">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-153">Yes</span></span> | <span data-ttu-id="7539b-154">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-154">Yes</span></span> | <span data-ttu-id="7539b-155">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="7539b-155">None</span></span> |
| <span data-ttu-id="7539b-156">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-156">Project task dependency</span></span> | <span data-ttu-id="7539b-157">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-157">Yes</span></span> | <span data-ttu-id="7539b-158">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-158">Yes</span></span> | | <span data-ttu-id="7539b-159">Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7539b-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="7539b-160">Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="7539b-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7539b-161">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="7539b-161">Resource assignment</span></span> | <span data-ttu-id="7539b-162">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-162">Yes</span></span> | <span data-ttu-id="7539b-163">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-163">Yes</span></span> | | <span data-ttu-id="7539b-164">Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="7539b-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="7539b-165">Les enregistrements d’attribution de ressource ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7539b-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="7539b-166">Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="7539b-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7539b-167">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-167">Project bucket</span></span> | <span data-ttu-id="7539b-168">N/A</span><span class="sxs-lookup"><span data-stu-id="7539b-168">N/A</span></span> | <span data-ttu-id="7539b-169">N/A</span><span class="sxs-lookup"><span data-stu-id="7539b-169">N/A</span></span> | <span data-ttu-id="7539b-170">N/A</span><span class="sxs-lookup"><span data-stu-id="7539b-170">N/A</span></span> | <span data-ttu-id="7539b-171">Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="7539b-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="7539b-172">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="7539b-172">Project team member</span></span> | <span data-ttu-id="7539b-173">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-173">Yes</span></span> | <span data-ttu-id="7539b-174">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-174">Yes</span></span> | <span data-ttu-id="7539b-175">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-175">Yes</span></span> | <span data-ttu-id="7539b-176">Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="7539b-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="7539b-177">Project</span><span class="sxs-lookup"><span data-stu-id="7539b-177">Project</span></span> | <span data-ttu-id="7539b-178">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-178">Yes</span></span> | <span data-ttu-id="7539b-179">Oui</span><span class="sxs-lookup"><span data-stu-id="7539b-179">Yes</span></span> | <span data-ttu-id="7539b-180">N/A</span><span class="sxs-lookup"><span data-stu-id="7539b-180">N/A</span></span> | <span data-ttu-id="7539b-181">Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**.</span><span class="sxs-lookup"><span data-stu-id="7539b-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="7539b-182">Ces API peuvent être appelées avec des objets d’entité qui incluent des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7539b-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="7539b-183">La propriété ID est facultative.</span><span class="sxs-lookup"><span data-stu-id="7539b-183">The ID property is optional.</span></span> <span data-ttu-id="7539b-184">Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7539b-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="7539b-185">Si elle n’est pas fournie, le système la générera.</span><span class="sxs-lookup"><span data-stu-id="7539b-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="7539b-186">Champs interdits</span><span class="sxs-lookup"><span data-stu-id="7539b-186">Restricted fields</span></span>

<span data-ttu-id="7539b-187">Les tableaux suivants définissent les champs interdits pour **Créer** et **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="7539b-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="7539b-188">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-188">Project task</span></span>

| <span data-ttu-id="7539b-189">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="7539b-189">**Logical name**</span></span>                       | <span data-ttu-id="7539b-190">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="7539b-190">**Can create**</span></span> | <span data-ttu-id="7539b-191">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="7539b-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="7539b-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="7539b-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="7539b-193">non</span><span class="sxs-lookup"><span data-stu-id="7539b-193">no</span></span>             | <span data-ttu-id="7539b-194">non</span><span class="sxs-lookup"><span data-stu-id="7539b-194">no</span></span>               |
| <span data-ttu-id="7539b-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="7539b-196">non</span><span class="sxs-lookup"><span data-stu-id="7539b-196">no</span></span>             | <span data-ttu-id="7539b-197">non</span><span class="sxs-lookup"><span data-stu-id="7539b-197">no</span></span>               |
| <span data-ttu-id="7539b-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="7539b-198">msdyn_actualend</span></span>                        | <span data-ttu-id="7539b-199">non</span><span class="sxs-lookup"><span data-stu-id="7539b-199">no</span></span>             | <span data-ttu-id="7539b-200">non</span><span class="sxs-lookup"><span data-stu-id="7539b-200">no</span></span>               |
| <span data-ttu-id="7539b-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7539b-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="7539b-202">non</span><span class="sxs-lookup"><span data-stu-id="7539b-202">no</span></span>             | <span data-ttu-id="7539b-203">non</span><span class="sxs-lookup"><span data-stu-id="7539b-203">no</span></span>               |
| <span data-ttu-id="7539b-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7539b-205">non</span><span class="sxs-lookup"><span data-stu-id="7539b-205">no</span></span>             | <span data-ttu-id="7539b-206">non</span><span class="sxs-lookup"><span data-stu-id="7539b-206">no</span></span>               |
| <span data-ttu-id="7539b-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="7539b-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="7539b-208">non</span><span class="sxs-lookup"><span data-stu-id="7539b-208">no</span></span>             | <span data-ttu-id="7539b-209">non</span><span class="sxs-lookup"><span data-stu-id="7539b-209">no</span></span>               |
| <span data-ttu-id="7539b-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="7539b-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="7539b-211">non</span><span class="sxs-lookup"><span data-stu-id="7539b-211">no</span></span>             | <span data-ttu-id="7539b-212">non</span><span class="sxs-lookup"><span data-stu-id="7539b-212">no</span></span>               |
| <span data-ttu-id="7539b-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="7539b-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="7539b-214">non</span><span class="sxs-lookup"><span data-stu-id="7539b-214">no</span></span>             | <span data-ttu-id="7539b-215">non</span><span class="sxs-lookup"><span data-stu-id="7539b-215">no</span></span>               |
| <span data-ttu-id="7539b-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7539b-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="7539b-217">non</span><span class="sxs-lookup"><span data-stu-id="7539b-217">no</span></span>             | <span data-ttu-id="7539b-218">non</span><span class="sxs-lookup"><span data-stu-id="7539b-218">no</span></span>               |
| <span data-ttu-id="7539b-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7539b-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7539b-220">non</span><span class="sxs-lookup"><span data-stu-id="7539b-220">no</span></span>             | <span data-ttu-id="7539b-221">non</span><span class="sxs-lookup"><span data-stu-id="7539b-221">no</span></span>               |
| <span data-ttu-id="7539b-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7539b-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="7539b-223">non</span><span class="sxs-lookup"><span data-stu-id="7539b-223">no</span></span>             | <span data-ttu-id="7539b-224">non</span><span class="sxs-lookup"><span data-stu-id="7539b-224">no</span></span>               |
| <span data-ttu-id="7539b-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="7539b-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="7539b-226">non</span><span class="sxs-lookup"><span data-stu-id="7539b-226">no</span></span>             | <span data-ttu-id="7539b-227">non</span><span class="sxs-lookup"><span data-stu-id="7539b-227">no</span></span>               |
| <span data-ttu-id="7539b-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="7539b-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="7539b-229">non</span><span class="sxs-lookup"><span data-stu-id="7539b-229">no</span></span>             | <span data-ttu-id="7539b-230">non</span><span class="sxs-lookup"><span data-stu-id="7539b-230">no</span></span>               |
| <span data-ttu-id="7539b-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="7539b-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="7539b-232">non</span><span class="sxs-lookup"><span data-stu-id="7539b-232">no</span></span>             | <span data-ttu-id="7539b-233">non</span><span class="sxs-lookup"><span data-stu-id="7539b-233">no</span></span>               |
| <span data-ttu-id="7539b-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="7539b-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="7539b-235">non</span><span class="sxs-lookup"><span data-stu-id="7539b-235">no</span></span>             | <span data-ttu-id="7539b-236">non</span><span class="sxs-lookup"><span data-stu-id="7539b-236">no</span></span>               |
| <span data-ttu-id="7539b-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="7539b-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="7539b-238">non</span><span class="sxs-lookup"><span data-stu-id="7539b-238">no</span></span>             | <span data-ttu-id="7539b-239">non</span><span class="sxs-lookup"><span data-stu-id="7539b-239">no</span></span>               |
| <span data-ttu-id="7539b-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="7539b-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="7539b-241">non</span><span class="sxs-lookup"><span data-stu-id="7539b-241">no</span></span>             | <span data-ttu-id="7539b-242">non</span><span class="sxs-lookup"><span data-stu-id="7539b-242">no</span></span>               |
| <span data-ttu-id="7539b-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="7539b-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="7539b-244">non</span><span class="sxs-lookup"><span data-stu-id="7539b-244">no</span></span>             | <span data-ttu-id="7539b-245">non</span><span class="sxs-lookup"><span data-stu-id="7539b-245">no</span></span>               |
| <span data-ttu-id="7539b-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="7539b-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="7539b-247">non</span><span class="sxs-lookup"><span data-stu-id="7539b-247">no</span></span>             | <span data-ttu-id="7539b-248">non</span><span class="sxs-lookup"><span data-stu-id="7539b-248">no</span></span>               |
| <span data-ttu-id="7539b-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7539b-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="7539b-250">non</span><span class="sxs-lookup"><span data-stu-id="7539b-250">no</span></span>             | <span data-ttu-id="7539b-251">non</span><span class="sxs-lookup"><span data-stu-id="7539b-251">no</span></span>               |
| <span data-ttu-id="7539b-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7539b-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="7539b-253">non</span><span class="sxs-lookup"><span data-stu-id="7539b-253">no</span></span>             | <span data-ttu-id="7539b-254">non</span><span class="sxs-lookup"><span data-stu-id="7539b-254">no</span></span>               |
| <span data-ttu-id="7539b-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="7539b-256">non</span><span class="sxs-lookup"><span data-stu-id="7539b-256">no</span></span>             | <span data-ttu-id="7539b-257">non</span><span class="sxs-lookup"><span data-stu-id="7539b-257">no</span></span>               |
| <span data-ttu-id="7539b-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7539b-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7539b-259">non</span><span class="sxs-lookup"><span data-stu-id="7539b-259">no</span></span>             | <span data-ttu-id="7539b-260">non</span><span class="sxs-lookup"><span data-stu-id="7539b-260">no</span></span>               |
| <span data-ttu-id="7539b-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7539b-262">non</span><span class="sxs-lookup"><span data-stu-id="7539b-262">no</span></span>             | <span data-ttu-id="7539b-263">non</span><span class="sxs-lookup"><span data-stu-id="7539b-263">no</span></span>               |
| <span data-ttu-id="7539b-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="7539b-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="7539b-265">non</span><span class="sxs-lookup"><span data-stu-id="7539b-265">no</span></span>             | <span data-ttu-id="7539b-266">non</span><span class="sxs-lookup"><span data-stu-id="7539b-266">no</span></span>               |
| <span data-ttu-id="7539b-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7539b-267">msdyn_progress</span></span>                         | <span data-ttu-id="7539b-268">non</span><span class="sxs-lookup"><span data-stu-id="7539b-268">no</span></span>             | <span data-ttu-id="7539b-269">Non (oui pour P4W)</span><span class="sxs-lookup"><span data-stu-id="7539b-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="7539b-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7539b-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7539b-271">non</span><span class="sxs-lookup"><span data-stu-id="7539b-271">no</span></span>             | <span data-ttu-id="7539b-272">non</span><span class="sxs-lookup"><span data-stu-id="7539b-272">no</span></span>               |
| <span data-ttu-id="7539b-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7539b-274">non</span><span class="sxs-lookup"><span data-stu-id="7539b-274">no</span></span>             | <span data-ttu-id="7539b-275">non</span><span class="sxs-lookup"><span data-stu-id="7539b-275">no</span></span>               |
| <span data-ttu-id="7539b-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7539b-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7539b-277">non</span><span class="sxs-lookup"><span data-stu-id="7539b-277">no</span></span>             | <span data-ttu-id="7539b-278">non</span><span class="sxs-lookup"><span data-stu-id="7539b-278">no</span></span>               |
| <span data-ttu-id="7539b-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7539b-280">non</span><span class="sxs-lookup"><span data-stu-id="7539b-280">no</span></span>             | <span data-ttu-id="7539b-281">non</span><span class="sxs-lookup"><span data-stu-id="7539b-281">no</span></span>               |
| <span data-ttu-id="7539b-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="7539b-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="7539b-283">non</span><span class="sxs-lookup"><span data-stu-id="7539b-283">no</span></span>             | <span data-ttu-id="7539b-284">non</span><span class="sxs-lookup"><span data-stu-id="7539b-284">no</span></span>               |
| <span data-ttu-id="7539b-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7539b-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="7539b-286">non</span><span class="sxs-lookup"><span data-stu-id="7539b-286">no</span></span>             | <span data-ttu-id="7539b-287">non</span><span class="sxs-lookup"><span data-stu-id="7539b-287">no</span></span>               |
| <span data-ttu-id="7539b-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="7539b-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="7539b-289">non</span><span class="sxs-lookup"><span data-stu-id="7539b-289">no</span></span>             | <span data-ttu-id="7539b-290">non</span><span class="sxs-lookup"><span data-stu-id="7539b-290">no</span></span>               |
| <span data-ttu-id="7539b-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7539b-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="7539b-292">non</span><span class="sxs-lookup"><span data-stu-id="7539b-292">no</span></span>             | <span data-ttu-id="7539b-293">non</span><span class="sxs-lookup"><span data-stu-id="7539b-293">no</span></span>               |
| <span data-ttu-id="7539b-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7539b-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="7539b-295">non</span><span class="sxs-lookup"><span data-stu-id="7539b-295">no</span></span>             | <span data-ttu-id="7539b-296">non</span><span class="sxs-lookup"><span data-stu-id="7539b-296">no</span></span>               |
| <span data-ttu-id="7539b-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7539b-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="7539b-298">non</span><span class="sxs-lookup"><span data-stu-id="7539b-298">no</span></span>             | <span data-ttu-id="7539b-299">non</span><span class="sxs-lookup"><span data-stu-id="7539b-299">no</span></span>               |
| <span data-ttu-id="7539b-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7539b-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="7539b-301">non</span><span class="sxs-lookup"><span data-stu-id="7539b-301">no</span></span>             | <span data-ttu-id="7539b-302">non</span><span class="sxs-lookup"><span data-stu-id="7539b-302">no</span></span>               |
| <span data-ttu-id="7539b-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7539b-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="7539b-304">non</span><span class="sxs-lookup"><span data-stu-id="7539b-304">no</span></span>             | <span data-ttu-id="7539b-305">non</span><span class="sxs-lookup"><span data-stu-id="7539b-305">no</span></span>               |
| <span data-ttu-id="7539b-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7539b-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7539b-307">non</span><span class="sxs-lookup"><span data-stu-id="7539b-307">no</span></span>             | <span data-ttu-id="7539b-308">non</span><span class="sxs-lookup"><span data-stu-id="7539b-308">no</span></span>               |
| <span data-ttu-id="7539b-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7539b-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7539b-310">non</span><span class="sxs-lookup"><span data-stu-id="7539b-310">no</span></span>             | <span data-ttu-id="7539b-311">non</span><span class="sxs-lookup"><span data-stu-id="7539b-311">no</span></span>               |
| <span data-ttu-id="7539b-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="7539b-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="7539b-313">non</span><span class="sxs-lookup"><span data-stu-id="7539b-313">no</span></span>             | <span data-ttu-id="7539b-314">non</span><span class="sxs-lookup"><span data-stu-id="7539b-314">no</span></span>               |
| <span data-ttu-id="7539b-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="7539b-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="7539b-316">non</span><span class="sxs-lookup"><span data-stu-id="7539b-316">no</span></span>             | <span data-ttu-id="7539b-317">non</span><span class="sxs-lookup"><span data-stu-id="7539b-317">no</span></span>               |
| <span data-ttu-id="7539b-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="7539b-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="7539b-319">non</span><span class="sxs-lookup"><span data-stu-id="7539b-319">no</span></span>             | <span data-ttu-id="7539b-320">non</span><span class="sxs-lookup"><span data-stu-id="7539b-320">no</span></span>               |
| <span data-ttu-id="7539b-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7539b-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7539b-322">non</span><span class="sxs-lookup"><span data-stu-id="7539b-322">no</span></span>             | <span data-ttu-id="7539b-323">non</span><span class="sxs-lookup"><span data-stu-id="7539b-323">no</span></span>               |
| <span data-ttu-id="7539b-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="7539b-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="7539b-325">non</span><span class="sxs-lookup"><span data-stu-id="7539b-325">no</span></span>             | <span data-ttu-id="7539b-326">non</span><span class="sxs-lookup"><span data-stu-id="7539b-326">no</span></span>               |
| <span data-ttu-id="7539b-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="7539b-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="7539b-328">non</span><span class="sxs-lookup"><span data-stu-id="7539b-328">no</span></span>             | <span data-ttu-id="7539b-329">non</span><span class="sxs-lookup"><span data-stu-id="7539b-329">no</span></span>               |
| <span data-ttu-id="7539b-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="7539b-330">msdyn_summary</span></span>                          | <span data-ttu-id="7539b-331">non</span><span class="sxs-lookup"><span data-stu-id="7539b-331">no</span></span>             | <span data-ttu-id="7539b-332">non</span><span class="sxs-lookup"><span data-stu-id="7539b-332">no</span></span>               |
| <span data-ttu-id="7539b-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="7539b-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="7539b-334">non</span><span class="sxs-lookup"><span data-stu-id="7539b-334">no</span></span>             | <span data-ttu-id="7539b-335">non</span><span class="sxs-lookup"><span data-stu-id="7539b-335">no</span></span>               |
| <span data-ttu-id="7539b-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="7539b-337">non</span><span class="sxs-lookup"><span data-stu-id="7539b-337">no</span></span>             | <span data-ttu-id="7539b-338">non</span><span class="sxs-lookup"><span data-stu-id="7539b-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="7539b-339">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="7539b-339">Project task dependency</span></span>

| <span data-ttu-id="7539b-340">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="7539b-340">**Logical name**</span></span>              | <span data-ttu-id="7539b-341">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="7539b-341">**Can create**</span></span> | <span data-ttu-id="7539b-342">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="7539b-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="7539b-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="7539b-343">msdyn_linktype</span></span>                | <span data-ttu-id="7539b-344">non</span><span class="sxs-lookup"><span data-stu-id="7539b-344">no</span></span>             | <span data-ttu-id="7539b-345">non</span><span class="sxs-lookup"><span data-stu-id="7539b-345">no</span></span>           |
| <span data-ttu-id="7539b-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="7539b-346">msdyn_linktypename</span></span>            | <span data-ttu-id="7539b-347">non</span><span class="sxs-lookup"><span data-stu-id="7539b-347">no</span></span>             | <span data-ttu-id="7539b-348">non</span><span class="sxs-lookup"><span data-stu-id="7539b-348">no</span></span>           |
| <span data-ttu-id="7539b-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="7539b-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="7539b-350">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-350">yes</span></span>            | <span data-ttu-id="7539b-351">non</span><span class="sxs-lookup"><span data-stu-id="7539b-351">no</span></span>           |
| <span data-ttu-id="7539b-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="7539b-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="7539b-353">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-353">yes</span></span>            | <span data-ttu-id="7539b-354">non</span><span class="sxs-lookup"><span data-stu-id="7539b-354">no</span></span>           |
| <span data-ttu-id="7539b-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7539b-355">msdyn_project</span></span>                 | <span data-ttu-id="7539b-356">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-356">yes</span></span>            | <span data-ttu-id="7539b-357">non</span><span class="sxs-lookup"><span data-stu-id="7539b-357">no</span></span>           |
| <span data-ttu-id="7539b-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="7539b-358">msdyn_projectname</span></span>             | <span data-ttu-id="7539b-359">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-359">yes</span></span>            | <span data-ttu-id="7539b-360">non</span><span class="sxs-lookup"><span data-stu-id="7539b-360">no</span></span>           |
| <span data-ttu-id="7539b-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="7539b-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="7539b-362">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-362">yes</span></span>            | <span data-ttu-id="7539b-363">non</span><span class="sxs-lookup"><span data-stu-id="7539b-363">no</span></span>           |
| <span data-ttu-id="7539b-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="7539b-364">msdyn_successortask</span></span>           | <span data-ttu-id="7539b-365">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-365">yes</span></span>            | <span data-ttu-id="7539b-366">non</span><span class="sxs-lookup"><span data-stu-id="7539b-366">no</span></span>           |
| <span data-ttu-id="7539b-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="7539b-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="7539b-368">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-368">yes</span></span>            | <span data-ttu-id="7539b-369">non</span><span class="sxs-lookup"><span data-stu-id="7539b-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="7539b-370">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="7539b-370">Resource assignment</span></span>

| <span data-ttu-id="7539b-371">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="7539b-371">**Logical name**</span></span>             | <span data-ttu-id="7539b-372">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="7539b-372">**Can create**</span></span> | <span data-ttu-id="7539b-373">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="7539b-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="7539b-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="7539b-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="7539b-375">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-375">yes</span></span>            | <span data-ttu-id="7539b-376">non</span><span class="sxs-lookup"><span data-stu-id="7539b-376">no</span></span>           |
| <span data-ttu-id="7539b-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="7539b-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="7539b-378">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-378">yes</span></span>            | <span data-ttu-id="7539b-379">non</span><span class="sxs-lookup"><span data-stu-id="7539b-379">no</span></span>           |
| <span data-ttu-id="7539b-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="7539b-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="7539b-381">non</span><span class="sxs-lookup"><span data-stu-id="7539b-381">no</span></span>             | <span data-ttu-id="7539b-382">non</span><span class="sxs-lookup"><span data-stu-id="7539b-382">no</span></span>           |
| <span data-ttu-id="7539b-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="7539b-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="7539b-384">non</span><span class="sxs-lookup"><span data-stu-id="7539b-384">no</span></span>             | <span data-ttu-id="7539b-385">non</span><span class="sxs-lookup"><span data-stu-id="7539b-385">no</span></span>           |
| <span data-ttu-id="7539b-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="7539b-386">msdyn_committype</span></span>             | <span data-ttu-id="7539b-387">non</span><span class="sxs-lookup"><span data-stu-id="7539b-387">no</span></span>             | <span data-ttu-id="7539b-388">non</span><span class="sxs-lookup"><span data-stu-id="7539b-388">no</span></span>           |
| <span data-ttu-id="7539b-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="7539b-389">msdyn_committypename</span></span>         | <span data-ttu-id="7539b-390">non</span><span class="sxs-lookup"><span data-stu-id="7539b-390">no</span></span>             | <span data-ttu-id="7539b-391">non</span><span class="sxs-lookup"><span data-stu-id="7539b-391">no</span></span>           |
| <span data-ttu-id="7539b-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7539b-392">msdyn_effort</span></span>                 | <span data-ttu-id="7539b-393">non</span><span class="sxs-lookup"><span data-stu-id="7539b-393">no</span></span>             | <span data-ttu-id="7539b-394">non</span><span class="sxs-lookup"><span data-stu-id="7539b-394">no</span></span>           |
| <span data-ttu-id="7539b-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7539b-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="7539b-396">non</span><span class="sxs-lookup"><span data-stu-id="7539b-396">no</span></span>             | <span data-ttu-id="7539b-397">non</span><span class="sxs-lookup"><span data-stu-id="7539b-397">no</span></span>           |
| <span data-ttu-id="7539b-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7539b-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="7539b-399">non</span><span class="sxs-lookup"><span data-stu-id="7539b-399">no</span></span>             | <span data-ttu-id="7539b-400">non</span><span class="sxs-lookup"><span data-stu-id="7539b-400">no</span></span>           |
| <span data-ttu-id="7539b-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7539b-401">msdyn_finish</span></span>                 | <span data-ttu-id="7539b-402">non</span><span class="sxs-lookup"><span data-stu-id="7539b-402">no</span></span>             | <span data-ttu-id="7539b-403">non</span><span class="sxs-lookup"><span data-stu-id="7539b-403">no</span></span>           |
| <span data-ttu-id="7539b-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7539b-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="7539b-405">non</span><span class="sxs-lookup"><span data-stu-id="7539b-405">no</span></span>             | <span data-ttu-id="7539b-406">non</span><span class="sxs-lookup"><span data-stu-id="7539b-406">no</span></span>           |
| <span data-ttu-id="7539b-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="7539b-408">non</span><span class="sxs-lookup"><span data-stu-id="7539b-408">no</span></span>             | <span data-ttu-id="7539b-409">non</span><span class="sxs-lookup"><span data-stu-id="7539b-409">no</span></span>           |
| <span data-ttu-id="7539b-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="7539b-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="7539b-411">non</span><span class="sxs-lookup"><span data-stu-id="7539b-411">no</span></span>             | <span data-ttu-id="7539b-412">non</span><span class="sxs-lookup"><span data-stu-id="7539b-412">no</span></span>           |
| <span data-ttu-id="7539b-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7539b-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="7539b-414">non</span><span class="sxs-lookup"><span data-stu-id="7539b-414">no</span></span>             | <span data-ttu-id="7539b-415">non</span><span class="sxs-lookup"><span data-stu-id="7539b-415">no</span></span>           |
| <span data-ttu-id="7539b-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="7539b-417">non</span><span class="sxs-lookup"><span data-stu-id="7539b-417">no</span></span>             | <span data-ttu-id="7539b-418">non</span><span class="sxs-lookup"><span data-stu-id="7539b-418">no</span></span>           |
| <span data-ttu-id="7539b-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="7539b-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="7539b-420">non</span><span class="sxs-lookup"><span data-stu-id="7539b-420">no</span></span>             | <span data-ttu-id="7539b-421">non</span><span class="sxs-lookup"><span data-stu-id="7539b-421">no</span></span>           |
| <span data-ttu-id="7539b-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="7539b-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="7539b-423">non</span><span class="sxs-lookup"><span data-stu-id="7539b-423">no</span></span>             | <span data-ttu-id="7539b-424">non</span><span class="sxs-lookup"><span data-stu-id="7539b-424">no</span></span>           |
| <span data-ttu-id="7539b-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="7539b-425">msdyn_projectid</span></span>              | <span data-ttu-id="7539b-426">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-426">yes</span></span>            | <span data-ttu-id="7539b-427">non</span><span class="sxs-lookup"><span data-stu-id="7539b-427">no</span></span>           |
| <span data-ttu-id="7539b-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="7539b-428">msdyn_projectidname</span></span>          | <span data-ttu-id="7539b-429">non</span><span class="sxs-lookup"><span data-stu-id="7539b-429">no</span></span>             | <span data-ttu-id="7539b-430">non</span><span class="sxs-lookup"><span data-stu-id="7539b-430">no</span></span>           |
| <span data-ttu-id="7539b-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="7539b-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="7539b-432">non</span><span class="sxs-lookup"><span data-stu-id="7539b-432">no</span></span>             | <span data-ttu-id="7539b-433">non</span><span class="sxs-lookup"><span data-stu-id="7539b-433">no</span></span>           |
| <span data-ttu-id="7539b-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="7539b-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="7539b-435">non</span><span class="sxs-lookup"><span data-stu-id="7539b-435">no</span></span>             | <span data-ttu-id="7539b-436">non</span><span class="sxs-lookup"><span data-stu-id="7539b-436">no</span></span>           |
| <span data-ttu-id="7539b-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7539b-437">msdyn_start</span></span>                  | <span data-ttu-id="7539b-438">non</span><span class="sxs-lookup"><span data-stu-id="7539b-438">no</span></span>             | <span data-ttu-id="7539b-439">non</span><span class="sxs-lookup"><span data-stu-id="7539b-439">no</span></span>           |
| <span data-ttu-id="7539b-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="7539b-440">msdyn_taskid</span></span>                 | <span data-ttu-id="7539b-441">non</span><span class="sxs-lookup"><span data-stu-id="7539b-441">no</span></span>             | <span data-ttu-id="7539b-442">non</span><span class="sxs-lookup"><span data-stu-id="7539b-442">no</span></span>           |
| <span data-ttu-id="7539b-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="7539b-443">msdyn_taskidname</span></span>             | <span data-ttu-id="7539b-444">non</span><span class="sxs-lookup"><span data-stu-id="7539b-444">no</span></span>             | <span data-ttu-id="7539b-445">non</span><span class="sxs-lookup"><span data-stu-id="7539b-445">no</span></span>           |
| <span data-ttu-id="7539b-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="7539b-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="7539b-447">non</span><span class="sxs-lookup"><span data-stu-id="7539b-447">no</span></span>             | <span data-ttu-id="7539b-448">non</span><span class="sxs-lookup"><span data-stu-id="7539b-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="7539b-449">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="7539b-449">Project team member</span></span>

| <span data-ttu-id="7539b-450">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="7539b-450">**Logical name**</span></span>                                 | <span data-ttu-id="7539b-451">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="7539b-451">**Can create**</span></span> | <span data-ttu-id="7539b-452">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="7539b-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="7539b-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="7539b-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="7539b-454">non</span><span class="sxs-lookup"><span data-stu-id="7539b-454">no</span></span>             | <span data-ttu-id="7539b-455">non</span><span class="sxs-lookup"><span data-stu-id="7539b-455">no</span></span>           |
| <span data-ttu-id="7539b-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="7539b-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="7539b-457">non</span><span class="sxs-lookup"><span data-stu-id="7539b-457">no</span></span>             | <span data-ttu-id="7539b-458">non</span><span class="sxs-lookup"><span data-stu-id="7539b-458">no</span></span>           |
| <span data-ttu-id="7539b-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="7539b-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="7539b-460">non</span><span class="sxs-lookup"><span data-stu-id="7539b-460">no</span></span>             | <span data-ttu-id="7539b-461">non</span><span class="sxs-lookup"><span data-stu-id="7539b-461">no</span></span>           |
| <span data-ttu-id="7539b-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="7539b-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="7539b-463">non</span><span class="sxs-lookup"><span data-stu-id="7539b-463">no</span></span>             | <span data-ttu-id="7539b-464">non</span><span class="sxs-lookup"><span data-stu-id="7539b-464">no</span></span>           |
| <span data-ttu-id="7539b-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7539b-465">msdyn_effort</span></span>                                     | <span data-ttu-id="7539b-466">non</span><span class="sxs-lookup"><span data-stu-id="7539b-466">no</span></span>             | <span data-ttu-id="7539b-467">non</span><span class="sxs-lookup"><span data-stu-id="7539b-467">no</span></span>           |
| <span data-ttu-id="7539b-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7539b-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="7539b-469">non</span><span class="sxs-lookup"><span data-stu-id="7539b-469">no</span></span>             | <span data-ttu-id="7539b-470">non</span><span class="sxs-lookup"><span data-stu-id="7539b-470">no</span></span>           |
| <span data-ttu-id="7539b-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7539b-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="7539b-472">non</span><span class="sxs-lookup"><span data-stu-id="7539b-472">no</span></span>             | <span data-ttu-id="7539b-473">non</span><span class="sxs-lookup"><span data-stu-id="7539b-473">no</span></span>           |
| <span data-ttu-id="7539b-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7539b-474">msdyn_finish</span></span>                                     | <span data-ttu-id="7539b-475">non</span><span class="sxs-lookup"><span data-stu-id="7539b-475">no</span></span>             | <span data-ttu-id="7539b-476">non</span><span class="sxs-lookup"><span data-stu-id="7539b-476">no</span></span>           |
| <span data-ttu-id="7539b-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="7539b-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="7539b-478">non</span><span class="sxs-lookup"><span data-stu-id="7539b-478">no</span></span>             | <span data-ttu-id="7539b-479">non</span><span class="sxs-lookup"><span data-stu-id="7539b-479">no</span></span>           |
| <span data-ttu-id="7539b-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="7539b-480">msdyn_hours</span></span>                                      | <span data-ttu-id="7539b-481">non</span><span class="sxs-lookup"><span data-stu-id="7539b-481">no</span></span>             | <span data-ttu-id="7539b-482">non</span><span class="sxs-lookup"><span data-stu-id="7539b-482">no</span></span>           |
| <span data-ttu-id="7539b-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="7539b-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="7539b-484">non</span><span class="sxs-lookup"><span data-stu-id="7539b-484">no</span></span>             | <span data-ttu-id="7539b-485">non</span><span class="sxs-lookup"><span data-stu-id="7539b-485">no</span></span>           |
| <span data-ttu-id="7539b-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="7539b-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="7539b-487">non</span><span class="sxs-lookup"><span data-stu-id="7539b-487">no</span></span>             | <span data-ttu-id="7539b-488">non</span><span class="sxs-lookup"><span data-stu-id="7539b-488">no</span></span>           |
| <span data-ttu-id="7539b-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7539b-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="7539b-490">non</span><span class="sxs-lookup"><span data-stu-id="7539b-490">no</span></span>             | <span data-ttu-id="7539b-491">non</span><span class="sxs-lookup"><span data-stu-id="7539b-491">no</span></span>           |
| <span data-ttu-id="7539b-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="7539b-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="7539b-493">non</span><span class="sxs-lookup"><span data-stu-id="7539b-493">no</span></span>             | <span data-ttu-id="7539b-494">non</span><span class="sxs-lookup"><span data-stu-id="7539b-494">no</span></span>           |
| <span data-ttu-id="7539b-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="7539b-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="7539b-496">non</span><span class="sxs-lookup"><span data-stu-id="7539b-496">no</span></span>             | <span data-ttu-id="7539b-497">non</span><span class="sxs-lookup"><span data-stu-id="7539b-497">no</span></span>           |
| <span data-ttu-id="7539b-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="7539b-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="7539b-499">non</span><span class="sxs-lookup"><span data-stu-id="7539b-499">no</span></span>             | <span data-ttu-id="7539b-500">non</span><span class="sxs-lookup"><span data-stu-id="7539b-500">no</span></span>           |
| <span data-ttu-id="7539b-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7539b-501">msdyn_start</span></span>                                      | <span data-ttu-id="7539b-502">non</span><span class="sxs-lookup"><span data-stu-id="7539b-502">no</span></span>             | <span data-ttu-id="7539b-503">non</span><span class="sxs-lookup"><span data-stu-id="7539b-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="7539b-504">Project</span><span class="sxs-lookup"><span data-stu-id="7539b-504">Project</span></span>

| <span data-ttu-id="7539b-505">**Nom logique**</span><span class="sxs-lookup"><span data-stu-id="7539b-505">**Logical name**</span></span>                       | <span data-ttu-id="7539b-506">**Peut créer**</span><span class="sxs-lookup"><span data-stu-id="7539b-506">**Can create**</span></span> | <span data-ttu-id="7539b-507">**Peut modifier**</span><span class="sxs-lookup"><span data-stu-id="7539b-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="7539b-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="7539b-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="7539b-509">non</span><span class="sxs-lookup"><span data-stu-id="7539b-509">no</span></span>             | <span data-ttu-id="7539b-510">non</span><span class="sxs-lookup"><span data-stu-id="7539b-510">no</span></span>           |
| <span data-ttu-id="7539b-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="7539b-512">non</span><span class="sxs-lookup"><span data-stu-id="7539b-512">no</span></span>             | <span data-ttu-id="7539b-513">non</span><span class="sxs-lookup"><span data-stu-id="7539b-513">no</span></span>           |
| <span data-ttu-id="7539b-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="7539b-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="7539b-515">non</span><span class="sxs-lookup"><span data-stu-id="7539b-515">no</span></span>             | <span data-ttu-id="7539b-516">non</span><span class="sxs-lookup"><span data-stu-id="7539b-516">no</span></span>           |
| <span data-ttu-id="7539b-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="7539b-518">non</span><span class="sxs-lookup"><span data-stu-id="7539b-518">no</span></span>             | <span data-ttu-id="7539b-519">non</span><span class="sxs-lookup"><span data-stu-id="7539b-519">no</span></span>           |
| <span data-ttu-id="7539b-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7539b-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="7539b-521">non</span><span class="sxs-lookup"><span data-stu-id="7539b-521">no</span></span>             | <span data-ttu-id="7539b-522">non</span><span class="sxs-lookup"><span data-stu-id="7539b-522">no</span></span>           |
| <span data-ttu-id="7539b-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7539b-524">non</span><span class="sxs-lookup"><span data-stu-id="7539b-524">no</span></span>             | <span data-ttu-id="7539b-525">non</span><span class="sxs-lookup"><span data-stu-id="7539b-525">no</span></span>           |
| <span data-ttu-id="7539b-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="7539b-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="7539b-527">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-527">yes</span></span>            | <span data-ttu-id="7539b-528">non</span><span class="sxs-lookup"><span data-stu-id="7539b-528">no</span></span>           |
| <span data-ttu-id="7539b-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7539b-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="7539b-530">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-530">yes</span></span>            | <span data-ttu-id="7539b-531">non</span><span class="sxs-lookup"><span data-stu-id="7539b-531">no</span></span>           |
| <span data-ttu-id="7539b-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7539b-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="7539b-533">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-533">yes</span></span>            | <span data-ttu-id="7539b-534">non</span><span class="sxs-lookup"><span data-stu-id="7539b-534">no</span></span>           |
| <span data-ttu-id="7539b-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="7539b-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="7539b-536">non</span><span class="sxs-lookup"><span data-stu-id="7539b-536">no</span></span>             | <span data-ttu-id="7539b-537">non</span><span class="sxs-lookup"><span data-stu-id="7539b-537">no</span></span>           |
| <span data-ttu-id="7539b-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7539b-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="7539b-539">non</span><span class="sxs-lookup"><span data-stu-id="7539b-539">no</span></span>             | <span data-ttu-id="7539b-540">non</span><span class="sxs-lookup"><span data-stu-id="7539b-540">no</span></span>           |
| <span data-ttu-id="7539b-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7539b-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="7539b-542">non</span><span class="sxs-lookup"><span data-stu-id="7539b-542">no</span></span>             | <span data-ttu-id="7539b-543">non</span><span class="sxs-lookup"><span data-stu-id="7539b-543">no</span></span>           |
| <span data-ttu-id="7539b-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="7539b-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="7539b-545">non</span><span class="sxs-lookup"><span data-stu-id="7539b-545">no</span></span>             | <span data-ttu-id="7539b-546">non</span><span class="sxs-lookup"><span data-stu-id="7539b-546">no</span></span>           |
| <span data-ttu-id="7539b-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="7539b-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="7539b-548">non</span><span class="sxs-lookup"><span data-stu-id="7539b-548">no</span></span>             | <span data-ttu-id="7539b-549">non</span><span class="sxs-lookup"><span data-stu-id="7539b-549">no</span></span>           |
| <span data-ttu-id="7539b-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="7539b-550">msdyn_duration</span></span>                         | <span data-ttu-id="7539b-551">non</span><span class="sxs-lookup"><span data-stu-id="7539b-551">no</span></span>             | <span data-ttu-id="7539b-552">non</span><span class="sxs-lookup"><span data-stu-id="7539b-552">no</span></span>           |
| <span data-ttu-id="7539b-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7539b-553">msdyn_effort</span></span>                           | <span data-ttu-id="7539b-554">non</span><span class="sxs-lookup"><span data-stu-id="7539b-554">no</span></span>             | <span data-ttu-id="7539b-555">non</span><span class="sxs-lookup"><span data-stu-id="7539b-555">no</span></span>           |
| <span data-ttu-id="7539b-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7539b-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7539b-557">non</span><span class="sxs-lookup"><span data-stu-id="7539b-557">no</span></span>             | <span data-ttu-id="7539b-558">non</span><span class="sxs-lookup"><span data-stu-id="7539b-558">no</span></span>           |
| <span data-ttu-id="7539b-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7539b-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="7539b-560">non</span><span class="sxs-lookup"><span data-stu-id="7539b-560">no</span></span>             | <span data-ttu-id="7539b-561">non</span><span class="sxs-lookup"><span data-stu-id="7539b-561">no</span></span>           |
| <span data-ttu-id="7539b-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7539b-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="7539b-563">non</span><span class="sxs-lookup"><span data-stu-id="7539b-563">no</span></span>             | <span data-ttu-id="7539b-564">non</span><span class="sxs-lookup"><span data-stu-id="7539b-564">no</span></span>           |
| <span data-ttu-id="7539b-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7539b-565">msdyn_finish</span></span>                           | <span data-ttu-id="7539b-566">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-566">yes</span></span>            | <span data-ttu-id="7539b-567">oui</span><span class="sxs-lookup"><span data-stu-id="7539b-567">yes</span></span>          |
| <span data-ttu-id="7539b-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="7539b-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="7539b-569">non</span><span class="sxs-lookup"><span data-stu-id="7539b-569">no</span></span>             | <span data-ttu-id="7539b-570">non</span><span class="sxs-lookup"><span data-stu-id="7539b-570">no</span></span>           |
| <span data-ttu-id="7539b-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="7539b-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="7539b-572">non</span><span class="sxs-lookup"><span data-stu-id="7539b-572">no</span></span>             | <span data-ttu-id="7539b-573">non</span><span class="sxs-lookup"><span data-stu-id="7539b-573">no</span></span>           |
| <span data-ttu-id="7539b-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="7539b-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="7539b-575">non</span><span class="sxs-lookup"><span data-stu-id="7539b-575">no</span></span>             | <span data-ttu-id="7539b-576">non</span><span class="sxs-lookup"><span data-stu-id="7539b-576">no</span></span>           |
| <span data-ttu-id="7539b-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="7539b-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="7539b-578">non</span><span class="sxs-lookup"><span data-stu-id="7539b-578">no</span></span>             | <span data-ttu-id="7539b-579">non</span><span class="sxs-lookup"><span data-stu-id="7539b-579">no</span></span>           |
| <span data-ttu-id="7539b-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="7539b-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="7539b-581">non</span><span class="sxs-lookup"><span data-stu-id="7539b-581">no</span></span>             | <span data-ttu-id="7539b-582">non</span><span class="sxs-lookup"><span data-stu-id="7539b-582">no</span></span>           |
| <span data-ttu-id="7539b-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="7539b-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="7539b-584">non</span><span class="sxs-lookup"><span data-stu-id="7539b-584">no</span></span>             | <span data-ttu-id="7539b-585">non</span><span class="sxs-lookup"><span data-stu-id="7539b-585">no</span></span>           |
| <span data-ttu-id="7539b-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="7539b-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="7539b-587">non</span><span class="sxs-lookup"><span data-stu-id="7539b-587">no</span></span>             | <span data-ttu-id="7539b-588">non</span><span class="sxs-lookup"><span data-stu-id="7539b-588">no</span></span>           |
| <span data-ttu-id="7539b-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="7539b-590">non</span><span class="sxs-lookup"><span data-stu-id="7539b-590">no</span></span>             | <span data-ttu-id="7539b-591">non</span><span class="sxs-lookup"><span data-stu-id="7539b-591">no</span></span>           |
| <span data-ttu-id="7539b-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="7539b-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="7539b-593">non</span><span class="sxs-lookup"><span data-stu-id="7539b-593">no</span></span>             | <span data-ttu-id="7539b-594">non</span><span class="sxs-lookup"><span data-stu-id="7539b-594">no</span></span>           |
| <span data-ttu-id="7539b-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="7539b-596">non</span><span class="sxs-lookup"><span data-stu-id="7539b-596">no</span></span>             | <span data-ttu-id="7539b-597">non</span><span class="sxs-lookup"><span data-stu-id="7539b-597">no</span></span>           |
| <span data-ttu-id="7539b-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7539b-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7539b-599">non</span><span class="sxs-lookup"><span data-stu-id="7539b-599">no</span></span>             | <span data-ttu-id="7539b-600">non</span><span class="sxs-lookup"><span data-stu-id="7539b-600">no</span></span>           |
| <span data-ttu-id="7539b-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7539b-602">non</span><span class="sxs-lookup"><span data-stu-id="7539b-602">no</span></span>             | <span data-ttu-id="7539b-603">non</span><span class="sxs-lookup"><span data-stu-id="7539b-603">no</span></span>           |
| <span data-ttu-id="7539b-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7539b-604">msdyn_progress</span></span>                         | <span data-ttu-id="7539b-605">non</span><span class="sxs-lookup"><span data-stu-id="7539b-605">no</span></span>             | <span data-ttu-id="7539b-606">non</span><span class="sxs-lookup"><span data-stu-id="7539b-606">no</span></span>           |
| <span data-ttu-id="7539b-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7539b-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7539b-608">non</span><span class="sxs-lookup"><span data-stu-id="7539b-608">no</span></span>             | <span data-ttu-id="7539b-609">non</span><span class="sxs-lookup"><span data-stu-id="7539b-609">no</span></span>           |
| <span data-ttu-id="7539b-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7539b-611">non</span><span class="sxs-lookup"><span data-stu-id="7539b-611">no</span></span>             | <span data-ttu-id="7539b-612">non</span><span class="sxs-lookup"><span data-stu-id="7539b-612">no</span></span>           |
| <span data-ttu-id="7539b-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7539b-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7539b-614">non</span><span class="sxs-lookup"><span data-stu-id="7539b-614">no</span></span>             | <span data-ttu-id="7539b-615">non</span><span class="sxs-lookup"><span data-stu-id="7539b-615">no</span></span>           |
| <span data-ttu-id="7539b-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7539b-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7539b-617">non</span><span class="sxs-lookup"><span data-stu-id="7539b-617">no</span></span>             | <span data-ttu-id="7539b-618">non</span><span class="sxs-lookup"><span data-stu-id="7539b-618">no</span></span>           |
| <span data-ttu-id="7539b-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="7539b-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="7539b-620">non</span><span class="sxs-lookup"><span data-stu-id="7539b-620">no</span></span>             | <span data-ttu-id="7539b-621">non</span><span class="sxs-lookup"><span data-stu-id="7539b-621">no</span></span>           |
| <span data-ttu-id="7539b-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="7539b-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="7539b-623">non</span><span class="sxs-lookup"><span data-stu-id="7539b-623">no</span></span>             | <span data-ttu-id="7539b-624">non</span><span class="sxs-lookup"><span data-stu-id="7539b-624">no</span></span>           |
| <span data-ttu-id="7539b-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7539b-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="7539b-626">non</span><span class="sxs-lookup"><span data-stu-id="7539b-626">no</span></span>             | <span data-ttu-id="7539b-627">non</span><span class="sxs-lookup"><span data-stu-id="7539b-627">no</span></span>           |
| <span data-ttu-id="7539b-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="7539b-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="7539b-629">non</span><span class="sxs-lookup"><span data-stu-id="7539b-629">no</span></span>             | <span data-ttu-id="7539b-630">non</span><span class="sxs-lookup"><span data-stu-id="7539b-630">no</span></span>           |
| <span data-ttu-id="7539b-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7539b-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7539b-632">non</span><span class="sxs-lookup"><span data-stu-id="7539b-632">no</span></span>             | <span data-ttu-id="7539b-633">non</span><span class="sxs-lookup"><span data-stu-id="7539b-633">no</span></span>           |
| <span data-ttu-id="7539b-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7539b-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7539b-635">non</span><span class="sxs-lookup"><span data-stu-id="7539b-635">no</span></span>             | <span data-ttu-id="7539b-636">non</span><span class="sxs-lookup"><span data-stu-id="7539b-636">no</span></span>           |
| <span data-ttu-id="7539b-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="7539b-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="7539b-638">non</span><span class="sxs-lookup"><span data-stu-id="7539b-638">no</span></span>             | <span data-ttu-id="7539b-639">non</span><span class="sxs-lookup"><span data-stu-id="7539b-639">no</span></span>           |
| <span data-ttu-id="7539b-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="7539b-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="7539b-641">non</span><span class="sxs-lookup"><span data-stu-id="7539b-641">no</span></span>             | <span data-ttu-id="7539b-642">non</span><span class="sxs-lookup"><span data-stu-id="7539b-642">no</span></span>           |
| <span data-ttu-id="7539b-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7539b-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7539b-644">non</span><span class="sxs-lookup"><span data-stu-id="7539b-644">no</span></span>             | <span data-ttu-id="7539b-645">non</span><span class="sxs-lookup"><span data-stu-id="7539b-645">no</span></span>           |
| <span data-ttu-id="7539b-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="7539b-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="7539b-647">non</span><span class="sxs-lookup"><span data-stu-id="7539b-647">no</span></span>             | <span data-ttu-id="7539b-648">non</span><span class="sxs-lookup"><span data-stu-id="7539b-648">no</span></span>           |
| <span data-ttu-id="7539b-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="7539b-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="7539b-650">non</span><span class="sxs-lookup"><span data-stu-id="7539b-650">no</span></span>             | <span data-ttu-id="7539b-651">non</span><span class="sxs-lookup"><span data-stu-id="7539b-651">no</span></span>           |
| <span data-ttu-id="7539b-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="7539b-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="7539b-653">non</span><span class="sxs-lookup"><span data-stu-id="7539b-653">no</span></span>             | <span data-ttu-id="7539b-654">non</span><span class="sxs-lookup"><span data-stu-id="7539b-654">no</span></span>           |
| <span data-ttu-id="7539b-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="7539b-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="7539b-656">non</span><span class="sxs-lookup"><span data-stu-id="7539b-656">no</span></span>             | <span data-ttu-id="7539b-657">non</span><span class="sxs-lookup"><span data-stu-id="7539b-657">no</span></span>           |
| <span data-ttu-id="7539b-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="7539b-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="7539b-659">non</span><span class="sxs-lookup"><span data-stu-id="7539b-659">no</span></span>             | <span data-ttu-id="7539b-660">non</span><span class="sxs-lookup"><span data-stu-id="7539b-660">no</span></span>           |
| <span data-ttu-id="7539b-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="7539b-662">non</span><span class="sxs-lookup"><span data-stu-id="7539b-662">no</span></span>             | <span data-ttu-id="7539b-663">non</span><span class="sxs-lookup"><span data-stu-id="7539b-663">no</span></span>           |
| <span data-ttu-id="7539b-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="7539b-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="7539b-665">non</span><span class="sxs-lookup"><span data-stu-id="7539b-665">no</span></span>             | <span data-ttu-id="7539b-666">non</span><span class="sxs-lookup"><span data-stu-id="7539b-666">no</span></span>           |
| <span data-ttu-id="7539b-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7539b-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="7539b-668">non</span><span class="sxs-lookup"><span data-stu-id="7539b-668">no</span></span>             | <span data-ttu-id="7539b-669">non</span><span class="sxs-lookup"><span data-stu-id="7539b-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="7539b-670">Limitations et problèmes connus</span><span class="sxs-lookup"><span data-stu-id="7539b-670">Limitations and known issues</span></span>
<span data-ttu-id="7539b-671">Voici une liste des limitations et des problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="7539b-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="7539b-672">Les API de planification de projets ne peuvent être utilisées que par les **Utilisateurs disposant d’une licence Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="7539b-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="7539b-673">Elles ne peuvent pas être utilisées par :</span><span class="sxs-lookup"><span data-stu-id="7539b-673">They can't be used by:</span></span>
    - <span data-ttu-id="7539b-674">Utilisateurs de l’application</span><span class="sxs-lookup"><span data-stu-id="7539b-674">Application users</span></span>
    - <span data-ttu-id="7539b-675">Utilisateurs du système</span><span class="sxs-lookup"><span data-stu-id="7539b-675">System users</span></span>
    - <span data-ttu-id="7539b-676">Utilisateurs de l’intégration</span><span class="sxs-lookup"><span data-stu-id="7539b-676">Integration users</span></span>
    - <span data-ttu-id="7539b-677">Autres utilisateurs ne disposant pas de la licence requise</span><span class="sxs-lookup"><span data-stu-id="7539b-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="7539b-678">Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.</span><span class="sxs-lookup"><span data-stu-id="7539b-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="7539b-679">Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.</span><span class="sxs-lookup"><span data-stu-id="7539b-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="7539b-680">Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.</span><span class="sxs-lookup"><span data-stu-id="7539b-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="7539b-681">Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="7539b-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="7539b-682">Limites des projets et des tâches</span><span class="sxs-lookup"><span data-stu-id="7539b-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="7539b-683">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="7539b-683">Error handling</span></span>

   - <span data-ttu-id="7539b-684">Pour consulter les erreurs générées par les ensembles d’opérations, accédez à **Paramètres** \> **Intégration de la planification** \> **Ensembles d’opérations**.</span><span class="sxs-lookup"><span data-stu-id="7539b-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="7539b-685">Pour consulter les erreurs générées par le service de planification de projets, accédez à **Paramètres** \> **Intégration de la planification** \> **Journaux d’erreurs PSS**.</span><span class="sxs-lookup"><span data-stu-id="7539b-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="7539b-686">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="7539b-686">Sample scenario</span></span>

<span data-ttu-id="7539b-687">Dans ce scénario, vous allez créer un projet, un membre de l’équipe, quatre tâches et deux affectations de ressources.</span><span class="sxs-lookup"><span data-stu-id="7539b-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="7539b-688">Ensuite, vous allez mettre à jour une tâche, mettre à jour le projet, supprimer une tâche, supprimer une affectation de ressource et créer une dépendance de tâche.</span><span class="sxs-lookup"><span data-stu-id="7539b-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="7539b-689">Exemples supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7539b-689">Additional samples</span></span>

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
