---
title: Configurer les catégories de dépense
description: Cette rubrique fournit des informations sur la configuration des catégories de dépenses et des catégories partagées pour les notes de frais.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276120"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="7016c-103">Configurer les catégories de dépense</span><span class="sxs-lookup"><span data-stu-id="7016c-103">Set up expense categories</span></span>

<span data-ttu-id="7016c-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="7016c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7016c-105">Lorsque les employés créent des notes de frais, chaque dépense qu’ils enregistrent doit être associée à une catégorie de dépenses.</span><span class="sxs-lookup"><span data-stu-id="7016c-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="7016c-106">Les catégories de dépenses sont dérivées de catégories partagées qui peuvent être partagées entre les entités juridiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7016c-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="7016c-107">Selon la manière dont votre organisation est définie, ces catégories de dépenses peuvent également être partagées dans d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="7016c-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="7016c-108">En fonction de la définition de votre organisation et des conseils de l’équipe de mise en œuvre, vous devez déterminer si les catégories utilisées dans la gestion des dépenses seront utilisées uniquement dans la gestion des dépenses ou devraient être partagées dans d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="7016c-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="7016c-109">Ces catégories peuvent être partagées entre la gestion de projet et la comptabilité et la gestion des dépenses, ou entre la gestion de projet et la comptabilité et la production.</span><span class="sxs-lookup"><span data-stu-id="7016c-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="7016c-110">Cependant, ils ne peuvent pas être partagés entre Gestion des dépenses et Production.</span><span class="sxs-lookup"><span data-stu-id="7016c-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="7016c-111">Avant de pouvoir commencer le processus de configuration, les décisions suivantes doivent être prises pour chaque catégorie de dépenses :</span><span class="sxs-lookup"><span data-stu-id="7016c-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="7016c-112">Qu’est-ce que la catégorie de dépense ?</span><span class="sxs-lookup"><span data-stu-id="7016c-112">What is the expense category?</span></span> <span data-ttu-id="7016c-113">Les exemples incluent des catégories pour les vols, l’hôtel ou le kilométrage.</span><span class="sxs-lookup"><span data-stu-id="7016c-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="7016c-114">La catégorie de dépenses peut-elle également être utilisée dans Gestion de projet et comptabilité ?</span><span class="sxs-lookup"><span data-stu-id="7016c-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="7016c-115">Si c’est le cas, vous devez également prendre les décisions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7016c-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7016c-116">Quels comptes de coûts seront utilisés pour les dépenses suivantes ?</span><span class="sxs-lookup"><span data-stu-id="7016c-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="7016c-117">Coût</span><span class="sxs-lookup"><span data-stu-id="7016c-117">Cost</span></span>
        - <span data-ttu-id="7016c-118">Répartition de la paie</span><span class="sxs-lookup"><span data-stu-id="7016c-118">Payroll allocation</span></span>
        - <span data-ttu-id="7016c-119">TEC-Valeur de coût</span><span class="sxs-lookup"><span data-stu-id="7016c-119">WIP-cost value</span></span>
        - <span data-ttu-id="7016c-120">Coût-article</span><span class="sxs-lookup"><span data-stu-id="7016c-120">Cost-item</span></span>
        - <span data-ttu-id="7016c-121">TEC-valeur de coût-article</span><span class="sxs-lookup"><span data-stu-id="7016c-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="7016c-122">Perte accumulée</span><span class="sxs-lookup"><span data-stu-id="7016c-122">Accrued loss</span></span>
        - <span data-ttu-id="7016c-123">TEC-perte accumulée</span><span class="sxs-lookup"><span data-stu-id="7016c-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="7016c-124">Quels comptes de revenus seront utilisés pour les sources de revenus suivantes ?</span><span class="sxs-lookup"><span data-stu-id="7016c-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="7016c-125">Revenu facturé</span><span class="sxs-lookup"><span data-stu-id="7016c-125">Invoiced revenue</span></span>
        - <span data-ttu-id="7016c-126">Revenus accumulés-valeur des ventes</span><span class="sxs-lookup"><span data-stu-id="7016c-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="7016c-127">TEC-valeur des ventes</span><span class="sxs-lookup"><span data-stu-id="7016c-127">WIP-sales value</span></span>
        - <span data-ttu-id="7016c-128">Produit à recevoir – production</span><span class="sxs-lookup"><span data-stu-id="7016c-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="7016c-129">Travaux en cours – production</span><span class="sxs-lookup"><span data-stu-id="7016c-129">WIP-production</span></span>
        - <span data-ttu-id="7016c-130">Produit à recevoir – profit</span><span class="sxs-lookup"><span data-stu-id="7016c-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="7016c-131">TEC-marge</span><span class="sxs-lookup"><span data-stu-id="7016c-131">WIP-profit</span></span>
        - <span data-ttu-id="7016c-132">Revenus accumulés-abonnement</span><span class="sxs-lookup"><span data-stu-id="7016c-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="7016c-133">TEC-abonnement</span><span class="sxs-lookup"><span data-stu-id="7016c-133">WIP-subscription</span></span>

- <span data-ttu-id="7016c-134">Qu’est-ce que le type de dépense ?</span><span class="sxs-lookup"><span data-stu-id="7016c-134">What is the expense type?</span></span>
- <span data-ttu-id="7016c-135">Quel est le mode de paiement par défaut pour la catégorie de dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7016c-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="7016c-136">Les dépenses de la catégorie de dépenses doivent-elles être détaillées ?</span><span class="sxs-lookup"><span data-stu-id="7016c-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="7016c-137">Quel est le compte par défaut principal pour la catégorie de dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7016c-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="7016c-138">Quel est le groupe de taxe d’article par défaut pour la catégorie de dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7016c-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="7016c-139">Des modes de paiement supplémentaires sont-ils autorisés pour la catégorie de dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7016c-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="7016c-140">Si oui, quelles sont-elles ?</span><span class="sxs-lookup"><span data-stu-id="7016c-140">If so, what are they?</span></span>
- <span data-ttu-id="7016c-141">Y a-t-il des sous-catégories dans cette catégorie de dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7016c-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="7016c-142">S’il existe des sous-catégories, vous devez également prendre les décisions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7016c-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7016c-143">Certaines des sous-catégories sont-elles exclues du recouvrement fiscal ?</span><span class="sxs-lookup"><span data-stu-id="7016c-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="7016c-144">Quel est le groupe de taxe d’article des sous-catégories ?</span><span class="sxs-lookup"><span data-stu-id="7016c-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]