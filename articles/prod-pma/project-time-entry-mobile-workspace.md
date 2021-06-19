---
title: Espace de travail mobile de saisie des heures de projet
description: Cette rubrique donne des informations sur l’espace de travail mobile de saisie des heures de projet. Cet espace de travail permet aux utilisateurs de saisir et de gagner du temps sur un projet en utilisant leur appareil mobile.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009928"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="fb4a5-104">Espace de travail mobile de saisie des heures de projet</span><span class="sxs-lookup"><span data-stu-id="fb4a5-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb4a5-105">Cette rubrique donne des informations sur l’espace de travail mobile de **saisie des heures de projet**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="fb4a5-106">Cet espace de travail permet aux utilisateurs de saisir et de gagner du temps sur un projet en utilisant leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="fb4a5-107">Cet espace de travail mobile est destiné à être utilisé avec l’application mobile Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="fb4a5-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="fb4a5-108">Overview</span></span>
<span data-ttu-id="fb4a5-109">Dans le cadre de leur travail quotidien, les ressources du projet sont souvent sur place ou en déplacement.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="fb4a5-110">L’espace de travail mobile **Entrée d’heure du projet** permet aux utilisateurs d’entrer leur temps facturable ou non facturable par rapport à un projet sur l’appareil mobile de leur choix.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="fb4a5-111">Par conséquent, les ressources du projet peuvent enregistrer des entrées des temps à tout moment et n’importe où.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="fb4a5-112">Elles peuvent également afficher les entrées des temps qui ont déjà été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="fb4a5-113">Plus précisément, dans l’espace de travail mobile **Entrée d’heure du projet**, les utilisateurs peuvent effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb4a5-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="fb4a5-114">Pour n’importe quelle date sélectionnée, entrer le nombre d’heures passé sur une tâche spécifique.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="fb4a5-115">Effectuer une recherche par nom de projet ou par client pour trouver le projet pour lequel entrer des heures.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="fb4a5-116">Spécifier la catégorie et l’activité pour les heures passées.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="fb4a5-117">Enregistrez le temps comme facturable ou non facturable pour le projet.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="fb4a5-118">Facultatif : saisissez des commentaires externes et internes.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fb4a5-119">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="fb4a5-119">Prerequisites</span></span>
<span data-ttu-id="fb4a5-120">Les conditions préalables varient en fonction de la version de Microsoft Dynamics 365 qui a été déployée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="fb4a5-121">Prérequis si vous utilisez Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fb4a5-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="fb4a5-122">Si Finance a été déployé pour votre organisation, l’administrateur système doit publier l’espace de travail mobile **Saisies des heures de projet**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="fb4a5-123">Pour obtenir des instructions, consultez [Publier un espace de travail mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="fb4a5-123">For instructions, see [Publish a mobile workspace](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="fb4a5-124">Conditions préalables si vous utilisez la version 1611 avec Platform update 3 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb4a5-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="fb4a5-125">Si la version 1611 avec Platform update 3 ou version ultérieure a été déployée pour votre organisation, l’administrateur système doit remplir les conditions préalables suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fb4a5-126">Éléments requis</span><span class="sxs-lookup"><span data-stu-id="fb4a5-126">Prerequisite</span></span></th>
<th><span data-ttu-id="fb4a5-127">Rôle</span><span class="sxs-lookup"><span data-stu-id="fb4a5-127">Role</span></span></th>
<th><span data-ttu-id="fb4a5-128">Description</span><span class="sxs-lookup"><span data-stu-id="fb4a5-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="fb4a5-129">Implémentez KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="fb4a5-130">Administrateur système</span><span class="sxs-lookup"><span data-stu-id="fb4a5-130">System administrator</span></span></td>
<td><span data-ttu-id="fb4a5-131">KB 4018050 est une mise à jour X++ ou un correctif de métadonnées qui contient l’espace de travail mobile <strong>Saisie des heures de projet</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="fb4a5-132">Pour implémenter KB 4018050, votre administrateur système doit procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="fb4a5-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Téléchargez le correctif des métadonnées à partir de Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-133"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="fb4a5-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installez le correctif des métadonnées</a>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-134"><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="fb4a5-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Créez un package déployable</a> qui contient les modèles <strong>ApplicationSuite</strong> et <strong>ProjectMobile</strong>, puis téléchargez le package déployable sur LCS.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-135"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="fb4a5-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Appliquez le package déployable</a>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-136"><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb4a5-137">Publiez l’espace de travail mobile de <strong>Saisie des heures de projet</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="fb4a5-138">Administrateur système</span><span class="sxs-lookup"><span data-stu-id="fb4a5-138">System administrator</span></span></td>
<td><span data-ttu-id="fb4a5-139">Voir <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publier un espace de travail mobile</a>.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-139">See <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="fb4a5-140">Télécharger et installer l’application mobile</span><span class="sxs-lookup"><span data-stu-id="fb4a5-140">Download and install the mobile app</span></span>

<span data-ttu-id="fb4a5-141">Télécharger et installer l’application mobile Finance and Operations :</span><span class="sxs-lookup"><span data-stu-id="fb4a5-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="fb4a5-142">Pour les téléphones Android</span><span class="sxs-lookup"><span data-stu-id="fb4a5-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="fb4a5-143">Pour les iPhones</span><span class="sxs-lookup"><span data-stu-id="fb4a5-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="fb4a5-144">Se connecter à l’application mobile</span><span class="sxs-lookup"><span data-stu-id="fb4a5-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="fb4a5-145">Démarrez l’application sur votre appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="fb4a5-146">Tapez votre URL Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="fb4a5-147">La première fois que vous vous connectez, vous êtes invité à saisir votre nom d’utilisateur et votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="fb4a5-148">Entrez vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="fb4a5-149">Une fois connecté, les espaces de travail disponibles pour votre entreprise s’affichent.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="fb4a5-150">Notez que si votre administrateur système publie un nouvel espace de travail ultérieurement, vous devez actualiser la liste des espaces de travail mobiles.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="fb4a5-151">[![Balayer pour actualiser](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="fb4a5-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="fb4a5-152">Saisir les heures à l’aide de l’espace de travail mobile de saisie des heures de projet</span><span class="sxs-lookup"><span data-stu-id="fb4a5-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="fb4a5-153">Sur votre appareil mobile, sélectionnez l’espace de travail **Saisie des heures de projet**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="fb4a5-154">Sélectionnez **Saisie des heures**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-154">Select **Time entry**.</span></span> <span data-ttu-id="fb4a5-155">Les dates du calendrier de la semaine en cours sont affichées.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="fb4a5-156">Pour une date sélectionnée, sélectionnez **Actions** &gt; **Nouvelle entrée**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="fb4a5-157">Entrez le nombre d’heures à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="fb4a5-158">Sélectionnez le projet pour la saisie des heures.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-158">Select the project for the time entry.</span></span> <span data-ttu-id="fb4a5-159">Une liste affiche les projets chargés dans votre application pour une utilisation hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb4a5-160">Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb4a5-161">Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb4a5-161">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="fb4a5-162">Si votre projet ne figure pas dans la liste, sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb4a5-163">Recherchez par nom ou passez à une recherche par nom de projet ou client.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="fb4a5-164">Sélectionnez une catégorie.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-164">Select a category.</span></span> <span data-ttu-id="fb4a5-165">Une liste affiche les catégories chargées dans votre application pour une utilisation hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb4a5-166">Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb4a5-167">Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb4a5-167">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="fb4a5-168">Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb4a5-169">Recherchez par catégorie ou passez à la recherche par nom de catégorie.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="fb4a5-170">Sélectionnez une activité.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-170">Select an activity.</span></span> <span data-ttu-id="fb4a5-171">Une liste affiche les activités chargées dans votre application pour une utilisation hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="fb4a5-172">Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="fb4a5-173">Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="fb4a5-173">For more information, see [Mobile platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="fb4a5-174">Si votre activité ne figure pas dans la liste, sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="fb4a5-175">Recherchez par numéro d’activité ou passez à la recherche par objectif.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="fb4a5-176">Sélectionnez la propriété de ligne.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-176">Select the line property.</span></span>
12. <span data-ttu-id="fb4a5-177">Facultatif : saisissez des commentaires externes et internes.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="fb4a5-178">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="fb4a5-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]