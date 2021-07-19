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
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

> [!IMPORTANT] 
> Certaines ou toutes les fonctionnalités mentionnées dans cette rubrique sont disponibles dans le cadre d’une version préliminaire. Le contenu et les fonctionnalités sont susceptibles d’être modifiés. 

## <a name="scheduling-entities"></a>Entités de planification

Les API de planification de projets offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec les **Entités de planification**. Ces entités sont gérées via le moteur de planification de l’application Project pour le Web. Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.

Le tableau suivant fournit une liste complète des entités de planification de projets.

| Nom de l'entité  | Nom logique de l’entité |
| --- | --- |
| Project | msdyn_project |
| Tâche du projet  | msdyn_projecttask  |
| Dépendance de la tâche du projet  | msdyn_projecttaskdependency  |
| Attribution de ressource | msdyn_resourceassignment |
| Compartiment du projet  | msdyn_projectbucket |
| Membre de l’équipe du projet | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.

## <a name="project-schedule-apis"></a>API de planification de projets

Voici la liste des API de planification de projet actuelles.

- **msdyn_CreateProjectV1** : Cette API peut être utilisée pour créer un projet. Le projet et le compartiment de projet par défaut sont créés immédiatement.
- **msdyn_CreateTeamMemberV1** : Cette API peut être utilisée pour créer un membre de l’équipe de projet. L’enregistrement de membre de l’équipe est créé immédiatement.
- **msdyn_CreateOperationSetV1** : Cette API peut être utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.
- **msdyn_PSSCreateV1** : Cette API peut être utilisée pour créer une entité. L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de création.
- **msdyn_PSSUpdateV1** : Cette API peut être utilisée pour mettre à jour une entité. L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de mise à jour.
- **msdyn_PSSDeleteV1** : Cette API peut être utilisée pour supprimer une entité. L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de suppression.
- **msdyn_ExecuteOperationSetV1** : Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.

## <a name="using-project-schedule-apis-with-operationset"></a>Utilisation des API de planification de projets avec OperationSet

Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**. Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.

## <a name="supported-operations"></a>Opérations prises en charge

| Entité de planification | Créer | Mise à jour | Suppr | Remarques importantes |
| --- | --- | --- | --- | --- |
Tâche du projet | Oui | Oui | Oui | Aucun(e) |
| Dépendance de la tâche du projet | Oui | Oui | | Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour. Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé. |
| Attribution de ressource | Oui | Oui | | Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**. Les enregistrements d’attribution de ressource ne sont pas mis à jour. Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé. |
| Compartiment du projet | N/A | N/A | N/A | Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**. |
| Membre de l’équipe projet | Oui | Oui | Oui | Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**. |
| Project | Oui | Oui | N/A | Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**. |

Ces API peuvent être appelées avec des objets d’entité qui incluent des champs personnalisés.

La propriété ID est facultative. Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée. Si elle n’est pas fournie, le système la générera.

## <a name="restricted-fields"></a>Champs interdits

Les tableaux suivants définissent les champs interdits pour **Créer** et **Modifier.**

### <a name="project-task"></a>Tâche du projet

| **Nom logique**                       | **Peut créer** | **Peut modifier**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | non             | non               |
| msdyn_actualcost_base                  | non             | non               |
| msdyn_actualend                        | non             | non               |
| msdyn_actualsales                      | non             | non               |
| msdyn_actualsales_base                 | non             | non               |
| msdyn_actualstart                      | non             | non               |
| msdyn_costatcompleteestimate           | non             | non               |
| msdyn_costatcompleteestimate_base      | non             | non               |
| msdyn_costconsumptionpercentage        | non             | non               |
| msdyn_effortcompleted                  | non             | non               |
| msdyn_effortestimateatcomplete         | non             | non               |
| msdyn_iscritical                       | non             | non               |
| msdyn_iscriticalname                   | non             | non               |
| msdyn_ismanual                         | non             | non               |
| msdyn_ismanualname                     | non             | non               |
| msdyn_ismilestone                      | non             | non               |
| msdyn_ismilestonename                  | non             | non               |
| msdyn_LinkStatus                       | non             | non               |
| msdyn_linkstatusname                   | non             | non               |
| msdyn_msprojectclientid                | non             | non               |
| msdyn_plannedcost                      | non             | non               |
| msdyn_plannedcost_base                 | non             | non               |
| msdyn_plannedsales                     | non             | non               |
| msdyn_plannedsales_base                | non             | non               |
| msdyn_pluginprocessingdata             | non             | non               |
| msdyn_progress                         | non             | Non (oui pour P4W) |
| msdyn_remainingcost                    | non             | non               |
| msdyn_remainingcost_base               | non             | non               |
| msdyn_remainingsales                   | non             | non               |
| msdyn_remainingsales_base              | non             | non               |
| msdyn_requestedhours                   | non             | non               |
| msdyn_resourcecategory                 | non             | non               |
| msdyn_resourcecategoryname             | non             | non               |
| msdyn_resourceorganizationalunitid     | non             | non               |
| msdyn_resourceorganizationalunitidname | non             | non               |
| msdyn_salesconsumptionpercentage       | non             | non               |
| msdyn_salesestimateatcomplete          | non             | non               |
| msdyn_salesestimateatcomplete_base     | non             | non               |
| msdyn_salesvariance                    | non             | non               |
| msdyn_salesvariance_base               | non             | non               |
| msdyn_scheduleddurationminutes         | non             | non               |
| msdyn_scheduledend                     | non             | non               |
| msdyn_scheduledstart                   | non             | non               |
| msdyn_schedulevariance                 | non             | non               |
| msdyn_skipupdateestimateline           | non             | non               |
| msdyn_skipupdateestimatelinename       | non             | non               |
| msdyn_summary                          | non             | non               |
| msdyn_varianceofcost                   | non             | non               |
| msdyn_varianceofcost_base              | non             | non               |

### <a name="project-task-dependency"></a>Dépendance de la tâche du projet

| **Nom logique**              | **Peut créer** | **Peut modifier** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | non             | non           |
| msdyn_linktypename            | non             | non           |
| msdyn_predecessortask         | oui            | non           |
| msdyn_predecessortaskname     | oui            | non           |
| msdyn_project                 | oui            | non           |
| msdyn_projectname             | oui            | non           |
| msdyn_projecttaskdependencyid | oui            | non           |
| msdyn_successortask           | oui            | non           |
| msdyn_successortaskname       | oui            | non           |

### <a name="resource-assignment"></a>Attribution de ressource

| **Nom logique**             | **Peut créer** | **Peut modifier** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | oui            | non           |
| msdyn_bookableresourceidname | oui            | non           |
| msdyn_bookingstatusid        | non             | non           |
| msdyn_bookingstatusidname    | non             | non           |
| msdyn_committype             | non             | non           |
| msdyn_committypename         | non             | non           |
| msdyn_effort                 | non             | non           |
| msdyn_effortcompleted        | non             | non           |
| msdyn_effortremaining        | non             | non           |
| msdyn_finish                 | non             | non           |
| msdyn_plannedcost            | non             | non           |
| msdyn_plannedcost_base       | non             | non           |
| msdyn_plannedcostcontour     | non             | non           |
| msdyn_plannedsales           | non             | non           |
| msdyn_plannedsales_base      | non             | non           |
| msdyn_plannedsalescontour    | non             | non           |
| msdyn_plannedwork            | non             | non           |
| msdyn_projectid              | oui            | non           |
| msdyn_projectidname          | non             | non           |
| msdyn_projectteamid          | non             | non           |
| msdyn_projectteamidname      | non             | non           |
| msdyn_start                  | non             | non           |
| msdyn_taskid                 | non             | non           |
| msdyn_taskidname             | non             | non           |
| msdyn_userresourceid         | non             | non           |

### <a name="project-team-member"></a>Membre de l’équipe projet

| **Nom logique**                                 | **Peut créer** | **Peut modifier** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | non             | non           |
| msdyn_creategenericteammemberwithrequirementname | non             | non           |
| msdyn_deletestatus                               | non             | non           |
| msdyn_deletestatusname                           | non             | non           |
| msdyn_effort                                     | non             | non           |
| msdyn_effortcompleted                            | non             | non           |
| msdyn_effortremaining                            | non             | non           |
| msdyn_finish                                     | non             | non           |
| msdyn_hardbookedhours                            | non             | non           |
| msdyn_hours                                      | non             | non           |
| msdyn_markedfordeletiontimer                     | non             | non           |
| msdyn_markedfordeletiontimestamp                 | non             | non           |
| msdyn_msprojectclientid                          | non             | non           |
| msdyn_percentage                                 | non             | non           |
| msdyn_requiredhours                              | non             | non           |
| msdyn_softbookedhours                            | non             | non           |
| msdyn_start                                      | non             | non           |

### <a name="project"></a>Project

| **Nom logique**                       | **Peut créer** | **Peut modifier** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | non             | non           |
| msdyn_actualexpensecost_base           | non             | non           |
| msdyn_actuallaborcost                  | non             | non           |
| msdyn_actuallaborcost_base             | non             | non           |
| msdyn_actualsales                      | non             | non           |
| msdyn_actualsales_base                 | non             | non           |
| msdyn_contractlineproject              | oui            | non           |
| msdyn_contractorganizationalunitid     | oui            | non           |
| msdyn_contractorganizationalunitidname | oui            | non           |
| msdyn_costconsumption                  | non             | non           |
| msdyn_costestimateatcomplete           | non             | non           |
| msdyn_costestimateatcomplete_base      | non             | non           |
| msdyn_costvariance                     | non             | non           |
| msdyn_costvariance_base                | non             | non           |
| msdyn_duration                         | non             | non           |
| msdyn_effort                           | non             | non           |
| msdyn_effortcompleted                  | non             | non           |
| msdyn_effortestimateatcompleteeac      | non             | non           |
| msdyn_effortremaining                  | non             | non           |
| msdyn_finish                           | oui            | oui          |
| msdyn_globalrevisiontoken              | non             | non           |
| msdyn_islinkedtomsprojectclient        | non             | non           |
| msdyn_islinkedtomsprojectclientname    | non             | non           |
| msdyn_linkeddocumenturl                | non             | non           |
| msdyn_msprojectdocument                | non             | non           |
| msdyn_msprojectdocumentname            | non             | non           |
| msdyn_plannedexpensecost               | non             | non           |
| msdyn_plannedexpensecost_base          | non             | non           |
| msdyn_plannedlaborcost                 | non             | non           |
| msdyn_plannedlaborcost_base            | non             | non           |
| msdyn_plannedsales                     | non             | non           |
| msdyn_plannedsales_base                | non             | non           |
| msdyn_progress                         | non             | non           |
| msdyn_remainingcost                    | non             | non           |
| msdyn_remainingcost_base               | non             | non           |
| msdyn_remainingsales                   | non             | non           |
| msdyn_remainingsales_base              | non             | non           |
| msdyn_replaylogheader                  | non             | non           |
| msdyn_salesconsumption                 | non             | non           |
| msdyn_salesestimateatcompleteeac       | non             | non           |
| msdyn_salesestimateatcompleteeac_base  | non             | non           |
| msdyn_salesvariance                    | non             | non           |
| msdyn_salesvariance_base               | non             | non           |
| msdyn_scheduleperformance              | non             | non           |
| msdyn_scheduleperformancename          | non             | non           |
| msdyn_schedulevariance                 | non             | non           |
| msdyn_taskearlieststart                | non             | non           |
| msdyn_teamsize                         | non             | non           |
| msdyn_teamsize_date                    | non             | non           |
| msdyn_teamsize_state                   | non             | non           |
| msdyn_totalactualcost                  | non             | non           |
| msdyn_totalactualcost_base             | non             | non           |
| msdyn_totalplannedcost                 | non             | non           |
| msdyn_totalplannedcost_base            | non             | non           |


## <a name="limitations-and-known-issues"></a>Limitations et problèmes connus
Voici une liste des limitations et des problèmes connus :

- Les API de planification de projets ne peuvent être utilisées que par les **Utilisateurs disposant d’une licence Microsoft Project.** Elles ne peuvent pas être utilisées par :
    - Utilisateurs de l’application
    - Utilisateurs du système
    - Utilisateurs de l’intégration
    - Autres utilisateurs ne disposant pas de la licence requise
- Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.
- Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.
- Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.
- Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.
- [Limites des projets et des tâches](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Gestion des erreurs

   - Pour consulter les erreurs générées par les ensembles d’opérations, accédez à **Paramètres** \> **Intégration de la planification** \> **Ensembles d’opérations**.
   - Pour consulter les erreurs générées par le service de planification de projets, accédez à **Paramètres** \> **Intégration de la planification** \> **Journaux d’erreurs PSS**.

## <a name="sample-scenario"></a>Exemple de scénario

Dans ce scénario, vous allez créer un projet, un membre de l’équipe, quatre tâches et deux affectations de ressources. Ensuite, vous allez mettre à jour une tâche, mettre à jour le projet, supprimer une tâche, supprimer une affectation de ressource et créer une dépendance de tâche.

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

## <a name="additional-samples"></a>Exemples supplémentaires

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
