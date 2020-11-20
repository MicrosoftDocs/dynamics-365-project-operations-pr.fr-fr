---
title: Mettre en service un nouvel environnement
description: Cette rubrique fournit des informations sur la mise en service d’un nouvel environnement Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121170"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="2b5fe-103">Mettre en service un nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="2b5fe-103">Provision a new environment</span></span>

<span data-ttu-id="2b5fe-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="2b5fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b5fe-105">Cette rubrique fournit des informations sur la façon de mettre en service un nouvel environnement Dynamics 365 Project Operations pour les scénarios basés sur les ressources/non stockés.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="2b5fe-106">Activer la mise en service automatisée de Project Operations dans un projet LCS</span><span class="sxs-lookup"><span data-stu-id="2b5fe-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="2b5fe-107">Utilisez les étapes suivantes pour activer le flux de mise en service automatisé de Project Operations pour votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="2b5fe-108">Accédez à [LCS](https://lcs.dynamics.com/v2) et sélectionnez la vignette **Gestion des fonctionnalités d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="2b5fe-109">Dans la liste **Fonctionnalité d’évaluation**, sélectionnez **Fonctionnalité Project Operations**, puis sélectionnez **Fonctionnalité d’évaluation activée** pour activer Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="2b5fe-110">Cette étape n’est effectuée qu’une seule fois par projet LCS.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="2b5fe-111">Mettre en service un environnement Project Operations</span><span class="sxs-lookup"><span data-stu-id="2b5fe-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="2b5fe-112">Ouvrez un nouveau déploiement [d’environnement de démonstration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ou [d’environnement bac à sable/de production](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="2b5fe-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="2b5fe-113">Parcourez l’Assistant **Mise en service d’environnement**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2b5fe-114">Assurez-vous que la version de l’application sélectionnée est 10.0.13 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="2b5fe-115">Pour mettre en service Project Operations, sous **Paramètres avancés**, sélectionnez **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="2b5fe-116">Activez le **paramètre Common Data Service** en sélectionnant **Oui**, puis entrez les informations dans les champs obligatoires :</span><span class="sxs-lookup"><span data-stu-id="2b5fe-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="2b5fe-117">Nom</span><span class="sxs-lookup"><span data-stu-id="2b5fe-117">Name</span></span>
  - <span data-ttu-id="2b5fe-118">Région</span><span class="sxs-lookup"><span data-stu-id="2b5fe-118">Region</span></span>
  - <span data-ttu-id="2b5fe-119">Langage</span><span class="sxs-lookup"><span data-stu-id="2b5fe-119">Language</span></span>
  - <span data-ttu-id="2b5fe-120">Devise</span><span class="sxs-lookup"><span data-stu-id="2b5fe-120">Currency</span></span>
 
5. <span data-ttu-id="2b5fe-121">Dans le champ **Modèle Common Data Service**, sélectionnez **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="2b5fe-122">Sélectionnez le type d’environnement pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="2b5fe-123">Un essai basé sur un abonnement vous permettra de déployer un environnement CDS pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Paramètres de déploiement](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="2b5fe-125">Sélectionnez **J’accepte** pour accepter les conditions d’utilisation, puis sélectionnez **Terminé** pour revenir aux paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentement au déploiement](./media/2DeploymentConsent.png)

7. <span data-ttu-id="2b5fe-127">Renseignez les champs obligatoires restants dans l’Assistant et confirmez le déploiement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="2b5fe-128">Le délai de mise en service de l’environnement varie en fonction du type d’environnement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="2b5fe-129">La mise en service peut prendre jusqu’à six heures.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="2b5fe-130">Une fois le déploiement terminé, l’environnement apparaîtra comme **Déployé**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="2b5fe-131">Pour confirmer que l’environnement a été déployé avec succès, sélectionnez **Connexion** et connectez-vous à l’environnement pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Détails de l’environnement](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="2b5fe-133">Appliquer des données de démonstration Finance à Project Operations (étape facultative)</span><span class="sxs-lookup"><span data-stu-id="2b5fe-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="2b5fe-134">Appliquez des données de démonstration de Finance Project Operations à l’environnement hébergé par le cloud, version de service 10.0.13 comme décrit dans [cet article](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="2b5fe-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="2b5fe-135">Appliquer des mises à jour à l’environnement Finance</span><span class="sxs-lookup"><span data-stu-id="2b5fe-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="2b5fe-136">Project Operations nécessite un environnement Finance avec la version de l’application **10.0.13 (10.0.569.20009)** ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="2b5fe-137">Vous devrez peut-être appliquer des mises à jour de qualité à votre environnement Finance pour recevoir cette version.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="2b5fe-138">Dans LCS, sur la page **Détails de l’environnement**, dans la section **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Afficher les mises à jour](./media/5ViewUpdates.png)

2. <span data-ttu-id="2b5fe-140">Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package.**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-140">On the **Binary updates** page, select **Save package.**</span></span>

![Enregistrer le package](./media/6SavePackage.png)

3. <span data-ttu-id="2b5fe-142">Cliquez sur **Sélectionner tout** et **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-142">Click **Select all** and then select **Save package**.</span></span>

![Relire et enregistrer les mises à jour](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="2b5fe-144">Saisissez un nom et une description du package, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="2b5fe-145">Selon la connexion Internet, ce processus peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-145">Depending on the internet connection, this process might take some time.</span></span>

![Charger le package dans la Bibliothèque d’actifs](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="2b5fe-147">Une fois le package enregistré, sélectionnez **Terminé** et enregistrez ce package dans la Bibliothèque d’actifs de votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="2b5fe-148">L’enregistrement et la validation du package peuvent prendre environ 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="2b5fe-149">Pour appliquer la mise à jour, accédez à la page **Détails de l’environnement** dans LCS, sélectionnez **Gérer** > **Appliquer les mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Gérer des environnements](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="2b5fe-151">Dans la liste des mises à jour, sélectionnez le package que vous avez créé et sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Appliquez les mises à jour](./media/10ApplyUpdates.png)

<span data-ttu-id="2b5fe-153">La maintenance de l’environnement prendra un certain temps.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-153">Environment servicing will take some time.</span></span> <span data-ttu-id="2b5fe-154">Une fois terminé, l’environnement retournera à un état déployé.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-154">After it is complete, the environment will return to a deployed state.</span></span>

![Environnement déployé](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="2b5fe-156">Établir une connexion en double écriture</span><span class="sxs-lookup"><span data-stu-id="2b5fe-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="2b5fe-157">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="2b5fe-158">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="2b5fe-159">Une fois le lien créé, sélectionnez à nouveau **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="2b5fe-160">Vous serez redirigé vers Double écriture dans Finance.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-160">You will be redirected to Dual Write in Finance.</span></span>

![Lien vers CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="2b5fe-162">Sélectionnez **Appliquer la solution** pour accéder aux entités qui seront mappées dans l’intégration.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Appliquer des solutions](./media/13ApplySolutions.png)

5. <span data-ttu-id="2b5fe-164">Sélectionnez les deux solutions, **Mappage d’entités de double écriture Dynamics 365 Finance and Operations** et **Mappage d’entités de double écriture Dynamics 365 Project Operations**, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmer des solutions](./media/14ConfirmSolutions.png)

<span data-ttu-id="2b5fe-166">Une fois les solutions appliquées, les entités Double écriture sont appliquées à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Application des solutions](./media/15ApplyingSolutions.png)

<span data-ttu-id="2b5fe-168">Une fois les entités appliquées, tous les mappages disponibles sont répertoriés dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mappages de double écriture](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="2b5fe-170">Actualiser les entités de données après la mise à jour</span><span class="sxs-lookup"><span data-stu-id="2b5fe-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="2b5fe-171">Dans Finance, accédez à l’espace de travail **Gestion des données**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-171">In Finance, go to the **Data management** workspace.</span></span>

![Espace de travail de la gestion de données](./media/16DataManagement.png)

2. <span data-ttu-id="2b5fe-173">Sélectionnez la vignette **Paramètres du cadre**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-173">Select the **Framework parameters** tile.</span></span>

![Paramètres du cadre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="2b5fe-175">Sur la page **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualiser la liste des entités](./media/18RefreshEntityList.png)

<span data-ttu-id="2b5fe-177">L’actualisation prendra environ 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="2b5fe-178">Vous recevrez une alerte lorsqu’elle sera terminée.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-178">You will receive an alert when it is complete.</span></span>

![Confirmer l’actualisation](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="2b5fe-180">Exécuter les mappages d’écriture double Project Operations</span><span class="sxs-lookup"><span data-stu-id="2b5fe-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="2b5fe-181">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="2b5fe-182">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="2b5fe-183">Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="2b5fe-184">Démarrez les mappages comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="2b5fe-185">Assurez-vous de suivre la séquence indiquée.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="2b5fe-186">**Mappage d’entité**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-186">**Entity Map**</span></span> | <span data-ttu-id="2b5fe-187">**Actualiser l’entité**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-187">**Refresh entity**</span></span> | <span data-ttu-id="2b5fe-188">**Synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-188">**Initial sync**</span></span> | <span data-ttu-id="2b5fe-189">**Sélection principale pour la synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-189">**Master for initial sync**</span></span> | <span data-ttu-id="2b5fe-190">**Exécuter la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-190">**Run prerequisites**</span></span> | <span data-ttu-id="2b5fe-191">**Synchronisation initiale de la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="2b5fe-192">**Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="2b5fe-193">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-193">No</span></span> | <span data-ttu-id="2b5fe-194">Oui</span><span class="sxs-lookup"><span data-stu-id="2b5fe-194">Yes</span></span> | <span data-ttu-id="2b5fe-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2b5fe-195">Common Data Service</span></span> | <span data-ttu-id="2b5fe-196">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-196">No</span></span> | <span data-ttu-id="2b5fe-197">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-197">N\A</span></span> |
| <span data-ttu-id="2b5fe-198">**Entités juridiques (cdm\_entreprises)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="2b5fe-199">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-199">No</span></span> | <span data-ttu-id="2b5fe-200">Oui</span><span class="sxs-lookup"><span data-stu-id="2b5fe-200">Yes</span></span> | <span data-ttu-id="2b5fe-201">Applications Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2b5fe-201">Finance and Operations apps</span></span> | <span data-ttu-id="2b5fe-202">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-202">No</span></span> | <span data-ttu-id="2b5fe-203">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-203">N\A</span></span> |
| <span data-ttu-id="2b5fe-204">**Intégration des chiffres réels Project Operations (msdyn\_chiffres réels)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="2b5fe-205">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-205">No</span></span> | <span data-ttu-id="2b5fe-206">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-206">No</span></span> | <span data-ttu-id="2b5fe-207">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-207">N\A</span></span> | <span data-ttu-id="2b5fe-208">Oui</span><span class="sxs-lookup"><span data-stu-id="2b5fe-208">Yes</span></span> | <span data-ttu-id="2b5fe-209">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-209">No</span></span> |
| <span data-ttu-id="2b5fe-210">**Lignes du contrat de projet (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="2b5fe-211">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-211">No</span></span> | <span data-ttu-id="2b5fe-212">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-212">No</span></span> | <span data-ttu-id="2b5fe-213">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-213">N\A</span></span> | <span data-ttu-id="2b5fe-214">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-214">No</span></span> | <span data-ttu-id="2b5fe-215">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-215">No</span></span> |
| <span data-ttu-id="2b5fe-216">**Entité d’intégration pour les relations de transaction du projet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="2b5fe-217">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-217">No</span></span> | <span data-ttu-id="2b5fe-218">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-218">No</span></span> | <span data-ttu-id="2b5fe-219">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-219">N\A</span></span> | <span data-ttu-id="2b5fe-220">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-220">No</span></span> | <span data-ttu-id="2b5fe-221">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-221">N\A</span></span> |
| <span data-ttu-id="2b5fe-222">**Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="2b5fe-223">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-223">No</span></span> | <span data-ttu-id="2b5fe-224">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-224">No</span></span> | <span data-ttu-id="2b5fe-225">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-225">N\A</span></span> | <span data-ttu-id="2b5fe-226">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-226">No</span></span> | <span data-ttu-id="2b5fe-227">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-227">N\A</span></span> |
| <span data-ttu-id="2b5fe-228">**Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="2b5fe-229">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-229">No</span></span> | <span data-ttu-id="2b5fe-230">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-230">No</span></span> | <span data-ttu-id="2b5fe-231">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-231">N\A</span></span> | <span data-ttu-id="2b5fe-232">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-232">No</span></span> | <span data-ttu-id="2b5fe-233">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-233">N\A</span></span> |
| <span data-ttu-id="2b5fe-234">**Entité d’exportation des catégories de dépenses de projet d’intégration de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="2b5fe-235">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-235">No</span></span> | <span data-ttu-id="2b5fe-236">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-236">No</span></span> | <span data-ttu-id="2b5fe-237">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-237">N\A</span></span> | <span data-ttu-id="2b5fe-238">No</span><span class="sxs-lookup"><span data-stu-id="2b5fe-238">No</span></span> | <span data-ttu-id="2b5fe-239">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-239">N\A</span></span> |
| <span data-ttu-id="2b5fe-240">**Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="2b5fe-241">Oui</span><span class="sxs-lookup"><span data-stu-id="2b5fe-241">Yes</span></span> | <span data-ttu-id="2b5fe-242">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-242">No</span></span> | <span data-ttu-id="2b5fe-243">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-243">N\A</span></span> | <span data-ttu-id="2b5fe-244">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-244">No</span></span> | <span data-ttu-id="2b5fe-245">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-245">N\A</span></span> |
| <span data-ttu-id="2b5fe-246">**Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="2b5fe-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="2b5fe-247">Oui</span><span class="sxs-lookup"><span data-stu-id="2b5fe-247">Yes</span></span> | <span data-ttu-id="2b5fe-248">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-248">No</span></span> | <span data-ttu-id="2b5fe-249">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-249">N\A</span></span> | <span data-ttu-id="2b5fe-250">Non</span><span class="sxs-lookup"><span data-stu-id="2b5fe-250">No</span></span> | <span data-ttu-id="2b5fe-251">S. O.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-251">N\A</span></span> |


4. <span data-ttu-id="2b5fe-252">Pour actualiser l’entité, sélectionnez le nom du mappage, puis sélectionnez **Actualiser les entités**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualiser le mappage](./media/20RefreshMapping.png)

5. <span data-ttu-id="2b5fe-254">Une fois l’actualisation terminée, exécutez le mappage.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="2b5fe-255">Avant d’activer le mappage suivant, vérifiez que le mappage du tableau est dans un état de **En cours d’exécution**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="2b5fe-256">L’exécution des mappages avec un plus grand nombre de prérequis peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="2b5fe-257">Pour exécuter un mappage avec des prérequis, activez le bouton de basculement **Afficher les mappages d’entités associés**.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="2b5fe-258">Si le tableau indique que **Synchronisation initiale préalable** est **Non**, vérifiez que l’indicateur **Synchronisation initiale** est **Désactivé** dans tous les mappages de prérequises avant de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Exécuter le mappage](./media/21RunMap.png)

6. <span data-ttu-id="2b5fe-260">Validez que tous les mappages liés au projet sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-260">Validate all project related maps are in the running state.</span></span>

![Tous les mappages en cours d’exécution](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="2b5fe-262">Appliquer les données de configuration dans CDS pour Project Operations (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2b5fe-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="2b5fe-263">Si vous avez appliqué des données de démonstration à l’environnement Finance, consultez [Configurer et appliquer les données de configuration dans Common Data Service pour Project Operations](resource-apply-pro-setup-config-data.md) pour appliquer les données de démonstration à l’environnement CDS.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="2b5fe-264">Votre environnement Project Operations est désormais mis en service et configuré.</span><span class="sxs-lookup"><span data-stu-id="2b5fe-264">Your Project Operations environment is now provisioned and configured.</span></span> 
