---
title: Lignes de facture fournisseur pour les jalons
description: Cet article explique comment créer des lignes de facture fournisseur pour les jalons d’un contrat de sous-traitance.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931327"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Lignes de facture fournisseur pour les jalons

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une facture fournisseur dans Microsoft Dynamics 365 Project Operations peut avoir des lignes de facture fournisseur pour les jalons définis sur une ligne de contrat de sous-traitance. Les chefs de projet peuvent utiliser des lignes de facture fournisseur pour les jalons afin d’enregistrer les coûts des services achetés en tant que coûts basés sur les jalons engagés sur les services ou les produits achetés pour le projet.

Les lignes de facture fournisseur pour les jalons doivent toujours faire référence à une ligne de contrat de sous-traitance avec un mode de facturation à prix fixe. Si une ligne de facture fournisseur pour les jalons fait référence à une ligne de contrat de sous-traitance, les chefs de projet pourront faire correspondre et vérifier les coûts sous-jacents de temps, dépense ou matériel qui fait référence à une ligne de contrat de sous-traitance par rapport au jalon facturé par le fournisseur.

Le tableau suivant fournit des informations sur les champs des lignes de facture fournisseur pour les jalons.

| Champ | Description | Impact fonctionnel |
| --- | --- | --- |
| Nom  | Le nom de la ligne de facture fournisseur, pour aider à l’identification. | Ce nom apparaît dans la première colonne de toutes les recherches basées sur les lignes de facture fournisseur. |
| Description | Brève description des services facturés par le fournisseur sur la ligne de facture fournisseur. | None |
| Sous-contrat | Le contrat de sous-traitance pour lequel les services ont été initialement commandés. | Lorsqu’un contrat de sous-traitance est sélectionné pour la facture fournisseur, toutes les lignes de la facture fournisseur héritent de cette sélection. Une facture fournisseur ne peut pas avoir de lignes de facture fournisseur faisant référence à différents contrats de sous-traitance. |
| Ligne de sous-traitance | La ligne de sous-traitance pour lequel les services ont été commandés. La liste des lignes de contrat de sous-traitance sélectionnables est limitée aux lignes du contrat de sous-traitance sélectionné. | Lorsqu’une ligne du contrat de sous-traitance est sélectionnée sur une ligne de facture fournisseur pour les jalons, les champs **Rôle** et **Catégorie de transaction** et les champs liés au produit ne sont pas pertinents et ne sont pas disponibles. Les champs **Quantité**, **Unité** et **Groupe d’unités** ne sont pas non plus pertinents pour les lignes de facture fournisseur basées sur des jalons. |
| Date de la transaction | La date à laquelle le chiffre réel du coût de la ligne de facture fournisseur sera enregistré sur le projet. | None |
| Classe de transaction | Sélectionnez **Jalon** pour enregistrer une facture fournisseur pour un jalon terminé qui a été défini sur une ligne de contrat de sous-traitance. | None |
| Jalon | Sélectionnez le jalon défini sur la ligne de contrat de sous-traitance associée marquée comme **Prêt pour la facturation**. | Impossible de sélectionner une ligne de contrat de sous-traitance avec le statut **Prêt pour la facturation** sur une ligne de facture fournisseur. |
| Project | Le nom du projet pour lequel les services facturés ont été utilisés. | Ce champ est obligatoire et ne peut pas être vide. |
| Task | Le nom de la tâche du projet pour lequel les services facturés ont été utilisés. Ce champ est disponible uniquement si un projet est sélectionné. La sélection d’une tâche de projet est facultative. | Si ce champ est laissé vide, le chef de projet peut associer la ligne de facture fournisseur à la classe de transactions sur la ligne de contrat de sous-traitance associée enregistrée sur n’importe quelle tâche du projet. Si la ligne de facture fournisseur ne fait pas référence à une ligne de contrat de sous-traitance et que ce champ est laissé vide, le chiffre réel du coût créé par la ligne de facture fournisseur ne sera pas associé à des chiffres réels de ventes non facturées. Dans ce cas, si la facturation à la tâche est mise en place, les frais ne pourront pas être facturés au client final. |
| Montant du jalon | Saisissez la valeur du jalon défini sur la ligne de contrat de sous-traitance marquée comme prête pour la facturation. | None |
| Taxe de vente | Entrez le montant de la taxe de ventes. | None |
| Montant total | Montant total de la ligne de facture fournisseur, taxes comprises. Ce champ est calculé de la façon suivante : *Montant du jalon* + *Taxe de vente*. | None |

> [!NOTE]
> Lorsqu’une ligne de facture fournisseur faisant référence à un jalon de ligne de sous-traitance est créée, le statut du jalon de sous-traitance est mis à jour sur **Facture fournisseur créée**. Ensuite, lorsque cette facture fournisseur est confirmée, le statut du jalon de la ligne de sous-traitance est mis à jour sur **Facture fournisseur confirmée**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
