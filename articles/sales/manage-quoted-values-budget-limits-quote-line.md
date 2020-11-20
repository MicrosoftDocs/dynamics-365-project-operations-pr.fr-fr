---
title: Vue d’ensemble de lignes du devis basées sur un projet
description: Cette rubrique fournit des informations sur l’utilisation des lignes de devis basées sur un projet pour le travail du projet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181854"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="0096e-103">Vue d’ensemble de lignes du devis basées sur un projet</span><span class="sxs-lookup"><span data-stu-id="0096e-103">Project-based quote lines overview</span></span>

<span data-ttu-id="0096e-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="0096e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0096e-105">Les lignes de devis basées sur un projet sont conçues pour aider à estimer le travail du projet sur un engagement.</span><span class="sxs-lookup"><span data-stu-id="0096e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="0096e-106">La structure d’une ligne de devis basée sur un projet est étendue pour les devis du projet avec les concepts suivants :</span><span class="sxs-lookup"><span data-stu-id="0096e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="0096e-107">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="0096e-107">Billing Method</span></span>
- <span data-ttu-id="0096e-108">Mappage de projet</span><span class="sxs-lookup"><span data-stu-id="0096e-108">Project Mapping</span></span>
- <span data-ttu-id="0096e-109">Classes de transaction incluses</span><span class="sxs-lookup"><span data-stu-id="0096e-109">Included Transaction classes</span></span>
- <span data-ttu-id="0096e-110">Limite à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="0096e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="0096e-111">Configuration de l’exigibilité</span><span class="sxs-lookup"><span data-stu-id="0096e-111">Chargeability setup</span></span>
- <span data-ttu-id="0096e-112">Estimation à l’aide des détails de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="0096e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="0096e-113">Clients de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="0096e-113">Quote line Customers</span></span>

<span data-ttu-id="0096e-114">Le tableau suivant fournit des informations sur les champs de l’onglet **Général** de la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="0096e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="0096e-115">Ces champs aident à jeter les bases d’une estimation détaillée et à la base du travail du projet.</span><span class="sxs-lookup"><span data-stu-id="0096e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="0096e-116">**Champ**</span><span class="sxs-lookup"><span data-stu-id="0096e-116">**Field**</span></span> | <span data-ttu-id="0096e-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="0096e-117">**Description**</span></span> | <span data-ttu-id="0096e-118">**Impact en aval**</span><span class="sxs-lookup"><span data-stu-id="0096e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0096e-119">Nom </span><span class="sxs-lookup"><span data-stu-id="0096e-119">Name</span></span> | <span data-ttu-id="0096e-120">Nom de la ligne de devis qui devrait vous aider à identifier le composant discret du devis qui est estimé.</span><span class="sxs-lookup"><span data-stu-id="0096e-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="0096e-121">Copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-122">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="0096e-122">Billing Method</span></span> | <span data-ttu-id="0096e-123">Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ correspondant sur la ligne d’opportunité.</span><span class="sxs-lookup"><span data-stu-id="0096e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="0096e-124">Ce champ comprend les deux principaux modèles de contrats pris en charge par Dynamics 365 Project Operations :</span><span class="sxs-lookup"><span data-stu-id="0096e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="0096e-125">- Prix fixe</span><span class="sxs-lookup"><span data-stu-id="0096e-125">- Fixed price</span></span></br><span data-ttu-id="0096e-126">- Temps et matériel.</span><span class="sxs-lookup"><span data-stu-id="0096e-126">- Time and material.</span></span>| <span data-ttu-id="0096e-127">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-128">Project</span><span class="sxs-lookup"><span data-stu-id="0096e-128">Project</span></span> | <span data-ttu-id="0096e-129">Utilisez ce champ facultatif pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement.</span><span class="sxs-lookup"><span data-stu-id="0096e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="0096e-130">Lorsqu’un projet est mappé à une ligne de devis, cela aide à configurer des tâches facturables et également à intégrer une estimation basée sur le projet à la ligne de devis en tant que détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="0096e-131">Lorsqu’un projet n’est pas mappé à une ligne de devis basée sur un projet, l’estimation doit être créée manuellement en créant chaque détail de ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="0096e-132">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-133">Inclure le temps</span><span class="sxs-lookup"><span data-stu-id="0096e-133">Include Time</span></span> | <span data-ttu-id="0096e-134">Un indicateur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-135">Une valeur de **Non** indique que le coût des transactions de temps ou de coûts de main-d’œuvre ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-136">Une valeur de **Oui** indique que le coût des transactions de temps ou de coûts de main-d’œuvre seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0096e-137">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-138">Inclure la dépense</span><span class="sxs-lookup"><span data-stu-id="0096e-138">Include Expense</span></span> | <span data-ttu-id="0096e-139">Un indicateur **Oui**/**Non** indique si les coûts de dépenses sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-140">Une valeur de **Non** indique que le coût de dépenses ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-141">Une valeur de **Oui** indique que le coût de dépenses seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0096e-142">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-143">Inclure les frais</span><span class="sxs-lookup"><span data-stu-id="0096e-143">Include Fee</span></span> | <span data-ttu-id="0096e-144">Un indicateur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-145">Une valeur de **Non** indique que les frais ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0096e-146">Une valeur de **Oui** indique que les frais seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0096e-147">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-148">Montant du devis</span><span class="sxs-lookup"><span data-stu-id="0096e-148">Quoted Amount</span></span> | <span data-ttu-id="0096e-149">Il s’agit du montant qui sera proposé au client pour tous les travaux prévus sur cette ligne de devis projet.</span><span class="sxs-lookup"><span data-stu-id="0096e-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="0096e-150">Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ **Budget client** sur la ligne d’opportunité.</span><span class="sxs-lookup"><span data-stu-id="0096e-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="0096e-151">Lorsque la ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant sur les détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="0096e-152">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-153">Estimation de taxe</span><span class="sxs-lookup"><span data-stu-id="0096e-153">Estimated Tax</span></span> | <span data-ttu-id="0096e-154">Il s’agit d’un champ modifiable permettant à l’utilisateur d’ajouter le montant estimé de la taxe sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="0096e-155">Lorsqu’une ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant de la taxe sur les détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="0096e-156">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-157">Montant du devis après taxes</span><span class="sxs-lookup"><span data-stu-id="0096e-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="0096e-158">Ce champ est le montant de la ligne de devis après taxes et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0096e-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="0096e-159">Le montant dans ce champ est calculé comme suit *Montant estimé + taxes*.</span><span class="sxs-lookup"><span data-stu-id="0096e-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="0096e-160">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-161">Limite à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="0096e-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="0096e-162">Ce champ est modifiable et n’est disponible que sur les lignes de devis basées sur un projet qui ont une méthode de facturation **Temps et matériel**.</span><span class="sxs-lookup"><span data-stu-id="0096e-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="0096e-163">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0096e-164">Budget client</span><span class="sxs-lookup"><span data-stu-id="0096e-164">Customer Budget</span></span> | <span data-ttu-id="0096e-165">Ce champ est modifiable et copié à partir du champ correspondant sur la ligne d’opportunité si le devis a été créé à partir d’une opportunité.</span><span class="sxs-lookup"><span data-stu-id="0096e-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="0096e-166">Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="0096e-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="0096e-167">Règles de validation pour les champs de l’onglet Général des lignes de devis basées sur le projet</span><span class="sxs-lookup"><span data-stu-id="0096e-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="0096e-168">**Règle 1** : Une certaine classe de transaction sur le projet sélectionné ne peut être incluse que sur une seule ligne de devis basée sur un projet d’un devis.</span><span class="sxs-lookup"><span data-stu-id="0096e-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="0096e-169">**Règle 2** : Si une opportunité comporte plusieurs devis, il peut y avoir des lignes de devis de différents devis qui font toutes référence au même projet et incluent la même classe de transaction.</span><span class="sxs-lookup"><span data-stu-id="0096e-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="0096e-170">**Règle 3** : Si les devis n’appartiennent pas à la même opportunité, ils ne peuvent pas inclure le même projet et la même classe de transaction.</span><span class="sxs-lookup"><span data-stu-id="0096e-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="0096e-171">
                    <strong>Opportunité</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0096e-172">
                    <strong>devis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0096e-173">
                    <strong>Ligne de devis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0096e-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0096e-175">
                    <strong>Inclure le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0096e-176">
                    <strong>Inclure la dépense</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0096e-177">
                    <strong>Inclure</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0096e-178">
                    <strong>frais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="0096e-179">
                    <strong>Valide/Non valide</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="0096e-180">
                    <strong>Motif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0096e-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-181">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-182">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-183">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-184">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-185">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-186">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-187">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-188">Non valide</span><span class="sxs-lookup"><span data-stu-id="0096e-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-189">Violation de la règle n° 1.</span><span class="sxs-lookup"><span data-stu-id="0096e-189">Violation of Rule #1.</span></span> <span data-ttu-id="0096e-190">Le temps, les dépenses et les frais du projet P1 sont inclus dans les deux lignes de devis, QL1 et QL2.</span><span class="sxs-lookup"><span data-stu-id="0096e-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-191">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-192">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-193">QL2</span><span class="sxs-lookup"><span data-stu-id="0096e-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-194">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-195">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-196">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-197">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-198">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-199">T1</span><span class="sxs-lookup"><span data-stu-id="0096e-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-200">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-201">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-202">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-203">No</span><span class="sxs-lookup"><span data-stu-id="0096e-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-204">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-205">Non valide</span><span class="sxs-lookup"><span data-stu-id="0096e-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-206">Violation de la règle n° 1.</span><span class="sxs-lookup"><span data-stu-id="0096e-206">Violation of Rule #1.</span></span> <span data-ttu-id="0096e-207">Le temps et les frais du projet P1 sont inclus dans les deux lignes de devis, QL1 et QL2.</span><span class="sxs-lookup"><span data-stu-id="0096e-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-208">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-209">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-210">QL2</span><span class="sxs-lookup"><span data-stu-id="0096e-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-211">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-212">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-213">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-214">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-215">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-216">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-217">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-218">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-219">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-220">No</span><span class="sxs-lookup"><span data-stu-id="0096e-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-221">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-222">Valide</span><span class="sxs-lookup"><span data-stu-id="0096e-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="0096e-223">Le temps et les frais du projet P1 sont inclus sur QL1.</span><span class="sxs-lookup"><span data-stu-id="0096e-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="0096e-224">Les dépenses du projet P1 sont inclus sur QL2.</span><span class="sxs-lookup"><span data-stu-id="0096e-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="0096e-225">Il n’y a pas de chevauchement dans ce qui est inclus sur chaque ligne de devis, donc c’est valide.</span><span class="sxs-lookup"><span data-stu-id="0096e-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-226">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-227">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-228">QL2</span><span class="sxs-lookup"><span data-stu-id="0096e-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-229">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-230">No</span><span class="sxs-lookup"><span data-stu-id="0096e-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-231">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-232">No</span><span class="sxs-lookup"><span data-stu-id="0096e-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-233">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-234">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-235">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-236">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-237">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-238">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-239">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-240">Non valide</span><span class="sxs-lookup"><span data-stu-id="0096e-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-241">Violation de la règle n° 1 ci-dessus</span><span class="sxs-lookup"><span data-stu-id="0096e-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="0096e-242">Q1 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1.</span><span class="sxs-lookup"><span data-stu-id="0096e-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0096e-243">QL2 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1 et chevauche ce qui est inclus dans Q1.</span><span class="sxs-lookup"><span data-stu-id="0096e-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-244">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-245">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-246">QL2</span><span class="sxs-lookup"><span data-stu-id="0096e-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-247">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-248">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-249">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-250">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-251">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-252">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-253">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-254">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-255">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-256">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-257">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0096e-258">Valide</span><span class="sxs-lookup"><span data-stu-id="0096e-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-259">Basé sur la règle n° 2, Q1 et Q2 sont deux citations sur la même opportunité, de sorte qu’ils peuvent tous les deux estimer pour les mêmes composants d’un projet.</span><span class="sxs-lookup"><span data-stu-id="0096e-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-260">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-261">Q2</span><span class="sxs-lookup"><span data-stu-id="0096e-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-262">QL1 sur Q2</span><span class="sxs-lookup"><span data-stu-id="0096e-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-263">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-264">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-265">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-266">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-267">O1</span><span class="sxs-lookup"><span data-stu-id="0096e-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-268">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-269">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-270">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-271">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-272">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-273">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0096e-274">Valide</span><span class="sxs-lookup"><span data-stu-id="0096e-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0096e-275">Basé sur la règle n° 3, Q1 et Q2 sont deux citations sur différentes opportunités, de sorte qu’ils peuvent tous les deux estimer pour les mêmes composants d’un même projet.</span><span class="sxs-lookup"><span data-stu-id="0096e-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0096e-276">O2</span><span class="sxs-lookup"><span data-stu-id="0096e-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0096e-277">Q1</span><span class="sxs-lookup"><span data-stu-id="0096e-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-278">QL1</span><span class="sxs-lookup"><span data-stu-id="0096e-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-279">P1</span><span class="sxs-lookup"><span data-stu-id="0096e-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-280">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0096e-281">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0096e-282">Oui</span><span class="sxs-lookup"><span data-stu-id="0096e-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0096e-283">Non valide</span><span class="sxs-lookup"><span data-stu-id="0096e-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

