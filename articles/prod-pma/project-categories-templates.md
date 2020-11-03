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
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075879"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="39a79-103">Synchroniser les catégories de dépenses de projet entre Finance and Operations et Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39a79-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39a79-104">Cette rubrique décrit les modèles et les tâches sous-jacentes qui sont utilisés pour synchroniser les catégories de dépense du projet entre Dynamics 365 Finance et Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="39a79-105">L’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités sont disponibles dans la version 8.0.</span><span class="sxs-lookup"><span data-stu-id="39a79-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="39a79-106">L’intégration des chiffres réels est disponible à partir de la version 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="39a79-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="39a79-107">Si vous utilisez Enterprise Edition 7.3.0 après avoir installé KB 4132657 et KB 4132660, vous pourrez utiliser les modèles pour intégrer des tâches de projet, des catégories de transaction de dépenses, des estimations d’heures, des estimations de dépenses et des chiffres réels, et pour configurer verrouillage des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="39a79-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="39a79-108">Si vous devez réinitialiser les répartitions comptables, nous vous recommandons d’installer également KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="39a79-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="39a79-109">Flux de données pour Project Service Automation et Finance</span><span class="sxs-lookup"><span data-stu-id="39a79-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="39a79-110">La solution d’intégration Project Service Automation et Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="39a79-111">Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de données sur les catégories de transaction de dépense entre Finance et Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="39a79-112">Si les catégories de dépenses de projet sont maîtrisées dans Finance, le flux d’intégration passe d’abord de Finance à Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="39a79-113">Les ID d’intégration des catégories de dépenses du projet sont ensuite mis à jour via la synchronisation de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="39a79-114">Si les catégories de dépenses de projet sont maîtrisées dans Project Service Automation, le flux d’intégration passe d’abord de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="39a79-115">Les catégories de projet doivent déjà être configurées dans Finance avant la synchronisation à partir de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="39a79-116">Ensuite, synchronisez de nouveau de Finance vers Project Service Automation, puis à nouveau de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="39a79-117">De cette manière, vous garantissez que les catégories sont liées et qu’aucun doublon n’est créé.</span><span class="sxs-lookup"><span data-stu-id="39a79-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="39a79-118">En règle générale, les catégories de dépenses de projet sont maîtrisées dans Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="39a79-119">Toutefois, si ce n’est pas le cas, ou si des catégories de dépenses ont déjà été créées dans Project Service Automation, vous devez d’abord effectuer la synchronisation à l’aide du modèle Catégories de transaction de dépenses de projet (PSA vers Fin et Ops).</span><span class="sxs-lookup"><span data-stu-id="39a79-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="39a79-120">Ensuite, synchronisez à l’aide du modèle Catégories de transaction de dépenses de projet (Fin et Ops vers PSA).</span><span class="sxs-lookup"><span data-stu-id="39a79-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="39a79-121">Vous devez ensuite exécuter à nouveau la synchronisation de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="39a79-122">Si vous synchronisez d’abord à partir de Project Service Automation, les conditions suivantes doivent être remplies dans Finance avant l’exécution de la synchronisation :</span><span class="sxs-lookup"><span data-stu-id="39a79-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="39a79-123">La catégorie partagée qui correspond à la catégorie de projet configurée dans Project Service Automation doit exister et elle doit être activée pour **Projet** et **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="39a79-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="39a79-124">Pour chaque entité juridique Finance qui doit être intégrée, les catégories de projet suivantes doivent exister :</span><span class="sxs-lookup"><span data-stu-id="39a79-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="39a79-125">**Catégorie de projet** existe.</span><span class="sxs-lookup"><span data-stu-id="39a79-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="39a79-126">**Utiliser dans dépenses** est activé.</span><span class="sxs-lookup"><span data-stu-id="39a79-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="39a79-127">**Actif dans le journal** est activé.</span><span class="sxs-lookup"><span data-stu-id="39a79-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="39a79-128">**Type de transaction** est réglé sur **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="39a79-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="39a79-129">L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="39a79-130">[![Flux de données pour l’intégration de Project Service Automation avec Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="39a79-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="39a79-131">Synchronisation de la catégorie des dépenses du projet de Finance vers Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39a79-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="39a79-132">Modèle et tâche</span><span class="sxs-lookup"><span data-stu-id="39a79-132">Template and task</span></span>

<span data-ttu-id="39a79-133">Pour accéder au modèle, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets** , puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.</span><span class="sxs-lookup"><span data-stu-id="39a79-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="39a79-134">Le modèle et la tâche sous-jacente suivants sont utilisés pour synchroniser les catégories de dépense du projet de Finance vers Project Service Automation :</span><span class="sxs-lookup"><span data-stu-id="39a79-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="39a79-135">**Nom du modèle dans l’intégration de données :** Catégories de transaction des dépenses du projet (Fin and Ops vers PSA)</span><span class="sxs-lookup"><span data-stu-id="39a79-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="39a79-136">**Nom de la tâche dans le projet :** Synchroniser les catégories avec PSA</span><span class="sxs-lookup"><span data-stu-id="39a79-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="39a79-137">Ensemble d’entités</span><span class="sxs-lookup"><span data-stu-id="39a79-137">Entity set</span></span>

| <span data-ttu-id="39a79-138">Finances</span><span class="sxs-lookup"><span data-stu-id="39a79-138">Finance</span></span>                           | <span data-ttu-id="39a79-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39a79-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="39a79-140">Entité d’intégration pour les catégories</span><span class="sxs-lookup"><span data-stu-id="39a79-140">Integration entity for categories</span></span> | <span data-ttu-id="39a79-141">Catégories de transactions</span><span class="sxs-lookup"><span data-stu-id="39a79-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="39a79-142">Flux d’entité</span><span class="sxs-lookup"><span data-stu-id="39a79-142">Entity flow</span></span>

<span data-ttu-id="39a79-143">Les catégories de dépense du projet sont gérées dans Finance, et elles sont synchronisées vers Project Service Automation en tant que catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="39a79-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="39a79-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="39a79-144">Power Query</span></span>

<span data-ttu-id="39a79-145">Lorsque vous synchronisez avec Project Service Automation, vous devez utiliser Microsoft Power Query pour Excel pour définir le type de facturation sur la catégorie de transaction.</span><span class="sxs-lookup"><span data-stu-id="39a79-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="39a79-146">Le modèle de catégories de transaction de dépenses du projet (Fin and Ops vers PSA) fournit une colonne et un mappage par défaut.</span><span class="sxs-lookup"><span data-stu-id="39a79-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="39a79-147">Si vous créez votre propre modèle, vous devez ajouter une colonne conditionnelle dans Power Query.</span><span class="sxs-lookup"><span data-stu-id="39a79-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="39a79-148">Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="39a79-148">Follow these steps.</span></span>

1. <span data-ttu-id="39a79-149">Cliquez sur la flèche pour ouvrir le mappage de la tâche des catégories de dépenses du projet dans le modèle Catégories de transaction de dépenses du projet (Fin and Ops vers PSA).</span><span class="sxs-lookup"><span data-stu-id="39a79-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="39a79-150">Cliquez sur le lien **Requête et filtrage avancés** pour ouvrir Power Query.</span><span class="sxs-lookup"><span data-stu-id="39a79-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="39a79-151">Sélectionnez **Ajouter une colonne conditionnelle**.</span><span class="sxs-lookup"><span data-stu-id="39a79-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="39a79-152">Entrez un nom pour la nouvelle colonne, tel que **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="39a79-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="39a79-153">Entrez la condition suivante : **si CATEGORYID n’est pas égal à null alors 19235001, sinon null**.</span><span class="sxs-lookup"><span data-stu-id="39a79-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="39a79-154">Cliquez sur **OK** sur la colonne.</span><span class="sxs-lookup"><span data-stu-id="39a79-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="39a79-155">Assurez-vous de mapper cette nouvelle colonne sur la page de mappage.</span><span class="sxs-lookup"><span data-stu-id="39a79-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="39a79-156">L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données.</span><span class="sxs-lookup"><span data-stu-id="39a79-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="39a79-157">Le mappage affiche les informations de champ qui seront synchronisées de Finance vers Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="39a79-158">[![Mappage du modèle Catégorie des dépenses à Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="39a79-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="39a79-159">Synchronisation de la catégorie des dépenses du projet de Project Service Automation vers Finance</span><span class="sxs-lookup"><span data-stu-id="39a79-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="39a79-160">Modèle et tâche</span><span class="sxs-lookup"><span data-stu-id="39a79-160">Template and task</span></span>

<span data-ttu-id="39a79-161">Le modèle et la tâche sous-jacente suivants sont utilisés pour synchroniser les catégories de dépense du projet de Project Service Automation vers Finance :</span><span class="sxs-lookup"><span data-stu-id="39a79-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="39a79-162">**Nom du modèle dans l’intégration de données :** Catégories de transaction des dépenses du projet (PSA vers Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="39a79-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="39a79-163">**Nom de la tâche dans le projet :** Synchroniser les catégories avec Fin Ops</span><span class="sxs-lookup"><span data-stu-id="39a79-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="39a79-164">Ensemble d’entités</span><span class="sxs-lookup"><span data-stu-id="39a79-164">Entity set</span></span>

| <span data-ttu-id="39a79-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="39a79-165">Project Service Automation</span></span> | <span data-ttu-id="39a79-166">Finances</span><span class="sxs-lookup"><span data-stu-id="39a79-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="39a79-167">Catégories de transactions</span><span class="sxs-lookup"><span data-stu-id="39a79-167">Transaction categories</span></span>     | <span data-ttu-id="39a79-168">Entité d’intégration pour les catégories</span><span class="sxs-lookup"><span data-stu-id="39a79-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="39a79-169">Flux d’entité</span><span class="sxs-lookup"><span data-stu-id="39a79-169">Entity flow</span></span>

<span data-ttu-id="39a79-170">Les catégories de dépense du projet sont gérées dans Finance, et elles sont synchronisées vers Project Service Automation en tant que catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="39a79-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="39a79-171">La synchronisation vers Finance met à jour la catégorie de projet dans Finance avec l’ID d’intégration depuis Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39a79-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="39a79-172">Mappage de modèles dans l’intégration de données</span><span class="sxs-lookup"><span data-stu-id="39a79-172">Template mapping in Data integration</span></span>

<span data-ttu-id="39a79-173">L’illustration suivante montre un exemple de mappage de tâches de modèle dans l’intégration de données.</span><span class="sxs-lookup"><span data-stu-id="39a79-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="39a79-174">Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="39a79-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="39a79-175">[![Mappage du modèle Project Service Automation vers Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="39a79-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>