---
title: Lignes de devis basées sur un produit
description: Cette rubrique fournit des informations sur les lignes de devis basées sur un produit.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284085"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="c4d5d-103">Lignes de devis basées sur un produit</span><span class="sxs-lookup"><span data-stu-id="c4d5d-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="c4d5d-104">Vous pouvez créer des lignes de devis basées sur un produit dans Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="c4d5d-105">Les lignes de devis basées sur un produit peuvent être des lignes « hors catalogue », ou elles peuvent provenir des articles du catalogue des produits.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="c4d5d-106">Catalogue de produits</span><span class="sxs-lookup"><span data-stu-id="c4d5d-106">Product catalog</span></span>

<span data-ttu-id="c4d5d-107">Les produits d’un catalogue de produits Dynamics 365 contiennent une unité et un groupe d’unités par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="c4d5d-108">Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui comporte également ces attributs.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="c4d5d-109">Tous les produits d’une famille de produits héritent du même ensemble d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="c4d5d-110">Par exemple, une société vend des licences d’abonnement pour différents logiciels.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="c4d5d-111">Tout les logiciels sur abonnement ont les deux attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="c4d5d-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="c4d5d-112">Nombre d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c4d5d-112">Number of users</span></span> 
- <span data-ttu-id="c4d5d-113">Durée de l’abonnement (en mois)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-113">Subscription duration (in months)</span></span>

<span data-ttu-id="c4d5d-114">Un excellent moyen de gérer ce type de catalogue est de créer une famille de produits nommée **Logiciels sur abonnement**, avec **Nombre d’utilisateurs** et **Durée de l’abonnement** comme attributs.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="c4d5d-115">Vous pouvez ensuite ajouter des produits individuels, comme **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à la famille de produits **Logiciels sur abonnement**.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="c4d5d-116">Ajouter des articles du catalogue de produits à un devis de projet</span><span class="sxs-lookup"><span data-stu-id="c4d5d-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="c4d5d-117">Les pages Devis de projet et Contrat de projet ont des sections pour deux types de lignes : lignes basées sur un projet et lignes basées sur un produit.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="c4d5d-118">Pour les lignes basées sur un produit, Dynamics 365 est utilisé pour ajouter des articles d’un catalogue de produits vers un devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="c4d5d-119">La liste déroulante dans la ligne de devis ou la ligne de contrat du projet comprend tous les produits et unités des tarifs des produits joints au devis ou au contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="c4d5d-120">Vous pouvez également ajouter des produits qui ne figurent pas dans les tarifs des produits du devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="c4d5d-121">En outre, vous pouvez sélectionner des produits d’autres tarifs, ou vous pouvez sélectionner des produits directement dans le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="c4d5d-122">Lorsque vous sélectionnez les produits directement à partir d’un catalogue de produits, les tarifs par défaut de ce produit sont utilisés pour obtenir le prix de vente du produit.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="c4d5d-123">Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="c4d5d-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="c4d5d-124">Si une ligne de devis est basée sur un catalogue de produits, vous pouvez remplacer le tarif de vente directement sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="c4d5d-125">Notez qu’une ligne de devis dans Dynamics 365 possède un champ **Tarification**.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="c4d5d-126">Deux valeurs sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c4d5d-126">Two values are available:</span></span>

- <span data-ttu-id="c4d5d-127">Remplacer la tarification</span><span class="sxs-lookup"><span data-stu-id="c4d5d-127">Override pricing</span></span>  
- <span data-ttu-id="c4d5d-128">Utiliser la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c4d5d-128">Use default</span></span>

<span data-ttu-id="c4d5d-129">Si vous définissez ce champ sur **Remplacer la tarification**, Dynamics 365 ne définit pas de prix par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="c4d5d-130">Vous devez entrer un prix pour le produit dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="c4d5d-131">Si vous définissez ce champ sur **Valeur par défaut**, Dynamics 365 utilise le prix de vente par défaut et verrouille le champ pour empêcher l’édition.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="c4d5d-132">Après avoir installé PSA, des prix de vente par défaut sont entrés dans les lignes basées sur un produit d’un devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="c4d5d-133">Le champ **Tarification** est alors défini sur **Remplacer la tarification** pour pouvoir modifier le prix par défaut sur les lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Définition du remplacement de la tarification](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="c4d5d-135">Facteurs de quantité pour les produits</span><span class="sxs-lookup"><span data-stu-id="c4d5d-135">Quantity factors for products</span></span>

<span data-ttu-id="c4d5d-136">PSA utilise des facteurs de quantité pour prendre en charge la vente des produits basés sur un abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="c4d5d-137">Pour les produits basés sur abonnement, la quantité sur le devis ou la ligne de contrat du projet est exprimée sous la forme du nombre de mois d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="c4d5d-138">En règle générale, le prix des logiciels sur abonnement est stocké dans le catalogue comme prix par utilisateur par mois.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="c4d5d-139">Cependant, vous pouvez utiliser d’autres descriptions de temps à la place.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="c4d5d-140">Durant le processus de vente, le prix sur la ligne de devis est généralement le prix par utilisateur, par mois, négocié et avec remise, par l’agent de vente informatique.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="c4d5d-141">Chaque transaction a un nombre différent d’utilisateurs et un nombre différent de mois d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="c4d5d-142">La quantité utilisée pour calculer le montant de la ligne de devis est un produit du nombre d’utilisateurs et du nombre de mois d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="c4d5d-143">Pour prendre en charge ce type de vente, PSA a présenté le concept de facteurs de quantité.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="c4d5d-144">Les facteurs de quantité reposent sur les attributs du produit dans Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="c4d5d-145">Lorsque vous configurez des propriétés spécifiques pour un produit, PSA vous permet de marquer un sous-ensemble de ces propriétés, ou toutes les propriétés, comme des facteurs de la quantité.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="c4d5d-146">PSA valide que seules les propriétés numériques ou les propriétés de produit ayant un type de données numérique sont marquées comme facteurs de la quantité.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="c4d5d-147">Lorsqu’un produit pour lequel des facteurs de quantité sont configurés est ajouté à une ligne de devis, le champ **Quantité** de la ligne de devis devient un champ en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="c4d5d-148">Après avoir entré des valeurs pour les propriétés du produit qui sont des facteurs de quantité, PSA calcule la quantité de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="c4d5d-149">Par exemple, Dynamics 365 peut contenir les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4d5d-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="c4d5d-150">**Nombre d’utilisateurs** : Le nombre d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c4d5d-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="c4d5d-151">**Nombre de mois** : Le nombre de mois d’abonnement</span><span class="sxs-lookup"><span data-stu-id="c4d5d-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="c4d5d-152">**SKU produit**</span><span class="sxs-lookup"><span data-stu-id="c4d5d-152">**Product SKU**</span></span> 

<span data-ttu-id="c4d5d-153">Les propriétés **Nombre d’utilisateurs** et **Nombre de mois** peuvent être marquées comme facteurs de quantité en modifiant les propriétés de la ligne de produit.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Marquage du Nombre d’utilisateurs et du Nombre de mois comme facteurs de qualité](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]