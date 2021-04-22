---
title: Gérer une facture pro forma pour un projet
description: Cette rubrique fournit des informations sur l’utilisation des factures de projet pro forma.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2146e62bddc4a6286fa303ff2cc2c5622ea3133c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866903"
---
# <a name="manage-a-proforma-project-invoice"></a>Gérer une facture pro forma pour un projet 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, les factures pro forma sont créées sous forme d’extension des factures dans Dynamics 365 Sales. Cependant, il existe de nombreuses différences dans le processus de facturation dans Sales et celui de Project Operations. Par exemple, il n’est pas possible de créer une facture à partir de la page **Liste des factures** dans Project Operations, alors que cela est possible dans Sales. Ces différences et extensions existent pour prendre en charge les processus de facturation pour les projets différents d’une facture typique pour une commande client.

> [!IMPORTANT]
> En raison de ces différences, n’utilisez pas les factures de manière interchangeable dans Sales et Project Operations.

## <a name="invoice-header"></a>En-tête de facture

Les informations suivantes sont disponibles sur un en-tête de facture pro forma dans Project Operations.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **ID de facture** | Onglet **Résumé** | La Réf. générée automatiquement lors de la création d’une facture pro forma. Un champ en lecture seule qui verrouillé pour modification. | Ce champ sert de référence pour chaque facture pro forma. |
| **Nom** | Onglet **Résumé** | Défini sur le nom du contrat de projet par défaut. Ce champ est modifiable par l’utilisateur. | &nbsp;  |
| **Devise** | Onglet **Résumé** | Défini sur la devise du contrat de projet par défaut. Un champ en lecture seule qui verrouillé pour modification. |&nbsp; |
| **Tarif** | Onglet **Résumé** | Défini sur les tarifs du contrat de projet par défaut. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Opportunité** | Onglet **Résumé** | La référence à l’opportunité liée. Un champ en lecture seule qui verrouillé pour modification. | &nbsp;  |
| **Contrat** | Onglet **Résumé** | La référence au contrat du projet lié. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Client** | Onglet **Résumé** | La référence au contrat du projet lié. Un champ en lecture seule qui verrouillé pour modification. |&nbsp;  |
| **Description** | Onglet **Résumé** | Le champ de texte qui décrit la facture. Ce champ est modifiable par l’utilisateur. | &nbsp; |
| **Facturation à** et champs connexes | Onglet **Résumé** | Les valeurs par défaut sont définies à partir du client du contrat de projet. Ce champ est modifiable par l’utilisateur.  | &nbsp; |
| **Statut** | Onglet **Résumé** | Définit les options suivantes : **Actif**, **Fermé**, **Payé** et **Annulé**. Modifiable par l’utilisateur. | Les statuts non pris en charge par Project Operations sont **Fermé** et **Annulé**. </br> Le statut est défini sur **Actif** lors de la création de la facture. </br>Le statut doit être défini sur **Payé** seulement après confirmation de la facture. |
| **Statut de la facture du projet** | Onglet **Résumé** | Définit les options suivantes : **Brouillon**, **En cours de révision** et **Confirmé**. Modifiable par l’utilisateur. | Les factures ayant les statuts **Brouillon** et **En cours de révision** sont modifiables. La facture ne peut pas être modifiée une fois confirmée. |
| **Montant détaillé** | Onglet **Résumé** | La somme des montants de toutes les lignes de facture après avances et déductions. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est utilisé pour calculer le montant final. |
| **Remise (%)** | Onglet **Résumé** | Ce champ est modifiable pour saisir un pourcentage de remise. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. | Il s’agit d’un champ non pris en charge. |
| **Montant de la remise** | Onglet **Résumé** | Ce champ est modifiable pour saisir le montant de la remise. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. | Il s’agit d’un champ non pris en charge. |
| **Montant hors frais de port** | Onglet **Résumé** | Le montant total de la facture après que les remises ont été appliquées. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est utilisé pour calculer le montant final. |
| **Frais de port** | Onglet **Résumé** | Ce champ est modifiable pour saisir le montant des fais de port. Ce champ n’est pas pris en charge par la fonctionnalité Project Operations. | Il s’agit d’un champ non pris en charge. |
| **Total des taxes** | Onglet **Résumé** | La taxe totale de toutes les lignes de facture sur la facture. Un champ en lecture seule qui verrouillé pour modification. | Aucune. |
| **Montant total** | Onglet **Résumé** | La somme du montant après les remises et les taxes. | La somme est le montant que le client doit payer. |
## <a name="project-based-invoice-lines"></a>Lignes de facture basées sur un projet

Dans Project Operations, il y a toujours une ligne de facture pour chaque ligne de contrat de projet. La ligne de facture est créée même s’il n’y a pas de chiffres réels. Les informations suivantes sont disponibles sur une ligne de facture pro forma.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **ID de facture** | Onglet **Général** | La référence à la Réf. facture. Un champ en lecture seule qui verrouillé pour modification. | Le lien de Réf. facture peut être utilisé pour revenir à l’en-tête de la facture. |
| **Nom** | Onglet **Général** | Le nom de la ligne de facture défini par défaut à partir du nom de la ligne de contrat. Ce champ est modifiable par l’utilisateur. | &nbsp; |
| **Project** | Onglet **Général** | Le projet sur la ligne de contrat de projet associée. Un champ en lecture seule qui verrouillé pour modification. | Le lien du projet peut être utilisé pour accéder au projet. |
| **Mode de facturation** | Onglet **Général** | Le mode de facturation sur la ligne de contrat de projet associée. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Montant de la ligne de contrat** | Onglet **Général** | Le montant du contrat sur la ligne de contrat du projet associée. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Facturé à ce jour** | Onglet **Général** | La somme des montants de tous les détails de la ligne de facture de cette facture. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Montant** | Onglet **Général** | La somme des montants de tous les détails de la ligne de facture facturables de cette facture. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est utilisé pour calculer le montant final sur l’en-tête de la facture. |
| **Télécopie** | Onglet **Général** | La somme des montants de taxes de tous les détails de la ligne de facture de cette ligne de facture. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est utilisé pour calculer le montant final des taxes sur l’en-tête de la facture. |
| **Total final** | Onglet **Général** | La somme des montants totaux (**Taxes + Montants**) de tous les détails de la ligne de facture facturables de cette ligne de facture. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est utilisé pour calculer le montant final sur l’en-tête de la facture. |


## <a name="invoice-line-details"></a>Détails de la ligne de facture

Chaque ligne de facture d’une facture de projet comprend les détails de la ligne de facture. Ces détails de ligne sont associés aux chiffres réels de vente non facturés et aux jalons associés à la ligne de contrat référencée par la ligne de facture. Toutes ces transactions sont marquées **Prêt pour la facturation**.

Pour une ligne **Facture de temps et de matériel**, les détails de la ligne de facture sont regroupés par catégories suivantes : **Facturable**, **Non facturable** et **Gratuit** sur la page **Ligne de facture**. Les détails de **Ligne de facturation facturable** s’ajoutent au total de la ligne de facture. **Gratuit** et **Chiffres réels non facturables** ne correspondent pas au total de la ligne de facture.

Pour une ligne **Facture à prix fixe**, les détails de la ligne de facture sont créés à partir des jalons marqués comme **Prêt pour la facturation** sur la ligne de contrat correspondante. Une fois le détail de la ligne de facture créé à partir d’un jalon, le statut de facturation du jalon est mis à jour et devient **Facture client créée**.

### <a name="edit-invoice-line-details"></a>Modifier les détails de ligne de facture

Les champs suivants sont disponibles sur un détail de la ligne de facture associé à un chiffre réel de vente non facturé :

| Champ | Description | Impact en aval |
| --- | --- | --- |
| **Ligne de facture** | Une référence à la **Réf. ligne de facture**. Champ en lecture seule, verrouillé pour modification. | Ce lien peut être utilisé pour revenir à l’en-tête de la facture. |
| **Description** | Une description du détail de la ligne de facture. Défini par défaut à partir du champ **Commentaires internes** pour **Entrée de temps** et à partir du champ **Description** pour **Entrée de dépenses**. Le champ est modifiable par l’utilisateur.| &nbsp; |
| **Description externe** | Une description du détail de la ligne de facture. Défini par défaut à partir du champ **Commentaires externes** pour **Entrée de temps** et du champ **Description** pour **Entrée de dépenses**. Le champ est modifiable par l’utilisateur. | Cette description peut être utilisée pour déterminer ce qui doit figurer sur la facture imprimée qui sera envoyée au client. Dans Project Operations, une facture pro forma ne dispose pas de toutes les fonctionnalités requises pour configurer les paramètres d’impression d’une facture. |
| **Date de début** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Ce champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à un chiffre réel source. |
| **Project** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Défini par défaut pour le projet à partir de la ligne de contrat associée. |
| **Tâche** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à un chiffre réel source. Une liste déroulante affiche toutes les tâches associées à la ligne de contrat de projet associée.  |
| **Catégorie de transaction** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une source réelle. |
| **Rôle** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une chiffre réel source. |
| **Ressource pouvant être réservée** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une source réelle. |
| **Unité d’allocation des ressources** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une chiffre réel source. |
| **Quantité** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une chiffre réel source. |
| **Planification d’unités** | Pour le détail de la ligne de facture relatif au temps, il est toujours défini sur Temps et n’est pas modifiable. Pour les dépenses, il est défini par défaut à partir du chiffre réel de dépense source. Un champ en lecture seule qui verrouillé pour modification. | Défini par défaut sur **Temps** sur un nouveau détail de ligne de facture qui n’est pas associé à un chiffre réel. |
| **Unité** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une chiffre réel source |
| **Tarif** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Le champ est modifiable dans un nouveau détail de ligne de facture qui n’est pas associé à une chiffre réel source. Si aucune valeur n’est saisie, elle est définie par défaut après l’action **Enregistrer**. |
| **Devise** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Défini par défaut à partir de l’en-tête de la facture lors de la création d’un nouveau détail de facture sans chiffres réels associés.  Un champ en lecture seule qui verrouillé pour modification. |
| **Montant** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Calculé comme **Quantité \* Prix** lors de la création d’un nouveau détail de facture sans chiffres réels associés. Le calcul est effectué après l’action **Enregistrer**. Un champ en lecture seule qui verrouillé pour modification. |
| **Télécopie** | Défini par défaut à partir d’un chiffre réel source. Le champ est modifiable par l’utilisateur | Le champ peut être modifié par l’utilisateur lors de la création d’un détail de ligne de facture sans chiffres réels associés. |
| **Total final** | Un champ calculé, calculé comme **Montant + Taxe**. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Type de facturation** | Défini par défaut à partir d’un chiffre réel source. Le champ est modifiable par l’utilisateur. | Sélectionner **Facturable** ajoute la ligne au total de la ligne de facture. **Gratuit** et **Non facturable** l’exclura du total de la ligne de facture. |
| **Sélectionner un produit** | Défini par défaut à partir du chiffre réel source, ce champ est en lecture seule. | Lorsque vous créez un nouveau détail de ligne de facture sans chiffre réel de sauvegarde, ce champ peut être modifié. |
| **Produit** | Défini par défaut à partir du chiffre réel source, ce champ est en lecture seule. | Lorsque vous créez un nouveau détail de ligne de facture sans chiffre réel de sauvegarde, ce champ peut être modifié si le champ **Sélectionner un produit** est défini sur **Produit existant**. |
| **Nom du produit** | Défini par défaut à partir du chiffre réel source, ce champ est en lecture seule. | Sur un nouveau détail de ligne de facture, où l’ID de produit est sélectionné dans le catalogue, ce champ est défini sur le nom du produit. Pour un produit hors catalogue, le champ est défini sur le nom du produit hors catalogue. |
| **Description du produit hors catalogue** | Défini par défaut à partir du chiffre réel source, ce champ est en lecture seule. | Lorsque vous créez un nouveau détail de ligne de facture sans chiffre réel de sauvegarde, vous pouvez ajouter une description écrite pour le produit. |
| **Type de transaction** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Défini par défaut sur **Ventes facturées** et verrouillé lors de la création d’un **Détail de la ligne de facture** sans chiffres réels associés.  |
| **Classe de transaction** | Défini par défaut à partir d’un chiffre réel source. Un champ en lecture seule qui verrouillé pour modification. | Défini par défaut selon que l’utilisateur choisit de créer un détail de la ligne de facture **Temps**, **Dépense**, **Matériel** ou **Frais** tout en créant un nouveau **Détail de la ligne de facture** sans chiffre réel de sauvegarde. Verrouillé pour modification. |

Les champs suivants sont disponibles sur un détail de la ligne de facture associé à un jalon :

| Champ | Description | Impact en aval |
| --- | --- | --- |
| **Ligne de facture** | Référence à la **Réf. ligne de facture**. Un champ en lecture seule qui verrouillé pour modification. | Le lien peut être utilisé pour revenir à l’en-tête de la facture. |
| **Description** | Description du détail de la ligne de facture. Défini par défaut à partir de la description du jalon source. | &nbsp; |
|**Description externe** | Description du détail de la ligne de facture définie par défaut à partir de la description du jalon source. | Ce champ peut être utilisé pour déterminer ce qui doit figurer sur la facture imprimée qui sera envoyée au client. Dans Project Operations, une facture pro forma ne dispose pas de toutes les fonctionnalités requises pour configurer les paramètres d’impression d’une facture. |
| **Date de début** | Défini par défaut à partir de la date de **Jalon** du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Project** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Tâche** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Catégorie de transaction** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Rôle** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Ressource pouvant être réservée** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Unité d’allocation des ressources** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Planification d’unités** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Unité** | Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Tarif** | Défini par défaut à partir du montant du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Devise** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. |&nbsp; |
| **Montant** | Défini par défaut à partir du montant du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Télécopie** | Défini par défaut à partir du montant de taxes du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Total final** | Défini par défaut à partir du montant étendu du jalon source. Le champ est modifiable par l’utilisateur | &nbsp; |
| **Type de facturation** | Toujours défini par défaut sur **Facturable**. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Type de transaction** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |
| **Classe de transaction** | Défini par défaut à partir du jalon source. Un champ en lecture seule qui verrouillé pour modification. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Créer des détails de la ligne de facture

Sur les lignes de facture de temps et de matériel, vous pouvez créer des détails de ligne de facture. Ces détails de ligne de facture ne sont pas associés à un chiffre réel. Sur la ligne de facture d’une ligne de facture de temps et de matériel, vous pouvez sélectionner **Nouveau** pour créer un détail de ligne de facture pour les classes de transactions incluses dans la ligne de contrat.

## <a name="refresh-invoice-transactions"></a>Actualiser les transactions de facture

Si des chiffres réels sont arrivés après la création de la facture, vous pouvez les inclure sur la facture.

1. Dans la **Vue Réplication de facturation**, marquez les données comme **Prêt pour la facturation**.   
2. Ouvrez le brouillon de facture pro forma et, sur le ruban **Actions**, cliquez sur **Actualiser les transactions de ligne de facture**.

  Cette action crée des détails de ligne de facture pour tout chiffre réel daté dans le passé et marqué comme **Prêt pour la facturation** ; mais ils ne sont pas inclus dans la facture.

## <a name="product-based-invoice-lines"></a>Lignes de facture basées sur les produits

Dans Project Operations, vous pouvez créer des lignes de facture pour des produits qui ne s’appliquent à aucun projet ou pour tous les projets avec des lignes de facture basées sur le projet. Ces lignes de facture sont créées en tant que lignes de contrat basées sur les produits et une fois marquées comme prêtes pour la facturation, elles sont ajoutées en tant que lignes de factures basées sur les produits.

Une fois des lignes de facture basées sur les produits ajoutées, elles ne sont plus modifiables. Elles peuvent, toutefois, être supprimées de la facture pro forma en mode brouillon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
