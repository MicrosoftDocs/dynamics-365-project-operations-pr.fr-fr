---
title: Créer des devis de projet à partir d’opportunités
description: Cette rubrique fournit des informations sur la création d’un devis de projet à partir d’une opportunité.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898529"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="97d5a-103">Créer des devis de projet à partir d’opportunités</span><span class="sxs-lookup"><span data-stu-id="97d5a-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="97d5a-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="97d5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="97d5a-105">Les devis peuvent être créés à partir d’opportunités de projet des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="97d5a-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="97d5a-106">À partir de l’onglet **Devis** sur la page **Opportunité de projet**</span><span class="sxs-lookup"><span data-stu-id="97d5a-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="97d5a-107">À partir du flux des processus de vente Opportunité</span><span class="sxs-lookup"><span data-stu-id="97d5a-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="97d5a-108">En mettant à jour la référence d’opportunité sur un devis existant</span><span class="sxs-lookup"><span data-stu-id="97d5a-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="97d5a-109">À partir de l’onglet Devis de la page Opportunité de projet</span><span class="sxs-lookup"><span data-stu-id="97d5a-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="97d5a-110">Pour créer un devis de projet à partir d’une opportunité, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="97d5a-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="97d5a-111">Ouvrez la page **Opportunité de projet** et sélectionnez l’onglet **Devis**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="97d5a-112">Sur la sous-grille **Devis**, sélectionnez le **+** pour créer un devis de projet en fonction de l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="97d5a-113">Toutes les lignes d’opportunité et les tarifs de projet associés sont copiés dans le nouveau devis à partir de l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="97d5a-114">À partir du flux des processus de vente Opportunité</span><span class="sxs-lookup"><span data-stu-id="97d5a-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="97d5a-115">Pour créer un devis de projet à partir du flux des processus de vente Opportunité, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="97d5a-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="97d5a-116">Dans le flux des processus de vente Opportunité, ouvrez l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="97d5a-117">Sélectionnez la phase **Qualifier**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="97d5a-118">Sélectionnez **Suivant**, puis **+ Créer** pour créer un devis.</span><span class="sxs-lookup"><span data-stu-id="97d5a-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="97d5a-119">La plupart des informations sur l’onglet **Résumé** pour ce nouveau devis seront par défaut à partir de l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="97d5a-120">Entrez les informations requises manquantes ou mettez à jour les valeurs par défaut si nécessaire sur l’onglet **Résumé**,</span><span class="sxs-lookup"><span data-stu-id="97d5a-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="97d5a-121">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-121">Select **Save**.</span></span> <span data-ttu-id="97d5a-122">Le devis est créé et associé à l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="97d5a-123">Vous pouvez maintenant afficher les informations de devis sur l’onglet **Devis** de la page **Opportunité**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="97d5a-124">Le processus de vente d’opportunité passe à l’étape suivante, **Proposer**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="97d5a-125">En mettant à jour la référence d’opportunité sur un devis existant</span><span class="sxs-lookup"><span data-stu-id="97d5a-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="97d5a-126">Un devis existant peut être lié à une opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="97d5a-127">Effectuez les étapes suivantes pour mettre à jour les informations d’opportunité sur un devis existant.</span><span class="sxs-lookup"><span data-stu-id="97d5a-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="97d5a-128">Ouvrez la page **Devis** et sélectionnez l’onglet **Résumé**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="97d5a-129">Dans le champ **Opportunité**, sélectionnez l’opportunité que vous souhaitez lier au devis.</span><span class="sxs-lookup"><span data-stu-id="97d5a-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="97d5a-130">Vous pouvez voir le devis dans la grille **Devis** de l’opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="97d5a-131">À l’aide du processus de vente Opportunité, l’opportunité peut être déplacée vers l’étape suivante, **Proposer**.</span><span class="sxs-lookup"><span data-stu-id="97d5a-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="97d5a-132">Lorsque vous déplacez une opportunité vers cette phase, vous pouvez sélectionner ce devis dans une liste de devis associés à cette opportunité.</span><span class="sxs-lookup"><span data-stu-id="97d5a-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="97d5a-133">La sélection de ce devis indique que vous poursuivez.</span><span class="sxs-lookup"><span data-stu-id="97d5a-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="97d5a-134">Tous les autres devis associés à l’opportunité seront toujours disponibles et actifs jusqu’à ce que l’un d’eux soit remporté.</span><span class="sxs-lookup"><span data-stu-id="97d5a-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="97d5a-135">Vous pouvez ramener le processus de vente à la phase précédente **Qualifier**, et choisir un autre devis pour avancer.</span><span class="sxs-lookup"><span data-stu-id="97d5a-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
