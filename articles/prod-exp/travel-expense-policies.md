---
title: Configurer des politiques de dépenses
description: Vous pouvez configurer des politiques de dépenses que vos collaborateurs devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement dans Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960694"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="a5ccf-103">Configurer des politiques de dépenses</span><span class="sxs-lookup"><span data-stu-id="a5ccf-103">Set up expense policies</span></span>

<span data-ttu-id="a5ccf-104">Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="a5ccf-105">La mise en œuvre de politiques de dépenses peut vous aider à gérer efficacement les dépenses.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="a5ccf-106">Par exemple, vous pouvez définir une politique pour les dépenses d'hôtel à New York, qui stipule que les dépenses par nuit ne peuvent pas dépasser 250 USD.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="a5ccf-107">Si un collaborateur soumet une note de frais ou une demande de voyage dans laquelle le tarif de la chambre dépasse ce montant, le système informera</span><span class="sxs-lookup"><span data-stu-id="a5ccf-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="a5ccf-108">l’employé que le montant de la dépense a été dépassé, conformément à la politique.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="a5ccf-109">Vous pouvez configurer le message que l’employé recevra lorsque vous</span><span class="sxs-lookup"><span data-stu-id="a5ccf-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="a5ccf-110">définissez la politique.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-110">define the policy.</span></span>      
        
<span data-ttu-id="a5ccf-111">Vous pouvez définir trois types de politiques :</span><span class="sxs-lookup"><span data-stu-id="a5ccf-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="a5ccf-112">Avertissement – Permet à l'employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et</span><span class="sxs-lookup"><span data-stu-id="a5ccf-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="a5ccf-113">pour un rapport ultérieur.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-113">for later reporting.</span></span>        

- <span data-ttu-id="a5ccf-114">Erreur – Oblige l'employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="a5ccf-115">Justification – Oblige l'employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="a5ccf-116">Conseils en matière de politique</span><span class="sxs-lookup"><span data-stu-id="a5ccf-116">Policy tips</span></span>
<span data-ttu-id="a5ccf-117">Voici quelques suggestions qui peuvent vous aider lors de la création de nouvelles politiques de gestion des dépenses.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="a5ccf-118">Les politiques prennent effet à une date et ne prennent pas effet si la politique est créée avec une date postérieure à la date à laquelle la dépense a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="a5ccf-119">Par exemple, si vous créez une politique aujourd'hui pour appliquer une dépense de repas maximale de 50 USD, toutes les dépenses existantes saisies avant aujourd'hui ne seront pas comparées à cette politique.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="a5ccf-120">Lors de la création d'une politique pour une catégorie de dépenses pouvant être détaillée, pensez à ajouter une condition pour le type de ligne de dépenses.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="a5ccf-121">Certaines politiques, telles que l'exigence d'un reçu, peuvent ne pas avoir de sens pour les lignes détaillées et ne doivent être appliquées qu'à la ligne d'en-tête ou à une ligne non détaillée.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="a5ccf-122">Les politiques de gestion des dépenses sont évaluées par défaut par rapport à l'entité source.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="a5ccf-123">Pour les scénarios intersociétés, vous pouvez définir la stratégie à évaluer par rapport à l’entité de destination (entité emprunteuse) à la place.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="a5ccf-124">Pour exécuter les politiques sur l'entité de destination, activez la fonctionnalité « Évaluer la politique de dépenses par rapport à l'entité juridique emprunteuse » dans l'espace de travail **Gestion des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="a5ccf-125">Quand évaluer les politiques</span><span class="sxs-lookup"><span data-stu-id="a5ccf-125">When to evaluate policies</span></span>

<span data-ttu-id="a5ccf-126">Dans les paramètres de gestion des dépenses, vous disposez d'une option pour évaluer les politiques de gestion des dépenses lorsqu'une ligne est enregistrée ou lorsqu'une note de frais est soumise.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="a5ccf-127">Si vous choisissez d'évaluer lorsqu'une ligne est enregistrée, cela permet de garantir que les utilisateurs ont une meilleure visibilité sur ce qu'ils doivent faire pour compléter leur note de frais en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="a5ccf-128">Sinon, vous pouvez retarder l'évaluation de la politique et gagner du temps si la validation a lieu à la fin, lors de la soumission au flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
