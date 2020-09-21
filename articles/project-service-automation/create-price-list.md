---
title: Créer un tarif
description: Procédure de création d'un tarif dans Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168142"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="c4fc6-103">Créer un tarif (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c4fc6-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c4fc6-104">Les tarifs fournissent un modèle que les directeurs de compte peuvent utiliser pour créer des devis et des projets, et pour fixer les coûts d'un projet.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="c4fc6-105">Ils fournissent une liste d'éléments de rôles et dépenses, et le prix que vous allez facturer pour chacun.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="c4fc6-106">Vous pouvez créer plusieurs tarifs afin de maintenir des structures de prix séparées pour chaque région où vous vendez vos produits dans ou sur différents canaux de vente.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="c4fc6-107">Il est préférable de créer au moins un tarif pour chaque devise dans laquelle vous envisagez de facturer vos clients.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="c4fc6-108">Pour créer des estimations financières pour le travail à fournir, assurez-vous que chaque projet a un coût de support et une liste de prix de vente.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="c4fc6-109">Configurez des coûts et tarifs de vente par défaut qui s'appliquent à tous les projets créés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="c4fc6-110">Les tarifs reposent sur les catégories de rôles et de dépenses donc, avant de créer des tarifs, vérifiez que vous avez déjà configuré les catégories de rôles et de dépenses à utiliser lors de la création des tarifs.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="c4fc6-111">Accédez à **Project Service > Tarifs**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="c4fc6-112">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="c4fc6-113">Dans **Contexte**, indiquez si ces tarifs sont pour **Coût**, **Achat** ou **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="c4fc6-114">Dans **Nom**, entrez un nom pour les tarifs.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="c4fc6-115">Dans **Devise**, sélectionnez la devise que vous comptez utiliser pour la facturation ou le prix.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="c4fc6-116">Dans **Unité de temps**, spécifiez la période à laquelle le prix s'applique, comme le jour ou l'heure.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="c4fc6-117">Complétez les champs **Date de début**, **Date de fin** et **Description** comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="c4fc6-118">Cliquez sur **Enregistrer** pour créer l’enregistrement et pouvoir continuer de le modifier.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="c4fc6-119">Pour ajouter un prix de rôle aux tarifs, cliquez sur **+** sous **Tarifs de rôle**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="c4fc6-120">Dans le volet **Prix du rôle**, remplissez les détails, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c4fc6-121">Continuez d'ajouter des prix de rôle selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="c4fc6-122">Lorsque vous avez fini, cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="c4fc6-123">Pour ajouter un prix de catégorie de dépense aux tarifs, cliquez sur **+** sous **Prix de catégorie**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="c4fc6-124">Dans le volet **Prix de la catégorie de transaction**, remplissez les détails, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c4fc6-125">Continuez d'ajouter des prix de catégorie selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="c4fc6-126">Lorsque vous avez fini, cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="c4fc6-127">Pour ajouter des éléments tarifaires aux tarifs, cliquez sur **+** sous **Éléments tarifaires**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="c4fc6-128">Dans le volet **Élément tarifaire**, remplissez les détails, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c4fc6-129">Continuez d'ajouter des éléments tarifaires selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="c4fc6-130">Lorsque vous avez fini, cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="c4fc6-131">Pour ajouter des relations de secteurs de vente au tarif, cliquez sur **+** sous **Relations de secteurs de vente**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="c4fc6-132">Dans le volet **Nouvelle connexion**, remplissez les détails, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c4fc6-133">Continuez d'ajouter des relations de secteurs de vente selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="c4fc6-134">Lorsque vous avez fini, cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c4fc6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4fc6-135">See Also</span></span>  
 [<span data-ttu-id="c4fc6-136">Configurer Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c4fc6-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
