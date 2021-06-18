---
title: Mettre en service un nouvel environnement
description: Cette rubrique fournit des informations sur la mise en service d’un nouvel environnement Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995483"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="f5850-103">Mettre en service un nouvel environnement</span><span class="sxs-lookup"><span data-stu-id="f5850-103">Provision a new environment</span></span>

<span data-ttu-id="f5850-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="f5850-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f5850-105">Cette rubrique fournit des informations sur la manière d’approvisionner un nouvel environnement Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.</span><span class="sxs-lookup"><span data-stu-id="f5850-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="f5850-106">Activer la mise en service automatisée de Project Operations dans un projet LCS</span><span class="sxs-lookup"><span data-stu-id="f5850-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="f5850-107">Utilisez les étapes suivantes pour activer le flux de mise en service automatisé de Project Operations pour votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="f5850-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="f5850-108">Accédez à [LCS](https://lcs.dynamics.com/v2) et sélectionnez la vignette **Gestion des fonctionnalités d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="f5850-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="f5850-109">Dans la liste **Fonctionnalité d’évaluation**, sélectionnez **Fonctionnalité Project Operations**, puis sélectionnez **Fonctionnalité d’évaluation activée** pour activer Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f5850-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f5850-110">Cette étape n’est effectuée qu’une seule fois par projet LCS.</span><span class="sxs-lookup"><span data-stu-id="f5850-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="f5850-111">Mettre en service un environnement Project Operations</span><span class="sxs-lookup"><span data-stu-id="f5850-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="f5850-112">Ouvrez un nouveau déploiement [d’environnement de démonstration](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ou [d’environnement bac à sable/de production](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="f5850-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="f5850-113">Parcourez l’Assistant **Mise en service d’environnement**.</span><span class="sxs-lookup"><span data-stu-id="f5850-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f5850-114">Assurez-vous que la version de l’application sélectionnée est 10.0.13 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f5850-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="f5850-115">Pour mettre en service Project Operations, sous **Paramètres avancés**, sélectionnez **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="f5850-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="f5850-116">Activez le **paramètre Common Data Service** en sélectionnant **Oui**, puis entrez les informations dans les champs obligatoires :</span><span class="sxs-lookup"><span data-stu-id="f5850-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="f5850-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f5850-117">Name</span></span>
  - <span data-ttu-id="f5850-118">Région</span><span class="sxs-lookup"><span data-stu-id="f5850-118">Region</span></span>
  - <span data-ttu-id="f5850-119">Langage</span><span class="sxs-lookup"><span data-stu-id="f5850-119">Language</span></span>
  - <span data-ttu-id="f5850-120">Devise</span><span class="sxs-lookup"><span data-stu-id="f5850-120">Currency</span></span>
 
5. <span data-ttu-id="f5850-121">Dans le champ **Modèle Common Data Service**, sélectionnez **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="f5850-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="f5850-122">Sélectionnez le type d’environnement pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="f5850-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="f5850-123">Un essai basé sur un abonnement vous permettra de déployer un environnement CDS pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="f5850-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Paramètres de déploiement](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="f5850-125">Sélectionnez **J’accepte** pour accepter les conditions d’utilisation, puis sélectionnez **Terminé** pour revenir aux paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f5850-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentement au déploiement](./media/2DeploymentConsent.png)

7. <span data-ttu-id="f5850-127">Facultatif – Appliquez les données de démonstration à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="f5850-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="f5850-128">Aller à **Réglages avancés**, sélectionnez **Personnaliser la configuration de SQL Database**, et définissez **Spécifier un jeu de données pour la base de données d’application** sur **Démo**.</span><span class="sxs-lookup"><span data-stu-id="f5850-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="f5850-129">Renseignez les champs obligatoires restants dans l’Assistant et confirmez le déploiement.</span><span class="sxs-lookup"><span data-stu-id="f5850-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="f5850-130">Le délai d’approvisionnement de l’environnement varie en fonction du type d’environnement.</span><span class="sxs-lookup"><span data-stu-id="f5850-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="f5850-131">La mise en service peut prendre jusqu’à six heures.</span><span class="sxs-lookup"><span data-stu-id="f5850-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="f5850-132">Une fois le déploiement terminé, l’environnement apparaîtra comme **Déployé**.</span><span class="sxs-lookup"><span data-stu-id="f5850-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="f5850-133">Pour confirmer que l’environnement s’est déployé avec succès, sélectionnez **Connexion** et connectez-vous à l’environnement pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="f5850-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Détails de l’environnement](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="f5850-135">Appliquer des mises à jour à l’environnement Finance</span><span class="sxs-lookup"><span data-stu-id="f5850-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="f5850-136">Project Operations nécessite un environnement Finance avec la version de l’application **10.0.13 (10.0.569.20009)** ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f5850-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="f5850-137">Vous devrez peut-être appliquer des mises à jour de qualité à votre environnement Finance pour recevoir cette version.</span><span class="sxs-lookup"><span data-stu-id="f5850-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="f5850-138">Dans LCS, sur la page **Détails de l’environnement**, dans la section **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="f5850-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Afficher les mises à jour](./media/5ViewUpdates.png)

2. <span data-ttu-id="f5850-140">Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package.**</span><span class="sxs-lookup"><span data-stu-id="f5850-140">On the **Binary updates** page, select **Save package.**</span></span>

![Enregistrer le package](./media/6SavePackage.png)

3. <span data-ttu-id="f5850-142">Cliquez sur **Sélectionner tout** et **Enregistrer le package**.</span><span class="sxs-lookup"><span data-stu-id="f5850-142">Click **Select all** and then select **Save package**.</span></span>

![Relire et enregistrer les mises à jour](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="f5850-144">Saisissez un nom et une description du package, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f5850-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="f5850-145">Selon la connexion Internet, ce processus peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="f5850-145">Depending on the internet connection, this process might take some time.</span></span>

![Charger le package dans la Bibliothèque d’actifs](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="f5850-147">Une fois le package enregistré, sélectionnez **Terminé** et enregistrez ce package dans la Bibliothèque d’actifs de votre projet LCS.</span><span class="sxs-lookup"><span data-stu-id="f5850-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="f5850-148">L’enregistrement et la validation du package peuvent prendre environ 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="f5850-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="f5850-149">Pour appliquer la mise à jour, accédez à la page **Détails de l’environnement** dans LCS, sélectionnez **Gérer** > **Appliquer les mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="f5850-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Gérer des environnements](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="f5850-151">Dans la liste des mises à jour, sélectionnez le package que vous avez créé et sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="f5850-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Appliquez les mises à jour](./media/10ApplyUpdates.png)

<span data-ttu-id="f5850-153">La maintenance de l’environnement prendra un certain temps.</span><span class="sxs-lookup"><span data-stu-id="f5850-153">Environment servicing will take some time.</span></span> <span data-ttu-id="f5850-154">Une fois terminé, l’environnement retournera à un état déployé.</span><span class="sxs-lookup"><span data-stu-id="f5850-154">After it is complete, the environment will return to a deployed state.</span></span>

![Environnement déployé](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="f5850-156">Établir une connexion en double écriture</span><span class="sxs-lookup"><span data-stu-id="f5850-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="f5850-157">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="f5850-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f5850-158">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="f5850-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="f5850-159">Une fois le lien créé, sélectionnez à nouveau **Lien vers CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="f5850-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="f5850-160">Vous serez redirigé vers Double écriture dans Finance.</span><span class="sxs-lookup"><span data-stu-id="f5850-160">You will be redirected to Dual Write in Finance.</span></span>

![Lien vers CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="f5850-162">Sélectionnez **Appliquer la solution** pour accéder aux entités qui seront mappées dans l’intégration.</span><span class="sxs-lookup"><span data-stu-id="f5850-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Appliquer des solutions](./media/13ApplySolutions.png)

5. <span data-ttu-id="f5850-164">Sélectionnez les deux solutions, **Dynamics 365 Finance and Operations Carte d’entité à double écriture** et **Dynamics 365 Project Operations Cartes d’entités à double écriture**, puis sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="f5850-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmer des solutions](./media/14ConfirmSolutions.png)

<span data-ttu-id="f5850-166">Une fois les solutions appliquées, les entités Double écriture sont appliquées à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="f5850-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Application des solutions](./media/15ApplyingSolutions.png)

<span data-ttu-id="f5850-168">Une fois les entités appliquées, tous les mappages disponibles sont répertoriés dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="f5850-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mappages de double écriture](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="f5850-170">Actualiser les entités de données après la mise à jour</span><span class="sxs-lookup"><span data-stu-id="f5850-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="f5850-171">Dans Finance, accédez à l’espace de travail **Gestion des données**.</span><span class="sxs-lookup"><span data-stu-id="f5850-171">In Finance, go to the **Data management** workspace.</span></span>

![Espace de travail de la gestion de données](./media/16DataManagement.png)

2. <span data-ttu-id="f5850-173">Sélectionnez la vignette **Paramètres du cadre**.</span><span class="sxs-lookup"><span data-stu-id="f5850-173">Select the **Framework parameters** tile.</span></span>

![Paramètres du cadre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="f5850-175">Sur la page **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.</span><span class="sxs-lookup"><span data-stu-id="f5850-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualiser la liste des entités](./media/18RefreshEntityList.png)

<span data-ttu-id="f5850-177">L’actualisation prendra environ 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="f5850-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="f5850-178">Vous recevrez une alerte lorsqu’elle sera terminée.</span><span class="sxs-lookup"><span data-stu-id="f5850-178">You will receive an alert when it is complete.</span></span>

![Confirmer l’actualisation](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="f5850-180">Mettre à jour les paramètres de sécurité sur Project Operations sur Dataverse</span><span class="sxs-lookup"><span data-stu-id="f5850-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="f5850-181">Accédez à Project Operations sur votre environnement Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f5850-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="f5850-182">Accédez à **Paramètres** > **Sécurité** > **Rôles de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="f5850-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="f5850-183">Sur la page **Rôles de sécurité**, dans la liste des rôles, sélectionnez **Utilisateur d’application à double écriture** et sélectionnez l’onglet **Entités personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="f5850-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="f5850-184">Vérifiez que le rôle a les autorisations en **Lecture** et **Ajouter à** pour :</span><span class="sxs-lookup"><span data-stu-id="f5850-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="f5850-185">**Type de taux de change devise**</span><span class="sxs-lookup"><span data-stu-id="f5850-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="f5850-186">**Plan comptable**</span><span class="sxs-lookup"><span data-stu-id="f5850-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="f5850-187">**Calendrier fiscal**</span><span class="sxs-lookup"><span data-stu-id="f5850-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="f5850-188">**Registre**</span><span class="sxs-lookup"><span data-stu-id="f5850-188">**Ledger**</span></span>

5. <span data-ttu-id="f5850-189">Une fois le rôle de sécurité mis à jour, accédez à **Paramètres** > **Sécurité** > **Équipes** et sélectionnez l’équipe par défaut dans la vue d’équipe **Propriétaire d’entreprise locale**.</span><span class="sxs-lookup"><span data-stu-id="f5850-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="f5850-190">Sélectionnez **Gérer les rôles** et vérifiez que le privilège de sécurité **Utilisateur d’application à double écriture** est appliqué à cette équipe.</span><span class="sxs-lookup"><span data-stu-id="f5850-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="f5850-191">Exécuter les mappages d’écriture double Project Operations</span><span class="sxs-lookup"><span data-stu-id="f5850-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="f5850-192">Dans votre projet LCS, accédez à la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="f5850-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f5850-193">Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="f5850-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="f5850-194">Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.</span><span class="sxs-lookup"><span data-stu-id="f5850-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="f5850-195">Démarrez les mappages comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5850-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="f5850-196">Assurez-vous de suivre la séquence indiquée.</span><span class="sxs-lookup"><span data-stu-id="f5850-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="f5850-197">**Mappage d’entité**</span><span class="sxs-lookup"><span data-stu-id="f5850-197">**Entity Map**</span></span> | <span data-ttu-id="f5850-198">**Actualiser l’entité**</span><span class="sxs-lookup"><span data-stu-id="f5850-198">**Refresh entity**</span></span> | <span data-ttu-id="f5850-199">**Synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="f5850-199">**Initial sync**</span></span> | <span data-ttu-id="f5850-200">**Sélection principale pour la synchronisation initiale**</span><span class="sxs-lookup"><span data-stu-id="f5850-200">**Master for initial sync**</span></span> | <span data-ttu-id="f5850-201">**Exécuter la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="f5850-201">**Run prerequisites**</span></span> | <span data-ttu-id="f5850-202">**Synchronisation initiale de la configuration requise**</span><span class="sxs-lookup"><span data-stu-id="f5850-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f5850-203">**Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="f5850-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="f5850-204">No</span><span class="sxs-lookup"><span data-stu-id="f5850-204">No</span></span> | <span data-ttu-id="f5850-205">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-205">Yes</span></span> | <span data-ttu-id="f5850-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f5850-206">Common Data Service</span></span> | <span data-ttu-id="f5850-207">No</span><span class="sxs-lookup"><span data-stu-id="f5850-207">No</span></span> | <span data-ttu-id="f5850-208">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-208">N\A</span></span> |
| <span data-ttu-id="f5850-209">**Entités juridiques (cdm\_entreprises)**</span><span class="sxs-lookup"><span data-stu-id="f5850-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="f5850-210">No</span><span class="sxs-lookup"><span data-stu-id="f5850-210">No</span></span> | <span data-ttu-id="f5850-211">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-211">Yes</span></span> | <span data-ttu-id="f5850-212">Applications Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f5850-212">Finance and Operations apps</span></span> | <span data-ttu-id="f5850-213">No</span><span class="sxs-lookup"><span data-stu-id="f5850-213">No</span></span> | <span data-ttu-id="f5850-214">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-214">N\A</span></span> |
| <span data-ttu-id="f5850-215">**Registre (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="f5850-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="f5850-216">No</span><span class="sxs-lookup"><span data-stu-id="f5850-216">No</span></span> | <span data-ttu-id="f5850-217">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-217">Yes</span></span> | <span data-ttu-id="f5850-218">Applications Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f5850-218">Finance and Operations apps</span></span> | <span data-ttu-id="f5850-219">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-219">Yes</span></span> | <span data-ttu-id="f5850-220">Oui, applications Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f5850-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="f5850-221">**Intégration des chiffres réels Project Operations (msdyn\_chiffres réels)**</span><span class="sxs-lookup"><span data-stu-id="f5850-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="f5850-222">No</span><span class="sxs-lookup"><span data-stu-id="f5850-222">No</span></span> | <span data-ttu-id="f5850-223">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-223">No</span></span> | <span data-ttu-id="f5850-224">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-224">N\A</span></span> | <span data-ttu-id="f5850-225">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-225">Yes</span></span> | <span data-ttu-id="f5850-226">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-226">No</span></span> |
| <span data-ttu-id="f5850-227">**Lignes du contrat de projet (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="f5850-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="f5850-228">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-228">No</span></span> | <span data-ttu-id="f5850-229">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-229">No</span></span> | <span data-ttu-id="f5850-230">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-230">N\A</span></span> | <span data-ttu-id="f5850-231">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-231">No</span></span> | <span data-ttu-id="f5850-232">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-232">No</span></span> |
| <span data-ttu-id="f5850-233">**Entité d’intégration pour les relations de transaction du projet (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="f5850-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="f5850-234">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-234">No</span></span> | <span data-ttu-id="f5850-235">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-235">No</span></span> | <span data-ttu-id="f5850-236">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-236">N\A</span></span> | <span data-ttu-id="f5850-237">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-237">No</span></span> | <span data-ttu-id="f5850-238">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-238">N\A</span></span> |
| <span data-ttu-id="f5850-239">**Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="f5850-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="f5850-240">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-240">No</span></span> | <span data-ttu-id="f5850-241">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-241">No</span></span> | <span data-ttu-id="f5850-242">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-242">N\A</span></span> | <span data-ttu-id="f5850-243">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-243">No</span></span> | <span data-ttu-id="f5850-244">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-244">N\A</span></span> |
| <span data-ttu-id="f5850-245">**Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="f5850-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="f5850-246">No</span><span class="sxs-lookup"><span data-stu-id="f5850-246">No</span></span> | <span data-ttu-id="f5850-247">No</span><span class="sxs-lookup"><span data-stu-id="f5850-247">No</span></span> | <span data-ttu-id="f5850-248">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-248">N\A</span></span> | <span data-ttu-id="f5850-249">No</span><span class="sxs-lookup"><span data-stu-id="f5850-249">No</span></span> | <span data-ttu-id="f5850-250">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-250">N\A</span></span> |
| <span data-ttu-id="f5850-251">**Entité d’exportation des catégories de dépenses de projet d’intégration de Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="f5850-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="f5850-252">No</span><span class="sxs-lookup"><span data-stu-id="f5850-252">No</span></span> | <span data-ttu-id="f5850-253">No</span><span class="sxs-lookup"><span data-stu-id="f5850-253">No</span></span> | <span data-ttu-id="f5850-254">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-254">N\A</span></span> | <span data-ttu-id="f5850-255">No</span><span class="sxs-lookup"><span data-stu-id="f5850-255">No</span></span> | <span data-ttu-id="f5850-256">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-256">N\A</span></span> |
| <span data-ttu-id="f5850-257">**Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="f5850-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="f5850-258">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-258">Yes</span></span> | <span data-ttu-id="f5850-259">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-259">No</span></span> | <span data-ttu-id="f5850-260">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-260">N\A</span></span> | <span data-ttu-id="f5850-261">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-261">No</span></span> | <span data-ttu-id="f5850-262">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-262">N\A</span></span> |
| <span data-ttu-id="f5850-263">**Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="f5850-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="f5850-264">Oui</span><span class="sxs-lookup"><span data-stu-id="f5850-264">Yes</span></span> | <span data-ttu-id="f5850-265">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-265">No</span></span> | <span data-ttu-id="f5850-266">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-266">N\A</span></span> | <span data-ttu-id="f5850-267">Non</span><span class="sxs-lookup"><span data-stu-id="f5850-267">No</span></span> | <span data-ttu-id="f5850-268">S. O.</span><span class="sxs-lookup"><span data-stu-id="f5850-268">N\A</span></span> |


4. <span data-ttu-id="f5850-269">Pour actualiser l’entité, sélectionnez le nom du mappage, puis sélectionnez **Actualiser les entités**.</span><span class="sxs-lookup"><span data-stu-id="f5850-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualiser le mappage](./media/20RefreshMapping.png)

5. <span data-ttu-id="f5850-271">Une fois l’actualisation terminée, exécutez le mappage.</span><span class="sxs-lookup"><span data-stu-id="f5850-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="f5850-272">Avant d’activer le mappage suivant, vérifiez que le mappage du tableau est dans un état de **En cours d’exécution**.</span><span class="sxs-lookup"><span data-stu-id="f5850-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="f5850-273">L’exécution des mappages avec un plus grand nombre de prérequis peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="f5850-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="f5850-274">Pour exécuter un mappage avec des prérequis, activez le bouton de basculement **Afficher les mappages d’entités associés**.</span><span class="sxs-lookup"><span data-stu-id="f5850-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="f5850-275">Si le tableau indique que **Synchronisation initiale préalable** est **Non**, vérifiez que l’indicateur **Synchronisation initiale** est **Désactivé** dans tous les mappages de prérequises avant de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="f5850-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Exécuter le mappage](./media/21RunMap.png)

6. <span data-ttu-id="f5850-277">Validez que tous les mappages liés au projet sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f5850-277">Validate all project related maps are in the running state.</span></span>

![Tous les mappages en cours d’exécution](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="f5850-279">Appliquer les données de configuration dans CDS pour Project Operations (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f5850-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="f5850-280">Si vous avez appliqué des données de démonstration à l’environnement Finance, consultez [Configurer et appliquer les données de configuration dans Common Data Service pour Project Operations](resource-apply-pro-setup-config-data.md) pour appliquer les données de démonstration à l’environnement CDS.</span><span class="sxs-lookup"><span data-stu-id="f5850-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="f5850-281">Votre environnement Project Operations est désormais mis en service et configuré.</span><span class="sxs-lookup"><span data-stu-id="f5850-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]