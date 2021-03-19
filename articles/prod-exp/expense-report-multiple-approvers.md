---
title: Plusieurs approbateurs sur une note de frais
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l'approbation de plusieurs personnes.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271710"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="bde0a-103">Plusieurs approbateurs sur une note de frais</span><span class="sxs-lookup"><span data-stu-id="bde0a-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="bde0a-104">En fonction des politiques d'approbation des dépenses de votre organisation, il est possible que l'approbation d'une note de frais qui est envoyée à un employé.</span><span class="sxs-lookup"><span data-stu-id="bde0a-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="bde0a-105">Lorsque vous configurez le processus de workflow pour l'approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais.</span><span class="sxs-lookup"><span data-stu-id="bde0a-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="bde0a-106">Par exemple, vous pouvez exiger que toutes les notes de frais soient d'abord approuvées par le responsable de l'employé qui a soumis la note, puis par le coordinateur de la comptabilité fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bde0a-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="bde0a-107">Si vous décidez d'exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l'une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="bde0a-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="bde0a-108">Ajoutez un élément d’approbation qui comporte une étape.</span><span class="sxs-lookup"><span data-stu-id="bde0a-108">Add one approval element that has one step.</span></span> <span data-ttu-id="bde0a-109">Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par 50 % des membres du groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bde0a-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="bde0a-110">Ajoutez un élément d’approbation qui comporte plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="bde0a-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="bde0a-111">Par exemple, l’élément d’approbation peut comporter les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bde0a-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="bde0a-112">Le responsable de l’employé qui a soumis la note de frais l’approuve.</span><span class="sxs-lookup"><span data-stu-id="bde0a-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="bde0a-113">Le commis à la comptabilité fournisseur vérifie les reçus et les articles des notes de frais.</span><span class="sxs-lookup"><span data-stu-id="bde0a-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="bde0a-114">Le responsable du budget approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="bde0a-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="bde0a-115">Ajoutez plusieurs éléments d’approbation, chacun comportant une étape.</span><span class="sxs-lookup"><span data-stu-id="bde0a-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="bde0a-116">Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bde0a-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="bde0a-117">Le responsable de l’employé approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="bde0a-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="bde0a-118">Le responsable du budget approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="bde0a-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]