---
title: Chiffres réels
description: Cette rubrique fournit des informations sur les chiffres réels du projet.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168115"
---
# <a name="actuals"></a><span data-ttu-id="655ba-103">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="655ba-104">Les chiffres réels sont la quantité de travail effectuée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="655ba-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="655ba-105">Les chiffres réels du projet peuvent être retracés jusqu'à leurs documents origine.</span><span class="sxs-lookup"><span data-stu-id="655ba-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="655ba-106">Ces documents origine incluent les écritures de temps, de dépenses et de journal, ainsi que les factures.</span><span class="sxs-lookup"><span data-stu-id="655ba-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Comment les chiffres réels du projet de planification sont retracés jusqu'aux documents origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="655ba-108">Envoi d'une entrée de temps</span><span class="sxs-lookup"><span data-stu-id="655ba-108">Submitting a time entry</span></span>

<span data-ttu-id="655ba-109">Dans PSA, quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="655ba-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="655ba-110">Une ligne est pour le coût, tandis que l'autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="655ba-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="655ba-111">Quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="655ba-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="655ba-112">La logique d'entrée des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="655ba-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="655ba-113">Toutes les valeurs de champ d'une entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="655ba-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="655ba-114">Ces champs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="655ba-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="655ba-115">Les champs qui touchent les prix par défaut, par exemple **Rôle** et **Unité d'organisation**, entraînent un tarif approprié à entrer par défaut sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="655ba-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="655ba-116">Si vous ajoutez un champ personnalisé à l'entrée de temps, et que vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l'entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l'entrée de temps dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="655ba-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="655ba-117">Envoi d'une entrée de dépenses</span><span class="sxs-lookup"><span data-stu-id="655ba-117">Submitting an expense entry</span></span>

<span data-ttu-id="655ba-118">Dans PSA, quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="655ba-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="655ba-119">Une ligne est pour le coût, tandis que l'autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="655ba-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="655ba-120">Quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="655ba-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="655ba-121">La logique d'entrée des prix par défaut pour les dépenses est basée sur la catégorie de dépenses sélectionnée sur la page **Entrée de dépense**.</span><span class="sxs-lookup"><span data-stu-id="655ba-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="655ba-122">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="655ba-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="655ba-123">Toutefois, pour le prix lui-même, le montant que l'utilisateur a entré est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes par défaut.</span><span class="sxs-lookup"><span data-stu-id="655ba-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="655ba-124">Dans la version actuelle de PSA, l'entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="655ba-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="655ba-125">Utilisation des journaux pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="655ba-125">Using journals to record costs</span></span>

<span data-ttu-id="655ba-126">Dans PSA, les journaux vous permettent d'enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="655ba-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="655ba-127">Un journal comporte un en-tête, des lignes, puis une action **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="655ba-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="655ba-128">Voici quelques scénarios où vous pourriez utiliser un journal :</span><span class="sxs-lookup"><span data-stu-id="655ba-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="655ba-129">Vous devez enregistrer les coûts et les ventes réels des matériaux sur un projet.</span><span class="sxs-lookup"><span data-stu-id="655ba-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="655ba-130">Vous devez déplacer des chiffres réels de la transaction d'un autre système à PSA.</span><span class="sxs-lookup"><span data-stu-id="655ba-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="655ba-131">Vous devez enregistrer les coûts qui se sont produits dans un autre système, tel que les coûts d'approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="655ba-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="655ba-132">Enregistrement des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-132">Recording actuals based on project events</span></span>

<span data-ttu-id="655ba-133">PSA enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="655ba-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="655ba-134">Ces transactions sont enregistrées comme **chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="655ba-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="655ba-135">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu'il s'agit d'un projet basé sur la durée et les matériaux ou d'un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d'un projet interne.</span><span class="sxs-lookup"><span data-stu-id="655ba-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="655ba-136">**La ressource appartient à la même unité d'organisation que l'unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="655ba-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="655ba-137">Event</span><span class="sxs-lookup"><span data-stu-id="655ba-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="655ba-138">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="655ba-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="655ba-139">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="655ba-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="655ba-140">Projet interne</span><span class="sxs-lookup"><span data-stu-id="655ba-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="655ba-141">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="655ba-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="655ba-142">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="655ba-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="655ba-143">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-143">Actuals</span></span></th>
<th><span data-ttu-id="655ba-144">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="655ba-144">Transaction currency</span></span></th>
<th><span data-ttu-id="655ba-145">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="655ba-145">Fixed price</span></span></th>
<th><span data-ttu-id="655ba-146">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="655ba-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="655ba-147">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="655ba-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="655ba-148">Aucune activité dans l'entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-149">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="655ba-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="655ba-150">Aucune activité dans l'entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="655ba-151">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l'approbation.</span><span class="sxs-lookup"><span data-stu-id="655ba-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="655ba-152">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-152">Cost actual</span></span></td>
<td><span data-ttu-id="655ba-153">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-154">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-155">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="655ba-156">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-157">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-158">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="655ba-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="655ba-159">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="655ba-160">Le temps est approuvé, et une diminution des heures facturables survient au cours de l'approbation.</span><span class="sxs-lookup"><span data-stu-id="655ba-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="655ba-161">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-161">Cost actual</span></span></td>
<td><span data-ttu-id="655ba-162">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-163">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-164">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-165">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-166">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-167">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-168">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-169">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-170">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="655ba-171">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="655ba-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="655ba-172">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="655ba-173">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-174">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="655ba-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-175">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-176">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-177">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-178">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-178">Billed sales</span></span></td>
<td><span data-ttu-id="655ba-179">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="655ba-180">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="655ba-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="655ba-181">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="655ba-182">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-183">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-184">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-185">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-187">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-188">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-189">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-190">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="655ba-191">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="655ba-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="655ba-192">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="655ba-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="655ba-193">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="655ba-194">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="655ba-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="655ba-195">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="655ba-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="655ba-196">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-197">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-198">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-199">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-199">Billed sales</span></span></td>
<td><span data-ttu-id="655ba-200">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="655ba-201">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="655ba-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="655ba-202">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="655ba-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="655ba-203">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-204">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-205">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-206">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-207">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="655ba-208">**La ressource appartient à une unité d'organisation différente de l'unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="655ba-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="655ba-209">Event</span><span class="sxs-lookup"><span data-stu-id="655ba-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="655ba-210">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="655ba-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="655ba-211">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="655ba-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="655ba-212">Projet interne</span><span class="sxs-lookup"><span data-stu-id="655ba-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="655ba-213">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="655ba-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="655ba-214">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="655ba-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="655ba-215">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-215">Actuals</span></span></th>
<th><span data-ttu-id="655ba-216">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="655ba-216">Transaction currency</span></span></th>
<th><span data-ttu-id="655ba-217">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="655ba-217">Fixed price</span></span></th>
<th><span data-ttu-id="655ba-218">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="655ba-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="655ba-219">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="655ba-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="655ba-220">Aucune activité dans l'entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-221">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="655ba-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="655ba-222">Aucune activité dans l'entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="655ba-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="655ba-223">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l'approbation.</span><span class="sxs-lookup"><span data-stu-id="655ba-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="655ba-224">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-224">Cost actual</span></span></td>
<td><span data-ttu-id="655ba-225">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="655ba-226">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="655ba-227">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="655ba-228">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="655ba-229">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-230">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="655ba-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="655ba-231">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-232">Coût unitaire d'allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="655ba-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="655ba-233">Devise de l'unité d'allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="655ba-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-234">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="655ba-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="655ba-235">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="655ba-236">Le temps est approuvé, et une diminution des heures facturables survient au cours de l'approbation.</span><span class="sxs-lookup"><span data-stu-id="655ba-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="655ba-237">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-237">Cost actual</span></span></td>
<td><span data-ttu-id="655ba-238">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-239">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-240">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-241">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-242">Coût réel</span><span class="sxs-lookup"><span data-stu-id="655ba-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-243">Coût unitaire d'allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="655ba-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="655ba-244">Devise de l'unité d'allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="655ba-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-245">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="655ba-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="655ba-246">Devise de l'unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="655ba-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-247">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-248">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-249">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-250">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="655ba-251">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="655ba-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="655ba-252">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="655ba-253">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-254">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="655ba-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-255">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-256">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="655ba-257">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-258">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-258">Billed sales</span></span></td>
<td><span data-ttu-id="655ba-259">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="655ba-260">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="655ba-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="655ba-261">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="655ba-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-263">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-264">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-265">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="655ba-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-267">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-268">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-269">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-270">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="655ba-271">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="655ba-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="655ba-272">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="655ba-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="655ba-273">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="655ba-274">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="655ba-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="655ba-275">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="655ba-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="655ba-276">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-277">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="655ba-278">Non applicable</span><span class="sxs-lookup"><span data-stu-id="655ba-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-279">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="655ba-279">Billed sales</span></span></td>
<td><span data-ttu-id="655ba-280">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="655ba-281">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="655ba-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="655ba-282">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="655ba-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="655ba-283">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-284">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="655ba-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="655ba-285">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="655ba-286">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="655ba-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="655ba-287">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="655ba-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
