---
title: Analyse des devis de projet
description: Cette rubrique fournit des informations sur l’analyse des devis de projet.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f3bff90f91e1df8bda495912a4aad0fa69342396
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592413"
---
# <a name="analysis-of-project-quotes"></a>Analyse des devis de projet

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyse des devis de projet pour estimer la rentabilité. Il analyse également à quel point le devis est aligné sur les exigences du client sur la date de livraison ou la date d’achèvement, puis sur les budgétisations.

## <a name="profitability-analysis"></a>Analyse de la rentabilité

Project Service Automation analyse la rentabilité à l’aide de la marge brute et de la marge brute ajustée.

- Les marges brutes sont comptabilisées à l’aide de la formule suivante :

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- La marge brute ajustée est comptabilisée à l’aide de la formule suivante :

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Si les valeurs de la marge brute et de la marge brute ajustée diffèrent d’une marge importante, une grande partie du travail dans le devis est classé comme non facturable.

## <a name="analysis-of-customer-expectations"></a>Analyse des exigences client

Vous pouvez analyser les devis et générer des graphiques pour les exigences client sur la planification et le budget si vous entrez des valeurs dans les champs suivants :

- Le champ **Date de livraison demandée** dans l’en-tête du devis.
- Le champ **Budget client** pour chaque ligne de devis (pour les lignes basées sur le projet et les lignes basées sur le produit).

L’analyse des exigences client sur la planification est effectuée en comparant la dernière date de fin de la ligne de détails du devis à la date de livraison demandée dans toutes les lignes de devis du devis.

L’analyse des exigences client sur le budget est effectuée en comparant la somme du budget total du client au montant du devis dans toutes les lignes de devis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
