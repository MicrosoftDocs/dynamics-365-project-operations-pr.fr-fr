---
title: Rappeler les entrées de temps ou de dépenses approuvées
description: Cette rubrique explique comment rappeler une transaction de temps et de dépenses approuvée précédemment.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147831"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="0d99f-103">Rappeler les entrées de temps ou de dépenses approuvées</span><span class="sxs-lookup"><span data-stu-id="0d99f-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0d99f-104">Un membre de l’équipe du projet ou une autre personne qui envoie une entrée de temps ou de dépenses peut rappeler cette entrée de temps ou de dépenses après qu’elle a été approuvée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="0d99f-105">Le processus de rappel d’une entrée de temps ou de dépenses approuvée se fait en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="0d99f-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="0d99f-106">Un expéditeur demande un rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="0d99f-107">Un approbateur approuve le rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="0d99f-108">Demander un rappel</span><span class="sxs-lookup"><span data-stu-id="0d99f-108">Request a recall</span></span>

<span data-ttu-id="0d99f-109">Procédez comme suit pour demander un rappel d’une entrée de temps ou de dépenses approuvée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="0d99f-110">Pour les entrées de temps, accédez à **Projets** \> **Mes tâches** \> **Entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="0d99f-111">-ou-</span><span class="sxs-lookup"><span data-stu-id="0d99f-111">–or–</span></span>

    <span data-ttu-id="0d99f-112">Pour les entrées de dépenses, accédez à **Projets** \> **Mes tâches** \> **Dépenses**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="0d99f-113">Pour les entrées de temps, sélectionnez toutes les entrées de temps pour une combinaison spécifique d’un projet et d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="0d99f-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="0d99f-114">Sinon, dans la grille, sélectionnez des cellules individuelles pour le temps à une date spécifique pour un projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="0d99f-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="0d99f-115">-ou-</span><span class="sxs-lookup"><span data-stu-id="0d99f-115">–or–</span></span>

    <span data-ttu-id="0d99f-116">Pour les entrées de dépenses, sélectionnez la ligne de l’entrée de dépenses afin de faire le rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="0d99f-117">Sélectionnez **Rappeler**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-117">Select **Recall**.</span></span> <span data-ttu-id="0d99f-118">Une boîte de dialogue de confirmation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0d99f-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="0d99f-119">Si les entrées de temps et de dépenses sélectionnées ont été déjà approuvées, vous êtes invité à indiquer une raison pour le rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="0d99f-120">Entrez une raison pour le rappel, puis sélectionnez **OK** pour confirmer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d99f-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="0d99f-121">Le système envoie à la personne ayant approuvé les entrées une demande d’approbation du rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="0d99f-122">Bien que des entrées de temps et de dépenses approuvées puissent être rappelées, si une entrée de temps ou de dépenses approuvée a déjà été facturée au client, aucune demande de rappel ne peut être créée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="0d99f-123">Un utilisateur qui tente de créer une demande de rappel reçoit un message qui déclare que l’entrée de temps ou de dépenses ne peut pas être rappelée, car elle a déjà été facturée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="0d99f-124">Approuver ou rejeter une demande de rappel</span><span class="sxs-lookup"><span data-stu-id="0d99f-124">Approve or reject a recall request</span></span>

<span data-ttu-id="0d99f-125">Procédez comme suit pour approuver ou rejeter une demande de rappel.</span><span class="sxs-lookup"><span data-stu-id="0d99f-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="0d99f-126">Accédez à **Projets** \> **Mes tâches** \> **Approbations**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="0d99f-127">Dans la page de liste **Approbations**, modifiez la vue avec **Rappeler les demandes d’approbation**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="0d99f-128">Une liste des demandes de rappel envoyées s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0d99f-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="0d99f-129">Sélectionnez une ou plusieurs entrées, puis sélectionnez **Approuver** ou **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="0d99f-130">Si vous avez sélectionné **Approuver**, un message d’avertissement s’affiche qui explique l’impact de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="0d99f-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="0d99f-131">Sélectionnez **OK** pour confirmer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d99f-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="0d99f-132">La demande de rappel est approuvée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-132">The recall request is approved.</span></span>

    <span data-ttu-id="0d99f-133">-ou-</span><span class="sxs-lookup"><span data-stu-id="0d99f-133">–or–</span></span>

    <span data-ttu-id="0d99f-134">Si vous avez sélectionné **Rejeter**, la demande de rappel est rejetée.</span><span class="sxs-lookup"><span data-stu-id="0d99f-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="0d99f-135">comme quand un rappel est demandé, lorsqu’un rappel est approuvé, le système vérifie l’activité de facturation sur les entrées de temps ou de dépenses.</span><span class="sxs-lookup"><span data-stu-id="0d99f-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="0d99f-136">Si une entrée a déjà été facturée, ou si elle figure sur un brouillon de facture, l’approbateur reçoit un message d’erreur qui déclare que le temps ou les dépenses ne peuvent pas être approuvé pour rappel, car ils ont déjà été facturés.</span><span class="sxs-lookup"><span data-stu-id="0d99f-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="0d99f-137">Impact d’une demande de rappel</span><span class="sxs-lookup"><span data-stu-id="0d99f-137">Impact of a recall request</span></span>

<span data-ttu-id="0d99f-138">Lorsqu’une approbation est rappelée, il existe un impact opérationnel et un impact financier.</span><span class="sxs-lookup"><span data-stu-id="0d99f-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="0d99f-139">Impact opérationnel</span><span class="sxs-lookup"><span data-stu-id="0d99f-139">Operational impact</span></span>

<span data-ttu-id="0d99f-140">Si une demande de rappel est approuvée, l’enregistrement de l’approbation est marqué comme **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="0d99f-141">Le statut de l’entrée passe à **Renvoyé** ou **Rejeté**, selon qu’il s’agit d’une entrée de temps ou d’une entrée de dépenses.</span><span class="sxs-lookup"><span data-stu-id="0d99f-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="0d99f-142">Le membre de l’équipe du projet peut afficher les entrées, les modifier, puis renvoyer les entrées, ou supprimer des entrées entièrement.</span><span class="sxs-lookup"><span data-stu-id="0d99f-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="0d99f-143">Si une demande de rappel est rejetée, le statut de l’entrée reste **Approuvé**, et l’entrée ne peut pas être modifiée par le membre de l’équipe du projet ou l’approbateur du projet.</span><span class="sxs-lookup"><span data-stu-id="0d99f-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="0d99f-144">Impact financier</span><span class="sxs-lookup"><span data-stu-id="0d99f-144">Financial impact</span></span>

<span data-ttu-id="0d99f-145">Si une demande de rappel est approuvée, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="0d99f-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="0d99f-146">Le champ **Statut d’ajustement** est mis à jour sur **Ajusté**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="0d99f-147">Le champ **Statut de facturation** est mis à jour sur **Annulé**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="0d99f-148">Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="0d99f-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="0d99f-149">Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux.</span><span class="sxs-lookup"><span data-stu-id="0d99f-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="0d99f-150">Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité.</span><span class="sxs-lookup"><span data-stu-id="0d99f-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="0d99f-151">Ces valeurs sont contrepassées à la place.</span><span class="sxs-lookup"><span data-stu-id="0d99f-151">These values are reversed instead.</span></span> <span data-ttu-id="0d99f-152">Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="0d99f-153">Le champ **Statut de l’ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le champ **Statut de facturation** est défini sur **Annulé**.</span><span class="sxs-lookup"><span data-stu-id="0d99f-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="0d99f-154">En raison de ces modifications, la dépense enregistrée et l’arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.</span><span class="sxs-lookup"><span data-stu-id="0d99f-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="0d99f-155">Si une demande de rappel est rejetée, il n’y a aucun impact financier sur le projet.</span><span class="sxs-lookup"><span data-stu-id="0d99f-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="0d99f-156">Modifications apportées aux enregistrements d’entrées de temps</span><span class="sxs-lookup"><span data-stu-id="0d99f-156">Changes to time entry records</span></span>

<span data-ttu-id="0d99f-157">L’illustration suivante montre les modifications qui se produisent pour des entrées de temps approuvées lorsqu’elles sont rappelées.</span><span class="sxs-lookup"><span data-stu-id="0d99f-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transitions d’état d’entrée de temps](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="0d99f-159">Modifications apportées aux enregistrements d’entrées de dépenses</span><span class="sxs-lookup"><span data-stu-id="0d99f-159">Changes to expense entry records</span></span>

<span data-ttu-id="0d99f-160">L’illustration suivante montre les modifications qui se produisent pour des entrées de dépenses approuvées lorsqu’elles sont rappelées.</span><span class="sxs-lookup"><span data-stu-id="0d99f-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transitions d’état d’entrée de dépenses](media/ExpenseEntryStateTransitions.png)
