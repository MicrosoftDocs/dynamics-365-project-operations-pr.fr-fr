---
title: Synchronisez les estimations de projet directement depuis Project Service Automation vers Finance and Operations
description: Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les estimations d'heures du projet et les estimations de dépense du projet directement à partir de Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289456"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3aa95-103">Synchronisez les estimations de projet directement depuis Project Service Automation vers Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3aa95-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3aa95-104">Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les estimations d'heures du projet et les estimations de dépense du projet directement à partir de Dynamics 365 Project Service Automation vers Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3aa95-105">L'intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d'heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.</span><span class="sxs-lookup"><span data-stu-id="3aa95-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="3aa95-106">L’intégration des chiffres réels est disponible à partir de la version 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="3aa95-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3aa95-107">Flux de données pour Project Service Automation vers Finance</span><span class="sxs-lookup"><span data-stu-id="3aa95-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="3aa95-108">La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3aa95-109">Les modèles d'intégration disponibles avec la fonctionnalité d'intégration de données permettent le flux de données sur les estimations heures et dépenses du projet de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3aa95-110">L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3aa95-111">[![Flux de données pour l'intégration de Project Service Automation avec Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3aa95-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="3aa95-112">Estimations des heures du projet</span><span class="sxs-lookup"><span data-stu-id="3aa95-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3aa95-113">Modèle et tâches</span><span class="sxs-lookup"><span data-stu-id="3aa95-113">Template and tasks</span></span>

<span data-ttu-id="3aa95-114">Pour accéder aux modèles disponibles, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.</span><span class="sxs-lookup"><span data-stu-id="3aa95-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3aa95-115">Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser les estimations en heures du projet de Project Service Automation vers Finance :</span><span class="sxs-lookup"><span data-stu-id="3aa95-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3aa95-116">**Nom du modèle dans l'intégration de données :** Estimations d'heures du projet (PSA vers Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3aa95-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3aa95-117">**Nom des tâches dans le projet :**</span><span class="sxs-lookup"><span data-stu-id="3aa95-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3aa95-118">Relations des transactions</span><span class="sxs-lookup"><span data-stu-id="3aa95-118">Transaction relationships</span></span>
    - <span data-ttu-id="3aa95-119">Estimations de dépenses</span><span class="sxs-lookup"><span data-stu-id="3aa95-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3aa95-120">Ensemble d'entités</span><span class="sxs-lookup"><span data-stu-id="3aa95-120">Entity set</span></span>

| <span data-ttu-id="3aa95-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3aa95-121">Project Service Automation</span></span> | <span data-ttu-id="3aa95-122">Finances</span><span class="sxs-lookup"><span data-stu-id="3aa95-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="3aa95-123">Tâches du projet</span><span class="sxs-lookup"><span data-stu-id="3aa95-123">Project tasks</span></span>              | <span data-ttu-id="3aa95-124">Entité d'intégration pour les estimations d'heures de projet</span><span class="sxs-lookup"><span data-stu-id="3aa95-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="3aa95-125">Flux d'entité</span><span class="sxs-lookup"><span data-stu-id="3aa95-125">Entity flow</span></span>

<span data-ttu-id="3aa95-126">Les estimations d'heures du projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que prévisions d'heures du projet.</span><span class="sxs-lookup"><span data-stu-id="3aa95-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3aa95-127">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3aa95-127">Prerequisites</span></span>

<span data-ttu-id="3aa95-128">Avant que la synchronisation des estimations des heures de projet puisse avoir lieu, vous devez synchroniser les projets, les tâches de projet et les catégories de transaction de dépenses de projet.</span><span class="sxs-lookup"><span data-stu-id="3aa95-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3aa95-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3aa95-129">Power Query</span></span>

<span data-ttu-id="3aa95-130">Dans le modèle d'estimations d'heures de projet, vous devez utiliser Microsoft Power Query pour Excel pour effectuer ces tâches :</span><span class="sxs-lookup"><span data-stu-id="3aa95-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="3aa95-131">Définissez l'ID de modèle de prévision par défaut qui sera utilisé lorsque l'intégration crée de nouvelles prévisions horaires.</span><span class="sxs-lookup"><span data-stu-id="3aa95-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3aa95-132">Filtrez tous les enregistrements spécifiques aux ressources de la tâche qui échoueront l'intégration dans les prévisions horaires.</span><span class="sxs-lookup"><span data-stu-id="3aa95-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="3aa95-133">Filtrez toutes les lignes de catégorie de transaction vides.</span><span class="sxs-lookup"><span data-stu-id="3aa95-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="3aa95-134">Le fait de ne pas effectuer cette tâche peut entraîner des prévisions horaires incorrectes.</span><span class="sxs-lookup"><span data-stu-id="3aa95-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3aa95-135">Définissez l'ID de modèle de prévision par défaut.</span><span class="sxs-lookup"><span data-stu-id="3aa95-135">Set the default forecast model ID</span></span>

<span data-ttu-id="3aa95-136">Pour mettre à jour l'ID de modèle de prévision par défaut dans le modèle, cliquez sur la flèche **Carte** pour ouvrir le mappage.</span><span class="sxs-lookup"><span data-stu-id="3aa95-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3aa95-137">Puis, sélectionnez le lien **Requête et filtrage avancés**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3aa95-138">Si vous utilisez le modèle par défaut Estimations des heures de projet (PSA vers Fin and Ops), dans Power Query, sélectionnez la dernière **Condition insérée** dans la liste des **Étapes appliquées**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="3aa95-139">Dans l'entrée **Fonction**, remplacez **O\_prévision** avec le nom de l'ID du modèle de prévision qui doit être utilisé avec l'intégration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3aa95-140">Le modèle par défaut a un ID de modèle de prévision issu des données de démonstration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3aa95-141">Si vous créez un nouveau modèle, vous devez ajouter cette colonne.</span><span class="sxs-lookup"><span data-stu-id="3aa95-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3aa95-142">Dans Power Query, sélectionnez **Ajouter une colonne conditionnelle** et entrez un nom pour la nouvelle colonne, tel que **IDModèle**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3aa95-143">Entrez la condition pour la colonne, où, si la tâche du projet n'est pas nulle, alors \<enter the forecast model ID\> ; sinon nul.</span><span class="sxs-lookup"><span data-stu-id="3aa95-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="3aa95-144">Filtrer les enregistrements spécifiques aux ressources</span><span class="sxs-lookup"><span data-stu-id="3aa95-144">Filter out resource-specific records</span></span>

<span data-ttu-id="3aa95-145">Le modèle d'estimation des heures du projet (PSA vers Fin and Ops) a un filtre par défaut qui supprime tous les enregistrements spécifiques aux ressources.</span><span class="sxs-lookup"><span data-stu-id="3aa95-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="3aa95-146">Si vous créez votre propre modèle, vous devez ajouter ce filtre.</span><span class="sxs-lookup"><span data-stu-id="3aa95-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3aa95-147">Sélectionnez le lien **Requête et filtrage avancés** pour filtrer sur la colonne **msdyn\_islinetask** de sorte que seuls les enregistrements **False** sont inclus.</span><span class="sxs-lookup"><span data-stu-id="3aa95-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="3aa95-148">Filtrer toutes les lignes de catégorie de transaction vides</span><span class="sxs-lookup"><span data-stu-id="3aa95-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="3aa95-149">Vous devez ajouter un filtre pour supprimer toutes les lignes contenant des catégories de transaction vides.</span><span class="sxs-lookup"><span data-stu-id="3aa95-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="3aa95-150">Cette tâche est requise, que vous utilisiez le modèle par défaut ou que vous créiez votre propre modèle.</span><span class="sxs-lookup"><span data-stu-id="3aa95-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="3aa95-151">Ce filtre supprime toutes les lignes récapitulatives de Project Service Automation qui pourraient entraîner des prévisions d'heures dans Finance incorrectes.</span><span class="sxs-lookup"><span data-stu-id="3aa95-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="3aa95-152">Sélectionnez le lien **Requête et filtrage avancés** pour filtrer les enregistrements nuls dans la colonne **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3aa95-153">Mappage de modèles dans l’intégration de données</span><span class="sxs-lookup"><span data-stu-id="3aa95-153">Template mapping in Data integration</span></span>

<span data-ttu-id="3aa95-154">L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données.</span><span class="sxs-lookup"><span data-stu-id="3aa95-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="3aa95-155">Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3aa95-156">[![Mappage de tâche de modèle dans l'intégration de données](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3aa95-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="3aa95-157">les estimations de dépense du projet.</span><span class="sxs-lookup"><span data-stu-id="3aa95-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3aa95-158">Modèle et tâches</span><span class="sxs-lookup"><span data-stu-id="3aa95-158">Template and tasks</span></span>

<span data-ttu-id="3aa95-159">Le modèle et les tâches sous-jacentes suivants sont utilisés pour synchroniser les estimations de dépense du projet de Project Service Automation vers Finance :</span><span class="sxs-lookup"><span data-stu-id="3aa95-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3aa95-160">**Nom du modèle dans l'intégration de données :** Estimations de dépense du projet (PSA vers Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3aa95-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3aa95-161">**Nom des tâches dans le projet :**</span><span class="sxs-lookup"><span data-stu-id="3aa95-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3aa95-162">Relations des transactions</span><span class="sxs-lookup"><span data-stu-id="3aa95-162">Transaction relationships</span></span> 
    - <span data-ttu-id="3aa95-163">Estimations de dépenses</span><span class="sxs-lookup"><span data-stu-id="3aa95-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3aa95-164">Ensemble d'entités</span><span class="sxs-lookup"><span data-stu-id="3aa95-164">Entity set</span></span>

| <span data-ttu-id="3aa95-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3aa95-165">Project Service Automation</span></span> | <span data-ttu-id="3aa95-166">Finances</span><span class="sxs-lookup"><span data-stu-id="3aa95-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="3aa95-167">Connexions de transactions</span><span class="sxs-lookup"><span data-stu-id="3aa95-167">Transaction Connections</span></span>    | <span data-ttu-id="3aa95-168">Entité d'intégration pour les relations de transaction du projet</span><span class="sxs-lookup"><span data-stu-id="3aa95-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="3aa95-169">Lignes d'estimation</span><span class="sxs-lookup"><span data-stu-id="3aa95-169">Estimate Lines</span></span>             | <span data-ttu-id="3aa95-170">Entité d'intégration pour les estimations de dépense de projet</span><span class="sxs-lookup"><span data-stu-id="3aa95-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="3aa95-171">Flux d'entité</span><span class="sxs-lookup"><span data-stu-id="3aa95-171">Entity flow</span></span>

<span data-ttu-id="3aa95-172">Les estimations de dépense du projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que prévisions de dépense du projet.</span><span class="sxs-lookup"><span data-stu-id="3aa95-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3aa95-173">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3aa95-173">Prerequisites</span></span>

<span data-ttu-id="3aa95-174">Avant que la synchronisation des estimations des dépenses du projet puisse avoir lieu, vous devez synchroniser les projets, les tâches de projet et les catégories de transaction de dépenses de projet.</span><span class="sxs-lookup"><span data-stu-id="3aa95-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3aa95-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="3aa95-175">Power Query</span></span>

<span data-ttu-id="3aa95-176">Dans le modèle d'estimations des dépenses du projet, vous devez utiliser Power Query pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3aa95-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="3aa95-177">Filtrez pour inclure uniquement les enregistrements de ligne d'estimation des dépenses.</span><span class="sxs-lookup"><span data-stu-id="3aa95-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="3aa95-178">Définissez l'ID de modèle de prévision par défaut qui sera utilisé lorsque l'intégration crée de nouvelles prévisions horaires.</span><span class="sxs-lookup"><span data-stu-id="3aa95-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3aa95-179">Transformez les types de facturation.</span><span class="sxs-lookup"><span data-stu-id="3aa95-179">Transform the billing types.</span></span>
- <span data-ttu-id="3aa95-180">Transformez les types de transaction.</span><span class="sxs-lookup"><span data-stu-id="3aa95-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="3aa95-181">Filtrez pour inclure uniquement les lignes d'estimation des dépenses.</span><span class="sxs-lookup"><span data-stu-id="3aa95-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="3aa95-182">Le modèle Estimations des dépenses du projet (PSA vers Fin et Ops) a un filtre par défaut qui inclut uniquement les lignes de dépenses dans l'intégration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="3aa95-183">Si vous créez votre propre modèle, vous devez ajouter ce filtre.</span><span class="sxs-lookup"><span data-stu-id="3aa95-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3aa95-184">Sélectionnez la tâche **Relations de transaction**, puis cliquez sur la flèche **Carte** pour ouvrir le mappage.</span><span class="sxs-lookup"><span data-stu-id="3aa95-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3aa95-185">Sélectionnez le lien **Requête et filtrage avancés**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="3aa95-186">Filtrez la colonne **msdyn\_transactiontype1** de manière à n'inclure que **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3aa95-187">Définissez l'ID de modèle de prévision par défaut.</span><span class="sxs-lookup"><span data-stu-id="3aa95-187">Set the default forecast model ID</span></span>

<span data-ttu-id="3aa95-188">Pour mettre à jour l'ID de modèle de prévision par défaut dans le modèle, sélectionnez la tâche **Estimations des dépenses**, puis cliquez sur la flèche **Carte** pour ouvrir le mappage.</span><span class="sxs-lookup"><span data-stu-id="3aa95-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3aa95-189">Sélectionnez le lien **Requête et filtrage avancés**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3aa95-190">Si vous utilisez le modèle par défaut Estimations des dépenses (PSA vers Fin and Ops), dans Power Query, sélectionnez la première **Condition insérée** de la section **Étapes appliquées**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="3aa95-191">Dans l'entrée **Fonction**, remplacez **O\_prévision** avec le nom de l'ID du modèle de prévision qui doit être utilisé avec l'intégration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3aa95-192">Le modèle par défaut a un ID de modèle de prévision issu des données de démonstration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3aa95-193">Si vous créez un nouveau modèle, vous devez ajouter cette colonne.</span><span class="sxs-lookup"><span data-stu-id="3aa95-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3aa95-194">Dans Power Query, sélectionnez **Ajouter une colonne conditionnelle** et entrez un nom pour la nouvelle colonne, tel que **IDModèle**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3aa95-195">Entrez la condition pour la colonne, où, si l'ID de ligne d'estimation n'est pas nulle, alors \<enter the forecast model ID\> ; sinon nul.</span><span class="sxs-lookup"><span data-stu-id="3aa95-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="3aa95-196">Transformer les types de facturation</span><span class="sxs-lookup"><span data-stu-id="3aa95-196">Transform the billing types</span></span>

<span data-ttu-id="3aa95-197">Le modèle Estimations des dépenses de projet (PSA vers Fin et Ops) comprend une colonne conditionnelle qui est utilisée pour transformer les types de facturation reçus de Project Service Automation lors de l'intégration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3aa95-198">Si vous créez votre propre modèle, vous devez ajouter cette colonne conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="3aa95-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3aa95-199">Sélectionnez le lien **Requête et filtrage avancés**, puis sélectionnez **Ajouter une colonne conditionnelle**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3aa95-200">Entrez un nom pour la nouvelle colonne, tel que **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="3aa95-201">Puis saisissez la condition suivante :</span><span class="sxs-lookup"><span data-stu-id="3aa95-201">Then enter the following condition:</span></span>

<span data-ttu-id="3aa95-202">Si **msdyn\_billingtype** = 192350000, alors **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="3aa95-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="3aa95-203">autre si **msdyn\_billingtype** = 192350001, alors **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="3aa95-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="3aa95-204">autre si **msdyn\_billingtype** = 192350002, alors **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="3aa95-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="3aa95-205">autre **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="3aa95-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="3aa95-206">Transformer les types de transaction</span><span class="sxs-lookup"><span data-stu-id="3aa95-206">Transform the transaction types</span></span>

<span data-ttu-id="3aa95-207">Le modèle Estimations des dépenses de projet (PSA vers Fin et Ops) comprend une colonne conditionnelle qui est utilisée pour transformer les types de transaction reçus de Project Service Automation lors de l'intégration.</span><span class="sxs-lookup"><span data-stu-id="3aa95-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3aa95-208">Si vous créez votre propre modèle, vous devez ajouter cette colonne conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="3aa95-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3aa95-209">Sélectionnez le lien **Requête et filtrage avancés**, puis sélectionnez **Ajouter une colonne conditionnelle**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3aa95-210">Entrez un nom pour la nouvelle colonne, tel que **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="3aa95-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="3aa95-211">Puis saisissez la condition suivante :</span><span class="sxs-lookup"><span data-stu-id="3aa95-211">Then enter the following condition:</span></span>

<span data-ttu-id="3aa95-212">Si **msdyn\_transactiontypecode** = 192350000, alors **Coût**</span><span class="sxs-lookup"><span data-stu-id="3aa95-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="3aa95-213">autre si **msdyn\_transactiontypecode** = 192350005, alors **Sales**</span><span class="sxs-lookup"><span data-stu-id="3aa95-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="3aa95-214">autre **null**</span><span class="sxs-lookup"><span data-stu-id="3aa95-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3aa95-215">Mappage de modèles dans l’intégration de données</span><span class="sxs-lookup"><span data-stu-id="3aa95-215">Template mapping in Data integration</span></span>

<span data-ttu-id="3aa95-216">Les illustrations suivantes montrent des exemples de mappage de tâches de modèle dans l’intégration de données.</span><span class="sxs-lookup"><span data-stu-id="3aa95-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="3aa95-217">Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="3aa95-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3aa95-218">[![Mappage des modèles de transactions d'estimation de dépenses](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3aa95-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="3aa95-219">[![Mappage des modèles d'estimation de dépenses](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3aa95-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]