---
title: Vue d’ensemble des chiffres réels
description: Cette rubrique fournit des informations sur les chiffres réels du projet.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075938"
---
# <a name="actuals-overview"></a><span data-ttu-id="2a68d-103">Vue d’ensemble des chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2a68d-104">Les chiffres réels sont la quantité de travail effectuée sur un projet.</span><span class="sxs-lookup"><span data-stu-id="2a68d-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="2a68d-105">Les chiffres réels du projet peuvent être retracés jusqu'à leurs documents origine.</span><span class="sxs-lookup"><span data-stu-id="2a68d-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="2a68d-106">Ces documents origine incluent les écritures de temps, de dépenses et de journal, ainsi que les factures.</span><span class="sxs-lookup"><span data-stu-id="2a68d-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Comment les chiffres réels du projet de planification sont retracés jusqu'aux documents origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="2a68d-108">Envoi d'une entrée de temps</span><span class="sxs-lookup"><span data-stu-id="2a68d-108">Submitting a time entry</span></span>

<span data-ttu-id="2a68d-109">Dans PSA, quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="2a68d-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="2a68d-110">Une ligne est pour le coût, tandis que l'autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="2a68d-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="2a68d-111">Quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="2a68d-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="2a68d-112">La logique d'entrée des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="2a68d-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="2a68d-113">Toutes les valeurs de champ d'une entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="2a68d-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="2a68d-114">Ces champs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="2a68d-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="2a68d-115">Les champs qui touchent les prix par défaut, par exemple **Rôle** et **Unité d'organisation** , entraînent un tarif approprié à entrer par défaut sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="2a68d-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="2a68d-116">Si vous ajoutez un champ personnalisé à l'entrée de temps, et que vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l'entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l'entrée de temps dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="2a68d-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="2a68d-117">Envoi d'une entrée de dépenses</span><span class="sxs-lookup"><span data-stu-id="2a68d-117">Submitting an expense entry</span></span>

<span data-ttu-id="2a68d-118">Dans PSA, quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées.</span><span class="sxs-lookup"><span data-stu-id="2a68d-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="2a68d-119">Une ligne est pour le coût, tandis que l'autre est pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="2a68d-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="2a68d-120">Quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.</span><span class="sxs-lookup"><span data-stu-id="2a68d-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="2a68d-121">La logique d'entrée des prix par défaut pour les dépenses est basée sur la catégorie de dépenses sélectionnée sur la page **Entrée de dépense**.</span><span class="sxs-lookup"><span data-stu-id="2a68d-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="2a68d-122">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="2a68d-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="2a68d-123">Toutefois, pour le prix lui-même, le montant que l'utilisateur a entré est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a68d-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="2a68d-124">Dans la version actuelle de PSA, l'entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2a68d-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="2a68d-125">Utilisation des journaux d'entrées pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="2a68d-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="2a68d-126">Dans PSA, les journaux d'entrées vous permettent d'enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="2a68d-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="2a68d-127">Un journal comporte un en-tête, des lignes, puis une action **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="2a68d-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="2a68d-128">Voici quelques scénarios où vous pourriez utiliser un journal :</span><span class="sxs-lookup"><span data-stu-id="2a68d-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="2a68d-129">Vous devez enregistrer les coûts et les ventes réels des matériaux sur un projet.</span><span class="sxs-lookup"><span data-stu-id="2a68d-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="2a68d-130">Vous devez déplacer des chiffres réels de la transaction d'un autre système à PSA.</span><span class="sxs-lookup"><span data-stu-id="2a68d-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="2a68d-131">Vous devez enregistrer les coûts qui se sont produits dans un autre système, tel que les coûts d'approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="2a68d-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a68d-132">L'utilisation des journaux d'entrées pour créer des chiffres réels ne doit être effectuée que par un utilisateur qui est pleinement conscient de l'impact comptable des chiffres réels sur le projet.</span><span class="sxs-lookup"><span data-stu-id="2a68d-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="2a68d-133">En effet, l'application ne valide pas le type de ligne de journal ou la tarification associée qui est entrée sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="2a68d-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="2a68d-134">En raison de l'impact de ce type de journal, choisissez attentivement les personnes autorisées à créer des journaux d'entrées.</span><span class="sxs-lookup"><span data-stu-id="2a68d-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="2a68d-135">Enregistrement des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-135">Recording actuals based on project events</span></span>

<span data-ttu-id="2a68d-136">PSA enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="2a68d-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="2a68d-137">Ces transactions sont enregistrées comme **chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="2a68d-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="2a68d-138">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="2a68d-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="2a68d-139">**La ressource appartient à la même unité d'organisation que l'unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="2a68d-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2a68d-140">Event</span><span class="sxs-lookup"><span data-stu-id="2a68d-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2a68d-141">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="2a68d-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2a68d-142">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="2a68d-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2a68d-143">Projet interne</span><span class="sxs-lookup"><span data-stu-id="2a68d-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2a68d-144">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="2a68d-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2a68d-145">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="2a68d-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a68d-146">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-146">Actuals</span></span></th>
<th><span data-ttu-id="2a68d-147">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="2a68d-147">Transaction currency</span></span></th>
<th><span data-ttu-id="2a68d-148">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="2a68d-148">Fixed price</span></span></th>
<th><span data-ttu-id="2a68d-149">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="2a68d-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2a68d-150">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="2a68d-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2a68d-151">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-152">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="2a68d-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2a68d-153">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2a68d-154">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="2a68d-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2a68d-155">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-155">Cost actual</span></span></td>
<td><span data-ttu-id="2a68d-156">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-157">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-158">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="2a68d-159">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-160">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-161">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="2a68d-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2a68d-162">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2a68d-163">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="2a68d-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2a68d-164">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-164">Cost actual</span></span></td>
<td><span data-ttu-id="2a68d-165">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-166">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-167">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-168">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-169">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-170">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-171">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-172">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-173">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2a68d-174">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="2a68d-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2a68d-175">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2a68d-176">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-177">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="2a68d-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-178">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-179">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-180">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-181">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-181">Billed sales</span></span></td>
<td><span data-ttu-id="2a68d-182">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2a68d-183">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="2a68d-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2a68d-184">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2a68d-185">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-187">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-188">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-189">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-190">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-191">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-192">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-193">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2a68d-194">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="2a68d-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2a68d-195">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="2a68d-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2a68d-196">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2a68d-197">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="2a68d-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2a68d-198">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="2a68d-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2a68d-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-200">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-201">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-202">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-202">Billed sales</span></span></td>
<td><span data-ttu-id="2a68d-203">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2a68d-204">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="2a68d-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2a68d-205">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="2a68d-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2a68d-206">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-207">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-208">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-209">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-210">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a68d-211">**La ressource appartient à une unité d'organisation différente de l'unité contractuelle du projet**</span><span class="sxs-lookup"><span data-stu-id="2a68d-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2a68d-212">Event</span><span class="sxs-lookup"><span data-stu-id="2a68d-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2a68d-213">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="2a68d-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2a68d-214">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="2a68d-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2a68d-215">Projet interne</span><span class="sxs-lookup"><span data-stu-id="2a68d-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2a68d-216">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="2a68d-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2a68d-217">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="2a68d-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2a68d-218">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-218">Actuals</span></span></th>
<th><span data-ttu-id="2a68d-219">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="2a68d-219">Transaction currency</span></span></th>
<th><span data-ttu-id="2a68d-220">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="2a68d-220">Fixed price</span></span></th>
<th><span data-ttu-id="2a68d-221">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="2a68d-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2a68d-222">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="2a68d-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2a68d-223">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-224">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="2a68d-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2a68d-225">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="2a68d-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="2a68d-226">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="2a68d-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2a68d-227">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-227">Cost actual</span></span></td>
<td><span data-ttu-id="2a68d-228">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2a68d-229">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2a68d-230">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2a68d-231">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2a68d-232">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-233">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="2a68d-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2a68d-234">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-235">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="2a68d-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2a68d-236">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="2a68d-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-237">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="2a68d-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2a68d-238">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="2a68d-239">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="2a68d-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2a68d-240">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-240">Cost actual</span></span></td>
<td><span data-ttu-id="2a68d-241">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-242">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-243">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-244">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-245">Coût réel</span><span class="sxs-lookup"><span data-stu-id="2a68d-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-246">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="2a68d-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2a68d-247">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="2a68d-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-248">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="2a68d-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2a68d-249">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="2a68d-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-250">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-251">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-252">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-253">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2a68d-254">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="2a68d-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2a68d-255">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2a68d-256">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-257">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="2a68d-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-258">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-259">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2a68d-260">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-261">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-261">Billed sales</span></span></td>
<td><span data-ttu-id="2a68d-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2a68d-263">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="2a68d-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2a68d-264">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2a68d-265">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-267">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-268">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2a68d-269">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-270">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-271">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-272">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-273">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2a68d-274">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="2a68d-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2a68d-275">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="2a68d-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2a68d-276">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2a68d-277">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="2a68d-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2a68d-278">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="2a68d-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2a68d-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-280">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2a68d-281">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2a68d-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-282">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="2a68d-282">Billed sales</span></span></td>
<td><span data-ttu-id="2a68d-283">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2a68d-284">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="2a68d-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2a68d-285">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="2a68d-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2a68d-286">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-287">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="2a68d-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2a68d-288">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a68d-289">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="2a68d-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2a68d-290">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="2a68d-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>