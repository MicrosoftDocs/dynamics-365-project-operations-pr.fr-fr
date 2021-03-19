---
title: Tarifs des produits
description: Cette rubrique fournit des informations sur les tarifs des catalogues utilisés pour les devis de projet et les contrats.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c0f30bec159254c078024549b7b0dd0c048ef65d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275355"
---
# <a name="product-price-lists"></a>Tarifs des produits

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les entités Tarifs et Élément tarifaire prennent en charge la tarification du catalogue des produits. Pour la plupart, cette fonction est utilisée pour les lignes basées sur un catalogue sur des devis de projet et des contrats de projet.

Pour les lignes basées sur un projet, un contrat représente la transaction après qu’elle a été remportée. Dans la mesure où le processus de négociation précède généralement la conclusion de la vente, la tarification qui est jointe au devis est toujours copiée conformément aux nouveaux tarifs et attachée au contrat. Ces nouveaux tarifs ne peuvent pas être modifiés en dehors de l’étendue du contrat. Cette limite aide à protéger la carte de tarifs négociée contre tous les changements de prix qui se produisent dans les principaux tarifs.

Les produits doivent être configurés afin de ne pas avoir le coût et les tarifs par défaut dans le catalogue des produits. Utilisez les tarifs, le coût standard, et le coût actuel pour configurer le coût et les tarifs par défaut. Les tarifs par défaut sont utilisés sur une ligne de devis ou une ligne de contrat du projet uniquement lorsque le système ne parvient pas à trouver une ligne de tarifs pour ce produit dans la liste des tarifs du devis ou du contrat du projet.

Le prix de revient des lignes du catalogue de produits peut être modifié entre devis. Cette fonctionnalité est importante, car si vous ne suivez pas précisément les coûts, vous ne pouvez pas déterminer les bénéfices opérationnels par rapport aux engagements du projet. Par défaut, le coût standard du produit est utilisé comme prix de revient. Toutefois, le prix de revient par défaut peut être mis à jour sur la ligne de devis s’il existe un prix de revient distinct pour ce devis.

## <a name="price-list-items"></a>Éléments tarifaires

Vous pouvez ajouter des produits d’un catalogue de produits à plusieurs tarifs. Les lignes de tarifs pour les produits référencent toujours une unité spécifique. La tarification d’un produit sur les éléments tarifaires peut être configurée comme un montant en devise. Sinon, elle peut être configurée en fonction du tarif, du coût actuel ou du coût standard.

PSA prend en charge diverses options d’arrondi si les prix sont configurés en fonction du tarif, du coût standard, ou du coût actuel. En plus de bénéficier de plusieurs modes de tarification et d’options d’arrondis, vous pouvez associer des types de remises aux éléments tarifaires. 

Lorsque vous créez des tarifs personnalisés pour un devis en sélectionnant **Créer une tarification personnalisée** sur la page **Devis du projet**, une copie des tarifs est effectuée, et le champ **Entité** sur l’en-tête des nouveaux tarifs est défini sur **Entité des ventes**. Le nom des nouveaux tarifs est ajouté au nom du devis avec un horodatage. Vous pouvez également utiliser le nom des nouveaux tarifs et le nom du devis dans les workflows personnalisés pour déclencher une révision et des approbations supplémentaires pour les devis qui utilisent la tarification personnalisée.

 
## <a name="default-product-price-list"></a>Tarif de produit par défaut
Chaque enregistrement client a un champ **Tarifs par défaut**, dans lequel vous pouvez spécifier un tarif correspondant à la devise du client. Une valeur par défaut n’est pas automatiquement entrée dans ce champ. Lorsqu’un contrat de tarification personnalisé avec un client spécifique existe, vous pouvez utiliser ce champ pour associer des tarifs à ce client.

Les entités Opportunité, Devis et Contrat de projet utilisent l’ordre suivant pour entrer des tarifs de produits par défaut. Le même ordre est utilisé pour les tarifs de projets.

1.  Devis
2.  Opportunité
3.  Client
4.  Paramètres globaux 

Par défaut, le champ **Produit** sur la ligne de devis liste tous les produits actifs dans les tarifs de produits du devis. Si un produit a été désactivé, ou s’il s’agit d’un brouillon de produit, il n’est pas répertorié, même s’il est dans les tarifs. 

Les lignes du catalogue de produits sont ajoutées en tant que lignes de facture dans la première facture créée pour un contrat de projet. Dans un brouillon de facture, ces lignes de facture peuvent être supprimées. Dans ce cas, les lignes s’afficheront sur une facture suivante jusqu’à ce qu’elles soient facturées, ou jusqu’à ce que la facture soit envoyée au client. Vous ne pouvez pas facturer une quantité partielle d’une ligne de facture de produit. Lorsque les lignes de produits du contrat du projet sont facturées, les chiffres réels sont créés. Toutefois, ces chiffres réels ne sont pas liés à l’entité de projet associée. En d’autres termes, les lignes du contrat du projet basé sur un produit sont indépendantes de toute utilisation basée sur un projet. Le suivi de la consommation de matériaux sur les projets n’est pas effectué.


[!INCLUDE[footer-include](../includes/footer-banner.md)]