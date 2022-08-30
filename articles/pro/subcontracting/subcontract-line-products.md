---
title: Lignes du contrat de sous-traitance pour les produits
description: Cet article explique comment enregistrer les lignes de sous-contrat pour les produits et utiliser les différents champs pour enregistrer les achats de produits auprès des fournisseurs.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262106"
---
# <a name="subcontract-lines-for-products"></a>Lignes du contrat de sous-traitance pour les produits

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de sous-traitance dans Dynamics 365 Project Operations peut comporter des lignes pour les produits. Ces lignes permettent à un chef de projet d’acheter des produits auprès de fournisseurs et de les utiliser ensuite sur des tâches de projet.

Procédez comme suit pour créer des lignes pour les produits dans le contrat de sous-traitance dans Project Operations.

1. Sur la page de navigation, sélectionnez **Contrats de sous-traitance**, puis ouvrez le contrat de sous-traitance que vous voulez utiliser. 
2. Sur l’onglet **Lignes du contrat de sous-traitance**, sélectionnez **+ Nouveau** pour créer une nouvelle ligne.
3. Sur la page **Création rapide**, dans le champ **Classe de transaction**, sélectionnez **Matériel** et entrez ou sélectionnez les informations de champ requises. 
4. Sélectionnez **Enregistrer**.

Le tableau suivant fournit des informations sur les champs de la page des détails **Ligne du contrat de sous-traitance** et de la page **Création rapide** qui sont pertinents pour l’achat de produits.

| Champ | Description | Impact fonctionnel|
| ----- | ----------- | ----------- |
| Nom | Le nom de la ligne du contrat de sous-traitance pour aider à l’identification. |Il apparaît dans la première colonne de toutes les recherches basées sur les lignes du contrat de sous-traitance.
| Description | Une brève description des produits qui sont commandés sur la ligne du contrat de sous-traitance. | Aucun(e) |
| Type de ligne | Ce champ contient la valeur par défaut **Basé sur la quantité**. |Aucun(e) |
| Mode de facturation | Ce groupe d’options représente les deux principaux modèles contractuels pris en charge par Project Operations : **Prix fixe** et **Temps et matériel**. | En fonction du mode de facturation sélectionné, une planification de facturation basée sur des jalons est mise à disposition pour les lignes du contrat de sous-traitance avec le mode de facturation à prix fixe. |
| Classe de transaction |Ce champ contient une valeur par défaut **Temps**. Pour créer des lignes de contrat de sous-traitance pour acheter des produits, définissez le champ **Classe de transaction** sur **Matériel**.  | Il indique que la ligne du contrat de sous-traitance est utilisée pour enregistrer l’achat de produits à utiliser dans les projets. |
| Sélectionner un produit | Sélectionnez cette option si le produit acheté est conservé dans le catalogue de produits ou s’il s’agit d’un produit hors catalogue. |Aucun(e) |
| Produit | Sélectionnez un produit actif dans le catalogue. Ce champ est disponible uniquement lorsque le champ **Sélectionner un produit** est défini sur **Existant**. |L’association **Produit** et **Unité** est utilisée par défaut ou calculée pour le prix unitaire de la ligne du contrat de sous-traitance.
| Produit hors catalogue | Entrez le nom du produit hors catalogue. Ce champ est disponible uniquement lorsque le champ **Sélectionner un produit** est défini sur **Hors catalogue**.  |Le prix d’achat n’est pas automatiquement renseigné pour les produits hors catalogue.|
| Date de livraison demandée | Entrez la date de livraison obligatoire pour les produits.| Cette date permet aussi de choisir un tarif projet parmi ceux rattachés au contrat de sous-traitance. Le coût du produit sur la ligne du contrat de sous-traitance est alors défini par défaut à partir de ce tarif. |
| Date de livraison contractuelle | Entrez la date à laquelle les produits sont contractuellement prévus d’être livrés.  |Aucun(e)|
| Quantité commandée | Entrez la quantité de produits achetée auprès du fournisseur.| Elle permet d’afficher des avertissements si un chef de projet puise excessivement dans cette quantité.|
| Groupe d’unités | Cette valeur est définie par défaut pour les produits du catalogue uniquement. |Lorsque **Produit** et **Date de livraison demandée** sont tous deux sélectionnés, le système sélectionne les tarifs applicables en fonction de la date de livraison. Les éléments tarifaires associés sont interrogés pour le produit correspondant. Les valeurs d’unité et de groupe d’unités par défaut proviennent de la configuration de l’enregistrement de l’élément tarifaire. |
| Unité | Cette valeur est par défaut l’unité configurée dans l’enregistrement de l’élément tarifaire. Vous pouvez la remplacer par une autre unité, si nécessaire.| La combinaison entre le produit et l’unité permet de calculer le prix unitaire par défaut de la ligne du contrat de sous-traitance pour les produits existants dans le catalogue. |
| Prix unitaire | Le prix unitaire provient par défaut de la combinaison entre le produit et l’unité des éléments tarifaires associés aux tarifs du projet qui s’applique à la date de livraison demandée de la ligne du contrat de sous-traitance.  |Aucun(e) |
| Sous-total | Ce champ en lecture seule est calculé comme suit : Quantité x Prix unitaire, si des valeurs sont saisies dans les deux champs. Si le champ **Quantité**, **Prix unitaire** ou les deux sont vides, vous pouvez saisir une valeur manuellement.  |Aucun(e) |
| Taxe de ventes | Entrez la valeur de la taxe de ventes. |Aucun(e) |
| Montant total | Ce champ calculé indique le montant total de la ligne du contrat de sous-traitance, taxes incluses. La valeur de ce champ est calculée de la façon suivante : Sous-total + Taxe. |Aucun(e) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
