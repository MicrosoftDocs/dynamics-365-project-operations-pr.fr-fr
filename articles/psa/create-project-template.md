---
title: Créer un modèle de projet
description: Procédure de création d’un modèle de projet dans Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997238"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="64481-103">Créer un modèle de projet (Project Service)</span><span class="sxs-lookup"><span data-stu-id="64481-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="64481-104">Les modèles de projet vous font gagner du temps si votre société fait régulièrement des offres sur des types de projet similaires.</span><span class="sxs-lookup"><span data-stu-id="64481-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="64481-105">Ils fournissent un jeu standard de rôles et d’heures estimés pour un type du projet.</span><span class="sxs-lookup"><span data-stu-id="64481-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="64481-106">Les responsables de compte et les responsables de projet peuvent créer des projets basés sur un modèle de projet, ou ils peuvent copier le modèle et réaliser leur propre projet.</span><span class="sxs-lookup"><span data-stu-id="64481-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="64481-107">Composants du modèle de projet</span><span class="sxs-lookup"><span data-stu-id="64481-107">Components of project template</span></span>
 <span data-ttu-id="64481-108">Un modèle de projet est composé de trois composants :</span><span class="sxs-lookup"><span data-stu-id="64481-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="64481-109">**Structure de répartition du travail** : une structure de répartition du travail dans un modèle de projet se compose du même ensemble d’éléments que le projet.</span><span class="sxs-lookup"><span data-stu-id="64481-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="64481-110">Vous pouvez créer une hiérarchie de tâches, associer des rôles à la tâche, définir des attributs de planification, définir des dépendances et afficher toutes les données dans le diagramme de Gantt.</span><span class="sxs-lookup"><span data-stu-id="64481-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="64481-111">La structure de répartition du travail dans les modèles de projet prend également en charge les modes de tâche de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="64481-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="64481-112">Il n’y a aucune différence entre un modèle de projet et un projet lors de la création de la planification des tâches.</span><span class="sxs-lookup"><span data-stu-id="64481-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="64481-113">**Estimations du projet** : les estimations de projet dans les modèles fonctionnent de la même manière que dans les projets, excepté les tarifs permettant le calcul des tarifs de vente et de prix de revient par défaut qui sont toujours les tarifs de vente et de prix de revient par défaut définis dans les paramètres du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="64481-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="64481-114">Le reste des fonctionnalités est le même que dans un projet.</span><span class="sxs-lookup"><span data-stu-id="64481-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="64481-115">**Formation de l’équipe du projet** : lors de la formation d’une équipe de projet pour un modèle de projet, vous ne pouvez pas inscrire une ressource nommée dans un modèle.</span><span class="sxs-lookup"><span data-stu-id="64481-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="64481-116">Vous pouvez **Générez l’équipe du projet** dans la structure de répartition du travail pour générer un ensemble de ressources génériques.</span><span class="sxs-lookup"><span data-stu-id="64481-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="64481-117">Vous pouvez également spécifier les aptitudes et les compétences requises pour les ressources génériques.</span><span class="sxs-lookup"><span data-stu-id="64481-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="64481-118">Vous ne pouvez pas substituer une ressource générique avec une ressource pouvant être réservée dans les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="64481-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="64481-119">Créer un projet à partir d’un modèle</span><span class="sxs-lookup"><span data-stu-id="64481-119">Create a project from a template</span></span>  
 <span data-ttu-id="64481-120">Vous pouvez créer un projet à partir d’un modèle de ces méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="64481-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="64481-121">En créant un projet à partir d’un devis, vous pouvez choisir un modèle de projet dans le formulaire de création rapide de projet.</span><span class="sxs-lookup"><span data-stu-id="64481-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="64481-122">Lors de la création d’un projet en cliquant sur **Nouveau projet**, le formulaire du projet s’affiche avant d’enregistrer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64481-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="64481-123">De là, vous pouvez cliquer sur le champ **Choisir un modèle** pour choisir dans la liste de modèles de projet prédéfinis de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="64481-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="64481-124">Cliquez sur **Créer un projet à partir d’un modèle** sur la page **Modèle du projet** pour créer un projet à partir du modèle.</span><span class="sxs-lookup"><span data-stu-id="64481-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="64481-125">Copie de composants d’un modèle dans un projet</span><span class="sxs-lookup"><span data-stu-id="64481-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="64481-126">Lorsque vous copiez les composants d’un modèle dans un projet, il y a quelques précautions à prendre.</span><span class="sxs-lookup"><span data-stu-id="64481-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="64481-127">**Copie d’une structure de distribution de travail** : lorsque vous copiez la structure de répartition du travail d’un modèle de projet, si le projet a un calendrier de projet différent du modèle, les heures de travail du calendrier du projet sont appliquées au programme des tâches.</span><span class="sxs-lookup"><span data-stu-id="64481-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="64481-128">Cela ajuste la planification au calendrier du projet de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="64481-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="64481-129">De même, la première tâche de la structure de répartition du travail prend la date de début du projet, par conséquent le reste de la planification de la hiérarchie des tâches est mis à jour selon la durée et les dépendances spécifiées dans la structure de répartition du travail du modèle.</span><span class="sxs-lookup"><span data-stu-id="64481-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="64481-130">**Copie des estimations du projet** : lorsque vous copiez dans les lignes d’évaluation de projet, les tarifs sont mis à jour selon l’unité propriétaire du projet pour les prix de revient et selon le client pour les tarifs de vente.</span><span class="sxs-lookup"><span data-stu-id="64481-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="64481-131">Le prix unitaire et les prix de vente sont déterminés à partir de ces tarifs dans les projets associés à une entité commerciale.</span><span class="sxs-lookup"><span data-stu-id="64481-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="64481-132">**Copie d’une équipe du projet** : lorsque vous copiez l’équipe du projet à partir du modèle d’un projet, les ressources génériques y sont copiées, avec toutes les aptitudes et compétences définies dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="64481-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="64481-133">Les affectations de ressources génériques sont également gérées comme dans le modèle du projet.</span><span class="sxs-lookup"><span data-stu-id="64481-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="64481-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64481-134">See Also</span></span>  
 [<span data-ttu-id="64481-135">Guide du responsable de projet</span><span class="sxs-lookup"><span data-stu-id="64481-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]