---
title: Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié
description: Cette rubrique fournit des informations sur la création
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997333"
---
# <a name="cost-product-based-contract-lines---lite"></a>Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Les lignes de contrat basées sur les produits dans Dynamics 365 Project Operations incluent le champ **Prix de revient**, qui stocke le prix de revient du produit pour les calculs de rentabilité en aval.

Lorsqu’une ligne de contrat basée sur un produit est créée pour un produit de catalogue, le coût de la ligne est par défaut du champ **Coût standard** dans le catalogue de produits. Le champ **Coût standard** dans le catalogue de produits est configuré dans la devise de base de l’organisation. Lorsque le coût unitaire est par défaut sur la ligne du contrat, il est converti dans la devise de vente du contrat.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Coût unitaire sur une ligne du contrat selon les produits

Avoir un coût unitaire sur une ligne de contrat basée sur un produit permet des coûts différents pour un produit pour chaque vente. Bien que cela ne soit pas toujours nécessaire, il existe certains scénarios dans lesquels le coût du produit peut être réduit pour le client par le fournisseur. Prenons l’exemple du scénario suivant :

Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d’Adatum Corporation. Fabrikam fournit des services d’installation mais les bras robotiques sont de Trey Research. Si l’installation de bras robotiques chez Adatum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey Research, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam. Dans ce cas, Fabrikam crée une ligne de contrat basée sur les produits pour Robotic Arms. Un coût unitaire est inscrit pour ce contrat. Le coût est différent du coût des bras robotiques de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]