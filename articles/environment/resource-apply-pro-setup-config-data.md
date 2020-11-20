---
title: Configurer et appliquer les données de configuration dans Common Data Service
description: Cette rubrique fournit des informations sur la configuration et l’application des données de configuration dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401125"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="0446d-103">Configurer et appliquer les données de configuration dans Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0446d-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="0446d-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="0446d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0446d-105">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="0446d-105">Prerequisites</span></span>

<span data-ttu-id="0446d-106">Avant de commencer à configurer les données dans Common Data Service (CDS), les conditions préalables suivantes doivent être respectées :</span><span class="sxs-lookup"><span data-stu-id="0446d-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="0446d-107">Configurer un environnement CDS et un environnement Dynamics 365 Finance pour Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0446d-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="0446d-108">Les informations sur l’entité juridique de Dynamics 365 Finance sont partagées avec l’environnement CDS.</span><span class="sxs-lookup"><span data-stu-id="0446d-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="0446d-109">Cela signifie que l’entité **Société** dans CDS possède les enregistrement de société suivants :</span><span class="sxs-lookup"><span data-stu-id="0446d-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="0446d-110">THPM</span><span class="sxs-lookup"><span data-stu-id="0446d-110">THPM</span></span>
  - <span data-ttu-id="0446d-111">USPM</span><span class="sxs-lookup"><span data-stu-id="0446d-111">USPM</span></span>
  - <span data-ttu-id="0446d-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="0446d-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="0446d-113">Installer la configuration de la démonstration et les données de configuration</span><span class="sxs-lookup"><span data-stu-id="0446d-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="0446d-114">Téléchargez, débloquez et décompressez le [Package de données d’installation et de configuration](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="0446d-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="0446d-115">Accédez au dossier décompressé et exécutez le fichier exécutable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="0446d-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="0446d-116">Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="0446d-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migration de la configuration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="0446d-118">Sur la page 2 de l’Assistant CMT, sélectionnez **Microsoft 365** comme **Type de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="0446d-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="0446d-119">Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.</span><span class="sxs-lookup"><span data-stu-id="0446d-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="0446d-120">Sélectionnez la région de votre client, entrez vos informations d’identification et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="0446d-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Connexion de configuration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="0446d-122">Sur la page 3, dans la liste des organisations sur le client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="0446d-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="0446d-123">Sur la page 4, sélectionnez le fichier zip, *SampleSetupAndConfigData* à partir du dossier décompressé.</span><span class="sxs-lookup"><span data-stu-id="0446d-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Sélection de fichier zip](./media/3ZipFile.png)

![Sélectionnez un fichier](./media/4SelectAFile.png)

9. <span data-ttu-id="0446d-126">Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.</span><span class="sxs-lookup"><span data-stu-id="0446d-126">After the zip file is selected, select **Import Data**.</span></span>

![Importer des données](./media/5ImportData.png)

10. <span data-ttu-id="0446d-128">L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="0446d-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="0446d-129">Une fois l’importation terminée, quittez l’Assistant CMT.</span><span class="sxs-lookup"><span data-stu-id="0446d-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="0446d-130">Vérifiez votre organisation pour les données dans les 19 entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="0446d-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="0446d-131">Devise</span><span class="sxs-lookup"><span data-stu-id="0446d-131">Currency</span></span>
  - <span data-ttu-id="0446d-132">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="0446d-132">Organizational Unit</span></span>
  - <span data-ttu-id="0446d-133">Contact</span><span class="sxs-lookup"><span data-stu-id="0446d-133">Contact</span></span>
  - <span data-ttu-id="0446d-134">Groupe fiscal</span><span class="sxs-lookup"><span data-stu-id="0446d-134">Tax Group</span></span>
  - <span data-ttu-id="0446d-135">Groupe de clients</span><span class="sxs-lookup"><span data-stu-id="0446d-135">Customer Group</span></span>
  - <span data-ttu-id="0446d-136">Unité</span><span class="sxs-lookup"><span data-stu-id="0446d-136">Unit</span></span>
  - <span data-ttu-id="0446d-137">Groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="0446d-137">Unit Group</span></span>
  - <span data-ttu-id="0446d-138">Tarifs</span><span class="sxs-lookup"><span data-stu-id="0446d-138">Price List</span></span>
  - <span data-ttu-id="0446d-139">Tarifs du paramètre du projet</span><span class="sxs-lookup"><span data-stu-id="0446d-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="0446d-140">Fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="0446d-140">Invoice Frequency</span></span>
  - <span data-ttu-id="0446d-141">Catégorie de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="0446d-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="0446d-142">Catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="0446d-142">Transaction Category</span></span>
  - <span data-ttu-id="0446d-143">Catégorie de dépense</span><span class="sxs-lookup"><span data-stu-id="0446d-143">Expense Category</span></span>
  - <span data-ttu-id="0446d-144">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="0446d-144">Role Price</span></span>
  - <span data-ttu-id="0446d-145">Prix de la catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="0446d-145">Transaction Category Price</span></span>
  - <span data-ttu-id="0446d-146">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="0446d-146">Characteristic</span></span>
  - <span data-ttu-id="0446d-147">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="0446d-147">Bookable Resource</span></span>
  - <span data-ttu-id="0446d-148">Association de catégories de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="0446d-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="0446d-149">Caractéristique des ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="0446d-149">Bookable Resource Characteristic</span></span>

![Importation terminée](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="0446d-151">Mettre à jour les configurations Project Operations</span><span class="sxs-lookup"><span data-stu-id="0446d-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="0446d-152">Accéder à l’environnement CE.</span><span class="sxs-lookup"><span data-stu-id="0446d-152">Navigate to the CE environment.</span></span> <span data-ttu-id="0446d-153">Vous pouvez le trouver en ouvrant le [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/environments), en sélectionnant l’environnement, puis en sélectionnant **Ouvrir l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="0446d-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Ouvrir l’environnement](./media/7OpenEnvironment.png)

2. <span data-ttu-id="0446d-155">Accédez à **Projets** > **Ressources**, puis sélectionnez **Nouveau** pour créer une ressource réservable pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0446d-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ressources pouvant être réservées](./media/8BookableResources.png)

3. <span data-ttu-id="0446d-157">Sur l’onglet **Général**, sélectionnez votre utilisateur administrateur.</span><span class="sxs-lookup"><span data-stu-id="0446d-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="0446d-158">Vérifiez que le fuseau horaire correspond à celui dans lequel vous vous trouvez.</span><span class="sxs-lookup"><span data-stu-id="0446d-158">Verify that the time zone matches the one you are in.</span></span> 

![Nouvelle ressource pouvant être réservée](./media/9NewBookableResource.png)

4. <span data-ttu-id="0446d-160">Sur l’onglet **Planification**, dans le champ **Société**, choisissez la société **USPM**, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0446d-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Onglet Planification](./media/10SchedulingTab.png)

5. <span data-ttu-id="0446d-162">Cliquez sur l’onglet **Heures de travail**.</span><span class="sxs-lookup"><span data-stu-id="0446d-162">Select the **Work hours** tab.</span></span>  

![Heures de travail](./media/11WorkHours.png)

6. <span data-ttu-id="0446d-164">Double-cliquez sur n’importe quelle valeur du calendrier et sélectionnez **Modifier** > **Tous les événements de la série**.</span><span class="sxs-lookup"><span data-stu-id="0446d-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendrier de travail](./media/12WorkCalendar.png)

7. <span data-ttu-id="0446d-166">Remplacez les heures de travail par une journée de travail de huit (8) heures, marquez les week-ends comme jours non travaillés et assurez-vous que le fuseau horaire correspond au vôtre.</span><span class="sxs-lookup"><span data-stu-id="0446d-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="0446d-167">Sélectionnez **Enregistrer et fermer**.</span><span class="sxs-lookup"><span data-stu-id="0446d-167">Select **Save and close**.</span></span>

![Mettre à jour un calendrier](./media/13UpdateCalendar.png)

9. <span data-ttu-id="0446d-169">Accédez à **Paramètres** > **Modèles de calendrier** et sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="0446d-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modèles de calendrier](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="0446d-171">Entrez un nom, sélectionnez la ressource de modèle que vous avez créée, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0446d-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Enregistrer un modèle de calendrier](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="0446d-173">Accédez à **Paramètres** et double-cliquez sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="0446d-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Paramètres du projet](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="0446d-175">Mettez à jour les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="0446d-175">Update the following fields:</span></span>

 - <span data-ttu-id="0446d-176">**Société par défaut** : USPM</span><span class="sxs-lookup"><span data-stu-id="0446d-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="0446d-177">**Unité d’organisation par défaut** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="0446d-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="0446d-178">**Fréquence de facturation** : Septième et dernier jour</span><span class="sxs-lookup"><span data-stu-id="0446d-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="0446d-179">**Modèle d’heure de travail** : Passez au modèle que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="0446d-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="0446d-180">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0446d-180">Select **Save**.</span></span> 

![Paramètres du projet mis à jour](./media/17UpdatedProjectParameters.png)
