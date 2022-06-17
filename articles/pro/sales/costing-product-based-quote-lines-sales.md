---
title: Lignes du devis selon les produits pour l’évaluation des coûts
description: Cet article fournit des informations sur l’application d’un prix de revient à une ligne de devis basée sur un produit.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932569"
---
# <a name="costing-product-based-quote-lines"></a>Lignes du devis selon les produits pour l’évaluation des coûts

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Les lignes de devis basées sur les produits dans Dynamics 365 Project Operations ont aussi un champ **Prix de revient**. Ce champ est utilisé pour suivre le prix de revient du produit sur la ligne de devis et pour les calculs de rentabilité en aval.

Lorsqu’une ligne de devis basée sur un produit est créée pour un produit du catalogue, le coût de la ligne de devis basée sur le produit est par défaut celui du champ **Coût standard** dans le catalogue de produits. Le champ de coût standard dans le catalogue de produits est configuré dans la devise de base de l’organisation. Le coût unitaire par défaut de la ligne de devis basée sur le produit est converti dans la devise de vente du devis.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Coût unitaire sur une ligne du devis selon les produits

Le but d’avoir un coût unitaire sur une ligne de devis basée sur un produit est de permettre des coûts différents pour un produit pour chaque vente. Ce n’est pas un scénario typique, mais parfois le coût du produit peut être réduit par le fournisseur en fonction du client de la vente finale.

Par exemple :

Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d’A Datum Corporation. Fabrikam fournit des services d’installation mais les bras robotiques sont fournis par Trey Robotics. Si l’installation de bras robotiques chez A Datum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam.

Dans ce cas, Fabrikam créera une ligne de devis basée sur le produit pour Robotic Arms et saisira un coût unitaire spécial pour ce devis. Ce coût est différent du coût standard des bras robotiques Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]