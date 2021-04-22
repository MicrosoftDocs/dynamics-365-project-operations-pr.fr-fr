---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852541"
---
# <a name="actuals"></a><span data-ttu-id="6e8df-103">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-103">Actuals</span></span> 

<span data-ttu-id="6e8df-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="6e8df-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e8df-105">Les chiffres réels représentent l’état d’avancement des finances et du calendrier révisé et approuvé d’un projet.</span><span class="sxs-lookup"><span data-stu-id="6e8df-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="6e8df-106">Ils sont créés suite à l’approbation des entrées de temps, de dépenses, de l’utilisation du matériel ainsi que des écritures feuille et des factures.</span><span class="sxs-lookup"><span data-stu-id="6e8df-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="6e8df-107">Lignes de journal et envoi de temps</span><span class="sxs-lookup"><span data-stu-id="6e8df-107">Journal lines and time submission</span></span>

<span data-ttu-id="6e8df-108">Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e8df-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6e8df-109">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="6e8df-109">Time and materials</span></span>

<span data-ttu-id="6e8df-110">Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="6e8df-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6e8df-111">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-111">Fixed price</span></span>

<span data-ttu-id="6e8df-112">Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="6e8df-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6e8df-113">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="6e8df-113">Default pricing</span></span>

<span data-ttu-id="6e8df-114">La logique de création des prix par défaut se trouve sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="6e8df-115">Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="6e8df-116">Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="6e8df-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="6e8df-117">Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6e8df-118">Vous pouvez ajouter un champ personnalisé sur l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="6e8df-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="6e8df-119">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="6e8df-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6e8df-120">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="6e8df-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6e8df-121">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6e8df-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="6e8df-122">Lignes de journal et envoi des dépenses de base</span><span class="sxs-lookup"><span data-stu-id="6e8df-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="6e8df-123">Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e8df-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6e8df-124">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="6e8df-124">Time and materials</span></span>

<span data-ttu-id="6e8df-125">Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="6e8df-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6e8df-126">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-126">Fixed price</span></span>

<span data-ttu-id="6e8df-127">Quand une entrée de dépenses de base envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="6e8df-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6e8df-128">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="6e8df-128">Default pricing</span></span>

<span data-ttu-id="6e8df-129">La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses.</span><span class="sxs-lookup"><span data-stu-id="6e8df-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="6e8df-130">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="6e8df-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6e8df-131">Les champs qui affectent la tarification par défaut, par exemple **Catégorie de transaction** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6e8df-132">Cependant, cela ne fonctionne que lorsque la méthode de tarification dans les tarifs est **Prix unitaire**.</span><span class="sxs-lookup"><span data-stu-id="6e8df-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="6e8df-133">Si la méthode de tarification est **À prix coûtant** ou **Majoration du coût**, le prix saisi lors de la création de l’entrée de dépense est utilisé pour le coût et le prix sur la ligne du journal des ventes est calculé en fonction de la méthode de tarification.</span><span class="sxs-lookup"><span data-stu-id="6e8df-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="6e8df-134">Vous pouvez ajouter un champ personnalisé sur l’entrée des dépenses.</span><span class="sxs-lookup"><span data-stu-id="6e8df-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="6e8df-135">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="6e8df-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6e8df-136">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="6e8df-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6e8df-137">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6e8df-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="6e8df-138">Soumission des lignes de journal et du journal d’utilisation du matériel</span><span class="sxs-lookup"><span data-stu-id="6e8df-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="6e8df-139">Pour plus d’informations sur l’entrée des dépenses, voir [Journal d’utilisation des matériaux](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="6e8df-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6e8df-140">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="6e8df-140">Time and materials</span></span>

<span data-ttu-id="6e8df-141">Lorsqu’une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat de temps et de matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.</span><span class="sxs-lookup"><span data-stu-id="6e8df-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6e8df-142">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-142">Fixed price</span></span>

<span data-ttu-id="6e8df-143">Quand une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.</span><span class="sxs-lookup"><span data-stu-id="6e8df-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6e8df-144">Tarification par défaut</span><span class="sxs-lookup"><span data-stu-id="6e8df-144">Default pricing</span></span>

<span data-ttu-id="6e8df-145">La logique d’entrée des prix par défaut pour le matériel est basée sur la combinaison de produit et d’unité.</span><span class="sxs-lookup"><span data-stu-id="6e8df-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="6e8df-146">La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats.</span><span class="sxs-lookup"><span data-stu-id="6e8df-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6e8df-147">Les champs qui affectent la tarification par défaut, par exemple **ID produit** et **Unité**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6e8df-148">Cependant, cela ne fonctionne que pour les produits du catalogue.</span><span class="sxs-lookup"><span data-stu-id="6e8df-148">However, this only works for catalog products.</span></span> <span data-ttu-id="6e8df-149">Pour les produits hors catalogue, le prix saisi lors de la création de l’entrée du journal d’utilisation du matériel est utilisé pour le prix de revient et le prix de vente sur les lignes de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="6e8df-150">Vous pouvez ajouter un champ personnalisé sur l’entrée **Journal d’utilisation des matériaux**.</span><span class="sxs-lookup"><span data-stu-id="6e8df-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="6e8df-151">Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**.</span><span class="sxs-lookup"><span data-stu-id="6e8df-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6e8df-152">Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions.</span><span class="sxs-lookup"><span data-stu-id="6e8df-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6e8df-153">Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6e8df-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="6e8df-154">Utiliser des journaux pour enregistrer les coûts</span><span class="sxs-lookup"><span data-stu-id="6e8df-154">Use entry journals to record costs</span></span>

<span data-ttu-id="6e8df-155">Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes.</span><span class="sxs-lookup"><span data-stu-id="6e8df-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6e8df-156">Les journaux peuvent être utilisés aux fins suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e8df-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="6e8df-157">Déplacer les chiffres réels de transactions d’un autre système vers Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6e8df-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="6e8df-158">Enregistrer les coûts survenus dans un autre système.</span><span class="sxs-lookup"><span data-stu-id="6e8df-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="6e8df-159">Ces coûts peuvent inclure des coûts d’approvisionnement ou de sous-traitance.</span><span class="sxs-lookup"><span data-stu-id="6e8df-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e8df-160">L’application ne valide pas le type de ligne de journal ou la tarification associée qui est saisie sur la ligne de journal.</span><span class="sxs-lookup"><span data-stu-id="6e8df-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="6e8df-161">Par conséquent, seul un utilisateur pleinement conscient de l’impact comptable des chiffres réels sur le projet doit utiliser des journaux d’entrées pour créer des chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="6e8df-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="6e8df-162">En raison de l’impact de ce type de journal, vous devez choisir soigneusement qui a accès pour créer des journaux d’entrées.</span><span class="sxs-lookup"><span data-stu-id="6e8df-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="6e8df-163">Enregistrer des chiffres réels en fonction des événements du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-163">Record actuals based on project events</span></span>

<span data-ttu-id="6e8df-164">Project Operations enregistre les transactions financières qui se produisent pendant un projet.</span><span class="sxs-lookup"><span data-stu-id="6e8df-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6e8df-165">Ces transactions sont enregistrées comme chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="6e8df-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="6e8df-166">Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.</span><span class="sxs-lookup"><span data-stu-id="6e8df-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="6e8df-167">La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6e8df-168">Event</span><span class="sxs-lookup"><span data-stu-id="6e8df-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6e8df-169">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="6e8df-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6e8df-170">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="6e8df-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6e8df-171">Projet interne</span><span class="sxs-lookup"><span data-stu-id="6e8df-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6e8df-172">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="6e8df-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6e8df-173">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6e8df-174">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-174">Actuals</span></span></th>
<th><span data-ttu-id="6e8df-175">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="6e8df-175">Transaction currency</span></span></th>
<th><span data-ttu-id="6e8df-176">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-176">Fixed price</span></span></th>
<th><span data-ttu-id="6e8df-177">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="6e8df-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e8df-178">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="6e8df-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6e8df-179">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-180">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="6e8df-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6e8df-181">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6e8df-182">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="6e8df-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6e8df-183">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-183">Cost actual</span></span></td>
<td><span data-ttu-id="6e8df-184">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-185">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-186">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6e8df-187">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-188">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-189">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="6e8df-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6e8df-190">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6e8df-191">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="6e8df-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6e8df-192">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-192">Cost actual</span></span></td>
<td><span data-ttu-id="6e8df-193">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-194">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-195">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-196">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-197">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-198">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-199">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-200">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-201">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6e8df-202">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="6e8df-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6e8df-203">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6e8df-204">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-205">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="6e8df-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-206">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-207">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-208">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-209">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-209">Billed sales</span></span></td>
<td><span data-ttu-id="6e8df-210">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6e8df-211">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="6e8df-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6e8df-212">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6e8df-213">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-214">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-215">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-216">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-217">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-218">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-219">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-220">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-221">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6e8df-222">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="6e8df-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6e8df-223">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="6e8df-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6e8df-224">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6e8df-225">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="6e8df-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6e8df-226">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="6e8df-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6e8df-227">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-228">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-229">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-230">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-230">Billed sales</span></span></td>
<td><span data-ttu-id="6e8df-231">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6e8df-232">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="6e8df-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6e8df-233">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="6e8df-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6e8df-234">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-235">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-236">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-237">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-238">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="6e8df-239">La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6e8df-240">Event</span><span class="sxs-lookup"><span data-stu-id="6e8df-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6e8df-241">Projet facturable ou vendu</span><span class="sxs-lookup"><span data-stu-id="6e8df-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6e8df-242">Projet dans la phase préalable à la vente</span><span class="sxs-lookup"><span data-stu-id="6e8df-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6e8df-243">Projet interne</span><span class="sxs-lookup"><span data-stu-id="6e8df-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6e8df-244">Temps et matériaux</span><span class="sxs-lookup"><span data-stu-id="6e8df-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6e8df-245">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6e8df-246">Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-246">Actuals</span></span></th>
<th><span data-ttu-id="6e8df-247">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="6e8df-247">Transaction currency</span></span></th>
<th><span data-ttu-id="6e8df-248">Prix fixe</span><span class="sxs-lookup"><span data-stu-id="6e8df-248">Fixed price</span></span></th>
<th><span data-ttu-id="6e8df-249">Devise de transaction</span><span class="sxs-lookup"><span data-stu-id="6e8df-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6e8df-250">Une entrée de temps est créée.</span><span class="sxs-lookup"><span data-stu-id="6e8df-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6e8df-251">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-252">Une entrée de temps est envoyée.</span><span class="sxs-lookup"><span data-stu-id="6e8df-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6e8df-253">Aucune activité dans l’entité Chiffres réels</span><span class="sxs-lookup"><span data-stu-id="6e8df-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6e8df-254">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="6e8df-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6e8df-255">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-255">Cost actual</span></span></td>
<td><span data-ttu-id="6e8df-256">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6e8df-257">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6e8df-258">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6e8df-259">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6e8df-260">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-261">Chiffre réel des ventes non facturées - Facturable</span><span class="sxs-lookup"><span data-stu-id="6e8df-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6e8df-262">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-263">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="6e8df-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6e8df-264">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="6e8df-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-265">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="6e8df-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6e8df-266">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6e8df-267">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="6e8df-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6e8df-268">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-268">Cost actual</span></span></td>
<td><span data-ttu-id="6e8df-269">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-270">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-271">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-272">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-273">Coût réel</span><span class="sxs-lookup"><span data-stu-id="6e8df-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-274">Coût unitaire d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="6e8df-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6e8df-275">Devise de l’unité d’allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="6e8df-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-276">Ventes entre organisations</span><span class="sxs-lookup"><span data-stu-id="6e8df-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6e8df-277">Devise de l’unité contractuelle</span><span class="sxs-lookup"><span data-stu-id="6e8df-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-278">Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-279">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-280">Chiffre réel des ventes non facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-281">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6e8df-282">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</span><span class="sxs-lookup"><span data-stu-id="6e8df-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6e8df-283">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6e8df-284">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-285">Ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="6e8df-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-286">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-287">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6e8df-288">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-289">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-289">Billed sales</span></span></td>
<td><span data-ttu-id="6e8df-290">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6e8df-291">Une facture est confirmée, et une diminution des heures facturables survient.</span><span class="sxs-lookup"><span data-stu-id="6e8df-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6e8df-292">Libération des ventes non facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6e8df-293">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-294">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-295">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-296">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6e8df-297">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-298">Ventes facturées - Facturable pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-299">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-300">Ventes facturées - Non facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-301">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6e8df-302">Une facture est corrigée pour augmenter la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="6e8df-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6e8df-303">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="6e8df-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6e8df-304">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6e8df-305">Libération des ventes facturées pour le jalon</span><span class="sxs-lookup"><span data-stu-id="6e8df-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6e8df-306">Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></span><span class="sxs-lookup"><span data-stu-id="6e8df-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6e8df-307">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-308">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6e8df-309">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6e8df-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-310">Ventes facturées</span><span class="sxs-lookup"><span data-stu-id="6e8df-310">Billed sales</span></span></td>
<td><span data-ttu-id="6e8df-311">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6e8df-312">Une facture est corrigée pour diminuer la quantité facturable.</span><span class="sxs-lookup"><span data-stu-id="6e8df-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6e8df-313">Ventes facturées - Libération</span><span class="sxs-lookup"><span data-stu-id="6e8df-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6e8df-314">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-315">Ventes facturées pour la nouvelle quantité</span><span class="sxs-lookup"><span data-stu-id="6e8df-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6e8df-316">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6e8df-317">Ventes non facturées - Facturable pour la différence</span><span class="sxs-lookup"><span data-stu-id="6e8df-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6e8df-318">Devise du contrat du projet</span><span class="sxs-lookup"><span data-stu-id="6e8df-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
