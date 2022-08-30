---
title: Lignes de facture fournisseur pour les catégories de dépenses
description: Cet article explique comment enregistrer les lignes de facture fournisseur pour les catégories de dépenses.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261679"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Lignes de facture fournisseur pour les catégories de dépenses

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une facture fournisseur dans Microsoft Dynamics 365 Project Operations peut avoir des lignes de facture fournisseur pour les catégories de dépenses. Les chefs de projet peuvent utiliser des lignes de facture fournisseur pour les catégories de dépenses afin d’enregistrer les coûts des services achetés en tant que catégories de dépenses.

Les lignes de facture fournisseur pour les catégories de dépenses peuvent ou non faire référence à une ligne de sous-traitance pour les catégories de dépenses. Si une ligne de facture fournisseur pour les catégories de dépenses fait référence à un sous-contrat, les chefs de projet pourront faire correspondre et vérifier les dépenses facturées par la ligne de facture fournisseur par rapport aux dépenses enregistrées dans ces catégories de dépenses et approuvées par les chefs de projet sur le projet.

Le tableau suivant fournit des informations sur les champs des lignes de facture fournisseur pour les catégories de dépense.

| Champ | Description | Impact fonctionnel |
| --- | --- | --- |
| Nom  | Le nom de la ligne de facture fournisseur, pour aider à l’identification. | Ce nom apparaît dans la première colonne de toutes les recherches basées sur les lignes de facture fournisseur. |
| Description | Brève description des services facturés par le fournisseur sur la ligne de facture fournisseur. | None |
| Sous-contrat | Le contrat de sous-traitance pour lequel les services ont été initialement commandés. | Lorsqu’un contrat de sous-traitance est sélectionné pour la facture fournisseur, toutes les lignes de la facture fournisseur héritent de cette sélection. Une facture fournisseur ne peut pas avoir de lignes de facture fournisseur faisant référence à différents contrats de sous-traitance. |
| Ligne de sous-traitance | La ligne de sous-traitance pour lequel les services ont été commandés. La liste des lignes de contrat de sous-traitance sélectionnables est limitée aux lignes du contrat de sous-traitance sélectionné. | Lorsqu’une ligne de sous-traitance est sélectionnée sur une ligne de facture fournisseur pour les catégories de dépenses, les valeurs par défaut des champs **Projet**, **Tâche** et **Catégorie d’opération** sont renseignés à partir des champs correspondants sur la ligne de sous-traitance. Si la ligne de sous-traitance sélectionnée a des valeurs dans les champs **Projet**, **Tâche de projet** et **Catégorie de transaction**, les valeurs des champs correspondants sur la ligne de facture fournisseur ne peuvent pas différer de ces valeurs. |
| Date de la transaction | La date à laquelle le chiffre réel du coût de la ligne de facture fournisseur sera enregistré sur le projet. |None |
| Classe de transaction | Sélectionnez **Dépense** pour enregistrer une facture fournisseur pour une catégorie de dépenses. | La valeur **Dépense** indique que la ligne de facture fournisseur est utilisée pour enregistrer le montant de la facture pour les services achetés en tant que catégories de dépenses. |
| Project | Le nom du projet pour lequel les services facturés ont été utilisés. | Ce champ est obligatoire et ne peut pas être vide. |
| Task | Le nom de la tâche du projet pour lequel les services facturés ont été utilisés. Ce champ est disponible uniquement si un projet est sélectionné. La sélection d’une tâche de projet est facultative. | Si ce champ est laissé vide, le chef de projet peut associer la ligne de facture fournisseur aux dépenses enregistrées sur n’importe quelle tâche du projet. Si la ligne de facture fournisseur ne fait pas référence à une ligne de contrat de sous-traitance et que ce champ est laissé vide, le chiffre réel du coût créé par la ligne de facture fournisseur ne sera pas associé à des chiffres réels de ventes non facturées. Dans ce cas, si la facturation à la tâche est mise en place, les frais ne pourront pas être facturés au client final. |
| Catégorie de transaction | La catégorie de transaction qui est facturée. Une catégorie de dépense correspondante doit être créée pour la catégorie de transaction sélectionnée. | L’association des valeurs **Catégorie de transaction** et **Unité** est utilisée par défaut ou calculée pour le champ **Prix unitaire** sur la ligne de facture fournisseur. |
| Quantité | Saisissez la quantité facturée par le fournisseur sur la ligne de facture. |None|
| Groupe d’unités | Une valeur par défaut est saisie en fonction du groupe d’unités de la catégorie de transaction sélectionnée. | None |
| Unité | La valeur par défaut de ce champ est l’unité de base du groupe d’unités sélectionné. Vous pouvez modifier cette valeur pour acheter toute unité du groupe d’unités. | L’association des valeurs **Catégorie de transaction** et **Unité** est utilisée par défaut ou calculée pour le champ **Prix unitaire** sur la ligne de facture fournisseur. |
| Prix unitaire | Le prix unitaire par défaut utilise la combinaison des valeurs **Catégorie de transaction** et **Unité** du tarif du projet applicables à la date de transaction de la ligne de facture fournisseur. | Si le tarif du projet applicable est configuré dans une unité différente de celle de l’unité sur la ligne de facture fournisseur, le système utilise la conversion d’unité pour calculer le prix unitaire. |
| Sous-total | Ce champ en lecture seule est calculé de la façon suivante : *Quantité* &times; *Prix unitaire*, si les valeurs sont saisies dans le champ **Quantité** et **Prix unitaire**. Si un ou les deux champs sont vides, vous pouvez entrer une valeur dans ce champ.| None |
| Taxe de vente | Entrez le montant de la taxe de ventes. | None |
| Montant total | Montant total de la ligne de facture fournisseur, taxes comprises. Ce champ est calculé de la façon suivante : *Sous-total* + *Taxe de vente*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
