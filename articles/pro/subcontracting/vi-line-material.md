---
title: Lignes de facture fournisseur pour les produits
description: Cet article explique comment enregistrer les lignes de facture fournisseur pour les produits et utiliser les différents champs pour enregistrer les achats de produits auprès des fournisseurs.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931373"
---
# <a name="vendor-invoice-lines-for-products"></a>Lignes de facture fournisseur pour les produits

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une facture fournisseur dans Microsoft Dynamics 365 Project Operations peut avoir des lignes de facture fournisseur pour les produits (également appelés matériaux). Les chefs de projet peuvent utiliser les lignes de facture fournisseur pour les produits afin d’enregistrer les coûts de produits qui ont été achetés sur les projets.

Les lignes de facture fournisseur pour les produits peuvent ou non faire référence à une ligne de sous-traitance pour les matériaux. Si une ligne de facture fournisseur pour les produits fait référence à un sous-contrat, les chefs de projet pourront faire correspondre et vérifier les produits facturés par la ligne de facture fournisseur par rapport à l’utilisation des produits achetés qui sont enregistrés par des sous-traitants et approuvés par les chefs de projet sur le projet.

Le tableau suivant fournit des informations sur les champs des lignes de facture fournisseur pour les produits.

| Champ | Description | Impact fonctionnel |
| --- | --- | --- |
| Nom  | Le nom de la ligne de facture fournisseur, pour aider à l’identification. | Ce nom apparaît dans la première colonne de toutes les recherches basées sur les lignes de facture fournisseur. |
| Description | Brève description des produits facturés par le fournisseur sur la ligne de facture fournisseur. | None |
| Sous-contrat | Le contrat de sous-traitance pour lequel les produits ont été initialement commandés. | Lorsqu’un contrat de sous-traitance est sélectionné pour la facture fournisseur, toutes les lignes de la facture fournisseur héritent de cette sélection. Une facture fournisseur ne peut pas avoir de lignes de facture fournisseur faisant référence à différents contrats de sous-traitance. |
| Ligne de sous-traitance | La ligne de sous-traitance pour lequel les produits ont été commandés. La liste des lignes de contrat de sous-traitance sélectionnables est limitée aux lignes du contrat de sous-traitance sélectionné. | Lorsqu’une ligne de sous-traitance est sélectionnée sur une ligne de facture fournisseur pour les produits, les valeurs par défaut des champs **Projet**, **Tâche** et **Produit** sont renseignés à partir des champs correspondants sur la ligne de sous-traitance. Si la ligne de sous-traitance sélectionnée a des valeurs dans les champs **Projet**, **Tâche** et **Produit**, les valeurs des champs correspondants sur la ligne de facture fournisseur ne peuvent pas différer de ces valeurs. |
| Date de la transaction | La date à laquelle le chiffre réel du coût de la ligne de facture fournisseur sera enregistré sur le projet. | None|
| Classe de transaction | Lorsque les produits sont facturés, ce champ doit être défini sur **Matériel**. | La valeur **Matériel** indique que la ligne de facture fournisseur est utilisée pour enregistrer le montant de la facture pour les matériels achetés. |
| Project | Le nom du projet pour lequel les produits facturés ont été utilisés. | Ce champ est obligatoire et ne peut pas être vide. |
| Task | Le nom de la tâche du projet pour lequel les produits facturés ont été utilisés. Ce champ est disponible uniquement si un projet est sélectionné. La sélection d’une tâche de projet est facultative. | Si ce champ est laissé vide, le chef de projet peut associer la ligne de facture fournisseur au produit acheté utilisé sur n’importe quelle tâche du projet. Si la ligne de facture fournisseur ne fait pas référence à une ligne de contrat de sous-traitance et que ce champ est laissé vide, le chiffre réel du coût créé par la ligne de facture fournisseur ne sera pas associé à des chiffres réels de ventes non facturées. Dans ce cas, si la facturation à la tâche est mise en place, les frais ne pourront pas être facturés au client final. |
| Sélectionner un produit | Indiquez si le produit en cours de facturation est un produit existant dans le catalogue de produits ou s’il s’agit d’un produit hors catalogue. | La valeur par défaut est saisie à partir de la ligne du contrat de sous-traitance lorsqu’une ligne de contrat de sous-traitance est sélectionnée. |
| Produit | Sélectionnez le produit dans le catalogue. Si le produit est un produit hors catalogue, entrez le nom du produit. | Ce champ est utilisé pour saisir les prix d’achat par défaut des produits existants. |
| Quantité | Saisissez la quantité de matériel facturée par le fournisseur sur cette ligne de facture. | None |
| Groupe d’unités | Sélectionnez le groupe d’unités de l’unité dans laquelle la quantité facturée est exprimée. | None |
| Unité | La valeur par défaut de ce champ est l’unité de base du groupe d’unités sélectionné. Vous pouvez modifier cette valeur pour payer dans toute unité du groupe d’unités sélectionné. | L’association des valeurs **Produit** et **Unité** est utilisée par défaut ou calculée pour le champ **Prix unitaire** sur la ligne de facture fournisseur. |
| Prix unitaire | Le prix unitaire par défaut utilise la combinaison des valeurs **Produit** et **Unité** du tarif du projet applicables à la date de transaction de la ligne de facture fournisseur. | None |
| Sous-total | Ce champ en lecture seule est calculé de la façon suivante : *Quantité* &times; *Prix unitaire*, si les valeurs sont saisies dans le champ **Quantité** et **Prix unitaire**. Si un ou les deux champs sont vides, vous pouvez entrer une valeur dans ce champ. | None |
| Taxe de vente | Entrez le montant de la taxe de ventes. | None |
| Montant total | Montant total de la ligne de facture fournisseur, taxes comprises. Ce champ est calculé de la façon suivante : *Sous-total* + *Taxe de vente*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
