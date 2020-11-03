---
title: Déterminer votre type de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075744"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="d28ae-103">Déterminer votre type de déploiement</span><span class="sxs-lookup"><span data-stu-id="d28ae-103">Determine your deployment type</span></span>

<span data-ttu-id="d28ae-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="d28ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d28ae-105">Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations à l’aide du [Flux d’installation guidé](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d28ae-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="d28ae-106">Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation.</span><span class="sxs-lookup"><span data-stu-id="d28ae-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="d28ae-107">Consultez les détails de déploiement pour terminer l'installation.</span><span class="sxs-lookup"><span data-stu-id="d28ae-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="d28ae-108">Clients Dynamics existants utilisant Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d28ae-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="d28ae-109">Project Operations inclut les fonctionnalités fournies avec Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d28ae-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="d28ae-110">Un chemin d’accès à la mise à niveau sera publié pour ces clients à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d28ae-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="d28ae-111">Clients Dynamics 365 Finance existants utilisant Gestion de projets et comptabilité</span><span class="sxs-lookup"><span data-stu-id="d28ae-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="d28ae-112">Les clients Finance existants qui utilisent la fonctionnalité Gestion de projet et comptabilité peuvent continuer à l'utiliser tel quel.</span><span class="sxs-lookup"><span data-stu-id="d28ae-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="d28ae-113">Voir [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma).</span><span class="sxs-lookup"><span data-stu-id="d28ae-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="d28ae-114">Types de déploiement</span><span class="sxs-lookup"><span data-stu-id="d28ae-114">Deployment types</span></span>
<span data-ttu-id="d28ae-115">Project Operations prend en charge plusieurs options de déploiement pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d28ae-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="d28ae-116">Que vous soyez un client Dynamics 365 nouveau ou existant, Project Operations peut répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d28ae-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="d28ae-117">Notre [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations) vous aidera à déterminer le bon déploiement.</span><span class="sxs-lookup"><span data-stu-id="d28ae-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="d28ae-118">Les résultats vous guideront vers l’un des types de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="d28ae-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="d28ae-119">Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="d28ae-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="d28ae-120">Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="d28ae-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="d28ae-121">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="d28ae-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="d28ae-122">Project Operations prend en charge les scénarios stockés/d’ordre de fabrication et les scénarios non stockés/basés sur les ressources dans le même environnement par le biais des configurations au niveau de l’entité juridique.</span><span class="sxs-lookup"><span data-stu-id="d28ae-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="d28ae-123">Par exemple, Contoso peut utiliser les fonctionnalités stockées/ordre de fabrication dans son usine de fabrication aux États-Unis (entité juridique = Contoso Manufacturing, États-Unis).</span><span class="sxs-lookup"><span data-stu-id="d28ae-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="d28ae-124">Contoso peut utiliser les fonctionnalités non stockées / basées sur les ressources dans son installation de maintenance Contoso Robotics Arms au Royaume-Uni (entité juridique = Contoso Robotics, Royaume-Uni).</span><span class="sxs-lookup"><span data-stu-id="d28ae-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="d28ae-125">Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="d28ae-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="d28ae-126">Le déploiement simplifié comprend les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d28ae-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="d28ae-127">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="d28ae-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d28ae-128">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="d28ae-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d28ae-129">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="d28ae-129">Unified Resource Management</span></span>
- <span data-ttu-id="d28ae-130">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="d28ae-130">Time Tracking</span></span>
- <span data-ttu-id="d28ae-131">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="d28ae-131">Basic Expense</span></span>
- <span data-ttu-id="d28ae-132">Proposition de facture</span><span class="sxs-lookup"><span data-stu-id="d28ae-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d28ae-133">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="d28ae-133">Deployment steps</span></span>
<span data-ttu-id="d28ae-134">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d28ae-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d28ae-135">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](lite-preview-subscription-sign-up.md) et [Mettre en service un nouvel environnement](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="d28ae-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="d28ae-136">Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="d28ae-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="d28ae-137">Project Operations pour les scénarios de ressources/non stockés incluent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d28ae-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="d28ae-138">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="d28ae-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d28ae-139">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="d28ae-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d28ae-140">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="d28ae-140">Unified Resource Management</span></span>
- <span data-ttu-id="d28ae-141">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="d28ae-141">Time Tracking</span></span>
- <span data-ttu-id="d28ae-142">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="d28ae-142">Basic Expense</span></span>
- <span data-ttu-id="d28ae-143">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="d28ae-143">Full Expense</span></span>
- <span data-ttu-id="d28ae-144">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="d28ae-144">Receipt OCR</span></span>
- <span data-ttu-id="d28ae-145">Facturation complète</span><span class="sxs-lookup"><span data-stu-id="d28ae-145">Full Invoicing</span></span>
- <span data-ttu-id="d28ae-146">Comptabilisation de clôture</span><span class="sxs-lookup"><span data-stu-id="d28ae-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d28ae-147">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="d28ae-147">Deployment steps</span></span>
<span data-ttu-id="d28ae-148">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d28ae-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d28ae-149">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](resource-sign-up-preview-subscription.md) et [Mettre en service un nouvel environnement](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d28ae-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="d28ae-150">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="d28ae-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="d28ae-151">Planification de projet à l’aide du WBS</span><span class="sxs-lookup"><span data-stu-id="d28ae-151">Project planning using WBS</span></span>
- <span data-ttu-id="d28ae-152">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="d28ae-152">Resource Management</span></span>
- <span data-ttu-id="d28ae-153">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="d28ae-153">Time Tracking</span></span>
- <span data-ttu-id="d28ae-154">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="d28ae-154">Full Expense</span></span>
- <span data-ttu-id="d28ae-155">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="d28ae-155">Receipt OCR</span></span>
- <span data-ttu-id="d28ae-156">Facturation complète</span><span class="sxs-lookup"><span data-stu-id="d28ae-156">Full Invoicing</span></span>
- <span data-ttu-id="d28ae-157">Comptabilisation de clôture</span><span class="sxs-lookup"><span data-stu-id="d28ae-157">Revenue Recognition</span></span>
- <span data-ttu-id="d28ae-158">Ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="d28ae-158">Production Orders</span></span>
- <span data-ttu-id="d28ae-159">Prise en charge des matériaux</span><span class="sxs-lookup"><span data-stu-id="d28ae-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d28ae-160">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="d28ae-160">Deployment steps</span></span>
<span data-ttu-id="d28ae-161">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d28ae-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d28ae-162">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) et [Mettre en service un nouvel environnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d28ae-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

