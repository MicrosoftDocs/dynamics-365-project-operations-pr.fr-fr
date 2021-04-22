---
title: Factures de projet correctives
description: Cette rubrique fournit des informations sur la création et la confirmation de factures correctives dans Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866588"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="fcf77-103">Factures de projet correctives</span><span class="sxs-lookup"><span data-stu-id="fcf77-103">Corrective project invoices</span></span>

<span data-ttu-id="fcf77-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="fcf77-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fcf77-105">Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="fcf77-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="fcf77-106">Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**.</span><span class="sxs-lookup"><span data-stu-id="fcf77-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="fcf77-107">Cette sélection n’est disponible que si une facture de projet est confirmée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="fcf77-108">Un nouveau projet de facture est créé à partir de la facture confirmée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="fcf77-109">Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon.</span><span class="sxs-lookup"><span data-stu-id="fcf77-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="fcf77-110">Voici quelques-uns des points clés à comprendre concernant les détails de la ligne sur la nouvelle facture corrigée :</span><span class="sxs-lookup"><span data-stu-id="fcf77-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="fcf77-111">Toutes les quantités sont mises à jour à zéro.</span><span class="sxs-lookup"><span data-stu-id="fcf77-111">All quantities are updated to zero.</span></span> <span data-ttu-id="fcf77-112">L’application suppose que tous les articles facturés sont entièrement crédités.</span><span class="sxs-lookup"><span data-stu-id="fcf77-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="fcf77-113">Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="fcf77-114">En fonction de la quantité que vous saisissez, l’application calcule la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="fcf77-115">Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="fcf77-116">Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.</span><span class="sxs-lookup"><span data-stu-id="fcf77-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="fcf77-117">Les lignes de contrat basées sur les produits précédemment confirmées ne sont pas copiées.</span><span class="sxs-lookup"><span data-stu-id="fcf77-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="fcf77-118">Le traitement des corrections sur une facture de projet basée sur le produit n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fcf77-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="fcf77-119">Les corrections d’étape sont toujours traitées comme des crédits complets.</span><span class="sxs-lookup"><span data-stu-id="fcf77-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="fcf77-120">Les montants de provision ou d’avance peuvent être corrigés si le client a été facturé pour un montant incorrect.</span><span class="sxs-lookup"><span data-stu-id="fcf77-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="fcf77-121">Les rapprochements des provisions et avances peuvent être corrigés si un montant incorrect a été utilisé pour effectuer le rapprochement avec les frais sur une facture précédemment confirmée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcf77-122">Les détails de la ligne de facture qui sont des corrections à d’autres frais déjà facturés ont le champ **Correction** défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="fcf77-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="fcf77-123">Les factures dont les détails de ligne de facture ont été corrigés ont un champ appelé **Contient des corrections** qui est également défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="fcf77-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="fcf77-124">Chiffres réels créés lorsqu’une facture corrective est confirmée</span><span class="sxs-lookup"><span data-stu-id="fcf77-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="fcf77-125">Le tableau suivant répertorie les chiffres réels créés lorsqu’une facture corrective est confirmée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="fcf77-126">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcf77-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="fcf77-127">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcf77-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="fcf77-128">Confirmer la correction d’une avance ou d’une provision facturée.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcf77-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-129">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="fcf77-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="fcf77-130">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l’avance.</span><span class="sxs-lookup"><span data-stu-id="fcf77-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-131">Une contrepassation de ventes facturée réelle est créée pour le montant de la provision ou de l’avance pour contrepasser les ventes facturées d’origine.</span><span class="sxs-lookup"><span data-stu-id="fcf77-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-132">Un nouveau chiffre d’affaires facturé réel est créé pour le montant corrigé sur la provision ou la ligne de facture corrigée basée sur l’avance.</span><span class="sxs-lookup"><span data-stu-id="fcf77-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-133">Un chiffre d’affaires non facturé réel d’un montant négatif de la provision ou une ligne de facture corrigée basée sur l’avance, qui sera utilisé pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="fcf77-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="fcf77-134">Une confirmation de la correction d’une provision ou d’une avance préalablement rapproché.</span><span class="sxs-lookup"><span data-stu-id="fcf77-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-135">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="fcf77-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="fcf77-136">Ce montant est positif et vise à annuler le négatif qui a été créé lors du rapprochement précédent.</span><span class="sxs-lookup"><span data-stu-id="fcf77-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-137">Une contrepassation de ventes facturée réelle pour le montant de la facture précédente.</span><span class="sxs-lookup"><span data-stu-id="fcf77-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-138">Un nouveau chiffre d’affaires facturé réel pour le montant de provision qui est appliqué sur la facture corrigée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-139">Un chiffre d’affaires réel non facturé avec un montant négatif de la provision ou de l’avance restante corrigée, qui sera utilisé pour le rapprochement sur les factures ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fcf77-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcf77-140">Facturation de l’intégralité du crédit d’une transaction horaire déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-141">Une annulation des ventes facturées pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fcf77-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-142">Un nouveau chiffre d’affaires non facturé réel pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fcf77-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fcf77-143">Facturation du crédit partiel sur une opération de temps.</span><span class="sxs-lookup"><span data-stu-id="fcf77-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-144">Une annulation des ventes facturées pour les heures et le montant facturé figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fcf77-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-145">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fcf77-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-146">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fcf77-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcf77-147">Facturation de l’intégralité du crédit d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-148">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="fcf77-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-149">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="fcf77-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fcf77-150">Facturation du crédit partiel d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-151">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour une dépense.</span><span class="sxs-lookup"><span data-stu-id="fcf77-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-152">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrigée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fcf77-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-153">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fcf77-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcf77-154">Facturation de l’intégralité du crédit d’une transaction de matériel déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-155">Une contrepassation des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fcf77-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-156">Un nouveau chiffre réel des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fcf77-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fcf77-157">Facturation du crédit partiel sur une transaction de matériel.</span><span class="sxs-lookup"><span data-stu-id="fcf77-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-158">Une contrepassation des ventes facturées pour la quantité et le montant facturés sur le détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fcf77-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-159">Un nouveau chiffre réel de ventes non facturées qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation de celui-ci et un chiffre réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fcf77-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-160">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fcf77-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcf77-161">Facturation de l’intégralité du crédit d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-162">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fcf77-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-163">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fcf77-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcf77-164">Facturation du crédit partiel d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-165">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fcf77-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-166">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrective modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fcf77-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fcf77-167">Facturation de l’intégralité du crédit d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="fcf77-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-168">Une annulation des ventes facturées pour le montant figurant sur la ligne de facture d’origine pour le jalon.</span><span class="sxs-lookup"><span data-stu-id="fcf77-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="fcf77-169">Le statut de la facture du jalon <b>Facture client publiée</b> est remplacé par <b>Prêt pour la facturation</b>.</span><span class="sxs-lookup"><span data-stu-id="fcf77-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fcf77-170">Facturation du crédit partiel d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="fcf77-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-171">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf77-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fcf77-172">Crédits et corrections d’une ligne de contrat basée sur des produits préalablement facturée.</span><span class="sxs-lookup"><span data-stu-id="fcf77-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcf77-173">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcf77-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
