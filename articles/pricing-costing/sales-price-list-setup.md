---
title: Configuration des tarifs de vente
description: Cette rubrique fournit des informations sur les tarifs de ventes associés pour la tarification de projet.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075795"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="a63aa-103">Configuration des tarifs de vente</span><span class="sxs-lookup"><span data-stu-id="a63aa-103">Sales price list setup</span></span>

<span data-ttu-id="a63aa-104">_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="a63aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a63aa-105">Pour les devis et les contrats du projet, les tarifs du projet ont un autre modèle de remplacement de prix qu'une liste de prix de produits.</span><span class="sxs-lookup"><span data-stu-id="a63aa-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="a63aa-106">Dans une ligne de devis basée sur un catalogue de produits, vous pouvez remplacer le prix des rôles et des catégories directement sur la ligne de devis, car chaque ligne de devis pointe exactement vers un article du catalogue.</span><span class="sxs-lookup"><span data-stu-id="a63aa-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="a63aa-107">Toutefois, sur une ligne de devis basée sur un projet, vous ne pouvez pas remplacer le tarif des rôles et des catégories directement sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="a63aa-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="a63aa-108">Vous pouvez utiliser le tarif du projet pour prendre en charge les deux modèles de remplacement distincts.</span><span class="sxs-lookup"><span data-stu-id="a63aa-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="a63aa-109">Il est recommandé d'avoir des tarifs distincts pour vos ressources de projet et vos articles de catalogue, en raison des différences de comportement entre les deux lors du remplacement de la tarification.</span><span class="sxs-lookup"><span data-stu-id="a63aa-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="a63aa-110">Chacune des entités suivantes peut contenir un ou plusieurs tarifs de ventes associés pour la tarification de projet :</span><span class="sxs-lookup"><span data-stu-id="a63aa-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="a63aa-111">Client (compte)</span><span class="sxs-lookup"><span data-stu-id="a63aa-111">Customer (account)</span></span> 
- <span data-ttu-id="a63aa-112">Opportunité</span><span class="sxs-lookup"><span data-stu-id="a63aa-112">Opportunity</span></span> 
- <span data-ttu-id="a63aa-113">Devis</span><span class="sxs-lookup"><span data-stu-id="a63aa-113">Quote</span></span> 
- <span data-ttu-id="a63aa-114">Contrat du projet</span><span class="sxs-lookup"><span data-stu-id="a63aa-114">Project Contract</span></span>

<span data-ttu-id="a63aa-115">L'association de ces entités avec des tarifs est indiquée par les tarifs du projet.</span><span class="sxs-lookup"><span data-stu-id="a63aa-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="a63aa-116">Vous pouvez associer un ou plusieurs tarifs avec les entités de vente Client, Opportunité, Devis et Contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="a63aa-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="a63aa-117">Des tarifs par défaut de projet ne sont pas automatiquement entrés sur un enregistrement client.</span><span class="sxs-lookup"><span data-stu-id="a63aa-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="a63aa-118">Cependant, vous pouvez manuellement joindre des tarifs de projet à l'enregistrement de client.</span><span class="sxs-lookup"><span data-stu-id="a63aa-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="a63aa-119">Toutefois, vous devez manuellement joindre des tarifs de projet uniquement si vous avez un contrat de tarification personnalisé avec le client.</span><span class="sxs-lookup"><span data-stu-id="a63aa-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="a63aa-120">Lorsque des tarifs de projet sont attachés à une entité de ventes, les informations suivantes sont validées :</span><span class="sxs-lookup"><span data-stu-id="a63aa-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="a63aa-121">Le tarif a un contexte de **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="a63aa-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="a63aa-122">La devise des tarifs correspond à la devise client.</span><span class="sxs-lookup"><span data-stu-id="a63aa-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="a63aa-123">Sur un contrat de projet, l'ordre suivant de priorité est utilisé pour définir automatiquement les tarifs associés de projet :</span><span class="sxs-lookup"><span data-stu-id="a63aa-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="a63aa-124">Devis</span><span class="sxs-lookup"><span data-stu-id="a63aa-124">Quote</span></span>
2. <span data-ttu-id="a63aa-125">Opportunité</span><span class="sxs-lookup"><span data-stu-id="a63aa-125">Opportunity</span></span>
3. <span data-ttu-id="a63aa-126">Client</span><span class="sxs-lookup"><span data-stu-id="a63aa-126">Customer</span></span> 
4. <span data-ttu-id="a63aa-127">Paramètres globaux</span><span class="sxs-lookup"><span data-stu-id="a63aa-127">Global settings</span></span> 

<span data-ttu-id="a63aa-128">Lorsque des tarifs de projet sont entrés par défaut, le système valide le fait que la devise corresponde à la devise client, et que les tarifs par défaut entrés ont un contexte de **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="a63aa-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="a63aa-129">Vous pouvez associer plusieurs tarifs de projet aux entités Client, Opportunité, Devis et Contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="a63aa-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="a63aa-130">Cette fonctionnalité prend en charge les prix par défaut spécifiques à une date dans un contrat de projet à long terme, où vous pouvez nécessiter plusieurs tarifs pour tenir compte des mises à jour des prix qui se produisent en raison de l'inflation.</span><span class="sxs-lookup"><span data-stu-id="a63aa-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="a63aa-131">Toutefois, si les tarifs que vous associez à l'entité Client, Opportunité, Devis ou Contrat du projet ont une validité de date se chevauchant, les prix par défaut peuvent être incorrects.</span><span class="sxs-lookup"><span data-stu-id="a63aa-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="a63aa-132">Par conséquent, vous devez vous assurer que les tarifs de projet qui ont une validité de dates se chevauchant ne sont pas associés à ces entités.</span><span class="sxs-lookup"><span data-stu-id="a63aa-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
