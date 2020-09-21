---
title: Annuler les entrées de temps et de dépenses précédemment approuvées
description: Cette rubrique explique comment annuler une transaction de temps et de dépenses de projet approuvée.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167940"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="f6314-103">Annuler les entrées de temps ou de dépenses précédemment approuvées</span><span class="sxs-lookup"><span data-stu-id="f6314-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f6314-104">Dans la dernière version de Dynamics 365 Project Service Automation, les approbateurs peuvent annuler les entrées de temps ou de dépenses qu'ils ont précédemment approuvées.</span><span class="sxs-lookup"><span data-stu-id="f6314-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="f6314-105">Annuler une entrée de temps ou de dépenses précédemment approuvée</span><span class="sxs-lookup"><span data-stu-id="f6314-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="f6314-106">Procédez comme suit pour annuler une entrée de temps ou de dépenses précédemment approuvée.</span><span class="sxs-lookup"><span data-stu-id="f6314-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="f6314-107">Accédez à **Projets** \> **Mes tâches** \> **Approbations**.</span><span class="sxs-lookup"><span data-stu-id="f6314-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="f6314-108">Dans la page de liste **Approbations**, modifiez la vue avec **Mes approbations passées**.</span><span class="sxs-lookup"><span data-stu-id="f6314-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="f6314-109">Une liste des entrées de temps et de dépenses que vous avez précédemment approuvée s'affiche.</span><span class="sxs-lookup"><span data-stu-id="f6314-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="f6314-110">Sélectionnez une ou plusieurs entrées, puis sélectionnez **Annuler l'approbation**.</span><span class="sxs-lookup"><span data-stu-id="f6314-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="f6314-111">Vous recevez un message d'avertissement.</span><span class="sxs-lookup"><span data-stu-id="f6314-111">You receive a warning message.</span></span>
4. <span data-ttu-id="f6314-112">Sélectionnez **OK** pour annuler l'approbation.</span><span class="sxs-lookup"><span data-stu-id="f6314-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="f6314-113">Comprendre l'impact de l'annulation d'une approbation d'entrée de temps ou de dépenses</span><span class="sxs-lookup"><span data-stu-id="f6314-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="f6314-114">Lorsqu'une approbation est annulée, il existe un impact opérationnel et un impact financier.</span><span class="sxs-lookup"><span data-stu-id="f6314-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="f6314-115">Impact opérationnel</span><span class="sxs-lookup"><span data-stu-id="f6314-115">Operational impact</span></span>

<span data-ttu-id="f6314-116">Du côté des opérations, quand une approbation est annulée, le statut de l'enregistrement est réinitialisé sur **Brouillon**, et l'approbation ne s'affiche plus dans la vue **Mes approbations passées**.</span><span class="sxs-lookup"><span data-stu-id="f6314-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="f6314-117">Au lieu de cela, l'approbation annulée apparaît dans la vue **Entrées de temps pour approbation** ou la vue **Entrées de dépenses pour approbation**, selon que c'était une entrée de temps ou une entrée de dépenses.</span><span class="sxs-lookup"><span data-stu-id="f6314-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="f6314-118">En outre, le statut de l'entrée de temps ou de dépenses associée passe à **Envoyé**, afin que l'entrée associée soit cohérente avec les approbations ayant le statut **Brouillon**.</span><span class="sxs-lookup"><span data-stu-id="f6314-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="f6314-119">En tant qu'approbateur, vous pouvez modifier certains champs d'une approbation qui a le statut **Brouillon**.</span><span class="sxs-lookup"><span data-stu-id="f6314-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="f6314-120">Ces champs incluent **Type de facturation** et **Heures facturables pour des entrées de temps**.</span><span class="sxs-lookup"><span data-stu-id="f6314-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="f6314-121">Après avoir apporté vos modifications, vous pouvez approuver l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f6314-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="f6314-122">Sinon, vous pouvez rejeter l'entrée.</span><span class="sxs-lookup"><span data-stu-id="f6314-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="f6314-123">Si vous rejetez l'approbation d'une entrée de temps, le statut de l'entrée passe à **Renvoyé**.</span><span class="sxs-lookup"><span data-stu-id="f6314-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="f6314-124">Si vous rejetez l'approbation d'une entrée de dépenses, le statut passe à **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="f6314-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="f6314-125">Fonctionellement, les entrées retournées et rejetées se comportent comme une entrée qui a le statut **Brouillon**.</span><span class="sxs-lookup"><span data-stu-id="f6314-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="f6314-126">Un membre de l'équipe du projet peut apporter des modifications requises à l'entrée puis les envoyer pour approbation, ou supprimer entièrement l'entrée.</span><span class="sxs-lookup"><span data-stu-id="f6314-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="f6314-127">Impact financier</span><span class="sxs-lookup"><span data-stu-id="f6314-127">Financial impact</span></span>

<span data-ttu-id="f6314-128">Un projet est également affecté financièrement lorsqu'une approbation est annulée.</span><span class="sxs-lookup"><span data-stu-id="f6314-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="f6314-129">D'abord, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="f6314-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="f6314-130">Le statut d'ajustement est défini sur **Ajusté**.</span><span class="sxs-lookup"><span data-stu-id="f6314-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="f6314-131">Le statut de facturation est défini sur **Annulé**.</span><span class="sxs-lookup"><span data-stu-id="f6314-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="f6314-132">Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="f6314-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="f6314-133">Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux.</span><span class="sxs-lookup"><span data-stu-id="f6314-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="f6314-134">Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité.</span><span class="sxs-lookup"><span data-stu-id="f6314-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="f6314-135">Ces valeurs sont contrepassées à la place.</span><span class="sxs-lookup"><span data-stu-id="f6314-135">These values are reversed instead.</span></span> <span data-ttu-id="f6314-136">Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**.</span><span class="sxs-lookup"><span data-stu-id="f6314-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="f6314-137">Le champ **Statut de l'ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le statut de facturation sur **Annulé**.</span><span class="sxs-lookup"><span data-stu-id="f6314-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="f6314-138">Une fois ces modifications effectuées, le montant enregistré comme dépensé dans le projet et l'arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.</span><span class="sxs-lookup"><span data-stu-id="f6314-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
