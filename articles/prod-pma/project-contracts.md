---
title: Contrats de projet
description: Cette rubrique offre des exemples des contrats de projet que vous pouvez créer pour différents types de projets et sources de financement et comment vous pouvez gérer les contrats et facturer les clients du projet.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999758"
---
# <a name="project-contracts"></a><span data-ttu-id="43411-103">Contrats de projet</span><span class="sxs-lookup"><span data-stu-id="43411-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43411-104">Cet article offre des exemples des contrats de projet que vous pouvez créer pour différents types de projets et sources de financement et comment vous pouvez gérer les contrats et facturer les clients du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="43411-105">Le type de projet que vous créez pour un contrat de projet détermine la méthode utilisée pour facturer les clients du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="43411-106">Vous pouvez modifier un contrat de projet et le projet associé, mais vous ne pouvez pas modifier le type de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="43411-107">En utilisant un contrat de projet, vous pouvez facturer un ou plusieurs projets simultanément.</span><span class="sxs-lookup"><span data-stu-id="43411-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="43411-108">Le contrat de projet permet également de garantir une procédure de facturation homogène pour chaque sous-projet d’une structure de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="43411-109">Chaque projet facturé doit être associé à un contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="43411-110">Les paramètres d’un contrat de projet s’appliquent à tous les projets et sous-projets associés à ce contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="43411-111">Un contrat de projet peut spécifier une ou plusieurs sources de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="43411-112">Par conséquent, vous pouvez répartir la facturation entre plusieurs bailleurs, définir des limites de financement afin que les sources de financement ne soient pas facturées plus qu’un montant spécifié et configurer des règles de financement pour la facturation des dépenses.</span><span class="sxs-lookup"><span data-stu-id="43411-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="43411-113">Financement des contrats de projet</span><span class="sxs-lookup"><span data-stu-id="43411-113">Funding for project contracts</span></span>
<span data-ttu-id="43411-114">Certains contrats de projet précisent que plusieurs parties partagent la responsabilité du financement des coûts du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="43411-115">En voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="43411-115">Here are some examples:</span></span>

-   <span data-ttu-id="43411-116">Un gros client avec plusieurs divisions demande que le financement d’un projet soit réparti par division.</span><span class="sxs-lookup"><span data-stu-id="43411-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="43411-117">Votre entreprise partage les coûts d’un grand projet avec une organisation externe.</span><span class="sxs-lookup"><span data-stu-id="43411-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="43411-118">Un projet routier est cofinancé par deux municipalités.</span><span class="sxs-lookup"><span data-stu-id="43411-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="43411-119">Un projet de pont est financé par une subvention publique et une société privée.</span><span class="sxs-lookup"><span data-stu-id="43411-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="43411-120">Dans Dynamics 365 Finance, vous pouvez répartir la facturation d’une seule transaction ou de l’ensemble d’un projet entre plusieurs clients, subventions ou organisations.</span><span class="sxs-lookup"><span data-stu-id="43411-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="43411-121">Dans les projets associés à plusieurs bailleurs de fonds, toutes les parties qui contribuent au financement d’un projet de financement avancé sont appelées sources de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="43411-122">Une fois qu’un client, une organisation ou une subvention est défini(e) comme source de financement, il/elle peut être affecté(e) à une ou plusieurs règles de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="43411-123">Les règles de financement contiennent les critères qui déterminent la répartition des frais entre les différentes sources de financement d’un projet.</span><span class="sxs-lookup"><span data-stu-id="43411-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="43411-124">Étant donné que les articles en stock, tels que ceux qui apparaissent sur les demandes d’achat et les bons de commande, ne peuvent pas être répartis, le montant du coût ne peut pas être réparti entre plusieurs sources de financement au moment de la distribution.</span><span class="sxs-lookup"><span data-stu-id="43411-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="43411-125">Par conséquent, la valeur de la source de financement reste 0 (zéro) jusqu’à ce que la sortie de stock soit validée.</span><span class="sxs-lookup"><span data-stu-id="43411-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="43411-126">Lorsque la sortie de stock est validée, le montant du coût est réparti selon les règles de répartition des comptes du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="43411-127">Voici quelques étapes que vous pouvez suivre pour faciliter la répartition de la facturation entre plusieurs sources de financement :</span><span class="sxs-lookup"><span data-stu-id="43411-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="43411-128">Spécifiez que toutes les transactions saisies pour un projet utilisent la même devise de vente que le contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="43411-129">Définissez des limites de financement, de sorte qu’une source de financement ne soit pas facturée plus qu’un montant spécifié pour un projet.</span><span class="sxs-lookup"><span data-stu-id="43411-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="43411-130">Configurez des règles de financement et des limites de financement pour chaque collaborateur, article, catégorie, groupe de catégories et type de transaction (ou pour tous les types de transaction).</span><span class="sxs-lookup"><span data-stu-id="43411-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="43411-131">Sélectionnez des dates de début et de fin facultatives pour définir la période pendant laquelle chaque règle de financement est valide.</span><span class="sxs-lookup"><span data-stu-id="43411-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="43411-132">Précisez le pourcentage dont chaque source de financement est responsable.</span><span class="sxs-lookup"><span data-stu-id="43411-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="43411-133">Spécifiez quelle source de financement est responsable des différences d’arrondi causées par les calculs d’allocation de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="43411-134">Définissez des règles qui déterminent la manière dont les coûts du projet sont facturés aux clients externes et facturés aux organisations internes.</span><span class="sxs-lookup"><span data-stu-id="43411-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="43411-135">Enregistrez les transactions dans un compte de financement en attente jusqu’à ce qu’un financement supplémentaire puisse être obtenu, ou jusqu’à ce que vous décidiez de supporter les coûts en interne.</span><span class="sxs-lookup"><span data-stu-id="43411-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="43411-136">Pour déterminer le groupe de taxes à associer à une transaction, le projet est recherché pour une affectation de groupe de taxes.</span><span class="sxs-lookup"><span data-stu-id="43411-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="43411-137">Si aucune affectation de groupe de taxes n’a été effectuée au niveau du projet, le contrat de projet est recherché.</span><span class="sxs-lookup"><span data-stu-id="43411-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="43411-138">Exemple : plusieurs sources de financement (scénario simple)</span><span class="sxs-lookup"><span data-stu-id="43411-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="43411-139">Le tableau suivant présente des scénarios de gestion de la répartition du financement entre plusieurs sources de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="43411-140">Ces scénarios reposent sur les hypothèses suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="43411-141">Les paramètres de priorité sont pris en compte dans l’allocation des fonds avant que d’autres critères de règle de financement ne soient appliqués.</span><span class="sxs-lookup"><span data-stu-id="43411-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="43411-142">Aucune plage de dates n’a été spécifiée pour définir la période d pendant laquelle la règle de financement est valide.</span><span class="sxs-lookup"><span data-stu-id="43411-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43411-143"><strong>Scénario</strong></span><span class="sxs-lookup"><span data-stu-id="43411-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="43411-144"><strong>Source de financement</strong></span><span class="sxs-lookup"><span data-stu-id="43411-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="43411-145"><strong>Pourcentage d’allocation</strong></span><span class="sxs-lookup"><span data-stu-id="43411-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="43411-146"><strong>Priorité d’allocation</strong></span><span class="sxs-lookup"><span data-stu-id="43411-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43411-147">Vous voulez affecter les coûts à une source de financement jusqu’à ce que ses fonds soient épuisés, allouer les coûts à une deuxième source de financement jusqu’à ce que ses fonds soient épuisés, et enfin allouer les coûts restants à une troisième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-148">Source de financement 1</span><span class="sxs-lookup"><span data-stu-id="43411-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="43411-149">Source de financement 2</span><span class="sxs-lookup"><span data-stu-id="43411-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="43411-150">Source de financement 3</span><span class="sxs-lookup"><span data-stu-id="43411-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-151">100%%</span><span class="sxs-lookup"><span data-stu-id="43411-151">100%</span></span></li>
<li><span data-ttu-id="43411-152">100%%</span><span class="sxs-lookup"><span data-stu-id="43411-152">100%</span></span></li>
<li><span data-ttu-id="43411-153">100%%</span><span class="sxs-lookup"><span data-stu-id="43411-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-154">1</span><span class="sxs-lookup"><span data-stu-id="43411-154">1</span></span></li>
<li><span data-ttu-id="43411-155">2</span><span class="sxs-lookup"><span data-stu-id="43411-155">2</span></span></li>
<li><span data-ttu-id="43411-156">3</span><span class="sxs-lookup"><span data-stu-id="43411-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43411-157">Vous souhaitez affecter 75 %% des coûts à une source de financement et 25 %% à une deuxième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="43411-158">Lorsque l’une de ces sources de financement est épuisée, vous voulez payer les coûts restants à partir d’une troisième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-159">Source de financement 1</span><span class="sxs-lookup"><span data-stu-id="43411-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="43411-160">Source de financement 2</span><span class="sxs-lookup"><span data-stu-id="43411-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="43411-161">Source de financement 3</span><span class="sxs-lookup"><span data-stu-id="43411-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-162">75 %%</span><span class="sxs-lookup"><span data-stu-id="43411-162">75%</span></span></li>
<li><span data-ttu-id="43411-163">25 %%</span><span class="sxs-lookup"><span data-stu-id="43411-163">25%</span></span></li>
<li><span data-ttu-id="43411-164">100%%</span><span class="sxs-lookup"><span data-stu-id="43411-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-165">1</span><span class="sxs-lookup"><span data-stu-id="43411-165">1</span></span></li>
<li><span data-ttu-id="43411-166">1</span><span class="sxs-lookup"><span data-stu-id="43411-166">1</span></span></li>
<li><span data-ttu-id="43411-167">2</span><span class="sxs-lookup"><span data-stu-id="43411-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43411-168">Vous souhaitez affecter 75 %% des coûts à une source de financement et 25 %% à une deuxième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="43411-169">Lorsque l’une de ces sources de financement est épuisée, vous voulez répartir les coûts restants entre une troisième source de financement et une quatrième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-170">Source de financement 1</span><span class="sxs-lookup"><span data-stu-id="43411-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="43411-171">Source de financement 2</span><span class="sxs-lookup"><span data-stu-id="43411-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="43411-172">Source de financement 3</span><span class="sxs-lookup"><span data-stu-id="43411-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="43411-173">Source de financement 4</span><span class="sxs-lookup"><span data-stu-id="43411-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-174">75 %%</span><span class="sxs-lookup"><span data-stu-id="43411-174">75%</span></span></li>
<li><span data-ttu-id="43411-175">25 %%</span><span class="sxs-lookup"><span data-stu-id="43411-175">25%</span></span></li>
<li><span data-ttu-id="43411-176">50 %%</span><span class="sxs-lookup"><span data-stu-id="43411-176">50%</span></span></li>
<li><span data-ttu-id="43411-177">50 %%</span><span class="sxs-lookup"><span data-stu-id="43411-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-178">1</span><span class="sxs-lookup"><span data-stu-id="43411-178">1</span></span></li>
<li><span data-ttu-id="43411-179">1</span><span class="sxs-lookup"><span data-stu-id="43411-179">1</span></span></li>
<li><span data-ttu-id="43411-180">2</span><span class="sxs-lookup"><span data-stu-id="43411-180">2</span></span></li>
<li><span data-ttu-id="43411-181">2</span><span class="sxs-lookup"><span data-stu-id="43411-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43411-182">Vous souhaitez affecter les premiers 25 %% des coûts à une source de financement et le reste à une deuxième source de financement.</span><span class="sxs-lookup"><span data-stu-id="43411-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-183">Source de financement 1</span><span class="sxs-lookup"><span data-stu-id="43411-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="43411-184">Source de financement 2</span><span class="sxs-lookup"><span data-stu-id="43411-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-185">25 %%</span><span class="sxs-lookup"><span data-stu-id="43411-185">25%</span></span></li>
<li><span data-ttu-id="43411-186">100%%</span><span class="sxs-lookup"><span data-stu-id="43411-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="43411-187">1</span><span class="sxs-lookup"><span data-stu-id="43411-187">1</span></span></li>
<li><span data-ttu-id="43411-188">2</span><span class="sxs-lookup"><span data-stu-id="43411-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="43411-189">Exemple : plusieurs sources de financement (complexe)</span><span class="sxs-lookup"><span data-stu-id="43411-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="43411-190">Vous disposez de trois sources de financement que vous souhaitez utiliser dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="43411-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="43411-191">Utiliser à parts égales la source de financement 2 et la source de financement 3 jusqu’à ce que la source de financement 2 soit épuisée.</span><span class="sxs-lookup"><span data-stu-id="43411-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="43411-192">Continuer à utiliser la source de financement 3 jusqu’à ce qu’elle soit épuisée.</span><span class="sxs-lookup"><span data-stu-id="43411-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="43411-193">Utiliser la source de financement 1 après avoir épuisé la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="43411-194">Pour atteindre cet objectif, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="43411-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="43411-195">Fixez des limites de financement pour la source de financement 2 et la source de financement 3, pour leurs montants respectifs.</span><span class="sxs-lookup"><span data-stu-id="43411-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="43411-196">Créez les règles de financement suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="43411-197">Règle 1 (priorité 1) : imputez 50 %% des transactions à la source de financement 2 et 50 %% à la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="43411-198">Règle 2 (priorité 2) : imputez 100 %% des transactions à la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="43411-199">Règle 3 (priorité 3) : imputez 100 %% des transactions à la source de financement 1.</span><span class="sxs-lookup"><span data-stu-id="43411-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="43411-200">Cette configuration fonctionne, car les transactions sont vérifiées par rapport aux règles et aux limites pour déterminer si l’une d’entre elles s’applique à la transaction concernée.</span><span class="sxs-lookup"><span data-stu-id="43411-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="43411-201">Si aucune règle ou limite spécifique ne s’applique à la transaction, la règle Toutes les transactions s’applique.</span><span class="sxs-lookup"><span data-stu-id="43411-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="43411-202">La règle Toutes les transactions correspond à toutes les transactions.</span><span class="sxs-lookup"><span data-stu-id="43411-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="43411-203">Si une règle correspond à une transaction, le pourcentage qui a été alloué dans cette règle est appliqué en premier, mais uniquement une fois que les correspondances ont été vérifiées par rapport aux limites définies.</span><span class="sxs-lookup"><span data-stu-id="43411-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="43411-204">Si une limite a été atteinte et si les fonds d’une source de financement sont épuisés, la règle de financement associée à la limite de financement n’est pas respectée et le programme vérifie la règle suivante qui s’applique.</span><span class="sxs-lookup"><span data-stu-id="43411-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="43411-205">Dans certains cas, seule une partie d’une transaction peut être imputée en vertu d’une règle,</span><span class="sxs-lookup"><span data-stu-id="43411-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="43411-206">car une limite est atteinte lorsque la transaction est imputée.</span><span class="sxs-lookup"><span data-stu-id="43411-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="43411-207">Dans ce cas, seul un certain montant est imputé selon cette règle, par exemple 50 %% à chaque source de financement,</span><span class="sxs-lookup"><span data-stu-id="43411-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="43411-208">comme indiqué dans la règle 1 susmentionnée.</span><span class="sxs-lookup"><span data-stu-id="43411-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="43411-209">Le reste est imputé selon la règle suivante de la séquence.</span><span class="sxs-lookup"><span data-stu-id="43411-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="43411-210">Le tableau suivant décrit ce scénario en détail :</span><span class="sxs-lookup"><span data-stu-id="43411-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43411-211"><strong>Focus</strong></span><span class="sxs-lookup"><span data-stu-id="43411-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="43411-212"><strong>Détails</strong></span><span class="sxs-lookup"><span data-stu-id="43411-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43411-213">Règles de financement</span><span class="sxs-lookup"><span data-stu-id="43411-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-214">Règle 1 (priorité 1) : Toutes les transactions.</span><span class="sxs-lookup"><span data-stu-id="43411-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="43411-215">Imputez 50 %% à la source de financement 2 et 50 %% à la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="43411-216">Règle 2 (priorité 2) : Toutes les transactions.</span><span class="sxs-lookup"><span data-stu-id="43411-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="43411-217">Imputez 100 %% à la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="43411-218">Règle 3 (priorité 2) : Toutes les transactions.</span><span class="sxs-lookup"><span data-stu-id="43411-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="43411-219">Imputez 100 %% à la source de financement 1.</span><span class="sxs-lookup"><span data-stu-id="43411-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43411-220">Limites de financement</span><span class="sxs-lookup"><span data-stu-id="43411-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-221">Limite de la source de financement 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="43411-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="43411-222">Limite de la source de financement 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="43411-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="43411-223">Limite de la source de financement 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="43411-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43411-224">Transaction 1</span><span class="sxs-lookup"><span data-stu-id="43411-224">Transaction 1</span></span></td>
<td><span data-ttu-id="43411-225"><strong>Montant de la transaction :</strong>100<strong>Financement :</strong> la transaction est payée selon la règle 1 uniquement, car la transaction est entièrement payée après l’application de la règle 1.</span><span class="sxs-lookup"><span data-stu-id="43411-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="43411-226">La transaction est financée à parts égales entre la source de financement 2 et la source de financement 3.</span><span class="sxs-lookup"><span data-stu-id="43411-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="43411-227">Source de financement 2 : 50,00</span><span class="sxs-lookup"><span data-stu-id="43411-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="43411-228">Source de financement 3 : 50,00</span><span class="sxs-lookup"><span data-stu-id="43411-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43411-229">Transaction 2</span><span class="sxs-lookup"><span data-stu-id="43411-229">Transaction 2</span></span></td>
<td><span data-ttu-id="43411-230"><strong>Montant de la transaction :</strong>5 000<strong>Financement :</strong> la transaction est payée selon les trois règles.</span><span class="sxs-lookup"><span data-stu-id="43411-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="43411-231"><strong>Règle 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="43411-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="43411-232">Source de financement 2 : 450,00</span><span class="sxs-lookup"><span data-stu-id="43411-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="43411-233">Source de financement 3 : 450,00</span><span class="sxs-lookup"><span data-stu-id="43411-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="43411-234">
<strong>Règle 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="43411-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="43411-235">Source de financement 3 : 250,00 (= 750,00 - 50,00 - 450,00)</span><span class="sxs-lookup"><span data-stu-id="43411-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="43411-236">
<strong>Règle 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="43411-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="43411-237">Source de financement 1 : 3 850,00 (= 5 000,00 - 450,00 - 450,00 - 250,00)</span><span class="sxs-lookup"><span data-stu-id="43411-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43411-238">Total des fonds imputés à chaque source de financement</span><span class="sxs-lookup"><span data-stu-id="43411-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="43411-239">Source de financement 1 : 3 850</span><span class="sxs-lookup"><span data-stu-id="43411-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="43411-240">Source de financement 2 : 500</span><span class="sxs-lookup"><span data-stu-id="43411-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="43411-241">Source de financement 3 : 750</span><span class="sxs-lookup"><span data-stu-id="43411-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="43411-242">Règles de facturation</span><span class="sxs-lookup"><span data-stu-id="43411-242">Billing rules</span></span>
<span data-ttu-id="43411-243">Lorsque vous négociez un contrat de projet avec un client, vous définissez comment et quand vous pouvez facturer le client pour le travail sur un projet.</span><span class="sxs-lookup"><span data-stu-id="43411-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="43411-244">Après avoir configuré le contrat de projet et le projet, vous pouvez définir des règles de facturation pour le projet.</span><span class="sxs-lookup"><span data-stu-id="43411-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="43411-245">Les règles de facturation sont basées sur les conditions du projet spécifiées dans le contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="43411-246">Les règles de facturation que vous pouvez créer dépendent des conditions du contrat de projet et du type de projet, par exemple Régie ou Prix fixe, que vous associez à la règle de facturation.</span><span class="sxs-lookup"><span data-stu-id="43411-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="43411-247">Vous pouvez créer plusieurs règles de facturation pour un contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="43411-248">Vous pouvez également affecter une règle de facturation à plusieurs projets associés au même contrat de projet et dont les conditions de facturation sont similaires.</span><span class="sxs-lookup"><span data-stu-id="43411-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="43411-249">Vous pouvez configurer les types de règles de facturation suivants :</span><span class="sxs-lookup"><span data-stu-id="43411-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="43411-250">**Unité de livraison** : facturez un client lorsque vous achevez une unité de livraison.</span><span class="sxs-lookup"><span data-stu-id="43411-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="43411-251">Vous définissez les unités de livraison dans le contrat.</span><span class="sxs-lookup"><span data-stu-id="43411-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="43411-252">**Avancement** : facturez un client lorsque vous achevez un pourcentage spécifié du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="43411-253">Vous pouvez soit configurer une règle de facturation pour calculer automatiquement le pourcentage de travail achevé, soit calculer manuellement le pourcentage de travail achevé et le montant à facturer au client.</span><span class="sxs-lookup"><span data-stu-id="43411-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="43411-254">**Jalon** : facturez à un client le montant total d’un jalon de projet lorsque le jalon est atteint.</span><span class="sxs-lookup"><span data-stu-id="43411-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="43411-255">**Frais** : facturez un client pour vos services plus des frais de gestion, qui correspondent généralement à un pourcentage du coût des services.</span><span class="sxs-lookup"><span data-stu-id="43411-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="43411-256">**Régie** : facturez à un client la valeur du temps et des matériaux utilisés sur un projet.</span><span class="sxs-lookup"><span data-stu-id="43411-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="43411-257">Pour tous les types de règles de facturation, vous pouvez spécifier un pourcentage de rétention déduit des factures client jusqu’à ce qu’un projet atteigne une phase convenue.</span><span class="sxs-lookup"><span data-stu-id="43411-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="43411-258">Le pourcentage de rétention de paiement est spécifié dans le contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="43411-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="43411-259">Le montant est calculé en fonction de la valeur totale des lignes d’une facture client et soustrait de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="43411-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="43411-260">Pour les règles de facturation **Régie** et **Avancement**, vous pouvez affecter des catégories facturables.</span><span class="sxs-lookup"><span data-stu-id="43411-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="43411-261">Les catégories facturables indiquent les transactions à inclure dans les factures client.</span><span class="sxs-lookup"><span data-stu-id="43411-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="43411-262">Lorsque vous êtes prêt à facturer le client, le montant à facturer pour le projet est calculé en fonction des règles de facturation et une proposition de facture de projet est générée.</span><span class="sxs-lookup"><span data-stu-id="43411-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="43411-263">Les sections suivantes fournissent des exemples qui montrent comment configurer et gérer les règles de facturation pour un projet.</span><span class="sxs-lookup"><span data-stu-id="43411-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="43411-264">Exemple : créer une règle de facturation basée sur le nombre d’unités livrées</span><span class="sxs-lookup"><span data-stu-id="43411-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="43411-265">Votre organisation conclut un accord pour fournir un total de cinq sessions de formation aux employés d’un client au coût de 10 000 par session de formation.</span><span class="sxs-lookup"><span data-stu-id="43411-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="43411-266">Vous facturez le client après chaque session de formation.</span><span class="sxs-lookup"><span data-stu-id="43411-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="43411-267">Lorsque vous configurez les règles de facturation pour le contrat, vous utilisez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="43411-268">L’unité de livraison est une session de formation.</span><span class="sxs-lookup"><span data-stu-id="43411-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="43411-269">Le prix unitaire est de 10 000 par session de formation.</span><span class="sxs-lookup"><span data-stu-id="43411-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="43411-270">Le nombre total d’unités est de cinq sessions de formation.</span><span class="sxs-lookup"><span data-stu-id="43411-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="43411-271">Lorsque vous avez terminé une session de formation, vous pouvez créer une facture de 10 000, pour la première unité livrée, et envoyer la facture au client.</span><span class="sxs-lookup"><span data-stu-id="43411-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="43411-272">Exemple : créer une règle de facturation basée sur un pourcentage spécifié d’achèvement du projet (calcul manuel)</span><span class="sxs-lookup"><span data-stu-id="43411-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="43411-273">Votre organisation, une société de conseil en logiciels, conclut un accord avec un client pour développer une partie d’un produit que le client développe.</span><span class="sxs-lookup"><span data-stu-id="43411-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="43411-274">Votre organisation s’engage à livrer le code logiciel sur une période de six mois.</span><span class="sxs-lookup"><span data-stu-id="43411-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="43411-275">Le client s’engage à payer à votre organisation un total de 100 000 pour les travaux.</span><span class="sxs-lookup"><span data-stu-id="43411-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="43411-276">Vous créez une règle de facturation pour facturer le client en fonction du pourcentage de travail achevé sur le projet, comme spécifié dans le contrat.</span><span class="sxs-lookup"><span data-stu-id="43411-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="43411-277">À la fin du premier mois, vous rencontrez le client pour déterminer le pourcentage de travail réalisé.</span><span class="sxs-lookup"><span data-stu-id="43411-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="43411-278">Une fois que vous et le client avez examiné le projet, vous décidez que le projet est achevé à 15 %%.</span><span class="sxs-lookup"><span data-stu-id="43411-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="43411-279">Vous créez une facture pour 15 000 (15 pour cent de 100 000) et l’envoyez au client.</span><span class="sxs-lookup"><span data-stu-id="43411-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="43411-280">Exemple : créer une règle de facturation basée sur un pourcentage spécifié d’achèvement du projet (calcul automatique)</span><span class="sxs-lookup"><span data-stu-id="43411-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="43411-281">Votre organisation, une entreprise de développement de logiciels, accepte de développer un progiciel de comptabilité de paie pour un client pour 30 000.</span><span class="sxs-lookup"><span data-stu-id="43411-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="43411-282">Le client s’engage à payer à votre organisation selon le pourcentage de travail exécuté.</span><span class="sxs-lookup"><span data-stu-id="43411-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="43411-283">Vous estimez que les coûts du projet sont de 20 000.</span><span class="sxs-lookup"><span data-stu-id="43411-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="43411-284">Le contrat de projet spécifie les catégories de travail que vous utilisez dans le processus de facturation.</span><span class="sxs-lookup"><span data-stu-id="43411-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="43411-285">Vous configurez des règles de facturation qui calculent automatiquement les montants de facture pour le pourcentage de travail achevé pour chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="43411-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="43411-286">Vous définissez un budget pour chaque catégorie :</span><span class="sxs-lookup"><span data-stu-id="43411-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="43411-287">**Développement** : coût de 15 000 et revenu de 20 000</span><span class="sxs-lookup"><span data-stu-id="43411-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="43411-288">**Installation** : coût de 5 000 et revenu de 10 000</span><span class="sxs-lookup"><span data-stu-id="43411-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="43411-289">Lorsque vous créez une facture client pour la première fois, le montant de la facture est automatiquement calculé en fonction des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="43411-290">Après un mois, l’employé du projet soumet une feuille de temps pour le projet.</span><span class="sxs-lookup"><span data-stu-id="43411-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="43411-291">Le coût des heures d’employé est de 5 000 heures pour le développement et 1 000 pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="43411-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="43411-292">Les travaux de développement sont terminés à 33 %% (5 000 coûts réels / 15 000 coûts budgétaires) et les travaux d’installation sont terminés à 20 %% (1 000 coûts réels / 5 000 coûts budgétaires).</span><span class="sxs-lookup"><span data-stu-id="43411-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="43411-293">Le montant de la facture de 8 667 est calculé automatiquement (33 %% de 20 000 + 20 %% de 10 000).</span><span class="sxs-lookup"><span data-stu-id="43411-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="43411-294">Vous créez une facture pour 8 667 et l’envoyez au client.</span><span class="sxs-lookup"><span data-stu-id="43411-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="43411-295">Exemple : créer une règle de facturation basée sur des jalon convenus</span><span class="sxs-lookup"><span data-stu-id="43411-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="43411-296">Votre organisation, une société de conseil en gestion, accepte de mener une étude de marché pour un produit de consommation que le client envisage de vendre.</span><span class="sxs-lookup"><span data-stu-id="43411-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="43411-297">Le client s’engage à utiliser vos services pendant une période de trois mois, à compter du mois de mars, et s’engage à payer 50 000 à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43411-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="43411-298">Le projet comporte trois étapes :</span><span class="sxs-lookup"><span data-stu-id="43411-298">The project has three milestones:</span></span>

-   <span data-ttu-id="43411-299">Jalon 1 : recueillir des données sur les consommateurs - 31 mars</span><span class="sxs-lookup"><span data-stu-id="43411-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="43411-300">Jalon 2 : analyser les données des consommateurs - 30 avril</span><span class="sxs-lookup"><span data-stu-id="43411-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="43411-301">Jalon 3 : présenter une proposition de viabilité du produit - 31 mai</span><span class="sxs-lookup"><span data-stu-id="43411-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="43411-302">Le client accepte de payer à votre organisation 10 000 pour le premier jalon, 20 000 pour le deuxième jalon et 20 000 pour le troisième jalon.</span><span class="sxs-lookup"><span data-stu-id="43411-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="43411-303">Lorsque vous configurez le contrat de projet, vous acceptez de facturer le client en fonction du jalon qui a été atteint.</span><span class="sxs-lookup"><span data-stu-id="43411-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="43411-304">La configuration de la règle de facturation comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="43411-305">Définissez les jalons du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-305">Define the project milestones.</span></span>
-   <span data-ttu-id="43411-306">Définissez le montant à facturer au client lorsque chaque jalon est atteint.</span><span class="sxs-lookup"><span data-stu-id="43411-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="43411-307">Lorsque le premier jalon est atteint le 31 mars, vous le marquer comme atteint, puis créez une facture pour 10 000 et l’envoyez au client.</span><span class="sxs-lookup"><span data-stu-id="43411-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="43411-308">Vous ne pouvez pas créer une facture pour un jalon tant que vous ne l’avez pas marqué comme atteint.</span><span class="sxs-lookup"><span data-stu-id="43411-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="43411-309">Exemple : Créer une règle de facturation basée sur des services plus des frais de gestion</span><span class="sxs-lookup"><span data-stu-id="43411-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="43411-310">Votre organisation, une société de conseil en gestion, accepte de mener des études de marché pour évaluer la viabilité d’un produit que le client, une entreprise de vente au détail, développe.</span><span class="sxs-lookup"><span data-stu-id="43411-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="43411-311">Les termes de l’accord précisent que vous fournirez les services de vos trois principaux consultants en gestion, qui mèneront la recherche en fonction du temps et des matériaux.</span><span class="sxs-lookup"><span data-stu-id="43411-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="43411-312">Le client accepte de payer 100 par heure, plus des frais de gestion de 10 %% pour les heures de consultation qui sont facturées au projet.</span><span class="sxs-lookup"><span data-stu-id="43411-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="43411-313">Lorsque vous configurez le contrat de projet, créez une règle de facturation pour ajouter des frais de gestion de 10 %% aux heures de consultation facturées au projet.</span><span class="sxs-lookup"><span data-stu-id="43411-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="43411-314">Lorsque vous créez une facture pour le client, le client reçoit des frais de gestion de 10 %% plus le coût des heures de consultation.</span><span class="sxs-lookup"><span data-stu-id="43411-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="43411-315">Par exemple, si les trois consultants ont travaillé un total de 200 heures sur le projet, une facture de 22 000 est créée sur la base du calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="43411-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="43411-316">200 heures à 100 par heure = 20 000</span><span class="sxs-lookup"><span data-stu-id="43411-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="43411-317">10 pour cent de frais de gestion = 2000</span><span class="sxs-lookup"><span data-stu-id="43411-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="43411-318">Total du montant de la facture = 22 000</span><span class="sxs-lookup"><span data-stu-id="43411-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="43411-319">Si les frais sont taxables pour un client et si vous sélectionnez un groupe de taxe de vente dans le contrat de projet, le groupe de taxe de vente est automatiquement saisi dans une règle de facturation pour les frais.</span><span class="sxs-lookup"><span data-stu-id="43411-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="43411-320">Exemple : Créer une règle de facturation pour la valeur du temps et des matériaux</span><span class="sxs-lookup"><span data-stu-id="43411-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="43411-321">Votre organisation, une société de conseil en logiciels, accepte de fournir cinq consultants techniques pour travailler sur un projet de développement logiciel pour un client pendant les six prochains mois.</span><span class="sxs-lookup"><span data-stu-id="43411-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="43411-322">Le client s’engage à payer 150 pour chaque heure de consultation, plus le coût des fournitures de bureau.</span><span class="sxs-lookup"><span data-stu-id="43411-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="43411-323">Votre organisation envoie une facture au client à la fin de chaque mois.</span><span class="sxs-lookup"><span data-stu-id="43411-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="43411-324">Lorsque vous configurez le contrat de projet, vous acceptez de facturer le client chaque mois pour le temps et les matériaux du projet.</span><span class="sxs-lookup"><span data-stu-id="43411-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="43411-325">Vous créez une règle de facturation qui comprend les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="43411-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="43411-326">La durée du contrat est de six mois.</span><span class="sxs-lookup"><span data-stu-id="43411-326">The contract period is six months.</span></span>
-   <span data-ttu-id="43411-327">Le temps de consultation est calculé à raison de 150 par heure.</span><span class="sxs-lookup"><span data-stu-id="43411-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="43411-328">Les fournitures de bureau sont facturées au prix coûtant et le coût total du projet ne doit pas dépasser 10 000.</span><span class="sxs-lookup"><span data-stu-id="43411-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="43411-329">Vous créez une facture client à la fin de chaque mois calendaire pendant le projet.</span><span class="sxs-lookup"><span data-stu-id="43411-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="43411-330">Au cours du premier mois, un total de 800 heures est enregistré par les consultants sur le projet.</span><span class="sxs-lookup"><span data-stu-id="43411-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="43411-331">Le coût des fournitures de bureau imputées au projet est de 2 000.</span><span class="sxs-lookup"><span data-stu-id="43411-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="43411-332">Par conséquent, à la fin du mois, vous créez une facture pour 122 000, qui est calculée comme 800 heures à 150 par heure, plus 2 000 pour les fournitures de bureau.</span><span class="sxs-lookup"><span data-stu-id="43411-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]