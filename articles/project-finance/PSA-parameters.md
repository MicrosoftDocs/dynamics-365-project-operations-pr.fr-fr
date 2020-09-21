---
title: Paramètres d’intégration de Project Service Automation
description: Cette rubrique explique comment configurer la saisie des données par défaut lors de l’intégration de Microsoft Dynamics 365 for Project Service Automation avec Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168037"
---
# <a name="project-service-automation-integration-parameters"></a>Paramètres d’intégration de Project Service Automation

[!include[banner](../includes/banner.md)]

Sur la page **Paramètres d’intégration de Project Service Automation**, vous pouvez configurer la manière dont les données par défaut sont saisies lorsque vous intégrez Dynamics 365 Project Service Automation avec Dynamics 365 Finance. Pour que les projets soient correctement synchronisés de Project Service Automation vers Finance, vous devez configurer les champs suivants.

Pour ouvrir la page **Paramètres d’intégration de Project Service Automation**, accédez à **Gestion de projets et comptabilité** \> **Configurer** \> **Paramètres d’intégration de Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - L’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.
> - L’intégration des chiffres réels est disponible à partir de la version 8.0.1.


| Tabulation                    | Champ                | Description |
|------------------------|----------------------|-------------|
| GÉNÉRAL                | Type de projet par défaut | Sélectionnez le type de projet par défaut. Lorsque les projets sont synchronisés à partir de Project Service Automation, cette valeur est utilisée si vous n’avez pas fourni de valeur par défaut dans le modèle d’intégration. Pendant la synchronisation, le champ **Type de projet** des nouveaux projets est défini sur cette valeur. Cependant, la valeur peut être mise à jour lorsque les lignes de contrat de projet sont synchronisées à partir de Project Service Automation. |
|                        | Catégorie de temps        | Sélectionnez la catégorie de temps par défaut. Cette valeur est utilisée lorsque les estimations d’heures sont synchronisées à partir de Project Service Automation. Lorsque les estimations horaires et les heures réelles sont synchronisées à partir de Project Service Automation, le champ **Catégorie** des nouvelles prévisions d’heures de projet dans Finance est défini sur cette valeur. |
|                        | Catégorie de frais         | Sélectionnez la catégorie de frais par défaut. Cette valeur est utilisée lorsque les estimations de frais réels sont synchronisées à partir de Project Service Automation. Lorsque les frais réels sont synchronisés à partir de Project Service Automation, le champ **Catégorie** des nouvelles transactions de frais dans Finance est défini sur cette valeur. |
| Paramètres par défaut du groupe de projets | Type de projet         | Cliquez sur **Nouveau** pour ajouter une ligne dans laquelle vous pouvez sélectionner le type de projet pour lequel définir le groupe de projets par défaut. Un type de projet spécifique ne peut être sélectionné qu’une seule fois dans la configuration. |
|                        | Groupe de projets        | Sélectionnez le groupe de projets par défaut pour le type de projet sélectionné. Lorsque de nouveaux projets sont synchronisés à partir de Project Service Automation, le champ **Groupe de projet** est défini sur la valeur par défaut du type de projet si vous n’avez pas fourni de valeur par défaut dans le modèle d’intégration. |
| Valeurs par défaut du type de facturation  | Type de facturation         | Cliquez sur **Nouveau** pour ajouter une ligne dans laquelle vous pouvez sélectionner le type de facturation pour lequel définir la propriété de ligne par défaut. Un type de facturation spécifique ne peut être sélectionné qu’une seule fois dans la configuration. |
|                        | Propriété de ligne        | Sélectionnez la propriété de ligne par défaut pour le type de facturation sélectionné. Lorsque de nouvelles estimations d’heures, de nouvelles estimations de dépenses ou de nouveaux chiffres réels sont synchronisés à partir de Project Service Automation, le champ **Propriété de ligne** est défini sur la valeur par défaut du type de facturation. |
| Verrouillage de fonctionnalité  | Non applicable       | Sélectionnez la fonctionnalité à désactiver dans Finance pour les projets et les contrats provenant de Project Service Automation. Par exemple, vous pouvez désactiver la possibilité de modifier des contrats et des projets, créer des structures de répartition du travail et saisir des feuilles de temps dans Finance. Les champs liés à la comptabilité continueront d’être activés, même s’ils ne sont pas disponibles par le paramétrage. Par défaut, toutes les fonctionnalités sont activées. |
