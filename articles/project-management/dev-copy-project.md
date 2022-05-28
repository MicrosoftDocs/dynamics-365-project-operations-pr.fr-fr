---
title: Développer des modèles de projet avec Copier le projet
description: Cette rubrique fournit des informations sur la création de modèles de projet à l’aide de l’action personnalisée Copier le projet.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590895"
---
# <a name="develop-project-templates-with-copy-project"></a>Développer des modèles de projet avec Copier le projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations prend en charge la possibilité de copier un projet et de rétablir toutes les affectations aux ressources génériques qui représentent le rôle. Les clients peuvent utiliser cette fonctionnalité pour créer des modèles de projet de base.

Lorsque vous sélectionnez **Copier le projet**, le statut du projet cible est mis à jour. Utilisez la **raison du statut** pour déterminer quand l’action de copie est terminée. La sélection **Copier le projet** met également à jour la date de début du projet à la date de début actuelle si aucune date cible n’est détectée dans l’entité de projet cible.

## <a name="copy-project-custom-action"></a>Copier l’action personnalisée du projet

### <a name="name"></a>Nom  

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Paramètres d’entrée

Il existe trois paramètres de saisie :

- **ReplaceNamedResources** ou **ClearTeamsAndAssignments** – Définissez uniquement une des options. Ne définissez pas les deux.

    - **\{"ReplaceNamedResources":true\}** – Comportement par défaut pour Project Operations. Toute ressource nommée est remplacée par la ressource générique.
    - **\{"ClearTeamsAndAssignments":true\}** – Comportement par défaut pour Project for the Web. Toutes les affectations et tous les membres de l’équipe sont supprimés.

- **SourceProject** – Référence de l’entité du projet source à partir duquel effectuer une copie. Ce paramètre ne peut pas avoir la valeur null.
- **Target** – Référence de l’entité du projet cible vers lequel effectuer une copie. Ce paramètre ne peut pas avoir la valeur null.

Le tableau suivant fournit un résumé des trois paramètres.

| Paramètre                | Type             | active                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Entier          | **True** ou **False** |
| ClearTeamsAndAssignments | Entier          | **True** ou **False** |
| SourceProject            | Référence d’entité | Projet source    |
| Cible                   | Référence d’entité | Projet cible    |

Pour plus de valeurs par défaut sur les actions, voir [Utiliser des actions API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Contrôles

Les validations suivantes sont terminées.

1. Null vérifie et récupère les projets source et cible pour confirmer l’existence des deux projets dans l’organisation.
2. Le système valide que le projet cible est valide pour la copie en vérifiant les conditions suivantes :

    - Il n’y a pas d’activité antérieure sur le projet (y compris la sélection de l’onglet **Tâches**), et le projet est récemment créé.
    - Il n’y a pas de copie précédente, aucune importation n’a été demandée sur ce projet et le statut du projet n’est pas défini sur **Échec**.

3. L’opération n’est pas appelée à l’aide de HTTP.

## <a name="specify-fields-to-copy"></a>Spécifier les champs à copier

Lorsque l’action est appelée **Copier le projet** regardera la vue du projet **Copier les colonnes du projet** pour déterminer les champs à copier lorsque le projet est copié.

### <a name="example"></a>Exemple

L’exemple suivant montre comment appeler l’action personnalisée **CopyProjectV3** avec le groupe de paramètres **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
