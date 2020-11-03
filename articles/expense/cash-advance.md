---
title: Paiement en avance
description: Cette rubrique fournit des informations sur les avances de fonds.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075623"
---
# <a name="cash-advance"></a>Paiement en avance

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une avance de fonds permet aux employés d’emprunter de l’argent à leur entreprise avant d’engager des dépenses. Lorsqu’une avance de fonds demandée est approuvée et versée, l’employé peut utiliser l’argent pour les dépenses professionnelles qu’il est sur le point d’engager. 

## <a name="create-and-submit-a-cash-advance-request"></a>Créer et soumettre une demande d’avance de fonds

1. Sous **Mes dépenses** , sélectionnez **Avances de fonds** > **Nouveau** pour créer une avance de fonds. 
2. Sur la page **Nouvelle demande d’avance de fonds** , entrez l’objet de la dépense et sélectionnez l’emplacement où la dépense sera engagée.
3. Saisissez le montant et la devise demandés, puis sélectionnez **Enregistrer**. 
4. Lorsque vous êtes prêt à soumettre la demande d’avance de fonds, sur la page **Demande d’avance de fonds** , sélectionnez **Workflow** > **Envoyer**.

## <a name="modify-a-cash-advance-request"></a>Modifier une demande d’avance de fonds

Vous pouvez modifier une demande d’avance de fonds si elle n’a pas été envoyée pour approbation.

1. Sous **Mes dépenses : avances de fonds** , recherchez et sélectionnez l’avance de fonds à modifier.
2. Sélectionnez **Modifier** , et apportez les modifications nécessaires à la demande d’avance de fonds. 
3. Sélectionnez **Enregistrer et fermer**.


## <a name="view-cash-advance-requests"></a>Afficher les demandes d’avance de fonds
Vous pouvez consulter la liste de toutes les avances de fonds qui sont en projet, soumises, en révision ou payées sous **Mes dépenses : avances de fonds**. 

## <a name="approve-cash-advance-requests"></a>Approuver les demandes d’avance de fonds

Les gestionnaires ou utilisateurs configurés comme approbateurs dans le workflow pourront approuver les avances de fonds qui leur sont envoyées pour examen. 

1. Pour approuver une avance de fonds, sous **Traiter les avances de fonds** , sélectionnez **Avances de fonds pour révision**.
2. Sélectionnez l’avance de fonds à vérifier et sélectionnez **Approuver**.  

## <a name="pay-cash-advances"></a>Payer une avance de fonds 
La procédure suivante est généralement effectuée par un comptable ou un utilisateur disposant d’autorisations de comptabilité.

1. Pour valider les avances de fonds approuvées, sélectionnez **Avances de fonds approuvées** , puis **Payer et transférer**.  
2. Fournissez les détails du journal pour les avances de fonds, puis sélectionnez **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Envoyer une note de frais contre une avance de fonds versée 

Lorsque vous créez et envoyez une note de frais pour l’avance de fonds que vous avez déjà reçue, les dépenses seront automatiquement ajustées par rapport à cette avance. Si votre avance de fonds est supérieure au montant dépensé, vous devez retourner le solde à l’entreprise en utilisant la catégorie de dépense **Retourner les fonds**. Si l’avance de fonds versée par l’entreprise est inférieure au montant que vous avez dépensé, l’entreprise doit vous rembourser le solde. 

### <a name="example"></a>Exemple
Vous prévoyez de voyager pour une conférence de Seattle à New York. Vous créez une demande d’avance de fonds pour 3 000,00 USD, car vous avez estimé le coût du billet de la conférence, des vols, de l’hôtel, des repas et du taxi à environ ce montant. Vous ne serez payé que si votre responsable a approuvé cette demande. Une fois que votre responsable l’a approuvée, l’avance de fonds demandée est payée d’un montant de 3 000,00 USD sur votre compte bancaire. Vous assistez ensuite à la conférence. Après avoir terminé votre voyage, vous constatez que la dépense totale n’était que de 2 790,00 USD. Sélectionnez **Espèces** dans le champ **Mode de paiement** et envoyez vos dépenses de 2 790,00 USD. Le montant de vos dépenses soumis est automatiquement ajusté par rapport à l’avance de fonds de 3 000,00 USD qui vous a été prêtée. Vous devez maintenant un solde de 210,00 USD (3 000,00-2 790,00) à l’entreprise, que vous pouvez lui restituer en utilisant la catégorie de dépense **Retourner les fonds**. 
