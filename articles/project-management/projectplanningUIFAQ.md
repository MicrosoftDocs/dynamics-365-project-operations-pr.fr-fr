---
title: Résolution des problèmes lors de l’utilisation de la grille des tâches
description: Cette rubrique fournit les informations de dépannage nécessaires lorsque vous travaillez dans la grille des tâches.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031534"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="dced6-103">Résolution des problèmes lors de l’utilisation de la grille des tâches</span><span class="sxs-lookup"><span data-stu-id="dced6-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="dced6-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="dced6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dced6-105">Ce sujet décrit comment résoudre les problèmes que vous pourriez rencontrer en travaillant avec la gestion des coûts.</span><span class="sxs-lookup"><span data-stu-id="dced6-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="dced6-106">Activer les cookies</span><span class="sxs-lookup"><span data-stu-id="dced6-106">Enable cookies</span></span>

<span data-ttu-id="dced6-107">Project Operations nécessite que les cookies tiers soient activés afin de rendre la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="dced6-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="dced6-108">Lorsque les cookies tiers ne sont pas activés, au lieu de voir les tâches, vous verrez une page vierge lorsque vous sélectionnez l'onglet **Tâches** sur la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="dced6-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Onglet vide lorsque les cookies tiers ne sont pas activés](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="dced6-110">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="dced6-110">Workaround</span></span>
<span data-ttu-id="dced6-111">Pour Microsoft Edge ou les navigateurs Google Chrome, les procédures suivantes décrivent comment mettre à jour les paramètres de votre navigateur pour activer les cookies tiers.</span><span class="sxs-lookup"><span data-stu-id="dced6-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="dced6-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dced6-112">Microsoft Edge</span></span>

1. <span data-ttu-id="dced6-113">Ouvrez votre navigateur Edge.</span><span class="sxs-lookup"><span data-stu-id="dced6-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="dced6-114">Dans l’angle supérieur droit, sélectionnez les **points de suspension** (...), puis **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="dced6-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="dced6-115">En dessous de **Cookies et autorisations du site**, sélectionnez **Cookies et données de site**.</span><span class="sxs-lookup"><span data-stu-id="dced6-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="dced6-116">Désactivez **Bloquer les cookies tiers**.</span><span class="sxs-lookup"><span data-stu-id="dced6-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="dced6-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="dced6-117">Google Chrome</span></span>

1. <span data-ttu-id="dced6-118">Ouvrez votre navigateur Chrome.</span><span class="sxs-lookup"><span data-stu-id="dced6-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="dced6-119">Dans l'angle supérieur droit, sélectionnez les trois points verticaux, puis sélectionnez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="dced6-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="dced6-120">En dessous de **Confidentialité et sécurité**, sélectionnez **Cookies et autres données de site**.</span><span class="sxs-lookup"><span data-stu-id="dced6-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="dced6-121">Sélectionnez **Autoriser tous les cookies**.</span><span class="sxs-lookup"><span data-stu-id="dced6-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dced6-122">Si vous bloquez les cookies tiers, tous les cookies et données de site d'autres sites seront bloqués, même si le site est autorisé sur votre liste d'exceptions.</span><span class="sxs-lookup"><span data-stu-id="dced6-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="dced6-123">Point de terminaison PEX</span><span class="sxs-lookup"><span data-stu-id="dced6-123">PEX Endpoint</span></span>

<span data-ttu-id="dced6-124">Project Operations requiert qu'un paramètre de projet fasse référence au point de terminaison PEX.</span><span class="sxs-lookup"><span data-stu-id="dced6-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="dced6-125">Ce point de terminaison est nécessaire pour communiquer avec le service utilisé pour rendre la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="dced6-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="dced6-126">Si le paramètre n'est pas activé, vous recevrez l'erreur "Le paramètre de projet n'est pas valide".</span><span class="sxs-lookup"><span data-stu-id="dced6-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="dced6-127">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="dced6-127">Workaround</span></span>
 ![Champ Point de terminaison PEX sur le paramètre de projet](media/projectparameter.png)

1. <span data-ttu-id="dced6-129">Ajoutez le champ **Point de terminaison PEX** à la page **Paramètres du projet**.</span><span class="sxs-lookup"><span data-stu-id="dced6-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="dced6-130">Mettez à jour le champ avec la valeur suivante : `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="dced6-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="dced6-131">Supprimez le champ de la page **Paramètres du projet**.</span><span class="sxs-lookup"><span data-stu-id="dced6-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="dced6-132">Privilèges pour Projet pour le web</span><span class="sxs-lookup"><span data-stu-id="dced6-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="dced6-133">Project Operations s'appuie sur un service de planification externe.</span><span class="sxs-lookup"><span data-stu-id="dced6-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="dced6-134">Le service exige qu'un utilisateur dispose de plusieurs rôles attribués pour lire et écrire sur des entités liées à la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="dced6-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="dced6-135">Ces entités incluent les tâches de projet, les affectations de ressources et les dépendances de tâches.</span><span class="sxs-lookup"><span data-stu-id="dced6-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="dced6-136">Si un utilisateur ne peut pas rendre la structure de répartition du travail lorsqu'il accède à l'onglet **Tâches**, c'est probablement parce que Projet pour Project Operations n'a pas été activé.</span><span class="sxs-lookup"><span data-stu-id="dced6-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="dced6-137">Un utilisateur peut recevoir soit une erreur rôle de sécurité, soit une erreur liée à un refus d'accès.</span><span class="sxs-lookup"><span data-stu-id="dced6-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="dced6-138">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="dced6-138">Workaround</span></span>

1. <span data-ttu-id="dced6-139">Accédez à **Paramètres > Sécurité > Utilisateurs > Utilisateurs de l'application**.</span><span class="sxs-lookup"><span data-stu-id="dced6-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lecteur d'application](media/applicationuser.jpg)
   
2. <span data-ttu-id="dced6-141">Double-cliquez sur l'enregistrement d'utilisateur de l'application pour vérifier ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="dced6-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="dced6-142">L’utilisateur a accès au projet.</span><span class="sxs-lookup"><span data-stu-id="dced6-142">The user has access to the project.</span></span> <span data-ttu-id="dced6-143">Cette vérification est généralement effectuée en s'assurant que l'utilisateur a un rôle de sécurité de **Chef de projet**.</span><span class="sxs-lookup"><span data-stu-id="dced6-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="dced6-144">L'utilisateur de l'application Microsoft Project existe et est configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="dced6-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="dced6-145">Si cet utilisateur n’existe pas, vous pouvez en un enregistrement d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dced6-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="dced6-146">Sélectionnez **Nouveaux utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="dced6-146">Select **New Users**.</span></span> <span data-ttu-id="dced6-147">Remplacez le formulaire de saisie par **Utilisateur de l'application**, puis ajoutez l'**ID d'application**.</span><span class="sxs-lookup"><span data-stu-id="dced6-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Détails de l'utilisateur de l'application](media/applicationuserdetails.jpg)

4. <span data-ttu-id="dced6-149">Vérifiez que l'utilisateur a reçu la licence correcte et que le service est activé dans les détails des plans de service de la licence.</span><span class="sxs-lookup"><span data-stu-id="dced6-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="dced6-150">Vérifiez que l'utilisateur peut ouvrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="dced6-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="dced6-151">Vérifiez à travers les paramètres du projet que le système pointe vers le bon point de terminaison du projet.</span><span class="sxs-lookup"><span data-stu-id="dced6-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="dced6-152">Vérifier que l'utilisateur de l'application de projet est créée.</span><span class="sxs-lookup"><span data-stu-id="dced6-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="dced6-153">Appliquez les rôles de sécurité suivants à l'utilisateur :</span><span class="sxs-lookup"><span data-stu-id="dced6-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="dced6-154">Utilisateur de Dataverse</span><span class="sxs-lookup"><span data-stu-id="dced6-154">Dataverse User</span></span>
  - <span data-ttu-id="dced6-155">Système de Project Operations</span><span class="sxs-lookup"><span data-stu-id="dced6-155">Project Operations System</span></span>
  - <span data-ttu-id="dced6-156">Système de projet</span><span class="sxs-lookup"><span data-stu-id="dced6-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="dced6-157">Erreur lors de la mise à jour de la structure de répartition du travail</span><span class="sxs-lookup"><span data-stu-id="dced6-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="dced6-158">Lorsqu'une ou plusieurs mises à jour sont apportées à la structure de répartition du travail, les modifications échouent finalement et ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="dced6-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="dced6-159">Une erreur se produit dans la grille de planification indiquant que « La modification récente que vous avez apportée n'a pas pu être enregistrée. »</span><span class="sxs-lookup"><span data-stu-id="dced6-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="dced6-160">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="dced6-160">Workaround</span></span>

1. <span data-ttu-id="dced6-161">Vérifiez que l'utilisateur a reçu la licence correcte et que le service est activé dans les détails des plans de service de la licence.</span><span class="sxs-lookup"><span data-stu-id="dced6-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="dced6-162">Vérifiez que l'utilisateur peut ouvrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="dced6-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="dced6-163">Vérifiez que le système pointe vers le bon point de terminaison du projet.</span><span class="sxs-lookup"><span data-stu-id="dced6-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="dced6-164">Vérifier que l'utilisateur de l'application de projet a été créé.</span><span class="sxs-lookup"><span data-stu-id="dced6-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="dced6-165">Appliquez les rôles de sécurité suivants à l'utilisateur :</span><span class="sxs-lookup"><span data-stu-id="dced6-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="dced6-166">Utilisateur ou utilisateur de base Dataverse</span><span class="sxs-lookup"><span data-stu-id="dced6-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="dced6-167">Système de Project Operations</span><span class="sxs-lookup"><span data-stu-id="dced6-167">Project Operations System</span></span>
  - <span data-ttu-id="dced6-168">Système de projet</span><span class="sxs-lookup"><span data-stu-id="dced6-168">Project System</span></span>
  - <span data-ttu-id="dced6-169">Système de double écriture Project Operations (ce rôle est requis si vous déployez le scénario basé sur les ressources/non stocké de Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="dced6-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
