---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291796"
---
# <a name="actuals"></a><span data-ttu-id="de768-103">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-103">Actuals</span></span> 

<span data-ttu-id="de768-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="de768-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="de768-105">Les chiffres réels sont la quantité de travail effectuée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="de768-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="de768-106">Ils sont créés à la suite d’écritures de temps et de dépenses, d’écritures de journal et de factures.</span><span class="sxs-lookup"><span data-stu-id="de768-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="de768-107">Lignes de journal et envoi de temps</span><span class="sxs-lookup"><span data-stu-id="de768-107">Journal lines and time submission</span></span>

<span data-ttu-id="de768-108">Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de768-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="de768-109">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="de768-109">Time and materials</span></span>

<span data-ttu-id="de768-110">Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="de768-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="de768-111">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-111">Fixed price</span></span>

<span data-ttu-id="de768-112">Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="de768-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="de768-113">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="de768-113">Default pricing</span></span>

<span data-ttu-id="de768-114">La logique de création des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="de768-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="de768-115">Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="de768-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="de768-116">Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="de768-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="de768-117">Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’organisation**, sont utilisés pour déterminer le tarif approprié à entrer par défaut sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="de768-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="de768-118">Vous pouvez ajouter un champ personnalisé sur l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="de768-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="de768-119">Si vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l’entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l’entrée de temps dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="de768-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="de768-120">Lignes de journal et envoi des dépenses de base</span><span class="sxs-lookup"><span data-stu-id="de768-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="de768-121">Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de768-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="de768-122">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="de768-122">Time and materials</span></span>

<span data-ttu-id="de768-123">Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="de768-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="de768-124">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-124">Fixed price</span></span>

<span data-ttu-id="de768-125">Quand une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="de768-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="de768-126">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="de768-126">Default pricing</span></span>

<span data-ttu-id="de768-127">La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses.</span><span class="sxs-lookup"><span data-stu-id="de768-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="de768-128">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="de768-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="de768-129">Toutefois, par défaut, le montant entré pour le prix lui-même est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes.</span><span class="sxs-lookup"><span data-stu-id="de768-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="de768-130">L’entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="de768-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="de768-131">Utiliser des journaux pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="de768-131">Use entry journals to record costs</span></span>

<span data-ttu-id="de768-132">Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="de768-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="de768-133">Les journaux peuvent être utilisés aux fins suivantes :</span><span class="sxs-lookup"><span data-stu-id="de768-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="de768-134">Enregistrer les coûts réels du matériel et les ventes sur un projet.</span><span class="sxs-lookup"><span data-stu-id="de768-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="de768-135">Déplacer les chiffres réels de transactions d’un autre système vers Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="de768-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="de768-136">Enregistrer les coûts survenus dans un autre système.</span><span class="sxs-lookup"><span data-stu-id="de768-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="de768-137">Ces coûts peuvent inclure des coûts d’approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="de768-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de768-138">L’application ne valide pas le type de ligne de journal ou la tarification associée qui est saisie sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="de768-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="de768-139">Par conséquent, seul un utilisateur pleinement conscient de l’impact comptable des chiffres réels sur le projet doit utiliser des journaux d’entrées pour créer des chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="de768-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="de768-140">En raison de l’impact de ce type de journal, vous devez choisir soigneusement qui a accès pour créer des journaux d’entrées.</span><span class="sxs-lookup"><span data-stu-id="de768-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="de768-141">Enregistrer des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="de768-141">Record actuals based on project events</span></span>

<span data-ttu-id="de768-142">Project Operations enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="de768-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="de768-143">Ces transactions sont enregistrées comme chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="de768-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="de768-144">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="de768-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="de768-145">La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="de768-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="de768-146">Event</span><span class="sxs-lookup"><span data-stu-id="de768-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="de768-147">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="de768-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="de768-148">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="de768-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="de768-149">Projet interne</span><span class="sxs-lookup"><span data-stu-id="de768-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="de768-150">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="de768-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="de768-151">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="de768-152">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-152">Actuals</span></span></th>
<th><span data-ttu-id="de768-153">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="de768-153">Transaction currency</span></span></th>
<th><span data-ttu-id="de768-154">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-154">Fixed price</span></span></th>
<th><span data-ttu-id="de768-155">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="de768-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="de768-156">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="de768-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="de768-157">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-158">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="de768-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="de768-159">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="de768-160">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="de768-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="de768-161">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-161">Cost actual</span></span></td>
<td><span data-ttu-id="de768-162">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-163">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-164">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="de768-165">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-166">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-167">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="de768-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="de768-168">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="de768-169">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="de768-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="de768-170">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-170">Cost actual</span></span></td>
<td><span data-ttu-id="de768-171">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-172">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-173">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-174">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-175">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-176">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="de768-177">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-178">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-179">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="de768-180">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="de768-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="de768-181">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="de768-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="de768-182">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-183">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="de768-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-184">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-185">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-187">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="de768-187">Billed sales</span></span></td>
<td><span data-ttu-id="de768-188">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="de768-189">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="de768-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="de768-190">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="de768-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="de768-191">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-192">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-193">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-194">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-195">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-196">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="de768-197">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-198">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="de768-200">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="de768-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="de768-201">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="de768-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="de768-202">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="de768-203">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="de768-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="de768-204">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="de768-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="de768-205">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-206">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-207">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-208">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="de768-208">Billed sales</span></span></td>
<td><span data-ttu-id="de768-209">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="de768-210">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="de768-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="de768-211">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="de768-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="de768-212">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-213">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="de768-214">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-215">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-216">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="de768-217">La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="de768-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="de768-218">Event</span><span class="sxs-lookup"><span data-stu-id="de768-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="de768-219">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="de768-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="de768-220">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="de768-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="de768-221">Projet interne</span><span class="sxs-lookup"><span data-stu-id="de768-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="de768-222">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="de768-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="de768-223">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="de768-224">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-224">Actuals</span></span></th>
<th><span data-ttu-id="de768-225">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="de768-225">Transaction currency</span></span></th>
<th><span data-ttu-id="de768-226">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="de768-226">Fixed price</span></span></th>
<th><span data-ttu-id="de768-227">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="de768-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="de768-228">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="de768-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="de768-229">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-230">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="de768-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="de768-231">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="de768-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="de768-232">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="de768-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="de768-233">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-233">Cost actual</span></span></td>
<td><span data-ttu-id="de768-234">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="de768-235">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="de768-236">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="de768-237">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="de768-238">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-239">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="de768-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="de768-240">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-241">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="de768-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="de768-242">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="de768-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-243">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="de768-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="de768-244">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="de768-245">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="de768-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="de768-246">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-246">Cost actual</span></span></td>
<td><span data-ttu-id="de768-247">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-248">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-249">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-250">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-251">Coût réel</span><span class="sxs-lookup"><span data-stu-id="de768-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-252">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="de768-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="de768-253">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="de768-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-254">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="de768-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="de768-255">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="de768-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-256">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="de768-257">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-258">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-259">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="de768-260">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="de768-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="de768-261">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="de768-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="de768-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-263">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="de768-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-264">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-265">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="de768-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-267">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="de768-267">Billed sales</span></span></td>
<td><span data-ttu-id="de768-268">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="de768-269">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="de768-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="de768-270">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="de768-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="de768-271">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-272">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-273">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-274">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="de768-275">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-276">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="de768-277">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-278">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="de768-280">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="de768-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="de768-281">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="de768-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="de768-282">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="de768-283">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="de768-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="de768-284">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="de768-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="de768-285">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-286">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="de768-287">Non applicable</span><span class="sxs-lookup"><span data-stu-id="de768-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-288">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="de768-288">Billed sales</span></span></td>
<td><span data-ttu-id="de768-289">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="de768-290">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="de768-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="de768-291">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="de768-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="de768-292">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-293">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="de768-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="de768-294">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="de768-295">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="de768-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="de768-296">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="de768-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]