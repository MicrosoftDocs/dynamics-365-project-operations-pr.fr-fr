---
title: Synchroniser les catégories de dépenses de projet entre Finance and Operations et Project Service Automation
description: Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les catégories de dépense du projet entre Microsoft Dynamics 365 Finance et Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289636"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchroniser les catégories de dépenses de projet entre Finance and Operations et Project Service Automation

[!include[banner](../includes/banner.md)]

Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les catégories de dépense du projet entre Dynamics 365 Finance et Dynamics 365 Project Service Automation.

> [!NOTE]
> - L’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.
> - L’intégration des chiffres réels est disponible à partir de la version 8.0.1.
> - Si vous utilisez Enterprise Edition 7.3.0 après avoir installé KB 4132657 et KB 4132660, vous pourrez utiliser les modèles pour intégrer des tâches de projet, des catégories de transaction de dépenses, des estimations d’heures, des estimations de dépenses et des chiffres réels, et pour configurer verrouillage des fonctionnalités. Si vous devez réinitialiser les répartitions comptables, nous vous recommandons d’installer également KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Flux de données pour Project Service Automation et Finance

La solution d’intégration Project Service Automation et Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance. Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de données sur les catégories de transaction de dépense entre Finance et Project Service Automation.

Si les catégories de dépenses de projet sont maîtrisées dans Finance, le flux d’intégration passe d’abord de Finance à Project Service Automation. Les ID d’intégration des catégories de dépenses du projet sont ensuite mis à jour via la synchronisation de Project Service Automation vers Finance.

Si les catégories de dépenses de projet sont maîtrisées dans Project Service Automation, le flux d’intégration passe d’abord de Project Service Automation vers Finance. Les catégories de projet doivent déjà être configurées dans Finance avant la synchronisation à partir de Project Service Automation. Ensuite, synchronisez de nouveau de Finance vers Project Service Automation, puis à nouveau de Project Service Automation vers Finance. De cette manière, vous garantissez que les catégories sont liées et qu’aucun doublon n’est créé.

> [!NOTE]
> En règle générale, les catégories de dépenses de projet sont maîtrisées dans Finance. Toutefois, si ce n’est pas le cas, ou si des catégories de dépenses ont déjà été créées dans Project Service Automation, vous devez d’abord effectuer la synchronisation à l’aide du modèle Catégories de transaction de dépenses de projet (PSA vers Fin et Ops). Ensuite, synchronisez à l’aide du modèle Catégories de transaction de dépenses de projet (Fin et Ops vers PSA). Vous devez ensuite exécuter à nouveau la synchronisation de Project Service Automation vers Finance.
>
> Si vous synchronisez d’abord à partir de Project Service Automation, les conditions suivantes doivent être remplies dans Finance avant l’exécution de la synchronisation :
>
> - La catégorie partagée qui correspond à la catégorie de projet configurée dans Project Service Automation doit exister et elle doit être activée pour **Projet** et **Dépense**.
> - Pour chaque entité juridique Finance qui doit être intégrée, les catégories de projet suivantes doivent exister :
>
>     - **Catégorie de projet** existe. 
>     - **Utiliser dans dépenses** est activé.
>     - **Actif dans le journal** est activé.
>     - **Type de transaction** est réglé sur **Dépense**.

L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.

[![Flux de données pour l’intégration de Project Service Automation avec Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronisation de la catégorie des dépenses du projet de Finance vers Project Service Automation

### <a name="template-and-task"></a>Modèle et tâche

Pour accéder au modèle, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.

Le modèle et la tâche sous-jacente suivants sont utilisés pour synchroniser les catégories de dépense du projet de Finance vers Project Service Automation :

- **Nom du modèle dans l’intégration de données :** Catégories de transaction des dépenses du projet (Fin and Ops vers PSA)
- **Nom de la tâche dans le projet :** Synchroniser les catégories avec PSA

### <a name="entity-set"></a>Ensemble d’entités

| Finances                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entité d’intégration pour les catégories | Catégories de transactions     |

### <a name="entity-flow"></a>Flux d’entité

Les catégories de dépense du projet sont gérées dans Finance, et elles sont synchronisées vers Project Service Automation en tant que catégories de transaction.

### <a name="power-query"></a>Power Query

Lorsque vous synchronisez avec Project Service Automation, vous devez utiliser Microsoft Power Query pour Excel pour définir le type de facturation sur la catégorie de transaction. Le modèle de catégories de transaction de dépenses du projet (Fin and Ops vers PSA) fournit une colonne et un mappage par défaut. Si vous créez votre propre modèle, vous devez ajouter une colonne conditionnelle dans Power Query. Procédez comme suit.

1. Cliquez sur la flèche pour ouvrir le mappage de la tâche des catégories de dépenses du projet dans le modèle Catégories de transaction de dépenses du projet (Fin and Ops vers PSA).
2. Cliquez sur le lien **Requête et filtrage avancés** pour ouvrir Power Query.
2. Sélectionnez **Ajouter une colonne conditionnelle**.
3. Entrez un nom pour la nouvelle colonne, tel que **BillingType**.
4. Entrez la condition suivante : **si CATEGORYID n’est pas égal à null alors 19235001, sinon null**.
5. Cliquez sur **OK** sur la colonne.
6. Assurez-vous de mapper cette nouvelle colonne sur la page de mappage.

L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Finance vers Project Service Automation.

[![Mappage du modèle Catégorie des dépenses à Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronisation de la catégorie des dépenses du projet de Project Service Automation vers Finance

### <a name="template-and-task"></a>Modèle et tâche

Le modèle et la tâche sous-jacente suivants sont utilisés pour synchroniser les catégories de dépense du projet de Project Service Automation vers Finance :

- **Nom du modèle dans l’intégration de données :** Catégories de transaction des dépenses du projet (PSA vers Fin and Ops)
- **Nom de la tâche dans le projet :** Synchroniser les catégories avec Fin Ops

### <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation | Finances                           |
|----------------------------|-----------------------------------|
| Catégories de transactions     | Entité d’intégration pour les catégories |

### <a name="entity-flow"></a>Flux d’entité

Les catégories de dépense du projet sont gérées dans Finance, et elles sont synchronisées vers Project Service Automation en tant que catégories de transaction. La synchronisation vers Finance met à jour la catégorie de projet dans Finance avec l’ID d’intégration depuis Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données.

> [!NOTE]
> Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Mappage du modèle Project Service Automation vers Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]