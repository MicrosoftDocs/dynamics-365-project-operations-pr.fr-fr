---
title: Projeter les commandes client pour les projets temps et matériels
description: Cette rubrique explique comment créer des commandes client basées sur des projets pour des projets de temps et matériels.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167995"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projeter les commandes client pour les projets temps et matériels

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Cette rubrique décrit comment créer une commande client pour un projet. Les commandes client ne peuvent être créées que pour des projets de type **temps et matériel**.

Si un projet temporel et matériel a plusieurs sources de financement sur le contrat de projet, vous devez activer le paramètre **Autoriser les commandes client pour des projets avec plusieurs sources de financement** sur la page **Gestion de projet et comptabilité**. 

> [!NOTE]
> - La prise en charge des commandes client de projet avec plusieurs sources de financement est disponible à partir de la version 10.0.2 de l’application.
> - Le paramètre permettant d’activer la prise en charge des commandes client de projet avec plusieurs sources de financement sera supprimé dans la vague de publication d’avril 2020, après quoi la fonctionnalité sera toujours activée.

Vous pouvez créer des commandes client basées sur un projet de deux manières :

- Accédez au projet lui-même. Dans le volet Actions, sélectionnez **Gérer > Tâches d’article > Commande client**. Les informations sur le projet seront par défaut la commande client du projet. Si le contrat de projet a plus d’une source de financement, vous devrez sélectionner la source de financement pour définir le client pour la commande client. S’il n’y a qu’une seule source de financement pour le projet, le client sera automatiquement défini.
- Accédez à la page de la liste **Toute commande client** et créez une nouvelle commande client. Vous devrez sélectionner le projet pour la commande client. Une fois le projet sélectionné, le client sera défini à partir de la source de financement ou vous devrez sélectionner la source de financement si le contrat de projet comporte plusieurs sources de financement.

