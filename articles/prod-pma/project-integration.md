---
title: Intégration de Microsoft Project Client
description: La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche. L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289321"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="16b50-104">Intégration de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16b50-105">La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="16b50-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="16b50-106">L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet.</span><span class="sxs-lookup"><span data-stu-id="16b50-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="16b50-107">Le chef de projet peut publier tout changement dans la structure de répartition du travail du projet Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="16b50-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="16b50-108">Si vous utilisez la mise à jour de juillet (version 10.0.4), vous devez installer KB 4054797 et 4055884.</span><span class="sxs-lookup"><span data-stu-id="16b50-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="16b50-109">Configurer le complément Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="16b50-110">Pour activer l’intégration avec Microsoft Project Client, un complément Microsoft Dynamics 365 doit être installé dans l’application client Microsoft Project de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16b50-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="16b50-111">Cela se fait en ouvrant l’**Espace de travail de gestion de projet**.</span><span class="sxs-lookup"><span data-stu-id="16b50-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="16b50-112">• Cliquez sur **Configurer le complément client du projet** depuis la section **Liens** > **Configurer** de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="16b50-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="16b50-113">• Cliquez sur **Ouvrir**, puis cliquez sur **Exécuter** à l’invite.</span><span class="sxs-lookup"><span data-stu-id="16b50-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="16b50-114">Ouvrir et modifier un brouillon de structure de répartition du travail existant dans Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="16b50-115">Si un projet dans Dynamics 365 Finance a déjà créé une structure de répartition du travail, la structure de répartition du travail peut être ouverte dans l’application Microsoft Project Client si la structure de répartition du travail est à l’état de brouillon.</span><span class="sxs-lookup"><span data-stu-id="16b50-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="16b50-116">Pour ouvrir depuis la page **Projet**, cliquez sur le lien **Ouvrir dans Microsoft Project** depuis l’onglet **Plan**. Cette page peut également être ouverte à partir de l’application Microsoft Project Client en cliquant sur **Ouvrir** dans l’onglet **Microsoft Dynamics 365**. Sélectionnez l’**Entité juridique** et **Projet** depuis la liste.</span><span class="sxs-lookup"><span data-stu-id="16b50-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="16b50-117">Si vous utilisez Internet Explorer comme navigateur, vous devrez cliquer sur **Enregistrer** pour ouvrir manuellement à partir de l’emplacement de téléchargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="16b50-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="16b50-118">Ou cliquez sur **Enregistrer et ouvrir** pour ouvrir le fichier dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="16b50-119">Ne renommez pas le nom du fichier lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="16b50-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="16b50-120">Avant d’apporter des modifications au fichier à l’aide de Microsoft Project Client, vous devez l’extraire. Cliquez sur **Extraire** dans l’onglet **Microsoft Dynamics 365**. Cela empêchera les autres utilisateurs de modifier la structure de répartition du travail à partir de Finance en même temps.</span><span class="sxs-lookup"><span data-stu-id="16b50-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="16b50-121">Pour publier la structure de répartition du travail après avoir effectué les modifications, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="16b50-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="16b50-122">Si une équipe de projet a déjà été ajoutée au projet dans Finance, la liste des ressources sera remplie avec les membres de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="16b50-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="16b50-123">Si une équipe de projet n’a pas encore été ajoutée au projet, vous pouvez sélectionner des ressources et créer l’équipe dans Microsoft Project Client en cliquant sur le bouton **Ressources** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="16b50-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="16b50-124">Les données suivantes seront synchronisées avec Finance dans le cadre du processus d’archivage :</span><span class="sxs-lookup"><span data-stu-id="16b50-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="16b50-125">•   Nom de tâche</span><span class="sxs-lookup"><span data-stu-id="16b50-125">•   Task name</span></span>

<span data-ttu-id="16b50-126">•   Date de début</span><span class="sxs-lookup"><span data-stu-id="16b50-126">•   Start date</span></span>

<span data-ttu-id="16b50-127">•   Date de fin</span><span class="sxs-lookup"><span data-stu-id="16b50-127">•   Finish date</span></span>

<span data-ttu-id="16b50-128">•   Prédécesseurs</span><span class="sxs-lookup"><span data-stu-id="16b50-128">•   Predecessors</span></span>

<span data-ttu-id="16b50-129">•   Noms de ressource</span><span class="sxs-lookup"><span data-stu-id="16b50-129">•   Resource names</span></span>

<span data-ttu-id="16b50-130">•   Catégorie</span><span class="sxs-lookup"><span data-stu-id="16b50-130">•   Category</span></span>

<span data-ttu-id="16b50-131">•   Catégorie de ressources</span><span class="sxs-lookup"><span data-stu-id="16b50-131">•   Resource category</span></span>

<span data-ttu-id="16b50-132">•   Heures de travail</span><span class="sxs-lookup"><span data-stu-id="16b50-132">•   Work hours</span></span>

<span data-ttu-id="16b50-133">•   Remarques</span><span class="sxs-lookup"><span data-stu-id="16b50-133">•   Notes</span></span>

<span data-ttu-id="16b50-134">•   Priorité</span><span class="sxs-lookup"><span data-stu-id="16b50-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="16b50-135">Si vous ajoutez d’autres colonnes à votre fichier Microsoft Project Client, elles ne seront pas enregistrées dans le fichier et ne seront pas affichées lorsque le fichier sera à nouveau ouvert.</span><span class="sxs-lookup"><span data-stu-id="16b50-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="16b50-136">Créer la structure de répartition du travail pour un projet existant à l’aide de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="16b50-137">Pour créer une structure de répartition du travail à l’aide de Microsoft Project Client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="16b50-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="16b50-138">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="16b50-139">Sous l’onglet **Microsoft Dynamics 365**, cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="16b50-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="16b50-140">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="16b50-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="16b50-141">Sélectionnez le **Projet**.</span><span class="sxs-lookup"><span data-stu-id="16b50-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="16b50-142">Cliquez sur **Extraire** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="16b50-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="16b50-143">Lorsque vous êtes prêt à publier dans Finance, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="16b50-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="16b50-144">Remplacer la structure de répartition du travail existante pour un projet existant à l’aide de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="16b50-145">Pour créer une nouvelle structure de répartition du travail à l’aide de Microsoft Project Client et remplacer une structure de répartition du travail existante pour un projet existant, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="16b50-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="16b50-146">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="16b50-147">Créez le programme dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="16b50-148">Sur l’onglet **Microsoft Dynamics 365**, cliquez sur **Enregistrer les modifications** > **Remplacer le projet existant**.</span><span class="sxs-lookup"><span data-stu-id="16b50-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="16b50-149">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="16b50-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="16b50-150">Sélectionnez le **Projet**.</span><span class="sxs-lookup"><span data-stu-id="16b50-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="16b50-151">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="16b50-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="16b50-152">Créer un nouveau projet à partir de Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="16b50-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="16b50-153">Ouvrez Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="16b50-154">Créez le programme dans Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="16b50-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="16b50-155">Sur l’onglet **Microsoft Dynamics 365**, cliquez sur **Enregistrer les modifications** > **Enregistrer dans un nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="16b50-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="16b50-156">Sélectionnez l’**Entité juridique** pour le projet.</span><span class="sxs-lookup"><span data-stu-id="16b50-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="16b50-157">Entrez l’**ID de projet**, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="16b50-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="16b50-158">Entrez le **Nom du produit**.</span><span class="sxs-lookup"><span data-stu-id="16b50-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="16b50-159">Sélectionnez le **Type de projet**, **Groupe de projet** et l’**ID de contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="16b50-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="16b50-160">Vous pouvez également créer un contrat de projet en cliquant sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="16b50-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="16b50-161">Sélectionnez le **Calendrier** à utiliser pour l’allocation des ressources.</span><span class="sxs-lookup"><span data-stu-id="16b50-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="16b50-162">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="16b50-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]