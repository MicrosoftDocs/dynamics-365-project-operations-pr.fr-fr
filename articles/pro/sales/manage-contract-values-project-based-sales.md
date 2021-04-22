---
title: Vue d’ensemble des lignes de contrat basées sur les projets
description: Cette rubrique fournit des informations pour travailler avec des lignes de contrat basées sur un projet.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858155"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="5d9a3-103">Vue d’ensemble des lignes de contrat basées sur les projets</span><span class="sxs-lookup"><span data-stu-id="5d9a3-103">Project-based contract lines overview</span></span>

<span data-ttu-id="5d9a3-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="5d9a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d9a3-105">Les lignes de contrat basées sur un projet dans Dynamics 365 Project Operations ont pour vocation de contenir l’estimation et les accords de facturation des composants spécifiques du travail de projet dans un engagement.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="5d9a3-106">La structure d’une ligne de contrat basée sur un projet est étendue pour les estimations de projet et les scénarios de facturation avec les concepts suivants :</span><span class="sxs-lookup"><span data-stu-id="5d9a3-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="5d9a3-107">Mode de facturation</span><span class="sxs-lookup"><span data-stu-id="5d9a3-107">Billing method</span></span>
- <span data-ttu-id="5d9a3-108">Mappage des projets et des tâches</span><span class="sxs-lookup"><span data-stu-id="5d9a3-108">Project and task mapping</span></span>
- <span data-ttu-id="5d9a3-109">Classes de transaction incluses</span><span class="sxs-lookup"><span data-stu-id="5d9a3-109">Included transaction classes</span></span>
- <span data-ttu-id="5d9a3-110">Limite à ne pas dépasser</span><span class="sxs-lookup"><span data-stu-id="5d9a3-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="5d9a3-111">Configuration de l’exigibilité</span><span class="sxs-lookup"><span data-stu-id="5d9a3-111">Chargeability setup</span></span>
- <span data-ttu-id="5d9a3-112">Estimations utilisant les détails de la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="5d9a3-112">Estimates using contract line details</span></span>
- <span data-ttu-id="5d9a3-113">Client de la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="5d9a3-113">Contract line customers</span></span>

<span data-ttu-id="5d9a3-114">Le tableau suivant comprend les champs présents sous l’onglet **Général** des lignes de contrat basées sur un projet qui aident à configurer la base de départ d’une estimation détaillée et les modalités de facturation pour un travail basé sur un projet.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="5d9a3-115">Champ</span><span class="sxs-lookup"><span data-stu-id="5d9a3-115">Field</span></span> | <span data-ttu-id="5d9a3-116">Description</span><span class="sxs-lookup"><span data-stu-id="5d9a3-116">Description</span></span> | <span data-ttu-id="5d9a3-117">Impact en aval</span><span class="sxs-lookup"><span data-stu-id="5d9a3-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5d9a3-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-118">**Name**</span></span> | <span data-ttu-id="5d9a3-119">Nom de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-119">Name of the contract line.</span></span> <span data-ttu-id="5d9a3-120">Il identifie le composant discret du contrat estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="5d9a3-121">Pour un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir d’une valeur correspondante de la ligne de devis basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="5d9a3-122">Le nom copié dans la ligne de facture du projet créée à partir de cette ligne de contrat lorsque la facture est créée.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="5d9a3-123">**Mode de facturation**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-123">**Billing Method**</span></span> | <span data-ttu-id="5d9a3-124">Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="5d9a3-125">Il s’agit d’un groupe d’options qui représente les deux principaux modèles de contrats pris en charge par Project Operations :</span><span class="sxs-lookup"><span data-stu-id="5d9a3-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="5d9a3-126">- **Prix fixe**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-126">- **Fixed Price**</span></span></br><span data-ttu-id="5d9a3-127">- **Temps et matériel**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-127">- **Time and Material**</span></span> | <span data-ttu-id="5d9a3-128">En fonction du mode de facturation de la ligne de contrat référencée, la transaction réelle sera traitée.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="5d9a3-129">Si la ligne de contrat référencée par la transaction réelle a un mode de facturation pour le temps et le matériel, des enregistrements réels des coûts et des ventes non facturées sont créés.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="5d9a3-130">Si la ligne de contrat référencée par la transaction réelle a un mode de facturation à prix fixe, seul un coût réel est créé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="5d9a3-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-131">**Project**</span></span> | <span data-ttu-id="5d9a3-132">Utilisez ce champ pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="5d9a3-133">Cette valeur sera utilisée en conjonction avec **Tâches incluses** et **Classes de transaction incluses** pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-134">**Tâches incluses**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-134">**Included Tasks**</span></span> | <span data-ttu-id="5d9a3-135">Indique si cette ligne de contrat comprend toutes les tâches du projet pour le projet sélectionné ou seulement un sous-ensemble de tâches.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="5d9a3-136">Il s’agit d’un groupe d’options avec les valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d9a3-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="5d9a3-137">- **Toutes les tâches du projet**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-137">- **All Project Tasks**</span></span></br><span data-ttu-id="5d9a3-138">- **Tâches du projet sélectionnées uniquement**.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="5d9a3-139">Une valeur vide dans ce champ équivaut à sélectionner **Toutes les tâches du projet**.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="5d9a3-140">Si **Tâches sélectionnées uniquement** est sélectionné, vous pouvez sélectionner des tâches spécifiques et les associer à cette ligne de contrat dans l’onglet **Configuration de la facturation de la tâche** sur la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="5d9a3-141">La valeur sera utilisée conjointement avec les classes **Projet** et **Transaction incluses** pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-142">**Inclure le temps**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-142">**Include Time**</span></span> | <span data-ttu-id="5d9a3-143">Une valeur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="5d9a3-144">La valeur **Non** indique que les transactions de temps ou le coût de main-d’œuvre ne seront pas inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="5d9a3-145">La valeur **Oui** indique qu’ils le seront.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="5d9a3-146">Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-147">**Inclure la dépense**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-147">**Include Expense**</span></span> | <span data-ttu-id="5d9a3-148">Une valeur **Oui**/**Non** indique si les coûts de dépense sur le projet sélectionné seront inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="5d9a3-149">La valeur **Non** indique que les dépenses ne seront pas incluses dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="5d9a3-150">La valeur **Oui** indique qu’elles le seront.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="5d9a3-151">Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-152">**Inclure le matériel**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-152">**Include Materials**</span></span> | <span data-ttu-id="5d9a3-153">Une valeur **Oui**/**Non** indique si les coûts de matériel sur le projet sélectionné seront inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="5d9a3-154">Une valeur **Non** indique que les coûts de matériel ne seront pas inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="5d9a3-155">La valeur **Oui** indique qu’elles le seront.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="5d9a3-156">Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-157">**Inclure les frais**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-157">**Include Fee**</span></span> | <span data-ttu-id="5d9a3-158">Une valeur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="5d9a3-159">La valeur **Non** indique que les frais ne seront pas inclus dans cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="5d9a3-160">La valeur **Oui** indique qu’ils le seront.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="5d9a3-161">Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="5d9a3-162">**Montant contractuel**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-162">**Contracted Amount**</span></span> | <span data-ttu-id="5d9a3-163">Sur une ligne de contrat à prix fixe, ce montant est la valeur convenue qui sera facturée au client pour tous les composants de travail associés à cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="5d9a3-164">Sur une ligne de contrat de temps et de matériel, ce montant est une valeur estimée de ce qui sera facturé au client pour tous les composants de travail associés à cette ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="5d9a3-165">Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="5d9a3-166">Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant sur les détails de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="5d9a3-167">Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des détails de ligne.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="5d9a3-168">Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer le montant avant taxes sur les jalons périodiques pour la facturation.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="5d9a3-169">**Estimation de taxe**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-169">**Estimated Tax**</span></span> | <span data-ttu-id="5d9a3-170">L’utilisateur peut modifier ce champ pour saisir le montant estimé des taxes sur la ligne du contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="5d9a3-171">Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant des taxes sur les détails de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="5d9a3-172">Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des taxes des détails de ligne.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="5d9a3-173">Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer les taxes sur les jalons périodiques pour la facturation.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="5d9a3-174">**Montant contractuel après taxes**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="5d9a3-175">Le montant de a ligne de contrat après taxes.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-175">The contract line amount after tax.</span></span> <span data-ttu-id="5d9a3-176">Ce champ est en lecture seule et est calculé comme **Montant contractuel + taxes**.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="5d9a3-177">Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer des jalons périodiques pour la facturation.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="5d9a3-178">**Limite à ne pas dépasser**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="5d9a3-179">L’utilisateur peut modifier ce champ et il n’est disponible que sur les lignes de contrat basées sur un projet qui ont un mode de facturation défini sur le temps et le matériel.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="5d9a3-180">Ce champ est modifiable par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-180">The user can edit this field.</span></span> <span data-ttu-id="5d9a3-181">Lorsqu’un chiffre réel de temps et de matériel fait référence à cette ligne de contrat pour le temps et le matériel, le montant réel est évalué par rapport à la limite à ne pas dépasser sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="5d9a3-182">Cette évaluation est finalisée après la comptabilisation des montants déjà dépensés et engagés.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="5d9a3-183">**Budget client**</span><span class="sxs-lookup"><span data-stu-id="5d9a3-183">**Customer Budget**</span></span> | <span data-ttu-id="5d9a3-184">Ce champ est modifiable et est copié du champ correspondant sur la ligne de devis si le contrat a été créé à partir d’un devis.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="5d9a3-185">Ce champ n’est utilisé qu’à titre informatif et n’a aucune signification en aval.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="5d9a3-186">Règles de validation pour les options de l’onglet Général des lignes de contrat basées sur un projet</span><span class="sxs-lookup"><span data-stu-id="5d9a3-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="5d9a3-187">Règle 1 : si le champ **Tâches incluses** est vide ou défini sur **Toutes les tâches du projet**, toutes les tâches du projet sont incluses dans la ligne du contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="5d9a3-188">Règle 2 : lorsque le champ **Tâches incluses** est vide ou défini explicitement sur **Toutes les tâches du projet**, un projet et une certaine classe de transactions ne peuvent être inclus que sur une seule ligne de contrat de projet d’un contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="5d9a3-189">Règle 3 : lorsque le champ **Tâches incluses** est défini sur **Tâches du projet sélectionnées uniquement**, un projet et une certaine classe de transactions peuvent être inclus que sur plusieurs lignes de contrat de projet d’un contrat.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="5d9a3-190">
                    <strong>Contrat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="5d9a3-191">
                    <strong>Ligne de contrat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5d9a3-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="5d9a3-193">
                    <strong>Tâches incluses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5d9a3-194">
                    <strong>Inclure le temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5d9a3-195">
                    <strong>Inclure la dépense</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5d9a3-196">
                    <strong>Inclure le matériel</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5d9a3-197">
                    <strong>Inclure </strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5d9a3-198">
                    <strong>Frais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="5d9a3-199">
                    <strong>Valide/Non valide</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="5d9a3-200">
                    <strong>Motif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5d9a3-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-201">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-202">CL1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-203">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-204">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-205">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-206">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-207">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-208">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-209">Non valide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-210">Violation de la règle n° 2.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-210">Violation of Rule #2.</span></span> <span data-ttu-id="5d9a3-211">Le temps, les dépenses, le matériel et les frais du projet P1 sont inclus dans les lignes de contrat CL1 et CL2.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-212">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-213">CL2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-214">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-215">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-216">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-217">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-218">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-219">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-220">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-221">CL1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-222">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-223">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-224">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-225">No</span><span class="sxs-lookup"><span data-stu-id="5d9a3-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-226">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-227">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-228">Non valide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-229">Violation de la règle n° 2.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-229">Violation of Rule #2.</span></span> <span data-ttu-id="5d9a3-230">Le temps, le matériel et les frais du projet P1 sont inclus dans les lignes de contrat CL1 et CL2.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-231">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-232">CL2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-233">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-234">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-235">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-236">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-237">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-238">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-239">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-240">CL1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-241">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-242">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-243">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-244">No</span><span class="sxs-lookup"><span data-stu-id="5d9a3-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-245">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-246">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-247">Valide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-248">Le temps, le matériel et les frais du projet P1 sont inclus dans CL1.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="5d9a3-249">Les dépenses du projet P1 sont inclus sur CL2.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="5d9a3-250">Il n’y a aucun chevauchement concernant ce qui est inclus sur chaque ligne de contrat et donc valide.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-251">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-252">CL2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-253">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-254">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-255">No</span><span class="sxs-lookup"><span data-stu-id="5d9a3-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-256">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-257">No</span><span class="sxs-lookup"><span data-stu-id="5d9a3-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-258">No</span><span class="sxs-lookup"><span data-stu-id="5d9a3-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-259">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-260">CL1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-261">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-262">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="5d9a3-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-263">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-264">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-265">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-266">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-267">Non valide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-268">Violation de la règle n° 2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="5d9a3-269">C1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5d9a3-270">CL2 comprend le temps, le matériel, les dépenses et les frais pour l’ensemble du projet P1 et chevauche donc ce qui est inclus dans C1.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-271">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-272">CL2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-273">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-274">Vide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-275">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-276">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-277">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-278">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-279">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-280">CL1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-281">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-282">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="5d9a3-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-283">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-284">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-285">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-286">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-287">Valide</span><span class="sxs-lookup"><span data-stu-id="5d9a3-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5d9a3-288">Selon la règle n° 3</span><span class="sxs-lookup"><span data-stu-id="5d9a3-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="5d9a3-289">C1 inclut le temps, les dépenses, le matériel et les frais sur un sous-ensemble de tâches du projet P1.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5d9a3-290">CL2 inclut le temps, les dépenses, le matériel et les frais pour un sous-ensemble de tâches du projet P1.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5d9a3-291">La seule validation supplémentaire concerne le sous-ensemble de tâches sur CL1 qui est différent du sous-ensemble de tâches sur CL2 pour s’assurer qu’il n’y a pas de chevauchements.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="5d9a3-292">Ceci est fait par le système lorsque des tâches sont associées.</span><span class="sxs-lookup"><span data-stu-id="5d9a3-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5d9a3-293">C1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="5d9a3-294">CL2</span><span class="sxs-lookup"><span data-stu-id="5d9a3-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-295">P1</span><span class="sxs-lookup"><span data-stu-id="5d9a3-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="5d9a3-296">Tâches sélectionnées uniquement</span><span class="sxs-lookup"><span data-stu-id="5d9a3-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-297">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5d9a3-298">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-299">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5d9a3-300">Oui</span><span class="sxs-lookup"><span data-stu-id="5d9a3-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
