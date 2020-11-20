---
title: Développer des modèles de projet avec Copier le projet
description: Cette rubrique fournit des informations sur la création de modèles de projet à l’aide de l’action personnalisée Copier le projet.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131610"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="17a84-103">Développer des modèles de projet avec Copier le projet</span><span class="sxs-lookup"><span data-stu-id="17a84-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="17a84-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="17a84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17a84-105">Dynamics 365 Project Operations prend en charge la possibilité de copier un projet et de rétablir toutes les affectations aux ressources génériques qui représentent le rôle.</span><span class="sxs-lookup"><span data-stu-id="17a84-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="17a84-106">Les clients peuvent utiliser cette fonctionnalité pour créer des modèles de projet de base.</span><span class="sxs-lookup"><span data-stu-id="17a84-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="17a84-107">Lorsque vous sélectionnez **Copier le projet**, le statut du projet cible est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="17a84-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="17a84-108">Utilisez la **raison du statut** pour déterminer quand l’action de copie est terminée.</span><span class="sxs-lookup"><span data-stu-id="17a84-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="17a84-109">La sélection **Copier le projet** met également à jour la date de début du projet à la date de début actuelle si aucune date cible n’est détectée dans l’entité de projet cible.</span><span class="sxs-lookup"><span data-stu-id="17a84-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="17a84-110">Copier l’action personnalisée du projet</span><span class="sxs-lookup"><span data-stu-id="17a84-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="17a84-111">Nom </span><span class="sxs-lookup"><span data-stu-id="17a84-111">Name</span></span> 

<span data-ttu-id="17a84-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="17a84-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="17a84-113">Paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="17a84-113">Input parameters</span></span>
<span data-ttu-id="17a84-114">Il existe trois paramètres de saisie :</span><span class="sxs-lookup"><span data-stu-id="17a84-114">There are three input parameters:</span></span>

| <span data-ttu-id="17a84-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="17a84-115">Parameter</span></span>          | <span data-ttu-id="17a84-116">Type</span><span class="sxs-lookup"><span data-stu-id="17a84-116">Type</span></span>   | <span data-ttu-id="17a84-117">Valeurs</span><span class="sxs-lookup"><span data-stu-id="17a84-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="17a84-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="17a84-118">ProjectCopyOption</span></span>  | <span data-ttu-id="17a84-119">String</span><span class="sxs-lookup"><span data-stu-id="17a84-119">String</span></span> | <span data-ttu-id="17a84-120">**{"removeNamedResources":true}** ou **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="17a84-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="17a84-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="17a84-121">SourceProject</span></span>      | <span data-ttu-id="17a84-122">Référence d’entité</span><span class="sxs-lookup"><span data-stu-id="17a84-122">Entity Reference</span></span> | <span data-ttu-id="17a84-123">Projet source</span><span class="sxs-lookup"><span data-stu-id="17a84-123">Source Project</span></span> |
| <span data-ttu-id="17a84-124">Cible </span><span class="sxs-lookup"><span data-stu-id="17a84-124">Target</span></span>             | <span data-ttu-id="17a84-125">Référence d’entité</span><span class="sxs-lookup"><span data-stu-id="17a84-125">Entity Reference</span></span> | <span data-ttu-id="17a84-126">Projet cible</span><span class="sxs-lookup"><span data-stu-id="17a84-126">Target Project</span></span> |


- <span data-ttu-id="17a84-127">**{"clearTeamsAndAssignments":true}**  : Trois comportements par défaut de Project pour le Web et suppression de toutes les affectations et des membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="17a84-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="17a84-128">**{"removeNamedResources":true}** Le comportement par défaut pour Project Operations et rétablira les affectations aux ressources génériques.</span><span class="sxs-lookup"><span data-stu-id="17a84-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="17a84-129">Pour plus de valeurs par défaut sur les actions, voir [Utiliser des actions API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="17a84-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="17a84-130">Spécifier les champs à copier</span><span class="sxs-lookup"><span data-stu-id="17a84-130">Specify fields to copy</span></span> 
<span data-ttu-id="17a84-131">Lorsque l’action est appelée **Copier le projet** regardera la vue du projet **Copier les colonnes du projet** pour déterminer les champs à copier lorsque le projet est copié.</span><span class="sxs-lookup"><span data-stu-id="17a84-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
