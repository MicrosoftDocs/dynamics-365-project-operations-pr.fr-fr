---
title: Entrée de dépense (simplifiée)
description: Cette rubrique fournit des informations sur la façon d’utiliser la saisie de dépenses dans un déploiement simplifié.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965778"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="bf523-103">Entrée de dépense (simplifiée)</span><span class="sxs-lookup"><span data-stu-id="bf523-103">Expense entry (lite)</span></span>

<span data-ttu-id="bf523-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="bf523-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf523-105">La gestion de base ou simplifiée des dépenses est la capacité d’enregistrer des dépenses simples.</span><span class="sxs-lookup"><span data-stu-id="bf523-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="bf523-106">Vous pouvez enregistrer les dépenses par rapport à un projet, puis l’approbateur de projet les examinera et les approuvera.</span><span class="sxs-lookup"><span data-stu-id="bf523-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="bf523-107">Pour plus d’informations sur les fonctionnalités de dépense dans Project Operations Dynamics 365, voir [Vue d’ensemble des dépenses](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf523-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="bf523-108">Capturer une dépense de base</span><span class="sxs-lookup"><span data-stu-id="bf523-108">Capture a basic expense</span></span>

<span data-ttu-id="bf523-109">Vous pouvez capturer vos dépenses afin de pouvoir les envoyer à l’approbateur.</span><span class="sxs-lookup"><span data-stu-id="bf523-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="bf523-110">Accédez à **Dépenses** et sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="bf523-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="bf523-111">Sur la page **Nouvelle dépense**, entrez les informations sur la dépense requise, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bf523-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="bf523-112">Envoyer une dépense de base</span><span class="sxs-lookup"><span data-stu-id="bf523-112">Submit a basic expense</span></span>

<span data-ttu-id="bf523-113">Une fois que vous avez fini de saisir toutes vos dépenses et que vous êtes prêt à les faire approuver, vous devez les envoyer.</span><span class="sxs-lookup"><span data-stu-id="bf523-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="bf523-114">Accédez à **Dépenses** et sélectionnez une dépense.</span><span class="sxs-lookup"><span data-stu-id="bf523-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="bf523-115">Sinon, sélectionnez toutes les dépenses en utilisant la case à cocher sur l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bf523-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="bf523-116">Sélectionnez **Soumettre**.</span><span class="sxs-lookup"><span data-stu-id="bf523-116">Select **Submit**.</span></span> <span data-ttu-id="bf523-117">Le système traite les entrées sélectionnées, puis crée des demandes d’approbation des dépenses.</span><span class="sxs-lookup"><span data-stu-id="bf523-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="bf523-118">Rappeler une dépense de base</span><span class="sxs-lookup"><span data-stu-id="bf523-118">Recall a basic expense</span></span>

<span data-ttu-id="bf523-119">Lorsque vous envoyez une dépense par erreur, vous pouvez la rappeler.</span><span class="sxs-lookup"><span data-stu-id="bf523-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="bf523-120">Le temps nécessaire pour rappeler une entrée de dépense dépend de son stade d’approbation.</span><span class="sxs-lookup"><span data-stu-id="bf523-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="bf523-121">Si l’approbateur n’a pas encore approuvé l’entrée, le rappel peut avoir lieu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bf523-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="bf523-122">Cependant, si l’entrée a déjà été approuvée, l’approbateur est invité à approuver le rappel et à annuler les transactions.</span><span class="sxs-lookup"><span data-stu-id="bf523-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="bf523-123">Accédez à **Dépenses**, puis, dans la liste des dépenses, sélectionnez la dépense à rappeler.</span><span class="sxs-lookup"><span data-stu-id="bf523-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="bf523-124">Sélectionnez **Rappeler**.</span><span class="sxs-lookup"><span data-stu-id="bf523-124">Select **Recall**.</span></span> <span data-ttu-id="bf523-125">Si l’entrée de dépenses n’a pas encore été approuvée, le système la rappelle immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bf523-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="bf523-126">Si l’écriture de dépenses a déjà été approuvée, une demande de rappel est créée pour informer l’approbateur que vous souhaitez annuler la dépense.</span><span class="sxs-lookup"><span data-stu-id="bf523-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="bf523-127">L’approbateur confirmera alors que l’annulation peut être effectuée et l’entrée sera renvoyée.</span><span class="sxs-lookup"><span data-stu-id="bf523-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="bf523-128">Supprimer une dépense de base</span><span class="sxs-lookup"><span data-stu-id="bf523-128">Delete a basic expense</span></span>

<span data-ttu-id="bf523-129">Les dépenses qui n’ont pas encore été envoyées peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="bf523-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="bf523-130">Pour supprimer une dépense déjà envoyée, vous devez d’abord la rappeler.</span><span class="sxs-lookup"><span data-stu-id="bf523-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf523-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf523-131">See also</span></span>

- [<span data-ttu-id="bf523-132">Vue d’ensemble des approbations</span><span class="sxs-lookup"><span data-stu-id="bf523-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
