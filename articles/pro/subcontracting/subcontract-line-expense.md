---
title: Lignes du contrat de sous-traitance pour les catégories de dépenses
description: Cette rubrique explique comment enregistrer des lignes du contrat de sous-traitance pour les dépenses et comment utiliser les champs pour enregistrer l’achat de temps auprès des fournisseurs.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506096"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Lignes du contrat de sous-traitance pour les catégories de dépenses

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de sous-traitance dans Dynamics 365 Project Operations peut comporter une ligne pour les catégories de dépenses. Les lignes de contrat de sous-traitance pour les catégories de dépenses permettent à un chef de projet d’acheter des catégories de services ou de produits auprès de fournisseurs qu’il peut ensuite imputer à un projet.

Dans Project Operations, pour créer une ligne pour les catégories de dépense dans le contrat de sous-traitance, procédez comme suit :

1. Dans le volet de navigation, sélectionnez **Contrats de sous-traitance** et ouvrez le contrat de sous-traitance que vous voulez utiliser.
2. Sur l’onglet **Lignes du contrat de sous-traitance**, sélectionnez **Nouveau** pour créer une nouvelle ligne.
3. Sur la page **Création rapide**, dans le champ **Classe de transaction**, sélectionnez **Dépense** et entrez ou sélectionnez toute autre information de champ requise.

Le tableau suivant fournit des informations sur les champs de la page des détails **Ligne du contrat de sous-traitance** et de la page **Création rapide**.

| **Champ** | **Description** | **Impact fonctionnel** |
| --- | --- | --- |
| Nom | Le nom de la ligne du contrat de sous-traitance pour aider à l’identification. | Il apparaît dans la première colonne de toutes les recherches basées sur les lignes du contrat de sous-traitance. |
| Description | Une brève description des catégories de dépense achetées sur la ligne du contrat de sous-traitance. | Aucun(e) |
|Type de ligne | Ce champ contient une valeur par défaut **Basé sur la quantité**. |Aucun(e) |
| Mode de facturation | Ce groupe d’options représente les deux principaux modèles contractuels pris en charge par Project Operations : **Prix fixe** et **Temps et matériel**. | Une planification de facture basée sur des jalons est mise à disposition pour les lignes du contrat de sous-traitance si le mode de facturation à prix fixe est sélectionné. |
| Classe de transaction | Ce champ contient une valeur par défaut **Temps**. Pour créer des lignes de contrat de sous-traitance pour l’achat de produits, définissez le champ **Classe de transaction** sur **Dépense**.  | Il indique que la ligne du contrat de sous-traitance sert à enregistrer l’achat d’une catégorie de dépenses à utiliser dans les projets. |
| Catégorie de transaction | Affiche une liste des catégories de transaction actives dans le système. |Aucun(e) |
| Début demandé | Entrez la date à laquelle les catégories d’achat doivent être disponibles auprès du fournisseur. | Le début demandé permet de choisir un tarif du projet dans les tarifs du projet joints au contrat de sous-traitance. Le coût de la catégorie sur la ligne du contrat de sous-traitance provient de ce tarif. |
| Fin demandée | Entrez la date à laquelle les catégories d’achat ne seraient plus nécessaires. | Elle permet d’afficher des avertissements si un chef de projet associe cette ligne du contrat de sous-traitance à des estimations de dépense spécifiques sur le projet qui sont nécessaires après cette date. |
| Quantité commandée | Quantité de la catégorie achetée auprès du fournisseur. | Elle permet d’afficher des avertissements si un chef de projet puise excessivement dans cette quantité.|
| Groupe d'unités | La valeur par défaut est basée sur le groupe d’unités par défaut configuré pour la catégorie sélectionnée. |Aucun(e) |
| Unité | La valeur par défaut est basée sur l’unité par défaut configurée pour la catégorie sélectionnée.  | L’association **Catégorie** et **Unité** est utilisée par défaut ou calculée pour le prix unitaire de la ligne du contrat de sous-traitance.  |
| Prix unitaire | La valeur par défaut utilise l’association **Catégorie** et **Unité** des prix de catégorie associés au tarif du projet qui s’applique au début demandé de la ligne du contrat de sous-traitance. |Aucun(e) |
| Sous-total | Champ en lecture seule calculé de la façon suivante : Quantité x Prix unitaire, si les valeurs de quantité et de prix unitaire sont entrées. Si un ou les deux champs sont vides, vous pouvez entrer une valeur dans ce champ. |Aucun(e) |
| Taxe de ventes | Entrez le montant de la taxe de ventes. |Aucun(e) |
| Montant total | Le montant total de la ligne de sous-traitance, taxes incluses. Ce champ est calculé de la façon suivante : Sous-total + Taxe de vente. |Aucun(e) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
