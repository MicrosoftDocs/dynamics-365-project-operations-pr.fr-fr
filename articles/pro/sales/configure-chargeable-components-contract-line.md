---
title: Configurer les composants facturables d’une ligne de contrat basée sur un projet
description: Cette rubrique fournit des informations sur l’ajout de composants facturables aux lignes de contrat dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858470"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="822e9-103">Configurer les composants facturables d’une ligne de contrat basée sur un projet</span><span class="sxs-lookup"><span data-stu-id="822e9-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="822e9-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="822e9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="822e9-105">Une ligne de contrat basée sur un projet a les composants *inclus* et *payant*.</span><span class="sxs-lookup"><span data-stu-id="822e9-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="822e9-106">Les composants inclus sont des composants soumis à :</span><span class="sxs-lookup"><span data-stu-id="822e9-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="822e9-107">Méthode de facturation et répartition des clients</span><span class="sxs-lookup"><span data-stu-id="822e9-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="822e9-108">Limites à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="822e9-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="822e9-109">Paramètres de fréquence de facturation définis sur la ligne de contrat basée sur le projet</span><span class="sxs-lookup"><span data-stu-id="822e9-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="822e9-110">Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**.</span><span class="sxs-lookup"><span data-stu-id="822e9-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="822e9-111">Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de contrat :</span><span class="sxs-lookup"><span data-stu-id="822e9-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="822e9-112">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-112">Chargeable</span></span>
  - <span data-ttu-id="822e9-113">Non facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-113">Non-chargeable</span></span>

<span data-ttu-id="822e9-114">Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.</span><span class="sxs-lookup"><span data-stu-id="822e9-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="822e9-115">La tarification est définie sur les tâches pour une ligne de contrat de projet et s’applique à toutes les classes de transaction incluses sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="822e9-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="822e9-116">Si le champ **Inclure les tâches** sur une ligne de contrat est vide ou est défini sur **Projet entier**, l’onglet **Tâches payantes** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="822e9-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="822e9-117">La tarification est définie sur les rôles pour une ligne de contrat de projet s’applique uniquement à la classe de transaction **Temps**.</span><span class="sxs-lookup"><span data-stu-id="822e9-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="822e9-118">Si le champ **Inclure le temps** sur une ligne de contrat est défini sur **Non**, l’onglet **Rôles facturables** ne sera pas disponible.</span><span class="sxs-lookup"><span data-stu-id="822e9-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="822e9-119">La tarification est définie sur les catégories de transaction pour une ligne de contrat de projet et s’applique uniquement à la classe de transaction **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="822e9-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="822e9-120">Si le champ **Inclure les dépenses** sur une ligne de contrat est défini sur **Non**, l’onglet **Catégories facturables** ne sera pas disponible.</span><span class="sxs-lookup"><span data-stu-id="822e9-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="822e9-121">Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="822e9-122">Une tâche de projet peut être facturable ou non sur une ligne de contrat spécifique, ce qui rend possible la configuration suivante :</span><span class="sxs-lookup"><span data-stu-id="822e9-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="822e9-123">Si une ligne de contrat basée sur un projet comprend **Temps** et une certaine tâche, **T1** y est associé comme payant.</span><span class="sxs-lookup"><span data-stu-id="822e9-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="822e9-124">S’il y a une deuxième ligne de contrat qui inclut **Dépenses**, vous pouvez associer la tâche T1 sur la ligne de contrat comme non facturable.</span><span class="sxs-lookup"><span data-stu-id="822e9-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="822e9-125">Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses sont non facturables.</span><span class="sxs-lookup"><span data-stu-id="822e9-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="822e9-126">Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de contrat en mettant à jour le champ **Type de facturation** dans la sous-grille des tâches de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="822e9-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="822e9-127">Vous pouvez également mettre à jour le champ **Type de facturation** dans la sous-grille Configuration de la facturation de la tâche d’un projet qui affiche les lignes de contrat associées à une tâche.</span><span class="sxs-lookup"><span data-stu-id="822e9-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="822e9-128">Mettre à jour un rôle pour qu’il soit facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="822e9-129">Un rôle peut être facturable ou non facturable sur une ligne de contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="822e9-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="822e9-130">Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles payants** d’une ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="822e9-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="822e9-131">Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.</span><span class="sxs-lookup"><span data-stu-id="822e9-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="822e9-132">Mettre à jour une catégorie de transaction comme facturable ou non facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="822e9-133">Une catégorie de transaction peut être facturable ou non facturable sur une ligne de contrat spécifique.</span><span class="sxs-lookup"><span data-stu-id="822e9-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="822e9-134">Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** d’une ligne de contrat basée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="822e9-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="822e9-135">Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.</span><span class="sxs-lookup"><span data-stu-id="822e9-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="822e9-136">Résoudre la chargeabilité</span><span class="sxs-lookup"><span data-stu-id="822e9-136">Resolve chargeability</span></span>

<span data-ttu-id="822e9-137">Une estimation ou un chiffre réel créé pour le temps n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="822e9-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="822e9-138">**Temps** est inclus dans la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="822e9-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="822e9-139">**Rôle** est configuré comme facturable sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="822e9-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="822e9-140">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="822e9-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="822e9-141">Si ces trois éléments sont vrais, la tâche est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="822e9-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="822e9-142">Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="822e9-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="822e9-143">**Dépense** est inclus dans la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="822e9-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="822e9-144">**Catégorie de transaction** est configuré comme facturable sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="822e9-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="822e9-145">**Tâches incluses** est défini sur **Tâche sélectionnée** sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="822e9-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="822e9-146">Si ces trois éléments sont vrais, la **Tâche** est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="822e9-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="822e9-147">Une estimation ou un chiffre réel créé pour du matériel n’est considéré comme facturable que si :</span><span class="sxs-lookup"><span data-stu-id="822e9-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="822e9-148">**Matériel** est inclus dans la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="822e9-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="822e9-149">**Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="822e9-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="822e9-150">Si ces deux éléments sont vrais, la **Tâche** est configurée comme facturable.</span><span class="sxs-lookup"><span data-stu-id="822e9-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-151">
                    <strong>Inclut le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="822e9-152">
                    <strong>Inclut la dépense</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="822e9-153">
                    <strong>Inclut le matériel</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="822e9-154">
                    <strong>Tâches incluses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-155">
                    <strong>Rôle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-156">
                    <strong>Catégorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-157">
                    <strong>Tâche</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="822e9-158">
                    <strong>Impact sur le fait que l’élément soit facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-159">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-160">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-161">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-162">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-163">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-164">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-165">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-166">Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-167">Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-168">Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-169">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-170">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-171">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-172">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="822e9-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-173">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-174">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-175">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-176">Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-177">Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-178">Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-179">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-180">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-181">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-182">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="822e9-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-183">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-184">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-185">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-186">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-187">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="822e9-188">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-189">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-190">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-191">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-192">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="822e9-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-193">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-194">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-195">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-196">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-197">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-198">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-199">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-200">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-201">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-202">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="822e9-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-203">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-204">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-205">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-206">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-207">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-208">Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-209">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-210">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-211">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-212">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="822e9-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-213">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-214">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-215">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-216">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-217">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-218">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-220">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-221">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-222">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-223">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-224">
                    <strong>Facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-225">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-226">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-227">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="822e9-228">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-230">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-231">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-232">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-233">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-234">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-235">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-236">Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-237">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-238">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-239">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="822e9-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-241">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-242">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-243">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-244">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-245">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-246">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="822e9-247">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-248">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-249">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="822e9-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="822e9-251">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-252">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-253">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-254">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-255">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-256">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-257">Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-258">Type de facturation à partir du chiffre réel de matériel : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-259">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-260">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="822e9-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-262">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-263">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-264">Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-265">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-266">Facturation à l’heure actuelle : Facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="822e9-267">Type de facturation sur les dépenses réelles : facturable</span><span class="sxs-lookup"><span data-stu-id="822e9-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="822e9-268">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="822e9-269">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="822e9-270">Oui</span><span class="sxs-lookup"><span data-stu-id="822e9-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="822e9-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="822e9-272">Projet entier</span><span class="sxs-lookup"><span data-stu-id="822e9-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="822e9-273">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="822e9-274">
                    <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="822e9-275">Impossible à définir</span><span class="sxs-lookup"><span data-stu-id="822e9-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="822e9-276">Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-277">Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="822e9-278">Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="822e9-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
