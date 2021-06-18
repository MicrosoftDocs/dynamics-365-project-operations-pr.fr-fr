---
title: Mapper les projets et les tâches sur une ligne du devis selon les projets
description: Cette rubrique fournit des informations sur la façon de mapper des projets et des tâches à une ligne de tâches basée sur un projet.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994583"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="af405-103">Mapper les projets et les tâches sur une ligne du devis selon les projets</span><span class="sxs-lookup"><span data-stu-id="af405-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="af405-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="af405-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af405-105">Sur les lignes de devis basées sur un projet, vous pouvez mapper les tâches spécifiques d’un projet déjà associé à une ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="af405-106">Lorsque vous mappez des tâches à une ligne de devis, les éléments suivants que vous avez définis sur la ligne de devis ne s’appliqueront qu’à ces tâches :</span><span class="sxs-lookup"><span data-stu-id="af405-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="af405-107">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="af405-107">Billing method</span></span>
- <span data-ttu-id="af405-108">Options d’exigibilité</span><span class="sxs-lookup"><span data-stu-id="af405-108">Chargeability options</span></span>
- <span data-ttu-id="af405-109">Limites à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="af405-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="af405-110">Clients</span><span class="sxs-lookup"><span data-stu-id="af405-110">Customers</span></span>

<span data-ttu-id="af405-111">Par exemple, vous pourriez avoir un projet où une phase est un prix fixe et toutes les autres phases sont le temps et les matériaux.</span><span class="sxs-lookup"><span data-stu-id="af405-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="af405-112">Dans ce cas, vous pouvez associer la première phase, et toutes ses tâches enfants, à la ligne de devis pour cette phase avec un mode de facturation à prix fixe.</span><span class="sxs-lookup"><span data-stu-id="af405-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="af405-113">Vous pouvez ensuite associer toutes les autres phases à la ligne de devis basée sur le temps et les matériaux.</span><span class="sxs-lookup"><span data-stu-id="af405-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="af405-114">Associer des tâches à une ligne de devis selon un projet</span><span class="sxs-lookup"><span data-stu-id="af405-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="af405-115">Vous pouvez associer des tâches à des lignes de devis à partir des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="af405-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="af405-116">Page **Projet** > onglet **Facturation des tâches** (optimal)</span><span class="sxs-lookup"><span data-stu-id="af405-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="af405-117">Page **Ligne de devis** > onglet **Tâches payantes**</span><span class="sxs-lookup"><span data-stu-id="af405-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="af405-118">À partir de la page du projet</span><span class="sxs-lookup"><span data-stu-id="af405-118">From the Project page</span></span>

<span data-ttu-id="af405-119">La page **Projet** offre une expérience optimale pour associer des tâches à des lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="af405-120">Vous pouvez utiliser cette page pour sélectionner plusieurs tâches et les associer toutes, ainsi que leurs tâches enfants, à la ligne de devis sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="af405-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="af405-121">Sur l’onglet **Général** d’une ligne de devis basée sur un projet, vérifiez que le champ **Projet** est rempli.</span><span class="sxs-lookup"><span data-stu-id="af405-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="af405-122">Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.</span><span class="sxs-lookup"><span data-stu-id="af405-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="af405-123">Enregistrez la ligne du devis selon les projets.</span><span class="sxs-lookup"><span data-stu-id="af405-123">Save the project-based quote line.</span></span> <span data-ttu-id="af405-124">Lorsque le formulaire est actualisé, l’onglet **Tâches payantes** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="af405-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="af405-125">Sur l’onglet **Général**, sélectionnez le lien du projet dans le champ **Projet**.</span><span class="sxs-lookup"><span data-stu-id="af405-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="af405-126">Sur la page **Projet**, sélectionnez l’onglet **Facturation des tâches**.</span><span class="sxs-lookup"><span data-stu-id="af405-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="af405-127">Dans la deuxième grille, qui s’applique à la configuration de la facturation spécifique aux tâches, sélectionnez une ou plusieurs tâches, puis sélectionnez **Associer des lignes de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="af405-128">Dans la page de dialogue qui apparaît, sélectionnez une ligne de devis qui affiche les lignes de devis basées sur le projet sur le devis.</span><span class="sxs-lookup"><span data-stu-id="af405-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="af405-129">Dans le champ **Type de facturation**, indiquez si ces tâches sont facturables ou non.</span><span class="sxs-lookup"><span data-stu-id="af405-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="af405-130">Cochez la case pour indiquer si l’association doit inclure les tâches enfants des tâches sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="af405-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="af405-131">Cochez la case pour associer les tâches enfants des tâches sélectionnées à la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="af405-132">Sélectionnez **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="af405-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="af405-133">À partir de la page de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="af405-133">From the Quote line page</span></span>

<span data-ttu-id="af405-134">Vous pouvez associer des tâches de projet aux lignes de devis de l’onglet **Tâches payantes** sur la page **Ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="af405-135">L’emplacement optimal pour associer des tâches de projet à des lignes de devis est l’onglet **Facturation des tâches** sur la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="af405-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="af405-136">Si vous associez des tâches de l’onglet **Tâches payantes** sur la page **Ligne de devis**, vous devez associer manuellement chaque projet.</span><span class="sxs-lookup"><span data-stu-id="af405-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="af405-137">Sur l’onglet **Général** d’une ligne de devis basée sur un projet, vérifiez qu’un projet est sélectionné dans le champ **Projet**.</span><span class="sxs-lookup"><span data-stu-id="af405-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="af405-138">Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.</span><span class="sxs-lookup"><span data-stu-id="af405-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="af405-139">Enregistrez la ligne du devis selon les projets.</span><span class="sxs-lookup"><span data-stu-id="af405-139">Save the project-based quote line.</span></span> <span data-ttu-id="af405-140">Lorsque le formulaire est actualisé, l’onglet **Tâches payantes** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="af405-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="af405-141">Sur l’onglet **Tâches payantes**, sélectionnez **Ajouter une tâche de ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="af405-142">Sur la page **Tâche de ligne de devis**, dans le champ **Tâches**, sélectionnez la tâche et dans le champ **Type de facturation**, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="af405-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="af405-143">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="af405-143">Close the page.</span></span> <span data-ttu-id="af405-144">La tâche sélectionnée est maintenant associée à la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="af405-145">Dissocier des tâches de lignes de devis selon un projet</span><span class="sxs-lookup"><span data-stu-id="af405-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="af405-146">À partir de la page du projet</span><span class="sxs-lookup"><span data-stu-id="af405-146">From the Project page</span></span>

<span data-ttu-id="af405-147">Cette méthode offre l’expérience la plus optimale pour dissocier des tâches des lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="af405-148">Vous sélectionner plusieurs tâches et les dissocier toutes, ainsi que leurs tâches enfants, de la ligne de devis sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="af405-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="af405-149">Sur l’onglet **Général** d’une ligne de devis basée sur un projet, dans le champ **Projet**, sélectionnez le lien du projet.</span><span class="sxs-lookup"><span data-stu-id="af405-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="af405-150">Sur la page **Projet**, sélectionnez l’onglet **Facturation des tâches**.</span><span class="sxs-lookup"><span data-stu-id="af405-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="af405-151">Dans la deuxième grille, qui s’applique à la configuration de la facturation spécifique aux tâches, sélectionnez une ou plusieurs tâches, puis sélectionnez **Dissocier des lignes de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="af405-152">Dans la page de dialogue qui apparaît, sélectionnez une ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="af405-153">Cochez la case pour indiquer si l’association doit également être supprimée des tâches enfants des tâches sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="af405-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="af405-154">Cochez la case pour dissocier également les tâches enfants des tâches sélectionnées à la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="af405-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="af405-155">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="af405-155">Select **OK**.</span></span> <span data-ttu-id="af405-156">Un message d’avertissement vous informe que si vous supprimez cette association, tout chiffre réel précédemment enregistré sur la tâche pourrait être annulé.</span><span class="sxs-lookup"><span data-stu-id="af405-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="af405-157">Sélectionnez **OK** pour continuer et supprimer l’association entre la tâche et la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="af405-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="af405-158">À partir de la page de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="af405-158">From the Quote line page</span></span>

<span data-ttu-id="af405-159">Vous pouvez également dissocier des tâches de projet aux lignes de devis de l’onglet **Tâches payantes** sur la page **Ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="af405-160">Sur l’onglet **Tâches payantes**, sélectionnez **Supprimer une tâche de ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="af405-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="af405-161">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="af405-161">Select **OK**.</span></span> <span data-ttu-id="af405-162">Un message d’avertissement vous informe que si vous supprimez cette association, tout chiffre réel précédemment enregistré sur la tâche pourrait être annulé.</span><span class="sxs-lookup"><span data-stu-id="af405-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="af405-163">Sélectionnez **OK** pour continuer et supprimer l’association entre la tâche et la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="af405-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="af405-164">Cette procédure ne supprime pas la tâche du projet.</span><span class="sxs-lookup"><span data-stu-id="af405-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="af405-165">Elle supprime uniquement l’association de tâche de la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="af405-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]