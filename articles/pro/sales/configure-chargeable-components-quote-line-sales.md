---
title: Configurer les composants facturables d’une ligne de devis
description: Cette rubrique fournit des informations sur la configuration de composants payants et non facturables sur une ligne de devis basée sur un projet.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003763"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="49749-103">Configurer les composants facturables d’une ligne de devis</span><span class="sxs-lookup"><span data-stu-id="49749-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="49749-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="49749-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="49749-105">Une ligne de devis basée sur un projet a le concept des composants *inclus* et *payant*.</span><span class="sxs-lookup"><span data-stu-id="49749-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="49749-106">Les composants inclus sont soumis à :</span><span class="sxs-lookup"><span data-stu-id="49749-106">Included components are subject to:</span></span>

  - <span data-ttu-id="49749-107">Méthode de facturation et répartition des clients</span><span class="sxs-lookup"><span data-stu-id="49749-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="49749-108">Limites à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="49749-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="49749-109">Paramètres de fréquence de facturation définis sur la ligne de devis basée sur le projet</span><span class="sxs-lookup"><span data-stu-id="49749-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="49749-110">Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**.</span><span class="sxs-lookup"><span data-stu-id="49749-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="49749-111">Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de devis :</span><span class="sxs-lookup"><span data-stu-id="49749-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="49749-112">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-112">Chargeable</span></span>
  - <span data-ttu-id="49749-113">Non facturable</span><span class="sxs-lookup"><span data-stu-id="49749-113">Non-chargeable</span></span>

<span data-ttu-id="49749-114">Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="49749-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="49749-115">La tarification est définie sur les tâches pour une ligne de devis et s’applique à toutes les classes de transaction incluses sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="49749-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="49749-116">Si le champ **Inclure les tâches** est défini sur **Projet entier** ou laissé vide, l’onglet **Tâches payantes** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="49749-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="49749-117">La tarification est définie sur les rôles pour une ligne de devis et s’applique uniquement à la classe de transaction **Temps**.</span><span class="sxs-lookup"><span data-stu-id="49749-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="49749-118">Si le champ **Inclure le temps** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Rôles facturables** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="49749-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="49749-119">La tarification est définie sur les catégories de transaction pour une ligne de devis et s’applique uniquement à la classe de transaction **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="49749-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="49749-120">Si le champ **Inclure les dépenses** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Catégories facturables** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="49749-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="49749-121">Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="49749-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="49749-122">Une tâche de projet peut être facturable ou non dans le contexte d’une ligne de devis basée sur un projet spécifique, ce qui rend possible la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="49749-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="49749-123">Si une ligne de devis basée sur un projet comprend **Temps** et la tâche **T1**, la tâche est associée à la ligne de devis comme facturable.</span><span class="sxs-lookup"><span data-stu-id="49749-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="49749-124">S’il y a une deuxième ligne de devis qui inclut **Dépenses**, vous pouvez associer la tâche **T1** sur la ligne de devis comme non facturable.</span><span class="sxs-lookup"><span data-stu-id="49749-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="49749-125">Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses enregistrées sur la tâche sont non facturables.</span><span class="sxs-lookup"><span data-stu-id="49749-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="49749-126">Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Tâches de la ligne de contrat**.</span><span class="sxs-lookup"><span data-stu-id="49749-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="49749-127">Vous pouvez également mettre à jour le type de facturation d’une tâche de projet dans le champ **Type de facturation** dans la sous-grille dans la configuration de la facturation de la tâche d’un projet qui affiche les lignes de devis associées à une tâche.</span><span class="sxs-lookup"><span data-stu-id="49749-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="49749-128">Mettre à jour un rôle pour qu’il soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="49749-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="49749-129">Un rôle peut être payant ou non dans le contexte d’une ligne de devis spécifique à un projet.</span><span class="sxs-lookup"><span data-stu-id="49749-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="49749-130">Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.</span><span class="sxs-lookup"><span data-stu-id="49749-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="49749-131">Mettre à jour une catégorie de transaction comme facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="49749-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="49749-132">Une catégorie de transaction peut être facturable ou non facturable sur une ligne de devis spécifique.</span><span class="sxs-lookup"><span data-stu-id="49749-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="49749-133">Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.</span><span class="sxs-lookup"><span data-stu-id="49749-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="49749-134">Résoudre la chargeabilité</span><span class="sxs-lookup"><span data-stu-id="49749-134">Resolve chargeability</span></span>
<span data-ttu-id="49749-135">Une estimation ou un chiffre réel créé pour le temps ne sera considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="49749-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="49749-136">**Temps** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="49749-137">**Rôle** est configuré comme facturable sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="49749-138">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="49749-139">Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="49749-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="49749-140">Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="49749-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="49749-141">**Dépense** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="49749-142">**Catégorie de transaction** est configuré comme facturable sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="49749-143">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="49749-144">Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="49749-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="49749-145">Une estimation ou un chiffre réel créé pour du matériel ne sera considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="49749-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="49749-146">**Matériel** est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="49749-147">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="49749-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="49749-148">Si ces deux éléments sont vrais, la **Tâche** doit également être configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="49749-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-149">
                    <strong>Inclut le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="49749-150">
                    <strong>Inclut la dépense</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="49749-151">
                    <strong>Inclut le matériel</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="49749-152">
                    <strong>Tâches incluses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-153">
                    <strong>Rôle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-154">
                    <strong>Catégorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-155">
                    <strong>Tâche</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="49749-156">
                    <strong>Impact sur le fait que l’élément soit facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-157">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-158">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-159">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-160">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-161">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-162">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-163">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-164">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-165">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="49749-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-166">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-167">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-168">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-169">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-170">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="49749-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-171">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-172">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-173">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-174">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-175">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="49749-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-176">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-177">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-178">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-179">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-180">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="49749-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-181">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-182">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-183">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-184">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-185">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="49749-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-186">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-187">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-188">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-189">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-190">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="49749-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-191">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-192">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-193">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-194">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-195">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-196">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-197">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-198">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-199">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-200">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="49749-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-201">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-202">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-203">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-204">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-205">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-206">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-207">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-208">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-209">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-210">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="49749-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-211">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-212">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-213">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-214">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-215">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-216">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-218">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-219">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-220">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-221">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-222">
                    <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-223">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-224">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-225">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="49749-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-226">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-228">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-229">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-230">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-231">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-232">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-233">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-234">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-235">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-236">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-237">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="49749-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-239">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-240">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-241">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-242">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-243">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-244">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-245">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-246">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-247">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="49749-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="49749-249">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-250">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-251">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-252">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-253">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-254">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-255">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-256">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-257">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-258">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="49749-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-260">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-261">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-262">Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-263">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-264">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="49749-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-265">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="49749-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="49749-266">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="49749-267">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="49749-268">Oui</span><span class="sxs-lookup"><span data-stu-id="49749-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="49749-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="49749-270">Projet entier</span><span class="sxs-lookup"><span data-stu-id="49749-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="49749-271">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="49749-272">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="49749-273">Ne peut pas être défini</span><span class="sxs-lookup"><span data-stu-id="49749-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="49749-274">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-275">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="49749-276">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="49749-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
