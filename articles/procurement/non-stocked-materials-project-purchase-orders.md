---
title: Commander des matériaux non stockés pour un projet à l’aide des bons de commande de projet
description: Cet article explique comment commander des matériaux non stockés pour un projet à l’aide des bons de commande de projet.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929809"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Catégories d’approvisionnement des commandes ou matériaux non stockés pour un projet à l’aide des bons de commande de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Le service des achats de votre organisation peut utiliser les [bons de commande](/dynamics365/supply-chain/procurement/purchase-order-overview) pour suivre les commandes de biens et services. Des bons de commande pour les catégories d’approvisionnement ou les matériaux non stockés peuvent être alloués à un projet. La facturation de ces bons de commande enregistre le coût par rapport au projet.

## <a name="prerequisites"></a>Conditions préalables
Effectuez les étapes suivantes pour activer la fonctionnalité de bons de commande de projet.

1. Dans Dynamics 365 Finance, accédez à l’espace de travail **Gestion des fonctionnalités**.
2. Dans la liste des fonctionnalités, recherchez et sélectionnez la fonctionnalité **Activer les bons de commande de projet sur Project Operations pour les scénarios basés sur les ressources/non stockés**.
3. Sélectionnez **Activer**.
4. Configurez les matériaux non stockés et les factures fournisseur en attente comme décrit dans [Configurer les matériaux non stockés et les factures fournisseur en attente](configure-materials-nonstocked.md).
5. Configurez les catégories d’approvisionnement comme décrit dans [Utiliser les catégories d’approvisionnement qui peuvent être utilisées avec les bons de commande de projet et les factures fournisseur en attente](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Créer un bon de commande de projet à partir de la liste des bons de commande de projet

1. Dans Finance, accédez à **Gestion et comptabilité des projets** > **Projets** > **Tous les projets** et sélectionnez un projet.
2. Dans le volet Actions, sous l’onglet **Gérer**, dans le groupe **Nouveau**, sélectionnez **Tâche article** > **Bon de commande**.
3. Dans la page **Créer un bon de commande**, sélectionnez le fournisseur auprès duquel vous souhaitez passer la commande, saisissez les autres informations, le cas échéant, puis cliquez sur **OK**.
4. Dans la page **Bon de commande**, dans la grille **Lignes de commande fournisseur**, sélectionnez **Ajouter une ligne**.
5. Entrez un numéro d’article ou une catégorie d’approvisionnement, une quantité, une unité, un prix unitaire et les autres informations, le cas échéant.

    > [!NOTE]
    > Seuls les catégories d’approvisionnement, les articles et services non stockés peuvent être utilisés avec les bons de commande de projet. Les articles stockés ne sont pas pris en charge.

6. Continuez à ajouter des articles ou des catégories d’approvisionnement, au besoin, et confirmez le bon de commande.

    Les accusés de réception de biens et services peuvent être enregistrés en créant et en validant un accusé de réception de marchandises.

    > [!NOTE]
    > Les réceptions de marchandises ne sont pas enregistrées dans les données réelles du projet dans Microsoft Dataverse et n’ont pas d’impact sur le livre auxiliaire du projet.

    Une fois qu’un fournisseur a envoyé la facture pour les articles et services du bon de commande, le service des achats peut générer une facture pour le bon de commande en accédant à **Facture** > **Générer** > **Facture** dans le volet Actions. Pour plus d’informations sur les factures fournisseur en attente, voir [Acheter des matériaux non stockés à l’aide d’une facture fournisseur en attente](pending-vendor-invoices.md).
