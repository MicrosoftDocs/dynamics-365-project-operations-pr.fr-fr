---
title: Synchronisez les données réelles du projet directement depuis Project Service Automation vers le journal d’intégration de projet pour les enregistrer dans Finance and Operations
description: Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les données réelles du projet directement à partir de Microsoft Dynamics 365 Project Service Automation vers Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075872"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronisez les données réelles du projet directement depuis Project Service Automation vers le journal d’intégration de projet pour les enregistrer dans Finance and Operations

[!include[banner](../includes/banner.md)]

Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les données réelles du projet directement à partir de Dynamics 365 Project Service Automation vers Dynamics 365 Finance.

Le modèle synchronise les transactions de Project Service Automation dans une table intermédiaire dans Finance. Une fois la synchronisation terminée, vous **devez** importer les données de la table intermédiaire dans le journal d’intégration.

> [!NOTE]
> - L’intégration des projets réels est disponible à partir de la version 8.0.1.
> - Si vous utilisez Enterprise Edition 7.3.0 après avoir installé KB 4132657 et KB 4132660, vous pourrez utiliser les modèles pour intégrer des tâches de projet, des catégories de transaction de dépenses, des estimations d’heures, des estimations de dépenses et des chiffres réels, et pour configurer verrouillage des fonctionnalités. Si vous devez réinitialiser les répartitions comptables, nous vous recommandons d’installer également KB 4131710.
> - Si vous utilisez la version 7.3.0 et si vous importez des transactions de frais à partir de Project Service Automation, vous devez installer KB 4345320 afin d’inclure ces frais dans la facture du projet.
> - Si vous saisissez des montants de taxe de vente sur des transactions de temps ou de dépenses dans Project Service Automation, vous devez installer Project Service Automation Mise à jour 7. Sinon, les chiffres réels des taxes ne seront pas liés aux chiffres réels des heures ou des dépenses associés, et ils ne seront pas synchronisés avec Finance. Pour plus d’informations, contacter le support.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de données pour Project Service Automation vers Finance

La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance. Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de données sur les données réelles du projet de Project Service Automation vers Finance.

L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.

[![Flux de données pour l’intégration de Project Service Automation avec Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Chiffres réels du projet depuis Project Service Automation

### <a name="template-and-tasks"></a>Modèle et tâches

Pour accéder aux modèles disponibles, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.

Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser les données réelles du projet de Project Service Automation vers Finance :

- **Nom du modèle dans l’intégration de données :** Chiffres réels du projet (PSA vers Fin and Ops)
- **Nom des tâches dans le projet :**

    - Chiffres réels
    - Connexions de la transaction

### <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation | Finances                                   |
|----------------------------|----------------------------------------------------------|
| Chiffres réels                    | Entité d’intégration pour les chiffres réels du projet                   |
| Connexions de transactions    | Entité d'intégration pour les relations de transaction du projet |

### <a name="entity-flow"></a>Flux d’entité

Les données réelles du projet sont gérées dans Project Service Automation et synchronisées avec le journal d’intégration de projet dans Finance. La comptabilité sera appliquée en fonction des dimensions financières par défaut et de la configuration de la comptabilisation.

### <a name="prerequisites"></a>Conditions préalables

Avant que la synchronisation des chiffres réels puisse avoir lieu, vous devez configurer les paramètres d’intégration de Project Service Automation et synchroniser les projets, les tâches de projet et les catégories de transaction de dépenses de projet.

### <a name="power-query"></a>Power Query

Dans le modèle de projets réels, vous devez utiliser Microsoft Power Query pour Excel pour effectuer ces tâches :

- Transformez le type de transaction dans Project Service Automation en le bon type de transaction dans Finance. Cette transformation est déjà définie dans le modèle Chiffres réels du projet (PSA vers Fin and Ops).
- Transformez le type de facturation dans Project Service Automation en le bon type de facturation dans Finance. Cette transformation est déjà définie dans le modèle Chiffres réels du projet (PSA vers Fin and Ops). Le type de facturation est ensuite mappé à la propriété de ligne, en fonction de la configuration sur la page **Paramètres d’intégration de Project Service Automation**.
- Filtrez sur des unités organisationnelles de ressources spécifiques qui doivent être synchronisées avec ce modèle.
- Si le temps intersociétés ou les dépenses réelles intersociétés sont synchronisés avec Finance, vous devez transformer l’unité organisationnelle du contrat en entité juridique appropriée dans Finance. Dans le modèle Chiffres réels du projet (PSA vers Fin and Ops), une colonne conditionnelle est définie en fonction des données de démonstration. Vous devez mettre à jour la dernière colonne conditionnelle insérée avec les entités juridiques appropriées. Sinon, une erreur d’intégration peut se produire ou des transactions réelles incorrectes peuvent être importées dans Finance.
- Si le temps intersociétés ou les dépenses réelles intersociétés ne sont pas synchronisés avec Finance, vous devez supprimer la dernière colonne conditionnelle insérée de votre modèle. Sinon, une erreur d’intégration peut se produire ou des transactions réelles incorrectes peuvent être importées dans Finance.

#### <a name="contract-organizational-unit"></a>Unité organisationnelle de contrat
Pour mettre à jour la colonne conditionnelle insérée dans le modèle, cliquez sur la flèche **Carte** pour ouvrir le mappage. Sélectionnez le lien **Requête et filtrage avancés** pour ouvrir Power Query.

- Si vous utilisez le modèle par défaut Chiffres réels du projet (PSA vers Fin and Ops), dans Power Query, sélectionnez la dernière **Condition insérée** de la section **Étapes appliquées**. Dans l’entrée **Fonction**, remplacez **USSI** avec le nom de l’entité juridique qui doit être utilisée avec l’intégration. Ajoutez des conditions supplémentaires à l’entrée **Fonction** comme vous le souhaitez et mettez à jour la condition **autre** depuis **USMF** vers l’entité juridique appropriée.
- Si vous créez un modèle, vous devez ajouter la colonne pour prendre en charge le temps et les dépenses intersociétés. Sélectionnez **Ajouter une colonne conditionnelle** et entrez un nom pour la colonne, tel que **EntitéJuridique**. Entrez une condition pour la colonne, où, si **msdyn\_contractorganizationalunitid.msdyn\_name** est \<organizational unit\>, alors \<enter the legal entity\> ; sinon nul.

### <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

Les illustrations suivantes montrent un exemple de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Cartographie des modèles - Chiffres réels](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Cartographie des modèles - Connexions de transactions](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importer à partir de la table de préparation après l’intégration à partir de Project Service Automation

Le processus périodique d’importation à partir de la table intermédiaire doit être exécuté après la synchronisation des données réelles de Project Service Automation vers Finance. Ce processus importe les transactions de projet de la table intermédiaire dans le journal d’intégration de Project Service Automation, où la comptabilité est appliquée et les transactions importées peuvent être validées. Nous vous recommandons d’exécuter ce processus en mode traitement ; il peut éventuellement être configuré pour s’exécuter en tant que traitement récurrent.

## <a name="update-actuals-from-finance"></a>Mettre à jour les chiffres réels depuis Finance

### <a name="template-and-tasks"></a>Modèle et tâches

Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser le numéro de pièce justificative et les taxes de vente pour les transactions de projet validées de Finance vers Project Service Automation :

- **Nom du modèle dans l’intégration de données :** mise à jour des chiffres réels du projet (Fin and Ops vers PSA)
- **Nom des tâches dans le projet :**

    - Chiffres réels 
    - Connexions de la transaction

### <a name="entity-set"></a>Ensemble d’entités

| Finances                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entité d’intégration pour les chiffres réels du projet                   | Chiffres réels                    |
| Entité d'intégration pour les relations de transaction du projet | Connexions de transactions    |

### <a name="entity-flow"></a>Flux d’entité

Les données réelles du projet sont gérées dans Project Service Automation et synchronisées avec le journal d’intégration de projet dans Finance. Une fois les chiffres réels validés dans Finance, ils sont mis à jour dans Project Service Automation avec le numéro de pièce justificative de Finance. Si les taxes de vente ont été ajoutées dans Finance, de nouvelles taxes réelles sont créées dans Project Service Automation.

### <a name="power-query"></a>Power Query

Dans le modèle de mise à jour des chiffres réels du projet, vous devez utiliser Power Query pour effectuer ces tâches :

- Transformez le type de transaction dans Finance en le bon type de transaction dans Project Service Automation. Cette transformation est déjà définie dans le modèle de mise à jour des chiffres réels du projet (Fin and Ops vers PSA).
- Transformez le type de facturation dans Finance en le bon type de facturation dans Project Service Automation. Cette transformation est déjà définie dans le modèle de mise à jour des chiffres réels du projet (Fin and Ops vers PSA).

### <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

Les illustrations suivantes montrent des exemples de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Finance vers Project Service Automation.

[![Cartographie des modèles - Mise à jour des chiffres réels](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Cartographie des modèles - Mise à jour des transactions](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
