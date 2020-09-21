---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des dépenses ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels de coût des dépenses.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168040"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des dépenses ?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cette FAQ s'applique aux chiffres réels des dépenses où la classe de transaction est définie sur Dépenses et le type de transaction est Coût.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Dépannage des taux de coûts sur les chiffres réels du coût des dépenses

Accédez à l'entrée de dépense associée et vérifiez qu'il existe un montant dans le champ d'entrée de dépenses. Si l'entrée de dépenses d'origine n'a pas le champ de montant rempli, cela signifie que vous avez isolé le problème.
 
Pour résoudre ce problème, recréez l'entrée de dépenses par un montant valide et approuvez-le.
