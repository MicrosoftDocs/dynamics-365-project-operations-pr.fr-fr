---
title: Configurer les ressources de projet
description: Cette rubrique fournit des informations sur la configuration ou la demande de ressources de projet.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075912"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="6fcf5-103">Configurer les ressources de projet</span><span class="sxs-lookup"><span data-stu-id="6fcf5-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fcf5-104">Vous devez configurer un calendrier et l’associer à un employé ou à un employé.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="6fcf5-105">Le calendrier permet de planifier le projet et le temps de travail des ressources réservées au projet.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="6fcf5-106">Lors de la configuration du calendrier, les chefs de projet peuvent effectuer un nivellement des ressources dans le cadre de l’optimisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="6fcf5-107">En fonction du calendrier du calendrier, des restrictions peuvent être appliquées aux ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="6fcf5-108">Vous pouvez configurer un calendrier sur la page **Calendriers**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="6fcf5-109">Lorsque vous configurez un employé en tant que ressource de projet, vous pouvez choisir parmi les employés qui travaillent dans l’entreprise pour laquelle vous configurez des ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="6fcf5-110">Vous pouvez également sélectionner des employés d’autres sociétés de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="6fcf5-111">Ces employés sont appelés ressources intersociétés.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="6fcf5-112">Les procédures suivantes expliquent comment configurer un employé en tant que ressource de projet dans votre entreprise et comment configurer une ressource de projet intersociétés.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="6fcf5-113">Configurer un employé en tant que ressource de projet</span><span class="sxs-lookup"><span data-stu-id="6fcf5-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="6fcf5-114">Sur la page **Employés** , dans la liste **Employés** , sélectionnez l’employé que vous ajoutez en tant que ressource de projet et ouvrez l’enregistrement de l’employé.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="6fcf5-115">Dans le volet Actions, sélectionnez **Projet** &gt;**Configurer** &gt; **Configuration du projet**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="6fcf5-116">Sélectionnez un calendrier, puis fermez la page.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="6fcf5-117">Vous pouvez également spécifier des projets par défaut pour une ressource en tant que type de pré-affectation.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="6fcf5-118">Les pré-affectations peuvent être utilisées lorsque le responsable de ressources ou le chef de projet sait à l’avance sur quels projets la ressource travaillera.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="6fcf5-119">Les pré-affectations peuvent être également basées sur la demande d’un commanditaire ou d’un client.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="6fcf5-120">Pour pré-attribuer un projet, sur la page **Attribuer des projets** , sur l’onglet **Projets** , dans la liste **Projets restants** , sélectionnez le projet approprié.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="6fcf5-121">Configurer une ressource intersociétés</span><span class="sxs-lookup"><span data-stu-id="6fcf5-121">Set up an intercompany resource</span></span>

<span data-ttu-id="6fcf5-122">Lorsque vous configurez un employé en tant que ressource intersociétés, vous devez terminer la configuration à la fois dans la société prêteuse et dans la société emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="6fcf5-123">Dans la société de prêt</span><span class="sxs-lookup"><span data-stu-id="6fcf5-123">In the lending company</span></span>

1. <span data-ttu-id="6fcf5-124">Dans Finance, vérifiez que la société de prêt est sélectionnée, puis suivez la procédure de la section précédente, « Configurer un employé en tant que ressource de projet ».</span><span class="sxs-lookup"><span data-stu-id="6fcf5-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="6fcf5-125">Sur la page **Comptabilité intersociétés** , sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="6fcf5-126">Dans le champ **ID d’entité juridique** , sélectionnez la société prêteuse.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="6fcf5-127">Complétez les champs restants, le cas échéant, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="6fcf5-128">Sur la page **Prix du transfert** , sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="6fcf5-129">Dans le champ **Entité juridique emprunteuse** , sélectionnez la société appropriée.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="6fcf5-130">Pour prêter à la société emprunteuse uniquement la ressource que vous avez créée au début de cette section, dans le champ **Ressource** , sélectionnez le nom de la ressource que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="6fcf5-131">Pour mettre toutes les ressources de la société prêteuse à disposition de la société emprunteuse, laissez le champ **Ressource** vide.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="6fcf5-132">Sur la page **Gestion de projet et comptabilité** , sur l’onglet **Intersociétés** , définissez l’option **Activer la planification des ressources et les feuilles de temps intersociétés** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="6fcf5-133">Dans la société emprunteuse</span><span class="sxs-lookup"><span data-stu-id="6fcf5-133">In the borrowing company</span></span>

- <span data-ttu-id="6fcf5-134">Sur la page **Liste des ressources** , dans le filtre de recherche, saisissez le nom de la ressource que vous avez créée pour la société prêteuse, afin de vérifier que le nom est inclus dans la liste des ressources de la société emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="6fcf5-135">Demander des ressources de projet</span><span class="sxs-lookup"><span data-stu-id="6fcf5-135">Request project resources</span></span>
<span data-ttu-id="6fcf5-136">La fonctionnalité de planification des ressources de projet permet uniquement aux responsables des ressources de distribuer les ressources en personnel sur les engagements ou les projets.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="6fcf5-137">Pour activer cette fonctionnalité, effectuez les tâches suivantes ou vérifiez qu’elles ont été effectuées :</span><span class="sxs-lookup"><span data-stu-id="6fcf5-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="6fcf5-138">Configurez des séquences de numéros.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-138">Set up number sequences.</span></span>
- <span data-ttu-id="6fcf5-139">Configurer les workflows de gestion et de comptabilité des projets</span><span class="sxs-lookup"><span data-stu-id="6fcf5-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="6fcf5-140">Activez les workflows de demande de ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-140">Enable resource request workflows.</span></span>

<span data-ttu-id="6fcf5-141">Une fois les tâches précédentes terminées, vous pouvez effectuer les tâches suivantes selon vos besoins :</span><span class="sxs-lookup"><span data-stu-id="6fcf5-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="6fcf5-142">Créez une demande de ressource à partir d’une ressource à réservation souple.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="6fcf5-143">Surveillez les demandes de ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-143">Monitor resource requests.</span></span>
- <span data-ttu-id="6fcf5-144">Répondez aux demandes de ressources.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="6fcf5-145">Demandez une ressource en personnel à une structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="6fcf5-146">Réservez des ressources pour un projet sans avoir de demande de ressource en personnel.</span><span class="sxs-lookup"><span data-stu-id="6fcf5-146">Book resources to a project without having a request for a staffed resource.</span></span>
