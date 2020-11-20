---
title: Configurer des workflows pour la gestion des dépenses
description: Vous pouvez configurer un processus de flux de travail utilisé pour examiner et approuver les documents de déplacement et de dépenses.
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
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127695"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="771d8-103">Configurer des workflows pour la gestion des dépenses</span><span class="sxs-lookup"><span data-stu-id="771d8-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="771d8-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="771d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="771d8-105">Vous pouvez configurer un processus de workflow pour examiner et approuver les documents de voyage et de dépenses.</span><span class="sxs-lookup"><span data-stu-id="771d8-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="771d8-106">Vous pouvez définir des workflows pour les notes de frais, les demandes de déplacement et les demandes d’avance de fonds.</span><span class="sxs-lookup"><span data-stu-id="771d8-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="771d8-107">Un workflow représente un processus métier et définit la manière dont un document circule dans le système.</span><span class="sxs-lookup"><span data-stu-id="771d8-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="771d8-108">Le workflow indique également qui doit terminer une tâche ou approuver un document.</span><span class="sxs-lookup"><span data-stu-id="771d8-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="771d8-109">Il y a plusieurs avantages à utiliser le système de workflow dans votre organisation :</span><span class="sxs-lookup"><span data-stu-id="771d8-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="771d8-110">**Processus cohérents** : Vous pouvez définir le processus d’approbation pour des documents spécifiques, tels que les demandes d’achat et les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="771d8-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="771d8-111">Le système de workflow permet de garantir que les documents sont traités et approuvés de manière cohérente et efficace.</span><span class="sxs-lookup"><span data-stu-id="771d8-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="771d8-112">**Visibilité des processus** : Vous pouvez suivre le statut, l’historique et les indicateurs de performance d’une instance de workflow spécifique.</span><span class="sxs-lookup"><span data-stu-id="771d8-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="771d8-113">Cette approche vous aide à déterminer si des modifications doivent être apportées au workflow pour améliorer l’efficacité.</span><span class="sxs-lookup"><span data-stu-id="771d8-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="771d8-114">**Liste de travail centralisée** : Les utilisateurs peuvent afficher une liste de travail centralisée pour afficher les tâches de workflow et les approbations qui leur sont affectées.</span><span class="sxs-lookup"><span data-stu-id="771d8-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="771d8-115">Types de workflow</span><span class="sxs-lookup"><span data-stu-id="771d8-115">Workflow types</span></span>

<span data-ttu-id="771d8-116">Le tableau ci-dessous répertorie les types de workflows que vous pouvez créer dans **Gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="771d8-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="771d8-117"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="771d8-118"><strong>Utilisez ce type pour ce qui suit</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="771d8-119"><strong>Approbation automatique des notes de frais</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="771d8-120">Créez des workflows d’approbation pour les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="771d8-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="771d8-121"><strong>Validation automatique des notes de frais</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="771d8-122">Créez des workflows de validation automatique pour les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="771d8-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="771d8-123"><strong>Article de ligne de dépense</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="771d8-124">Créez des workflows d’approbation pour les articles de ligne sur les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="771d8-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="771d8-125"><strong>Validation automatique des lignes de dépense</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="771d8-126">Créez des workflows de validation automatique pour les articles de ligne sur les notes de frais.</span><span class="sxs-lookup"><span data-stu-id="771d8-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="771d8-127"><strong>Demande de trajet</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="771d8-128">Créez des workflows d’approbation pour les demandes de voyage.</span><span class="sxs-lookup"><span data-stu-id="771d8-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="771d8-129"><strong>Demande d’avance de disponibilités</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="771d8-130">Créez des workflows d’approbation pour les demandes d’avance de fonds.</span><span class="sxs-lookup"><span data-stu-id="771d8-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="771d8-131"><strong>Recouvrement fiscal de la TVA</strong></span><span class="sxs-lookup"><span data-stu-id="771d8-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="771d8-132">Créez des workflows d’approbation pour la récupération de la taxe sur la valeur ajoutée (TVA).</span><span class="sxs-lookup"><span data-stu-id="771d8-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
