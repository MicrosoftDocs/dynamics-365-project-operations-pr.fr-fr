---
title: Configurer les composants facturables d’une ligne de contrat basée sur un projet
description: Cette rubrique fournit des informations sur l’ajout de composants facturables aux lignes de contrat dans Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003718"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="6a28e-103">Configurer les composants facturables d’une ligne de contrat basée sur un projet</span><span class="sxs-lookup"><span data-stu-id="6a28e-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="6a28e-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="6a28e-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6a28e-105">Une ligne de contrat basée sur un projet a les composants *inclus* et *payant*.</span><span class="sxs-lookup"><span data-stu-id="6a28e-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="6a28e-106">Les composants inclus sont des composants soumis à :</span><span class="sxs-lookup"><span data-stu-id="6a28e-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="6a28e-107">Méthode de facturation et répartition des clients</span><span class="sxs-lookup"><span data-stu-id="6a28e-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="6a28e-108">Limites à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="6a28e-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="6a28e-109">Paramètres de fréquence de facturation définis sur la ligne de contrat basée sur le projet</span><span class="sxs-lookup"><span data-stu-id="6a28e-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="6a28e-110">Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**.</span><span class="sxs-lookup"><span data-stu-id="6a28e-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="6a28e-111">Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de contrat :</span><span class="sxs-lookup"><span data-stu-id="6a28e-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="6a28e-112">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-112">Chargeable</span></span>
  - <span data-ttu-id="6a28e-113">Non facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-113">Non-chargeable</span></span>

<span data-ttu-id="6a28e-114">Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="6a28e-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="6a28e-115">La tarification est définie sur les tâches pour une ligne de contrat de projet et s’applique à toutes les classes de transaction incluses sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="6a28e-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="6a28e-116">Si le champ **Inclure les tâches** sur une ligne de contrat est vide ou est défini sur **Projet entier**, l’onglet **Tâches payantes** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6a28e-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="6a28e-117">La tarification est définie sur les rôles pour une ligne de contrat de projet s’applique uniquement à la classe de transaction **Temps**.</span><span class="sxs-lookup"><span data-stu-id="6a28e-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="6a28e-118">Si le champ **Inclure le temps** sur une ligne de contrat est défini sur **Non**, l’onglet **Rôles facturables** ne sera pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6a28e-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="6a28e-119">La tarification est définie sur les catégories de transaction pour une ligne de contrat de projet et s’applique uniquement à la classe de transaction **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="6a28e-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="6a28e-120">Si le champ **Inclure les dépenses** sur une ligne de contrat est défini sur **Non**, l’onglet **Catégories facturables** ne sera pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6a28e-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6a28e-121">Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="6a28e-122">Une tâche de projet peut être facturable ou non sur une ligne de contrat spécifique, ce qui rend possible la configuration suivante :</span><span class="sxs-lookup"><span data-stu-id="6a28e-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="6a28e-123">Si une ligne de contrat basée sur un projet comprend **Temps** et une certaine tâche, **T1** y est associé comme payant.</span><span class="sxs-lookup"><span data-stu-id="6a28e-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="6a28e-124">S’il y a une deuxième ligne de contrat qui inclut **Dépenses**, vous pouvez associer la tâche T1 sur la ligne de contrat comme non facturable.</span><span class="sxs-lookup"><span data-stu-id="6a28e-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="6a28e-125">Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses sont non facturables.</span><span class="sxs-lookup"><span data-stu-id="6a28e-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="6a28e-126">Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de contrat en mettant à jour le champ **Type de facturation** dans la sous-grille des tâches de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a28e-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="6a28e-127">Vous pouvez également mettre à jour le champ **Type de facturation** dans la sous-grille Configuration de la facturation de la tâche d’un projet qui affiche les lignes de contrat associées à une tâche.</span><span class="sxs-lookup"><span data-stu-id="6a28e-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6a28e-128">Mettre à jour un rôle pour qu’il soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="6a28e-129">Un rôle peut être facturable ou non facturable sur une ligne de contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a28e-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6a28e-130">Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles payants** d’une ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a28e-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="6a28e-131">Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.</span><span class="sxs-lookup"><span data-stu-id="6a28e-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6a28e-132">Mettre à jour une catégorie de transaction comme facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="6a28e-133">Une catégorie de transaction peut être facturable ou non facturable sur une ligne de contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a28e-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6a28e-134">Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** d’une ligne de contrat basée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="6a28e-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="6a28e-135">Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.</span><span class="sxs-lookup"><span data-stu-id="6a28e-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="6a28e-136">Résoudre la chargeabilité</span><span class="sxs-lookup"><span data-stu-id="6a28e-136">Resolve chargeability</span></span>

<span data-ttu-id="6a28e-137">Une estimation ou un chiffre réel créé pour le temps n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="6a28e-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="6a28e-138">**Temps** est inclus dans la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a28e-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="6a28e-139">**Rôle** est configuré comme facturable sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a28e-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="6a28e-140">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a28e-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="6a28e-141">Si ces trois éléments sont vrais, la tâche est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="6a28e-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="6a28e-142">Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="6a28e-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="6a28e-143">**Dépense** est inclus dans la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="6a28e-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="6a28e-144">**Catégorie de transaction** est configuré comme facturable sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="6a28e-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="6a28e-145">**Tâches incluses** est défini sur **Tâche sélectionnée** sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="6a28e-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="6a28e-146">Si ces trois éléments sont vrais, la **Tâche** est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="6a28e-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="6a28e-147">Une estimation ou un chiffre réel créé pour du matériel n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="6a28e-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="6a28e-148">**Matériel** est inclus dans la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="6a28e-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="6a28e-149">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="6a28e-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="6a28e-150">Si ces deux éléments sont vrais, la **Tâche** est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="6a28e-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-151">
                    <strong>Inclut le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6a28e-152">
                    <strong>Inclut la dépense</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6a28e-153">
                    <strong>Inclut le matériel</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="6a28e-154">
                    <strong>Tâches incluses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-155">
                    <strong>Rôle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-156">
                    <strong>Catégorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-157">
                    <strong>Tâche</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="6a28e-158">
                    <strong>Impact sur le fait que l’élément soit facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-159">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-160">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-161">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-162">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-163">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-164">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-165">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-166">Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-167">Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-168">Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-169">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-170">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-171">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-172">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="6a28e-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-173">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-174">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-175">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-176">Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-177">Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-178">Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-179">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-180">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-181">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-182">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="6a28e-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-183">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-184">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-185">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-186">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-187">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6a28e-188">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-189">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-190">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-191">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-192">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="6a28e-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-193">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-194">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-195">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-196">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-197">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-198">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-199">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-200">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-201">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-202">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="6a28e-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-203">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-204">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-205">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-206">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-207">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-208">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-209">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-210">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-211">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-212">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="6a28e-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-213">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-214">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-215">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-216">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-217">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-218">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-220">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-221">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-222">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-223">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-224">
                    <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-225">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-226">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-227">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6a28e-228">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-230">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-231">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-232">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-233">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-234">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-235">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-236">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-237">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-238">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-239">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6a28e-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-241">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-242">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-243">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-244">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-245">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-246">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6a28e-247">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-248">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-249">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6a28e-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6a28e-251">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-252">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-253">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-254">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-255">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-256">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-257">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-258">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-259">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-260">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6a28e-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-262">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-263">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-264">Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-265">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-266">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6a28e-267">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="6a28e-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6a28e-268">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6a28e-269">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6a28e-270">Oui</span><span class="sxs-lookup"><span data-stu-id="6a28e-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6a28e-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6a28e-272">Projet entier</span><span class="sxs-lookup"><span data-stu-id="6a28e-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6a28e-273">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6a28e-274">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6a28e-275">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="6a28e-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6a28e-276">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-277">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6a28e-278">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a28e-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
