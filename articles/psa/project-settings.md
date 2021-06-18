---
title: Paramètres du projet
description: Cette rubrique fournit des informations sur les paramètres de gestion du projet.
author: ruhercul
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
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998318"
---
# <a name="project-settings"></a><span data-ttu-id="3978b-103">Paramètres du projet</span><span class="sxs-lookup"><span data-stu-id="3978b-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3978b-104">Utilisez les paramètres suivants pour accéder aux fonctionnalités de planification du projet.</span><span class="sxs-lookup"><span data-stu-id="3978b-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="3978b-105">Modèle de travail</span><span class="sxs-lookup"><span data-stu-id="3978b-105">Work template</span></span>

<span data-ttu-id="3978b-106">Pour créer une planification de projet, créez un modèle de calendrier de projet qui définit le nombre d’heures de travail par jour et les heures de fermeture.</span><span class="sxs-lookup"><span data-stu-id="3978b-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="3978b-107">Pour créer un modèle de calendrier de projet, vous associez un modèle de travail au champ **Modèle de calendrier** du projet.</span><span class="sxs-lookup"><span data-stu-id="3978b-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="3978b-108">Pour créer un modèle de travail, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3978b-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="3978b-109">Dans PSA, dans le volet de navigation gauche, cliquez sur **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="3978b-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="3978b-110">Sur la page de liste **Ressources**, ouvrez enregistrement utilisateur, puis sélectionnez **Afficher les heures de travail**.</span><span class="sxs-lookup"><span data-stu-id="3978b-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3978b-111">Vérifiez que vous autorisez les fenêtres contextuelles sur la page de navigateur.</span><span class="sxs-lookup"><span data-stu-id="3978b-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="3978b-112">Cela vous permet de voir les heures de travail définies pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="3978b-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="3978b-113">Dans l’onglet **Vue mensuelle**, cliquez sur **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="3978b-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="3978b-114">Une liste de trois options apparaît :</span><span class="sxs-lookup"><span data-stu-id="3978b-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="3978b-115">Nouvelle planification hebdomadaire</span><span class="sxs-lookup"><span data-stu-id="3978b-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="3978b-116">Planification des tâches sur un jour</span><span class="sxs-lookup"><span data-stu-id="3978b-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="3978b-117">Absence</span><span class="sxs-lookup"><span data-stu-id="3978b-117">Time Off</span></span>

> ![Groupe d’options](media/project-13.png)

4. <span data-ttu-id="3978b-119">Sélectionnez **Nouvelle planification hebdomadaire**, puis définissez les options de cette planification de ressource.</span><span class="sxs-lookup"><span data-stu-id="3978b-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="3978b-120">Vous pouvez définir une planification hebdomadaire récurrente, des paramètres d’heure quotidiens, des fermetures de bureaux, et plus encore.</span><span class="sxs-lookup"><span data-stu-id="3978b-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="3978b-121">Définissez la plage de dates, la sélectionnez **Enregistrer**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="3978b-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="3978b-122">Revenez à la page de liste **Ressources**, puis sélectionnez la ressource pour laquelle vous avez défini les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="3978b-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="3978b-123">Sélectionnez **Définir le calendrier comme** pour définir le modèle de travail.</span><span class="sxs-lookup"><span data-stu-id="3978b-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="3978b-124">Dans la boîte de dialogue **Modèle de travail**, entrez le nom pour le modèle de travail, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="3978b-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="3978b-125">Vous pouvez désormais associer le modèle de travail à un modèle de calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="3978b-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="3978b-126">Rôles des ressources</span><span class="sxs-lookup"><span data-stu-id="3978b-126">Resource roles</span></span>

<span data-ttu-id="3978b-127">Le terme *rôle de la ressource* fait référence à l’ensemble de compétences, de qualifications et de certifications qu’une personne doit avoir pour effectuer un ensemble spécifique de tâches sur un projet.</span><span class="sxs-lookup"><span data-stu-id="3978b-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="3978b-128">PSA vous permet d’établir le coût et de facturer le temps d’une ressource en fonction du rôle auquel la ressource est associée.</span><span class="sxs-lookup"><span data-stu-id="3978b-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="3978b-129">Chaque organisation doit configurer ces rôles à l’aide de la navigation gauche sur le menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="3978b-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="3978b-130">Chaque organisation doit configurer ces rôles sur la page **Catégories de ressources actives**.</span><span class="sxs-lookup"><span data-stu-id="3978b-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="3978b-131">Pour ouvrir cette page, dans le volet de navigation de gauche, sélectionnez **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="3978b-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="3978b-132">Tarifs</span><span class="sxs-lookup"><span data-stu-id="3978b-132">Price lists</span></span>

<span data-ttu-id="3978b-133">Les tarifs vous permettent de définir le coût et les prix de vente des rôles de ressources, des catégories de dépenses, des produits et d’autres éléments dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3978b-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="3978b-134">Avant de définir des estimations financières pour le travail à fournir pour un projet, vous devez créer un coût de support et des tarifs de vente.</span><span class="sxs-lookup"><span data-stu-id="3978b-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="3978b-135">Dans la section des paramètres, vous devez configurer un coût et des tarifs de vente par défaut qui s’appliquent à tous les projets créés dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3978b-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="3978b-136">Dans la page **Paramètres du projet actifs**, vérifiez que vous configurez un coût et des tarifs de vente par défaut.</span><span class="sxs-lookup"><span data-stu-id="3978b-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]