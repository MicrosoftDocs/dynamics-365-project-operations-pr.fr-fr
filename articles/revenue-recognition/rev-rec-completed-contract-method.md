---
title: Gérer les estimations de revenus
description: Cette rubrique fournit des informations sur la manière de gérer les estimations de revenus pour les projets.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279000"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="5b7fe-103">Gérer les estimations de revenus</span><span class="sxs-lookup"><span data-stu-id="5b7fe-103">Manage revenue estimates</span></span>

<span data-ttu-id="5b7fe-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="5b7fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5b7fe-105">Vous pouvez créer, calculer, valider, annuler ou éliminer des estimations de revenus.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="5b7fe-106">Vous pouvez le faire manuellement ou en utilisant un processus périodique.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="5b7fe-107">Cette rubrique fournit des informations sur la manière de gérer les estimations de revenus pour les projets.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="5b7fe-108">Gérer les estimations de revenus manuellement</span><span class="sxs-lookup"><span data-stu-id="5b7fe-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="5b7fe-109">Sur le projet d'estimation des revenus à prix fixe ou la page **Demande d'estimation** (**Gestion et comptabilité des projets** > **Rapports et demandes** > **Demandes de devis et rapports**), sélectionnez **Estimations**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="5b7fe-110">Gérer les estimations de revenus à l'aide d'un processus périodique</span><span class="sxs-lookup"><span data-stu-id="5b7fe-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="5b7fe-111">Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Estimations** et sélectionnez le processus correspondant.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="5b7fe-112">Créer une estimation de revenus</span><span class="sxs-lookup"><span data-stu-id="5b7fe-112">Create a revenue estimate</span></span>

<span data-ttu-id="5b7fe-113">Pour créer une estimation de revenus, suivez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="5b7fe-114">Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Estimations**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="5b7fe-115">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-115">Select **New**.</span></span> <span data-ttu-id="5b7fe-116">Sur la page **Création d'une estimation**, sélectionnez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b7fe-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="5b7fe-117">**Code période** : ce code détermine la fréquence à laquelle les estimations sont validées.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="5b7fe-118">**Date estimée** : date à laquelle l'estimation est traitée.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="5b7fe-119">**Continu** : cochez cette case pour créer des estimations uniquement si les estimations ont été validées dans la période précédente, ou si l'estimation est la première estimation qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="5b7fe-120">Si cette option n'est pas sélectionnée, les estimations sont créées même si les estimations n'ont pas été validées au cours de la période précédente.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="5b7fe-121">**Coût pour compléter les méthodes** : définissez comment estimer le travail de projet restant.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="5b7fe-122">Pour plus d'informations, voir [Coût pour compléter les méthodes](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5b7fe-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="5b7fe-123">**Méthode d'achèvement** : sélectionnez une méthode d'achèvement parmi les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b7fe-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="5b7fe-124">**Automatique** : le pourcentage d'achèvement est calculé automatiquement et basé sur les lignes de coût incluses dans le calcul.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="5b7fe-125">Le modèle de coût définit les lignes de coût incluses.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="5b7fe-126">**Manuel** : le pourcentage d'achèvement est égal au pourcentage d'achèvement de la dernière estimation.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="5b7fe-127">Une fois l'estimation créée, vous pouvez modifier le **Calcul manuel** sur la page **Estimations**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="5b7fe-128">**À partir du modèle de coût** : une combinaison des méthodes automatique et manuelle.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="5b7fe-129">Cette option est définie automatiquement ou manuellement, en fonction de la valeur par défaut dans le modèle de coût.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="5b7fe-130">**Modèle de prévision** : sélectionnez un modèle de prévision pour l'estimation.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="5b7fe-131">**Imprimer la liste des estimations** : créez et affichez une liste d'estimations.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="5b7fe-132">La liste contient l'état de la fonction en cours.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-132">The list contains the status of the current function.</span></span> <span data-ttu-id="5b7fe-133">Vous pouvez imprimer tous les avertissements concernant l'estimation sur le rapport.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="5b7fe-134">Les conditions suivantes font apparaître des avertissements dans la liste des estimations :</span><span class="sxs-lookup"><span data-stu-id="5b7fe-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="5b7fe-135">Un pourcentage d'achèvement supérieur à 100 %.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="5b7fe-136">Un pourcentage d'achèvement inférieur à zéro %.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="5b7fe-137">Un montant négatif dans la colonne **À terminer**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="5b7fe-138">Une estimation sans montant de contrat correspondant.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="5b7fe-139">Une estimation sans estimation de coût jointe.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="5b7fe-140">**Afficher la fenêtre Infos** : sélectionnez cette option pour recevoir un message contenant des informations sur les projets d'estimation qui ont été traités lors de l'exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="5b7fe-141">Valider TEC ou régularisations</span><span class="sxs-lookup"><span data-stu-id="5b7fe-141">Post WIP or accruals</span></span>

<span data-ttu-id="5b7fe-142">Une fois les estimations évaluées, elles sont maintenues, diminuées ou augmentées.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="5b7fe-143">Vous pouvez ensuite valider le TEC lorsque vous travaillez avec le principe d'évaluation **Contrat terminé**, ou valider les provisions lorsque vous travaillez avec le principe d'évaluation **Pourcentage terminé**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="5b7fe-144">Le statut de la période estimée change passe **Créé** à **Validé**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="5b7fe-145">Inverser TEC ou régularisations</span><span class="sxs-lookup"><span data-stu-id="5b7fe-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="5b7fe-146">Utilisez l'option d'inversement pour créditer les TEC ou les provisions déjà validés, puis créez des estimations pour la période.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="5b7fe-147">Pour inverser une période qui se situe entre d'autres périodes, inversez les périodes d'estimation nécessaires, puis revalidez-les.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="5b7fe-148">Étant donné que toutes les périodes suivantes dépendent des estimations de la période précédente, ne sautez aucune période.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="5b7fe-149">Éliminer le projet d'estimation et terminer le projet</span><span class="sxs-lookup"><span data-stu-id="5b7fe-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="5b7fe-150">La dernière étape du processus d'estimation consiste à éliminer le projet d'estimation et à mettre fin au projet à prix fixe lorsque le pourcentage d'achèvement atteint 100 %.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="5b7fe-151">Voici ce qui suit se produit lorsque vous exécutez l'élimination :</span><span class="sxs-lookup"><span data-stu-id="5b7fe-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="5b7fe-152">Pour un projet à prix fixe avec un contrat achevé, les valeurs TEC sont effacées des comptes de bilan et validés dans les comptes de résultat.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="5b7fe-153">Pour un projet à prix fixe avec un pourcentage achevé, les provisions sont supprimées des comptes de résultat.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="5b7fe-154">L'estimation fait passer le statut à **Éliminé**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="5b7fe-155">Dans des cas particuliers, le pourcentage peut dépasser 100 %.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="5b7fe-156">Lorsque cela se produit, réduisez le pourcentage d'achèvement en utilisant la **Méthode Définir le coût à terminer à zéro** pour atteindre 100 pour cent.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="5b7fe-157">Inverser élimination</span><span class="sxs-lookup"><span data-stu-id="5b7fe-157">Reverse elimination</span></span>

1. <span data-ttu-id="5b7fe-158">Accéder à **Gestion et comptabilité des projets** > **Périodique** > **Estimations** > **Inverser élimination**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="5b7fe-159">Dans le volet Actions, sur l’onglet **Processus**, dans le groupe **Maintenir**, sélectionnez **Estimation**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="5b7fe-160">Sélectionnez **Inverser élimination**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="5b7fe-161">Utilisez cette page pour inverser toutes les éliminations avec une date d'estimation spécifiée et avec le statut d'estimation **Éliminé**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="5b7fe-162">Le statut de la transaction change une fois que vous avez sélectionné les champs appropriés.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="5b7fe-163">Cela change définit également automatiquement le projet sur le statut **En cours** si l'étape du projet est définie comme terminée.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="5b7fe-164">Le statut de l'estimation de la période du projet repasse au statut **Validé**.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]