---
title: Mettre en service un nouvel environnement
description: Cette rubrique fournit des informations sur la mise en service d’un nouvel environnement Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949359"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="eb076-103">Mettre en service un nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="eb076-103">Provision a new environment</span></span>

<span data-ttu-id="eb076-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="eb076-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb076-105">Cette rubrique fournit des informations sur la façon de mettre en service un nouvel environnement Dynamics 365 Project Operations pour les scénarios basés sur les ressources/non stockés.</span><span class="sxs-lookup"><span data-stu-id="eb076-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="eb076-106">Activer la mise en service automatisée de Project Operations dans un projet LCS</span><span class="sxs-lookup"><span data-stu-id="eb076-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="eb076-107">Utilisez les étapes suivantes pour activer le flux de mise en service automatisé de Project Operations pour votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="eb076-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="eb076-108">Accédez à [LCS](https://lcs.dynamics.com/v2) et sélectionnez la vignette **Gestion des fonctionnalités d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="eb076-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="eb076-109">Dans la liste **Fonctionnalité d’évaluation**, sélectionnez **Project Operations** et sélectionnez **Fonctionnalité d’évaluation activée** pour activer Project Operations.</span><span class="sxs-lookup"><span data-stu-id="eb076-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="eb076-110">Cette étape n’est effectuée qu’une seule fois par projet LCS.</span><span class="sxs-lookup"><span data-stu-id="eb076-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="eb076-111">Mettre en service un environnement Project Operations</span><span class="sxs-lookup"><span data-stu-id="eb076-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="eb076-112">Ouvrez un nouveau déploiement [d’environnement de démonstration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ou [d’environnement bac à sable/de production](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="eb076-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="eb076-113">Parcourez l’Assistant **Mise en service d’environnement**.</span><span class="sxs-lookup"><span data-stu-id="eb076-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="eb076-114">Assurez-vous que la version de l’application sélectionnée est 10.0.13 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="eb076-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="eb076-115">Pour mettre en service Project Operations, sous **Paramètres avancés**, sélectionnez **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="eb076-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="eb076-116">Activez le **paramètre Common Data Service** en sélectionnant **Oui**, puis entrez les informations dans les champs obligatoires :</span><span class="sxs-lookup"><span data-stu-id="eb076-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="eb076-117">Nom</span><span class="sxs-lookup"><span data-stu-id="eb076-117">Name</span></span>
  - <span data-ttu-id="eb076-118">Région</span><span class="sxs-lookup"><span data-stu-id="eb076-118">Region</span></span>
  - <span data-ttu-id="eb076-119">Langage</span><span class="sxs-lookup"><span data-stu-id="eb076-119">Language</span></span>
  - <span data-ttu-id="eb076-120">Devise</span><span class="sxs-lookup"><span data-stu-id="eb076-120">Currency</span></span>
 
5. <span data-ttu-id="eb076-121">Dans le champ **Modèle Common Data Service**, sélectionnez **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="eb076-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="eb076-122">Sélectionnez le type d’environnement pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="eb076-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="eb076-123">Un essai basé sur un abonnement vous permettra de déployer un environnement CDS pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="eb076-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Paramètres de déploiement](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="eb076-125">Sélectionnez **J’accepte** pour accepter les conditions d’utilisation, puis sélectionnez **Terminé** pour revenir aux paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="eb076-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentement au déploiement](./media/2DeploymentConsent.png)

7. <span data-ttu-id="eb076-127">Renseignez les champs obligatoires restants dans l’Assistant et confirmez le déploiement.</span><span class="sxs-lookup"><span data-stu-id="eb076-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="eb076-128">Le délai de mise en service de l’environnement varie en fonction du type d’environnement.</span><span class="sxs-lookup"><span data-stu-id="eb076-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="eb076-129">La mise en service peut prendre jusqu’à six heures.</span><span class="sxs-lookup"><span data-stu-id="eb076-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="eb076-130">Une fois le déploiement terminé, l’environnement apparaîtra comme **Déployé**.</span><span class="sxs-lookup"><span data-stu-id="eb076-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="eb076-131">Pour confirmer que l’environnement a été déployé avec succès, sélectionnez **Connexion** et connectez-vous à l’environnement pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="eb076-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Détails de l’environnement](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="eb076-133">Appliquer des données de démonstration Finance à Project Operations (étape facultative)</span><span class="sxs-lookup"><span data-stu-id="eb076-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="eb076-134">Appliquez des données de démonstration de Finance Project Operations à l’environnement hébergé par le cloud, version de service 10.0.13 comme décrit dans [cet article](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="eb076-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="eb076-135">Appliquer des mises à jour à l’environnement Finance</span><span class="sxs-lookup"><span data-stu-id="eb076-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="eb076-136">Project Operations nécessite un environnement Finance avec la version de l’application **10.0.13 (10.0.569.20009)** ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb076-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="eb076-137">Vous devrez peut-être appliquer des mises à jour de qualité à votre environnement Finance pour recevoir cette version.</span><span class="sxs-lookup"><span data-stu-id="eb076-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="eb076-138">Dans LCS, sur la page **Détails de l’environnement**, dans la section **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="eb076-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Afficher les mises à jour](./media/5ViewUpdates.png)

2. <span data-ttu-id="eb076-140">Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package.**</span><span class="sxs-lookup"><span data-stu-id="eb076-140">On the **Binary updates** page, select **Save package.**</span></span>

![Enregistrer le package](./media/6SavePackage.png)

3. <span data-ttu-id="eb076-142">Cliquez sur **Sélectionner tout** et **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="eb076-142">Click **Select all** and then select **Save package**.</span></span>

![Relire et enregistrer les mises à jour](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="eb076-144">Saisissez un nom et une description du package, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="eb076-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="eb076-145">Selon la connexion Internet, ce processus peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="eb076-145">Depending on the internet connection, this process might take some time.</span></span>

![Charger le package dans la Bibliothèque d’actifs](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="eb076-147">Une fois le package enregistré, sélectionnez **Terminé** et enregistrez ce package dans la Bibliothèque d’actifs de votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="eb076-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="eb076-148">L’enregistrement et la validation du package peuvent prendre environ 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="eb076-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="eb076-149">Pour appliquer la mise à jour, accédez à la page **Détails de l’environnement** dans LCS, sélectionnez **Gérer** > **Appliquer les mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="eb076-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Gérer des environnements](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="eb076-151">Dans la liste des mises à jour, sélectionnez le package que vous avez créé et sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="eb076-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Appliquez les mises à jour](./media/10ApplyUpdates.png)

<span data-ttu-id="eb076-153">La maintenance de l’environnement prendra un certain temps.</span><span class="sxs-lookup"><span data-stu-id="eb076-153">Environment servicing will take some time.</span></span> <span data-ttu-id="eb076-154">Une fois terminé, l’environnement retournera à un état déployé.</span><span class="sxs-lookup"><span data-stu-id="eb076-154">After it is complete, the environment will return to a deployed state.</span></span>

![Environnement déployé](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="eb076-156">Établir une connexion en double écriture</span><span class="sxs-lookup"><span data-stu-id="eb076-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="eb076-157">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="eb076-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="eb076-158">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="eb076-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="eb076-159">Une fois le lien créé, sélectionnez à nouveau **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="eb076-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="eb076-160">Vous serez redirigé vers Double écriture dans Finance.</span><span class="sxs-lookup"><span data-stu-id="eb076-160">You will be redirected to Dual Write in Finance.</span></span>

![Lien vers CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="eb076-162">Sélectionnez **Appliquer la solution** pour accéder aux entités qui seront mappées dans l’intégration.</span><span class="sxs-lookup"><span data-stu-id="eb076-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Appliquer des solutions](./media/13ApplySolutions.png)

5. <span data-ttu-id="eb076-164">Sélectionnez les deux solutions, **Mappage d’entités de double écriture Dynamics 365 Finance and Operations** et **Mappage d’entités de double écriture Dynamics 365 Project Operations**, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="eb076-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmer des solutions](./media/14ConfirmSolutions.png)

<span data-ttu-id="eb076-166">Une fois les solutions appliquées, les entités Double écriture sont appliquées à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="eb076-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Application des solutions](./media/15ApplyingSolutions.png)

<span data-ttu-id="eb076-168">Une fois les entités appliquées, tous les mappages disponibles sont répertoriés dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="eb076-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mappages de double écriture](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="eb076-170">Actualiser les entités de données après la mise à jour</span><span class="sxs-lookup"><span data-stu-id="eb076-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="eb076-171">Dans Finance, accédez à l’espace de travail **Gestion des données**.</span><span class="sxs-lookup"><span data-stu-id="eb076-171">In Finance, go to the **Data management** workspace.</span></span>

![Espace de travail de la gestion de données](./media/16DataManagement.png)

2. <span data-ttu-id="eb076-173">Sélectionnez la vignette **Paramètres du cadre**.</span><span class="sxs-lookup"><span data-stu-id="eb076-173">Select the **Framework parameters** tile.</span></span>

![Paramètres du cadre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="eb076-175">Sur la page **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.</span><span class="sxs-lookup"><span data-stu-id="eb076-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualiser la liste des entités](./media/18RefreshEntityList.png)

<span data-ttu-id="eb076-177">L’actualisation prendra environ 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="eb076-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="eb076-178">Vous recevrez une alerte lorsqu’elle sera terminée.</span><span class="sxs-lookup"><span data-stu-id="eb076-178">You will receive an alert when it is complete.</span></span>

![Confirmer l’actualisation](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="eb076-180">Exécuter les mappages d’écriture double Project Operations</span><span class="sxs-lookup"><span data-stu-id="eb076-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="eb076-181">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="eb076-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="eb076-182">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="eb076-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="eb076-183">Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.</span><span class="sxs-lookup"><span data-stu-id="eb076-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="eb076-184">Démarrez les mappages comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="eb076-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="eb076-185">Assurez-vous de suivre la séquence indiquée.</span><span class="sxs-lookup"><span data-stu-id="eb076-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="eb076-186">**Mappage d’entité**</span><span class="sxs-lookup"><span data-stu-id="eb076-186">**Entity Map**</span></span> | <span data-ttu-id="eb076-187">**Actualiser l’entité**</span><span class="sxs-lookup"><span data-stu-id="eb076-187">**Refresh entity**</span></span> | <span data-ttu-id="eb076-188">**Synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="eb076-188">**Initial sync**</span></span> | <span data-ttu-id="eb076-189">**Sélection principale pour la synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="eb076-189">**Master for initial sync**</span></span> | <span data-ttu-id="eb076-190">**Exécuter la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="eb076-190">**Run prerequisites**</span></span> | <span data-ttu-id="eb076-191">**Synchronisation initiale de la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="eb076-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="eb076-192">**Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="eb076-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="eb076-193">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-193">No</span></span> | <span data-ttu-id="eb076-194">Oui</span><span class="sxs-lookup"><span data-stu-id="eb076-194">Yes</span></span> | <span data-ttu-id="eb076-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eb076-195">Common Data Service</span></span> | <span data-ttu-id="eb076-196">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-196">No</span></span> | <span data-ttu-id="eb076-197">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-197">N\A</span></span> |
| <span data-ttu-id="eb076-198">**Entités juridiques (cdm\_entreprises)**</span><span class="sxs-lookup"><span data-stu-id="eb076-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="eb076-199">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-199">No</span></span> | <span data-ttu-id="eb076-200">Oui</span><span class="sxs-lookup"><span data-stu-id="eb076-200">Yes</span></span> | <span data-ttu-id="eb076-201">Applications Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="eb076-201">Finance and Operations apps</span></span> | <span data-ttu-id="eb076-202">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-202">No</span></span> | <span data-ttu-id="eb076-203">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-203">N\A</span></span> |
| <span data-ttu-id="eb076-204">**Intégration des chiffres réels Project Operations (msdyn\_chiffres réels)**</span><span class="sxs-lookup"><span data-stu-id="eb076-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="eb076-205">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-205">No</span></span> | <span data-ttu-id="eb076-206">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-206">No</span></span> | <span data-ttu-id="eb076-207">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-207">N\A</span></span> | <span data-ttu-id="eb076-208">Oui</span><span class="sxs-lookup"><span data-stu-id="eb076-208">Yes</span></span> | <span data-ttu-id="eb076-209">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-209">No</span></span> |
| <span data-ttu-id="eb076-210">**Lignes du contrat de projet (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="eb076-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="eb076-211">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-211">No</span></span> | <span data-ttu-id="eb076-212">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-212">No</span></span> | <span data-ttu-id="eb076-213">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-213">N\A</span></span> | <span data-ttu-id="eb076-214">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-214">No</span></span> | <span data-ttu-id="eb076-215">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-215">No</span></span> |
| <span data-ttu-id="eb076-216">**Entité d’intégration pour les relations de transaction du projet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="eb076-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="eb076-217">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-217">No</span></span> | <span data-ttu-id="eb076-218">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-218">No</span></span> | <span data-ttu-id="eb076-219">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-219">N\A</span></span> | <span data-ttu-id="eb076-220">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-220">No</span></span> | <span data-ttu-id="eb076-221">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-221">N\A</span></span> |
| <span data-ttu-id="eb076-222">**Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="eb076-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="eb076-223">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-223">No</span></span> | <span data-ttu-id="eb076-224">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-224">No</span></span> | <span data-ttu-id="eb076-225">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-225">N\A</span></span> | <span data-ttu-id="eb076-226">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-226">No</span></span> | <span data-ttu-id="eb076-227">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-227">N\A</span></span> |
| <span data-ttu-id="eb076-228">**Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="eb076-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="eb076-229">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-229">No</span></span> | <span data-ttu-id="eb076-230">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-230">No</span></span> | <span data-ttu-id="eb076-231">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-231">N\A</span></span> | <span data-ttu-id="eb076-232">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-232">No</span></span> | <span data-ttu-id="eb076-233">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-233">N\A</span></span> |
| <span data-ttu-id="eb076-234">**Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="eb076-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="eb076-235">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-235">No</span></span> | <span data-ttu-id="eb076-236">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-236">No</span></span> | <span data-ttu-id="eb076-237">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-237">N\A</span></span> | <span data-ttu-id="eb076-238">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-238">No</span></span> | <span data-ttu-id="eb076-239">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-239">N\A</span></span> |
| <span data-ttu-id="eb076-240">**Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="eb076-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="eb076-241">Oui</span><span class="sxs-lookup"><span data-stu-id="eb076-241">Yes</span></span> | <span data-ttu-id="eb076-242">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-242">No</span></span> | <span data-ttu-id="eb076-243">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-243">N\A</span></span> | <span data-ttu-id="eb076-244">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-244">No</span></span> | <span data-ttu-id="eb076-245">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-245">N\A</span></span> |
| <span data-ttu-id="eb076-246">**Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="eb076-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="eb076-247">Oui</span><span class="sxs-lookup"><span data-stu-id="eb076-247">Yes</span></span> | <span data-ttu-id="eb076-248">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-248">No</span></span> | <span data-ttu-id="eb076-249">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-249">N\A</span></span> | <span data-ttu-id="eb076-250">Non</span><span class="sxs-lookup"><span data-stu-id="eb076-250">No</span></span> | <span data-ttu-id="eb076-251">S. O.</span><span class="sxs-lookup"><span data-stu-id="eb076-251">N\A</span></span> |

4. <span data-ttu-id="eb076-252">Pour actualiser l’entité, sélectionnez le nom du mappage, puis sélectionnez **Actualiser les entités**.</span><span class="sxs-lookup"><span data-stu-id="eb076-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="eb076-253">Continuez à exécuter le mappage une fois l’actualisation terminée.</span><span class="sxs-lookup"><span data-stu-id="eb076-253">Proceed with running the map after the refresh is complete.</span></span>

![Actualiser le mappage](./media/20RefreshMapping.png)

<span data-ttu-id="eb076-255">Avant d’activer le mappage suivant, vérifiez que le mappage du tableau est dans un état de **En cours d’exécution**.</span><span class="sxs-lookup"><span data-stu-id="eb076-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="eb076-256">L’exécution des mappages avec un plus grand nombre de prérequis peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="eb076-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="eb076-257">Pour exécuter un mappage avec des prérequis, activez le bouton de basculement **Afficher les mappages d’entités associés**.</span><span class="sxs-lookup"><span data-stu-id="eb076-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="eb076-258">Si le tableau indique que **Synchronisation initiale préalable** est **Non**, vérifiez que l’indicateur **Synchronisation initiale** est **Désactivé** dans tous les mappages de prérequises avant de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="eb076-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Exécuter le mappage](./media/21RunMap.png)

6. <span data-ttu-id="eb076-260">Validez que tous les mappages liés au projet sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb076-260">Validate all project related maps are in the running state.</span></span>

![Toutes les mappages en cours d’exécution](./media/22AllMapsRunning.png)

<span data-ttu-id="eb076-262">Votre environnement Project Operations est désormais mis en service et configuré.</span><span class="sxs-lookup"><span data-stu-id="eb076-262">Your Project Operations environment is now provisioned and configured.</span></span>
