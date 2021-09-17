---
title: Lignes du contrat de sous-traitance pour les catégories de dépenses
description: Cette rubrique explique comment enregistrer des lignes du contrat de sous-traitance pour les dépenses et comment utiliser les champs pour enregistrer l’achat de temps auprès des fournisseurs.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323818"
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

| **Champ** |  **Description** |
| ----------| ---------------- |
| Nom | Le nom de la ligne du contrat de sous-traitance. |
| Description | Une brève description des catégories de services ou de produits qui sont achetés sur la ligne du contrat de sous-traitance. |
| Type de ligne | Ce champ contient la valeur par défaut **Basé sur la quantité**.  |
| Mode de facturation | Le mode de facturation de la ligne du contrat de sous-traitance. En fonction du mode de facturation de la ligne, un échéancier de facturation basé sur des jalons est mis à disposition pour le mode de facturation à prix fixe.  |
| Classe de transaction | Ce champ contient la valeur par défaut **Temps**. Pour créer des lignes de contrat de sous-traitance pour l’achat de produits, définissez le champ **Classe de transaction** sur **Dépense**. Cette valeur de champ indique que la ligne du contrat de sous-traitance est utilisée pour enregistrer un achat d’une catégorie de produits ou de services à utiliser sur des projets. |
| Catégorie de transaction | Sélectionnez la catégorie de transaction. |
| Début demandé | La date à laquelle les catégories d’achat doivent être disponibles auprès du fournisseur. Le démarrage demandé permet de choisir un tarif projet parmi ceux rattachés au contrat de sous-traitance. Le coût de la catégorie sur la ligne du contrat de sous-traitance est défini par défaut à partir de ce tarif. |
| Fin demandée | La date à laquelle les catégories d’achat ne sont plus nécessaires. Un avertissement s’affiche si un chef de projet associe cette ligne du contrat de sous-traitance à des estimations de dépenses spécifiques sur les projets qui sont postérieures à cette date. |
| Quantité commandée | La quantité d’articles de cette catégorie achetée auprès du fournisseur. Un avertissement s’affiche si un chef de projet dépasse la quantité achetée.  |
| Groupe d’unités | La valeur par défaut de ce champ est basée sur le groupe d’unités par défaut configuré pour la catégorie sélectionnée. |
| Unité | La valeur par défaut de ce champ est basée sur l’unité par défaut configurée pour la catégorie sélectionnée. La combinaison entre la catégorie et l’unité permet de calculer le prix unitaire par défaut de la ligne du contrat de sous-traitance. |
| Prix unitaire | La valeur du champ Prix unitaire provient par défaut de la combinaison entre la catégorie et l’unité des prix de la catégorie associés aux tarifs du projet qui s’applique à la date de début demandée de la ligne du contrat de sous-traitance.  |
| Sous-total | Il s’agit d’un champ en lecture seule qui est automatiquement calculé comme prix unitaire de quantité, si les valeurs de quantité et de prix unitaire sont saisies. Si l’un des champs ou les deux sont vides, vous pouvez y saisir une valeur manuellement.  |
| Taxe de ventes | Entrez le montant de la taxe de ventes.  |
| Montant total | Le montant total de la ligne de sous-traitance, taxes incluses. Ce champ est calculé comme suit : sous-total + taxe de vente.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
