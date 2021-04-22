---
title: Vue d’ensemble de lignes du devis basées sur un projet
description: Cette rubrique fournit des informations sur l’utilisation des lignes de devis basées sur un projet pour le travail du projet.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858695"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="daff9-103">Présentation de lignes du devis basées sur un projet</span><span class="sxs-lookup"><span data-stu-id="daff9-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="daff9-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="daff9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="daff9-105">Les lignes de devis basées sur un projet sont conçues pour aider à estimer le travail du projet sur un engagement.</span><span class="sxs-lookup"><span data-stu-id="daff9-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="daff9-106">La structure d’une ligne de devis basée sur un projet est étendue pour les devis du projet avec les concepts suivants :</span><span class="sxs-lookup"><span data-stu-id="daff9-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="daff9-107">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="daff9-107">Billing Method</span></span>
- <span data-ttu-id="daff9-108">Mappage des tâches et projets</span><span class="sxs-lookup"><span data-stu-id="daff9-108">Project and Task Mapping</span></span>
- <span data-ttu-id="daff9-109">Classes de transaction incluses</span><span class="sxs-lookup"><span data-stu-id="daff9-109">Included Transaction classes</span></span>
- <span data-ttu-id="daff9-110">Limite à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="daff9-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="daff9-111">Configuration de l’exigibilité</span><span class="sxs-lookup"><span data-stu-id="daff9-111">Chargeability setup</span></span>
- <span data-ttu-id="daff9-112">Estimation à l’aide des détails de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="daff9-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="daff9-113">Clients de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="daff9-113">Quote line Customers</span></span>

<span data-ttu-id="daff9-114">Le tableau suivant fournit des informations sur les champs de l’onglet **Général** de la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="daff9-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="daff9-115">Ces champs aident à jeter les bases d’une estimation détaillée et à la base du travail du projet.</span><span class="sxs-lookup"><span data-stu-id="daff9-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="daff9-116">**Champ**</span><span class="sxs-lookup"><span data-stu-id="daff9-116">**Field**</span></span> | <span data-ttu-id="daff9-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="daff9-117">**Description**</span></span> | <span data-ttu-id="daff9-118">**Impact en aval**</span><span class="sxs-lookup"><span data-stu-id="daff9-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="daff9-119">Nom </span><span class="sxs-lookup"><span data-stu-id="daff9-119">Name</span></span> | <span data-ttu-id="daff9-120">Le nom de la ligne de devis qui vous aide à identifier le composant discret du devis qui est estimé.</span><span class="sxs-lookup"><span data-stu-id="daff9-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="daff9-121">Copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-122">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="daff9-122">Billing Method</span></span> | <span data-ttu-id="daff9-123">Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ correspondant sur la ligne d’opportunité.</span><span class="sxs-lookup"><span data-stu-id="daff9-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="daff9-124">Ce champ comprend les deux principaux modèles de contrats pris en charge par Dynamics 365 Project Operations :</span><span class="sxs-lookup"><span data-stu-id="daff9-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="daff9-125">- Prix fixe</span><span class="sxs-lookup"><span data-stu-id="daff9-125">- Fixed price</span></span></br><span data-ttu-id="daff9-126">- Temps et matériel.</span><span class="sxs-lookup"><span data-stu-id="daff9-126">- Time and material.</span></span>| <span data-ttu-id="daff9-127">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-128">Project</span><span class="sxs-lookup"><span data-stu-id="daff9-128">Project</span></span> | <span data-ttu-id="daff9-129">Utilisez ce champ facultatif pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement.</span><span class="sxs-lookup"><span data-stu-id="daff9-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="daff9-130">Lorsqu’un projet est mappé à une ligne de devis, cela aide à configurer des tâches facturables et également à intégrer une estimation basée sur le projet à la ligne de devis en tant que détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="daff9-131">Lorsqu’un projet n’est pas mappé à une ligne de devis basée sur un projet, l’estimation doit être créée manuellement en créant chaque détail de ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="daff9-132">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="daff9-133">Tâches incluses</span><span class="sxs-lookup"><span data-stu-id="daff9-133">Included Tasks</span></span> | <span data-ttu-id="daff9-134">Indique si cette ligne de devis est utilisée pour tout ou partie des tâches du projet pour le projet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="daff9-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="daff9-135">Ce champ contient les valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="daff9-135">This field has the following possible values:</span></span></br><span data-ttu-id="daff9-136">- Toutes les tâches du projet</span><span class="sxs-lookup"><span data-stu-id="daff9-136">- All project tasks</span></span></br><span data-ttu-id="daff9-137">- Tâches du projet sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="daff9-137">- Selected project tasks only</span></span></br><span data-ttu-id="daff9-138">Une valeur vide dans ce champ équivaut à l’option **Toutes les tâches du projet**.</span><span class="sxs-lookup"><span data-stu-id="daff9-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="daff9-139">Lorsque **Tâches du projet sélectionnées uniquement** est sélectionné sur la page du projet, l’onglet **Configuration de la facturation de la tâche** vous permet de sélectionner des tâches spécifiques pour les associer à cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="daff9-140">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-141">Inclure le temps</span><span class="sxs-lookup"><span data-stu-id="daff9-141">Include Time</span></span> | <span data-ttu-id="daff9-142">Une valeur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-143">Une valeur de **Non** indique que le coût des transactions de temps ou de coûts de main-d’œuvre ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-144">Une valeur de **Oui** indique que le coût des transactions de temps ou de coûts de main-d’œuvre seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="daff9-145">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-146">Inclure la dépense</span><span class="sxs-lookup"><span data-stu-id="daff9-146">Include Expense</span></span> | <span data-ttu-id="daff9-147">Une valeur **Oui**/**Non** indique si les coûts de dépense sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-148">Une valeur de **Non** indique que le coût de dépenses ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-149">Une valeur de **Oui** indique que le coût de dépenses seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="daff9-150">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-151">Inclure le matériel</span><span class="sxs-lookup"><span data-stu-id="daff9-151">Include Material</span></span> | <span data-ttu-id="daff9-152">Une valeur **Oui**/**Non** indique si les coûts de matériel sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-153">Une valeur **Non** indique que les coûts de matériel ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-154">Une valeur **Oui** indique que les coûts de matériel seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="daff9-155">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-156">Inclure les frais</span><span class="sxs-lookup"><span data-stu-id="daff9-156">Include Fee</span></span> | <span data-ttu-id="daff9-157">Une valeur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-158">Une valeur **Non** indique que les frais ne seront pas inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="daff9-159">Une valeur **Oui** indique que les frais seront inclus dans l’estimation sur cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="daff9-160">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-161">Montant du devis</span><span class="sxs-lookup"><span data-stu-id="daff9-161">Quoted Amount</span></span> | <span data-ttu-id="daff9-162">Il s’agit du montant qui sera proposé au client pour tous les travaux prévus sur cette ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="daff9-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="daff9-163">Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ **Budget client** sur la ligne d’opportunité.</span><span class="sxs-lookup"><span data-stu-id="daff9-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="daff9-164">Lorsque la ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant sur les détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="daff9-165">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-166">Estimation de taxe</span><span class="sxs-lookup"><span data-stu-id="daff9-166">Estimated Tax</span></span> | <span data-ttu-id="daff9-167">Il s’agit d’un champ modifiable permettant à l’utilisateur d’ajouter le montant estimé de la taxe sur la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="daff9-168">Lorsqu’une ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant de la taxe sur les détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="daff9-169">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-170">Montant du devis après taxes</span><span class="sxs-lookup"><span data-stu-id="daff9-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="daff9-171">Ce champ est le montant de la ligne de devis après taxes et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="daff9-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="daff9-172">Le montant dans ce champ est calculé comme suit *Montant estimé + taxes*.</span><span class="sxs-lookup"><span data-stu-id="daff9-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="daff9-173">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-174">Limite à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="daff9-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="daff9-175">Ce champ est modifiable et n’est disponible que sur les lignes de devis basées sur un projet qui ont une méthode de facturation **Temps et matériel**.</span><span class="sxs-lookup"><span data-stu-id="daff9-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="daff9-176">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="daff9-177">Budget client</span><span class="sxs-lookup"><span data-stu-id="daff9-177">Customer Budget</span></span> | <span data-ttu-id="daff9-178">Ce champ est modifiable et copié à partir du champ correspondant sur la ligne d’opportunité si le devis a été créé à partir d’une opportunité.</span><span class="sxs-lookup"><span data-stu-id="daff9-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="daff9-179">Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.</span><span class="sxs-lookup"><span data-stu-id="daff9-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="daff9-180">Règles de validation pour les champs de l’onglet Général des lignes de devis basées sur le projet</span><span class="sxs-lookup"><span data-stu-id="daff9-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="daff9-181">**Règle 1** : Si le champ **Tâches incluses** est vide ou s’il est défini sur **Toutes les tâches du projet**, un projet est inclus dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="daff9-182">**Règle 2** : Si le champ **Tâches incluses** est vide ou s’il est défini sur **Toutes les tâches du projet**, un projet et une certaine classe de transaction ne peuvent être inclus que sur une seule ligne de devis basée sur un projet d’un devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="daff9-183">**Règle 3** : Si le champ **Tâches incluses** est défini sur **Tâches du projet sélectionnées uniquement**, un projet et une certaine classe de transaction ne peuvent être inclus que sur plusieurs lignes de devis basées sur un projet d’un devis.</span><span class="sxs-lookup"><span data-stu-id="daff9-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="daff9-184">**Règle 4** : Si une opportunité comporte plusieurs devis, il peut y avoir des lignes de devis de différents devis qui font toutes référence au même projet et incluent la même classe de transaction.</span><span class="sxs-lookup"><span data-stu-id="daff9-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="daff9-185">**Règle 5** : Si les devis n’appartiennent pas à la même opportunité, ils ne peuvent pas inclure le même projet et la même classe de transaction.</span><span class="sxs-lookup"><span data-stu-id="daff9-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="daff9-186">
                    <strong>Opportunité</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="daff9-187">
                    <strong>devis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="daff9-188">
                    <strong>Ligne de devis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="daff9-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="daff9-190">
                    <strong>Tâches incluses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="daff9-191">
                    <strong>Inclure le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="daff9-192">
                    <strong>Inclure la dépense</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="daff9-193">
                    <strong>Inclure le matériel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="daff9-194">
                    <strong>Inclure </strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="daff9-195">
                    <strong>Frais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="daff9-196">
                    <strong>Valide/Non valide</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="daff9-197">
                    <strong>Motif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="daff9-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-198">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-199">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-200">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-201">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-202">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-203">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-204">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-205">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-206">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-207">Non valide</span><span class="sxs-lookup"><span data-stu-id="daff9-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-208">Violation de la règle n° 2.</span><span class="sxs-lookup"><span data-stu-id="daff9-208">Violation of Rule #2.</span></span> <span data-ttu-id="daff9-209">Le temps, les dépenses et les frais du projet P1 sont inclus dans les lignes de devis, QL1 et QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-210">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-211">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-212">QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-213">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-214">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-215">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-216">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-217">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-218">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-219">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-220">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-221">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-222">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-223">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-224">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-225">No</span><span class="sxs-lookup"><span data-stu-id="daff9-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-226">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-227">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-228">Non valide</span><span class="sxs-lookup"><span data-stu-id="daff9-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-229">Violation de la règle n° 2.</span><span class="sxs-lookup"><span data-stu-id="daff9-229">Violation of Rule #2.</span></span> <span data-ttu-id="daff9-230">Le temps, le matériel et les frais du projet P1 sont inclus dans les lignes de devis, QL1 et QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-231">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-232">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-233">QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-234">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-235">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-236">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-237">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-238">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-239">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-240">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-241">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-242">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-243">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-244">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-245">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-246">No</span><span class="sxs-lookup"><span data-stu-id="daff9-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-247">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-248">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-249">Valide</span><span class="sxs-lookup"><span data-stu-id="daff9-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-250">Le temps, le matériel et les frais du projet P1 sont inclus dans QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="daff9-251">Les dépenses du projet P1 sont inclus sur QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="daff9-252">Il n’y a aucun chevauchement concernant ce qui est inclus sur chaque ligne de devis et donc valide.</span><span class="sxs-lookup"><span data-stu-id="daff9-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-253">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-254">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-255">QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-256">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-257">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-258">No</span><span class="sxs-lookup"><span data-stu-id="daff9-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-259">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-260">No</span><span class="sxs-lookup"><span data-stu-id="daff9-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-261">No</span><span class="sxs-lookup"><span data-stu-id="daff9-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-262">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-263">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-264">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-265">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-266">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="daff9-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-267">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-268">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-269">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-270">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-271">Non valide</span><span class="sxs-lookup"><span data-stu-id="daff9-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-272">Violation de la règle n° 2</span><span class="sxs-lookup"><span data-stu-id="daff9-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="daff9-273">Q1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1</span><span class="sxs-lookup"><span data-stu-id="daff9-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="daff9-274">QL2 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1 et il y a donc chevauchement avec ce qui est inclus sur Q1.</span><span class="sxs-lookup"><span data-stu-id="daff9-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-275">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-276">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-277">QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-278">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-279">Vide</span><span class="sxs-lookup"><span data-stu-id="daff9-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-280">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-281">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-282">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-283">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-284">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-285">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-286">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-287">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-288">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="daff9-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-289">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-290">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-291">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-292">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-293">Valide</span><span class="sxs-lookup"><span data-stu-id="daff9-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-294">Selon la règle n° 3,</span><span class="sxs-lookup"><span data-stu-id="daff9-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="daff9-295">Q1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1.</span><span class="sxs-lookup"><span data-stu-id="daff9-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="daff9-296">QL2 inclut le temps, le matériel, les dépenses et les frais pour un sous-ensemble de tâches du projet P1.</span><span class="sxs-lookup"><span data-stu-id="daff9-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="daff9-297">La seule validation supplémentaire concerne le sous-ensemble de tâches sur QL1 qui est différent du sous-ensemble de tâches sur QL2 pour s’assurer qu’il n’y a pas de chevauchement.</span><span class="sxs-lookup"><span data-stu-id="daff9-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="daff9-298">Ceci est fait par le système lorsque des tâches sont associées.</span><span class="sxs-lookup"><span data-stu-id="daff9-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-299">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-300">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-301">QL2</span><span class="sxs-lookup"><span data-stu-id="daff9-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-302">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-303">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="daff9-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-304">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-305">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-306">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-307">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-308">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-309">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-310">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-311">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-312">Toutes les tâches du projet ou vides</span><span class="sxs-lookup"><span data-stu-id="daff9-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-313">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-314">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-315">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-316">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-317">Valide</span><span class="sxs-lookup"><span data-stu-id="daff9-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-318">Selon la règle n° 5, Q1 et Q2 sont deux devis sur la même opportunité. Ils peuvent ainsi tous les deux faire une estimation pour les mêmes composants d’un projet.</span><span class="sxs-lookup"><span data-stu-id="daff9-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-319">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-320">T2</span><span class="sxs-lookup"><span data-stu-id="daff9-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-321">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-322">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-323">Toutes les tâches du projet ou vides</span><span class="sxs-lookup"><span data-stu-id="daff9-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-324">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-325">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-326">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-327">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-328">O1</span><span class="sxs-lookup"><span data-stu-id="daff9-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-329">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-330">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-331">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-332">Toutes les tâches du projet ou vides</span><span class="sxs-lookup"><span data-stu-id="daff9-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-333">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-334">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-335">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-336">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-337">Non valide</span><span class="sxs-lookup"><span data-stu-id="daff9-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="daff9-338">Selon la règle n° 4, Q1 et Q2 sont deux devis sur différentes opportunités. Ils ne peuvent ainsi par faire d’estimation pour les mêmes composants d’un même projet.</span><span class="sxs-lookup"><span data-stu-id="daff9-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="daff9-339">O2</span><span class="sxs-lookup"><span data-stu-id="daff9-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="daff9-340">T1</span><span class="sxs-lookup"><span data-stu-id="daff9-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="daff9-341">QL1</span><span class="sxs-lookup"><span data-stu-id="daff9-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-342">P1</span><span class="sxs-lookup"><span data-stu-id="daff9-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="daff9-343">Toutes les tâches du projet ou vides</span><span class="sxs-lookup"><span data-stu-id="daff9-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="daff9-344">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="daff9-345">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="daff9-346">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="daff9-347">Oui</span><span class="sxs-lookup"><span data-stu-id="daff9-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
