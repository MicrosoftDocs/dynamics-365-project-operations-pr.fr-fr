---
title: Utiliser les catégories d’approvisionnement avec les bons de commande de projet et les factures fournisseur en attente
description: Cet article décrit comment configurer les catégories d’approvisionnement qui peuvent être utilisées avec les bons de commande de projet et les factures fournisseur en attente.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927417"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utiliser les catégories d’approvisionnement avec les bons de commande de projet et les factures fournisseur en attente

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Les acheteurs peuvent créer et mettre à jour les catalogues des articles et services pouvant être utilisés dans les bons de commande de projet et les factures fournisseur en cours. Les [catalogues d’approvisionnement](/dynamics365/supply-chain/procurement/procurement-catalogs) vous offrent un moyen simple de catégoriser les achats sans avoir à configurer et à utiliser un catalogue de produits lancés. Chaque catégorie d’approvisionnement peut être mappée à une catégorie de projet pour les transactions de temps, de dépense ou d’articles. Une fois qu’une facture fournisseur en attente qui utilise une catégorie d’approvisionnement est validée, le système crée des chiffres réels de temps, de dépense ou de matériel de projet, des transactions de projet et des écritures du livre auxiliaire.

## <a name="minimum-version-requirements"></a>Version minimale requise

Les versions suivantes sont requises pour utiliser les catégories d’approvisionnement avec les bons de commande de projet pour les scénarios basés sur les ressources/produits non stockés Microsoft Dynamics 365 Project Operations :

- Solution Project Operations Dataverse, version 4.41.0.45 ou ultérieure
- Environnement Finance and Operations version 10.0.26 ou ultérieure

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Exécutez des cartes à double écriture pour la prise en charge des catégories d’approvisionnement

Veillez à ce que le mappage pour **Entité d’exportation de ligne de facture fournisseur de projet d’intégration de Project Operations msdyn\_projectvendorinvoicelines** utilise la version 1.0.0.4 ou ultérieure.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Activer la clé de fonctionnalité pour les catégories d’approvisionnement

Procédez comme suit pour activer la fonctionnalité pour utiliser les catégories d’approvisionnement avec les bons de commande de projet.

1. Dans Dynamics 365 Finance, ouvrez l’espace de travail **Gestion des fonctionnalités**.
1. Dans la liste des fonctionnalités, recherchez la fonctionnalité **Utiliser les catégories d’approvisionnement dans Project Operations pour les scénarios basés sur les ressources/non stockés**, puis sélectionnez **Activer**.

> [!IMPORTANT]
> Comme condition préalable, vous devez également activer la fonctionnalité **Activer les factures fournisseur en attente sur Project Operations pour les scénarios basés sur les ressources/non stockés**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapper les catégories dans la hiérarchie des catégories d’approvisionnement

Suivez la procédure suivante pour les catégories de projet aux catégories d’approvisionnement dans la hiérarchie **Catégorie d’approvisionnement** :

1. Accédez à **Approvisionnements \> Catégories d’approvisionnement**.
1. Sélectionnez **Modifier la hiérarchie de catégories**.
1. Sélectionnez le nœud de hiérarchie de catégories souhaité, puis, sur l’onglet **Attribuer des catégories de projet**, associez le nœud à la catégorie de projet à partir de la catégorie **Temps**, **Dépense** ou **Projet d’article** (c’est-à-dire la catégorie **Heure par défaut** ou **Dépense par défaut**).
1. Cliquez sur **Enregistrer**.
1. Fermez la page.

> [!NOTE]
> Le mappage d’une catégorie d’approvisionnement à une catégorie de projet est facultatif. Si une catégorie d’approvisionnement n’est pas mappée, le système utilisera la valeur définie dans le champ **Article** dans la section **Valeurs par défaut de la catégorie de projet** sur l’onglet **Project Operations sur Dynamics 365 Customer Engagement** de la page **Paramètres de gestion et comptabilité des projets**.
