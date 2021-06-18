---
title: Synchronisez les estimations de projet directement depuis Project Service Automation vers Finance and Operations
description: Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les estimations d’heures du projet et les estimations de dépense du projet directement à partir de Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999713"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisez les estimations de projet directement depuis Project Service Automation vers Finance and Operations

[!include[banner](../includes/banner.md)]

Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les estimations d’heures du projet et les estimations de dépense du projet directement à partir de Dynamics 365 Project Service Automation vers Dynamics 365 Finance.

> [!NOTE]
> - L’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.
> - L’intégration des chiffres réels est disponible à partir de la version 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de données pour Project Service Automation vers Finance

La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance. Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de données sur les estimations heures et dépenses du projet de Project Service Automation vers Finance.

L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.

[![Flux de données pour l’intégration de Project Service Automation avec Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimations des heures du projet

### <a name="template-and-tasks"></a>Modèle et tâches

Pour accéder aux modèles disponibles, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.

Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser les estimations en heures du projet de Project Service Automation vers Finance :

- **Nom du modèle dans l’intégration de données :** Estimations d’heures du projet (PSA vers Fin and Ops)
- **Nom des tâches dans le projet :**

    - Relations des transactions
    - Estimations de dépenses

### <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation | Finances                                       |
|----------------------------|-----------------------------------------------|
| Tâches du projet              | Entité d’intégration pour les estimations d’heures de projet |

### <a name="entity-flow"></a>Flux d’entité

Les estimations d’heures du projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que prévisions d’heures du projet.

### <a name="prerequisites"></a>Conditions préalables

Avant que la synchronisation des estimations des heures de projet puisse avoir lieu, vous devez synchroniser les projets, les tâches de projet et les catégories de transaction de dépenses de projet.

### <a name="power-query"></a>Power Query

Dans le modèle d’estimations d’heures de projet, vous devez utiliser Microsoft Power Query pour Excel pour effectuer ces tâches :

- Définissez l’ID de modèle de prévision par défaut qui sera utilisé lorsque l’intégration crée de nouvelles prévisions horaires.
- Filtrez tous les enregistrements spécifiques aux ressources de la tâche qui échoueront l’intégration dans les prévisions horaires.
- Filtrez toutes les lignes de catégorie de transaction vides. Le fait de ne pas effectuer cette tâche peut entraîner des prévisions horaires incorrectes.

#### <a name="set-the-default-forecast-model-id"></a>Définissez l’ID de modèle de prévision par défaut.

Pour mettre à jour l’ID de modèle de prévision par défaut dans le modèle, cliquez sur la flèche **Carte** pour ouvrir le mappage. Puis, sélectionnez le lien **Requête et filtrage avancés**.

- Si vous utilisez le modèle par défaut Estimations des heures de projet (PSA vers Fin and Ops), dans Power Query, sélectionnez la dernière **Condition insérée** dans la liste des **Étapes appliquées**. Dans l’entrée **Fonction**, remplacez **O\_prévision** avec le nom de l’ID du modèle de prévision qui doit être utilisé avec l’intégration. Le modèle par défaut a un ID de modèle de prévision issu des données de démonstration.
- Si vous créez un nouveau modèle, vous devez ajouter cette colonne. Dans Power Query, sélectionnez **Ajouter une colonne conditionnelle** et entrez un nom pour la nouvelle colonne, tel que **IDModèle**. Entrez la condition pour la colonne, où, si la tâche du projet n’est pas nulle, alors \<enter the forecast model ID\> ; sinon nul.

#### <a name="filter-out-resource-specific-records"></a>Filtrer les enregistrements spécifiques aux ressources

Le modèle d’estimation des heures du projet (PSA vers Fin and Ops) a un filtre par défaut qui supprime tous les enregistrements spécifiques aux ressources. Si vous créez votre propre modèle, vous devez ajouter ce filtre. Sélectionnez le lien **Requête et filtrage avancés** pour filtrer sur la colonne **msdyn\_islinetask** de sorte que seuls les enregistrements **False** sont inclus.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrer toutes les lignes de catégorie de transaction vides

Vous devez ajouter un filtre pour supprimer toutes les lignes contenant des catégories de transaction vides. Cette tâche est requise, que vous utilisiez le modèle par défaut ou que vous créiez votre propre modèle. Ce filtre supprime toutes les lignes récapitulatives de Project Service Automation qui pourraient entraîner des prévisions d’heures dans Finance incorrectes. Sélectionnez le lien **Requête et filtrage avancés** pour filtrer les enregistrements nuls dans la colonne **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Mappage de tâche de modèle dans l’intégration de données](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>les estimations de dépense du projet.

### <a name="template-and-tasks"></a>Modèle et tâches

Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser les estimations de dépense du projet de Project Service Automation vers Finance :

- **Nom du modèle dans l’intégration de données :** Estimations de dépense du projet (PSA vers Fin and Ops)
- **Nom des tâches dans le projet :**

    - Relations des transactions 
    - Estimations de dépenses

### <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation | Finances                                                  |
|----------------------------|----------------------------------------------------------|
| Connexions de transactions    | Entité d’intégration pour les relations de transaction du projet |
| Lignes d’estimation             | Entité d’intégration pour les estimations de dépense de projet         |

### <a name="entity-flow"></a>Flux d’entité

Les estimations de dépense du projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que prévisions de dépense du projet.

### <a name="prerequisites"></a>Conditions préalables

Avant que la synchronisation des estimations des dépenses du projet puisse avoir lieu, vous devez synchroniser les projets, les tâches de projet et les catégories de transaction de dépenses de projet.

### <a name="power-query"></a>Power Query

Dans le modèle d’estimations des dépenses du projet, vous devez utiliser Power Query pour effectuer les tâches suivantes :

- Filtrez pour inclure uniquement les enregistrements de ligne d’estimation des dépenses.
- Définissez l’ID de modèle de prévision par défaut qui sera utilisé lorsque l’intégration crée de nouvelles prévisions horaires.
- Transformez les types de facturation.
- Transformez les types de transaction.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrez pour inclure uniquement les lignes d’estimation des dépenses.

Le modèle Estimations des dépenses du projet (PSA vers Fin et Ops) a un filtre par défaut qui inclut uniquement les lignes de dépenses dans l’intégration. Si vous créez votre propre modèle, vous devez ajouter ce filtre. Sélectionnez la tâche **Relations de transaction**, puis cliquez sur la flèche **Carte** pour ouvrir le mappage. Sélectionnez le lien **Requête et filtrage avancés**. Filtrez la colonne **msdyn\_transactiontype1** de manière à n’inclure que **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Définissez l’ID de modèle de prévision par défaut.

Pour mettre à jour l’ID de modèle de prévision par défaut dans le modèle, sélectionnez la tâche **Estimations des dépenses**, puis cliquez sur la flèche **Carte** pour ouvrir le mappage. Sélectionnez le lien **Requête et filtrage avancés**.

- Si vous utilisez le modèle par défaut Estimations des dépenses (PSA vers Fin and Ops), dans Power Query, sélectionnez la première **Condition insérée** de la section **Étapes appliquées**. Dans l’entrée **Fonction**, remplacez **O\_prévision** avec le nom de l’ID du modèle de prévision qui doit être utilisé avec l’intégration. Le modèle par défaut a un ID de modèle de prévision issu des données de démonstration.
- Si vous créez un nouveau modèle, vous devez ajouter cette colonne. Dans Power Query, sélectionnez **Ajouter une colonne conditionnelle** et entrez un nom pour la nouvelle colonne, tel que **IDModèle**. Entrez la condition pour la colonne, où, si l’ID de ligne d’estimation n’est pas nulle, alors \<enter the forecast model ID\> ; sinon nul.

#### <a name="transform-the-billing-types"></a>Transformer les types de facturation

Le modèle Estimations des dépenses de projet (PSA vers Fin et Ops) comprend une colonne conditionnelle qui est utilisée pour transformer les types de facturation reçus de Project Service Automation lors de l’intégration. Si vous créez votre propre modèle, vous devez ajouter cette colonne conditionnelle. Sélectionnez le lien **Requête et filtrage avancés**, puis sélectionnez **Ajouter une colonne conditionnelle**. Entrez un nom pour la nouvelle colonne, tel que **BillingType**. Puis saisissez la condition suivante :

Si **msdyn\_billingtype** = 192350000, alors **NonChargeable**  
autre si **msdyn\_billingtype** = 192350001, alors **Chargeable**  
autre si **msdyn\_billingtype** = 192350002, alors **Complimentary**  
autre **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformer les types de transaction

Le modèle Estimations des dépenses de projet (PSA vers Fin et Ops) comprend une colonne conditionnelle qui est utilisée pour transformer les types de transaction reçus de Project Service Automation lors de l’intégration. Si vous créez votre propre modèle, vous devez ajouter cette colonne conditionnelle. Sélectionnez le lien **Requête et filtrage avancés**, puis sélectionnez **Ajouter une colonne conditionnelle**. Entrez un nom pour la nouvelle colonne, tel que **TransactionType**. Puis saisissez la condition suivante :

Si **msdyn\_transactiontypecode** = 192350000, alors **Coût**  
autre si **msdyn\_transactiontypecode** = 192350005, alors **Sales**  
autre **null**

### <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

Les illustrations suivantes montrent des exemples de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Mappage des modèles de transactions d’estimation de dépenses](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mappage des modèles d’estimation de dépenses](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]