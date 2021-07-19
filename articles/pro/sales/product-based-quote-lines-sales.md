---
title: Vue d’ensemble des lignes du devis basées sur les produits – Simplifié
description: Cette rubrique fournit des informations pour travailler avec des lignes de devis basées sur les produits.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369823"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="6d492-103">Vue d’ensemble des lignes du devis basées sur les produits – Simplifié</span><span class="sxs-lookup"><span data-stu-id="6d492-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="6d492-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="6d492-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6d492-105">Vous pouvez créer des lignes de devis basées sur un produit dans Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6d492-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="6d492-106">Les lignes de devis basées sur les produits peuvent ajoutées manuellement, ou elles peuvent provenir des articles du catalogue des produits.</span><span class="sxs-lookup"><span data-stu-id="6d492-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="6d492-107">Catalogue de produits</span><span class="sxs-lookup"><span data-stu-id="6d492-107">Product catalog</span></span>

<span data-ttu-id="6d492-108">Chaque produit dans le catalogue de produits contient une unité et un groupe d’unités par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d492-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="6d492-109">Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui partage ces attributs.</span><span class="sxs-lookup"><span data-stu-id="6d492-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="6d492-110">Par exemple, une société vend des licences d’abonnement pour différents types de logiciel.</span><span class="sxs-lookup"><span data-stu-id="6d492-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="6d492-111">Tout les logiciels sur abonnement ont les deux attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="6d492-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="6d492-112">Nombre d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6d492-112">Number of users</span></span>
- <span data-ttu-id="6d492-113">Durée de l’abonnement mesurée en mois</span><span class="sxs-lookup"><span data-stu-id="6d492-113">A subscription duration measured in months</span></span>

<span data-ttu-id="6d492-114">Pour gérer ce type de catalogue, créez une famille de produits nommée **Logiciel sur abonnement** et ajoutez le nombre d’utilisateurs et la durée de l’abonnement comme attributs.</span><span class="sxs-lookup"><span data-stu-id="6d492-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="6d492-115">Ensuite, ajoutez des produits individuels à la famille de produits **Logiciel sur abonnement**.</span><span class="sxs-lookup"><span data-stu-id="6d492-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="6d492-116">Ajouter des articles du catalogue de produits à un devis de projet</span><span class="sxs-lookup"><span data-stu-id="6d492-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="6d492-117">Les pages **Devis de devis** et **Contrat du projet** ont des sections pour deux types de lignes : lignes basées sur un projet et lignes basées sur les produits.</span><span class="sxs-lookup"><span data-stu-id="6d492-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="6d492-118">Pour les lignes basées sur les produits, la liste déroulante dans la ligne de devis ou la ligne de contrat du projet comprend tous les produits et unités des tarifs des produits.</span><span class="sxs-lookup"><span data-stu-id="6d492-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="6d492-119">Vous pouvez également ajouter des produits qui ne figurent pas dans les tarifs des produits.</span><span class="sxs-lookup"><span data-stu-id="6d492-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="6d492-120">En outre, vous pouvez sélectionner des produits d’autres tarifs ou directement dans le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="6d492-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="6d492-121">Lorsque vous sélectionnez les produits directement à partir d’un catalogue de produits, les tarifs par défaut de ce produit sont utilisés pour obtenir le prix de vente du produit.</span><span class="sxs-lookup"><span data-stu-id="6d492-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="6d492-122">Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6d492-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="6d492-123">Lorsqu’une ligne de devis est basée sur un catalogue de produits, vous pouvez remplacer le prix de vente directement sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="6d492-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="6d492-124">Une ligne de devis dans le champ **Tarification** avec deux valeurs disponibles :</span><span class="sxs-lookup"><span data-stu-id="6d492-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="6d492-125">**Remplacer tarifs**</span><span class="sxs-lookup"><span data-stu-id="6d492-125">**Override Pricing**</span></span>
- <span data-ttu-id="6d492-126">**Utiliser la valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="6d492-126">**Use Default**</span></span>

<span data-ttu-id="6d492-127">Si vous sélectionnez **Remplacer la tarification**, le prix par défaut n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6d492-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="6d492-128">Vous devez plutôt saisir un prix pour le produit dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="6d492-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="6d492-129">Si vous sélectionnez **Utiliser la valeur par défaut**, le tarif de vente par défaut est utilisé et le champ est verrouillé pour modification.</span><span class="sxs-lookup"><span data-stu-id="6d492-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="6d492-130">Des prix de vente par défaut sont saisis dans les lignes basées sur les produits d’un devis.</span><span class="sxs-lookup"><span data-stu-id="6d492-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="6d492-131">Le champ **Tarification** est alors défini sur **Remplacer la tarification** pour pouvoir modifier le prix par défaut sur les lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="6d492-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="6d492-132">Il s’agit d’un remplacement spécifique à Project Operations du comportement des lignes basées sur les produits dans Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6d492-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]