---
title: Détails de l’en-tête des factures fournisseur
description: Cet article explique la fonctionnalité fournie sur l’en-tête de la facture fournisseur dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929855"
---
# <a name="header-details-for-vendor-invoices"></a>Détails de l’en-tête des factures fournisseur

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article explique la fonctionnalité fournie sur l’en-tête de la facture fournisseur dans Microsoft Dynamics 365 Project Operations.

Lorsque les chefs de projet planifient et exécutent des projets, ils peuvent employer des sous-traitants et acheter des produits et des services auprès de fournisseurs. Au cours de l’exécution d’un projet, des coûts sont encourus à partir des services, des matériaux et des catégories de dépenses qui sont achetés dans le cadre de contrats de sous-traitance avec des fournisseurs. Les fournisseurs facturent ces coûts aux projets en créant des factures fournisseur.

Le tableau suivant fournit des informations sur les champs des en-têtes de facture fournisseur dans Project Operations.

| Champ | Description | Impact fonctionnel |
| --- | --- | --- |
| Nom  | Nom de la facture fournisseur. | Dans toutes les listes déroulantes de factures fournisseur, le nom de la facture fournisseur apparaît dans la première colonne pour vous aider à l’identifier. Par défaut, lorsqu’une facture fournisseur est créée à partir d’un contrat de sous-traitance, le champ **Nom** de la facture fournisseur est défini sur une valeur composée du nom du contrat de sous-traitance et de la date actuelle. |
| Description | Brève description des services et produits facturés sur la facture fournisseur. | None |
| Distributeur | Nom de la société qui facture les produits et services. Cette société doit être un enregistrement de compte dont le type de relation est défini sur **Vendeur** ou **Fournisseur**. | <p>En fonction du fournisseur sélectionné, des valeurs par défaut sont automatiquement saisies dans les champs suivants :</p><ul><li>Devise</li><li>Tarifs</li><li>Modalités de paiement</li><li>Adresse de règlement</li></ul> |
| Sous-contrat | Une référence au sous-contrat pour la facture fournisseur. | <p>En fonction du contrat de sous-traitance sélectionné, des valeurs par défaut sont automatiquement saisies dans les champs suivants :</p><ul><li>Devise</li><li>Tarifs</li><li>Modalités de paiement</li><li>Adresse de règlement</li></ul><p>Le contrat de sous-traitance sélectionné sur l’en-tête de la facture fournisseur est renseigné par défaut sur les lignes de la facture fournisseur et ne peut pas y être modifié.</p> |
| Date de facture | Date des chiffres réels du coût qui seront créés lors de la confirmation de la facture fournisseur. | La date de facturation permet également de sélectionner le tarif d’achat correct, soit à partir des tarifs joints au fournisseur concerné, soit à partir des paramètres du projet. |
| Raison du statut | Statut de la facture fournisseur. | <p>Le statut détermine où se trouve la facture fournisseur dans le processus d’entreprise et si elle peut être modifiée. Voici quelques-unes des valeurs disponibles :</p><ul><li>**Brouillon** : la facture fournisseur peut être modifiée.</li><li>**Confirmé** : La facture fournisseur a été vérifiée et confirmée. Impossible de modifier ou de supprimer les factures fournisseur dont le statut est celui-ci.</li><li>**En cours** : La facture fournisseur est en cours d’examen. Possibilité de modifier les factures fournisseur dont le statut est celui-ci, mais impossible de les supprimer.</li><li>**Annulé** : La facture fournisseur a été annulée. Impossible de modifier ou de supprimer les factures fournisseur dont le statut est celui-ci.</li></ul> |
| Devise | Devise dans laquelle le fournisseur facture les produits et services sur la facture fournisseur. | Sur une facture fournisseur faisant référence à un contrat de sous-traitance, la devise de ce contrat est saisie par défaut comme devise de la facture fournisseur. Sur une facture fournisseur qui ne fait pas référence à un contrat de sous-traitance, la valeur par défaut est saisie à partir de l’enregistrement du compte fournisseur et peut être modifiée. Une fois qu’une facture fournisseur est enregistrée, la devise ne peut plus être modifiée. |
| Unité contractante | Division de l’entreprise qui est responsable de la réception des services et/ou des produits du fournisseur. | None |
| Modalités de paiement | Conditions de paiement sur les factures fournisseur émises. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | Les conditions de paiement du contrat de sous-traitance sont copiées sur toutes les factures fournisseur associées à ce contrat de sous-traitance. Les conditions de paiement peuvent être mises à jour si la facture fournisseur est définie sur **Brouillon**. |
| Adresse de règlement | L’adresse du fournisseur à laquelle les paiements doivent être envoyés. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | L’adresse de règlement du contrat de sous-traitance est copiée comme adresse de règlement sur toutes les factures fournisseur créées pour ce contrat de sous-traitance. L’adresse de paiement peut être mise à jour si la facture fournisseur est définie sur **Brouillon**. |
| Sous-total | Si la facture fournisseur n’a pas de lignes, entrez le sous-total de la facture hors taxes. Si la facture fournisseur comporte des lignes, ce champ est en lecture seule. Dans ce cas, le montant affiché correspond au sous-total de toutes les lignes de la facture fournisseur. | None |
| Total des taxes | Si la facture fournisseur n’a pas de lignes, entrez le total des taxes sur le contrat de sous-traitance. Si la facture fournisseur comporte des lignes, ce champ est en lecture seule. Dans ce cas, le montant affiché correspond à la somme des montants de taxe de toutes les lignes de la facture fournisseur. | None |
| Montant total | Ce champ calculé affiche le montant total de la facture fournisseur après taxes. | None |

> [!NOTE]
> Les champs suivants d’une facture fournisseur ne peuvent pas être modifiés une fois la facture fournisseur enregistrée : **Vendeur**, **Sous-traitance**, **Devise**, **Unité contractante** et **Modalités de paiement**. Si des modifications doivent être apportées à ces champs sur une facture fournisseur, vous devez supprimer la facture fournisseur et créer une facture fournisseur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
