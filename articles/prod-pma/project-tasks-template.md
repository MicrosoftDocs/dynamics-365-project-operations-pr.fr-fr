---
title: Synchroniser les tâches de projet directement de Project Service Automation vers Finance and Operations
description: Cet article décrit le modèle et la tâche sous-jacente utilisés pour synchroniser les tâches de projet directement depuis Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931143"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchroniser les tâches de projet directement de Project Service Automation vers Finance and Operations

[!include[banner](../includes/banner.md)]

Cet article décrit le modèle et la tâche sous-jacente utilisés pour synchroniser les tâches de projet directement depuis Dynamics 365 Project Service Automation vers Dynamics 365 Finance.

> [!NOTE]
> - L’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.
> - Si vous utilisez Enterprise Edition 7.3.0 après avoir installé KB 4132657 et KB 4132660, vous pourrez utiliser les modèles pour intégrer des tâches de projet, des catégories de transaction de dépenses, des estimations d’heures, des estimations de dépenses et des chiffres réels, et pour configurer verrouillage des fonctionnalités. Si vous devez réinitialiser les répartitions comptables, nous vous avons recommandé d’installer également KB 4131710.
> - L’intégration des chiffres réels est disponible à partir de la version 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de données pour Project Service Automation vers Finance

La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance. Le modèle d’intégration disponible avec la fonctionnalité d’intégration de données permet le flux de données sur les tâches du projet de Project Service Automation vers Finance.

L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.

[![Flux de données pour l’intégration de Project Service Automation avec Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Modèle et tâche

Pour accéder au modèle, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.

Le modèle et la tâche sous-jacente suivante sont utilisés pour synchroniser les tâches du projet de Project Service Automation vers Finance :

- **Nom du modèle dans l’intégration de données :** Tâches du projet (PSA vers Fin and Ops)
- **Nom de la tâche dans le projet :** Tâches du projet

Avant que la synchronisation des tâches de projet, vous devez synchroniser les contrats de projet et les projets.

## <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation | Finances                             |
|----------------------------|-------------------------------------|
| Tâches du projet              | Entité d’intégration pour la tâche de projet |

## <a name="entity-flow"></a>Flux d’entité

Les tâches de projet sont géréees dans Project Service Automation et synchronisés vers Finance en tant qu’activités de projet.

## <a name="prerequisites-and-mapping-setup"></a>Prérequis et configuration de mappage

Avant que la synchronisation des tâches de projet, vous devez synchroniser les contrats de projet et les projets.

## <a name="power-query"></a>Power Query

Vous devez utiliser Microsoft Power Query pour Excel pour filtrer les données si la condition suivante est satisfaite :

- Vous avez des enregistrements spécifiques aux ressources dans une tâche de projet.

Si vous devez utiliser Power Query, suivez cette instruction ci-après :

- Le modèle Tâches de projet (PSA vers Fin et Ops) a un filtre par défaut qui exclut les enregistrements spécifiques aux ressources d’une tâche de projet en définissant le filtre **IsLineTask** sur **False**. Si vous créez votre propre modèle, vous devez ajouter ce filtre.

## <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Mappage de modèles.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]