---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996608"
---
# <a name="actuals"></a><span data-ttu-id="16427-103">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-103">Actuals</span></span> 

<span data-ttu-id="16427-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="16427-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16427-105">Les chiffres réels représentent l’état d’avancement des finances et du calendrier révisé et approuvé d’un projet.</span><span class="sxs-lookup"><span data-stu-id="16427-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="16427-106">Ils sont créés suite à l’approbation des entrées de temps, de dépenses, de l’utilisation du matériel ainsi que des écritures feuille et des factures.</span><span class="sxs-lookup"><span data-stu-id="16427-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="16427-107">Lignes de journal et envoi de temps</span><span class="sxs-lookup"><span data-stu-id="16427-107">Journal lines and time submission</span></span>

<span data-ttu-id="16427-108">Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16427-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="16427-109">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="16427-109">Time and materials</span></span>

<span data-ttu-id="16427-110">Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="16427-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="16427-111">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-111">Fixed price</span></span>

<span data-ttu-id="16427-112">Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="16427-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="16427-113">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="16427-113">Default pricing</span></span>

<span data-ttu-id="16427-114">La logique de création des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="16427-115">Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="16427-116">Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="16427-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="16427-117">Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="16427-118">Vous pouvez ajouter un champ personnalisé sur l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="16427-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="16427-119">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="16427-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="16427-120">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="16427-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="16427-121">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="16427-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="16427-122">Lignes de journal et envoi des dépenses de base</span><span class="sxs-lookup"><span data-stu-id="16427-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="16427-123">Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16427-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="16427-124">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="16427-124">Time and materials</span></span>

<span data-ttu-id="16427-125">Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="16427-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="16427-126">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-126">Fixed price</span></span>

<span data-ttu-id="16427-127">Quand une entrée de dépenses de base envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="16427-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="16427-128">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="16427-128">Default pricing</span></span>

<span data-ttu-id="16427-129">La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses.</span><span class="sxs-lookup"><span data-stu-id="16427-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="16427-130">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="16427-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="16427-131">Les champs qui affectent la tarification par défaut, par exemple **Catégorie de transaction** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="16427-132">Cependant, cela ne fonctionne que lorsque la méthode de tarification dans les tarifs est **Prix unitaire**.</span><span class="sxs-lookup"><span data-stu-id="16427-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="16427-133">Si la méthode de tarification est **À prix coûtant** ou **Majoration du coût**, le prix saisi lors de la création de l’entrée de dépense est utilisé pour le coût et le prix sur la ligne du journal des ventes est calculé en fonction de la méthode de tarification.</span><span class="sxs-lookup"><span data-stu-id="16427-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="16427-134">Vous pouvez ajouter un champ personnalisé sur l’entrée des dépenses.</span><span class="sxs-lookup"><span data-stu-id="16427-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="16427-135">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="16427-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="16427-136">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="16427-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="16427-137">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="16427-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="16427-138">Soumission des lignes de journal et du journal d’utilisation du matériel</span><span class="sxs-lookup"><span data-stu-id="16427-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="16427-139">Pour plus d’informations sur l’entrée des dépenses, voir [Journal d’utilisation des matériaux](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="16427-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="16427-140">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="16427-140">Time and materials</span></span>

<span data-ttu-id="16427-141">Lorsqu’une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat de temps et de matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="16427-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="16427-142">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-142">Fixed price</span></span>

<span data-ttu-id="16427-143">Quand une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="16427-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="16427-144">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="16427-144">Default pricing</span></span>

<span data-ttu-id="16427-145">La logique d’entrée des prix par défaut pour le matériel est basée sur la combinaison de produit et d’unité.</span><span class="sxs-lookup"><span data-stu-id="16427-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="16427-146">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="16427-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="16427-147">Les champs qui affectent la tarification par défaut, par exemple **ID produit** et **Unité**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="16427-148">Cependant, cela ne fonctionne que pour les produits du catalogue.</span><span class="sxs-lookup"><span data-stu-id="16427-148">However, this only works for catalog products.</span></span> <span data-ttu-id="16427-149">Pour les produits hors catalogue, le prix saisi lors de la création de l’entrée du journal d’utilisation du matériel est utilisé pour le prix de revient et le prix de vente sur les lignes de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="16427-150">Vous pouvez ajouter un champ personnalisé sur l’entrée **Journal d’utilisation des matériaux**.</span><span class="sxs-lookup"><span data-stu-id="16427-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="16427-151">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="16427-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="16427-152">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="16427-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="16427-153">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="16427-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="16427-154">Utiliser des journaux pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="16427-154">Use entry journals to record costs</span></span>

<span data-ttu-id="16427-155">Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="16427-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="16427-156">Les journaux peuvent être utilisés aux fins suivantes :</span><span class="sxs-lookup"><span data-stu-id="16427-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="16427-157">Déplacer les chiffres réels de transactions d’un autre système vers Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="16427-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="16427-158">Enregistrer les coûts survenus dans un autre système.</span><span class="sxs-lookup"><span data-stu-id="16427-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="16427-159">Ces coûts peuvent inclure des coûts d’approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="16427-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16427-160">L’application ne valide pas le type de ligne de journal ou la tarification associée qui est saisie sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="16427-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="16427-161">Par conséquent, seul un utilisateur pleinement conscient de l’impact comptable des chiffres réels sur le projet doit utiliser des journaux d’entrées pour créer des chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="16427-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="16427-162">En raison de l’impact de ce type de journal, vous devez choisir soigneusement qui a accès pour créer des journaux d’entrées.</span><span class="sxs-lookup"><span data-stu-id="16427-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="16427-163">Enregistrer des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="16427-163">Record actuals based on project events</span></span>

<span data-ttu-id="16427-164">Project Operations enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="16427-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="16427-165">Ces transactions sont enregistrées comme chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="16427-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="16427-166">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="16427-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="16427-167">La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="16427-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="16427-168">Event</span><span class="sxs-lookup"><span data-stu-id="16427-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="16427-169">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="16427-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="16427-170">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="16427-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="16427-171">Projet interne</span><span class="sxs-lookup"><span data-stu-id="16427-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="16427-172">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="16427-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="16427-173">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="16427-174">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-174">Actuals</span></span></th>
<th><span data-ttu-id="16427-175">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="16427-175">Transaction currency</span></span></th>
<th><span data-ttu-id="16427-176">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-176">Fixed price</span></span></th>
<th><span data-ttu-id="16427-177">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="16427-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="16427-178">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="16427-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="16427-179">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-180">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="16427-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="16427-181">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16427-182">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="16427-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16427-183">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-183">Cost actual</span></span></td>
<td><span data-ttu-id="16427-184">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-185">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-186">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="16427-187">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-188">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-189">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="16427-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="16427-190">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16427-191">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="16427-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16427-192">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-192">Cost actual</span></span></td>
<td><span data-ttu-id="16427-193">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-194">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-195">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-196">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-197">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-198">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16427-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-200">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-201">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16427-202">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="16427-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16427-203">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="16427-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16427-204">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-205">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="16427-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-206">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-207">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-208">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-209">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="16427-209">Billed sales</span></span></td>
<td><span data-ttu-id="16427-210">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16427-211">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="16427-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16427-212">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="16427-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16427-213">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-214">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-215">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-216">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-217">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-218">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16427-219">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-220">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-221">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16427-222">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="16427-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16427-223">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="16427-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16427-224">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="16427-225">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="16427-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="16427-226">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="16427-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="16427-227">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-228">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-229">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-230">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="16427-230">Billed sales</span></span></td>
<td><span data-ttu-id="16427-231">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16427-232">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="16427-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16427-233">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="16427-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16427-234">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-235">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="16427-236">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-237">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-238">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="16427-239">La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="16427-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="16427-240">Event</span><span class="sxs-lookup"><span data-stu-id="16427-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="16427-241">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="16427-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="16427-242">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="16427-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="16427-243">Projet interne</span><span class="sxs-lookup"><span data-stu-id="16427-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="16427-244">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="16427-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="16427-245">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="16427-246">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-246">Actuals</span></span></th>
<th><span data-ttu-id="16427-247">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="16427-247">Transaction currency</span></span></th>
<th><span data-ttu-id="16427-248">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="16427-248">Fixed price</span></span></th>
<th><span data-ttu-id="16427-249">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="16427-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="16427-250">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="16427-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="16427-251">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-252">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="16427-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="16427-253">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="16427-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="16427-254">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="16427-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16427-255">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-255">Cost actual</span></span></td>
<td><span data-ttu-id="16427-256">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="16427-257">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="16427-258">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="16427-259">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="16427-260">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-261">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="16427-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="16427-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-263">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="16427-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="16427-264">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="16427-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-265">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="16427-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="16427-266">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="16427-267">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="16427-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="16427-268">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-268">Cost actual</span></span></td>
<td><span data-ttu-id="16427-269">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-270">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-271">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-272">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-273">Coût réel</span><span class="sxs-lookup"><span data-stu-id="16427-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-274">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="16427-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="16427-275">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="16427-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-276">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="16427-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="16427-277">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="16427-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-278">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16427-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-280">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-281">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16427-282">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="16427-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16427-283">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="16427-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16427-284">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-285">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="16427-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-286">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-287">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="16427-288">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-289">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="16427-289">Billed sales</span></span></td>
<td><span data-ttu-id="16427-290">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16427-291">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="16427-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="16427-292">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="16427-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="16427-293">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-294">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-295">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-296">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="16427-297">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-298">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="16427-299">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-300">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-301">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="16427-302">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="16427-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16427-303">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="16427-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16427-304">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="16427-305">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="16427-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="16427-306">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="16427-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="16427-307">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-308">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="16427-309">Non applicable</span><span class="sxs-lookup"><span data-stu-id="16427-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-310">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="16427-310">Billed sales</span></span></td>
<td><span data-ttu-id="16427-311">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="16427-312">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="16427-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="16427-313">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="16427-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="16427-314">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-315">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="16427-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="16427-316">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="16427-317">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="16427-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="16427-318">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="16427-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
