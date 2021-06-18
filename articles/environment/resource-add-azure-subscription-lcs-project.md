---
title: Ajouter un abonnement Azure à un projet LCS
description: Cette rubrique fournit des informations sur la connexion de votre abonnement Azure à un projet LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000613"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="00bca-103">Ajouter un abonnement Azure à un projet LCS</span><span class="sxs-lookup"><span data-stu-id="00bca-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="00bca-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="00bca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="00bca-105">Les environnements hébergés dans le cloud doivent être déployés à l’aide d’un abonnement Azure existant.</span><span class="sxs-lookup"><span data-stu-id="00bca-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="00bca-106">Cette rubrique explique comment connecter votre abonnement Azure existant à un projet LCS.</span><span class="sxs-lookup"><span data-stu-id="00bca-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="00bca-107">Accorder un consentement d’administrateur</span><span class="sxs-lookup"><span data-stu-id="00bca-107">Grant admin consent</span></span>

1. <span data-ttu-id="00bca-108">Dans votre projet LCS, dans la section **Environnements**, sélectionnez **Paramètres Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="00bca-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Paramètres de l’application Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="00bca-110">Sur la page **Paramètres du projet**, sur l’onglet **Connecteurs Azure**, sélectionnez **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="00bca-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="00bca-111">Cela permet aux environnements d’être déployés dans ce projet.</span><span class="sxs-lookup"><span data-stu-id="00bca-111">This allows environments to be deployed to this project.</span></span>

![Connecteurs Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="00bca-113">Sélectionnez **Autoriser** à nouveau pour donner le consentement de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="00bca-113">Select **Authorize** again to provide admin consent.</span></span>

![Accorder un consentement d’administrateur](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="00bca-115">Acceptez la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="00bca-115">Accept the permissions request.</span></span>

![Accepter la demande d’autorisation](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="00bca-117">L’autorisation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="00bca-117">The authorization is now complete.</span></span> 

![Autorisation réussie](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="00bca-119">Fournissez l’accès à Dynamics Deployment Services à votre abonnement Azure</span><span class="sxs-lookup"><span data-stu-id="00bca-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="00bca-120">Accédez à [Facturation Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) et sélectionnez votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="00bca-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="00bca-121">Dynamics Deployment Services doit accéder à cet abonnement pour pouvoir déployer des environnements.</span><span class="sxs-lookup"><span data-stu-id="00bca-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Détails de l’abonnement Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="00bca-123">Sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation, puis sélectionnez **Ajouter une attribution de rôle**.</span><span class="sxs-lookup"><span data-stu-id="00bca-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="00bca-124">Dans le curseur sur le côté droit, sélectionnez **Rôle Contributeur**, et dans la liste fournie, recherchez et sélectionnez **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="00bca-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="00bca-125">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="00bca-125">Select **Save**.</span></span>

![Accès à l’abonnement](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="00bca-127">Ajouter un connecteur d’abonnement à un projet LCS</span><span class="sxs-lookup"><span data-stu-id="00bca-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="00bca-128">Dans votre projet LCS, sur la page **Paramètres Microsoft Azure**, sélectionnez **Ajouter** pour ajouter un nouveau connecteur.</span><span class="sxs-lookup"><span data-stu-id="00bca-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="00bca-129">Entrer votre ID d’abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="00bca-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="00bca-130">Vous pouvez trouver votre ID d’abonnement Azure dans le [portail Azure](https://ms.portal.azure.com/), sous **Paramètres** en bas à gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="00bca-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="00bca-131">Dans le champ **Configurer pour utiliser Azure Resource Manager**, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="00bca-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="00bca-132">Assurez-vous que le domaine du client AAD d’abonnement d’Azure correspond à l’abonnement Azure propriétaire du domaine que vous utilisez, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="00bca-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="00bca-133">Sur l’écran **Configuration Microsoft Azure**, sélectionnez **Suivant** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="00bca-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="00bca-134">Si vous recevez une erreur sur cet écran, revenez à la section [Fournir l’accès à Dynamics Deployment Services à l’abonnement Azure](#provide) dans cette rubrique et assurez-vous que vous avez terminé toutes les étapes.</span><span class="sxs-lookup"><span data-stu-id="00bca-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="00bca-135">Téléchargez le certificat de gestion Azure dans un dossier local sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00bca-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="00bca-136">Demandez à votre administrateur d’abonnement Azure de charger le certificat sur le Portail de gestion Azure en sélectionnant l’abonnement et en accédant à **Paramètres** > **Certificats de gestion**.</span><span class="sxs-lookup"><span data-stu-id="00bca-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="00bca-137">Ce certificat permet à LCS de communiquer avec Azure en votre nom.</span><span class="sxs-lookup"><span data-stu-id="00bca-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="00bca-138">Vous pouvez ignorer cette étape si votre utilisateur a accès à l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="00bca-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="00bca-139">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="00bca-139">Select  **Next**.</span></span>
8. <span data-ttu-id="00bca-140">Sélectionnez la région Azure dans laquelle déployer et sélectionnez un centre de données proche de l’endroit où vous prévoyez d’utiliser ce système.</span><span class="sxs-lookup"><span data-stu-id="00bca-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="00bca-141">Cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="00bca-141">Select  **Connect**.</span></span>

<span data-ttu-id="00bca-142">Vous avez connecté avec succès votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="00bca-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="00bca-143">Vous pouvez maintenant déployer environnements hébergés dans le cloud Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="00bca-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
