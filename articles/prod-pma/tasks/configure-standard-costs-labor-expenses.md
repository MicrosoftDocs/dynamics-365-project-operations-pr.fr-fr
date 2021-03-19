---
title: Configurer les coûts standard pour la main-d’œuvre et les dépenses
description: Cette rubrique explique comment configurer les coûts standard de la main-d’œuvre et les dépenses pour un projet.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288331"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6d8f0-103">Configurer les coûts standard pour la main-d’œuvre et les dépenses</span><span class="sxs-lookup"><span data-stu-id="6d8f0-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d8f0-104">Cette rubrique explique comment configurer les coûts standard de la main-d’œuvre et les dépenses pour un projet.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6d8f0-105">Cette tâche utilise le jeu de données USSI.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6d8f0-106">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de revient (heure)**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="6d8f0-107">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-107">Select **New**.</span></span>
3. <span data-ttu-id="6d8f0-108">Dans le champ **Date effective**, saisissez une date.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="6d8f0-109">Dans le champ **Prix de revient**, saisissez un numéro.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6d8f0-110">Vous pouvez définir un prix de revient standard pour la catégorie de projet, ou vous pouvez définir un prix de revient par numéro d’employé, numéro de projet, catégorie, date ou toute combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6d8f0-111">Le prix de revient appliqué correspond au prix de revient avec le plus haut niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6d8f0-112">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-112">Select **Save**.</span></span>
6. <span data-ttu-id="6d8f0-113">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de vente (heure)**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="6d8f0-114">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-114">Select **New**.</span></span>
8. <span data-ttu-id="6d8f0-115">Dans le champ **Date effective**, saisissez une date.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="6d8f0-116">Dans le champ **Valide pour**, sélectionnez une option.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="6d8f0-117">Dans le champ **Tarification**, saisissez un nombre.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6d8f0-118">Vous pouvez configurer un prix de vente standard pour les transactions horaires ou pour une catégorie de projet.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6d8f0-119">Vous pouvez également configurer les prix de vente par numéro d’employé, numéro de projet, catégorie, date de transaction ou toute combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6d8f0-120">Le prix de vente réel, qui est appliqué lorsqu’un employé entre une transaction dans le journal des heures, correspond au prix de vente avec le niveau de détail le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6d8f0-121">Par exemple, si un prix de vente général et un prix de vente spécifique à l’employé sont définis, le prix de vente spécifique à l’employé est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="6d8f0-122">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-122">Select **Save**.</span></span>
12. <span data-ttu-id="6d8f0-123">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-123">Close the page.</span></span>
13. <span data-ttu-id="6d8f0-124">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de revient (dépense)**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="6d8f0-125">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-125">Select **New**.</span></span>
15. <span data-ttu-id="6d8f0-126">Dans le champ **Date effective**, saisissez une date.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="6d8f0-127">Dans le champ **Prix de revient**, saisissez un numéro.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6d8f0-128">Plusieurs champs peuvent être remplis, mais il s’agit là des champs minimum nécessaires pour enregistrer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="6d8f0-129">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-129">Select **Save**.</span></span>
18. <span data-ttu-id="6d8f0-130">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de vente (dépense)**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="6d8f0-131">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-131">Select **New**.</span></span>
20. <span data-ttu-id="6d8f0-132">Dans le champ **Date effective**, saisissez une date.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="6d8f0-133">Dans le champ **Valide pour**, sélectionnez une option.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="6d8f0-134">Dans le champ **Tarification**, saisissez un nombre.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6d8f0-135">Le prix de vente réel, qui est appliqué lorsqu’un employé saisit des transactions dans le journal des dépenses, correspond au prix de vente avec le niveau de détail le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6d8f0-136">Par exemple, si un prix de vente général et un prix de vente spécifique à l’employé sont définis, le prix de vente spécifique à l’employé est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="6d8f0-137">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6d8f0-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]