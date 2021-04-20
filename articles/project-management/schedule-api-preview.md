---
title: Utiliser les API de planification pour effectuer des opérations avec des entités de planification
description: Cette rubrique fournit des informations et des exemples d’utilisation des API de planification.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868126"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="3dd54-103">Utiliser les API de planification pour effectuer des opérations avec des entités de planification</span><span class="sxs-lookup"><span data-stu-id="3dd54-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="3dd54-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="3dd54-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="3dd54-105">Certaines ou toutes les fonctionnalités mentionnées dans cette rubrique sont disponibles dans le cadre d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="3dd54-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="3dd54-106">Le contenu et les fonctionnalités sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="3dd54-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="3dd54-107">Entités de planification</span><span class="sxs-lookup"><span data-stu-id="3dd54-107">Scheduling entities</span></span>

<span data-ttu-id="3dd54-108">Les API de planification offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="3dd54-109">Ces entités sont gérées via le moteur de planification de l’application Project pour le Web.</span><span class="sxs-lookup"><span data-stu-id="3dd54-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="3dd54-110">Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3dd54-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="3dd54-111">Le tableau suivant fournit une liste complète des **Entités de planification**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="3dd54-112">Nom de l'entité</span><span class="sxs-lookup"><span data-stu-id="3dd54-112">Entity name</span></span>  | <span data-ttu-id="3dd54-113">Nom logique de l’entité</span><span class="sxs-lookup"><span data-stu-id="3dd54-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="3dd54-114">Project</span><span class="sxs-lookup"><span data-stu-id="3dd54-114">Project</span></span> | <span data-ttu-id="3dd54-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="3dd54-115">msdyn_project</span></span> |
| <span data-ttu-id="3dd54-116">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-116">Project Task</span></span>  | <span data-ttu-id="3dd54-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="3dd54-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="3dd54-118">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-118">Project Task Dependency</span></span>  | <span data-ttu-id="3dd54-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="3dd54-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="3dd54-120">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="3dd54-120">Resource Assignment</span></span> | <span data-ttu-id="3dd54-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="3dd54-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="3dd54-122">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-122">Project Bucket</span></span>  | <span data-ttu-id="3dd54-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="3dd54-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="3dd54-124">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-124">Project Team Member</span></span> | <span data-ttu-id="3dd54-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="3dd54-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="3dd54-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="3dd54-126">OperationSet</span></span>

<span data-ttu-id="3dd54-127">OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="3dd54-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="3dd54-128">API de planification</span><span class="sxs-lookup"><span data-stu-id="3dd54-128">Schedule APIs</span></span>

<span data-ttu-id="3dd54-129">Voici une liste des API de planification actuelles.</span><span class="sxs-lookup"><span data-stu-id="3dd54-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="3dd54-130">**msdyn_CreateProjectV1** : Cette API peut être utilisée pour créer un projet.</span><span class="sxs-lookup"><span data-stu-id="3dd54-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="3dd54-131">Le projet et le compartiment de projet par défaut sont créés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="3dd54-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="3dd54-132">**msdyn_CreateTeamMemberV1** : Cette API peut être utilisée pour créer un membre de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="3dd54-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="3dd54-133">L’enregistrement de membre de l’équipe est créé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="3dd54-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="3dd54-134">**msdyn_CreateOperationSetV1** : Cette API peut être utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="3dd54-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="3dd54-135">**msdyn_PSSCreateV1** : Cette API peut être utilisée pour créer une entité.</span><span class="sxs-lookup"><span data-stu-id="3dd54-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="3dd54-136">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="3dd54-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="3dd54-137">**msdyn_PSSUpdateV1** : Cette API peut être utilisée pour mettre à jour une entité.</span><span class="sxs-lookup"><span data-stu-id="3dd54-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="3dd54-138">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3dd54-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="3dd54-139">**msdyn_PSSDeleteV1** : Cette API peut être utilisée pour supprimer une entité.</span><span class="sxs-lookup"><span data-stu-id="3dd54-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="3dd54-140">L’entité peut être n’importe quelle entité de planification prenant en charge l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="3dd54-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="3dd54-141">**msdyn_ExecuteOperationSetV1** : Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.</span><span class="sxs-lookup"><span data-stu-id="3dd54-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="3dd54-142">Utilisation des API de planification avec OperationSet</span><span class="sxs-lookup"><span data-stu-id="3dd54-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="3dd54-143">Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="3dd54-144">Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="3dd54-145">Opérations prises en charge</span><span class="sxs-lookup"><span data-stu-id="3dd54-145">Supported operations</span></span>

| <span data-ttu-id="3dd54-146">Entité de planification</span><span class="sxs-lookup"><span data-stu-id="3dd54-146">Scheduling entity</span></span> | <span data-ttu-id="3dd54-147">Créer</span><span class="sxs-lookup"><span data-stu-id="3dd54-147">Create</span></span> | <span data-ttu-id="3dd54-148">Mise à jour</span><span class="sxs-lookup"><span data-stu-id="3dd54-148">Update</span></span> | <span data-ttu-id="3dd54-149">Suppr</span><span class="sxs-lookup"><span data-stu-id="3dd54-149">Delete</span></span> | <span data-ttu-id="3dd54-150">Remarques importantes</span><span class="sxs-lookup"><span data-stu-id="3dd54-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="3dd54-151">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-151">Project task</span></span> | <span data-ttu-id="3dd54-152">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-152">Yes</span></span> | <span data-ttu-id="3dd54-153">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-153">Yes</span></span> | <span data-ttu-id="3dd54-154">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-154">Yes</span></span> | <span data-ttu-id="3dd54-155">Aucun(e)</span><span class="sxs-lookup"><span data-stu-id="3dd54-155">None</span></span> |
| <span data-ttu-id="3dd54-156">Dépendance de la tâche du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-156">Project task dependency</span></span> | <span data-ttu-id="3dd54-157">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-157">Yes</span></span> | <span data-ttu-id="3dd54-158">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-158">Yes</span></span> | | <span data-ttu-id="3dd54-159">Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3dd54-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="3dd54-160">Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="3dd54-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3dd54-161">Attribution de ressource</span><span class="sxs-lookup"><span data-stu-id="3dd54-161">Resource assignment</span></span> | <span data-ttu-id="3dd54-162">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-162">Yes</span></span> | <span data-ttu-id="3dd54-163">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-163">Yes</span></span> | | <span data-ttu-id="3dd54-164">Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="3dd54-165">Les enregistrements d’attribution de ressource ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3dd54-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="3dd54-166">Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.</span><span class="sxs-lookup"><span data-stu-id="3dd54-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3dd54-167">Compartiment du projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-167">Project bucket</span></span> | <span data-ttu-id="3dd54-168">N/A</span><span class="sxs-lookup"><span data-stu-id="3dd54-168">N/A</span></span> | <span data-ttu-id="3dd54-169">N/A</span><span class="sxs-lookup"><span data-stu-id="3dd54-169">N/A</span></span> | <span data-ttu-id="3dd54-170">N/A</span><span class="sxs-lookup"><span data-stu-id="3dd54-170">N/A</span></span> | <span data-ttu-id="3dd54-171">Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="3dd54-172">Membre de l’équipe projet</span><span class="sxs-lookup"><span data-stu-id="3dd54-172">Project team member</span></span> | <span data-ttu-id="3dd54-173">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-173">Yes</span></span> | <span data-ttu-id="3dd54-174">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-174">Yes</span></span> | <span data-ttu-id="3dd54-175">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-175">Yes</span></span> | <span data-ttu-id="3dd54-176">Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="3dd54-177">Project</span><span class="sxs-lookup"><span data-stu-id="3dd54-177">Project</span></span> | <span data-ttu-id="3dd54-178">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-178">Yes</span></span> | <span data-ttu-id="3dd54-179">Oui</span><span class="sxs-lookup"><span data-stu-id="3dd54-179">Yes</span></span> | <span data-ttu-id="3dd54-180">N/A</span><span class="sxs-lookup"><span data-stu-id="3dd54-180">N/A</span></span> | <span data-ttu-id="3dd54-181">Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="3dd54-182">Ces API peuvent être appelées avec des objets d’entité qui incluent des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3dd54-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="3dd54-183">La propriété ID est facultative.</span><span class="sxs-lookup"><span data-stu-id="3dd54-183">The ID property is optional.</span></span> <span data-ttu-id="3dd54-184">Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="3dd54-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="3dd54-185">Si elle n’est pas fournie, le système la générera.</span><span class="sxs-lookup"><span data-stu-id="3dd54-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="3dd54-186">Limitations et problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3dd54-186">Limitations and known issues</span></span>
<span data-ttu-id="3dd54-187">Voici une liste des limitations et des problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="3dd54-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="3dd54-188">Les API de planification ne peuvent être utilisées que par les **utilisateurs disposant d’une licence Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="3dd54-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="3dd54-189">Elles ne peuvent pas être utilisées par :</span><span class="sxs-lookup"><span data-stu-id="3dd54-189">They can't be used by:</span></span>
    - <span data-ttu-id="3dd54-190">Utilisateurs de l'application</span><span class="sxs-lookup"><span data-stu-id="3dd54-190">Application users</span></span>
    - <span data-ttu-id="3dd54-191">Utilisateurs du système</span><span class="sxs-lookup"><span data-stu-id="3dd54-191">System users</span></span>
    - <span data-ttu-id="3dd54-192">Utilisateurs de l’intégration</span><span class="sxs-lookup"><span data-stu-id="3dd54-192">Integration users</span></span>
    - <span data-ttu-id="3dd54-193">Autres utilisateurs ne disposant pas de la licence requise</span><span class="sxs-lookup"><span data-stu-id="3dd54-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="3dd54-194">Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.</span><span class="sxs-lookup"><span data-stu-id="3dd54-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="3dd54-195">Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.</span><span class="sxs-lookup"><span data-stu-id="3dd54-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="3dd54-196">Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.</span><span class="sxs-lookup"><span data-stu-id="3dd54-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="3dd54-197">Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="3dd54-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="3dd54-198">Les API de planification sont disponibles en version préliminaire publique.</span><span class="sxs-lookup"><span data-stu-id="3dd54-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="3dd54-199">L’utilisation de ces API dans un environnement de production n’est pas prise en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3dd54-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="3dd54-200">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="3dd54-200">Sample scenario</span></span>

<span data-ttu-id="3dd54-201">Dans ce scénario, vous allez créer un projet, un membre de l’équipe, quatre tâches et deux affectations de ressources.</span><span class="sxs-lookup"><span data-stu-id="3dd54-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="3dd54-202">Ensuite, vous allez mettre à jour une tâche, mettre à jour le projet, supprimer une tâche, supprimer une affectation de ressource et créer une dépendance de tâche.</span><span class="sxs-lookup"><span data-stu-id="3dd54-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="3dd54-203">Exemples supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3dd54-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
