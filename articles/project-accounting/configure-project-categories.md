---
title: Configurer les catégories de projets
description: Cette rubrique fournit des informations sur le paramétrage des catégories de projet.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075636"
---
# <a name="configure-project-categories"></a><span data-ttu-id="9e91f-103">Configurer les catégories de projets</span><span class="sxs-lookup"><span data-stu-id="9e91f-103">Configure project categories</span></span>

<span data-ttu-id="9e91f-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="9e91f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9e91f-105">Project Operations offre de solides capacités de catégorisation des revenus et des dépenses sur les projets.</span><span class="sxs-lookup"><span data-stu-id="9e91f-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="9e91f-106">Les catégories offrent la possibilité de rendre compte et d’analyser les transactions du projet et de diriger la validation dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="9e91f-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="9e91f-107">Le diagramme suivant illustre la corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet.</span><span class="sxs-lookup"><span data-stu-id="9e91f-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="9e91f-108">Les catégories de transaction constituent le regroupement de base des transactions de projet.</span><span class="sxs-lookup"><span data-stu-id="9e91f-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="9e91f-109">Au sein de ce groupe, il existe un ensemble de catégories partagées qui peuvent être partagées entre les applications et les modules.</span><span class="sxs-lookup"><span data-stu-id="9e91f-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="9e91f-110">Pour aller encore plus loin dans les détails, les catégories de projets sont le niveau de catégories le plus granulaire.</span><span class="sxs-lookup"><span data-stu-id="9e91f-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="9e91f-111">Les catégories de projet sont spécifiques à l’entité juridique, au module et à l’application.</span><span class="sxs-lookup"><span data-stu-id="9e91f-111">Project categories are specific to legal entity, module, and application.</span></span>

![Corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="9e91f-113">Catégories de transactions</span><span class="sxs-lookup"><span data-stu-id="9e91f-113">Transaction categories</span></span>

<span data-ttu-id="9e91f-114">Les catégories de transaction représentent le regroupement de base des transactions de projet et ne sont pas spécifiques à la société ou au type de transaction.</span><span class="sxs-lookup"><span data-stu-id="9e91f-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="9e91f-115">Par exemple, Contoso Robotics utilise les catégories Conception, Déplacement, Installation et Transaction de service pour regrouper les transactions de projet.</span><span class="sxs-lookup"><span data-stu-id="9e91f-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="9e91f-116">Les catégories de transaction sont définies dans le module Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9e91f-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="9e91f-117">Accédez à **Paramètres** \> **Catégories de transaction** pour ouvrir le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9e91f-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="9e91f-118">Créez une catégorie de transaction en sélectionnant **Nouveau** ou en sélectionnant **Importer depuis Excel**.</span><span class="sxs-lookup"><span data-stu-id="9e91f-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="9e91f-119">Catégories partagées</span><span class="sxs-lookup"><span data-stu-id="9e91f-119">Shared categories</span></span>

<span data-ttu-id="9e91f-120">Dynamics 365 utilise le concept de catégories partagées pour classer les dépenses dans différentes applications, telles que Dynamics 365 Finance, Dynamics 365 Supply Chain et Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9e91f-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="9e91f-121">Pour chaque catégorie de transaction créée, Project Operations crée automatiquement quatre catégories partagées associées : Heures, Dépenses, Frais et Article.</span><span class="sxs-lookup"><span data-stu-id="9e91f-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="9e91f-122">Vous pouvez consulter et ajuster les catégories partagées en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories partagées**.</span><span class="sxs-lookup"><span data-stu-id="9e91f-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="9e91f-123">Catégories de projets</span><span class="sxs-lookup"><span data-stu-id="9e91f-123">Project categories</span></span>

<span data-ttu-id="9e91f-124">Les catégories de projet représentent le niveau le plus granulaire de configuration de catégorie et doivent être configurées séparément, et pour chaque entreprise, par un comptable de projet.</span><span class="sxs-lookup"><span data-stu-id="9e91f-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="9e91f-125">Accédez à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories de projets**.</span><span class="sxs-lookup"><span data-stu-id="9e91f-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="9e91f-126">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9e91f-126">Select **New**.</span></span>
3. <span data-ttu-id="9e91f-127">Sélectionnez l’ **Identificateur de catégorie** de la catégorie partagée créée dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="9e91f-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="9e91f-128">Project Operations permet d’utiliser uniquement les catégories partagées associées aux catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="9e91f-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="9e91f-129">Sélectionnez un groupe de catégories.</span><span class="sxs-lookup"><span data-stu-id="9e91f-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="9e91f-130">Groupes de catégories</span><span class="sxs-lookup"><span data-stu-id="9e91f-130">Category groups</span></span>

<span data-ttu-id="9e91f-131">Les groupes de catégories sont utilisés pour partager des propriétés, principalement des profils de publication, entre des catégories de projet associées.</span><span class="sxs-lookup"><span data-stu-id="9e91f-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="9e91f-132">Il doit y avoir au moins un groupe de catégories pour chaque type de transaction et chaque catégorie de projet se voit attribuer un groupe.</span><span class="sxs-lookup"><span data-stu-id="9e91f-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="9e91f-133">Les spécifications de validation dans Project Operations sont définies par les règles de profil de coût et de produit du projet, les catégories de projet et les groupes de catégories.</span><span class="sxs-lookup"><span data-stu-id="9e91f-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="9e91f-134">Vous pouvez configurer des groupes de catégories en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Groupes de catégories**.</span><span class="sxs-lookup"><span data-stu-id="9e91f-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
