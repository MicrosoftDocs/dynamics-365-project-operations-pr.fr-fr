---
title: Chiffres réels
description: Cette rubrique fournit des informations sur la façon d’utiliser les chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075730"
---
# <a name="actuals"></a><span data-ttu-id="e17a2-103">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-103">Actuals</span></span> 

<span data-ttu-id="e17a2-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="e17a2-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e17a2-105">Les chiffres réels sont la quantité de travail effectuée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="e17a2-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="e17a2-106">Ils sont créés à la suite d’écritures de temps et de dépenses, d’écritures de journal et de factures.</span><span class="sxs-lookup"><span data-stu-id="e17a2-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="e17a2-107">Lignes de journal et envoi de temps</span><span class="sxs-lookup"><span data-stu-id="e17a2-107">Journal lines and time submission</span></span>

<span data-ttu-id="e17a2-108">Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e17a2-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e17a2-109">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="e17a2-109">Time and materials</span></span>

<span data-ttu-id="e17a2-110">Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="e17a2-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e17a2-111">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-111">Fixed price</span></span>

<span data-ttu-id="e17a2-112">Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="e17a2-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e17a2-113">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="e17a2-113">Default pricing</span></span>

<span data-ttu-id="e17a2-114">La logique de création des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="e17a2-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="e17a2-115">Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="e17a2-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="e17a2-116">Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="e17a2-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="e17a2-117">Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’organisation** , sont utilisés pour déterminer le tarif approprié à entrer par défaut sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="e17a2-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="e17a2-118">Vous pouvez ajouter un champ personnalisé sur l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="e17a2-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="e17a2-119">Si vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l’entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l’entrée de temps dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="e17a2-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="e17a2-120">Lignes de journal et envoi des dépenses de base</span><span class="sxs-lookup"><span data-stu-id="e17a2-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="e17a2-121">Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e17a2-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="e17a2-122">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="e17a2-122">Time and materials</span></span>

<span data-ttu-id="e17a2-123">Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="e17a2-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="e17a2-124">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-124">Fixed price</span></span>

<span data-ttu-id="e17a2-125">Quand une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="e17a2-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="e17a2-126">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="e17a2-126">Default pricing</span></span>

<span data-ttu-id="e17a2-127">La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses.</span><span class="sxs-lookup"><span data-stu-id="e17a2-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="e17a2-128">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="e17a2-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="e17a2-129">Toutefois, par défaut, le montant entré pour le prix lui-même est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes.</span><span class="sxs-lookup"><span data-stu-id="e17a2-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="e17a2-130">L’entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e17a2-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="e17a2-131">Utiliser des journaux pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="e17a2-131">Use entry journals to record costs</span></span>

<span data-ttu-id="e17a2-132">Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="e17a2-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="e17a2-133">Les journaux peuvent être utilisés aux fins suivantes :</span><span class="sxs-lookup"><span data-stu-id="e17a2-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="e17a2-134">Enregistrer les coûts réels du matériel et les ventes sur un projet.</span><span class="sxs-lookup"><span data-stu-id="e17a2-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="e17a2-135">Déplacer des chiffres réels de la transaction d’un autre système à Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e17a2-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="e17a2-136">Enregistrer les coûts survenus dans un autre système.</span><span class="sxs-lookup"><span data-stu-id="e17a2-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="e17a2-137">Ces coûts peuvent inclure des coûts d’approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="e17a2-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e17a2-138">L’application ne valide pas le type de ligne de journal ou la tarification associée qui est saisie sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="e17a2-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="e17a2-139">Par conséquent, seul un utilisateur pleinement conscient de l’impact comptable des chiffres réels sur le projet doit utiliser des journaux d’entrées pour créer des chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="e17a2-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="e17a2-140">En raison de l’impact de ce type de journal, vous devez choisir soigneusement qui a accès pour créer des journaux d’entrées.</span><span class="sxs-lookup"><span data-stu-id="e17a2-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="e17a2-141">Enregistrer des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-141">Record actuals based on project events</span></span>

<span data-ttu-id="e17a2-142">Project Operations enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="e17a2-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="e17a2-143">Ces transactions sont enregistrées comme chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="e17a2-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="e17a2-144">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="e17a2-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="e17a2-145">La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e17a2-146">Event</span><span class="sxs-lookup"><span data-stu-id="e17a2-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e17a2-147">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="e17a2-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e17a2-148">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="e17a2-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e17a2-149">Projet interne</span><span class="sxs-lookup"><span data-stu-id="e17a2-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e17a2-150">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="e17a2-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e17a2-151">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e17a2-152">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-152">Actuals</span></span></th>
<th><span data-ttu-id="e17a2-153">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="e17a2-153">Transaction currency</span></span></th>
<th><span data-ttu-id="e17a2-154">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-154">Fixed price</span></span></th>
<th><span data-ttu-id="e17a2-155">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="e17a2-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e17a2-156">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="e17a2-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e17a2-157">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-158">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="e17a2-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e17a2-159">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e17a2-160">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="e17a2-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e17a2-161">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-161">Cost actual</span></span></td>
<td><span data-ttu-id="e17a2-162">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-163">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-164">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="e17a2-165">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-166">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-167">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="e17a2-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e17a2-168">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e17a2-169">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="e17a2-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e17a2-170">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-170">Cost actual</span></span></td>
<td><span data-ttu-id="e17a2-171">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-172">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-173">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-174">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-175">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-176">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-177">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-178">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-179">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e17a2-180">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="e17a2-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e17a2-181">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e17a2-182">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-183">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="e17a2-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-184">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-185">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-187">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-187">Billed sales</span></span></td>
<td><span data-ttu-id="e17a2-188">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e17a2-189">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="e17a2-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e17a2-190">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e17a2-191">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-192">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-193">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-194">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-195">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-196">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-197">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-198">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e17a2-200">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="e17a2-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e17a2-201">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="e17a2-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e17a2-202">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e17a2-203">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="e17a2-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e17a2-204">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="e17a2-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e17a2-205">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-206">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-207">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-208">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-208">Billed sales</span></span></td>
<td><span data-ttu-id="e17a2-209">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e17a2-210">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="e17a2-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e17a2-211">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="e17a2-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e17a2-212">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-213">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-214">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-215">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-216">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="e17a2-217">La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="e17a2-218">Event</span><span class="sxs-lookup"><span data-stu-id="e17a2-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="e17a2-219">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="e17a2-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="e17a2-220">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="e17a2-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="e17a2-221">Projet interne</span><span class="sxs-lookup"><span data-stu-id="e17a2-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="e17a2-222">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="e17a2-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="e17a2-223">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e17a2-224">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-224">Actuals</span></span></th>
<th><span data-ttu-id="e17a2-225">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="e17a2-225">Transaction currency</span></span></th>
<th><span data-ttu-id="e17a2-226">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="e17a2-226">Fixed price</span></span></th>
<th><span data-ttu-id="e17a2-227">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="e17a2-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e17a2-228">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="e17a2-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="e17a2-229">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-230">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="e17a2-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="e17a2-231">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="e17a2-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="e17a2-232">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="e17a2-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e17a2-233">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-233">Cost actual</span></span></td>
<td><span data-ttu-id="e17a2-234">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e17a2-235">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e17a2-236">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="e17a2-237">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="e17a2-238">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-239">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="e17a2-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="e17a2-240">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-241">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="e17a2-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e17a2-242">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="e17a2-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-243">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="e17a2-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e17a2-244">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="e17a2-245">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="e17a2-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="e17a2-246">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-246">Cost actual</span></span></td>
<td><span data-ttu-id="e17a2-247">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-248">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-249">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-250">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-251">Coût réel</span><span class="sxs-lookup"><span data-stu-id="e17a2-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-252">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="e17a2-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="e17a2-253">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="e17a2-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-254">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="e17a2-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="e17a2-255">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="e17a2-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-256">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-257">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-258">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-259">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e17a2-260">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="e17a2-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e17a2-261">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e17a2-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-263">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="e17a2-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-264">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-265">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="e17a2-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-267">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-267">Billed sales</span></span></td>
<td><span data-ttu-id="e17a2-268">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e17a2-269">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="e17a2-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="e17a2-270">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="e17a2-271">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-272">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-273">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-274">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="e17a2-275">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-276">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-277">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-278">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="e17a2-280">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="e17a2-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e17a2-281">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="e17a2-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e17a2-282">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="e17a2-283">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="e17a2-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="e17a2-284">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="e17a2-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="e17a2-285">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-286">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="e17a2-287">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e17a2-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-288">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="e17a2-288">Billed sales</span></span></td>
<td><span data-ttu-id="e17a2-289">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="e17a2-290">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="e17a2-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="e17a2-291">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="e17a2-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="e17a2-292">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-293">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="e17a2-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="e17a2-294">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e17a2-295">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="e17a2-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="e17a2-296">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="e17a2-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
