---
title: Vue d’ensemble des lignes de contrat basées sur un projet – Simplifié
description: Cette rubrique fournit des informations sur les lignes de contrat basées sur un produit.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994538"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="55e32-103">Vue d’ensemble des lignes de contrat basées sur un projet – Simplifié</span><span class="sxs-lookup"><span data-stu-id="55e32-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="55e32-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="55e32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55e32-105">Vous pouvez créer des lignes de contrat basées sur un produit dans Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="55e32-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="55e32-106">Les lignes de contrat basées sur un produit peuvent être créées manuellement ou provenir des articles du catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="55e32-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="55e32-107">Catalogue de produits</span><span class="sxs-lookup"><span data-stu-id="55e32-107">Product catalog</span></span>

<span data-ttu-id="55e32-108">Les produits du catalogue de produits contiennent une unité et un groupe d’unités par défaut.</span><span class="sxs-lookup"><span data-stu-id="55e32-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="55e32-109">Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui comporte également ces attributs.</span><span class="sxs-lookup"><span data-stu-id="55e32-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="55e32-110">Tous les produits d’une famille de produits héritent du même ensemble d’attributs.</span><span class="sxs-lookup"><span data-stu-id="55e32-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="55e32-111">Par exemple, une société vend des licences d’abonnement pour différents types de logiciel.</span><span class="sxs-lookup"><span data-stu-id="55e32-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="55e32-112">Tout les logiciels sur abonnement ont les deux attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="55e32-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="55e32-113">Nombre d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="55e32-113">Number of users</span></span>
- <span data-ttu-id="55e32-114">Durée de l’abonnement (en mois)</span><span class="sxs-lookup"><span data-stu-id="55e32-114">Subscription duration (in months)</span></span>

<span data-ttu-id="55e32-115">Pour gérer ce type de catalogue, créez une famille de produits nommée **Logiciel d’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="55e32-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="55e32-116">Ajoutez les attributs, **Nombre d’utilisateurs** et **Durée de l’abonnement** à la famille de produits.</span><span class="sxs-lookup"><span data-stu-id="55e32-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="55e32-117">Ajoutez ensuite des produits individuels à la famille de produits **Logiciel d’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="55e32-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="55e32-118">Ajouter des articles du catalogue de produits à un contrat de projet</span><span class="sxs-lookup"><span data-stu-id="55e32-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="55e32-119">Les contrats de projet comportent des sections pour deux types de lignes : basées sur un projet et basées sur un produit.</span><span class="sxs-lookup"><span data-stu-id="55e32-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="55e32-120">Les lignes basées sur un produit incluent tous les produits et unités du tarif des produits du contrat.</span><span class="sxs-lookup"><span data-stu-id="55e32-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="55e32-121">Les produits qui ne figurent pas dans les tarifs des produits du contrat peuvent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="55e32-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="55e32-122">Vous pouvez sélectionner des produits à partir d’autres tarifs ou directement à partir du catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="55e32-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="55e32-123">Lorsque vous sélectionnez des produits directement à partir d’un catalogue de produits, le tarif par défaut de ce produit est utilisé pour le prix de vente du produit.</span><span class="sxs-lookup"><span data-stu-id="55e32-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="55e32-124">Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="55e32-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="55e32-125">Si une ligne de contrat est basée sur un catalogue de produits, vous pouvez remplacer le tarif de vente directement sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="55e32-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="55e32-126">Le champ **Tarification** d’une ligne de contrat a les deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="55e32-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="55e32-127">**Remplacer la tarification**</span><span class="sxs-lookup"><span data-stu-id="55e32-127">**Override pricing**</span></span>
- <span data-ttu-id="55e32-128">**Utiliser la valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="55e32-128">**Use default**</span></span>

<span data-ttu-id="55e32-129">Si vous définissez le champ **Tarification** sur **Remplacer la tarification**, le prix par défaut n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="55e32-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="55e32-130">Entrez un prix pour le produit sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="55e32-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="55e32-131">Si vous définissez le champ sur **Utiliser la valeur par défaut**, le prix de vente par défaut est utilisé et le champ ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="55e32-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="55e32-132">Après avoir installé Project Operations, des prix de vente par défaut sont entrés dans les lignes basées sur un produit d’un contrat.</span><span class="sxs-lookup"><span data-stu-id="55e32-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="55e32-133">Le champ **Tarification** est défini sur **Remplacer la tarification** afin que vous puissiez modifier le prix par défaut sur les lignes de contrat.</span><span class="sxs-lookup"><span data-stu-id="55e32-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="55e32-134">Il s’agit d’un remplacement spécifique à Project Operations du comportement des lignes basées sur un produit dans Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="55e32-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]