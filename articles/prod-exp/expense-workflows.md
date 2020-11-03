---
title: Configurer des workflows pour la gestion des dépenses
description: Vous pouvez configurer un processus de workflow pour examiner et approuver les documents de voyage et de dépenses.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075894"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="e3ea4-103">Configurer des workflows pour la gestion des dépenses</span><span class="sxs-lookup"><span data-stu-id="e3ea4-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3ea4-104">Vous pouvez configurer un processus de flux de travail utilisé pour examiner et approuver les documents de déplacement et de dépenses.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="e3ea4-105">Les documents pour lesquels les workflows peuvent être définis incluent les notes de frais, les demandes de déplacement et les demandes d'avance de fonds.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e3ea4-106">Un flux de travail représente un processus métier.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-106">A workflow represents a business process.</span></span> <span data-ttu-id="e3ea4-107">Il définit le transfert d’un document dans le système et indique qui doit traiter une tâche ou approuver un document.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e3ea4-108">Il y a plusieurs avantages à utiliser le système de workflow dans votre organisation :</span><span class="sxs-lookup"><span data-stu-id="e3ea4-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="e3ea4-109">**Processus cohérents** — Vous pouvez définir le processus d’approbation pour des documents spécifiques, tels que des demandes d’achat ou des états de dépenses.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e3ea4-110">Le système de workflow permet de s’assurer que les documents sont traités et approuvés de manière cohérente et efficace.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="e3ea4-111">Visibilité de processus — Vous pouvez suivre le statut, l’historique et les mesures de performance d’une instance de workflow spécifique.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e3ea4-112">Cette approche vous aide à déterminer si des modifications doivent être apportées au workflow pour améliorer l'efficacité.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="e3ea4-113">Liste de travail centralisée — Les utilisateurs peuvent afficher une liste de travail centralisée pour afficher les tâches de workflow et les approbations qui leur sont affectées.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="e3ea4-114">**Types de workflows qu’il est possible de créer**</span><span class="sxs-lookup"><span data-stu-id="e3ea4-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="e3ea4-115">Le tableau ci-dessous répertorie les types de workflows que vous pouvez créer dans **Dépense**.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="e3ea4-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="e3ea4-117"><strong>Utilisez ce type pour ce qui suit</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="e3ea4-118"><strong>Rapport de dépenses</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="e3ea4-119">Créez des workflows d'approbation pour les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="e3ea4-120"><strong>Validation automatique des notes de frais</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="e3ea4-121">Créez des workflows de validation automatique pour les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="e3ea4-122"><strong>Article de ligne de dépense</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="e3ea4-123">Créez des workflows d'approbation pour les articles de ligne sur les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="e3ea4-124"><strong>Validation automatique des lignes de dépense</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="e3ea4-125">Créez des workflows de validation automatique pour les articles de ligne sur les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="e3ea4-126"><strong>Demande de trajet</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="e3ea4-127">Créez des workflows d'approbation pour les demandes de voyage.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="e3ea4-128"><strong>Demande d'avance de disponibilités</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="e3ea4-129">Créez des workflows d'approbation pour les demandes d'avance de fonds.</span><span class="sxs-lookup"><span data-stu-id="e3ea4-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="e3ea4-130"><strong>Recouvrement fiscal de la TVA</strong></span><span class="sxs-lookup"><span data-stu-id="e3ea4-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="e3ea4-131">Créez des workflows d'approbation pour la récupération de la taxe sur la valeur ajoutée (TVA).</span><span class="sxs-lookup"><span data-stu-id="e3ea4-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

