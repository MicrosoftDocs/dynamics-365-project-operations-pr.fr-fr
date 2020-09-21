---
title: Configurer Project Service Automation
description: Étapes de configuration de Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168031"
---
# <a name="configure-project-service"></a><span data-ttu-id="88da9-103">Configurer Project Service</span><span class="sxs-lookup"><span data-stu-id="88da9-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="88da9-104">Avant de pouvoir utiliser les fonctionnalités d'automatisation du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dans [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pour gérer vos comptes, projets et ressources, vous devez exécuter quelques étapes de configuration pour garantir que la solution de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] correspond aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88da9-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="88da9-105">Il s’agit notamment des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="88da9-105">These steps include:</span></span>  
  
-   <span data-ttu-id="88da9-106">[Configurer les unités de temps](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="88da9-107">Configurez les unités de temps dans le catalogue de produits que vous utiliserez comme base pour planifier et facturer vos projets.</span><span class="sxs-lookup"><span data-stu-id="88da9-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="88da9-108">[Configurer les devises et les taux de change](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="88da9-109">Configurez les devises pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="88da9-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="88da9-110">[Créer des unités d’organisation](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="88da9-111">Configurez les groupes que votre société utilise pour diviser son entreprise, par zone géographique, fonction professionnelle, ou toute autre division logique.</span><span class="sxs-lookup"><span data-stu-id="88da9-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="88da9-112">[Configurer les fréquences de facturation](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="88da9-113">Configurez des périodes de temps à utiliser pour facturer vos clients.</span><span class="sxs-lookup"><span data-stu-id="88da9-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="88da9-114">[Configurer les catégories de transactions](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="88da9-115">Configurez les catégories de transactions pour lesquelles vos consultants peuvent facturer leurs dépenses facturables et non facturables.</span><span class="sxs-lookup"><span data-stu-id="88da9-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="88da9-116">[Configurer les catégories de dépenses](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="88da9-117">Configurez les catégories pour lesquelles vos consultants peuvent facturer leurs dépenses facturables et non facturables.</span><span class="sxs-lookup"><span data-stu-id="88da9-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="88da9-118">[Créer des articles du catalogue de produits](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="88da9-119">Ajoutez les produits que vous vendez, tels que des licences de logiciels, au catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="88da9-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="88da9-120">[Créer un tarif](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="88da9-121">Configurez les différents tarifs, selon le prix que vous voulez facturer à vos clients pour chaque rôle dont leur projet a besoin.</span><span class="sxs-lookup"><span data-stu-id="88da9-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="88da9-122">[Configurer les ressources](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="88da9-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="88da9-123">Ajoutez les qualifications, les compétences, les rôles de ressource, et d'autres données des ressources dont vous aurez besoin pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="88da9-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="88da9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88da9-124">See Also</span></span>  
 <span data-ttu-id="88da9-125">[Vue d'ensemble de Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="88da9-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="88da9-126">[Configurer Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="88da9-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="88da9-127">[Guide du responsable de projet](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="88da9-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="88da9-128">[Guide du responsable de projet](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="88da9-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="88da9-129">[Guide du gestionnaire de ressources](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="88da9-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="88da9-130">Guide sur le temps, les dépenses et la collaboration</span><span class="sxs-lookup"><span data-stu-id="88da9-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
