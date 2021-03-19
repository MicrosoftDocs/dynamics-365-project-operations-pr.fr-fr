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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="465e1-103">Développer des modèles de projet avec Copier le projet</span><span class="sxs-lookup"><span data-stu-id="465e1-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="465e1-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="465e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="465e1-105">Dynamics 365 Project Operations prend en charge la possibilité de copier un projet et de rétablir toutes les affectations aux ressources génériques qui représentent le rôle.</span><span class="sxs-lookup"><span data-stu-id="465e1-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="465e1-106">Les clients peuvent utiliser cette fonctionnalité pour créer des modèles de projet de base.</span><span class="sxs-lookup"><span data-stu-id="465e1-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="465e1-107">Lorsque vous sélectionnez **Copier le projet**, le statut du projet cible est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="465e1-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="465e1-108">Utilisez la **raison du statut** pour déterminer quand l’action de copie est terminée.</span><span class="sxs-lookup"><span data-stu-id="465e1-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="465e1-109">La sélection **Copier le projet** met également à jour la date de début du projet à la date de début actuelle si aucune date cible n’est détectée dans l’entité de projet cible.</span><span class="sxs-lookup"><span data-stu-id="465e1-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="465e1-110">Copier l’action personnalisée du projet</span><span class="sxs-lookup"><span data-stu-id="465e1-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="465e1-111">Nom</span><span class="sxs-lookup"><span data-stu-id="465e1-111">Name</span></span> 

<span data-ttu-id="465e1-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="465e1-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="465e1-113">Paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="465e1-113">Input parameters</span></span>
<span data-ttu-id="465e1-114">Il existe trois paramètres de saisie :</span><span class="sxs-lookup"><span data-stu-id="465e1-114">There are three input parameters:</span></span>

| <span data-ttu-id="465e1-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="465e1-115">Parameter</span></span>          | <span data-ttu-id="465e1-116">Type</span><span class="sxs-lookup"><span data-stu-id="465e1-116">Type</span></span>   | <span data-ttu-id="465e1-117">Valeurs</span><span class="sxs-lookup"><span data-stu-id="465e1-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="465e1-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="465e1-118">ProjectCopyOption</span></span>  | <span data-ttu-id="465e1-119">String</span><span class="sxs-lookup"><span data-stu-id="465e1-119">String</span></span> | <span data-ttu-id="465e1-120">**{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="465e1-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="465e1-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="465e1-121">SourceProject</span></span>      | <span data-ttu-id="465e1-122">Référence d’entité</span><span class="sxs-lookup"><span data-stu-id="465e1-122">Entity Reference</span></span> | <span data-ttu-id="465e1-123">Projet source</span><span class="sxs-lookup"><span data-stu-id="465e1-123">Source Project</span></span> |
| <span data-ttu-id="465e1-124">Cible</span><span class="sxs-lookup"><span data-stu-id="465e1-124">Target</span></span>             | <span data-ttu-id="465e1-125">Référence d’entité</span><span class="sxs-lookup"><span data-stu-id="465e1-125">Entity Reference</span></span> | <span data-ttu-id="465e1-126">Projet cible</span><span class="sxs-lookup"><span data-stu-id="465e1-126">Target Project</span></span> |


- <span data-ttu-id="465e1-127">**{"clearTeamsAndAssignments":true}**  : Trois comportements par défaut de Project pour le Web et suppression de toutes les affectations et des membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="465e1-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="465e1-128">**{"removeNamedResources":true}** Le comportement par défaut pour Project Operations et rétablira les affectations aux ressources génériques.</span><span class="sxs-lookup"><span data-stu-id="465e1-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="465e1-129">Pour plus de valeurs par défaut sur les actions, voir [Utiliser des actions API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="465e1-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="465e1-130">Spécifier les champs à copier</span><span class="sxs-lookup"><span data-stu-id="465e1-130">Specify fields to copy</span></span> 
<span data-ttu-id="465e1-131">Lorsque l’action est appelée **Copier le projet** regardera la vue du projet **Copier les colonnes du projet** pour déterminer les champs à copier lorsque le projet est copié.</span><span class="sxs-lookup"><span data-stu-id="465e1-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="465e1-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="465e1-132">Example</span></span>
<span data-ttu-id="465e1-133">L'exemple suivant montre comment appeler l'action personnalisée **CopyProject** avec le jeu de paramètres **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="465e1-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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