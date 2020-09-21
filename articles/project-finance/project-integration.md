---
title: Intégration de Microsoft Project Client
description: La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche. L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168113"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="bddf0-104">Intégration de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bddf0-105">La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="bddf0-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="bddf0-106">L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet.</span><span class="sxs-lookup"><span data-stu-id="bddf0-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="bddf0-107">Le chef de projet peut publier tout changement dans la structure de répartition du travail du projet Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bddf0-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="bddf0-108">Si vous utilisez la mise à jour de juillet (version 10.0.4), vous devez installer KB 4054797 et 4055884.</span><span class="sxs-lookup"><span data-stu-id="bddf0-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="bddf0-109">Configurer le complément Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="bddf0-110">Pour activer l’intégration avec Microsoft Project Client, un complément Microsoft Dynamics 365 doit être installé dans l’application client Microsoft Project de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bddf0-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="bddf0-111">Cela se fait en ouvrant l’**Espace de travail de gestion de projet**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="bddf0-112">• Cliquez sur **Configurer le complément client du projet** depuis la section **Liens** > **Configurer** de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="bddf0-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="bddf0-113">• Cliquez sur **Ouvrir**, puis cliquez sur **Exécuter** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="bddf0-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="bddf0-114">Ouvrir et modifier un brouillon de structure de répartition du travail existant dans Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="bddf0-115">Si un projet dans Dynamics 365 Finance a déjà créé une structure de répartition du travail, la structure de répartition du travail peut être ouverte dans l’application Microsoft Project Client si la structure de répartition du travail est à l’état de brouillon.</span><span class="sxs-lookup"><span data-stu-id="bddf0-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="bddf0-116">Pour ouvrir depuis la page **Projet**, cliquez sur le lien **Ouvrir dans Microsoft Project** depuis l’onglet **Plan**. Cette page peut également être ouverte à partir de l’application Microsoft Project Client en cliquant sur **Ouvrir** dans l’onglet **Microsoft Dynamics 365**. Sélectionnez l’**Entité juridique** et **Projet** depuis la liste.</span><span class="sxs-lookup"><span data-stu-id="bddf0-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="bddf0-117">Si vous utilisez Internet Explorer comme navigateur, vous devrez cliquer sur **Enregistrer** pour ouvrir manuellement à partir de l’emplacement de téléchargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="bddf0-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="bddf0-118">Ou cliquez sur **Enregistrer et ouvrir** pour ouvrir le fichier dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="bddf0-119">Ne renommez pas le nom du fichier lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bddf0-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="bddf0-120">Avant d’apporter des modifications au fichier à l’aide de Microsoft Project Client, vous devez l’extraire. Cliquez sur **Extraire** dans l’onglet **Microsoft Dynamics 365**. Cela empêchera les autres utilisateurs de modifier la structure de répartition du travail à partir de Finance en même temps.</span><span class="sxs-lookup"><span data-stu-id="bddf0-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="bddf0-121">Pour publier la structure de répartition du travail après avoir effectué les modifications, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="bddf0-122">Si une équipe de projet a déjà été ajoutée au projet dans Finance, la liste des ressources sera remplie avec les membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="bddf0-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="bddf0-123">Si une équipe de projet n’a pas encore été ajoutée au projet, vous pouvez sélectionner des ressources et créer l’équipe dans Microsoft Project Client en cliquant sur le bouton **Ressources** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="bddf0-124">Les données suivantes seront synchronisées avec Finance dans le cadre du processus d’archivage :</span><span class="sxs-lookup"><span data-stu-id="bddf0-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="bddf0-125">•   Nom de tâche</span><span class="sxs-lookup"><span data-stu-id="bddf0-125">•   Task name</span></span>

<span data-ttu-id="bddf0-126">•   Date de début</span><span class="sxs-lookup"><span data-stu-id="bddf0-126">•   Start date</span></span>

<span data-ttu-id="bddf0-127">•   Date de fin</span><span class="sxs-lookup"><span data-stu-id="bddf0-127">•   Finish date</span></span>

<span data-ttu-id="bddf0-128">•   Prédécesseurs</span><span class="sxs-lookup"><span data-stu-id="bddf0-128">•   Predecessors</span></span>

<span data-ttu-id="bddf0-129">•   Noms de ressource</span><span class="sxs-lookup"><span data-stu-id="bddf0-129">•   Resource names</span></span>

<span data-ttu-id="bddf0-130">•   Catégorie</span><span class="sxs-lookup"><span data-stu-id="bddf0-130">•   Category</span></span>

<span data-ttu-id="bddf0-131">•   Catégorie de ressources</span><span class="sxs-lookup"><span data-stu-id="bddf0-131">•   Resource category</span></span>

<span data-ttu-id="bddf0-132">•   Heures de travail</span><span class="sxs-lookup"><span data-stu-id="bddf0-132">•   Work hours</span></span>

<span data-ttu-id="bddf0-133">•   Remarques</span><span class="sxs-lookup"><span data-stu-id="bddf0-133">•   Notes</span></span>

<span data-ttu-id="bddf0-134">•   Priorité</span><span class="sxs-lookup"><span data-stu-id="bddf0-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="bddf0-135">Si vous ajoutez d’autres colonnes à votre fichier Microsoft Project Client, elles ne seront pas enregistrées dans le fichier et ne seront pas affichées lorsque le fichier sera à nouveau ouvert.</span><span class="sxs-lookup"><span data-stu-id="bddf0-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bddf0-136">Créer la structure de répartition du travail pour un projet existant à l’aide de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bddf0-137">Pour créer une structure de répartition du travail à l’aide de Microsoft Project Client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bddf0-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="bddf0-138">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bddf0-139">Sous l’onglet **Microsoft Dynamics 365**, cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="bddf0-140">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="bddf0-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="bddf0-141">Sélectionnez le **Projet**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="bddf0-142">Cliquez sur **Extraire** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="bddf0-143">Lorsque vous êtes prêt à publier dans Finance, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bddf0-144">Remplacer la structure de répartition du travail existante pour un projet existant à l’aide de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bddf0-145">Pour créer une nouvelle structure de répartition du travail à l’aide de Microsoft Project Client et remplacer une structure de répartition du travail existante pour un projet existant, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bddf0-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="bddf0-146">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bddf0-147">Créez le programme dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bddf0-148">Sur l’onglet **Microsoft Dynamics 365**, cliquez sur **Enregistrer les modifications** > **Remplacer le projet existant**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="bddf0-149">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="bddf0-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bddf0-150">Sélectionnez le **Projet**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="bddf0-151">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="bddf0-152">Créer un nouveau projet à partir de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bddf0-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="bddf0-153">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bddf0-154">Créez le programme dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bddf0-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bddf0-155">Sur l’onglet **Microsoft Dynamics 365**, cliquez sur **Enregistrer les modifications** > **Enregistrer dans un nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="bddf0-156">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="bddf0-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bddf0-157">Entrez l’**ID de projet**, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bddf0-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="bddf0-158">Entrez le **Nom du produit**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="bddf0-159">Sélectionnez le **Type de projet**, **Groupe de projet** et l’**ID de contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="bddf0-160">Vous pouvez également créer un contrat de projet en cliquant sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="bddf0-161">Sélectionnez le **Calendrier** à utiliser pour l’allocation des ressources.</span><span class="sxs-lookup"><span data-stu-id="bddf0-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="bddf0-162">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bddf0-162">Click **OK**.</span></span>
