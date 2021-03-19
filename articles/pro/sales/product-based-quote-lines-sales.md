---
title: Vue d’ensemble des lignes du devis basées sur les produits – Simplifié
description: Cette rubrique fournit des informations pour travailler avec des lignes de devis basées sur les produits.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272565"
---
# <a name="product-based-quote-lines-overview---lite"></a>Vue d’ensemble des lignes du devis basées sur les produits – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez créer des lignes de devis basées sur un produit dans Dynamics 365 Project Operations. Les lignes de devis basées sur les produits peuvent ajoutées manuellement, ou elles peuvent provenir des articles du catalogue des produits.

## <a name="product-catalog"></a>Catalogue de produits

Chaque produit dans le catalogue de produits contient une unité et un groupe d’unités par défaut. Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui partage ces attributs. 

Par exemple, une société vend des licences d’abonnement pour différents types de logiciel. Tout les logiciels sur abonnement ont les deux attributs suivants :

- Nombre d’utilisateurs
- Durée de l’abonnement mesurée en mois

Pour gérer ce type de catalogue, créez une famille de produits nommée **Logiciel sur abonnement** et ajoutez le nombre d’utilisateurs et la durée de l’abonnement comme attributs. Ensuite, ajoutez des produits individuels à la famille de produits **Logiciel sur abonnement**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Ajouter des articles du catalogue de produits à un devis de projet

Les pages **Devis de devis** et **Contrat du projet** ont des sections pour deux types de lignes : lignes basées sur un projet et lignes basées sur les produits. Pour les lignes basées sur les produits, la liste déroulante dans la ligne de devis ou la ligne de contrat du projet comprend tous les produits et unités des tarifs des produits. Vous pouvez également ajouter des produits qui ne figurent pas dans les tarifs des produits.

En outre, vous pouvez sélectionner des produits d’autres tarifs ou directement dans le catalogue de produits. Lorsque vous sélectionnez les produits directement à partir d’un catalogue de produits, les tarifs par défaut de ce produit sont utilisés pour obtenir le prix de vente du produit. Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).

Lorsqu’une ligne de devis est basée sur un catalogue de produits, vous pouvez remplacer le prix de vente directement sur la ligne de devis. Une ligne de devis dans le champ **Tarification** avec deux valeurs disponibles :

- **Remplacer tarifs**
- **Utiliser la valeur par défaut**

Si vous sélectionnez **Remplacer la tarification**, le prix par défaut n’est pas défini. Vous devez plutôt saisir un prix pour le produit dans la ligne de devis. Si vous sélectionnez **Utiliser la valeur par défaut**, le tarif de vente par défaut est utilisé et le champ est verrouillé pour modification.

Des prix de vente par défaut sont saisis dans les lignes basées sur les produits d’un devis. Le champ **Tarification** est alors défini sur **Remplacer la tarification** pour pouvoir modifier le prix par défaut sur les lignes de devis. Il s’agit d’un remplacement spécifique à Project Operations du comportement des lignes basées sur les produits dans Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]