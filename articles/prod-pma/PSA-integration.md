---
title: Vue d’ensemble de Project Service Automation
description: Cette rubrique offre des informations sur Dynamics 365 Project Service Automation vers la solution d’intégration Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075881"
---
# <a name="project-service-automation-overview"></a>Vue d’ensemble de Project Service Automation

[!include[banner](../includes/banner.md)]

La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Dynamics 365 Finance et Dynamics 365 Project Service Automation via Common Data Service. Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de projets, les contrats de projet, les projets, les lignes de contrat de projet, les tâches de projets, les catégories de transaction de dépenses, les estimations d’heures et les estimations de dépense depuis Project Service Automation vers Finance.

> [!NOTE]
> - Si vous utilisez la version 7.3.0, vous devez installer KB 4074835. Vous pourrez alors intégrer des projets à prix fixe.
> - Si vous utilisez la version 7.3.0 et si vous importez des transactions de frais à partir de Project Service Automation, vous devez installer KB 4345320 afin d’inclure ces frais dans la facture du projet.
> - Si vous utilisez la version 8.0, vous serez en mesure d’utiliser l’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités.
> - Si vous utilisez la version 8.0.1 ou une version ultérieure, vous pourrez synchroniser les chiffres réels.

Avant de pouvoir intégrer Project Service Automation Finance, vous devez configurer les paramètres d’intégration de Project Service Automation. Pour plus d’informations, consultez [Paramètres d’intégration de Project Service Automation](PSA-parameters.md).

Cette solution d’intégration permet une synchronisation directe dans les scénarios suivants :

- Gérez les contrats de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Créer des projets dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Gérez les lignes de contrat de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Gérez les jalons de lignes de contrat de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Gérez les tâches de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Gérez les catégories de transaction des dépenses dans Finance et synchronisez-les directement de Finance vers Project Service Automation.
- Créer des estimations des heures de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Créer des estimations des dépenses de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.
- Créez les heures de projet, les dépenses et les frais réels dans Project Service Automation, et créez des transactions de projet dans le journal d’intégration de Project Service Automation afin qu’elles soient publiées dans Finance.

## <a name="data-synchronization"></a>Synchronisation des données

L’illustration suivante montre comment les données sont synchronisées dans le cadre de l’intégration entre Project Service Automation et Finance.

> [!NOTE]
> Tous les modèles ne sont pas actuellement disponibles. Les modèles seront publiés au fur et à mesure qu’ils seront terminés.

[![Intégration de Project Service Automation avec Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Configuration requise pour Finance

Pour utiliser la solution d’intégration Project Service Automation vers Finance, vous devez installer Enterprise Edition 7.3 avec Platform update 12 ou version ultérieure.

## <a name="system-requirements-for-project-service-automation"></a>Configuration système requise pour Project Service Automation

Pour utiliser la solution d’intégration Project Service Automation vers Finance, vous devez installer les composants suivants :

- Dynamics 365 Project Service Automation version 9.0.0.0 ou ultérieure
- Solution Prospect en disponibilités pour Dynamics 365 Sales, version 1.14.0.0 (v14) ou version ultérieure
- Solution de Project Service Automation vers Finance pour Dynamics 365 Project Service Automation version 1.0.0.0 ou ultérieure

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installer la solution d’intégration Project Service Automation vers Finance dans votre instance Project Service Automation

Téléchargez la solution d’intégration Project Service Automation vers Finance à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) et suivez les instructions fournies avec la solution.
