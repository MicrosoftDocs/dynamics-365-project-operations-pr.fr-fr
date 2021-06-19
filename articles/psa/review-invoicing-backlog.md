---
title: Réviser l’arriéré de facturation sur les projets et les contrats de projet
description: Cette rubrique explique comment vérifier les arriérés de temps, de dépenses, et de produits, et comment les marquer comme prêts pour la facturation.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008533"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="7197e-103">Réviser l’arriéré de facturation sur les projets et les contrats de projet</span><span class="sxs-lookup"><span data-stu-id="7197e-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7197e-104">Lorsqu’une transaction est prête pour qu’une facture soit créée et traitée, la transaction doit être marquée comme **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="7197e-105">Cette rubrique décrit les types de transactions qui peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="7197e-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="7197e-106">Réviser les arriérés de facturation du temps et des matériaux</span><span class="sxs-lookup"><span data-stu-id="7197e-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="7197e-107">Lorsqu’une entrée de temps ou de dépenses est envoyée et approuvée pour un projet, PSA crée un chiffre réel de projet.</span><span class="sxs-lookup"><span data-stu-id="7197e-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="7197e-108">Si la combinaison du projet et de la classe de transaction sont mappés à une ligne de contrat pour le projet temps et matériaux, deux chiffres réels sont créés lorsque l’entrée est approuvée :</span><span class="sxs-lookup"><span data-stu-id="7197e-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="7197e-109">Coût réel</span><span class="sxs-lookup"><span data-stu-id="7197e-109">Cost actual</span></span> 
- <span data-ttu-id="7197e-110">Chiffre réel de ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="7197e-110">Unbilled sales actual</span></span>

<span data-ttu-id="7197e-111">Les chiffres réels de ventes non facturées représentent l’arriéré de facturation, et leur statut de facturation doit être défini sur **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="7197e-112">Lorsqu’une facture de projet est créée, les chiffres réels de ventes non facturées marqués comme **Prêt pour la facturation** sont copiés comme des détails de ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="7197e-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="7197e-113">Pour vérifier les arriérés de facturation pour le temps et les matériaux, accédez à **Ventes** \> **Facturation** \> **Arriéré de facturation de temps et de matériaux**.</span><span class="sxs-lookup"><span data-stu-id="7197e-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="7197e-114">Sélectionnez tous les chiffres réels de ventes non facturés prêts à être facturés, puis sélectionnez **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="7197e-115">Le statut de facturation de ces chiffres réels passe à **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Arriérés de facturation pour le temps et le matériel](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="7197e-117">Vérifier l’arriéré de facturation pour les produits</span><span class="sxs-lookup"><span data-stu-id="7197e-117">Review the product billing backlog</span></span>

<span data-ttu-id="7197e-118">Dans PSA, lorsqu’un contrat de projet contient des lignes de contrat basées sur les produits, ces lignes sont considérées pour la facturation chaque fois qu’une facture est créée pour le contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="7197e-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="7197e-119">Tout produit qui possède des lignes de contrat marquées comme **Prêt pour la facturation** est copié sur une facture de projet sous forme de lignes de facture de projet.</span><span class="sxs-lookup"><span data-stu-id="7197e-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="7197e-120">Pour vérifier les arriérés de facturation pour les produits, accédez à **Ventes** \> **Facturation** \> **Arriéré de facturation de produit**.</span><span class="sxs-lookup"><span data-stu-id="7197e-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="7197e-121">Sélectionnez toutes les lignes de contrat basées sur des produits prêtes à être facturées, puis sélectionnez **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="7197e-122">Le statut de facturation de ces lignes passe à **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Arriéré de facturation pour les produits](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="7197e-124">Vérifiez les jalons de facturation sur les contrats à prix fixe</span><span class="sxs-lookup"><span data-stu-id="7197e-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="7197e-125">Chaque ligne de contrat de projet avec une méthode de facturation à prix fixe doit définir des jalons de contrat.</span><span class="sxs-lookup"><span data-stu-id="7197e-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="7197e-126">Ces jalons de contrat peuvent être facturés uniquement s’ils sont marqués comme **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="7197e-127">Pour vérifier les jalons de facturation, accédez à **Ventes** \> **Facturation** \> **Jalons de forfait**.</span><span class="sxs-lookup"><span data-stu-id="7197e-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="7197e-128">Sélectionnez les jalons prêts à être facturés, puis sélectionnez **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="7197e-129">Le statut de facturation de ces jalons passe à **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="7197e-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Jalons à prix fixe](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]