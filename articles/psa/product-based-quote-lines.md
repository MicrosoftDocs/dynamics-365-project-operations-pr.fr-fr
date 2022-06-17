---
title: Lignes de devis basées sur un produit
description: Cet article fournit des informations sur les lignes de devis basées sur un produit.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: a5385e1bb0f18a7cc1d23f4e46c86d8340ba951d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922679"
---
# <a name="product-based-quote-lines"></a>Lignes de devis basées sur un produit

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Vous pouvez créer des lignes de devis basées sur un produit dans Dynamics 365 Project Service Automation. Les lignes de devis basées sur un produit peuvent être des lignes « hors catalogue », ou elles peuvent provenir des articles du catalogue des produits.

## <a name="product-catalog"></a>Catalogue de produits

Les produits d’un catalogue de produits Dynamics 365 contiennent une unité et un groupe d’unités par défaut. Si plusieurs produits partagent le même ensemble d’attributs, vous pouvez créer une famille de produits qui comporte également ces attributs. Tous les produits d’une famille de produits héritent du même ensemble d’attributs.

Par exemple, une société vend des licences d’abonnement pour différents logiciels. Tout les logiciels sur abonnement ont les deux attributs suivants :

- Nombre d’utilisateurs 
- Durée de l’abonnement (en mois)

Un excellent moyen de gérer ce type de catalogue est de créer une famille de produits nommée **Logiciels sur abonnement**, avec **Nombre d’utilisateurs** et **Durée de l’abonnement** comme attributs. Vous pouvez ensuite ajouter des produits individuels, comme **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à la famille de produits **Logiciels sur abonnement**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Ajouter des articles du catalogue de produits à un devis de projet

Les pages Devis de projet et Contrat de projet ont des sections pour deux types de lignes : lignes basées sur un projet et lignes basées sur un produit. Pour les lignes basées sur un produit, Dynamics 365 est utilisé pour ajouter des articles d’un catalogue de produits vers un devis. La liste déroulante dans la ligne de devis ou la ligne de contrat du projet comprend tous les produits et unités des tarifs des produits joints au devis ou au contrat du projet. Vous pouvez également ajouter des produits qui ne figurent pas dans les tarifs des produits du devis.

En outre, vous pouvez sélectionner des produits d’autres tarifs, ou vous pouvez sélectionner des produits directement dans le catalogue de produits. Lorsque vous sélectionnez les produits directement à partir d’un catalogue de produits, les tarifs par défaut de ce produit sont utilisés pour obtenir le prix de vente du produit. Si un tarif par défaut n’est pas configuré, le prix est défini sur 0 (zéro).

Si une ligne de devis est basée sur un catalogue de produits, vous pouvez remplacer le tarif de vente directement sur la ligne de devis. Notez qu’une ligne de devis dans Dynamics 365 possède un champ **Tarification**. Deux valeurs sont disponibles :

- Remplacer la tarification  
- Utiliser la valeur par défaut

Si vous définissez ce champ sur **Remplacer la tarification**, Dynamics 365 ne définit pas de prix par défaut. Vous devez entrer un prix pour le produit dans la ligne de devis. Si vous définissez ce champ sur **Valeur par défaut**, Dynamics 365 utilise le prix de vente par défaut et verrouille le champ pour empêcher l’édition.

Après avoir installé PSA, des prix de vente par défaut sont entrés dans les lignes basées sur un produit d’un devis. Le champ **Tarification** est alors défini sur **Remplacer la tarification** pour pouvoir modifier le prix par défaut sur les lignes de devis.

> ![Définition du remplacement de la tarification.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Facteurs de quantité pour les produits

PSA utilise des facteurs de quantité pour prendre en charge la vente des produits basés sur un abonnement. Pour les produits basés sur abonnement, la quantité sur le devis ou la ligne de contrat du projet est exprimée sous la forme du nombre de mois d’utilisateur.

En règle générale, le prix des logiciels sur abonnement est stocké dans le catalogue comme prix par utilisateur par mois. Cependant, vous pouvez utiliser d’autres descriptions de temps à la place. Durant le processus de vente, le prix sur la ligne de devis est généralement le prix par utilisateur, par mois, négocié et avec remise, par l’agent de vente informatique. Chaque transaction a un nombre différent d’utilisateurs et un nombre différent de mois d’abonnement. La quantité utilisée pour calculer le montant de la ligne de devis est un produit du nombre d’utilisateurs et du nombre de mois d’abonnement.

Pour prendre en charge ce type de vente, PSA a présenté le concept de facteurs de quantité. Les facteurs de quantité reposent sur les attributs du produit dans Dynamics 365. Lorsque vous configurez des propriétés spécifiques pour un produit, PSA vous permet de marquer un sous-ensemble de ces propriétés, ou toutes les propriétés, comme des facteurs de la quantité.

PSA valide que seules les propriétés numériques ou les propriétés de produit ayant un type de données numérique sont marquées comme facteurs de la quantité. Lorsqu’un produit pour lequel des facteurs de quantité sont configurés est ajouté à une ligne de devis, le champ **Quantité** de la ligne de devis devient un champ en lecture seule. Après avoir entré des valeurs pour les propriétés du produit qui sont des facteurs de quantité, PSA calcule la quantité de la ligne de devis.

Par exemple, Dynamics 365 peut contenir les propriétés suivantes : 

- **Nombre d’utilisateurs** : Le nombre d’utilisateurs 
- **Nombre de mois** : Le nombre de mois d’abonnement
- **SKU produit** 

Les propriétés **Nombre d’utilisateurs** et **Nombre de mois** peuvent être marquées comme facteurs de quantité en modifiant les propriétés de la ligne de produit. 

> ![Marquage du Nombre d’utilisateurs et du Nombre de mois comme facteurs de qualité.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
