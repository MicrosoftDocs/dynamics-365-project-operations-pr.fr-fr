---
title: Confirmer une facture pro forma basée sur un projet
description: Cette rubrique fournit des informations sur la confirmation d’une facture pro forma basée sur un projet.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867127"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="18c3d-103">Confirmer une facture pro forma basée sur un projet</span><span class="sxs-lookup"><span data-stu-id="18c3d-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="18c3d-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="18c3d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="18c3d-105">Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**.</span><span class="sxs-lookup"><span data-stu-id="18c3d-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="18c3d-106">Lorsqu’une facture est confirmée, elle devient en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="18c3d-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="18c3d-107">À partir de ce moment-là, la facture ne pourra être corrigée que s’il y a des corrections ou des crédits initiés par le client.</span><span class="sxs-lookup"><span data-stu-id="18c3d-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="18c3d-108">Le tableau suivant répertorie les chiffres réels créés par le système.</span><span class="sxs-lookup"><span data-stu-id="18c3d-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="18c3d-109">Ces chiffres réels sont créés lorsque certaines opérations sont effectuées sur le projet de facture de projet avant sa confirmation.</span><span class="sxs-lookup"><span data-stu-id="18c3d-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="18c3d-110">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="18c3d-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="18c3d-111">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="18c3d-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-112">Facturation d’une avance ou d’une provision</span><span class="sxs-lookup"><span data-stu-id="18c3d-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-113">Un chiffre d’affaires facturé réel de type <strong>Provision</strong> est créé pour le montant de l’avance ou de la provision.</span><span class="sxs-lookup"><span data-stu-id="18c3d-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-114">Un chiffre réel de vente non facturé avec un montant négatif de la provision ou de l’avance à utiliser pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="18c3d-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-115">Après avoir entièrement rapproché une provision ou une avance sur une facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-116">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="18c3d-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="18c3d-117">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l’avance.</span><span class="sxs-lookup"><span data-stu-id="18c3d-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-118">Les chiffres réels des ventes facturées pour le montant de cette facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18c3d-119">Après avoir partiellement rapproché une provision ou une avance sur une facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-120">Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="18c3d-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="18c3d-121">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l’avance.</span><span class="sxs-lookup"><span data-stu-id="18c3d-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-122">Les chiffres réels des ventes facturées pour le montant de cette facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-123">Un chiffre d’affaires non facturé négatif d’un montant de la provision ou de l’avance restant à utiliser pour le rapprochement sur les prochaines factures.</span><span class="sxs-lookup"><span data-stu-id="18c3d-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-124">Facturation d’une transaction de temps sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-125">Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-126">Un chiffre réel de vente facturée pour les heures et le montant figurant sur l’approbation du temps d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18c3d-127">Facturation d’une transaction de temps qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-128">Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-129">Un nouveau réel de ventes qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-130">Un nouveau chiffre réel de vente non facturé qui n’est pas facturable pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture modifiée, une contrepassation des chiffres réels de vente et un chiffre réel de ventes facturées équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-131">Facturation d’une opération de temps qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-132">Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-133">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-134">Facturation d’une transaction de dépense sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="18c3d-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-135">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-136">Un chiffre réel de vente pour la quantité et le montant figurant sur l’approbation de dépense d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18c3d-137">Facturation d’une transacton de dépense qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-138">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-139">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-140">Un nouveau réel de ventes non facturé qui n’est pas facturable pour la quantité et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-141">Facturation d’une transacton de dépense qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-142">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-143">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-144">Facturation d’une transaction de matériel sans aucune modification sur la facture provisoire.</span><span class="sxs-lookup"><span data-stu-id="18c3d-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-145">Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-146">Un chiffre réel de vente facturée pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18c3d-147">Facturation d’une transaction de matériel qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-148">Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation du temps d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-149">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-150">Un nouveau réel de ventes non facturé qui n’est pas facturable pour la quantité et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-151">Facturation d’une transaction de matériel qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="18c3d-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-152">Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-153">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="18c3d-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18c3d-154">Facturation des frais.</span><span class="sxs-lookup"><span data-stu-id="18c3d-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-155">Une annulation des ventes non facturées pour le montant des frais sur la ligne de journal d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-156">Un chiffre réel de vente pour la quantité et le montant figurant sur la ligne de journal d’origine.</span><span class="sxs-lookup"><span data-stu-id="18c3d-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="18c3d-157">Facturation d’un jalon.</span><span class="sxs-lookup"><span data-stu-id="18c3d-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18c3d-158">Un chiffre réel de vente facturée pour le montant du jalon sur le jalon d’origine dans la ligne de contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="18c3d-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
