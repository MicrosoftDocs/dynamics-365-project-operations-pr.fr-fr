---
title: Recevoir les articles sur la commande achat depuis le besoin d’article
description: Cette rubrique explique comment recevoir des articles sur une commande achat à partir d’un besoin d’article.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011683"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="134ef-103">Recevoir les articles sur la commande achat depuis le besoin d’article</span><span class="sxs-lookup"><span data-stu-id="134ef-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="134ef-104">Cette rubrique explique comment recevoir des articles sur une commande achat à partir d’un besoin d’article.</span><span class="sxs-lookup"><span data-stu-id="134ef-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="134ef-105">En utilisant une demande d’article au lieu d’une transaction d’article, vous pouvez planifier la livraison juste avant que l’article ne soit réellement utilisé, créer une commande d’achat, inclure l’article dans le cadre de l’accord commercial et inclure l’exigence d’article dans la planification de la production.</span><span class="sxs-lookup"><span data-stu-id="134ef-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="134ef-106">Cette tâche utilise le jeu de données USSI.</span><span class="sxs-lookup"><span data-stu-id="134ef-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="134ef-107">Dans le volet de navigation, accédez à **Modules > Gestion de projet et comptabilité > Projets > Tous les projets**.</span><span class="sxs-lookup"><span data-stu-id="134ef-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="134ef-108">Dans la liste, sélectionnez le lien sur la ligne souhaitée.</span><span class="sxs-lookup"><span data-stu-id="134ef-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="134ef-109">Dans le volet Actions, sélectionnez **Planifier**.</span><span class="sxs-lookup"><span data-stu-id="134ef-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="134ef-110">Sélectionnez **Demandes d’article**.</span><span class="sxs-lookup"><span data-stu-id="134ef-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="134ef-111">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="134ef-111">Select **New**.</span></span>
6. <span data-ttu-id="134ef-112">Dans la nouvelle ligne, saisissez ou sélectionnez une valeur dans le champ **Numéro d’article**.</span><span class="sxs-lookup"><span data-stu-id="134ef-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="134ef-113">Dans le champ **Quantité**, tapez un nombre.</span><span class="sxs-lookup"><span data-stu-id="134ef-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="134ef-114">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="134ef-114">Select **Save**.</span></span>
9. <span data-ttu-id="134ef-115">Dans le volet Actions, sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="134ef-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="134ef-116">Sélectionnez **Fonctions**.</span><span class="sxs-lookup"><span data-stu-id="134ef-116">Select **Functions**.</span></span>
11. <span data-ttu-id="134ef-117">Sélectionnez **Créer une commande achat**.</span><span class="sxs-lookup"><span data-stu-id="134ef-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="134ef-118">Cochez la case **Tout inclure**.</span><span class="sxs-lookup"><span data-stu-id="134ef-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="134ef-119">Dans le champ **Compte fournisseur**, tapez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="134ef-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="134ef-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="134ef-120">Select **OK**.</span></span>
15. <span data-ttu-id="134ef-121">Dans le volet de navigation, accédez à **Modules > Comptabilité fournisseur > Commandes fournisseur > Toutes les commandes fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="134ef-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="134ef-122">Dans la liste, sélectionnez le lien sur la ligne souhaitée.</span><span class="sxs-lookup"><span data-stu-id="134ef-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="134ef-123">Dans le volet Actions, sélectionnez **Achat**.</span><span class="sxs-lookup"><span data-stu-id="134ef-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="134ef-124">Cliquez sur **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="134ef-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="134ef-125">Dans le volet Actions, sélectionnez **Recevoir**.</span><span class="sxs-lookup"><span data-stu-id="134ef-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="134ef-126">Sélectionnez **Accusé de réception de marchandises**.</span><span class="sxs-lookup"><span data-stu-id="134ef-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="134ef-127">Dans le champ **Accusé de réception de marchandises**, tapez une valeur.</span><span class="sxs-lookup"><span data-stu-id="134ef-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="134ef-128">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="134ef-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]