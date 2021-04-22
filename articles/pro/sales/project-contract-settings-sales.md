---
title: Paramètres de contrat de projet – Simplifié
description: Cette rubrique fournit des informations sur les champs qui ont un impact sur les lignes de contrat et les informations sur le contrat qui sont résumées sur tous les éléments de ligne.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1eedd912bedc43b1d5e847c574b5f1d5233cd038
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663906"
---
# <a name="header-details-for-project-contracts"></a>Détails d’en-tête pour les contrats de projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique fournit des informations sur les champs qui s’appliquent à l’ensemble du contrat de projet, y compris les paramètres qui affectent toutes les lignes de contrat. Sont également incluses des informations sur le contrat qui sont récapitulées sur tous les éléments de ligne pour piloter les indicateurs du contrat de projet.

Le tableau suivant répertorie les champs d’un contrat de projet qui sont propres à Dynamics 365 Project Operations ou qui ont des changements importants dans le comportement des commandes client dans Dynamics 365 Sales.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Type | Onglet **Résumé** (masqué) | Il s’agit d’un champ de groupe d’options qui comporte les options suivantes :</br>- **Basé sur le travail** (disponible uniquement lorsque Project Operations est installé)</br>- **Basé sur l’article** (disponible uniquement lorsque Project Operations et Sales sont installés)</br>- **Service basé sur la maintenance** (disponible lorsque Dynamics 365 Field Service est installé) | Dans Project Operations, la valeur de ce champ est par défaut **Basé sur le travail** et classe le contrat comme un contrat basé sur un projet. Un contrat doit être basé sur un projet pour activer toutes les extensions et fonctionnalités spécifiques au projet. |
| Prospect | Onglet **Résumé** | Référence à la société ou à l’enregistrement de compte du client. Lorsqu’un contrat est créé à partir d’un devis, ce champ est copié à partir du champ correspondant sur l’enregistrement du devis. | La devise du contrat de projet est définie par défaut en fonction de la devise du client. Elle peut être modifiée avant l’enregistrement du contrat. |
| Gestionnaire de comptes | Onglet **Résumé** | Nom du Gestionnaire de compte de cette transaction. Lorsqu’un contrat est créé à partir d’un devis, ce champ est copié à partir du champ correspondant sur l’enregistrement du devis. | Le gestionnaire de compte est responsable de la gestion de la relation avec le client jusqu’à la réalisation du projet. En fonction de l’enregistrement de ressource réservable lié au gestionnaire du compte, l’unité contractuelle utilise par défaut le contrat du projet. |
| Unité contractuelle | Onglet **Résumé** | Unité organisationnelle responsable de la livraison des projets associés à ce contrat. Lorsqu’un contrat est créé à partir d’un devis, ce champ est copié à partir du champ correspondant sur l’enregistrement du devis. | L’unité contractuelle est la division de la société qui exécute les projets. Chaque unité contractuelle dispose d’une devise, et cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant le projet. |
| Tarif des produits | Onglet **Résumé** | Ce tarif est utilisé pour les prix par défaut sur les lignes de contrat basées sur le produit. La liste des options de liste déroulante de ce champ affiche un tarif où la devise correspond à la devise du contrat. Lorsqu’un contrat est créé à partir d’un devis, ce champ est copié à partir du champ correspondant sur l’enregistrement du devis. Sur le contrat du projet, ce champ est défini par défaut en fonction de l’enregistrement de compte, mais peut être modifié. | Aucune pertinence en aval n’est disponible pour ce champ. |
| Devise | Onglet **Résumé** | Devise utilisée pour déclarer la valeur de cette transaction et devise dans laquelle le client sera facturé. Lorsqu’un contrat est créé à partir d’un devis, ce champ est copié à partir du champ correspondant sur l’enregistrement du devis. Sur le contrat du projet, ce champ est défini par défaut en fonction de l’enregistrement de compte, mais peut être modifié. | Une fois un contrat enregistré, ce champ n’est plus modifiable. Ce champ est utilisé pour définir les tarifs de produits et de projets par défaut sur le contrat. La devise présente sur le contrat est utilisée pour correspondre à la devise du tarif. |
| Limite à ne pas dépasser | Onglet **Résumé** | Ce champ indique le plafond négocié sur la valeur finale que le client a accepté pour cette transaction. | Le plafond est évalué lors de l’exécution et s’applique à tous les éléments de ligne et projets associés à cette transaction. |
| Date de livraison demandée | Onglet **Résumé** | Lorsqu’un contrat est créé à partir d’un devis de projet, ce champ est copié à partir du champ correspondant sur le devis de projet. | Cette date est utilisée comme date de fin pour générer des planifications de facture. |

Les indicateurs suivants sont disponibles dans l’onglet **Performance du contrat** d’un contrat de projet.

| Champ | Emplacement | Description |
| --- | --- | --- |
| Valeur du contrat | Contrat d’ensemble | Valeur totale du contrat de projet. |
| Montant facturé | Contrat d’ensemble | Somme des montants sur l’ensemble des factures correspondant à ce contrat. |
| Coût engagé | Contrat d’ensemble | Somme de tous les chiffres réels de coût enregistrés sur l’ensemble des projets mappés au contrat. |
| Marge brute | Contrat d’ensemble | Montant facturé - Coût engagé à ce jour / Montant facturé |
| Marge prévue | Contrat d’ensemble | (Valeur du contrat - Coûts estimés) / Valeur du contrat Coûts estimés = Somme de tous les coûts estimés pour l’ensemble des projets associés au contrat.|
| Valeur du contrat | Lignes selon le projet | Valeur de la ligne de contrat. |
| Montant facturé | Lignes selon le projet | Pour la ligne de contrat à prix fixe : somme des montants de l’ensemble des chiffres réels des jalons de vente facturés par rapport à cette ligne de contrat sur diverses factures créées pour ce contrat. Pour la ligne de contrat du temps et du matériel : somme des montants de l’ensemble des chiffres réels des ventes facturés facturables par rapport à cette ligne de contrat sur diverses factures créées pour ce contrat. |
| Coût engagé | Lignes selon le projet | Somme de tous les chiffres réels de coût enregistrés sur l’ensemble des projets mappés à la ligne de contrat. |
| Marge brute | Lignes selon le projet | (Montant facturé - Coût engagé à ce jour) / Montant facturé |
| Marge prévue | Lignes selon le projet | (Montant de la ligne de contrat dans la devise de base - Coûts estimés pour la ligne de contrat dans la devise de base) / Montant de la ligne de contrat dans la devise de base |
| Coût engagé | Détail d’une ligne basée sur un projet | Temps : somme du montant des chiffres réels de coût des heures enregistrés pour ce rôle sur le projet mappé à la ligne de contrat. Dépenses : somme du montant des chiffres réels de coût des dépenses enregistrés pour cette catégorie sur le projet mappé à la ligne de contrat. |
| Quantité enregistrée | Détail d’une ligne basée sur un projet | Temps : quantité de temps sur l’ensemble des chiffres réels de coût des heures pour un rôle du projet mappé à cette ligne de contrat. Dépenses : toutes les quantités pour cette catégorie de dépenses sur les chiffres réels de coût des dépenses sur le projet sont mappées à cette ligne de contrat. |
| Montant facturé | Détail d’une ligne basée sur un projet | Pour une ligne de contrat à prix fixe, ce champ est laissé vide au niveau de détail et s’affiche uniquement au niveau de la ligne de contrat. Pour une ligne de contrat du temps et du matériel, les calculs sont effectués au niveau de détail. Les détails indiquent la somme du montant de toutes les lignes de revenus facturés par rapport à cette ligne de contrat qui sont facturables. |
| Quantité facturée | Détail d’une ligne basée sur un projet | Pour une ligne de contrat à prix fixe, ce champ est laissé vide au niveau de détail et s’affiche uniquement au niveau de la ligne de contrat. Pour une ligne de contrat du temps et du matériel, les calculs sont effectués au niveau de détail pour le temps et les dépenses. Temps : somme des heures de toutes les lignes de revenus facturés pour ce rôle par rapport à cette ligne de contrat qui sont facturables. Dépenses : toutes les quantités pour cette catégorie de dépenses sur les chiffres réels de coût des dépenses sur le projet sont mappées à cette ligne de contrat. |
| Valeur du contrat | Lignes basées sur le produit | Valeur de la ligne de contrat de cette ligne de contrat basée sur un produit. |
| Montant facturé | Lignes basées sur le produit | Somme des montants de toutes les lignes de facture par rapport à cette ligne de contrat basé sur un produit sur diverses factures créées pour ce contrat. |
| Coût engagé | Lignes basées sur le produit | Somme de tous les chiffres réels de coût enregistrés pour la ligne de contrat basée sur un produit. |
| Marge brute | Lignes selon le projet | Montant facturé - Coût engagé à ce jour / Montant facturé |
| Marge prévue | Lignes basées sur le produit | (Valeur de la ligne de contrat - Coûts estimés de la ligne de contrat) / Valeur de la ligne de contrat |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
