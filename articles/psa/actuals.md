---
title: Vue d’ensemble des chiffres réels
description: Cette rubrique fournit des informations sur les chiffres réels du projet.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146120"
---
# <a name="actuals-overview"></a><span data-ttu-id="64087-103">Vue d’ensemble des chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="64087-104">Les chiffres réels sont la quantité de travail effectuée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="64087-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="64087-105">Les chiffres réels du projet peuvent être retracés jusqu’à leurs documents origine.</span><span class="sxs-lookup"><span data-stu-id="64087-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="64087-106">Ces documents origine incluent les écritures de temps, de dépenses et de journal, ainsi que les factures.</span><span class="sxs-lookup"><span data-stu-id="64087-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Comment les chiffres réels du projet de planification sont retracés jusqu’aux documents origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="64087-108">Envoi d’une entrée de temps</span><span class="sxs-lookup"><span data-stu-id="64087-108">Submitting a time entry</span></span>

<span data-ttu-id="64087-109">Dans PSA, quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="64087-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="64087-110">Une ligne est pour le coût, tandis que l’autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="64087-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="64087-111">Quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="64087-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="64087-112">La logique d’entrée des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="64087-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="64087-113">Toutes les valeurs de champ d’une entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="64087-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="64087-114">Ces champs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="64087-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="64087-115">Les champs qui touchent les prix par défaut, par exemple **Rôle** et **Unité d’organisation**, entraînent un tarif approprié à entrer par défaut sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="64087-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="64087-116">Si vous ajoutez un champ personnalisé à l’entrée de temps, et que vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l’entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l’entrée de temps dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="64087-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="64087-117">Envoi d’une entrée de dépenses</span><span class="sxs-lookup"><span data-stu-id="64087-117">Submitting an expense entry</span></span>

<span data-ttu-id="64087-118">Dans PSA, quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="64087-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="64087-119">Une ligne est pour le coût, tandis que l’autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="64087-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="64087-120">Quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="64087-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="64087-121">La logique d’entrée des prix par défaut pour les dépenses est basée sur la catégorie de dépenses sélectionnée sur la page **Entrée de dépense**.</span><span class="sxs-lookup"><span data-stu-id="64087-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="64087-122">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="64087-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="64087-123">Toutefois, pour le prix lui-même, le montant que l’utilisateur a entré est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes par défaut.</span><span class="sxs-lookup"><span data-stu-id="64087-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="64087-124">Dans la version actuelle de PSA, l’entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="64087-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="64087-125">Utilisation des journaux d’entrées pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="64087-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="64087-126">Dans PSA, les journaux d’entrées vous permettent d’enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="64087-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="64087-127">Un journal comporte un en-tête, des lignes, puis une action **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="64087-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="64087-128">Voici quelques scénarios où vous pourriez utiliser un journal :</span><span class="sxs-lookup"><span data-stu-id="64087-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="64087-129">Vous devez enregistrer les coûts et les ventes réels des matériaux sur un projet.</span><span class="sxs-lookup"><span data-stu-id="64087-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="64087-130">Vous devez déplacer des chiffres réels de la transaction d’un autre système à PSA.</span><span class="sxs-lookup"><span data-stu-id="64087-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="64087-131">Vous devez enregistrer les coûts qui se sont produits dans un autre système, tel que les coûts d’approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="64087-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64087-132">L’utilisation des journaux d’entrées pour créer des chiffres réels ne doit être effectuée que par un utilisateur qui est pleinement conscient de l’impact comptable des chiffres réels sur le projet.</span><span class="sxs-lookup"><span data-stu-id="64087-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="64087-133">En effet, l’application ne valide pas le type de ligne de journal ou la tarification associée qui est entrée sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="64087-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="64087-134">En raison de l’impact de ce type de journal, choisissez attentivement les personnes autorisées à créer des journaux d’entrées.</span><span class="sxs-lookup"><span data-stu-id="64087-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="64087-135">Enregistrement des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="64087-135">Recording actuals based on project events</span></span>

<span data-ttu-id="64087-136">PSA enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="64087-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="64087-137">Ces transactions sont enregistrées comme **chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="64087-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="64087-138">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="64087-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="64087-139">**La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="64087-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64087-140">Event</span><span class="sxs-lookup"><span data-stu-id="64087-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64087-141">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="64087-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64087-142">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="64087-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64087-143">Projet interne</span><span class="sxs-lookup"><span data-stu-id="64087-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64087-144">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="64087-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64087-145">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="64087-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64087-146">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-146">Actuals</span></span></th>
<th><span data-ttu-id="64087-147">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="64087-147">Transaction currency</span></span></th>
<th><span data-ttu-id="64087-148">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="64087-148">Fixed price</span></span></th>
<th><span data-ttu-id="64087-149">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="64087-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64087-150">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="64087-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64087-151">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-152">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="64087-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64087-153">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64087-154">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="64087-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64087-155">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-155">Cost actual</span></span></td>
<td><span data-ttu-id="64087-156">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-157">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-158">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="64087-159">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-160">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-161">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="64087-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64087-162">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64087-163">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="64087-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64087-164">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-164">Cost actual</span></span></td>
<td><span data-ttu-id="64087-165">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-166">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-167">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-168">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-169">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-170">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64087-171">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-172">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-173">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64087-174">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="64087-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64087-175">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="64087-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64087-176">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-177">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="64087-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-178">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-179">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-180">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-181">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="64087-181">Billed sales</span></span></td>
<td><span data-ttu-id="64087-182">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64087-183">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="64087-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64087-184">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="64087-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64087-185">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-187">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-188">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-189">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-190">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64087-191">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-192">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-193">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64087-194">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="64087-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64087-195">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="64087-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64087-196">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64087-197">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="64087-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64087-198">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="64087-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64087-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-200">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-201">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-202">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="64087-202">Billed sales</span></span></td>
<td><span data-ttu-id="64087-203">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64087-204">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="64087-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64087-205">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="64087-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64087-206">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-207">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64087-208">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-209">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-210">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="64087-211">**La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="64087-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64087-212">Event</span><span class="sxs-lookup"><span data-stu-id="64087-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64087-213">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="64087-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64087-214">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="64087-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64087-215">Projet interne</span><span class="sxs-lookup"><span data-stu-id="64087-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64087-216">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="64087-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64087-217">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="64087-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64087-218">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-218">Actuals</span></span></th>
<th><span data-ttu-id="64087-219">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="64087-219">Transaction currency</span></span></th>
<th><span data-ttu-id="64087-220">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="64087-220">Fixed price</span></span></th>
<th><span data-ttu-id="64087-221">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="64087-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64087-222">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="64087-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64087-223">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-224">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="64087-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64087-225">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="64087-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="64087-226">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="64087-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64087-227">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-227">Cost actual</span></span></td>
<td><span data-ttu-id="64087-228">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64087-229">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64087-230">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64087-231">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64087-232">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-233">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="64087-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64087-234">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-235">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="64087-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64087-236">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="64087-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-237">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="64087-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64087-238">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="64087-239">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="64087-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64087-240">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-240">Cost actual</span></span></td>
<td><span data-ttu-id="64087-241">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-242">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-243">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-244">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-245">Coût réel</span><span class="sxs-lookup"><span data-stu-id="64087-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-246">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="64087-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64087-247">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="64087-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-248">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="64087-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64087-249">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="64087-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-250">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64087-251">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-252">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-253">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64087-254">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="64087-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64087-255">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="64087-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64087-256">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-257">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="64087-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-258">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-259">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64087-260">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-261">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="64087-261">Billed sales</span></span></td>
<td><span data-ttu-id="64087-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64087-263">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="64087-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64087-264">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="64087-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64087-265">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-267">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-268">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64087-269">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-270">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64087-271">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-272">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-273">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64087-274">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="64087-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64087-275">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="64087-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64087-276">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64087-277">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="64087-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64087-278">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="64087-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64087-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-280">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64087-281">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64087-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-282">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="64087-282">Billed sales</span></span></td>
<td><span data-ttu-id="64087-283">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64087-284">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="64087-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64087-285">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="64087-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64087-286">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-287">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="64087-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64087-288">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64087-289">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="64087-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64087-290">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="64087-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
