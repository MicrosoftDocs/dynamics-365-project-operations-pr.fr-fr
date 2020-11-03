---
title: Confirmation d’une facture pro forma
description: Cette rubrique fournit des informations sur la confirmation des factures pro forma dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075648"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="9abda-103">Confirmation d’une facture pro forma</span><span class="sxs-lookup"><span data-stu-id="9abda-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="9abda-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="9abda-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9abda-105">Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**.</span><span class="sxs-lookup"><span data-stu-id="9abda-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9abda-106">Lorsqu'une facture est confirmée, elle devient en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9abda-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9abda-107">À l'avenir, la facture ne pourra être corrigée que s'il y a des corrections ou des crédits initiés par le client, ou si la facture est marquée comme payée.</span><span class="sxs-lookup"><span data-stu-id="9abda-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="9abda-108">Le tableau suivant répertorie les chiffres réels créés par le système.</span><span class="sxs-lookup"><span data-stu-id="9abda-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9abda-109">Ces chiffres réels sont créés lorsque certaines opérations sont effectuées sur le projet de facture de projet avant sa confirmation.</span><span class="sxs-lookup"><span data-stu-id="9abda-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9abda-110">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9abda-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9abda-111">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9abda-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-112">Facturation d'une avance ou d'une provision</span><span class="sxs-lookup"><span data-stu-id="9abda-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-113">Un chiffre d'affaires facturé réel de type <strong>Provision</strong> est créé pour le montant de l'avance ou de la provision.</span><span class="sxs-lookup"><span data-stu-id="9abda-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-114">Un chiffre d'affaires non facturé réel d'un montant négatif de la provision ou de l'avance à utiliser pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="9abda-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-115">Après avoir entièrement rapproché une provision ou une avance sur une facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-116">Une contrepassation des ventes non facturées de la provision ou de l'avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="9abda-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9abda-117">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l'avance.</span><span class="sxs-lookup"><span data-stu-id="9abda-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-118">Les chiffres réels des ventes facturées pour le montant de cette facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9abda-119">Après avoir partiellement rapproché une provision ou une avance sur une facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-120">Une contrepassation des ventes non facturées de la provision ou de l'avance qui a été créée pour le rapprochement.</span><span class="sxs-lookup"><span data-stu-id="9abda-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9abda-121">Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l'avance.</span><span class="sxs-lookup"><span data-stu-id="9abda-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-122">Les chiffres réels des ventes facturées pour le montant de cette facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-123">Un chiffre d'affaires non facturé négatif d'un montant de la provision ou de l'avance restant à utiliser pour le rapprochement sur les prochaines factures.</span><span class="sxs-lookup"><span data-stu-id="9abda-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-124">Facturation d'une transaction de temps sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-125">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-126">Un chiffre réel de vente facturée pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9abda-127">Facturation d'une transaction de temps qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="9abda-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-128">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-129">Un nouveau réel de ventes qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-130">Un nouveau réel de ventes non facturé qui n'est pas facturable pour les heures et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-131">Facturation d'une opération de temps qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="9abda-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-132">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-133">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-134">Facturation d'une transaction de dépense sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="9abda-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-135">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-136">Un chiffre réel de vente pour la quantité et le montant figurant sur l'approbation de dépense d'origine</span><span class="sxs-lookup"><span data-stu-id="9abda-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9abda-137">Facturation d'une transacton de dépense qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="9abda-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-138">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-139">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-140">Un nouveau réel de ventes non facturé qui n'est pas facturable pour la quantité et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-141">Facturation d'une transacton de dépense qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="9abda-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-142">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-143">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="9abda-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9abda-144">Facturation des frais.</span><span class="sxs-lookup"><span data-stu-id="9abda-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-145">Une annulation des ventes non facturées pour le montant des frais sur la ligne de journal d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-146">Un chiffre réel de vente pour la quantité et le montant figurant sur la ligne de journal d'origine.</span><span class="sxs-lookup"><span data-stu-id="9abda-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9abda-147">Facturation d'un jalon.</span><span class="sxs-lookup"><span data-stu-id="9abda-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-148">Un chiffre réel de vente facturée pour le montant du jalon sur le jalon d'origine dans la ligne de contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="9abda-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9abda-149">Facturation d'une ligne de contrat selon les produits.</span><span class="sxs-lookup"><span data-stu-id="9abda-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9abda-150">Un chiffre d'affaires facturé réel pour la ligne de produits avec la quantité et le montant provenant de la ligne de contrat basée sur le produit.</span><span class="sxs-lookup"><span data-stu-id="9abda-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
