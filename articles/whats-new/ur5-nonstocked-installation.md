---
title: Mettre à jour Project Operations dans votre environnement Finance
description: Cette rubrique fournit des informations sur la façon de mettre à jour Project Operations dans votre environnement Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011053"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="40cbe-103">Mettre à jour Project Operations dans votre environnement Finance</span><span class="sxs-lookup"><span data-stu-id="40cbe-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="40cbe-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="40cbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="40cbe-105">Cette rubrique fournit des informations sur la façon de mettre à jour Dynamics 365 Project Operations dans votre environnement Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="40cbe-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="40cbe-106">Trois procédures sont nécessaires pour mettre à jour Project Operations vers la mise à jour 5 (UR5) :</span><span class="sxs-lookup"><span data-stu-id="40cbe-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="40cbe-107">Importez le package dans votre projet de prévisualisation</span><span class="sxs-lookup"><span data-stu-id="40cbe-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="40cbe-108">Appliquez la mise à jour</span><span class="sxs-lookup"><span data-stu-id="40cbe-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="40cbe-109">Mettez à jour votre environnement Dataverse</span><span class="sxs-lookup"><span data-stu-id="40cbe-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="40cbe-110">Importez le package dans votre projet LCS</span><span class="sxs-lookup"><span data-stu-id="40cbe-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="40cbe-111">Se connecter à [Lifecycle Services (LCS)](https://lcs.dynamics.com/) en tant que propriétaire de projet ou responsable environnement.</span><span class="sxs-lookup"><span data-stu-id="40cbe-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="40cbe-112">Dans la liste de vos projets, sélectionnez votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="40cbe-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="40cbe-113">Sur la page **Projet**, dans le groupe **Environnements**, ouvrez l’environnement que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="40cbe-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="40cbe-114">Assurez-vous que l’environnement s’exécute.</span><span class="sxs-lookup"><span data-stu-id="40cbe-114">Verify that the environment is running.</span></span> <span data-ttu-id="40cbe-115">S’il n’est pas démarré, démarrez l’environnement.</span><span class="sxs-lookup"><span data-stu-id="40cbe-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="40cbe-116">Dans la section **Nouvelle version** sous **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour** pour 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="40cbe-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Bouton Afficher la mise à jour](media/view-update.png)

6. <span data-ttu-id="40cbe-118">Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="40cbe-119">Sur la page **Consulter et enregistrer les mises à jour**, cliquez sur **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="40cbe-120">Sur le volet **Enregistrer le package dans la bibliothèque d’actifs** qui s’ouvre, saisissez le nom du package, puis cliquez sur **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="40cbe-121">Lorsque LCS a terminé d’enregistrer le package, le bouton **Terminé** est activé.</span><span class="sxs-lookup"><span data-stu-id="40cbe-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="40cbe-122">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-122">Select **Done**.</span></span> <span data-ttu-id="40cbe-123">LCS vérifiera le package.</span><span class="sxs-lookup"><span data-stu-id="40cbe-123">LCS will verify the package.</span></span> <span data-ttu-id="40cbe-124">La vérification peut prendre quelques minutes ou jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="40cbe-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="40cbe-125">Appliquez la mise à jour du package</span><span class="sxs-lookup"><span data-stu-id="40cbe-125">Apply the package update</span></span>

1. <span data-ttu-id="40cbe-126">Dans LCS, sur la page **Détails de l’environnement**, sélectionnez **Mettre à jour** > **Appliquer les mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="40cbe-127">Dans la liste, sélectionnez le package que vous avez enregistré précédemment, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="40cbe-128">Cliquez sur **Oui** pour confirmer le déploiement du package.</span><span class="sxs-lookup"><span data-stu-id="40cbe-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Boîte de dialogue Confirmer le déploiement du package](media/confirm-package-deployment.png)

4. <span data-ttu-id="40cbe-130">Cliquez sur **Oui** pour confirmer la mise à jour de l’application.</span><span class="sxs-lookup"><span data-stu-id="40cbe-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Boîte de dialogue Confirmer la mise à jour de l’application](media/confirm-application-update.png)

<span data-ttu-id="40cbe-132">Le déploiement et la mise à jour de l’application commenceront.</span><span class="sxs-lookup"><span data-stu-id="40cbe-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="40cbe-133">Sur la page **Détails de l’environnement**, dans le coin supérieur droit, le statut de l’environnement sera mis à jour sur **Maintenance**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="40cbe-134">Dans environ deux heures, la mise à jour sera terminée.</span><span class="sxs-lookup"><span data-stu-id="40cbe-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="40cbe-135">Les informations de version de l’application seront mises à jour pour **Microsoft Dynamics 365 for Finance and Operations 10.0.15** et le statut de l’environnement sera mis à jour sur **Déployé**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="40cbe-136">Mettez à jour votre environnement Dataverse</span><span class="sxs-lookup"><span data-stu-id="40cbe-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="40cbe-137">Connectez-vous au [centre d’administration Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="40cbe-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="40cbe-138">Dans la liste, recherchez et ouvrez l’environnement que vous avez utilisé pour installer Project Operations.</span><span class="sxs-lookup"><span data-stu-id="40cbe-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="40cbe-139">Sur la page **Environnements**, sélectionnez **Ressource** > **Applications Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="40cbe-140">Dans la liste, recherchez **Microsoft Dynamics 365 Project Operations**, et dans la colonne **Statut**, sélectionnez **Mise à jour disponible**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="40cbe-141">Cochez la case **J’accepte les conditions d’utilisation**, puis sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="40cbe-142">La dernière version de la solution sera installée.</span><span class="sxs-lookup"><span data-stu-id="40cbe-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="40cbe-143">Une fois l’installation terminée, vous aurez la version 4.5.0.134 installée.</span><span class="sxs-lookup"><span data-stu-id="40cbe-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="40cbe-144">Configurer de nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="40cbe-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="40cbe-145">Activer le mappage de la double écriture</span><span class="sxs-lookup"><span data-stu-id="40cbe-145">Enable dual-write mapping</span></span>

<span data-ttu-id="40cbe-146">Après avoir terminé la mise à jour sur les environnements Finance et Dataverse, vous pouvez activer les mappages à double écriture requis.</span><span class="sxs-lookup"><span data-stu-id="40cbe-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="40cbe-147">Terminez les procédures suivantes pour activer les mappages de table de double écriture.</span><span class="sxs-lookup"><span data-stu-id="40cbe-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="40cbe-148">Mettre à jour les paramètres de sécurité sur l’environnement Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="40cbe-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="40cbe-149">Actualiser les entités de données</span><span class="sxs-lookup"><span data-stu-id="40cbe-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="40cbe-150">Mettez à jour et exécutez les mappages en double écriture</span><span class="sxs-lookup"><span data-stu-id="40cbe-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="40cbe-151">Mettre à jour les paramètres de sécurité sur l’environnement Dataverse</span><span class="sxs-lookup"><span data-stu-id="40cbe-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="40cbe-152">Les mises à jour suivantes des privilèges de sécurité pour les entités sont requises dans le cadre de la mise à jour vers UR5.</span><span class="sxs-lookup"><span data-stu-id="40cbe-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="40cbe-153">Dans votre environnement Dataverse, allez à **Paramètres**, et dans le groupe **Système**, sélectionnez **Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Paramètres de l’environnement Dataverse](media/Picture21.png)

2. <span data-ttu-id="40cbe-155">Sélectionnez **Rôles de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="40cbe-156">Dans la liste des rôles, sélectionnez **Utilisateur d’application à double écriture** et sélectionnez l’onglet **Entités personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="40cbe-157">Vérifiez que le rôle a les autorisations en **Lecture** et **Ajouter à** pour :</span><span class="sxs-lookup"><span data-stu-id="40cbe-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="40cbe-158">**Type de taux de change devise**</span><span class="sxs-lookup"><span data-stu-id="40cbe-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="40cbe-159">**Plan comptable**</span><span class="sxs-lookup"><span data-stu-id="40cbe-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="40cbe-160">**Calendrier fiscal**</span><span class="sxs-lookup"><span data-stu-id="40cbe-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="40cbe-161">**Registre**</span><span class="sxs-lookup"><span data-stu-id="40cbe-161">**Ledger**</span></span>

5. <span data-ttu-id="40cbe-162">Une fois le rôle de sécurité mis à jour, accédez à **Paramètres** > **Sécurité** > **Équipes**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="40cbe-163">Vérifiez que le rôle **Utilisateur d’application à double écriture** a été appliqué à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="40cbe-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="40cbe-164">Actualiser les entités de données à partir de la mise à jour</span><span class="sxs-lookup"><span data-stu-id="40cbe-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="40cbe-165">Dans votre environnement Finance, ouvrez l’espace de travail **Gestion de données**, puis ouvrez la page **Paramètres du cadre**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="40cbe-166">Sur l’onglet **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="40cbe-167">Sélectionnez **Fermer** pour confirmer l’actualisation de l’entité.</span><span class="sxs-lookup"><span data-stu-id="40cbe-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="40cbe-168">Ce processus prendra environ 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="40cbe-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="40cbe-169">Vous serez averti lorsque l’actualisation sera terminée.</span><span class="sxs-lookup"><span data-stu-id="40cbe-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="40cbe-170">Mettre à jour les mappages de la double écriture</span><span class="sxs-lookup"><span data-stu-id="40cbe-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="40cbe-171">Dans l’espace de travail **Gestion des données**, sélectionnez **Double écriture**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="40cbe-172">Sélectionnez **Appliquer des solutions**, sélectionnez les deux solutions dans la liste, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="40cbe-173">Sur la page **Double écriture**, sélectionnez les cartes de table suivantes, puis sélectionnez **Arrêter**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="40cbe-174">**Intégration des chiffres réels Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="40cbe-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="40cbe-175">**Catégories de dépenses de projet d’intégration de Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="40cbe-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="40cbe-176">**Catégories de l’entité d’exportation des dépenses de projet de chiffres réels d’intégration de Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="40cbe-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="40cbe-177">Sur la page **Version carte de table**, appliquez une nouvelle version de la carte à chacune des trois entités.</span><span class="sxs-lookup"><span data-stu-id="40cbe-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="40cbe-178">Sur la page **Double écriture**, sélectionnez Exécuter pour redémarrer les cartes.</span><span class="sxs-lookup"><span data-stu-id="40cbe-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="40cbe-179">Dans la liste des cartes, sélectionnez la carte **Registre (msdyn_ledgers)** avec tous les prérequis et cocher la case **Synchronisation initiale**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="40cbe-180">Dans le champ **Maître pour la synchronisation initiale**, sélectionnez **Applications Finance and Operations** puis sélectionnez **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="40cbe-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronisation de la carte du registre](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]