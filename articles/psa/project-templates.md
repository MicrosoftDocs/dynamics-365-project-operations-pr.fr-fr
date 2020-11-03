---
title: Modèles de projet
description: Cette rubrique fournit des informations sur l'utilisation des modèles de projet pour un paramétrage rapide de projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075902"
---
# <a name="project-templates"></a><span data-ttu-id="3eee7-103">Modèles de projet</span><span class="sxs-lookup"><span data-stu-id="3eee7-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3eee7-104">Un modèle de projet est un cadre prédéfini qui vous permet de démarrer rapidement et facilement un projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="3eee7-105">Vous pouvez utiliser un modèle prédéfini pour créer un projet avec un simple clic.</span><span class="sxs-lookup"><span data-stu-id="3eee7-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="3eee7-106">Quant aux projets, vous devez définir les conditions préalables pour les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="3eee7-107">Vous devez définir un calendrier de projet pour chaque modèle de projet, et des rôles et des tarifs doivent être prédéfinis dans l'organisation, afin que les composants du modèle aient des informations utiles.</span><span class="sxs-lookup"><span data-stu-id="3eee7-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="3eee7-108">Un modèle de projet est composé de trois composants : une planification, des estimations de projet, et des membres de l'équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="3eee7-109">Planifier</span><span class="sxs-lookup"><span data-stu-id="3eee7-109">Schedule</span></span>

<span data-ttu-id="3eee7-110">Une planification dans un modèle de projet possède le même ensemble d'éléments qu'une planification dans un projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="3eee7-111">Vous pouvez créer une hiérarchie de tâches, associer des rôles aux tâches, définir des attributs de planification et définir des dépendances.</span><span class="sxs-lookup"><span data-stu-id="3eee7-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="3eee7-112">Une planification dans un modèle de projet prend également en charge les modes de tâches de chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="3eee7-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="3eee7-113">Par conséquent, il prend en charge le moteur de planification.</span><span class="sxs-lookup"><span data-stu-id="3eee7-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="3eee7-114">Vous devez associer un calendrier de projet au projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="3eee7-115">Lors de la création d'une planification des tâches, il n'y a aucune différence entre un modèle de projet et un projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="3eee7-116">Estimations de projets</span><span class="sxs-lookup"><span data-stu-id="3eee7-116">Project estimates</span></span>

<span data-ttu-id="3eee7-117">Les estimations de projet dans un modèle de projet fonctionnent de la même manière que des estimations de projet dans un projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="3eee7-118">Toutefois, le coût et les prix de vente sont extraits des listes de coût et des tarifs de vente par défaut qui sont définis dans les paramètres.</span><span class="sxs-lookup"><span data-stu-id="3eee7-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="3eee7-119">Création d'un projet à partir d'un modèle</span><span class="sxs-lookup"><span data-stu-id="3eee7-119">Creating a project from a template</span></span>
 
<span data-ttu-id="3eee7-120">Il existe plusieurs manières de créer un projet à partir d'un modèle de projet :</span><span class="sxs-lookup"><span data-stu-id="3eee7-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="3eee7-121">Lorsque vous créez un projet à partir d'un devis, vous pouvez sélectionner un modèle de projet dans la boîte de dialogue **Création rapide : Projet**.</span><span class="sxs-lookup"><span data-stu-id="3eee7-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Boîte de dialogue Création rapide : Projet](media/project-11.png)

- <span data-ttu-id="3eee7-123">Lorsque vous créez un projet en sélectionnant **Nouveau projet** , la page **Projet** s'affiche avant l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3eee7-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="3eee7-124">Dans le champ **Choisir un modèle** , sélectionnez l'un des modèles de projet prédéfinis dans l'organisation.</span><span class="sxs-lookup"><span data-stu-id="3eee7-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="3eee7-125">Utilisez **Créer un projet à partir d'un modèle** sur la page **Entité Modèle**.</span><span class="sxs-lookup"><span data-stu-id="3eee7-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="3eee7-126">Copie de composants de modèle dans un projet</span><span class="sxs-lookup"><span data-stu-id="3eee7-126">Copying components of template to project</span></span>

<span data-ttu-id="3eee7-127">Lorsque vous copiez les composants d'un modèle de projet dans un projet, certains chevauchement peuvent se produire, selon les paramètres du projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="3eee7-128">Copie de la planification</span><span class="sxs-lookup"><span data-stu-id="3eee7-128">Copying the schedule</span></span>

<span data-ttu-id="3eee7-129">Lorsque vous copiez la planification d'un modèle de projet, si le projet a un calendrier de projet différent du modèle, les heures de travail du calendrier du projet sont appliquées au programme des tâches.</span><span class="sxs-lookup"><span data-stu-id="3eee7-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="3eee7-130">Ainsi, la planification est ajustée au calendrier du projet de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3eee7-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="3eee7-131">De même, la première tâche de la planification prend la date de début du projet, la planification du reste de la hiérarchie est mise à jour selon la durée et les dépendances spécifiées dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="3eee7-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="3eee7-132">Copie d'estimations de projets</span><span class="sxs-lookup"><span data-stu-id="3eee7-132">Copying project estimates</span></span> 

<span data-ttu-id="3eee7-133">Lorsque vous copiez dans les lignes d'estimation du projet, les tarifs sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3eee7-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="3eee7-134">Pour la liste de prix de revient, ces mises à jour sont basées sur l'unité propriétaire du projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="3eee7-135">Pour les tarifs de vente, ils sont basés sur le client.</span><span class="sxs-lookup"><span data-stu-id="3eee7-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="3eee7-136">Pour les projets associés à une entité commerciale, le prix unitaire et les prix de vente sont déterminés sur la base de ces tarifs.</span><span class="sxs-lookup"><span data-stu-id="3eee7-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="3eee7-137">Copie d'une équipe de projet</span><span class="sxs-lookup"><span data-stu-id="3eee7-137">Copying a project team</span></span>

<span data-ttu-id="3eee7-138">Lorsque vous copiez une équipe de projet à partir du modèle d'un projet, les ressources génériques sont copiées, avec toutes les aptitudes et compétences définies dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="3eee7-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="3eee7-139">Les affectations de ressources génériques sont également gérées comme elles l'étaient dans le modèle du projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="3eee7-140">Les ressources nommées ne sont pas prises en charge dans les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="3eee7-140">Named resources aren't supported in project templates.</span></span>
