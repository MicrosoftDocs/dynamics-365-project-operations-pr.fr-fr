---
title: Commandes fournisseur pour un projet
description: Cet article décrit les différentes méthodes que vous pouvez utiliser pour créer des commandes fournisseur pour un projet. La méthode que vous utilisez dépend de l’objectif de la commande fournisseur et quand les articles achetés sont consommés et, par conséquent, facturés sur un projet.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168035"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="56071-104">Commandes fournisseur pour un projet</span><span class="sxs-lookup"><span data-stu-id="56071-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56071-105">Cet article décrit les différentes méthodes que vous pouvez utiliser pour créer des commandes fournisseur pour un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="56071-106">La méthode que vous utilisez dépend de l’objectif de la commande fournisseur et quand les articles achetés sont consommés et, par conséquent, facturés sur un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="56071-107">Méthodes de création d’une commande fournisseur</span><span class="sxs-lookup"><span data-stu-id="56071-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="56071-108">Vous pouvez utiliser l’une des méthodes suivantes pour créer une commande fournisseur dans Gestion de projet et comptabilité.</span><span class="sxs-lookup"><span data-stu-id="56071-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="56071-109">Le but de la commande fournisseur détermine quand la commande fournisseur est consommée et, par conséquent, quand les articles sont facturés vers un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56071-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="56071-110">Method</span></span></th>
<th><span data-ttu-id="56071-111">Objectif</span><span class="sxs-lookup"><span data-stu-id="56071-111">Purpose</span></span></th>
<th><span data-ttu-id="56071-112">Consommation d’articles</span><span class="sxs-lookup"><span data-stu-id="56071-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56071-113">Créez une commande fournisseur directement à partir d’un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="56071-114">Utilisez cette méthode pour acheter des articles auprès d’un fournisseur externe pour les consommer sur un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="56071-115">Vous pouvez créer la commande fournisseur de l’une des deux méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="56071-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="56071-116">À partir du projet lui-même.</span><span class="sxs-lookup"><span data-stu-id="56071-116">From the project itself.</span></span> <span data-ttu-id="56071-117">Dans ce cas, le projet est déjà défini pour la commande fournisseur.</span><span class="sxs-lookup"><span data-stu-id="56071-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="56071-118">En accédant à la commande fournisseur du projet.</span><span class="sxs-lookup"><span data-stu-id="56071-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="56071-119">Vous devez sélectionner à la fois le fournisseur et le projet pour lesquels créer la commande fournisseur.</span><span class="sxs-lookup"><span data-stu-id="56071-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="56071-120">Les articles sont consommés lors de la mise à jour de la facture fournisseur.</span><span class="sxs-lookup"><span data-stu-id="56071-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56071-121">Créer une commande achat à partir d'une commande client.</span><span class="sxs-lookup"><span data-stu-id="56071-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="56071-122">Utilisez cette méthode pour acheter des articles lorsque vous créez une commande client à partir d’un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="56071-123">Les articles sont consommés lorsque la commande client est facturée au client.</span><span class="sxs-lookup"><span data-stu-id="56071-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56071-124">Créez une commande fournisseur à partir d’une exigence d’article.</span><span class="sxs-lookup"><span data-stu-id="56071-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="56071-125">Utilisez cette méthode pour acheter des articles lorsque vous créez une exigence d’article à partir d’un projet.</span><span class="sxs-lookup"><span data-stu-id="56071-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="56071-126">Les articles sont consommés lorsque le bon de livraison de l’exigence d’article est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="56071-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="56071-127">Lorsque vous mettez à jour la facture fournisseur ou le bon de livraison, vous êtes invité à mettre à jour le bon de livraison sur l’exigence de l’article.</span><span class="sxs-lookup"><span data-stu-id="56071-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="56071-128">Pour plus d’informations, consultez [Recevoir les articles sur la commande fournisseur depuis l’exigence d’article](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="56071-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

