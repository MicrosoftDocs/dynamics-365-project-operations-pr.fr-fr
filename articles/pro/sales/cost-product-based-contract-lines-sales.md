---
title: Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié
description: Cette rubrique fournit des informations sur la création
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599267"
---
# <a name="cost-product-based-contract-lines---lite"></a>Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Les lignes de contrat basées sur les produits dans Dynamics 365 Project Operations incluent le champ **Prix de revient**, qui stocke le prix de revient du produit pour les calculs de rentabilité en aval.

Lorsqu’une ligne de contrat basée sur un produit est créée pour un produit de catalogue, le coût de la ligne est par défaut du champ **Coût standard** dans le catalogue de produits. Le champ **Coût standard** dans le catalogue de produits est configuré dans la devise de base de l’organisation. Lorsque le coût unitaire est par défaut sur la ligne du contrat, il est converti dans la devise de vente du contrat.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Coût unitaire sur une ligne du contrat selon les produits

Avoir un coût unitaire sur une ligne de contrat basée sur un produit permet des coûts différents pour un produit pour chaque vente. Bien que cela ne soit pas toujours nécessaire, il existe certains scénarios dans lesquels le coût du produit peut être réduit pour le client par le fournisseur. Prenons l’exemple du scénario suivant :

Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d’Adatum Corporation. Fabrikam fournit des services d’installation mais les bras robotiques sont de Trey Research. Si l’installation de bras robotiques chez Adatum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey Research, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam. Dans ce cas, Fabrikam crée une ligne de contrat basée sur les produits pour Robotic Arms. Un coût unitaire est inscrit pour ce contrat. Le coût est différent du coût des bras robotiques de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]