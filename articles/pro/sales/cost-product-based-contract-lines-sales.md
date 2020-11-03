---
title: Lignes de contrat selon les produits pour évaluation des coûts
description: Cette rubrique fournit des informations sur la création
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075971"
---
# <a name="costing-product-based-contract-lines"></a>Lignes de contrat selon les produits pour évaluation des coûts

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Les lignes de contrat basées sur les produits dans Dynamics 365 Project Operations incluent le champ **Prix de revient** , qui stocke le prix de revient du produit pour les calculs de rentabilité en aval.

Lorsqu'une ligne de contrat basée sur un produit est créée pour un produit du catalogue, le coût de la ligne de contrat basée sur le produit est par défaut celui du champ **Coût standard** dans le catalogue de produits. Le champ **Coût standard** dans le catalogue de produits est configuré dans la devise de base de l’organisation. Lorsque le coût unitaire est par défaut sur la ligne du contrat, il est converti dans la devise de vente du contrat.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Coût unitaire sur une ligne du contrat selon les produits

Avoir un coût unitaire sur une ligne de contrat basée sur un produit permet des coûts différents pour un produit pour chaque vente. Bien que cela ne soit pas toujours nécessaire, il existe certains scénarios dans lesquels le coût du produit peut être réduit pour le client par le fournisseur. Prenons l'exemple du scénario suivant :

Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d'Adatum Corporation. Fabrikam fournit des services d'installation mais les bras robotiques sont fournis par Trey Research. Si l'installation de bras robotiques chez Adatum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey Research, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam. Dans ce cas, Fabrikam crée une ligne de contrat basée sur les produits pour Robotic Arms et saisit un coût unitaire pour ce contrat qui est différent du coût standard des bras robotiques de Trey Research.
