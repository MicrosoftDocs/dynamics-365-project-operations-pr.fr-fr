---
title: Lignes du contrat de sous-traitance pour les produits
description: Cette rubrique explique comment enregistrer des lignes du contrat de sous-traitance pour les produits et comment utiliser les différents champs pour enregistrer les achats de produits auprès des fournisseurs.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323683"
---
# <a name="subcontract-lines-for-products"></a>Lignes du contrat de sous-traitance pour les produits

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de sous-traitance dans Dynamics 365 Project Operations peut comporter des lignes pour les produits. Ces lignes permettent à un chef de projet d’acheter des produits auprès de fournisseurs et de les utiliser ensuite sur des tâches de projet.

Procédez comme suit pour créer des lignes pour les produits dans le contrat de sous-traitance dans Project Operations.

1. Sur la page de navigation, sélectionnez **Contrats de sous-traitance**, puis ouvrez le contrat de sous-traitance que vous voulez utiliser. 
2. Sur l’onglet **Lignes du contrat de sous-traitance**, sélectionnez **+ Nouveau** pour créer une nouvelle ligne.
3. Sur la page **Création rapide**, dans le champ **Classe de transaction**, sélectionnez **Matériel** et entrez ou sélectionnez les informations de champ requises. 
4. Sélectionnez **Enregistrer**.

Le tableau suivant fournit des informations sur les champs de la page des détails **Ligne du contrat de sous-traitance** et de la page **Création rapide** qui sont pertinents pour l’achat de produits.

| Champ | Description |
| ----- | ----------- |
| Nom | Le nom de la ligne du contrat de sous-traitance. |
| Description | Une brève description des produits qui sont commandés sur la ligne du contrat de sous-traitance. |
| Type de ligne | La valeur de ce champ est définie par défaut sur **Basé sur la quantité**. |
| Mode de facturation |  Le mode de facturation de la ligne du contrat de sous-traitance. Un échéancier de facturation basé sur des jalons est disponible pour les modes de facturation à prix fixe. |
| Classe de transaction | La valeur de ce champ est définie par défaut sur **Temps**. Pour créer des lignes de contrat de sous-traitance pour l’achat de produits, dans le champ **Classe de transaction**, sélectionnez **Matériel**. Cette sélection indique que la ligne du contrat de sous-traitance est utilisée pour enregistrer un achat de produits à utiliser sur des projets. |
| Sélectionner un produit | Sélectionnez cette option si le produit acheté est conservé dans le catalogue de produits ou s’il s’agit d’un produit hors catalogue. |
| Produit | Sélectionnez un produit actif dans le catalogue. Ce champ est disponible uniquement lorsque le champ **Sélectionner un produit** est défini sur **Existant**. |
| Produit hors catalogue | Entrez le nom du produit hors catalogue. Ce champ est disponible uniquement lorsque le champ **Sélectionner un produit** est défini sur **Hors catalogue**.  |
| Date de livraison demandée | Sélectionnez la date de livraison souhaitée pour les produits. Cette date permet aussi de choisir un tarif projet parmi ceux rattachés au contrat de sous-traitance. Le coût du produit sur la ligne du contrat de sous-traitance est alors défini par défaut à partir de ce tarif. |
| Date de livraison contractuelle | Sélectionnez la date à laquelle il est convenu que les produits soient livrés.  |
| Quantité commandée | Entrez la quantité de produits achetée auprès du fournisseur. Un avertissement s’affiche si un chef de projet dépasse cette quantité. |
| Groupe d’unités | Cette valeur est définie par défaut pour les produits du catalogue uniquement. Lorsque **Produit** et **Date de livraison demandée** sont tous deux sélectionnés, le système sélectionne les tarifs applicables en fonction de la date de livraison. Les éléments tarifaires associés sont interrogés pour le produit correspondant. Les valeurs d’unité et de groupe d’unités par défaut proviennent de la configuration de l’enregistrement de l’élément tarifaire. |
| Unité | Cette valeur est définie par défaut sur la configuration de l’unité sur l’enregistrement de l’élément tarifaire. Vous pouvez la remplacer par une autre unité, si nécessaire. La combinaison entre le produit et l’unité permet de calculer le prix unitaire par défaut de la ligne du contrat de sous-traitance pour les produits existants dans le catalogue. |
| Prix unitaire | Le prix unitaire provient par défaut de la combinaison entre le produit et l’unité des éléments tarifaires associés aux tarifs du projet qui s’applique à la date de livraison demandée de la ligne du contrat de sous-traitance.  |
| Sous-total | Ce champ en lecture seule est calculé comme suit : Quantité x Prix unitaire, si des valeurs sont saisies dans les deux champs. Si le champ **Quantité**, **Prix unitaire** ou les deux sont vides, vous pouvez saisir une valeur manuellement.  |
| Taxe de ventes | Entrez la valeur de la taxe de ventes. |
| Montant total | Ce champ calculé indique le montant total de la ligne du contrat de sous-traitance, taxes incluses. La valeur de ce champ est calculée comme suit : sous-total + taxe. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
