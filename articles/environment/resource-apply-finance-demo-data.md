---
title: Appliquer les données de démonstration à un environnement hébergé par le cloud Finance
description: Ce sujet explique comment appliquer les données de démonstration entre Project Operations et un environnement hébergé dans le cloud Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000147"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="64cf1-103">Appliquer les données de démonstration à un environnement hébergé par le cloud Finance</span><span class="sxs-lookup"><span data-stu-id="64cf1-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="64cf1-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="64cf1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64cf1-105">Cette rubrique ne s’applique qu’à Microsoft Dynamics 365 Finance version 10.0.13 et ne peut être effectuée que sur un environnement hébergé dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="64cf1-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="64cf1-106">Suivez les étapes de cette rubrique **AVANT** d’appliquer des mises à jour de qualité à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="64cf1-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="64cf1-107">Dans votre projet LCS, ouvrez la page **Détails de l’environnement**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="64cf1-108">Notez qu’elle inclut les détails nécessaires pour se connecter à l’environnement à l’aide du protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="64cf1-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Détails de l’environnement](./media/1EnvironmentDetails.png)

<span data-ttu-id="64cf1-110">Le premier ensemble d’informations d’identification mises en évidence sont les informations d’identification du compte local et contiennent un lien hypertexte vers la connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="64cf1-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="64cf1-111">Les informations d’identification incluent le nom d’utilisateur et le mot de passe de l’administrateur de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="64cf1-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="64cf1-112">Le deuxième ensemble d’informations d’identification est utilisé pour se connecter à SQL Server dans cet environnement.</span><span class="sxs-lookup"><span data-stu-id="64cf1-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="64cf1-113">Connectez-vous à l’environnement à distance par le lien hypertexte dans **Comptes locaux** et utilisez les **Informations d’identification du compte local** pour vous authentifier.</span><span class="sxs-lookup"><span data-stu-id="64cf1-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="64cf1-114">Accédez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et arrêtez le service.</span><span class="sxs-lookup"><span data-stu-id="64cf1-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="64cf1-115">Vous arrêtez le service à ce stade afin de pouvoir continuer à remplacer la base de données SQL.</span><span class="sxs-lookup"><span data-stu-id="64cf1-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Arrêter AOS](./media/2StopAOS.png)

4. <span data-ttu-id="64cf1-117">Accédez à **Services** et arrêtez les deux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="64cf1-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="64cf1-118">Microsoft Dynamics 365 Unified Operations : Service de gestion des lots</span><span class="sxs-lookup"><span data-stu-id="64cf1-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="64cf1-119">Microsoft Dynamics 365 Unified Operations : Cadre d’importation et d’exportation des données</span><span class="sxs-lookup"><span data-stu-id="64cf1-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Arrêter les services](./media/3StopServices.png)

5. <span data-ttu-id="64cf1-121">Ouvrez Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="64cf1-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="64cf1-122">Connectez-vous avec les informations d’identification SQL Server et utilisez l’utilisateur et le mot de passe axdbadmin de la page **Détails des environnements** de LCS.</span><span class="sxs-lookup"><span data-stu-id="64cf1-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="64cf1-124">Dans l’Explorateur d’objets, **Bases de données** et localisez **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="64cf1-125">Vous allez remplacer la base de données par une nouvelle base de données située dans le [centre de téléchargement](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="64cf1-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="64cf1-126">Copiez le fichier zip sur la machine virtuelle dans laquelle vous êtes distant et extrayez le contenu du zip.</span><span class="sxs-lookup"><span data-stu-id="64cf1-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="64cf1-127">Dans SQL Server Management Studio, cliquez avec le bouton droit sur **AxDB**, puis sélectionnez **Tâches** > **Restaurer** > **Base de données**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurer la base de données](./media/5RestoreDatabase.png)

9. <span data-ttu-id="64cf1-129">Sélectionnez **Périphérique source** et accédez au fichier extrait du zip que vous avez copié.</span><span class="sxs-lookup"><span data-stu-id="64cf1-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Périphériques sources](./media/6SourceDevice.png)

10. <span data-ttu-id="64cf1-131">Sélectionnez **Options**, puis **Remplacer la base de données existante** et **Fermer les connexions existantes à la base de données de destination**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="64cf1-132">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-132">Select **OK**.</span></span>

![Restaurer les paramètres](./media/7RestoreSetting.png)

<span data-ttu-id="64cf1-134">Vous recevrez la confirmation que la restauration AXDB a réussi.</span><span class="sxs-lookup"><span data-stu-id="64cf1-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="64cf1-135">Après avoir reçu cette confirmation, vous pouvez fermer SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="64cf1-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="64cf1-136">Revenez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et démarrez AOSService.</span><span class="sxs-lookup"><span data-stu-id="64cf1-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="64cf1-137">Accédez à **Services** et démarrez les deux services que vous avez arrêtés précédemment.</span><span class="sxs-lookup"><span data-stu-id="64cf1-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="64cf1-138">Localisez l’outil AdminUserProvisioning sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="64cf1-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="64cf1-139">Regardez sous K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="64cf1-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="64cf1-140">Exécutez le fichier .ext en utilisant votre adresse utilisateur dans le champ **Adresse électronique**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="64cf1-141">Sélectionnez **Soumettre**.</span><span class="sxs-lookup"><span data-stu-id="64cf1-141">Select **Submit**.</span></span>

![Attribution d’utilisateur administrateur](./media/8AdminUserProvisioning.png)

<span data-ttu-id="64cf1-143">Ce processus peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="64cf1-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="64cf1-144">Vous devriez recevoir un message de confirmation indiquant que l’utilisateur administrateur a été mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="64cf1-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="64cf1-145">Enfin, exécutez l’invite de commande en tant qu’administrateur et exécutez iisreset</span><span class="sxs-lookup"><span data-stu-id="64cf1-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS Reset](./media/9IISReset.png)

18. <span data-ttu-id="64cf1-147">Fermez la session de bureau à distance et utilisez la page **Détails de l’environnement** de LCS pour vous connecter à l’environnement pour confirmer qu’il fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="64cf1-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]