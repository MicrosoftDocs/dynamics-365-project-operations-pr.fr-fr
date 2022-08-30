---
title: Détails d’en-tête pour les contrats de sous-traitance
description: Cet article explique la fonctionnalité fournie sur l’en-tête de sous-traitance dans Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce16b7a968bc7e6904411ae9e021a5ca1839d02e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261414"
---
# <a name="header-details-for-subcontracts"></a>Détails d’en-tête pour les contrats de sous-traitance

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article explique la fonctionnalité fournie sur l’en-tête de sous-traitance dans Dynamics 365 Project Operations.

Un chef de projet planifie et exécute des projets, il peut donc employer des sous-traitants et acheter des produits et des services auprès de fournisseurs. Lorsqu’un chef de projet doit acheter des produits ou des services, il peut créer un contrat de sous-traitance dans Project Operations.

Pour créer un contrat de sous-traitance, procédez comme suit :

1. Dans le volet de navigation, sélectionnez **Contrats de sous-traitance**, puis sur la page **Contrat de sous-traitance**, sélectionnez **Nouveau**.
2. Entrez les informations requises, puis cliquez sur **Enregistrer**.

    Le tableau suivant fournit des informations sur les champs de la page **En-tête du contrat de sous-traitance**.

    | Champ | Description |Impact fonctionnel |
    |---|------|---| 
    | Nom | Le nom du contrat de sous-traitance. | Dans toutes les listes déroulantes du contrat de sous-traitance, le nom du contrat de sous-traitance apparaît dans la première colonne pour vous aider à l’identifier. | 
    | Description | Une brève description des services et des produits qui sont achetés sur le contrat de sous-traitance. | Aucun(e) |
    | Distributeur | Le nom de la société auprès de laquelle les produits et les services sont achetés. Cet enregistrement de compte a un type de relation **Vendeur** ou **Fournisseur**. | En fonction du fournisseur sélectionné, des valeurs par défaut sont automatiquement saisies dans les champs suivants :<br/> **• Devise** </br> **• Tarifs** </br> **• Conditions de paiement**</br> **• Adresse de règlement**</br> **• Adresse de facturation**</br> **• Nom de facturation** </br>**• Gestionnaire de compte fournisseur**|
    | Date de sous-traitance | La date de création du contrat de sous-traitance. | Cette date permet de sélectionner le tarif d’achat correct, soit à partir des tarifs joints au fournisseur concerné, soit à partir des paramètres du projet. |
    | Raison du statut | Le statut du contrat de sous-traitance. | Le statut détermine où se trouve le contrat de sous-traitance dans le processus d’entreprise et s’il peut être modifié. <br/>Les valeurs incluent :<br>• **Brouillon** : le contrat de sous-traitance peut être modifié. Vous ne pouvez modifier que les contrats de sous-traitance définis sur **Brouillon**.<br/>• **Confirmé** : la négociation avec le fournisseur est terminée et le contrat de sous-traitance est approuvé pour livraison. <br/>• **Fermé** : la livraison sur le contrat de sous-traitance est terminée.<br/>• **Annulé** : le contrat de sous-traitance a été annulé et aucune livraison n’est prévue.  | 
    | Devise | La devise d’achat des produits et services. La valeur par défaut est automatiquement saisie à partir du compte fournisseur, mais elle peut être modifiée. | La devise du contrat de sous-traitance permet de sélectionner le tarif d’achat, soit à partir des tarifs joints au fournisseur concerné, soit à partir des paramètres du projet. Des tarifs dans une autre devise ne peuvent pas être associés au contrat de sous-traitance. Le coût du temps, les dépenses et les matériaux que les ressources du fournisseur fournissent à partir de ce contrat de sous-traitance sont enregistrés dans cette devise sur le projet. Une fois l’enregistrement du contrat de sous-traitance réalisé, sa devise n’est plus modifiable.|
    | Unité contractuelle | La division de l’entreprise qui conclut un contrat d’achat ou un contrat de sous-traitance avec le fournisseur. | Aucun(e) |
    | Modalités de paiement | Les conditions de paiement sur les factures fournisseur émises sur ce contrat de sous-traitance. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | Les conditions de paiement du contrat de sous-traitance sont copiées sur toutes les factures fournisseur associées à ce contrat de sous-traitance. Les conditions de paiement peuvent être mises à jour si le contrat de sous-traitance est défini sur **Brouillon**. | 
    | Adresse de règlement | L’adresse du fournisseur à laquelle les paiements doivent être envoyés. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | L’adresse de règlement du contrat de sous-traitance est copiée comme adresse de règlement sur toutes les factures fournisseur créées pour ce contrat de sous-traitance. L’adresse de règlement peut être mise à jour si le contrat de sous-traitance est défini sur **Brouillon**.|
    | Nom de facturation | Le nom de la personne ou de la division de l’entreprise du fournisseur qui enverra la facture. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | La valeur **Nom de facturation** du contrat de sous-traitance est copiée sur toutes les factures fournisseur associées à ce contrat de sous-traitance. Ce champ peut être mis à jour si le contrat de sous-traitance est défini sur **Brouillon**.|
    | Adresse de facturation | L’adresse utilisée sur les factures du fournisseur. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. | Cette adresse est l’adresse de facturation d’origine sur les factures fournisseur créées pour ce contrat de sous-traitance. |
    | Sous-total | Si un contrat de sous-traitance n’a pas de lignes, entrez le sous-total de la commande hors taxes. Si le contrat de sous-traitance comporte des lignes, ce champ est en lecture seule. Le montant affiché correspond au sous-total de toutes les lignes du contrat de sous-traitance. | Aucun(e) |
    | Total des taxes | Si un contrat de sous-traitance n’a pas de lignes, entrez le total des taxes du contrat de sous-traitance. Si le contrat de sous-traitance comporte des lignes, ce champ est en lecture seule. Le montant affiché correspond à la somme des taxes de toutes les lignes du contrat de sous-traitance. | Aucun(e) |
    | Montant total | Ce champ calculé indique le montant total du contrat de sous-traitance, taxes incluses. | Aucun(e) |
    | Date confirmée | La date de confirmation du contrat de sous-traitance. | Aucun(e) |
    | Demandé par | Par défaut, ce champ est défini sur le nom de l’utilisateur qui crée le contrat de sous-traitance. Toutefois, le créateur du contrat de sous-traitance peut modifier la valeur pour indiquer le nom de la personne pour laquelle il crée ce contrat. | Aucun(e) |
    | Gestionnaire de compte fournisseur | Le nom du contact principal du compte fournisseur. La valeur par défaut est automatiquement entrée à partir de l’enregistrement de compte fournisseur. Vous pouvez sélectionner un contact différent en tant que gestionnaire de compte fournisseur du contrat de sous-traitance. | Vous pouvez configurer des alertes par e-mail pour informer le contact en cas de modification du contrat de sous-traitance suite à des négociations de prix. |
