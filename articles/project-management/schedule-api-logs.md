---
title: Journaux de planification de projet
description: Cette rubrique fournit des informations et des exemples qui vous aideront à utiliser les journaux de planification de projet pour suivre les échecs liés au service de planification de projets et aux API de planification de projet.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589515"
---
# <a name="project-scheduling-logs"></a>Journaux de planification de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés, déploiement simplifié : traiter la facturation pro forma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations utilise [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) comme moteur de planification principal. Au lieu d’utiliser les API web Microsoft Dataverse standard, Project Operations utilise les nouvelles API de planification de projets pour créer, mettre à jour et supprimer des tâches de projet, des affectations de ressources, des dépendances de tâches, des compartiments de projet et des membres d’équipes de projet. Cependant, lorsque des opérations de création, de mise à jour ou de suppression sont exécutées par programme sur des entités WBS (structure de répartition du travail), des erreurs peuvent se produire. Pour suivre ces erreurs et l’historique des opérations, deux nouveaux journaux administratifs ont été mis en place : **Ensemble d’opérations** et **Service de planification de projets (PSS)**. Pour accéder à ces journaux, accédez à **Paramètres** \> **Intégration de la planification**.

L’illustration suivante présente le modèle de données pour les journaux de planification de projet.

![Modèle de données pour les journaux de planification de projet.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Journal Ensemble d’opérations

Le journal Ensemble d’opérations suit l’exécution d’un ensemble d’opérations utilisé pour exécuter une ou plusieurs opérations de création, de mise à jour ou de suppression dans un lot sur des projets, des tâches de projet, des affectations de ressources, des dépendances de tâches, des compartiments de projet ou des membres d’équipe de projet. Le champ **Opération en statut** affiche le statut général de l’ensemble d’opérations. Les détails de la charge utile de l’ensemble d’opérations sont capturés dans les enregistrements Détails de l’ensemble d’opérations associés.

### <a name="operation-set"></a>Ensemble d’opérations

Le tableau suivant indique les champs qui sont associés à l’entité **Ensemble d’opérations**.

| SchemaName            | Description                                                                                                  | Nom complet            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Date et heure de fin ou de l’échec de l’ensemble d’opérations.                                                | CompletedOn            |
| msdyn_correlationid   | Valeur **correlationId** de la requête.                                                                  | CorrelationId          |
| msdyn_description     | Description de l’ensemble d’opérations.                                                                        | Description            |
| msdyn_executedon      | Date et heure d’exécution de l’enregistrement.                                                                       | Exécuté le            |
| msdyn_operationsetId  | Identificateur unique des instances d’entité.                                                                   | OperationSet           |
| msdyn_Project         | Le projet associé à l’ensemble d’opérations.                                                            | Project                |
| msdyn_projectid       | Valeur **projectId** de la requête.                                                                      | ProjectId (obsolète) |
| msdyn_projectName     | Non applicable.                                                                                              | Non applicable         |
| msdyn_PSSErrorLog     | Identificateur unique du journal des erreurs du service de planification de projets associé à l’ensemble d’opérations. | Journal d’erreurs PSS          |
| msdyn_PSSErrorLogName | Non applicable.                                                                                              | Non applicable         |
| msdyn_status          | Statut de l’ensemble d’opérations.                                                                             | Status                 |
| msdyn_statusName      | Non applicable.                                                                                              | Non applicable         |
| msdyn_useraadid       | ID d’objet Azure Active Directory (Azure AD) de l’utilisateur auquel cette requête appartient.                     | UserAADID              |

### <a name="operation-set-detail"></a>Détails de l’ensemble d’opérations

Le tableau suivant indique les champs qui sont associés à l’entité **Détails de l’ensemble d’opérations**.

| SchemaName                 | Description                                                                                 | Nom complet           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Les champs Dataverse sérialisés pour la requête.                                            | CdsPayload            |
| msdyn_entityname           | Nom de l’entité pour la requête.                                                     | Nom de l’entité            |
| msdyn_httpverb             | Méthode de la requête.                                                                         | Verbe HTTP (Obsolète) |
| msdyn_httpverbName         | Non applicable.                                                                             | Non applicable        |
| msdyn_operationset         | Identificateur unique de l’ensemble d’opérations auquel appartient l’enregistrement.                      | OperationSet          |
| msdyn_operationsetdetailId | Identificateur unique des instances d’entité.                                                  | Détail de OperationSet   |
| msdyn_operationsetName     | Non applicable.                                                                             | Non applicable        |
| msdyn_operationtype        | Type d’opération du détail de l’ensemble d’opérations.                                             | OperationType         |
| msdyn_operationtypeName    | Non applicable.                                                                             | Non applicable        |
| msdyn_psspayload           | Champs sérialisés du service de planification de projets pour la requête.                           | PssPayload            |
| msdyn_recordid             | Identificateur de l’enregistrement de la requête.                                                       | ID d’enregistrement             |
| msdyn_requestnumber        | Numéro généré automatiquement qui identifie l’ordre dans lequel les requêtes ont été reçues. | Numéro de demande        |

## <a name="project-scheduling-service-error-logs"></a>Journal des erreurs du service de planification de projets

Les journaux d’erreurs du service de planification de projets capturent les échecs qui se produisent lorsque le service de planification de projets tente une opération **Enregistrer** ou **Ouvrir**. Il existe trois scénarios pris en charge dans lesquels ces journaux sont générés :

- Les actions lancées par l’utilisateur échouent de manière critique (par exemple, une affectation ne peut pas être créée en raison de privilèges manquants).
- Le service de planification de projets ne peut pas créer, mettre à jour, supprimer ou effectuer par programmation une quelconque opération en cascade sur une entité.
- L’utilisateur rencontre des erreurs lorsqu’un enregistrement ne s’ouvre pas (par exemple, lorsqu’un projet est ouvert ou que les informations d’un membre de l’équipe sont mises à jour).

### <a name="project-scheduling-service-log"></a>Journal du service de planification de projets

Le tableau suivant indique les champs qui sont inclus dans le journal du service de planification de projets.

| SchemaName          | Description                                                                    | Nom complet    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Pile des appels de l’exception.                                               | Pile des appels     |
| msdyn_correlationid | ID de corrélation de l’erreur.                                               | CorrelationId  |
| msdyn_errorcode     | Un champ qui est utilisé pour stocker le code d’erreur Dataverse ou le code d’erreur HTTP. | Code d’erreur     |
| msdyn_HelpLink      | Lien vers la documentation d’aide publique.                                       | Lien de l’aide      |
| msdyn_log           | Le journal du service de planification de projets.                                   | Journal            |
| msdyn_project       | Le projet associé au journal d’erreurs.                             | Project        |
| msdyn_projectName   | Le nom du projet si la charge utile de l’ensemble d’opérations sera persistante. | Non applicable |
| msdyn_psserrorlogId | Identificateur unique des instances d’entité.                                     | Journal d’erreurs PSS  |
| msdyn_SessionId     | ID de session du projet.                                                        | ID de session     |

## <a name="error-log-cleanup"></a>Nettoyage du journal des erreurs

Par défaut, les journaux d’erreurs du service de planification de projets et du journal d’ensemble d’opérations peuvent être nettoyés tous les 90 jours. Tous les enregistrements antérieurs à 90 jours seront supprimés. Cependant, en changeant la valeur du champ **msdyn_StateOperationSetAge** sur la page **Paramètres du projet**, les administrateurs peuvent ajuster la plage de nettoyage pour qu’elle soit comprise entre 1 et 120 jours. Plusieurs méthodes pour modifier cette valeur sont disponibles :

- Personnalisez l’entité **Paramètre du projet** en créant une page personnalisée et en ajoutant le champ **Âge défini pour les opérations obsolètes**.
- Utilisez un code client qui utilise le [Kit de développement logiciel (SDK) WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Utilisez le code du SDK Service qui utilise la méthode **updateRecord** du SDK Xrm (référence d’API client) dans les applications pilotées par modèle. Power Apps comprend une description et des paramètres pris en charge pour la méthode **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
