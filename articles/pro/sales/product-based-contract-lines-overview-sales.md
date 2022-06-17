---
title: Vue d’ensemble des lignes de contrat basées sur un projet – Simplifié
description: Cet article fournit des informations sur les lignes de contrat basées sur un produit.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919873"
---
# <a name="product-based-contract-lines-overview---lite"></a>Vue d’ensemble des lignes de contrat basées sur un produit – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez créer des lignes de contrat basées sur un produit dans Dynamics 365 Project Operations. Les lignes de contrat basées sur un produit peuvent être créées manuellement ou provenir des articles du catalogue de produits.

## <a name="product-catalog"></a>Catalogue de produits

Les produits du catalogue de produits contiennent une unité et un groupe d’unités par défaut. Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui comporte également ces attributs. Tous les produits d’une famille de produits héritent du même ensemble d’attributs.

Par exemple, une société vend des licences d’abonnement pour différents types de logiciel. Tout les logiciels sur abonnement ont les deux attributs suivants :

- Nombre d’utilisateurs
- Durée de l’abonnement (en mois)

Pour gérer ce type de catalogue, créez une famille de produits nommée **Logiciel d’abonnement**. Ajoutez les attributs, **Nombre d’utilisateurs** et **Durée de l’abonnement** à la famille de produits. Ajoutez ensuite des produits individuels à la famille de produits **Logiciel d’abonnement**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Ajouter des articles du catalogue de produits à un contrat de projet

Les contrats de projet comportent des sections pour deux types de lignes : basées sur un projet et basées sur un produit. Les lignes basées sur un produit incluent tous les produits et unités du tarif des produits du contrat. Les produits qui ne figurent pas dans les tarifs des produits du contrat peuvent être ajoutés.

Vous pouvez sélectionner des produits à partir d’autres tarifs ou directement à partir du catalogue de produits. Lorsque vous sélectionnez des produits directement à partir d’un catalogue de produits, le tarif par défaut de ce produit est utilisé pour le prix de vente du produit. Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).

Si une ligne de contrat est basée sur un catalogue de produits, vous pouvez remplacer le tarif de vente directement sur la ligne. Le champ **Tarification** d’une ligne de contrat a les deux valeurs :

- **Remplacer la tarification**
- **Utiliser la valeur par défaut**

Si vous définissez le champ **Tarification** sur **Remplacer la tarification**, le prix par défaut n’est pas défini. Entrez un prix pour le produit sur la ligne de contrat. Si vous définissez le champ sur **Utiliser la valeur par défaut**, le prix de vente par défaut est utilisé et le champ ne peut pas être modifié.

Après avoir installé Project Operations, des prix de vente par défaut sont entrés dans les lignes basées sur un produit d’un contrat. Le champ **Tarification** est défini sur **Remplacer la tarification** afin que vous puissiez modifier le prix par défaut sur les lignes de contrat. Il s’agit d’un remplacement spécifique à Project Operations du comportement des lignes basées sur un produit dans Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]