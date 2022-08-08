---
title: Intégration de la gestion des dépenses
description: Cet article fournit des informations sur l’intégration des notes de frais dans Project Operations à l’aide de la double écriture.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e11f1cfd714212691146eed59bcfb5b5facd750c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029206"
---
# <a name="expense-management-integration"></a>Intégration de la gestion des dépenses

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article fournit des informations sur l’intégration des notes de frais dans le [déploiement complet des dépenses](../expense/expense-overview.md) dans Project Operations à l’aide de la double écriture.

## <a name="expense-categories"></a>Catégories de dépenses

Dans un déploiement complet des dépenses, les catégories de dépenses sont créées et gérées dans les applications de finances et d’opérations. Pour créer une catégorie de dépenses, procédez comme suit :

1. Dans Microsoft Dataverse, créez une catégorie **Transaction**. L’intégration en double écriture synchronisera cette catégorie de transaction avec les applications de finances et d’opérations. Pour plus d’informations, voir [Configurer les catégories de projets](/dynamics365/project-operations/project-accounting/configure-project-categories) et [Intégration des données de configuration et d’installation Project Operations](resource-dual-write-setup-integration.md). Suite à cette intégration, le système crée quatre enregistrements de catégorie partagés dans les applications de finances et d’opérations.
2. Dans Finance, accédez à **Gestion des dépenses** > **Configurer** > **Catégories partagées** et sélectionnez une catégorie partagée avec une classe de transaction **Dépense**. Définissez le paramètre **Peut être utilisé dans les dépenses** sur **Vrai** et définissez le type de dépense à utiliser.
3. À l’aide de cet enregistrement de catégorie partagée, créez une catégorie de dépenses en accédant à **Gestion des dépenses** > **Configurer** > **Catégories de dépenses** et en sélectionnant **Nouveau**. Lorsque l’enregistrement est enregistré, la double écriture utilise le mappage de table, l’**entité d’exportation des catégories de dépenses de projet d’intégration de Project Operations (msdyn\_expensecategories)** pour synchroniser cet enregistrement avec Dataverse.

  ![Intégration des catégories de dépenses.](./media/DW6ExpenseCategories.png)

Les catégories de dépenses dans les applications de finances et d’opérations sont spécifiques à l’entreprise ou à l’entité juridique. Il existe des enregistrements distincts, correspondants et spécifiques à l’entité juridique dans Dataverse. Lorsqu’un chef de projet estime les dépenses, il ne peut pas sélectionner de catégories de dépenses qui ont été créées pour un projet appartenant à une entreprise différente de celle qui possède le projet sur lequel il travaille. 

## <a name="expense-reports"></a>Rapports de dépenses

Les notes de frais sont créées et approuvées dans les applications de finances et d’opérations. Pour plus d’informations, voir [Créer et traiter des notes de frais dans Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Une fois la note de frais approuvée par le chef de projet, elle est enregistrée dans la comptabilité. Dans Project Operations, les lignes de notes de frais liées au projet sont validées à l’aide de règles de validation spéciales :

  - Le coût lié au projet (y compris la taxe non récupérable) n’est pas immédiatement imputé au compte de coût du projet dans la comptabilité, mais est imputé au compte d’intégration des dépenses. Ce compte est configuré dans **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets**, dans l’onglet **Project Operations sur Dynamics 365 Customer engagement**.
  - La double écriture est synchronisée avec Dataverse à l’aide du mappage de table **Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses)**.
  - Le livre auxiliaire fiscal, le livre auxiliaire fournisseur et les autres écritures financières sont enregistrés, en fonction de la situation, au moment de la comptabilisation des notes de frais.

  ![Intégration des notes de frais.](./media/DW6ExpenseReports.png)

Lorsqu’un enregistrement est écrit sur l’entité **Dépense** dans Dataverse, le système déclenche le processus d’approbation automatisé de l’enregistrement. Si nécessaire, le statut du processus d’approbation automatisé peut être révisé dans Dataverse en accédant à **Réglages avancés** > **Système** > **Tâches système**. Une fois l’approbation terminée, les enregistrements de classe de transaction de dépense sont créés dans l’entité **Chiffres réels**.

Les chiffres réels liés aux dépenses sont ensuite traités à l’aide du mappage de table à double écriture **Chiffres réels d’intégration Project Operations (msdyn\_actuals)**. Pour plus d’informations, voir [Estimations de projet et chiffres réels](resource-dual-write-estimates-actuals.md).

Le processus périodique **Importer depuis la table intermédiaire** crée des lignes de journal liées aux notes de frais dans la feuille Intégration de Project Operations. Le compte de contrepartie est par défaut le compte d’intégration des dépenses. Le journal d’intégration de comptabilisation efface le solde de compte pour la transaction de dépense et transfère le montant de la dépense vers le compte de coûts du projet. Le système crée également des transactions de livre auxiliaire de projet à des fins de facturation en aval et de comptabilisation des produits.
