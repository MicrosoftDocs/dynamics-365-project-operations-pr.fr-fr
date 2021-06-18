---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des dépenses ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels de coût des dépenses.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992783"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="5a9a6-103">Pourquoi le tarif prend-il la valeur par défaut de zéro sur les chiffres réels de coût des dépenses</span><span class="sxs-lookup"><span data-stu-id="5a9a6-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5a9a6-104">Cette FAQ s’applique aux chiffres réels des dépenses où la classe de transaction est définie sur Dépenses et le type de transaction est Coût.</span><span class="sxs-lookup"><span data-stu-id="5a9a6-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="5a9a6-105">Dépannage des taux de coûts sur les chiffres réels du coût des dépenses</span><span class="sxs-lookup"><span data-stu-id="5a9a6-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="5a9a6-106">Accédez à l’entrée de dépense associée et vérifiez qu’il existe un montant dans le champ d’entrée de dépenses.</span><span class="sxs-lookup"><span data-stu-id="5a9a6-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="5a9a6-107">Si l’entrée de dépenses d’origine n’a pas le champ de montant rempli, cela signifie que vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="5a9a6-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="5a9a6-108">Pour résoudre ce problème, recréez l’entrée de dépenses par un montant valide et approuvez-le.</span><span class="sxs-lookup"><span data-stu-id="5a9a6-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]