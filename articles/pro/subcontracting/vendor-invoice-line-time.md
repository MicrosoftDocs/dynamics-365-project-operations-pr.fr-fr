---
title: Lignes de facture fournisseur pour le temps
description: Cet article explique comment enregistrer les lignes de facture fournisseur pour les coûts de temps que les sous-traitants ont mis en place.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262009"
---
# <a name="vendor-invoice-lines-for-time"></a>Lignes de facture fournisseur pour le temps

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une facture fournisseur dans Microsoft Dynamics 365 Project Operations peut avoir des lignes de facture fournisseur pour le temps. Les chefs de projet peuvent utiliser les lignes de facture fournisseur pour le temps afin d’enregistrer les coûts du temps des sous-traitants sur les projets.

Les lignes de facture fournisseur pour le temps peuvent ou non faire référence à une ligne de sous-traitance pour le temps. Si une ligne de facture fournisseur pour les catégories de dépenses fait référence à un sous-contrat, les chefs de projet pourront faire correspondre et vérifier le temps facturé par la ligne de facture fournisseur par rapport au temps enregistré par des sous-traitants et approuvées par les chefs de projet sur le projet.

Le tableau suivant fournit des informations sur les champs des lignes de facture fournisseur pour le temps.

| Champ | Description | Impact fonctionnel |
| --- | --- | --- |
| Nom  | Le nom de la ligne de facture fournisseur, pour aider à l’identification. | Ce nom apparaît dans la première colonne de toutes les recherches basées sur les lignes de facture fournisseur. |
| Description | Brève description des services facturés par le fournisseur sur la ligne de facture fournisseur. | None |
| Sous-contrat | Le contrat de sous-traitance pour lequel les services ont été initialement commandés. | Lorsqu’un contrat de sous-traitance est sélectionné pour la facture fournisseur, toutes les lignes de la facture fournisseur héritent de cette sélection. Une facture fournisseur ne peut pas avoir de lignes de facture fournisseur faisant référence à différents contrats de sous-traitance. |
| Ligne de sous-traitance | La ligne de sous-traitance pour lequel les services ont été commandés. La liste des lignes de contrat de sous-traitance sélectionnables est limitée aux lignes du contrat de sous-traitance sélectionné. | Lorsqu’une ligne de sous-traitance est sélectionnée sur une ligne de facture fournisseur pour le temps, les valeurs par défaut des champs **Projet**, **Rôle** et **Ressource réservable** sont renseignés à partir des champs correspondants sur la ligne de sous-traitance. Si la ligne de sous-traitance sélectionnée a des valeurs dans les champs **Projet**, **Rôle** et **Réservable**, les valeurs des champs correspondants sur la ligne de facture fournisseur ne peuvent pas différer de ces valeurs. |
| Date de la transaction | La date à laquelle le chiffre réel du coût de la ligne de facture fournisseur sera enregistré sur le projet. | None |
| Classe de transaction | La valeur par défaut est **Temps**. | La valeur **Temps** indique que la ligne de facture fournisseur est utilisée pour enregistrer le montant de la facture du temps du sous-traitant. |
| Project | Le nom du projet pour lequel les services facturés ont été utilisés. | Ce champ est obligatoire et ne peut pas être vide. |
| Task | Le nom de la tâche du projet pour lequel les services facturés ont été utilisés. Ce champ est disponible uniquement si un projet est sélectionné. La sélection d’une tâche de projet est facultative. | Si ce champ est laissé vide, le chef de projet peut associer la ligne de facture fournisseur au temps enregistré par les ressources de sous-traitance sur n’importe quelle tâche du projet. Si la ligne de facture fournisseur ne fait pas référence à une ligne de contrat de sous-traitance et que ce champ est laissé vide, le chiffre réel du coût créé par la ligne de facture fournisseur ne sera pas associé à des chiffres réels de ventes non facturées. Dans ce cas, si la facturation à la tâche est mise en place, les frais ne pourront pas être facturés au client final. |
| Role | Rôle des ressources de sous-traitance dont le temps est facturé. | Ce champ spécifie le rôle joué par les ressources de sous-traitance dont le temps est facturé sur la facture fournisseur. |
| Ressource pouvant être réservée | Nom du sous-traitant dont le temps est facturé. La sélection d’une ressource réservable est facultative. | Si ce champ est laissé vide, le chef de projet peut associer la ligne de facture fournisseur au temps enregistré par toute ressource appartenant au fournisseur sur la ligne de facture du fournisseur. |
| Quantité | Saisissez le nombre d’heures facturées par le fournisseur sur la ligne de facture. |None |
| Groupe d’unités | La valeur par défaut est le **groupe d’unités Temps**, valeur qui ne peut pas être modifiée. | None |
| Unité | La valeur par défaut de ce champ est l’unité de base en heures à partir du groupe d’unités Temps. Vous pouvez modifier cette valeur pour acheter toute unité du groupe d’unités Temps, comme un jour ou une semaine. | L’association des valeurs **Rôle** et **Unité** est utilisée par défaut ou calculée pour le champ **Prix unitaire** sur la ligne de facture fournisseur. |
| Prix unitaire | Le prix unitaire par défaut utilise la combinaison des valeurs **Rôle** et **Unité** du tarif du projet applicables à la date de transaction de la ligne de facture fournisseur. | Si le tarif du projet applicable est configuré dans une unité différente de celle de l’unité sur la ligne de facture fournisseur, le système utilise la conversion d’unité pour calculer le prix unitaire. |
| Sous-total | Ce champ en lecture seule est calculé de la façon suivante : *Quantité* &times; *Prix unitaire*, si les valeurs sont saisies dans le champ **Quantité** et **Prix unitaire**. Si un ou les deux champs sont vides, vous pouvez entrer une valeur dans ce champ. | None |
| Taxe de vente | Entrez le montant de la taxe de ventes. | None |
| Montant total | Montant total de la ligne de facture fournisseur, taxes comprises. Ce champ est calculé de la façon suivante : *Sous-total* + *Taxe de vente*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
