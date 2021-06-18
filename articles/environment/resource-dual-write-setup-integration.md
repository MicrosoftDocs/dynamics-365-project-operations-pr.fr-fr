---
title: Intégration des données de configuration et d’installation Project Operations
description: Cette rubrique fournit des informations sur l’installation et la configuration de mappages à double écriture Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001063"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Intégration des données de configuration et d’installation Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique fournit des informations sur l’intégration en double écriture de Project Operations pour les entités d’installation et de configuration.

## <a name="project-contracts-contract-lines-and-projects"></a>Contrats de projet, lignes de contrat et projets

Les contrats de projet, les lignes de contrat et les projets sont créés dans Dataverse, et synchronisés avec les applications Finance and Operations pour une comptabilité supplémentaire. Les enregistrements de ces entités ne peuvent être créés et supprimés que dans Dataverse. Cependant, des attributs comptables tels que les valeurs par défaut du groupe de taxe de vente et les dimensions financières peuvent être ajoutés à ces enregistrements dans les applications Finance and Operations.

  ![Concepts d’intégration de contrat de projet](./media/1ProjectContract.jpg)

Les prospects, les opportunités et les devis des activités de vente sont suivis dans Dataverse et ne sont pas synchronisés avec les applications Finance and Operations, car il n’y a pas de comptabilité en aval associée à cette activité.

La fonctionnalité de contrat de projet dans Dataverse crée un enregistrement de contrat de projet dans les applications Finance and Operations à l’aide du mappage de table **En-têtes de contrat du projet (salesorders)**. L’enregistrement d’un contrat de projet dans Dataverse démarre également la création d’un enregistrement d’entité client de contrat de projet. Cet enregistrement est synchronisé avec les applications Finance and Operations à l’aide du mappage de table **Source de financement de projet (msdyn\_projectcontractssplitbillingrules)**. Ce mappage synchronise également les ajouts, les mises à jour et les suppressions des clients du contrat de projet. Les pourcentages de facturation fractionnés entre les clients du contrat de projet ne sont maîtrisés que dans Dataverse et ne sont pas synchronisés avec les applications Finance and Operations.

Après la création d’un contrat de projet dans Dataverse, le comptable de projet peut mettre à jour les attributs comptables de ce contrat de projet dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Configuration** > **Afficher la comptabilité par défaut**. Le comptable peut examiner les attributs opérationnels du contrat de projet, tels que la date de livraison demandée et le montant du contrat en sélectionnant l’ID de contrat de projet dans les applications Finance and Operations, qui ouvre l’enregistrement de contrat de projet associé dans Dataverse.

L’entité de projet est synchronisée avec les applications Finance and Operations à l’aide du mappage de table **Projets V2 (msdyn\_projects)**. Le comptable du projet peut :

  - Examiner les projets dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Tous les projets**. 
  - Mettre à jour les attributs comptables du projet dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Configurer** > **Afficher la comptabilité par défaut**.  
  - Passer en revue les attributs opérationnels du projet, tels que les dates de début et de fin estimées, en sélectionnant l’ID du projet dans les applications Finance and Operations, qui ouvre l’enregistrement de projet associé dans Dataverse.

Un projet est associé à un contrat de projet via l’entité **Ligne de contrat du projet**.

Les lignes de contrat de projet dans Dataverse créent une règle de facturation de contrat de projet dans les applications Finance and Operations à l’aide du mappage de table **Lignes de contrat de projet (salesorderdetails)**. Le mode de facturation définit le type de règle de facturation de contrat de projet dans les applications Finance and Operations :

  - Les lignes de contrat de projet avec un mode de facturation du temps et du matériel créent une règle de facturation du temps et du type de matériel.
  - Les lignes de contrat de mode de facturation à prix fixe créent une règle de facturation jalon.

Les lignes de contrat de projet peuvent être examinées par le comptable du projet dans les applications Finance and Operations en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Configuration** > **Afficher la comptabilité par défaut**, et en examinant les détails dans l’onglet **Lignes de contrat**. Le comptable peut également définir des dimensions financières par défaut pour les lignes de contrat du mode de facturation à prix fixe dans cet onglet.

## <a name="billing-milestones"></a>Jalons de facturation

Les lignes de contrat de projet utilisant le mode de facturation à prix fixe sont facturées via des jalons de facturation. Les jalons de facturation sont synchronisés à des transactions en compte de projet dans les applications Finance and Operations à l’aide du mappage de table **Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Intégration des jalons de facturation](./media/2Milestones.jpg)

Le comptable peut examiner les transactions en compte et ajuster les attributs comptables de ces transactions en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Gérer** > **Transactions en compte** ou à **Gestion de projet et comptabilité** > **Tous les projets** > **Gérer** > **Transactions en compte**.

Lorsque vous créez pour la première fois un jalon de facturation pour une ligne de contrat de projet donnée, le système crée automatiquement un projet d’estimation du chiffre d’affaires à prix fixe pour le projet associé à cette ligne de contrat. Les projets d’estimation des revenus à prix fixe peuvent être consultés en accédant à **Gestion de projet et comptabilité** > **Projets d’estimation de revenus à prix fixe**.

### <a name="project-tasks"></a>Tâches du projet

Les tâches de projet sont synchronisées avec les applications Finance and Operations via le mappage de table **Tâches de projet (msdyn\_projecttasks)** à des fins de référence seulement. Les opérations de création, de mise à jour et de suppression ne sont pas prises en charge via les applications Finance and Operations.

  ![Intégration de tâches de projet](./media/3Tasks.jpg)

## <a name="project-resources"></a>Ressources de projet

L’entité **Rôles des ressources de projet** est synchronisée avec les applications Finance and Operations à l’aide du mappage de table **Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories)**. Comme les rôles de ressources dans Dataverse ne sont pas spécifiques à l’entreprise, le système crée automatiquement des enregistrements de rôles de ressources spécifiques à l’entreprise dans les applications Finance and Operations pour toutes les entités juridiques incluses dans le périmètre d’intégration à double écriture.

![Intégration des rôles de ressources](./media/5Resources.jpg)

Les ressources de projet dans Project Operations sont gérées dans Dataverse et ne sont pas synchronisés avec les applications Finance and Operations.

### <a name="transaction-categories"></a>Catégories de transactions

Les catégories de transaction sont gérées dans Dataverse et synchronisées avec les applications Finance and Operations à l’aide du mappage de table **Catégories de transactions du projet (msdyn\_transactioncategories)**. Une fois l’enregistrement de catégorie de transaction synchronisé, le système crée automatiquement quatre enregistrements de catégorie partagée. Chaque enregistrement correspond à un type de transaction dans les applications Finance and Operations et les lie à l’enregistrement de la catégorie de transaction.

![Intégration des catégories de transactions](./media/4TransactionCategories.jpg)

L’utilisation de catégories de transactions pour les estimations et les chiffres réels nécessite que le comptable du projet ou l’administrateur système crée les catégories de projet correspondantes dans chaque entité juridique. Pour plus d’informations, voir [Configurer les catégories de projets](../project-accounting/configure-project-categories.md).
