---
title: Notes de frais et approbateurs multiples
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l’approbation de plusieurs personnes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120990"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="40c11-103">Notes de frais et approbateurs multiples</span><span class="sxs-lookup"><span data-stu-id="40c11-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="40c11-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="40c11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40c11-105">En fonction des politiques d’approbation des dépenses de votre organisation, il est possible que l’approbation de plusieurs personnes soit nécessaire lors de la soumission d’une note de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="40c11-106">Lorsque vous configurez le processus de workflow pour l’approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="40c11-107">Par exemple, vous pouvez exiger que toutes les notes de frais soient approuvées par deux personnes distinctes, le responsable de l’employé qui a soumis la note et le coordinateur de la comptabilité fournisseur.</span><span class="sxs-lookup"><span data-stu-id="40c11-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="40c11-108">Si vous décidez d’exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="40c11-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="40c11-109">Ajoutez un élément d’approbation qui comporte une étape.</span><span class="sxs-lookup"><span data-stu-id="40c11-109">Add one approval element that has one step.</span></span> <span data-ttu-id="40c11-110">Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par 50 % des membres du groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="40c11-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="40c11-111">Ajoutez un élément d’approbation qui comporte plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="40c11-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="40c11-112">Par exemple, l’élément d’approbation peut comporter les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40c11-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="40c11-113">Le responsable de l’employé qui a soumis la note de frais l’approuve.</span><span class="sxs-lookup"><span data-stu-id="40c11-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="40c11-114">Le commis à la comptabilité fournisseur vérifie les reçus et les articles des notes de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="40c11-115">Le responsable du budget approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="40c11-116">Ajoutez plusieurs éléments d’approbation, chacun comportant une étape.</span><span class="sxs-lookup"><span data-stu-id="40c11-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="40c11-117">Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40c11-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="40c11-118">Le responsable de l’employé approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="40c11-119">Le responsable du budget approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="40c11-119">The budget owner approves the expense report.</span></span>
