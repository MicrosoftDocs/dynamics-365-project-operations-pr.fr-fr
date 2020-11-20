---
title: Déterminer votre type de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401215"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="87731-103">Déterminer votre type de déploiement</span><span class="sxs-lookup"><span data-stu-id="87731-103">Determine your deployment type</span></span>

<span data-ttu-id="87731-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="87731-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87731-105">Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations à l’aide du [Flux d’installation guidé](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="87731-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="87731-106">Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation.</span><span class="sxs-lookup"><span data-stu-id="87731-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="87731-107">Consultez les détails de déploiement pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="87731-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="87731-108">Clients Dynamics existants utilisant Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="87731-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="87731-109">Project Operations inclut les fonctionnalités fournies avec Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="87731-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="87731-110">Une mise à niveau sera publiée pour ces clients dans la vague de lancement de 2021.</span><span class="sxs-lookup"><span data-stu-id="87731-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="87731-111">Clients Dynamics 365 Finance existants utilisant Gestion de projets et comptabilité</span><span class="sxs-lookup"><span data-stu-id="87731-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="87731-112">Les clients existants de Finance qui utilisent la fonctionnalité Gestion du projet et comptabilité peuvent continuer à l’utiliser tel qu’il est.</span><span class="sxs-lookup"><span data-stu-id="87731-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="87731-113">Voir [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma).</span><span class="sxs-lookup"><span data-stu-id="87731-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="87731-114">Types de déploiement</span><span class="sxs-lookup"><span data-stu-id="87731-114">Deployment types</span></span>
<span data-ttu-id="87731-115">Project Operations prend en charge plusieurs options de déploiement pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="87731-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="87731-116">Que vous soyez un client Dynamics 365 nouveau ou existant, Project Operations peut répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="87731-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="87731-117">Notre [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations) vous aidera à déterminer le bon déploiement.</span><span class="sxs-lookup"><span data-stu-id="87731-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="87731-118">Les résultats vous guideront vers l’un des types de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="87731-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="87731-119">Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="87731-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="87731-120">Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="87731-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="87731-121">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="87731-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="87731-122">Project Operations prend en charge les scénarios stockés/d’ordre de fabrication et les scénarios non stockés/basés sur les ressources dans le même environnement par le biais des configurations au niveau de l’entité juridique.</span><span class="sxs-lookup"><span data-stu-id="87731-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="87731-123">Par exemple, Contoso peut utiliser les fonctionnalités stockées/ordre de fabrication dans son usine de fabrication aux États-Unis (entité juridique = Contoso Manufacturing, États-Unis).</span><span class="sxs-lookup"><span data-stu-id="87731-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="87731-124">Contoso peut utiliser les fonctionnalités non stockées / basées sur les ressources dans son installation de maintenance Contoso Robotics Arms au Royaume-Uni (entité juridique = Contoso Robotics, Royaume-Uni).</span><span class="sxs-lookup"><span data-stu-id="87731-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="87731-125">Déploiement simplifié – Traiter la facturation pro forma</span><span class="sxs-lookup"><span data-stu-id="87731-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="87731-126">Le déploiement simplifié comprend les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="87731-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="87731-127">Processus de vente pour les projets qui étendent les expériences d’application Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="87731-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="87731-128">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="87731-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="87731-129">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="87731-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="87731-130">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="87731-130">Unified resource management</span></span>
- <span data-ttu-id="87731-131">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="87731-131">Time tracking</span></span>
- <span data-ttu-id="87731-132">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="87731-132">Basic expense</span></span>
- <span data-ttu-id="87731-133">Facturation pro forma et client</span><span class="sxs-lookup"><span data-stu-id="87731-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="87731-134">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="87731-134">Deployment steps</span></span>
<span data-ttu-id="87731-135">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="87731-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="87731-136">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](lite-preview-subscription-sign-up.md) et [Mettre en service un nouvel environnement](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="87731-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="87731-137">Project Operations pour les scénarios basés sur les ressources/produits non stockés</span><span class="sxs-lookup"><span data-stu-id="87731-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="87731-138">Project Operations pour les scénarios de ressources/non stockés incluent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="87731-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="87731-139">Processus de vente pour les projets qui étendent les applications Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="87731-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="87731-140">Planification de projet à l’aide de Microsoft Project pour le web</span><span class="sxs-lookup"><span data-stu-id="87731-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="87731-141">Tarification multidimensionnelle</span><span class="sxs-lookup"><span data-stu-id="87731-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="87731-142">Gestion des ressources unifiée</span><span class="sxs-lookup"><span data-stu-id="87731-142">Unified resource management</span></span>
- <span data-ttu-id="87731-143">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="87731-143">Time tracking</span></span>
- <span data-ttu-id="87731-144">Dépenses de base</span><span class="sxs-lookup"><span data-stu-id="87731-144">Basic expense</span></span>
- <span data-ttu-id="87731-145">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="87731-145">Full expense</span></span>
- <span data-ttu-id="87731-146">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="87731-146">Receipt OCR</span></span>
- <span data-ttu-id="87731-147">Facturation pro forma et client</span><span class="sxs-lookup"><span data-stu-id="87731-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="87731-148">Constatation du produit pour les projets</span><span class="sxs-lookup"><span data-stu-id="87731-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="87731-149">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="87731-149">Deployment steps</span></span>
<span data-ttu-id="87731-150">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="87731-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="87731-151">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](resource-sign-up-preview-subscription.md) et [Mettre en service un nouvel environnement](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="87731-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="87731-152">Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="87731-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="87731-153">Planification de projet à l’aide du WBS</span><span class="sxs-lookup"><span data-stu-id="87731-153">Project planning using WBS</span></span>
- <span data-ttu-id="87731-154">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="87731-154">Resource Management</span></span>
- <span data-ttu-id="87731-155">Suivi du temps</span><span class="sxs-lookup"><span data-stu-id="87731-155">Time Tracking</span></span>
- <span data-ttu-id="87731-156">Dépense complète</span><span class="sxs-lookup"><span data-stu-id="87731-156">Full Expense</span></span>
- <span data-ttu-id="87731-157">OCR du reçu</span><span class="sxs-lookup"><span data-stu-id="87731-157">Receipt OCR</span></span>
- <span data-ttu-id="87731-158">Facturation complète</span><span class="sxs-lookup"><span data-stu-id="87731-158">Full Invoicing</span></span>
- <span data-ttu-id="87731-159">Comptabilisation de clôture</span><span class="sxs-lookup"><span data-stu-id="87731-159">Revenue Recognition</span></span>
- <span data-ttu-id="87731-160">Ordres de fabrication</span><span class="sxs-lookup"><span data-stu-id="87731-160">Production Orders</span></span>
- <span data-ttu-id="87731-161">Prise en charge des matériaux</span><span class="sxs-lookup"><span data-stu-id="87731-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="87731-162">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="87731-162">Deployment steps</span></span>
<span data-ttu-id="87731-163">Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="87731-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="87731-164">Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) et [Mettre en service un nouvel environnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="87731-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

