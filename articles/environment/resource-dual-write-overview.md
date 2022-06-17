---
title: Intégration à double écriture Project Operations
description: Cet article fournit une vue d’ensemble de l’intégration à double écriture de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927969"
---
# <a name="project-operations-dual-write-integration-overview"></a>Vue d’ensemble Intégration à double écriture Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations utilise les [fonctionnalités en double écriture](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pour synchroniser les données à travers Microsoft Dataverse et Dynamics 365 Finance.

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
