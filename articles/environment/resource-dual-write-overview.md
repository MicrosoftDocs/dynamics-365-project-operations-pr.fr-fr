---
title: Intégration à double écriture Project Operations
description: Cette rubrique offre une vue d’ensemble de l’intégration à double écriture Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007908"
---
# <a name="project-operations-dual-write-integration-overview"></a>Vue d’ensemble Intégration à double écriture Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations utilise des [fonctionnalités de double écriture](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pour synchroniser les données sur Microsoft Dataverse et Dynamics 365 Finance.

L’illustration suivante montre comment les données sont synchronisées dans le cadre de cette intégration entre Dataverse et Finance.

![Vue d’ensemble des flux de données Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations sur Dataverse fournit une interface utilisateur moderne et une extensibilité sans code/low-code facile à l’aide de fonctionnalités Power Platform. Les chefs de projet, les gestionnaires de ressources, les membres de l’équipe de projet et d’autres collaborateurs en front-office effectuent leurs activités dans Project Operations sur Dataverse.

Project Operations dans Finance fournit un support à la comptabilité de projet et à la constatation du produit. Project Operations se connecte au cadre financier de Finance pour le calcul de la taxe de vente, les taux de change des devises, les rapports sur les dimensions financières, etc. Les expériences des comptables de projet sont principalement basées dans Finance.

L’intégration Project Operations comprend l’intégration des composants suivants :


- [Intégration des données de configuration et d’installation Project Operations](resource-dual-write-setup-integration.md) 
- [Estimations et chiffres réels de projet](resource-dual-write-estimates-actuals.md)
- [Factures de projet](resource-dual-write-project-invoice.md)
- [Gestion des dépenses](resource-dual-write-expense.md)
- [Facture fournisseur](resource-dual-write-vendor-invoice.md)
