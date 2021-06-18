---
title: Créer des factures correctives basées sur un projet
description: Cette rubrique fournit des informations sur les factures correctives dans Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001609"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="f3ad2-103">Créer des factures correctives basées sur un projet</span><span class="sxs-lookup"><span data-stu-id="f3ad2-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="f3ad2-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="f3ad2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f3ad2-105">Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f3ad2-106">Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3ad2-107">Cette sélection n’est disponible que si une facture de projet est confirmée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f3ad2-108">Un nouveau projet de facture est créé à partir de la facture confirmée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f3ad2-109">Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f3ad2-110">Voici quelques points clés pour vous aider à mieux comprendre les détails de la ligne sur la nouvelle facture corrigée :</span><span class="sxs-lookup"><span data-stu-id="f3ad2-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f3ad2-111">Toutes les quantités sont mises à jour à zéro.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f3ad2-112">Cela suppose que tous les articles facturés sont entièrement crédités.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f3ad2-113">Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f3ad2-114">En fonction de la quantité que vous saisissez, l’application calcule la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f3ad2-115">Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f3ad2-116">Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f3ad2-117">Les corrections d’étape sont toujours traitées comme des crédits complets.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f3ad2-118">Les montants de provision ou d’avance peuvent être corrigés si le client a été facturé pour un montant incorrect.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f3ad2-119">Les rapprochements des provisions et avances peuvent être corrigés si un montant incorrect a été utilisé pour effectuer le rapprochement avec les frais sur une facture précédemment confirmée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3ad2-120">Pour les détails de la ligne de facture qui sont des corrections d’autres frais déjà facturés, le champ **Correction** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="f3ad2-121">Les factures dont les détails de ligne de facture ont été corrigés ont un champ appelé **Contient des corrections** qui est également défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f3ad2-122">Chiffres réels créés lors de la confirmation d’une facture corrective</span><span class="sxs-lookup"><span data-stu-id="f3ad2-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="f3ad2-123">Le tableau suivant répertorie les chiffres réels créés lorsqu’une facture corrective est confirmée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f3ad2-124">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3ad2-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f3ad2-125">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3ad2-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f3ad2-126">Confirmer la correction d’une avance ou d’une provision facturée.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3ad2-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-127">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f3ad2-128">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l’avance.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-129">Une contrepassation de ventes facturée réelle est créée pour le montant de la provision ou de l’avance pour contrepasser les ventes facturées d’origine.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-130">Un nouveau chiffre d’affaires facturé réel est créé pour le montant corrigé sur la provision ou la ligne de facture corrigée basée sur l’avance.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-131">Un chiffre d’affaires non facturé réel d’un montant négatif de la provision ou une ligne de facture corrigée basée sur l’avance, qui sera utilisé pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f3ad2-132">Une confirmation de la correction d’une provision ou d’une avance préalablement rapproché.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-133">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f3ad2-134">Ce montant est positif et vise à annuler le négatif qui a été créé lors du rapprochement précédent.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-135">Une contrepassation de ventes facturée réelle pour le montant de la facture précédente.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-136">Un nouveau chiffre d’affaires facturé réel pour le montant de provision qui est appliqué sur la facture corrigée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-137">Un chiffre d’affaires réel non facturé avec un montant négatif de la provision ou de l’avance restante corrigée, qui sera utilisé pour le rapprochement sur les factures ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3ad2-138">Facturation de l’intégralité du crédit d’une transaction horaire déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-139">Une annulation des ventes facturées pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-140">Un nouveau chiffre d’affaires non facturé réel pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f3ad2-141">Facturation du crédit partiel sur une opération de temps.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-142">Une annulation des ventes facturées pour les heures et le montant facturé figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-143">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-144">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3ad2-145">Facturation de l’intégralité du crédit d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-146">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-147">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f3ad2-148">Facturation du crédit partiel d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-149">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour une dépense.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-150">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrigée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-151">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3ad2-152">Facturation de l’intégralité du crédit d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-153">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-154">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f3ad2-155">Facturation du crédit partiel d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-156">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-157">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrective modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f3ad2-158">Facturation de l’intégralité du crédit d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-159">Une annulation des ventes facturées pour le montant figurant sur la ligne de facture d’origine pour le jalon.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f3ad2-160">Le statut de la facture du jalon <b>Facture client validée</b> est remplacé par <b>Prêt pour la facturation</b>.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f3ad2-161">Facturation du crédit partiel d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="f3ad2-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f3ad2-162">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3ad2-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
