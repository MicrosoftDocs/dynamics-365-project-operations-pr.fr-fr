---
title: Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification
description: Cet article fournit des informations et des exemples d’utilisation des API de planification de projet.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541121"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_


**Entités de planification**

Les API de planification de projets offrent la possibilité d’effectuer des opérations de création, de mise à jour et de suppression avec les **Entités de planification**. Ces entités sont gérées via le moteur de planification de l’application Project pour le Web. Les opérations de création, de mise à jour et de suppression avec des **Entités de planification** étaient restreintes dans les précédentes versions de Dynamics 365 Project Operations.

Le tableau suivant fournit une liste complète des entités de planification de projets.

| **Nom de l'entité**         | **Nom logique de l’entité**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tâche du projet            | msdyn_projecttask           |
| Dépendance de la tâche du projet | msdyn_projecttaskdependency |
| Attribution de ressource     | msdyn_resourceassignment    |
| Compartiment du projet          | msdyn_projectbucket         |
| Membre de l’équipe du projet     | msdyn_projectteam           |
| Listes de contrôle du projet      | msdyn_projectchecklist      |
| Étiquette du projet           | msdyn_projectlabel          |
| Tâche du projet à étiqueter   | msdyn_projecttasktolabel    |
| Sprint du projet          | msdyn_projectsprint         |

**OperationSet**

OperationSet est un modèle d’unité de travail qui peut être utilisé lorsque plusieurs demandes ayant un impact sur la planification doivent être traitées dans une transaction.

**API de planification de projets**

Voici la liste des API de planification de projet actuelles.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Cette API est utilisée pour créer un projet. Le projet et le compartiment de projet par défaut sont créés immédiatement.                         |
| **msdyn_CreateTeamMemberV1**            | Cette API est utilisée pour créer un membre de l’équipe de projet. L’enregistrement de membre de l’équipe est créé immédiatement.                                  |
| **msdyn_CreateOperationSetV1**          | Cette API est utilisée pour planifier plusieurs demandes qui doivent être effectuées dans une transaction.                                        |
| **msdyn_PssCreateV1**                   | Cette API est utilisée pour créer une entité. L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de création. |
| **msdyn_PssUpdateV1**                   | Cette API est utilisée pour mettre à jour une entité. L’entité peut être n’importe laquelle des entités de planification de projets prenant en charge l’opération de mise à jour  |
| **msdyn_PssDeleteV1**                   | Cette API est utilisée pour supprimer une entité. L’entité peut être n’importe laquelle des entités de planification de projets qui prennent en charge l’opération de suppression. |
| **msdyn_ExecuteOperationSetV1**         | Cette API est utilisée pour exécuter toutes les opérations dans l’ensemble d’opérations donné.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Cette API est utilisée pour mettre à jour un profil de travail planifié d’affectation de ressources.                                                        |



**Utilisation des API de planification de projets avec OperationSet**

Étant donné que les enregistrements avec **CreateProjectV1** et **CreateTeamMemberV1** sont créés immédiatement, ces API ne peuvent pas être utilisées directement dans l’**OperationSet**. Cependant, vous pouvez utiliser l’API pour créer les enregistrements nécessaires, créer un **OperationSet**, puis utiliser ces enregistrements précréés dans l’**OperationSet**.

**Opérations prises en charge**

| **Entité de planification**   | **Créer** | **Mise à jour** | **Delete** | **Remarques importantes**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tâche du projet            | Oui        | Oui        | Oui        | Les champs **En cours**, **EffortCompleted** et **EffortRemaining** peuvent être modifiés dans Project for the Web, mais ils ne peuvent pas être modifiés dans Project Operations.                                                                                                                                                                                             |
| Dépendance de la tâche du projet | Oui        | No         | Oui        | Les enregistrements de dépendance de la tâche du projet ne sont pas mis à jour. Au lieu de cela, un ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé.                                                                                                                                                                                                                                 |
| Attribution de ressource     | Oui        | Oui\*      | Oui        | Les opérations avec les champs suivants ne sont pas prises en charge : **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** et **PlannedWork**. Les enregistrements d’attribution de ressource ne sont pas mis à jour. Au lieu de cela, l’ancien enregistrement peut être supprimé et un nouvel enregistrement peut être créé. Une API distincte a été fournie pour mettre à jour les contours d’affectation des ressources. |
| Compartiment du projet          | Oui        | Oui        | Oui        | Le compartiment par défaut est créé à l’aide de l’API **CreateProjectV1**. La prise en charge de la création et de la suppression de compartiments de projet a été ajoutée dans la mise à jour de la version 16.                                                                                                                                                                                                   |
| Membre de l’équipe projet     | Oui        | Oui        | Oui        | Pour l’opération de création, utilisez l’API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Oui        | Oui        |            | Les opérations avec les champs suivants ne sont pas prises en charge : **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** et **Duration**.                                                                                       |
| Listes de contrôle du projet      | Oui        | Oui        | Oui        |                                                                                                                                                                                                                                                                                                                                                         |
| Étiquette du projet           | No         | Oui        | No         | Les noms des étiquettes peuvent être modifiés. Cette fonctionnalité n'est disponible que pour Project for the Web                                                                                                                                                                                                                                                                      |
| Tâche du projet à étiqueter   | Oui        | No         | Oui        | Cette fonctionnalité n'est disponible que pour Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint du projet          | Oui        | Oui        | Oui        | Le champ **Début** doit avoir une date antérieure au champ **Fin**. Les sprints d’un même projet ne peuvent pas se chevaucher. Cette fonctionnalité n'est disponible que pour Project for the Web                                                                                                                                                                    |




La propriété ID est facultative. Si elle est fournie, le système tente de l’utiliser et renvoie une exception si elle ne peut pas être utilisée. Si elle n’est pas fournie, le système la générera.

**Limitations et problèmes connus**

Voici une liste des limitations et des problèmes connus :

-   Les API de planification de projets ne peuvent être utilisées que par les **Utilisateurs disposant d’une licence Microsoft Project**. Elles ne peuvent pas être utilisées par :
    -   Utilisateurs de l’application
    -   Utilisateurs du système
    -   Utilisateurs de l’intégration
    -   Autres utilisateurs ne disposant pas de la licence requise
-   Chaque **OperationSet** peut seulement avoir un maximum de 100 opérations.
-   Chaque utilisateur peut seulement avoir un maximum de 10 **OperationSets** ouverts.
-   Project Operations prend actuellement en charge un maximum de 500 tâches au total sur un projet.
-   Chaque opération de mise à jour du profil d’affectation des ressources compte comme une seule opération.
-   Chaque liste de contours mis à jour peut contenir un maximum de 100 secteurs de temps.
-   Les statuts d’échec et les journaux d’échec **OperationSet** ne sont pas disponibles actuellement.
-   Il y a un maximum de 400 sprints par projet.
-   [Limites des projets et des tâches](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Les étiquettes sont actuellement disponibles uniquement pour Project for the Web.

**Gestion des erreurs**

-   Pour consulter les erreurs générées par les ensembles d’opérations, accédez à **Paramètres** \> **Intégration de la planification** \> **Ensembles d’opérations**.
-   Pour consulter les erreurs générées par le service de planification de projets, accédez à **Paramètres** \> **Intégration de la planification** \> **Journaux d’erreurs PSS**.

**Modification des contours d’affectation des ressources**

Contrairement à toutes les autres API de planification de projet qui mettent à jour une entité, l’API de contour d’affectation de ressources est uniquement responsable des mises à jour d’un seul champ, msdyn_plannedwork, sur une seule entité, msydn_resourceassignment.

Le mode de planification donné est :

-   **unités fixes**
-   le calendrier du projet est de 9h à 17h est de 9h à 17h, lundi, mardi, jeudi, vendredi (PAS DE TRAVAIL LES MERCREDIS)
-   et le calendrier des ressources est de 9h à 13h PST du lundi au vendredi

Cette mission dure une semaine, quatre heures par jour. En effet, le calendrier des ressources est du 9h à 13h PST, soit quatre heures par jour.

| &nbsp;     | Task | Date de début | Date de fin  | Quantité | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Collaborateur 9h-13h |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Par exemple, si vous souhaitez que le collaborateur ne travaille que trois heures par jour cette semaine et prévoyez une heure pour d’autres tâches.

#### <a name="updatedcontours-sample-payload"></a>Exemple de charge utile UpdatedContours :

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Il s’agit de l’affectation après l’exécution de l’API Mettre à jour la planification des contours.

| &nbsp;     | Task | Date de début | Date de fin  | Quantité | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Collaborateur 9h-13h | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Exemple de scénario**

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

** Exemples supplémentaires

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
