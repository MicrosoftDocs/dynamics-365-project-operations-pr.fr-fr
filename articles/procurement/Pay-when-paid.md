---
title: Payer quand les paiements des fournisseurs sont payés
description: Ce sujet explique comment utiliser le scénario Payer quand payé.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525334"
---
# <a name="pay-when-paid-vendor-payments"></a>Payer quand les paiements des fournisseurs sont payés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Ce sujet explique comment utiliser le scénario Payer quand payé.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Créer un bon de commande avec des termes Payer quand payé

Lorsque vous validez une facture d’un fournisseur, si le fournisseur est soumis aux conditions de paiement Payer quand payé, ces conditions sont affichées sur les lignes du bon de commande. Pour créer un bon de commande avec conditions de paiement Payer quand payé, procédez comme suit.

1. Dans Microsoft Dynamics 365 Finance, effectuez une ou plusieurs des opérations suivantes :

    - Accédez à **Achats et approvisionnement** \> **Commandes fournisseur** \> **Toutes les commandes fournisseur**. Dans le volet Actions, sélectionnez **Nouveau**. Dans la boîte de dialogue **Créer un bon de commande**, sélectionnez le fournisseur pour lequel les conditions Payer quand payé sont configurés sur le projet, entrez les autres informations requises, puis sélectionnez **OK**.
    - Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**. Dans le volet Actions, sur l’onglet **Gérer**, sélectionnez **Tâche de l’article**. Sélectionnez la commande achat. Sélectionnez le fournisseur pour lequel les conditions Payer quand payé sont configurés sur le projet, puis sélectionnez **OK**.

2. Sur la page **Bon de commande**, sur le raccourci **Lignes de bon de commande**, sélectionnez **Ajouter une ligne** pour créer une ligne de bon de commande.
3. Sélectionnez le numéro d’article ou la catégorie d’approvisionnement et entrez les autres détails requis. Vérifiez les détails de la ligne de commande du fournisseur.

    L’option **Payer quand payé** est automatiquement sélectionnée et la valeur du champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** est automatiquement copiée à partir du champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** sur la page **Projets**.

4. Si vous ne souhaitez pas appliquer les conditions Payer quand payé au fournisseur pour une ligne de bon de commande, désactivez l’option **Payer quand payé**. Dans ce cas, le champ **Pourcentage minimal de mise en œuvre de la clause Payer quand payé** de la ligne de bon de commande sera réinitialisé à **0** (zéro).
5. Dans le volet Actions, sous l’onglet **Commande fournisseur**, dans le groupe **Actions**, cliquez sur **Confirmer** pour confirmer la commande fournisseur.
6. Dans le volet Actions, sur l’onglet **Facture**, sélectionnez **Facture** pour générer la facture pour la commande.

## <a name="create-a-project-invoice-proposal"></a>Créer une proposition de facture pour un projet

Les propositions de facture de projet sont utilisées pour créer des factures de projet pour le client. Dans le scénario Payer quand payé, les paiements fournisseur dépendent des paiements client selon les paramètres Payer quand payé. Cependant, il existe des options qui vous permettent de débloquer les paiements sans les paiements des clients selon vos besoins. Pour créer une facture de projet pour le client, procédez comme suit.

1. Dans les applications d’engagement client, accédez à **Projet** \> **Projets**, et sélectionnez le projet.
2. Sur l’onglet **Chiffres réels**, sélectionnez la ligne réelle qui est générée par le bon de commande avec une transaction de type **Ventes non facturées**. Sélectionnez ensuite **Prêt pour facture**.
3. Accédez à **Ventes** \> **Ventes** \>**Contrat de projet** et sélectionnez le contrat de projet.
4. Sur le volet Actions, sélectionnez **Facture** pour générer la facture client.
5. Dans Finance, accédez à **Gestion de projet et comptabilité** \> **Périodique** \> **Importer depuis la table intermédiaire**, et sélectionnez **OK** pour générer l’intégration de Project Operations.
6. Accédez à **Gestion de projet et comptabilité** \> **Factures de projet** \> **Proposition de facture de projet** et sélectionnez **Valider** pour valider la proposition de facture générée pour le projet.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Mettre à jour un paiement client et payer le fournisseur

Lorsqu’un fournisseur termine son travail sur un projet et vous envoie une facture, vous devez examiner le statut du projet et les factures client pour déterminer si les conditions de paiement Payer quand payé ont été respectées pour le projet. Si les conditions de paiement Payer quand payé du fournisseur ont été respectées, vous pouvez déterminer les lignes de la facture fournisseur à payer, en fonction des paiements client pour le projet. Si vous décidez de payer le fournisseur même si les conditions de paiement Payer quand payé n’ont pas été respectées, vous pouvez remplacer les conditions de paiement Payer quand payé sur la page **Facture fournisseur avec clause Payer quand payé**.

1. Dans Finance, accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Tous les projets** et sélectionnez le projet.
2. Dans le volet Actions, sélectionnez **Contrôler**, puis sélectionnez **Factures fournisseurs** pour afficher toutes les factures fournisseur qui ont été générées pour le projet.
3. Sur la page **Facture fournisseur avec clause Payer quand payé**, dans le champ de recherche, saisissez des valeurs pour trouver la facture fournisseur que vous souhaitez consulter, puis sélectionnez **Rechercher**.
4. Sélectionnez l’option **Payer quand payé** pour afficher uniquement les factures Payer quand payé.
5. Sur le raccourci **Lignes de facture fournisseur**, sélectionnez les lignes que vous souhaitez débloquer pour paiement.
6. Sélectionnez **Débloquer le paiement fournisseur**. L’option **Payer quand payé** est désactivée et la valeur du champ **Prêt à payer** est remplacée par **Oui**.
