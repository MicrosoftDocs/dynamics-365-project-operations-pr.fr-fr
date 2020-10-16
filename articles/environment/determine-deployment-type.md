---
title: Types de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948848"
---
# <a name="deployment-types"></a><span data-ttu-id="23cda-103">Types de déploiement</span><span class="sxs-lookup"><span data-stu-id="23cda-103">Deployment types</span></span>

<span data-ttu-id="23cda-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="23cda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23cda-105">Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations à l’aide du [Flux d’installation guidé](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="23cda-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="23cda-106">Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation.</span><span class="sxs-lookup"><span data-stu-id="23cda-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="23cda-107">Consultez les détails de déploiement ci-dessous pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="23cda-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="23cda-108">Clients Dynamics existants utilisant Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="23cda-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="23cda-109">Project Operations inclut les fonctionnalités fournies avec Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="23cda-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="23cda-110">Un chemin d’accès à la mise à niveau sera publié pour ces clients à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="23cda-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="23cda-111">Clients Dynamics 365 Finance existants utilisant Gestion de projet et comptabilité</span><span class="sxs-lookup"><span data-stu-id="23cda-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="23cda-112">Les clients Finance existants qui utilisent la fonctionnalité Gestion de projet et comptabilité peuvent continuer à l’utiliser tel quel.</span><span class="sxs-lookup"><span data-stu-id="23cda-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="23cda-113">Voir [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma).</span><span class="sxs-lookup"><span data-stu-id="23cda-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="23cda-114">Project Operations prend en charge plusieurs options de déploiement pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="23cda-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="23cda-115">Que vous soyez un client Dynamics 365 nouveau ou existant, Project Operations peut répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="23cda-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="23cda-116">Notre [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations) vous aidera à déterminer le bon déploiement.</span><span class="sxs-lookup"><span data-stu-id="23cda-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="23cda-117">Les résultats vous guideront vers l’un des types de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="23cda-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="23cda-118">Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="23cda-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="23cda-119">Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="23cda-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="23cda-120">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="23cda-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="23cda-121">Project Operations prend en charge les scénarios stockés/d’ordre de fabrication et les scénarios non stockés/basés sur les ressources dans le même environnement par le biais des configurations au niveau de l’entité juridique.</span><span class="sxs-lookup"><span data-stu-id="23cda-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="23cda-122">Par exemple, Contoso peut tirer parti des capacités stockées/d’ordre de production dans son usine de fabrication aux États-Unis (entité juridique = Contoso Manufacturing United States) et des capacités non stockées/basées sur les ressources dans son installation de maintenance Contoso Robotics Arms au Royaume-Uni (entité juridique = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="23cda-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="23cda-123"><a name="lite"><a/>Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="23cda-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="23cda-124">Le déploiement simplifié comprend les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="23cda-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="23cda-125">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="23cda-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="23cda-126">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="23cda-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="23cda-127">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="23cda-127">Unified Resource Management</span></span>
- <span data-ttu-id="23cda-128">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="23cda-128">Time Tracking</span></span>
- <span data-ttu-id="23cda-129">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="23cda-129">Basic Expense</span></span>
- <span data-ttu-id="23cda-130">Proposition de facture</span><span class="sxs-lookup"><span data-stu-id="23cda-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="23cda-131">Étapes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="23cda-131">Deployment steps:</span></span>
<span data-ttu-id="23cda-132">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="23cda-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="23cda-133">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](lite-preview-subscription-sign-up.md) et [Mettre en service un nouvel environnement](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="23cda-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="23cda-134"><a name="integrated"><a/>Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="23cda-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="23cda-135">Project Operations pour les scénarios de ressources/non stockés incluent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="23cda-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="23cda-136">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="23cda-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="23cda-137">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="23cda-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="23cda-138">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="23cda-138">Unified Resource Management</span></span>
- <span data-ttu-id="23cda-139">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="23cda-139">Time Tracking</span></span>
- <span data-ttu-id="23cda-140">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="23cda-140">Basic Expense</span></span>
- <span data-ttu-id="23cda-141">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="23cda-141">Full Expense</span></span>
- <span data-ttu-id="23cda-142">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="23cda-142">Receipt OCR</span></span>
- <span data-ttu-id="23cda-143">Facturation complète</span><span class="sxs-lookup"><span data-stu-id="23cda-143">Full Invoicing</span></span>
- <span data-ttu-id="23cda-144">Comptabilisation de clôture</span><span class="sxs-lookup"><span data-stu-id="23cda-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="23cda-145">Étapes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="23cda-145">Deployment steps:</span></span>
<span data-ttu-id="23cda-146">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="23cda-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="23cda-147">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](resource-sign-up-preview-subscription.md) et [Mettre en service un nouvel environnement](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="23cda-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="23cda-148">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="23cda-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="23cda-149">Planification de projet à l’aide du WBS</span><span class="sxs-lookup"><span data-stu-id="23cda-149">Project planning using WBS</span></span>
- <span data-ttu-id="23cda-150">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="23cda-150">Resource Management</span></span>
- <span data-ttu-id="23cda-151">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="23cda-151">Time Tracking</span></span>
- <span data-ttu-id="23cda-152">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="23cda-152">Full Expense</span></span>
- <span data-ttu-id="23cda-153">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="23cda-153">Receipt OCR</span></span>
- <span data-ttu-id="23cda-154">Facturation complète</span><span class="sxs-lookup"><span data-stu-id="23cda-154">Full Invoicing</span></span>
- <span data-ttu-id="23cda-155">Comptabilisation de clôture</span><span class="sxs-lookup"><span data-stu-id="23cda-155">Revenue Recognition</span></span>
- <span data-ttu-id="23cda-156">Ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="23cda-156">Production Orders</span></span>
- <span data-ttu-id="23cda-157">Prise en charge des matériaux</span><span class="sxs-lookup"><span data-stu-id="23cda-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="23cda-158">Étapes de déploiement :</span><span class="sxs-lookup"><span data-stu-id="23cda-158">Deployment steps:</span></span>
<span data-ttu-id="23cda-159">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="23cda-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="23cda-160">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) et [Mettre en service un nouvel environnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="23cda-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



