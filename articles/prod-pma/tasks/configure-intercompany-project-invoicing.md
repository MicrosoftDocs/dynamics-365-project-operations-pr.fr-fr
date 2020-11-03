---
title: Configurer la facturation des projets intersociétés
description: Cette rubrique présente comment configurer la facturation des projets entre deux sociétés au sein de votre organisation.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075799"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="7399a-103">Configurer la facturation des projets intersociétés</span><span class="sxs-lookup"><span data-stu-id="7399a-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7399a-104">Cette rubrique présente comment configurer la facturation des projets entre deux sociétés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7399a-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="7399a-105">Cette tâche utilise le jeu de données USSI.</span><span class="sxs-lookup"><span data-stu-id="7399a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="7399a-106">Dans le volet de navigation, accédez à **Modules > Comptabilité fournisseur > Fournisseurs > Tous les fournisseurs**.</span><span class="sxs-lookup"><span data-stu-id="7399a-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="7399a-107">Dans la liste **Tous les fournisseurs** , recherchez et sélectionnez l’enregistrement souhaité.</span><span class="sxs-lookup"><span data-stu-id="7399a-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="7399a-108">Cliquez sur **Général** dans le volet Actions.</span><span class="sxs-lookup"><span data-stu-id="7399a-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="7399a-109">Sélectionnez **Intersociétés**.</span><span class="sxs-lookup"><span data-stu-id="7399a-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="7399a-110">Définissez **Actif** sur **Oui** pour activer les échanges intersociétés.</span><span class="sxs-lookup"><span data-stu-id="7399a-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="7399a-111">Dans le champ **Société du client** , tapez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="7399a-112">Dans le champ **Mon compte** , tapez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="7399a-113">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7399a-113">Select **Save**.</span></span>
9. <span data-ttu-id="7399a-114">Fermez les pages pour revenir à la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="7399a-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="7399a-115">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Paramètres de gestion de projets et de comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="7399a-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="7399a-116">Cliquez sur l’onglet **Intersociétés**.</span><span class="sxs-lookup"><span data-stu-id="7399a-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="7399a-117">Déplacez le curseur vers **Oui** pour activer la planification des ressources et les feuilles de temps intersociétés.</span><span class="sxs-lookup"><span data-stu-id="7399a-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="7399a-118">Dans la liste, marquez la ligne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7399a-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="7399a-119">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7399a-119">Select **New**.</span></span>
15. <span data-ttu-id="7399a-120">Dans le champ **Entité juridique emprunteuse** , saisissez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="7399a-121">Cochez la case **Provisionner le produit**.</span><span class="sxs-lookup"><span data-stu-id="7399a-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="7399a-122">Dans le champ **Catégorie de feuille de temps par défaut** , saisissez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="7399a-123">Dans le champ **Catégorie de dépense par défaut** , saisissez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="7399a-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7399a-124">Select **Save**.</span></span>
20. <span data-ttu-id="7399a-125">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="7399a-125">Close the page.</span></span>
21. <span data-ttu-id="7399a-126">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Validation > Paramétrage de la validation dans la comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="7399a-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="7399a-127">Dans le champ **Types de compte** , sélectionnez une option.</span><span class="sxs-lookup"><span data-stu-id="7399a-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="7399a-128">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7399a-128">Select **New**.</span></span>
24. <span data-ttu-id="7399a-129">Dans le champ **Compte principal** de la nouvelle ligne, spécifiez les valeurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="7399a-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="7399a-130">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7399a-130">Select **Save**.</span></span>
26. <span data-ttu-id="7399a-131">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="7399a-131">Close the page.</span></span>
27. <span data-ttu-id="7399a-132">Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de transfert**.</span><span class="sxs-lookup"><span data-stu-id="7399a-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="7399a-133">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7399a-133">Select **New**.</span></span>
29. <span data-ttu-id="7399a-134">Dans le champ **Date effective** , saisissez une date.</span><span class="sxs-lookup"><span data-stu-id="7399a-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="7399a-135">Dans le champ **Entité juridique emprunteuse** , saisissez ou sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="7399a-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="7399a-136">Dans le champ **Modèle de prix de transfert** , sélectionnez une option.</span><span class="sxs-lookup"><span data-stu-id="7399a-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="7399a-137">Dans le champ **Tarification** , saisissez un nombre.</span><span class="sxs-lookup"><span data-stu-id="7399a-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="7399a-138">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7399a-138">Select **Save**.</span></span>

