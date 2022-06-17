---
title: Gérer une facture pro forma basée sur un projet
description: Cet article fournit des informations sur la façon de gérer et d’utiliser des factures proforma basées sur des projet.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932109"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Gérer une facture pro forma basée sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Dans Dynamics 365 Project Operations, les factures pro forma sont créées sous forme d’extension des factures dans Dynamics 365 Sales. Cependant, le processus de facturation présente de nombreuses différences entre Sales et Project Operations. Par exemple, il n’est pas possible de créer une facture à partir de la page de liste **Factures** dans Project Operations, mais il est possible de le faire dans Sales. Ces différences et extensions sont en place pour prendre en charge les processus de facturation pour des projets différents d’une facture typique pour une commande client.

> [!IMPORTANT]
> En raison de ces différences, n’utilisez pas les factures de manière interchangeable dans Sales et Project Operations.

## <a name="invoice-header"></a>En-tête de facture

Les informations suivantes sont disponibles sur un en-tête de facture pro forma dans Project Operations.

| Champ | Emplacement | Description |
| --- | --- | --- | 
| **Référence facture** | Onglet **Résumé** | La Réf. générée automatiquement lors de la création d’une facture pro forma. Un champ en lecture seule qui verrouillé pour modification. Ce champ sert de référence pour chaque facture pro forma. |
| **Nom** | Onglet **Résumé** | Défini sur le nom du contrat de projet par défaut. Ce champ peut être modifié. | 
| **Devise** | Onglet **Résumé** | Défini sur la devise du contrat de projet par défaut. Un champ en lecture seule qui verrouillé pour modification. |
| **Tarif** | Onglet **Résumé** | Défini sur les tarifs du contrat de projet par défaut. Un champ en lecture seule qui verrouillé pour modification. | 
| **Opportunité** | Onglet **Résumé** | La référence à l’opportunité liée. Un champ en lecture seule qui verrouillé pour modification. | 
| **Contrat** | Onglet **Résumé** | La référence au contrat du projet lié. Un champ en lecture seule qui verrouillé pour modification. | 
| **Client** | Onglet **Résumé** | La référence au contrat du projet lié. Un champ en lecture seule qui verrouillé pour modification. |
| **Description** | Onglet **Résumé** | Le champ de texte qui décrit la facture. Ce champ peut être modifié. | 
| **Facturation à** et champs connexes | Onglet **Résumé** | Les valeurs par défaut sont définies à partir du client du contrat de projet. Ce champ peut être modifié.  | 
| **Statut** | Onglet **Résumé** | Définit les options suivantes : **Actif**, **Fermé**, **Payé** et **Annulé**, et peut être modifié. Les statuts non pris en charge par Project Operations sont **Fermé** et **Annulé**. </br> Le statut est défini sur **Actif** lors de la création de la facture. </br>Le statut doit être défini sur **Payé** seulement après confirmation de la facture.  | 
| **Statut de la facture du projet** | Onglet **Résumé** | Définit les options suivantes : **Brouillon**, **En cours de révision** et **Confirmé**, et peut être modifié. Les factures ayant les statuts **Brouillon** et **En cours de révision** sont modifiables. La facture ne peut pas être modifiée une fois confirmée. | 
| **Montant détaillé** | Onglet **Résumé** | La somme des montants de toutes les lignes de facture après avances et déductions. Un champ en lecture seule qui verrouillé pour modification.  Ce champ est utilisé pour calculer le montant final. | 
| **Remise (%%)** | Onglet **Résumé** | Ce champ est modifiable pour saisir un pourcentage de remise. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. Il s’agit d’un champ non pris en charge.|  
| **Montant de la remise** | Onglet **Résumé** | Ce champ est modifiable pour saisir le montant de la remise. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. Il s’agit d’un champ non pris en charge. |  
| **Montant hors frais de port** | Onglet **Résumé** | Le montant total de la facture après que les remises ont été appliquées. Un champ en lecture seule qui verrouillé pour modification. Ce champ est utilisé pour calculer le montant final.  | 
| **Frais de port** | Onglet **Résumé** | Ce champ est modifiable pour saisir le montant des fais de port. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. Il s’agit d’un champ non pris en charge. |
| **Total des taxes** | Onglet **Résumé** | La taxe totale de toutes les lignes de facture sur la facture. Un champ en lecture seule qui verrouillé pour modification. | 
| **Montant total** | Onglet **Résumé** | La somme du montant après les remises et les taxes. La somme est le montant que le client doit payer. | 

## <a name="project-based-invoice-lines"></a>Lignes de facture basées sur un projet

Dans Project Operations, il y a toujours une ligne de facture pour chaque ligne de contrat de projet. La ligne de facture est créée même s’il n’y a pas de chiffres réels. Les informations suivantes sont disponibles sur une ligne de facture pro forma.

| Champ | Emplacement | Description | 
| --- | --- | --- |
| **Référence facture** | Onglet **Général** | La référence à la Réf. facture. Un champ en lecture seule qui verrouillé pour modification. Le lien de Réf. facture peut être utilisé pour revenir à l’en-tête de la facture. | 
| **Nom** | Onglet **Général** | Le nom de la ligne de facture défini par défaut à partir du nom de la ligne de contrat. Ce champ peut être modifié. |
| **Project** | Onglet **Général** | Le projet sur la ligne de contrat de projet associée. Un champ en lecture seule qui verrouillé pour modification. Le lien du projet peut être utilisé pour accéder au projet. | 
| **Mode de facturation** | Onglet **Général** | Le mode de facturation sur la ligne de contrat de projet associée. Un champ en lecture seule qui verrouillé pour modification. |
| **Montant de la ligne de contrat** | Onglet **Général** | Le montant du contrat sur la ligne de contrat du projet associée. Un champ en lecture seule qui verrouillé pour modification. | 
| **Facturé à ce jour** | Onglet **Général** | La somme des montants de tous les détails de la ligne de facture de cette facture. Un champ en lecture seule qui verrouillé pour modification. | 
| **Montant** | Onglet **Général** | La somme des montants de tous les détails de la ligne de facture facturables de cette facture. Un champ en lecture seule qui verrouillé pour modification. Ce champ est utilisé pour calculer le montant final sur l’en-tête de la facture. | 
| **Télécopie** | Onglet **Général** | La somme des montants de taxes de tous les détails de la ligne de facture de cette ligne de facture. Un champ en lecture seule qui verrouillé pour modification. Ce champ est utilisé pour calculer le montant final des taxes sur l’en-tête de la facture. | 
| **Total final** | Onglet **Général** | La somme des montants totaux (**Taxes + Montants**) de tous les détails de la ligne de facture facturables de cette ligne de facture. Un champ en lecture seule qui verrouillé pour modification. Ce champ est utilisé pour calculer le montant final sur l’en-tête de la facture. |

## <a name="invoice-line-details"></a>Détails de la ligne de facture

Chaque ligne de facture d’une facture de projet comprend les détails de la ligne de facture. Ces détails de ligne sont associés aux chiffres réels de vente non facturés et aux jalons associés à la ligne de contrat référencée par la ligne de facture. Toutes ces transactions sont marquées **Prêt pour la facturation**.

Pour une ligne **Facture de temps et de matériel**, les détails de la ligne de facture sont regroupés par catégories suivantes : **Facturable**, **Non facturable** et **Gratuit** sur la page **Ligne de facture**. Les détails de **Ligne de facturation facturable** s’ajoutent au total de la ligne de facture. **Gratuit** et **Chiffres réels non facturables** ne s’ajoutent pas au total de la ligne de facture.

Pour une ligne **Facture à prix fixe**, les détails de la ligne de facture sont créés à partir des jalons marqués comme **Prêt pour la facturation** sur la ligne de contrat correspondante. Une fois le détail de la ligne de facture créé à partir d’un jalon, le statut de facturation du jalon est mis à jour et devient **Facture client créée**.

### <a name="edit-invoice-line-details"></a>Modifier les détails de ligne de facture

Les champs suivants sont disponibles sur le détail de la ligne de facture associé à un chiffre réel de vente non facturé.

| Champ | Description |
| --- | --- | 
| **Ligne de facture** | Une référence à la **Réf. ligne de facture**. Ce champ est en lecture seule, verrouillé et ne peut pas être modifié. Ce lien peut être utilisé pour revenir à l’en-tête de la facture. | 
| **Description** | Une description du détail de la ligne de facture. Défini par défaut à partir du champ **Commentaires internes** pour **Entrée de temps** et à partir du champ **Description** pour **Entrée de dépenses**. Le champ peut être modifié.| 
| **Description externe** | Une description du détail de la ligne de facture. Défini par défaut à partir du champ **Commentaires externes** pour **Entrée de temps** et du champ **Description** pour **Entrée de dépenses**. Le champ peut être modifié. Cette description peut être utilisée pour déterminer ce qui doit figurer sur la facture imprimée qui sera envoyée au client. Dans Project Operations, une facture pro forma ne dispose pas de toutes les fonctionnalités requises pour configurer les paramètres d’impression d’une facture. | 
| **Date de début** | Il s’agit d’un champ en lecture seule qui est défini par défaut à partir du chiffre réel source. |
| **Project** | Il s’agit d’un champ en lecture seule qui est défini par défaut à partir du chiffre réel source pour le projet sur la ligne de contrat associée. |  
| **Tâche** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |
| **Catégorie de transaction** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Rôle** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |  
| **Ressource réservable** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Société d’allocation de ressources** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Unité d’allocation des ressources** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Quantité** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |  
| **Planification d’unités** | Pour le détail de la ligne de facture relatif au temps, il est toujours défini sur Temps et n’est pas modifiable. Pour les dépenses, il est défini par défaut à partir du chiffre réel de dépense source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Unité** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |  
| **Prix** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |
| **Devise** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Montant** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Taxes** | Défini par défaut à partir d’un chiffre réel source. Le champ peut être modifié.| 
| **Total final** | Un champ calculé, calculé comme **Montant + Taxe**. Un champ en lecture seule qui verrouillé pour modification. | 
| **Type de facturation** | Défini par défaut à partir d’un chiffre réel source. Le champ peut être modifié. Sélectionner **Facturable** ajoute la ligne au total de la ligne de facture. **Gratuit** et **Non facturable** l’exclura du total de la ligne de facture.| 
| **Sélectionner un produit** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |
| **Produit** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Nom du produit** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |  
| **Description du produit hors catalogue** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. |
| **Type de transaction** | Il s’agit d’un champ en lecture seule qui est défini par défaut à partir du chiffre réel source sur **Ventes facturées**. |  
| **Classe de transaction** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | 

Les champs suivants sont disponibles sur un détail de la ligne de facture associé à un jalon.

| Champ | Description |
| --- | --- | 
| **Ligne de facture** | Référence à la **Réf. ligne de facture**. Un champ en lecture seule qui verrouillé pour modification. Le lien peut être utilisé pour revenir à l’en-tête de la facture.  | 
| **Description** | Description du détail de la ligne de facture. Défini par défaut à partir de la description du jalon source. | 
|**Description externe** | Description du détail de la ligne de facture définie par défaut à partir de la description du jalon source. Ce champ peut être utilisé pour déterminer ce qui doit figurer sur la facture imprimée qui sera envoyée au client. Dans Project Operations, une facture pro forma ne dispose pas de toutes les fonctionnalités requises pour configurer les paramètres d’impression d’une facture. | 
| **Date de début** | Défini par défaut à partir de la date de **Jalon** du jalon source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Project** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. |
| **Tâche** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Catégorie de transaction** | Un champ en lecture seule qui verrouillé pour modification. |
| **Rôle** | Un champ en lecture seule qui verrouillé pour modification. | 
| **Ressource pouvant être réservée** | Un champ en lecture seule qui verrouillé pour modification. | 
| **Unité d’allocation des ressources** | Un champ en lecture seule qui verrouillé pour modification. | 
| **Planification d’unités** | Un champ en lecture seule qui verrouillé pour modification. | 
| **Unité** | Un champ en lecture seule qui verrouillé pour modification. | 
| **Tarif** | Défini par défaut à partir du montant du jalon source. Un champ en lecture seule qui verrouillé pour modification. |
| **Devise** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. |
| **Montant** | Défini par défaut à partir du montant du jalon source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Télécopie** | Défini par défaut à partir du montant de taxes du jalon source. Un champ en lecture seule qui verrouillé pour modification. |
| **Total final** | Défini par défaut à partir du montant étendu du jalon source. Le champ peut être modifié. | 
| **Type de facturation** | Toujours défini par défaut sur **Facturable**. Un champ en lecture seule qui verrouillé pour modification. |
| **Type de transaction** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | 
| **Classe de transaction** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | 

## <a name="refresh-invoice-transactions"></a>Actualiser les transactions de facture

Si des chiffres réels sont arrivés après la création de la facture, vous pouvez les inclure sur la facture.

1. Dans la **Vue Réplication de facturation**, marquez les données comme **Prêt pour la facturation**.   
2. Ouvrez la facture pro forma provisoire et, sur le ruban **Actions**, sélectionnez **Actualiser les transactions de ligne de facture**.

  Les détails de la ligne de facture sont créés pour tout chiffre réel révolu et marqué comme **Prêt pour la facturation**, mais qui n’est pas inclus sur la facture.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
