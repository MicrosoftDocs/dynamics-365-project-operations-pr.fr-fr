---
title: Intégration des données de configuration et d’installation Project Operations
description: Cet article fournit des informations sur l’installation et la configuration des mappages à double écriture de Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029149"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Intégration des données de configuration et d’installation Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article fournit des informations sur l’intégration de la double écriture de Project Operations pour l’installation et la configuration des entités.

## <a name="project-contracts-contract-lines-and-projects"></a>Contrats de projet, lignes de contrat et projets

Les contrats de projet, les lignes de contrat et les projets sont créés dans Dataverse et synchronisés avec les applications de finances et d’opérations pour une comptabilité supplémentaire. Les enregistrements de ces entités ne peuvent être créés et supprimés que dans Dataverse. Toutefois, des attributs comptables tels que les valeurs par défaut du groupe de taxe de vente et les dimensions financières peuvent être ajoutés à ces enregistrements dans les applications de finances et d’opérations.

  ![Concepts d’intégration de contrat de projet.](./media/1ProjectContract.jpg)

Les prospects, les opportunités et les devis des activités de vente font l'objet d'un suivi dans Dataverse et ne se synchronisent pas avec les applications de finances et d’opérations, car il n’y a pas de comptabilité en aval associée à cette activité.

La fonctionnalité de contrat de projet dans Dataverse crée un enregistrement de contrat de projet dans les applications de finances et d’opérations à l’aide du mappage de table **En-têtes de contrat de projet (commandes clients)**. L’enregistrement d’un contrat de projet dans Dataverse démarre également la création d’un enregistrement d’entité client de contrat de projet. Cet enregistrement est synchronisé avec les applications de finances et d’opérations à l’aide du mappage de table **Source de financement du projet (msdyn\_projectcontractssplitbillingrules)**. Ce mappage synchronise également les ajouts, les mises à jour et les suppressions des clients du contrat de projet. Les pourcentages de facturation fractionnés entre les clients du contrat de projet ne sont maîtrisés que dans Dataverse et non synchronisés avec les applications de finances et d’opérations.

Après la création d’un contrat de projet dans Dataverse, le comptable du projet peut mettre à jour les attributs comptables de ce contrat de projet dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Configurer** > **Afficher la comptabilité par défaut**. Le comptable peut examiner les attributs de contrat de projet opérationnel, tels que la date de livraison demandée et le montant du contrat en sélectionnant l’ID de contrat de projet dans les applications de finances et d’opérations, ce qui ouvre l’enregistrement de contrat de projet associé dans Dataverse.

L’entité de projet est synchronisée avec les applications de finances et d’opérations à l’aide du mappage de table **Projects V2 (msdyn\_projects)**. Le comptable du projet peut :

  - Passez en revue les projets dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Tous les projets**. 
  - Mettez à jour les attributs comptables du projet dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Configurer** > **Afficher la comptabilité par défaut**.  
  - Passez en revue les attributs de projet opérationnel, tels que les dates de début et de fin estimées, en sélectionnant l’ID de projet dans les applications de finances et d’opérations, ce qui ouvre l’enregistrement de projet associé dans Dataverse.

Un projet est associé à un contrat de projet via l’entité **Ligne de contrat du projet**.

La fonctionnalité Lignes de contrat de projet dans Dataverse crée une règle de facturation de contrat de projet dans les applications de finances et d’opérations à l’aide du mappage de table **Lignes de contrat de projet (salesorderdetails)**. Le mode de facturation définit le type de règle de facturation du contrat de projet dans les applications de finances et d’opérations :

  - Les lignes de contrat de projet avec un mode de facturation du temps et du matériel créent une règle de facturation du temps et du type de matériel.
  - Les lignes de contrat de mode de facturation à prix fixe créent une règle de facturation jalon.

Les lignes de contrat du projet peuvent être examinées par le comptable du projet dans les applications de finances et d’opérations en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Configuration** > **Afficher la comptabilité par défaut**, et en examinant les détails sur l’onglet **Lignes de contrat**. Le comptable peut également définir des dimensions financières par défaut pour les lignes de contrat du mode de facturation à prix fixe dans cet onglet.

## <a name="billing-milestones"></a>Jalons de facturation

Les lignes de contrat de projet utilisant le mode de facturation à prix fixe sont facturées via des jalons de facturation. Les jalons de facturation sont synchronisés pour projeter les transactions de compte dans les applications de finances et d’opérations à l’aide du mappage de carte **Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Intégration de jalons de facturation.](./media/2Milestones.jpg)

Le comptable peut examiner les transactions en compte et ajuster les attributs comptables de ces transactions en accédant à **Gestion de projet et comptabilité** > **Contrats de projet** > **Gérer** > **Transactions en compte** ou à **Gestion de projet et comptabilité** > **Tous les projets** > **Gérer** > **Transactions en compte**.

Lorsque vous créez pour la première fois un jalon de facturation pour une ligne de contrat de projet donnée, le système crée automatiquement un projet d’estimation du chiffre d’affaires à prix fixe pour le projet associé à cette ligne de contrat. Les projets d’estimation des revenus à prix fixe peuvent être consultés en accédant à **Gestion de projet et comptabilité** > **Projets d’estimation de revenus à prix fixe**.

### <a name="project-tasks"></a>Tâches du projet

Les tâches de projet sont synchronisées avec les applications de finances et d’opérations via le mappage de table **Tâches de projet (msdyn\_projecttasks)** à des fins de référence uniquement. Les opérations de création, de mise à jour et de suppression ne sont pas prises en charge via les applications de finances et d’opérations.

  ![Intégration de tâches du projet.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Ressources de projet

L’entité **Rôles des ressources du projet** est synchronisée avec les applications de finances et d’opérations à l’aide du mappage de table **Rôles de ressource de projet pour toutes les entreprises (bookableresourcecategories)** à des fins de référence uniquement. Étant donné que les rôles de ressource dans Dataverse ne sont pas spécifiques à l’entreprise, le système crée automatiquement des enregistrements de rôles de ressource spécifiques à l’entreprise dans les applications de finances et d’opérations pour toutes les entités juridiques incluses dans la portée de l’intégration en double écriture.

![Intégration des rôles des ressources.](./media/5Resources.jpg)

Les ressources de projet dans Project Operations sont conservées dans Dataverse et ne sont pas synchronisés avec les applications de finances et d’opérations.

### <a name="transaction-categories"></a>Catégories de transactions

Les catégories de transactions sont conservées dans Dataverse et synchronisées avec les applications de finances et d’opérations à l’aide du mappage de table **Catégories de transaction de projet (msdyn\_transactioncategories)**. Une fois l’enregistrement de catégorie de transaction synchronisé, le système crée automatiquement quatre enregistrements de catégorie partagée. Chaque enregistrement correspond à un type de transaction dans les applications de finances et d’opérations et les associe à l’enregistrement de catégorie de transaction.

![Intégration de catégories de transaction.](./media/4TransactionCategories.jpg)

L’utilisation de catégories de transactions pour les estimations et les chiffres réels nécessite que le comptable du projet ou l’administrateur système crée les catégories de projet correspondantes dans chaque entité juridique. Pour plus d’informations, voir [Configurer les catégories de projets](../project-accounting/configure-project-categories.md).
