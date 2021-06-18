---
title: Appliquer la configuration de la démonstration et les données de configuration – Simplifié
description: Cette rubrique fournit des informations sur l’application de la configuration de démonstration et des données de configuration dans Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997148"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="99ab3-103">Appliquer la configuration de la démonstration et les données de configuration pour Project Operations – Simplifié</span><span class="sxs-lookup"><span data-stu-id="99ab3-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="99ab3-104">_\*\*Déploiement simplifié – traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="99ab3-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="99ab3-105">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="99ab3-105">Prerequisites</span></span>

<span data-ttu-id="99ab3-106">Avant de commencer la configuration, vous devez disposer d’un environnement Common Data Service (CDS) mis en service pour Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="99ab3-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="99ab3-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="99ab3-107">Instructions</span></span>

1. <span data-ttu-id="99ab3-108">Téléchargez le [package de données principal](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="99ab3-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="99ab3-109">Accédez au dossier *ProjOpsSampleSetupData - CE only CMT* et lancez le fichier exécutable *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="99ab3-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="99ab3-110">Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migration de la configuration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="99ab3-112">Sur la page 2 de l’Assistant CMT, sélectionnez **Microsoft 365** comme **Type de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="99ab3-113">Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="99ab3-114">Sélectionnez la région de votre client, entrez vos informations d’identification, puis sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Connexion de configuration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="99ab3-116">Sur la page 3, dans la liste des Organisations sur le Client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="99ab3-117">À la page 4, sélectionnez le fichier zip *ExempleSetupAndConfigData* dans le dossier décompressé *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="99ab3-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Fichier compressé](./media/3ZipFile.png)

   ![Sélectionner un fichier](./media/4SelectAFile.png)

9. <span data-ttu-id="99ab3-120">Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.</span><span class="sxs-lookup"><span data-stu-id="99ab3-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importer les données](./media/5ImportData.png)

10. <span data-ttu-id="99ab3-122">L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="99ab3-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="99ab3-123">Une fois terminé, quittez l’Assistant CMT.</span><span class="sxs-lookup"><span data-stu-id="99ab3-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="99ab3-124">Vérifiez votre organisation pour les données dans les 18 entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="99ab3-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="99ab3-125">Devise</span><span class="sxs-lookup"><span data-stu-id="99ab3-125">Currency</span></span>
    -   <span data-ttu-id="99ab3-126">Compte</span><span class="sxs-lookup"><span data-stu-id="99ab3-126">Account</span></span>
    -   <span data-ttu-id="99ab3-127">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="99ab3-127">Organizational Unit</span></span>
    -   <span data-ttu-id="99ab3-128">Contact</span><span class="sxs-lookup"><span data-stu-id="99ab3-128">Contact</span></span>
    -   <span data-ttu-id="99ab3-129">Unité</span><span class="sxs-lookup"><span data-stu-id="99ab3-129">Unit</span></span>
    -   <span data-ttu-id="99ab3-130">Groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="99ab3-130">Unit Group</span></span>
    -   <span data-ttu-id="99ab3-131">Tarifs</span><span class="sxs-lookup"><span data-stu-id="99ab3-131">Price List</span></span>
    -   <span data-ttu-id="99ab3-132">Tarifs du paramètre du projet</span><span class="sxs-lookup"><span data-stu-id="99ab3-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="99ab3-133">Fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="99ab3-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="99ab3-134">Catégorie de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="99ab3-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="99ab3-135">Catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="99ab3-135">Transaction Category</span></span>
    -   <span data-ttu-id="99ab3-136">Catégorie de dépense</span><span class="sxs-lookup"><span data-stu-id="99ab3-136">Expense Category</span></span>
    -   <span data-ttu-id="99ab3-137">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="99ab3-137">Role Price</span></span>
    -   <span data-ttu-id="99ab3-138">Prix de la catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="99ab3-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="99ab3-139">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="99ab3-139">Characteristic</span></span>
    -   <span data-ttu-id="99ab3-140">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="99ab3-140">Bookable Resource</span></span>
    -   <span data-ttu-id="99ab3-141">Association de catégories de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="99ab3-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="99ab3-142">Caractéristique des ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="99ab3-142">Bookable Resource Characteristic</span></span>

    ![Importation terminée](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
