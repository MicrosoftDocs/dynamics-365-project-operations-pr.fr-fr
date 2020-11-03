---
title: Configurer et appliquer les données de configuration dans le Common Data Service pour Project Operations
description: Cette rubrique fournit des informations sur la configuration et l’application des données de configuration dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075613"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="b20bd-103">Configurer et appliquer les données de configuration dans le Common Data Service pour Project Operations</span><span class="sxs-lookup"><span data-stu-id="b20bd-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="b20bd-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="b20bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="b20bd-105">Installer la configuration de la démonstration et les données de configuration</span><span class="sxs-lookup"><span data-stu-id="b20bd-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="b20bd-106">Téléchargez, débloquez et décompressez le [Package de données d’installation et de configuration](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="b20bd-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="b20bd-107">Accédez au dossier décompressé et exécutez le fichier exécutable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="b20bd-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b20bd-108">Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données** , puis **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migration de la configuration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b20bd-110">Sur la page 2 de l'Assistant CMT, sélectionnez **Microsoft 365** comme **Type de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b20bd-111">Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b20bd-112">Sélectionnez la région de votre client, entrez vos informations d’identification et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Connexion de configuration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b20bd-114">Sur la page 3, dans la liste des organisations sur le client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="b20bd-115">Sur la page 4, sélectionnez le fichier zip, *SampleSetupAndConfigData* à partir du dossier décompressé.</span><span class="sxs-lookup"><span data-stu-id="b20bd-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Sélection de fichier zip](./media/3ZipFile.png)

![Sélectionnez un fichier](./media/4SelectAFile.png)

9. <span data-ttu-id="b20bd-118">Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-118">After the zip file is selected, select **Import Data**.</span></span>

![Importer des données](./media/5ImportData.png)

10. <span data-ttu-id="b20bd-120">L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="b20bd-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b20bd-121">Une fois l’importation terminée, quittez l’Assistant CMT.</span><span class="sxs-lookup"><span data-stu-id="b20bd-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b20bd-122">Vérifiez votre organisation pour les données dans les 19 entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="b20bd-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="b20bd-123">Devise</span><span class="sxs-lookup"><span data-stu-id="b20bd-123">Currency</span></span>
  - <span data-ttu-id="b20bd-124">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="b20bd-124">Organizational Unit</span></span>
  - <span data-ttu-id="b20bd-125">Contact</span><span class="sxs-lookup"><span data-stu-id="b20bd-125">Contact</span></span>
  - <span data-ttu-id="b20bd-126">Groupe fiscal</span><span class="sxs-lookup"><span data-stu-id="b20bd-126">Tax Group</span></span>
  - <span data-ttu-id="b20bd-127">Groupe de clients</span><span class="sxs-lookup"><span data-stu-id="b20bd-127">Customer Group</span></span>
  - <span data-ttu-id="b20bd-128">Unité</span><span class="sxs-lookup"><span data-stu-id="b20bd-128">Unit</span></span>
  - <span data-ttu-id="b20bd-129">Groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="b20bd-129">Unit Group</span></span>
  - <span data-ttu-id="b20bd-130">Tarifs</span><span class="sxs-lookup"><span data-stu-id="b20bd-130">Price List</span></span>
  - <span data-ttu-id="b20bd-131">Tarifs du paramètre du projet</span><span class="sxs-lookup"><span data-stu-id="b20bd-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="b20bd-132">Fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="b20bd-132">Invoice Frequency</span></span>
  - <span data-ttu-id="b20bd-133">Catégorie de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="b20bd-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="b20bd-134">Catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="b20bd-134">Transaction Category</span></span>
  - <span data-ttu-id="b20bd-135">Catégorie de dépense</span><span class="sxs-lookup"><span data-stu-id="b20bd-135">Expense Category</span></span>
  - <span data-ttu-id="b20bd-136">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="b20bd-136">Role Price</span></span>
  - <span data-ttu-id="b20bd-137">Prix de la catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="b20bd-137">Transaction Category Price</span></span>
  - <span data-ttu-id="b20bd-138">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="b20bd-138">Characteristic</span></span>
  - <span data-ttu-id="b20bd-139">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="b20bd-139">Bookable Resource</span></span>
  - <span data-ttu-id="b20bd-140">Association de catégories de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="b20bd-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="b20bd-141">Caractéristique des ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="b20bd-141">Bookable Resource Characteristic</span></span>

![Importation terminée](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="b20bd-143">Mettre à jour les configurations Project Operations</span><span class="sxs-lookup"><span data-stu-id="b20bd-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="b20bd-144">Accéder à l’environnement CE.</span><span class="sxs-lookup"><span data-stu-id="b20bd-144">Navigate to the CE environment.</span></span> <span data-ttu-id="b20bd-145">Vous pouvez le trouver en ouvrant le [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/environments), en sélectionnant l’environnement, puis en sélectionnant **Ouvrir l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Ouvrir l’environnement](./media/7OpenEnvironment.png)

2. <span data-ttu-id="b20bd-147">Accédez à **Projets** > **Ressources** , puis sélectionnez **Nouveau** pour créer une ressource réservable pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b20bd-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ressources pouvant être réservées](./media/8BookableResources.png)

3. <span data-ttu-id="b20bd-149">Sur l’onglet **Général** , sélectionnez votre utilisateur administrateur.</span><span class="sxs-lookup"><span data-stu-id="b20bd-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="b20bd-150">Vérifiez que le fuseau horaire correspond à celui dans lequel vous vous trouvez.</span><span class="sxs-lookup"><span data-stu-id="b20bd-150">Verify that the time zone matches the one you are in.</span></span> 

![Nouvelle ressource pouvant être réservée](./media/9NewBookableResource.png)

4. <span data-ttu-id="b20bd-152">Sur l’onglet **Planification** , dans le champ **Société** , choisissez la société **USPM** , puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Onglet Planification](./media/10SchedulingTab.png)

5. <span data-ttu-id="b20bd-154">Cliquez sur l’onglet **Heures de travail**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-154">Select the **Work hours** tab.</span></span>  

![Heures de travail](./media/11WorkHours.png)

6. <span data-ttu-id="b20bd-156">Double-cliquez sur n’importe quelle valeur du calendrier et sélectionnez **Modifier** > **Tous les événements de la série**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendrier de travail](./media/12WorkCalendar.png)

7. <span data-ttu-id="b20bd-158">Remplacez les heures de travail par une journée de travail de huit (8) heures, marquez les week-ends comme jours non travaillés et assurez-vous que le fuseau horaire correspond au vôtre.</span><span class="sxs-lookup"><span data-stu-id="b20bd-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="b20bd-159">Sélectionnez **Enregistrer et fermer**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-159">Select **Save and close**.</span></span>

![Mettre à jour un calendrier](./media/13UpdateCalendar.png)

9. <span data-ttu-id="b20bd-161">Accédez à **Paramètres** > **Modèles de calendrier** et sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modèles de calendrier](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="b20bd-163">Entrez un nom, sélectionnez la ressource de modèle que vous avez créée, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Enregistrer un modèle de calendrier](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="b20bd-165">Accédez à **Paramètres** et double-cliquez sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b20bd-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Paramètres du projet](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="b20bd-167">Mettez à jour les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="b20bd-167">Update the following fields:</span></span>

 - <span data-ttu-id="b20bd-168">**Société par défaut**  : USPM</span><span class="sxs-lookup"><span data-stu-id="b20bd-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="b20bd-169">**Unité d’organisation par défaut**  : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="b20bd-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="b20bd-170">**Fréquence de facturation**  : Septième et dernier jour</span><span class="sxs-lookup"><span data-stu-id="b20bd-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="b20bd-171">**Modèle d’heure de travail**  : Passez au modèle que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="b20bd-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="b20bd-172">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b20bd-172">Select **Save**.</span></span> 

![Paramètres du projet mis à jour](./media/17UpdatedProjectParameters.png)
