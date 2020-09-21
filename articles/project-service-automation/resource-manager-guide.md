---
title: Guide du gestionnaire de ressources
description: Guide de gestion de ressources dans Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168128"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="d6fef-103">Guide du gestionnaire de ressources (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d6fef-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d6fef-104">Les fonctionnalités [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dans l'aide [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] vous permettent de rechercher les ressources appropriées au moment approprié pour le projet approprié et de vérifier que toutes les ressources sont utilisées efficacement.</span><span class="sxs-lookup"><span data-stu-id="d6fef-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="d6fef-105">Déployez les consultants de votre entreprise de manière efficace avec le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="d6fef-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="d6fef-106">Ils vous offrent les outils dont vous avez besoin pour planifier les ressources en fonction des besoins et programmes des projets de conseil et des compétences et de la disponibilité des consultants.</span><span class="sxs-lookup"><span data-stu-id="d6fef-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="d6fef-107">Vous pouvez rapidement trouver les consultants les plus qualifiés disponibles pour travailler sur des projets, et vous pouvez facilement voir comment améliorer leur planification au cours de chaque projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="d6fef-108">La planification des ressources vous permet de faire ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d6fef-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="d6fef-109">Mettre en correspondance les ressources avec les projets, en fonction du niveau de correspondance de leurs compétences et qualifications aux besoins en ressources du projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="d6fef-110">Mettre en correspondance la planification d'une ressource avec un calendrier de projet, en fonction des disponibilités et des absences prévues.</span><span class="sxs-lookup"><span data-stu-id="d6fef-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="d6fef-111">Le calendrier codé avec des couleurs offre des indices visuels sur la disponibilité des ressources.</span><span class="sxs-lookup"><span data-stu-id="d6fef-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="d6fef-112">Examinez la capacité de chaque consultant et déterminez comment cette capacité est actuellement utilisée.</span><span class="sxs-lookup"><span data-stu-id="d6fef-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="d6fef-113">Cela peut vous aider à déterminer si un consultant est sous ou sur-utilisé, ou s'il travaille conformément à sa capacité.</span><span class="sxs-lookup"><span data-stu-id="d6fef-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="d6fef-114">Attribuez un pourcentage ou un nombre spécifique d'heures pour la capacité d'un employé pour un projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="d6fef-115">Procédez à des réservations de ressources groupées.</span><span class="sxs-lookup"><span data-stu-id="d6fef-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="d6fef-116">Réservez des ressources temporairement ou fermement, et convertissez les heures temporairement réservées en heures fermement réservées en une étape.</span><span class="sxs-lookup"><span data-stu-id="d6fef-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="d6fef-117">Formez automatiquement une équipe de projet selon des ressources définies dans une structure de répartition du travail pour un projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="d6fef-118">Exécutez les demandes de ressources (réservation, objectif, trouver des ressources de remplacement).</span><span class="sxs-lookup"><span data-stu-id="d6fef-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="d6fef-119">Attribuez les ressources en fonction d'un modèle central (le gestionnaire de ressources attribue les ressources) ou hybride (le gestionnaire de ressources et d'autres responsables peuvent les attribuer).</span><span class="sxs-lookup"><span data-stu-id="d6fef-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="d6fef-120">Pour plus d'informations sur la définition d'un modèle de gestion des ressources hybride ou central, voir [Configurer des paramètres supplémentaires (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d6fef-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="d6fef-121">Vous pouvez gérer les ressources efficacement dans les projets et vous assurer que les projets sont dotés en personnel de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="d6fef-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="d6fef-122">Vous devrez réaliser les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6fef-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="d6fef-123">[Gérer les demandes de ressource](../project-service/manage-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="d6fef-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="d6fef-124">Mettre en correspondance les compétences et les qualifications des consultants avec les bons projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="d6fef-125">[Afficher la disponibilité des ressources](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="d6fef-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="d6fef-126">Vérifier la disponibilité des consultants dans une vue du calendrier.</span><span class="sxs-lookup"><span data-stu-id="d6fef-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="d6fef-127">[Afficher l'utilisation des ressources](../project-service/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="d6fef-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="d6fef-128">Consulter le pourcentage de temps de réservation actuel de vos consultants.</span><span class="sxs-lookup"><span data-stu-id="d6fef-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="d6fef-129">[Planifier des ressources pour un projet](../project-service/schedule-resources-project.md)</span><span class="sxs-lookup"><span data-stu-id="d6fef-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="d6fef-130">Planifiez des consultants pour un projet.</span><span class="sxs-lookup"><span data-stu-id="d6fef-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="d6fef-131">Pour plus d'informations sur l'envoi de demandes de ressources pour des projets individuels, voir [Soumettre les demandes de ressource](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="d6fef-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d6fef-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6fef-132">See Also</span></span>  
 <span data-ttu-id="d6fef-133">[Vue d'ensemble de Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="d6fef-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="d6fef-134">[Guide de l'administrateur](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d6fef-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="d6fef-135">[Guide du responsable de projet](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d6fef-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="d6fef-136">[Guide du responsable de projet](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d6fef-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="d6fef-137">Guide sur le temps, les dépenses et la collaboration</span><span class="sxs-lookup"><span data-stu-id="d6fef-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
