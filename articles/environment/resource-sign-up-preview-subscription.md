---
title: Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés
description: Cette rubrique fournit des informations sur la façon de s’abonner et de déployer des scénarios basés sur les ressource/non-stockés Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948852"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="ad3a0-103">Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés</span><span class="sxs-lookup"><span data-stu-id="ad3a0-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="ad3a0-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="ad3a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ad3a0-105">Cette rubrique explique comment souscrire à l’offre de version préliminaire/partenaire et déployer l’environnement Project Operations pour les scénarios basés sur les ressources/non stockés.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ad3a0-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="ad3a0-106">Prerequisites</span></span>

- <span data-ttu-id="ad3a0-107">Vous recevrez un e-mail vous invitant à participer à la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="ad3a0-108">Vous pouvez demander une version préliminaire sur le [site web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="ad3a0-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="ad3a0-109">L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="ad3a0-110">Le déploiement d’un environnement Finance nécessite un abonnement Azure valide qui sera facturé par environnement.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="ad3a0-111">Vous pouvez utiliser l’abonnement existant de votre organisation ou utiliser un [Essai Azure](https://azure.microsoft.com/en-us/free/) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="ad3a0-112">L’environnement CDS sera fourni gratuitement pendant une période limitée de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="ad3a0-113">S’abonner</span><span class="sxs-lookup"><span data-stu-id="ad3a0-113">Subscribe</span></span>

<span data-ttu-id="ad3a0-114">Lorsque vous recevez une approbation à votre [demande de version préliminaire](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), vous recevez deux offres de Microsoft par e-mail.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="ad3a0-115">Ces offres vous permettent de déployer la version préliminaire de Project Operations :</span><span class="sxs-lookup"><span data-stu-id="ad3a0-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="ad3a0-116">Dynamics 365 Project Operations – Version d’essai</span><span class="sxs-lookup"><span data-stu-id="ad3a0-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="ad3a0-117">Version d’essai Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad3a0-118">Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="ad3a0-119">Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="ad3a0-120">Dynamics 365 Project Operations – Version d’essai</span><span class="sxs-lookup"><span data-stu-id="ad3a0-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="ad3a0-121">Utilisez la première offre, **version d’essai Dynamics 365 Project Operations**, avec l’URL fournie dans votre e-mail de bienvenue.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Première offre](./media/1FirstOffer.png)

2. <span data-ttu-id="ad3a0-123">Vérifiez que vous êtes connecté en tant qu’utilisateur appartenant à l’organisation qui s’abonnera au service.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="ad3a0-124">Continuez à utiliser l’offre.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="ad3a0-125">Sélectionnez **Oui, ajoutez-le à mon compte**.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-125">Select **Yes, add it to my account**.</span></span>

![Accepter l’offre](./media/2RedeemFirstOffer.png)

![Confirmer l’offre](./media/3ConfirmFirstOffer.png)

![Offre utilisée](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="ad3a0-129">Version d’essai Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ad3a0-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="ad3a0-130">Répétez les mêmes étapes avec la deuxième offre de l’e-mail de bienvenue.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="ad3a0-131">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="ad3a0-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad3a0-132">Vous aurez besoin d’un accès administratif au portail Office 365 de votre organisation pour terminer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="ad3a0-133">Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Portail d’administration d’Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="ad3a0-135">Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Attribuer des licences](./media/6AssignLicenses.png)

3. <span data-ttu-id="ad3a0-137">Vérifiez que la licence Project Operations a été sélectionnée et sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad3a0-138">L’offre d’essai Finance n’a pas besoin d’être attribuée à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="ad3a0-139">Commencer un nouveau projet dans LCS</span><span class="sxs-lookup"><span data-stu-id="ad3a0-139">Start a new project in LCS</span></span>

<span data-ttu-id="ad3a0-140">Créez un projet LCS comme décrit dans la rubrique, [Démarrer un nouveau projet dans LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="ad3a0-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="ad3a0-141">Ajouter un abonnement Azure à un projet LCS</span><span class="sxs-lookup"><span data-stu-id="ad3a0-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="ad3a0-142">Pour terminer cette tâche, suivez les étapes du sujet, [Ajouter un abonnement Azure au projet LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="ad3a0-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="ad3a0-143">Déployer l’environnement de démonstration Finance avec Project Operations pour les scénarios basés sur des ressources/non stockés</span><span class="sxs-lookup"><span data-stu-id="ad3a0-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="ad3a0-144">Suivez les instructions de la rubrique [Mettre en service un nouvel environnement](resource-provision-new-environment.md) pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="ad3a0-145">Utilisez le type de déploiement [d’environnement de démonstration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pour la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="ad3a0-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="ad3a0-146">Installer la configuration de la démonstration et les données de configuration CDS</span><span class="sxs-lookup"><span data-stu-id="ad3a0-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="ad3a0-147">Installez les données d’installation et de configuration CDS comme décrit dans la rubrique [Configurer et appliquer les données de configuration dans Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="ad3a0-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

