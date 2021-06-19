---
title: Factures correctives basées sur un projet
description: Cette rubrique fournit des informations sur la création et la confirmation de factures correctives basées sur un projet dans Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012268"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="fb348-103">Factures correctives basées sur un projet</span><span class="sxs-lookup"><span data-stu-id="fb348-103">Corrective project-based invoices</span></span>

<span data-ttu-id="fb348-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="fb348-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb348-105">Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="fb348-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="fb348-106">Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**.</span><span class="sxs-lookup"><span data-stu-id="fb348-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb348-107">Cette sélection n’est pas disponible, sauf si une facture de projet est confirmée ou si la facture basée sur le projet comporte des avances, des provisions ou des rapprochements d’avances ou de provisions.</span><span class="sxs-lookup"><span data-stu-id="fb348-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="fb348-108">Un nouveau projet de facture est créé à partir de la facture confirmée.</span><span class="sxs-lookup"><span data-stu-id="fb348-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="fb348-109">Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon.</span><span class="sxs-lookup"><span data-stu-id="fb348-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="fb348-110">Voici quelques-uns des points clés à comprendre concernant les détails de la ligne sur la nouvelle facture corrigée :</span><span class="sxs-lookup"><span data-stu-id="fb348-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="fb348-111">Toutes les quantités sont mises à jour à zéro.</span><span class="sxs-lookup"><span data-stu-id="fb348-111">All quantities are updated to zero.</span></span> <span data-ttu-id="fb348-112">Dynamics 365 Project Operations suppose que tous les articles facturés sont entièrement crédités.</span><span class="sxs-lookup"><span data-stu-id="fb348-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="fb348-113">Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="fb348-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="fb348-114">En fonction de la quantité que vous saisissez, l’application calcule la quantité créditée.</span><span class="sxs-lookup"><span data-stu-id="fb348-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="fb348-115">Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée.</span><span class="sxs-lookup"><span data-stu-id="fb348-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="fb348-116">Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.</span><span class="sxs-lookup"><span data-stu-id="fb348-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="fb348-117">Les corrections d’étape sont toujours traitées comme des crédits complets.</span><span class="sxs-lookup"><span data-stu-id="fb348-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="fb348-118">Pour les détails de la ligne de facture qui sont des corrections d’autres frais déjà facturés, le champ **Correction** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="fb348-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="fb348-119">Pour les factures dont des détails de la ligne de facture sont corrigés, le champ **Contient des corrections** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="fb348-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="fb348-120">Chiffres réels créés lorsqu’une facture corrective est confirmée</span><span class="sxs-lookup"><span data-stu-id="fb348-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="fb348-121">Le tableau suivant répertorie les chiffres réels créés lorsqu’une facture corrective est confirmée.</span><span class="sxs-lookup"><span data-stu-id="fb348-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="fb348-122">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb348-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="fb348-123">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb348-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb348-124">Facturation de l’intégralité du crédit d’une transaction horaire déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-125">Une annulation des ventes facturées pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fb348-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-126">Un nouveau chiffre d’affaires non facturé réel pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fb348-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fb348-127">Facturation du crédit partiel sur une opération de temps.</span><span class="sxs-lookup"><span data-stu-id="fb348-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-128">Une annulation des ventes facturées pour les heures et le montant facturé figurant sur la ligne de facture d’origine pour le temps.</span><span class="sxs-lookup"><span data-stu-id="fb348-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-129">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fb348-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-130">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fb348-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb348-131">Facturation de l’intégralité du crédit d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-132">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="fb348-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-133">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.</span><span class="sxs-lookup"><span data-stu-id="fb348-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fb348-134">Facturation du crédit partiel d’une transaction de dépense déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-135">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour une dépense.</span><span class="sxs-lookup"><span data-stu-id="fb348-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-136">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrigée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fb348-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-137">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fb348-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb348-138">Facturation de l’intégralité du crédit d’une transaction de matériel déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-139">Une contrepassation des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fb348-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-140">Un nouveau chiffre réel des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fb348-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fb348-141">Facturation du crédit partiel sur une transaction de matériel.</span><span class="sxs-lookup"><span data-stu-id="fb348-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-142">Une contrepassation des ventes facturées pour la quantité et le montant facturés sur le détail de la ligne de facture d’origine du matériel.</span><span class="sxs-lookup"><span data-stu-id="fb348-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-143">Un nouveau chiffre réel de ventes non facturées qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation de celui-ci et un chiffre réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fb348-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-144">Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.</span><span class="sxs-lookup"><span data-stu-id="fb348-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb348-145">Facturation de l’intégralité du crédit d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-146">Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fb348-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-147">Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fb348-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb348-148">Facturation du crédit partiel d’une transaction avec frais déjà facturée.</span><span class="sxs-lookup"><span data-stu-id="fb348-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-149">Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour les frais.</span><span class="sxs-lookup"><span data-stu-id="fb348-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-150">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrective modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="fb348-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fb348-151">Facturation de l’intégralité du crédit d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="fb348-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-152">Une annulation des ventes facturées pour le montant figurant sur la ligne de facture d’origine pour le jalon.</span><span class="sxs-lookup"><span data-stu-id="fb348-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="fb348-153">Le statut de la facture du jalon <b>Facture client publiée</b> est remplacé par <b>Prêt pour la facturation</b>.</span><span class="sxs-lookup"><span data-stu-id="fb348-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fb348-154">Facturation du crédit partiel d’un jalon facturé.</span><span class="sxs-lookup"><span data-stu-id="fb348-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fb348-155">Ce scénario n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fb348-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
