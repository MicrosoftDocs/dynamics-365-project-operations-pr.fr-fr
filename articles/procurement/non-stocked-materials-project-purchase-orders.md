---
title: Commander des matériaux non stockés pour un projet à l’aide des bons de commande de projet
description: Cette rubrique explique comment commander des matériaux non stockés pour un projet à l’aide des bons de commande de projet.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563019"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Commander des matériaux non stockés pour un projet à l’aide des bons de commande de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Le service des achats de votre organisation peut utiliser les [bons de commande](/dynamics365/supply-chain/procurement/purchase-order-overview) pour suivre les commandes de biens et services. Des bons de commande pour des matériaux non stockés peuvent être attribués à un projet. La facturation de ces bons de commande enregistre le coût par rapport au projet.

## <a name="prerequisites"></a>Conditions préalables
Effectuez les étapes suivantes pour activer la fonctionnalité de bons de commande de projet.

1. Dans Dynamics 365 Finance, accédez à l’espace de travail **Gestion des données**.
2. Dans la liste des fonctionnalités, recherchez et sélectionnez la fonctionnalité **Activer les bons de commande de projet sur Project Operations pour les scénarios basés sur les ressources/non stockés**.
3. Sélectionnez **Activer**.
4. Configurez les matériaux non stockés et les factures fournisseur en attente comme décrit dans [Configurer les matériaux non stockés et les factures fournisseur en attente](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Créer un bon de commande de projet à partir de la liste des bons de commande de projet

1. Dans Finance, accédez à **Gestion et comptabilité des projets** > **Projets** > **Tous les projets** et sélectionnez un projet.
2. Dans le volet Actions, sous l’onglet **Gérer**, dans le groupe **Nouveau**, sélectionnez **Tâche article** > **Bon de commande**.
3. Dans la page **Créer un bon de commande**, sélectionnez le fournisseur auprès duquel vous souhaitez passer la commande, saisissez les autres informations, le cas échéant, puis cliquez sur **OK**.
4. Dans la page **Bon de commande**, dans la grille **Lignes de commande fournisseur**, sélectionnez **Ajouter une ligne**.
5. Entrez un numéro d’article, une quantité, une unité, un prix unitaire et les autres informations, le cas échéant.

    > [!NOTE]
    > Seuls les articles et services non stockés peuvent être utilisés avec les bons de commande de projet. Les articles stockés et les catégories d’approvisionnement ne sont pas pris en charge.

6. Continuez à ajouter des articles au besoin et confirmez le bon de commande.

    Les accusés de réception de biens et services peuvent être enregistrés en créant et en validant un accusé de réception de marchandises.

    > [!NOTE]
    > Les réceptions de marchandises ne sont pas enregistrées dans les données réelles du projet dans Microsoft Dataverse et n’ont pas d’impact sur le livre auxiliaire du projet.

    Une fois qu’un fournisseur a envoyé la facture pour les articles et services du bon de commande, le service des achats peut générer une facture pour le bon de commande en accédant à **Facture** > **Générer** > **Facture** dans le volet Actions. Pour plus d’informations sur les factures fournisseur en attente, voir [Acheter des matériaux non stockés à l’aide d’une facture fournisseur en attente](pending-vendor-invoices.md).
