---
title: Développer des modèles de projet avec Copier le projet
description: Cette rubrique fournit des informations sur la création de modèles de projet à l’aide de l’action personnalisée Copier le projet.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286920"
---
# <a name="develop-project-templates-with-copy-project"></a>Développer des modèles de projet avec Copier le projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations prend en charge la possibilité de copier un projet et de rétablir toutes les affectations aux ressources génériques qui représentent le rôle. Les clients peuvent utiliser cette fonctionnalité pour créer des modèles de projet de base.

Lorsque vous sélectionnez **Copier le projet**, le statut du projet cible est mis à jour. Utilisez la **raison du statut** pour déterminer quand l’action de copie est terminée. La sélection **Copier le projet** met également à jour la date de début du projet à la date de début actuelle si aucune date cible n’est détectée dans l’entité de projet cible.

## <a name="copy-project-custom-action"></a>Copier l’action personnalisée du projet 

### <a name="name"></a>Nom 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Paramètres d’entrée
Il existe trois paramètres de saisie :

| Paramètre          | Type   | Valeurs                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Référence d’entité | Projet source |
| Cible             | Référence d’entité | Projet cible |


- **{"clearTeamsAndAssignments":true}**  : Trois comportements par défaut de Project pour le Web et suppression de toutes les affectations et des membres de l’équipe.
- **{"removeNamedResources":true}** Le comportement par défaut pour Project Operations et rétablira les affectations aux ressources génériques.

Pour plus de valeurs par défaut sur les actions, voir [Utiliser des actions API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Spécifier les champs à copier 
Lorsque l’action est appelée **Copier le projet** regardera la vue du projet **Copier les colonnes du projet** pour déterminer les champs à copier lorsque le projet est copié.


### <a name="example"></a>Exemple
L'exemple suivant montre comment appeler l'action personnalisée **CopyProject** avec le jeu de paramètres **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]