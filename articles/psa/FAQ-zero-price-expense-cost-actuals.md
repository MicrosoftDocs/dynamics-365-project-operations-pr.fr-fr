---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des dépenses ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels de coût des dépenses.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122115"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="7067a-103">Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des dépenses ?</span><span class="sxs-lookup"><span data-stu-id="7067a-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7067a-104">Cette FAQ s’applique aux chiffres réels des dépenses où la classe de transaction est définie sur Dépenses et le type de transaction est Coût.</span><span class="sxs-lookup"><span data-stu-id="7067a-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="7067a-105">Dépannage des taux de coûts sur les chiffres réels du coût des dépenses</span><span class="sxs-lookup"><span data-stu-id="7067a-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="7067a-106">Accédez à l’entrée de dépense associée et vérifiez qu’il existe un montant dans le champ d’entrée de dépenses.</span><span class="sxs-lookup"><span data-stu-id="7067a-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="7067a-107">Si l’entrée de dépenses d’origine n’a pas le champ de montant rempli, cela signifie que vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="7067a-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="7067a-108">Pour résoudre ce problème, recréez l’entrée de dépenses par un montant valide et approuvez-le.</span><span class="sxs-lookup"><span data-stu-id="7067a-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
