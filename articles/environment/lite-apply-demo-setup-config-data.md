---
title: Appliquer la configuration de la démonstration et les données de configuration
description: Cette rubrique fournit des informations sur l’application de la configuration de démonstration et des données de configuration dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948847"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="802ef-103">Appliquer la configuration de démonstration et les données de configuration pour le déploiement simplifié de Project Operations – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="802ef-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="802ef-104">_\*\*Déploiement simplifié – traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="802ef-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="802ef-105">Téléchargez le [package de données principal](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="802ef-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="802ef-106">Accédez au dossier *ProjOpsDemoDataSetupAndMaster - Integrated CMT* et exécutez le fichier exécutable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="802ef-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="802ef-107">Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="802ef-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migration de la configuration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="802ef-109">Sur la page 2 de l’Assistant CMT, sélectionnez **Office 365** comme le **Type de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="802ef-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="802ef-110">Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.</span><span class="sxs-lookup"><span data-stu-id="802ef-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="802ef-111">Sélectionnez la région de votre client, entrez vos informations d’identification, puis sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="802ef-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Connexion de configuration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="802ef-113">Sur la page 3, dans la liste des Organisations sur le Client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="802ef-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="802ef-114">Sur la page 4, sélectionnez le fichier compressé, *MasterAndSetupData* à partir du dossier décompressé *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="802ef-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fichier compressé](./media/3ZipFile.png)

![Sélectionnez un fichier](./media/4SelectAFile.png)

9. <span data-ttu-id="802ef-117">Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.</span><span class="sxs-lookup"><span data-stu-id="802ef-117">After the zip file is selected, select **Import Data**.</span></span>

![Importer les données](./media/5ImportData.png)

10. <span data-ttu-id="802ef-119">L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="802ef-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="802ef-120">Une fois terminé, quittez l’Assistant CMT.</span><span class="sxs-lookup"><span data-stu-id="802ef-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="802ef-121">Vérifiez votre organisation pour les données dans les 20 entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="802ef-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="802ef-122">Devise</span><span class="sxs-lookup"><span data-stu-id="802ef-122">Currency</span></span>
- <span data-ttu-id="802ef-123">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="802ef-123">Organizational Unit</span></span>
- <span data-ttu-id="802ef-124">Contact</span><span class="sxs-lookup"><span data-stu-id="802ef-124">Contact</span></span>
- <span data-ttu-id="802ef-125">Groupe fiscal</span><span class="sxs-lookup"><span data-stu-id="802ef-125">Tax Group</span></span>
- <span data-ttu-id="802ef-126">Groupe de clients</span><span class="sxs-lookup"><span data-stu-id="802ef-126">Customer Group</span></span>
- <span data-ttu-id="802ef-127">Unité</span><span class="sxs-lookup"><span data-stu-id="802ef-127">Unit</span></span>
- <span data-ttu-id="802ef-128">Groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="802ef-128">Unit Group</span></span>
- <span data-ttu-id="802ef-129">Tarifs</span><span class="sxs-lookup"><span data-stu-id="802ef-129">Price List</span></span>
- <span data-ttu-id="802ef-130">Tarifs du paramètre du projet</span><span class="sxs-lookup"><span data-stu-id="802ef-130">Project Parameter Price List</span></span>
- <span data-ttu-id="802ef-131">Fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="802ef-131">Invoice Frequency</span></span>
- <span data-ttu-id="802ef-132">Détail de la fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="802ef-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="802ef-133">Catégorie de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="802ef-133">Bookable Resource Category</span></span>
- <span data-ttu-id="802ef-134">Catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="802ef-134">Transaction Category</span></span>
- <span data-ttu-id="802ef-135">Catégorie de dépense</span><span class="sxs-lookup"><span data-stu-id="802ef-135">Expense Category</span></span>
- <span data-ttu-id="802ef-136">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="802ef-136">Role Price</span></span>
- <span data-ttu-id="802ef-137">Prix de la catégorie de transaction</span><span class="sxs-lookup"><span data-stu-id="802ef-137">Transaction Category Price</span></span>
- <span data-ttu-id="802ef-138">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="802ef-138">Characteristic</span></span>
- <span data-ttu-id="802ef-139">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="802ef-139">Bookable Resource</span></span>
- <span data-ttu-id="802ef-140">Association de catégories de ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="802ef-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="802ef-141">Caractéristique des ressources pouvant être réservées</span><span class="sxs-lookup"><span data-stu-id="802ef-141">Bookable Resource Characteristic</span></span>

![Importation terminée](./media/6CompleteImport.png)
