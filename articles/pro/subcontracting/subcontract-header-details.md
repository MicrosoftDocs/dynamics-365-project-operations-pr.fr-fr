---
title: Détails d’en-tête pour les contrats de sous-traitance
description: Cette rubrique explique la fonctionnalité fournie sur l’en-tête d’un contrat de sous-traitance dans Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323638"
---
# <a name="header-details-for-subcontracts"></a>Détails d’en-tête pour les contrats de sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique explique la fonctionnalité fournie sur l’en-tête d’un contrat de sous-traitance dans Dynamics 365 Project Operations.

Un chef de projet planifie et exécute des projets, il peut donc employer des sous-traitants et acheter des produits et des services auprès de fournisseurs. Lorsqu’un chef de projet doit acheter des produits ou des services, il peut créer un contrat de sous-traitance dans Project Operations.

Pour créer un contrat de sous-traitance, procédez comme suit :

1. Dans le volet de navigation, sélectionnez **Contrats de sous-traitance**, puis sur la page **Contrat de sous-traitance**, sélectionnez **Nouveau**.
2. Entrez les informations requises, puis cliquez sur **Enregistrer**.

    Le tableau suivant fournit des informations sur les champs de la page En-tête d’un contrat de sous-traitance.

    | **Champ** | **Description** |
    | --- | --- | 
    | Nom | Le nom du contrat de sous-traitance. |
    | Description | Une brève description des services et des produits qui sont achetés sur le contrat de sous-traitance. |
    | Distributeur | Le nom de la société auprès de laquelle les produits et les services sont achetés. Cet enregistrement de compte a un type de relation **Vendeur** ou **Fournisseur**. |
    | Date de sous-traitance | La date de création du contrat de sous-traitance. |
    | Raison du statut | Le statut du contrat de sous-traitance. |
    | Devise | La devise dans laquelle les produits et les services sont achetés. La valeur de ce champ provient par défaut du compte fournisseur, mais elle peut être modifiée. Les tarifs utilisés pour les produits et les services sur le contrat de sous-traitance doivent être dans cette devise. Les tarifs dans une autre devise ne peuvent pas être associés au contrat de sous-traitance. Le coût des produits et des services engagés sur ce contrat de sous-traitance sera enregistré sur le projet dans cette devise. |
    | Unité contractuelle | La division de l’entreprise qui conclut un contrat d’achat ou un contrat de sous-traitance avec le fournisseur. |
    | Modalités de paiement | Les conditions de paiement sur les factures fournisseurs qui sont émises sur ce contrat de sous-traitance. La valeur de ce champ provient par défaut de l’enregistrement de compte fournisseur. |
    | Adresse de règlement | L’adresse où le paiement sur les factures fournisseur est envoyé. La valeur de ce champ provient par défaut de l’enregistrement de compte fournisseur. |
    | Nom de facturation | Le nom de la personne ou de la division de l’entreprise du fournisseur qui enverra la facture. La valeur de ce champ provient par défaut de l’enregistrement du compte fournisseur et sera utilisée comme nom du contact principal sur les factures fournisseur créées pour ce contrat de sous-traitance. |
    | Adresse de facturation | L’adresse utilisée sur les factures de ce fournisseur. La valeur de ce champ provient par défaut de l’enregistrement de compte fournisseur. Cette adresse est également utilisée comme adresse de facturation sur les factures fournisseurs créées pour ce contrat de sous-traitance. |
    | Sous-total | Si un contrat de sous-traitance n’a pas de ligne, saisissez une valeur dans ce champ qui indique le sous-total de la commande avant taxes. Si le contrat de sous-traitance comporte des lignes, ce champ est en lecture seule. Le montant affiché est le sous-total de toutes les lignes du contrat de sous-traitance. |
    | Total des taxes | Si un contrat de sous-traitance n’a pas de ligne, saisissez une valeur dans ce champ qui indique les taxes de ce contrat de sous-traitance. Si le contrat de sous-traitance comporte des lignes, ce champ est en lecture seule. Le montant affiché représente la somme de la taxe de toutes les lignes du contrat de sous-traitance. |
    | Montant total |  Ce champ calculé indique le montant total du contrat de sous-traitance, taxes incluses.  |
    | Date confirmée | La date de confirmation du contrat de sous-traitance.  |
    | Demandé par | La valeur de ce champ est par défaut le nom de l’utilisateur qui crée le contrat de sous-traitance. Cette valeur peut être modifiée par le créateur du contrat de sous-traitance pour indiquer la personne au nom de laquelle il crée le sous-contrat.  |
    | Gestionnaire de compte fournisseur | Le nom du contact principal du compte fournisseur. La valeur de ce champ provient par défaut de l’enregistrement de compte fournisseur. Cette valeur de champ peut être modifiée par l’utilisateur pour sélectionner un contact différent en tant que gestionnaire de compte fournisseur du sous-contrat. Les alertes e-mail et les négociations de prix peuvent être paramétrées et envoyées par ce contact. |


