---
title: Configurer les composants facturables d’une ligne de devis
description: Cette rubrique fournit des informations sur la configuration de composants payants et non facturables sur une ligne de devis basée sur un projet.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858290"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="45ed3-103">Configurer les composants facturables d’une ligne de devis</span><span class="sxs-lookup"><span data-stu-id="45ed3-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="45ed3-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="45ed3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="45ed3-105">Une ligne de devis basée sur un projet a le concept des composants *inclus* et *payant*.</span><span class="sxs-lookup"><span data-stu-id="45ed3-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="45ed3-106">Les composants inclus sont soumis à :</span><span class="sxs-lookup"><span data-stu-id="45ed3-106">Included components are subject to:</span></span>

  - <span data-ttu-id="45ed3-107">Méthode de facturation et répartition des clients</span><span class="sxs-lookup"><span data-stu-id="45ed3-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="45ed3-108">Limites à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="45ed3-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="45ed3-109">Paramètres de fréquence de facturation définis sur la ligne de devis basée sur le projet</span><span class="sxs-lookup"><span data-stu-id="45ed3-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="45ed3-110">Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="45ed3-111">Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de devis :</span><span class="sxs-lookup"><span data-stu-id="45ed3-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="45ed3-112">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-112">Chargeable</span></span>
  - <span data-ttu-id="45ed3-113">Non facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-113">Non-chargeable</span></span>

<span data-ttu-id="45ed3-114">Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="45ed3-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="45ed3-115">La tarification est définie sur les tâches pour une ligne de devis et s’applique à toutes les classes de transaction incluses sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="45ed3-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="45ed3-116">Si le champ **Inclure les tâches** est défini sur **Projet entier** ou laissé vide, l’onglet **Tâches payantes** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45ed3-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="45ed3-117">La tarification est définie sur les rôles pour une ligne de devis et s’applique uniquement à la classe de transaction **Temps**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="45ed3-118">Si le champ **Inclure le temps** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Rôles facturables** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45ed3-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="45ed3-119">La tarification est définie sur les catégories de transaction pour une ligne de devis et s’applique uniquement à la classe de transaction **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="45ed3-120">Si le champ **Inclure les dépenses** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Catégories facturables** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45ed3-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="45ed3-121">Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="45ed3-122">Une tâche de projet peut être facturable ou non dans le contexte d’une ligne de devis basée sur un projet spécifique, ce qui rend possible la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="45ed3-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="45ed3-123">Si une ligne de devis basée sur un projet comprend **Temps** et la tâche **T1**, la tâche est associée à la ligne de devis comme facturable.</span><span class="sxs-lookup"><span data-stu-id="45ed3-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="45ed3-124">S’il y a une deuxième ligne de devis qui inclut **Dépenses**, vous pouvez associer la tâche **T1** sur la ligne de devis comme non facturable.</span><span class="sxs-lookup"><span data-stu-id="45ed3-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="45ed3-125">Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses enregistrées sur la tâche sont non facturables.</span><span class="sxs-lookup"><span data-stu-id="45ed3-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="45ed3-126">Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Tâches de la ligne de contrat**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="45ed3-127">Vous pouvez également mettre à jour le type de facturation d’une tâche de projet dans le champ **Type de facturation** dans la sous-grille dans la configuration de la facturation de la tâche d’un projet qui affiche les lignes de devis associées à une tâche.</span><span class="sxs-lookup"><span data-stu-id="45ed3-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="45ed3-128">Mettre à jour un rôle pour qu’il soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="45ed3-129">Un rôle peut être payant ou non dans le contexte d’une ligne de devis spécifique à un projet.</span><span class="sxs-lookup"><span data-stu-id="45ed3-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="45ed3-130">Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="45ed3-131">Mettre à jour une catégorie de transaction comme facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="45ed3-132">Une catégorie de transaction peut être facturable ou non facturable sur une ligne de devis spécifique.</span><span class="sxs-lookup"><span data-stu-id="45ed3-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="45ed3-133">Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.</span><span class="sxs-lookup"><span data-stu-id="45ed3-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="45ed3-134">Résoudre la chargeabilité</span><span class="sxs-lookup"><span data-stu-id="45ed3-134">Resolve chargeability</span></span>
<span data-ttu-id="45ed3-135">Une estimation ou un chiffre réel créé pour le temps ne sera considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="45ed3-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="45ed3-136">**Temps** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="45ed3-137">**Rôle** est configuré comme facturable sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="45ed3-138">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="45ed3-139">Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="45ed3-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="45ed3-140">Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="45ed3-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="45ed3-141">**Dépense** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="45ed3-142">**Catégorie de transaction** est configuré comme facturable sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="45ed3-143">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="45ed3-144">Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="45ed3-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="45ed3-145">Une estimation ou un chiffre réel créé pour du matériel ne sera considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="45ed3-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="45ed3-146">**Matériel** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="45ed3-147">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="45ed3-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="45ed3-148">Si ces deux éléments sont vrais, la **Tâche** doit également être configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="45ed3-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-149">
                    <strong>Inclut le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="45ed3-150">
                    <strong>Inclut la dépense</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="45ed3-151">
                    <strong>Inclut le matériel</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="45ed3-152">
                    <strong>Tâches incluses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-153">
                    <strong>Rôle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-154">
                    <strong>Catégorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-155">
                    <strong>Tâche</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="45ed3-156">
                    <strong>Impact sur le fait que l’élément soit facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-157">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-158">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-159">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-160">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-161">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-162">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-163">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-164">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-165">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-166">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-167">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-168">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-169">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-170">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="45ed3-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-171">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-172">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-173">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-174">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-175">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-176">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-177">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-178">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-179">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-180">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="45ed3-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-181">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-182">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-183">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-184">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-185">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-186">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-187">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-188">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-189">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-190">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="45ed3-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-191">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-192">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-193">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-194">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-195">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-196">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-197">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-198">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-199">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-200">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="45ed3-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-201">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-202">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-203">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-204">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-205">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-206">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-207">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-208">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-209">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-210">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="45ed3-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-211">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-212">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-213">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-214">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-215">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-216">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-218">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-219">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-220">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-221">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-222">
                    <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-223">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-224">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-225">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-226">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-228">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-229">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-230">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-231">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-232">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-233">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-234">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-235">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-236">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-237">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="45ed3-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-239">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-240">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-241">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-242">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-243">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-244">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-245">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-246">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-247">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="45ed3-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="45ed3-249">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-250">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-251">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-252">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-253">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-254">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-255">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-256">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-257">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-258">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="45ed3-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-260">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-261">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-262">Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-263">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-264">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-265">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="45ed3-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="45ed3-266">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="45ed3-267">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="45ed3-268">Oui</span><span class="sxs-lookup"><span data-stu-id="45ed3-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="45ed3-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="45ed3-270">Projet entier</span><span class="sxs-lookup"><span data-stu-id="45ed3-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="45ed3-271">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="45ed3-272">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="45ed3-273">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="45ed3-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="45ed3-274">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-275">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="45ed3-276">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="45ed3-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
