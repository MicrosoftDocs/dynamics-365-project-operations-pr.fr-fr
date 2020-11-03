---
title: Confirmer une facture pro forma
description: Cette rubrique offre des informations sur la confirmation d’une facture pro forma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075585"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="34ea8-103">Confirmer une facture pro forma</span><span class="sxs-lookup"><span data-stu-id="34ea8-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="34ea8-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="34ea8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="34ea8-105">Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**.</span><span class="sxs-lookup"><span data-stu-id="34ea8-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="34ea8-106">Lorsqu'une facture est confirmée, elle devient en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="34ea8-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="34ea8-107">À l'avenir, la facture ne pourra être corrigée que s'il y a des corrections ou des crédits initiés par le client, ou lorsqu'elle est marquée comme payée.</span><span class="sxs-lookup"><span data-stu-id="34ea8-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="34ea8-108">Le tableau suivant répertorie les chiffres réels créés par le système.</span><span class="sxs-lookup"><span data-stu-id="34ea8-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="34ea8-109">Ces chiffres réels sont créés lorsque certaines opérations sont effectuées sur le projet de facture de projet avant sa confirmation.</span><span class="sxs-lookup"><span data-stu-id="34ea8-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="34ea8-110">
                    <strong>Scénario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34ea8-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="34ea8-111">
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34ea8-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="34ea8-112">Facturation d'une transaction de temps sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="34ea8-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-113">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-114">Un chiffre réel de vente facturée pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="34ea8-115">Facturation d'une transaction de temps qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="34ea8-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-116">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-117">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-118">Un nouveau réel de ventes non facturé qui n'est pas facturable pour les heures et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="34ea8-119">Facturation d'une opération de temps qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="34ea8-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-120">Une annulation des ventes non facturées pour les heures et le montant figurant sur l'approbation du temps d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-121">Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="34ea8-122">Facturation d'une transaction de dépense sans aucune modification sur le projet de facture.</span><span class="sxs-lookup"><span data-stu-id="34ea8-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-123">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-124">Un chiffre réel de vente pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="34ea8-125">Facturation d'une transacton de dépense qui a été modifiée pour réduire la quantité.</span><span class="sxs-lookup"><span data-stu-id="34ea8-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-126">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-127">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-128">Un nouveau réel de ventes non facturé qui n'est pas facturable pour la quantité et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="34ea8-129">Facturation d'une transacton de dépense qui a été modifiée pour augmenter la quantité.</span><span class="sxs-lookup"><span data-stu-id="34ea8-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-130">Une annulation des ventes non facturées pour la quantité et le montant figurant sur l'approbation de dépense d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-131">Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.</span><span class="sxs-lookup"><span data-stu-id="34ea8-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="34ea8-132">Facturation des frais.</span><span class="sxs-lookup"><span data-stu-id="34ea8-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-133">Une annulation des ventes non facturées pour le montant des frais sur la ligne de journal d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-134">Un chiffre réel de vente pour la quantité et le montant figurant sur la ligne de journal d'origine.</span><span class="sxs-lookup"><span data-stu-id="34ea8-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="34ea8-135">Facturation d'un jalon.</span><span class="sxs-lookup"><span data-stu-id="34ea8-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="34ea8-136">Un chiffre réel de vente facturée pour le montant du jalon sur le jalon d'origine dans la ligne de contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="34ea8-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>