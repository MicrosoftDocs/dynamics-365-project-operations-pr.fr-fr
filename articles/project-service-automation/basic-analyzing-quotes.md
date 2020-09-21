---
title: Analyse des devis de projet
description: Cette rubrique fournit des informations sur l'analyse des devis de projet.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167979"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="0dbf1-103">Analyse des devis de projet</span><span class="sxs-lookup"><span data-stu-id="0dbf1-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0dbf1-104">Dynamics 365 Project Service Automation analyse des devis de projet pour estimer la rentabilité.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="0dbf1-105">Il analyse également à quel point le devis est aligné sur les exigences du client sur la date de livraison ou la date d'achèvement, puis sur les budgétisations.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="0dbf1-106">Analyse de la rentabilité</span><span class="sxs-lookup"><span data-stu-id="0dbf1-106">Profitability analysis</span></span>

<span data-ttu-id="0dbf1-107">Project Service Automation analyse la rentabilité à l'aide de la marge brute et de la marge brute ajustée.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="0dbf1-108">Les marges brutes sont comptabilisées à l'aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="0dbf1-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="0dbf1-109">La marge brute ajustée est comptabilisée à l'aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="0dbf1-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="0dbf1-110">Si les valeurs de la marge brute et de la marge brute ajustée diffèrent d'une marge importante, une grande partie du travail dans le devis est classé comme non facturable.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="0dbf1-111">Analyse des exigences client</span><span class="sxs-lookup"><span data-stu-id="0dbf1-111">Analysis of customer expectations</span></span>

<span data-ttu-id="0dbf1-112">Vous pouvez analyser les devis et générer des graphiques pour les exigences client sur la planification et le budget si vous entrez des valeurs dans les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="0dbf1-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="0dbf1-113">Le champ **Date de livraison demandée** dans l'en-tête du devis.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="0dbf1-114">Le champ **Budget client** pour chaque ligne de devis (pour les lignes basées sur le projet et les lignes basées sur le produit).</span><span class="sxs-lookup"><span data-stu-id="0dbf1-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="0dbf1-115">L'analyse des exigences client sur la planification est effectuée en comparant la dernière date de fin de la ligne de détails du devis à la date de livraison demandée dans toutes les lignes de devis du devis.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="0dbf1-116">L'analyse des exigences client sur le budget est effectuée en comparant la somme du budget total du client au montant du devis dans toutes les lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="0dbf1-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
