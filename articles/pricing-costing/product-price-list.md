---
title: Tarifs des produits
description: Cette rubrique fournit des informations sur les tarifs des catalogues utilisés pour les devis de projet et les contrats.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877487"
---
# <a name="product-price-lists"></a><span data-ttu-id="3ff7f-103">Tarifs des produits</span><span class="sxs-lookup"><span data-stu-id="3ff7f-103">Product price lists</span></span>

<span data-ttu-id="3ff7f-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="3ff7f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="3ff7f-105">Dans Project Operations, les **tarifs des produits** et les entités d’élément tarifaire associées prennent en charge la fonctionnalité de tarification des produits sur des lignes de devis et de contrats basés sur des produits.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="3ff7f-106">Pour les produits utilisés dans les projets, les enregistrements d’élément tarifaire pour les listes de prix de projet sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="3ff7f-107">Les produits doivent être configurés afin de ne pas avoir le coût et les tarifs par défaut dans le catalogue des produits.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="3ff7f-108">Utilisez les tarifs, le coût standard, et le coût actuel pour configurer le coût et les tarifs par défaut.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="3ff7f-109">Les tarifs par défaut sont utilisés sur une ligne de devis ou une ligne de contrat du projet uniquement lorsque le système ne parvient pas à trouver une ligne de tarifs pour ce produit dans la liste des tarifs du devis ou du contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="3ff7f-110">Le prix de revient des lignes du catalogue de produits peut être modifié entre devis.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="3ff7f-111">Cette fonctionnalité est importante, car si vous ne suivez pas précisément les coûts, vous ne pouvez pas déterminer les bénéfices opérationnels par rapport aux engagements du projet.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="3ff7f-112">Par défaut, le coût standard du produit est utilisé comme prix de revient.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="3ff7f-113">Toutefois, le prix de revient par défaut peut être mis à jour sur la ligne de devis s’il existe un prix de revient distinct pour ce devis.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="3ff7f-114">Éléments tarifaires</span><span class="sxs-lookup"><span data-stu-id="3ff7f-114">Price list items</span></span>

<span data-ttu-id="3ff7f-115">Vous pouvez ajouter des produits d’un catalogue de produits à plusieurs tarifs.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="3ff7f-116">Les lignes de tarifs pour les produits référencent toujours une unité spécifique.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="3ff7f-117">La tarification d’un produit sur les éléments tarifaires peut être configurée comme un montant en devise.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="3ff7f-118">Sinon, elle peut être configurée en fonction du tarif, du coût actuel ou du coût standard.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="3ff7f-119">La fonctionnalité de tarification prend en charge diverses options d’arrondi si les prix des produits sont configurés en fonction du tarif, du coût standard ou du coût actuel.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="3ff7f-120">En plus de bénéficier de plusieurs modes de tarification et d’options d’arrondis, vous pouvez associer des types de remises aux éléments tarifaires.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="3ff7f-121">Tarif de produit par défaut</span><span class="sxs-lookup"><span data-stu-id="3ff7f-121">Default product price list</span></span>
<span data-ttu-id="3ff7f-122">Chaque enregistrement client a un champ **Tarifs par défaut**, dans lequel vous pouvez spécifier un tarif correspondant à la devise du client.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="3ff7f-123">Une valeur par défaut n’est pas automatiquement entrée dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="3ff7f-124">Lorsqu’un contrat de tarification personnalisé avec un client spécifique existe, vous pouvez utiliser ce champ pour associer des tarifs à ce client.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="3ff7f-125">Les entités Opportunité, Devis et Contrat de projet utilisent l’ordre suivant pour entrer des tarifs de produits par défaut.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="3ff7f-126">Le même ordre est utilisé pour les tarifs de projets.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="3ff7f-127">Devis</span><span class="sxs-lookup"><span data-stu-id="3ff7f-127">Quote</span></span>
2.  <span data-ttu-id="3ff7f-128">Opportunité</span><span class="sxs-lookup"><span data-stu-id="3ff7f-128">Opportunity</span></span>
3.  <span data-ttu-id="3ff7f-129">Client</span><span class="sxs-lookup"><span data-stu-id="3ff7f-129">Customer</span></span>
4.  <span data-ttu-id="3ff7f-130">Paramètres globaux</span><span class="sxs-lookup"><span data-stu-id="3ff7f-130">Global settings</span></span> 

<span data-ttu-id="3ff7f-131">Par défaut, le champ **Produit** sur la ligne de devis liste tous les produits actifs dans les tarifs de produits du devis.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="3ff7f-132">Si un produit a été désactivé, ou s’il s’agit d’un brouillon de produit, il n’est pas répertorié, même s’il est dans les tarifs.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="3ff7f-133">Les lignes du catalogue de produits sont ajoutées en tant que lignes de facture dans la première facture créée pour un contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="3ff7f-134">Dans un brouillon de facture, ces lignes de facture peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="3ff7f-135">Dans ce cas, les lignes s’afficheront sur une facture suivante jusqu’à ce qu’elles soient facturées, ou jusqu’à ce que la facture soit envoyée au client.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="3ff7f-136">Vous ne pouvez pas facturer une quantité partielle d’une ligne de facture de produit.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="3ff7f-137">Lorsque les lignes de produits du contrat du projet sont facturées, les chiffres réels sont créés.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="3ff7f-138">Toutefois, ces chiffres réels ne sont pas liés à l’entité de projet associée.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="3ff7f-139">En d’autres termes, les lignes du contrat du projet basé sur un produit sont indépendantes de toute utilisation basée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
