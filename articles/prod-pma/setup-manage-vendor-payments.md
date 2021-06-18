---
title: Configurer et utiliser les paiements fournisseur Payer quand payé
description: Cette rubrique explique comment créer des conditions de paiement Payer quand payé afin que vous puissiez débloquer des paiements fournisseur partiels, en fonction des paiements des clients.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: c6f7888f3803b2c83a72bcac4caed1a7d7bc5f65
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997553"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurer et utiliser les paiements fournisseur Payer quand payé

[!include [banner](../includes/banner.md)]

Lorsque vous autorisez un fournisseur à travailler en tant que sous-traitant, vous pouvez souhaiter retenir le paiement dû au fournisseur jusqu’à ce que votre client vous paie pour le projet. Pour prendre en charge ce scénario, vous pouvez configurer des conditions de paiement Payer quand payé lorsque vous configurez le bon de commande avec le fournisseur.

Par exemple, lorsqu’un client paie un montant sur une facture de projet, vous pouvez débloquer tout ou partie du montant de la facture fournisseur. Il vous suffit de configurer des conditions de paiement Payer quand payé qui spécifient que le fournisseur sera payé une fois que vous aurez reçu un pourcentage du paiement correspondant de la part du client. Si vous recevez un paiement partiel de la part d’un client, vous pouvez valider manuellement certaines des factures fournisseur associées afin qu’elles soient payées.

L’exemple suivant décrit le processus lorsque des conditions de paiement Payer quand payé sont utilisées.

## <a name="example"></a>Exemple

Votre organisation s’engage à fournir à un client 100 ordinateurs sur lesquels un logiciel est installé, pour un prix de 150,00 USD par ordinateur. Vous engagez ensuite un fournisseur pour vous fournir les ordinateurs sur lesquels un logiciel est installé. Conformément à l’accord, le client doit approuver la qualité des ordinateurs avant de payer votre organisation. La politique de votre organisation est de retenir le paiement dû aux fournisseurs jusqu’à ce que le client vous ait payé. Par conséquent, vous configurez le projet afin que le pourcentage de paiement Payer quand payé soit 100 %%.

Le fournisseur vous envoie les 100 ordinateurs sur lesquels un logiciel est installé, ainsi qu’une facture d’un montant de 10 000,00 USD. Comme les conditions de paiement Payer quand payé sont définies pour votre projet, vous ne payez pas le fournisseur à la réception des ordinateurs. Au lieu de cela, vous envoyez les ordinateurs au client, accompagnés d’une facture d’un montant de 15 000,00 USD. Le client vérifie les ordinateurs et approuve le montant total de la facture du projet.

Après avoir reçu le paiement intégral du client, vous payez 10 000,00 USD au fournisseur, c’est-à-dire le montant total de la facture fournisseur.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurer les conditions de paiement Payer quand payé pour un projet

Lorsque vous configurez les conditions de paiement Payer quand payé pour un projet, vous devez spécifier, sous forme de pourcentage, le montant minimum qu’un client doit vous payer pour le projet avant que vous ne payiez le fournisseur. Le montant de seuil est automatiquement calculé sur les factures client du projet. Suivez ces étapes pour configurer le pourcentage de seuil pour les conditions de paiement Payer quand payé.

1. Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**.
2. Recherchez et ouvrez le projet pour lequel vous souhaitez configurer les conditions de paiement Payer quand payé.
3. Dans le raccourci **Accords fournisseur**, cliquez sur **Ajouter une ligne**.
3. Dans le champ **Code de compte**, sélectionnez l’une des options suivantes :

    - **Table** – Les conditions de paiement Payer quand payé s’appliquent à un seul fournisseur.
    - **Groupe** – Les conditions de paiement Payer quand payé s’appliquent à tous les fournisseurs d’un groupe de fournisseurs.
    - **Tout** – Les conditions de paiement Payer quand payé s’appliquent à tous les fournisseurs.

4. Si vous avez sélectionné **Table** ou **Groupe** à l’étape précédente, dans le champ **Fournisseur/Groupe de fournisseurs**, sélectionnez le fournisseur ou le groupe de fournisseurs auquel s’appliquent les conditions de paiement Payer quand payé. Si vous avez sélectionné **Tout** à l’étape précédente, le champ **Fournisseur / Groupe de fournisseurs** ne peut pas être modifié.
5. Si des conditions de rétention des fournisseurs sont configurées pour le fournisseur dans le projet, dans le champ **Conditions de rétention des fournisseurs**, sélectionnez l’ID de règle pour les conditions de rétention.
6. Dans le champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé**, entrez le pourcentage de seuil pour le projet. Le pourcentage que vous saisissez pour le projet définit le montant minimum que le client doit vous payer avant que vous ne payiez le fournisseur.

## <a name="create-a-po-that-has-pwp-terms"></a>Créer un bon de commande avec conditions de paiement Payer quand payé

Lorsque vous validez une facture d’un fournisseur, si le fournisseur est soumis aux conditions de paiement Payer quand payé, ces conditions sont affichées sur les lignes du bon de commande. Pour créer un bon de commande avec conditions de paiement Payer quand payé, procédez comme suit.

1. Accédez à **Achats et approvisionnement** \> **Commandes fournisseur** \> **Toutes les commandes fournisseur**.
2. Dans le volet Actions, sélectionnez **Nouveau**. Puis, dans la boîte de dialogue **Créer une commande achat**, entrez les informations requises, puis sélectionnez **OK**.

    Vous pouvez également ouvrir un bon de commande existant dans la page de liste **Toutes les commandes fournisseur**.

4. Sur la page **Bon de commande**, sur le raccourci **Lignes de commande fournisseur**, passez en revue les détails de la ligne de bon de commande pour le fournisseur. L’option **Payer quand payé** est automatiquement sélectionnée et la valeur du champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** est automatiquement copiée à partir du champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** sur la page **Projets**.
6. Si vous ne souhaitez pas appliquer les conditions Payer quand payé au fournisseur pour une ligne de bon de commande, désactivez l’option **Payer quand payé**. Dans ce cas, le champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** de la ligne de bon de commande sera réinitialisé à 0 (zéro).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Mettre à jour un paiement client et payer le fournisseur

Lorsqu’un fournisseur termine son travail sur un projet et vous envoie une facture, vous devez examiner le statut du projet et les factures client pour déterminer si les conditions de paiement Payer quand payé ont été respectées pour le projet. Si les conditions de paiement Payer quand payé du fournisseur ont été respectées, vous pouvez déterminer les lignes de la facture fournisseur à payer, en fonction des paiements client pour le projet. Si vous décidez de payer le fournisseur même si les conditions de paiement Payer quand payé n’ont pas été respectées, vous pouvez remplacer les conditions de paiement Payer quand payé sur la page **Facture fournisseur avec clause Payer quand payé**.

1. Accédez à **Gestion de projet et comptabilité** \> **Recherches et états** \> **Demandes de rétention** \> **Facture fournisseur avec clause Payer quand payé**.
2. Sur la page **Facture fournisseur avec clause Payer quand payé**, dans le champ de recherche, saisissez des valeurs pour trouver la facture fournisseur que vous souhaitez consulter, puis sélectionnez **Rechercher**.
3. Sur le raccourci **Lignes de facture fournisseur**, sélectionnez les lignes que vous souhaitez modifier.
4. Si les conditions **Payer quand payé** sont remplies pour la ligne de facture, sélectionnez **Débloquer le paiement fournisseur**. L’option **Payer quand payé** est désactivée et la valeur du champ **Prêt à payer** est remplacée par **Oui**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]