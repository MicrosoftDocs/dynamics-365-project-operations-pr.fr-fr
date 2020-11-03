---
title: Crédits et factures corrigées
description: Cette rubrique fournit des informations sur les factures corrigées dans Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075851"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="3811c-103">Crédits et factures corrigées</span><span class="sxs-lookup"><span data-stu-id="3811c-103">Credits and corrected invoices</span></span>

<span data-ttu-id="3811c-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="3811c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3811c-105">Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="3811c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="3811c-106">Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**.</span><span class="sxs-lookup"><span data-stu-id="3811c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="3811c-107">Cette sélection n'est disponible que si une facture de projet est confirmée.</span><span class="sxs-lookup"><span data-stu-id="3811c-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="3811c-108">Un nouveau projet de facture est créé à partir de la facture confirmée.</span><span class="sxs-lookup"><span data-stu-id="3811c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="3811c-109">Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon.</span><span class="sxs-lookup"><span data-stu-id="3811c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="3811c-110">Voici quelques-uns des points clés à comprendre concernant les détails de la ligne sur la nouvelle facture corrigée :</span><span class="sxs-lookup"><span data-stu-id="3811c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="3811c-111">Toutes les quantités sont mises à jour à zéro.</span><span class="sxs-lookup"><span data-stu-id="3811c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="3811c-112">L'application suppose que tous les articles facturés sont entièrement crédités.</span><span class="sxs-lookup"><span data-stu-id="3811c-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="3811c-113">Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="3811c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="3811c-114">En fonction de la quantité que vous saisissez, l'application calcule la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="3811c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="3811c-115">Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée.</span><span class="sxs-lookup"><span data-stu-id="3811c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="3811c-116">Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.</span><span class="sxs-lookup"><span data-stu-id="3811c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="3811c-117">Les lignes de contrat basées sur les produits précédemment confirmées ne sont pas copiées.</span><span class="sxs-lookup"><span data-stu-id="3811c-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="3811c-118">Le traitement des corrections sur une facture de projet basée sur le produit n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3811c-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="3811c-119">Les corrections d'étape sont toujours traitées comme des crédits complets.</span><span class="sxs-lookup"><span data-stu-id="3811c-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="3811c-120">Les montants de provision ou d'avance peuvent être corrigés si le client a été facturé pour un montant incorrect.</span><span class="sxs-lookup"><span data-stu-id="3811c-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="3811c-121">Les rapprochements des provisions et avances peuvent être corrigés si un montant incorrect a été utilisé pour effectuer le rapprochement avec les frais sur une facture précédemment confirmée.</span><span class="sxs-lookup"><span data-stu-id="3811c-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3811c-122">Les détails de la ligne de facture qui sont des corrections à d'autres frais déjà facturés ont le champ **Correction** défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3811c-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="3811c-123">Les factures dont les détails de ligne de facture ont été corrigés ont un champ appelé **Contient des corrections** qui est également défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3811c-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="3811c-124">Rapports réels créés lors de la confirmation d'une facture corrective :</span><span class="sxs-lookup"><span data-stu-id="3811c-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="3811c-125">Ci-dessous les chiffres réels créés par l'application lors de la confirmation d'un correctif en fonction des opérations effectuées sur le projet de facture corrective avant confirmation.</span><span class="sxs-lookup"><span data-stu-id="3811c-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="3811c-126">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3811c-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="3811c-127">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3811c-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="3811c-128">Confirmer la correction d'une avance ou d'une provision facturée.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3811c-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-129">Une contrepassation des ventes non facturées de la provision ou de l'avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="3811c-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3811c-130">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l'avance.</span><span class="sxs-lookup"><span data-stu-id="3811c-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-131">Une contrepassation de ventes facturée réelle est créée pour le montant de la provision ou de l'avance pour contrepasser les ventes facturées d'origine.</span><span class="sxs-lookup"><span data-stu-id="3811c-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-132">Un nouveau chiffre d'affaires facturé réel est créé pour le montant corrigé sur la provision ou la ligne de facture corrigée basée sur l'avance.</span><span class="sxs-lookup"><span data-stu-id="3811c-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-133">Un chiffre d'affaires non facturé réel d'un montant négatif de la provision ou une ligne de facture corrigée basée sur l'avance, qui sera utilisé pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="3811c-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="3811c-134">Une confirmation de la correction d'une provision ou d'une avance préalablement rapproché.</span><span class="sxs-lookup"><span data-stu-id="3811c-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-135">Une contrepassation des ventes non facturées de la provision ou de l'avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="3811c-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="3811c-136">Ce montant est positif et vise à annuler le négatif qui a été créé lors du rapprochement précédent.</span><span class="sxs-lookup"><span data-stu-id="3811c-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-137">Une contrepassation de ventes facturée réelle pour le montant de la facture précédente.</span><span class="sxs-lookup"><span data-stu-id="3811c-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-138">Un nouveau chiffre d'affaires facturé réel pour le montant de provision qui est appliqué sur la facture corrigée.</span><span class="sxs-lookup"><span data-stu-id="3811c-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-139">Un chiffre d'affaires réel non facturé avec un montant négatif de la provision ou de l'avance restante corrigée, qui sera utilisé pour le rapprochement sur les factures ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3811c-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3811c-140">Facturation de l'intégralité du crédit d'une transaction horaire déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-141">Une annulation des ventes facturées pour les heures et le montant figurant sur la ligne de facture d'origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="3811c-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-142">Un nouveau chiffre d'affaires non facturé réel pour les heures et le montant figurant sur la ligne de facture d'origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="3811c-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3811c-143">Facturation du crédit partiel sur une opération de temps.</span><span class="sxs-lookup"><span data-stu-id="3811c-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-144">Une annulation des ventes facturées pour les heures et le montant facturé figurant sur la ligne de facture d'origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="3811c-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-145">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="3811c-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-146">Un nouveau chiffre d'affaires réel non facturé qui est facturé pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="3811c-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3811c-147">Facturation de l'intégralité du crédit d'une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-148">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d'origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="3811c-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-149">Un nouveau chiffre d'affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d'origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="3811c-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="3811c-150">Facturation du crédit partiel d'une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-151">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d'origine pour une dépense.</span><span class="sxs-lookup"><span data-stu-id="3811c-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-152">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrigée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="3811c-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-153">Un nouveau chiffre d'affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="3811c-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3811c-154">Facturation de l'intégralité du crédit d'une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-155">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d'origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="3811c-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-156">Un nouveau chiffre d'affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d'origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="3811c-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="3811c-157">Facturation du crédit partiel d'une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-158">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d'origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="3811c-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-159">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrective modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="3811c-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3811c-160">Facturation de l'intégralité du crédit d'un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="3811c-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-161">Une annulation des ventes facturées pour le montant figurant sur la ligne de facture d'origine pour le jalon.</span><span class="sxs-lookup"><span data-stu-id="3811c-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="3811c-162">La facture de jalon ou le statut de facturation sur la ligne de contrat de projet est mis à jour sur **Prêt à facturer**.</span><span class="sxs-lookup"><span data-stu-id="3811c-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3811c-163">Facturation du crédit partiel d'un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="3811c-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-164">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="3811c-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="3811c-165">Crédits et corrections d'une ligne de contrat basée sur des produits préalablement facturée.</span><span class="sxs-lookup"><span data-stu-id="3811c-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="3811c-166">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="3811c-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
