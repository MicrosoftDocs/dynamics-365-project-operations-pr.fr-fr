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
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075849"
---
# <a name="configure-project-service"></a><span data-ttu-id="8a3f0-103">Configurer Project Service</span><span class="sxs-lookup"><span data-stu-id="8a3f0-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8a3f0-104">Avant de pouvoir utiliser les fonctionnalités d'automatisation du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dans [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pour gérer vos comptes, projets et ressources, vous devez exécuter quelques étapes de configuration pour garantir que la solution de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] correspond aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="8a3f0-105">Il s’agit notamment des mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a3f0-105">These steps include:</span></span>  
  
-   <span data-ttu-id="8a3f0-106">[Configurer les unités de temps](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="8a3f0-107">Configurez les unités de temps dans le catalogue de produits que vous utiliserez comme base pour planifier et facturer vos projets.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="8a3f0-108">[Configurer les devises et les taux de change](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="8a3f0-109">Configurez les devises pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="8a3f0-110">[Créer des unités d’organisation](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="8a3f0-111">Configurez les groupes que votre société utilise pour diviser son entreprise, par zone géographique, fonction professionnelle, ou toute autre division logique.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="8a3f0-112">[Configurer les fréquences de facturation](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="8a3f0-113">Configurez des périodes de temps à utiliser pour facturer vos clients.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="8a3f0-114">[Configurer les catégories de transactions](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="8a3f0-115">Configurez les catégories de transactions pour lesquelles vos consultants peuvent facturer leurs dépenses facturables et non facturables.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="8a3f0-116">[Configurer les catégories de dépenses](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="8a3f0-117">Configurez les catégories pour lesquelles vos consultants peuvent facturer leurs dépenses facturables et non facturables.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="8a3f0-118">[Créer des articles du catalogue de produits](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="8a3f0-119">Ajoutez les produits que vous vendez, tels que des licences de logiciels, au catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="8a3f0-120">[Créer un tarif](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="8a3f0-121">Configurez les différents tarifs, selon le prix que vous voulez facturer à vos clients pour chaque rôle dont leur projet a besoin.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="8a3f0-122">[Configurer les ressources](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f0-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="8a3f0-123">Ajoutez les qualifications, les compétences, les rôles de ressource, et d'autres données des ressources dont vous aurez besoin pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="8a3f0-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8a3f0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a3f0-124">See Also</span></span>  
 <span data-ttu-id="8a3f0-125">[Vue d'ensemble de Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="8a3f0-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="8a3f0-126">[Configurer Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="8a3f0-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="8a3f0-127">[Guide du responsable de projet](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8a3f0-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="8a3f0-128">[Guide du responsable de projet](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8a3f0-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="8a3f0-129">[Guide du gestionnaire de ressources](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8a3f0-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="8a3f0-130">Guide sur le temps, les dépenses et la collaboration</span><span class="sxs-lookup"><span data-stu-id="8a3f0-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
