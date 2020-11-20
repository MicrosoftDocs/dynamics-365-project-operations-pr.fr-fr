---
title: Définir des politiques de dépenses
description: Vous pouvez définir des politiques de dépenses que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.
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
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128415"
---
# <a name="define-expense-policies"></a><span data-ttu-id="25b5c-103">Définir des politiques de dépenses</span><span class="sxs-lookup"><span data-stu-id="25b5c-103">Define expense policies</span></span>

<span data-ttu-id="25b5c-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="25b5c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25b5c-105">Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.</span><span class="sxs-lookup"><span data-stu-id="25b5c-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="25b5c-106">La mise en œuvre de politiques de dépenses peut vous aider à gérer efficacement les dépenses.</span><span class="sxs-lookup"><span data-stu-id="25b5c-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="25b5c-107">Par exemple, vous pouvez définir une politique pour les dépenses d’hôtel à New York, qui stipule que les dépenses par nuit ne peuvent pas dépasser 250 USD.</span><span class="sxs-lookup"><span data-stu-id="25b5c-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="25b5c-108">Si un employé soumet une note de frais ou une demande de voyage où le tarif de la chambre dépasse ce montant, le système informera</span><span class="sxs-lookup"><span data-stu-id="25b5c-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="25b5c-109">l’employé que le montant de la dépense a été dépassé, conformément à la politique.</span><span class="sxs-lookup"><span data-stu-id="25b5c-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="25b5c-110">Vous pouvez configurer le message que l’employé recevra lorsque vous</span><span class="sxs-lookup"><span data-stu-id="25b5c-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="25b5c-111">définissez la politique.</span><span class="sxs-lookup"><span data-stu-id="25b5c-111">define the policy.</span></span>      
        
<span data-ttu-id="25b5c-112">Vous pouvez définir trois types de politiques :</span><span class="sxs-lookup"><span data-stu-id="25b5c-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="25b5c-113">**Avertissement** : Permet à l’employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et</span><span class="sxs-lookup"><span data-stu-id="25b5c-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="25b5c-114">pour un rapport ultérieur.</span><span class="sxs-lookup"><span data-stu-id="25b5c-114">for later reporting.</span></span>        

- <span data-ttu-id="25b5c-115">**Erreur** : Oblige l’employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.</span><span class="sxs-lookup"><span data-stu-id="25b5c-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="25b5c-116">**Justification** : Oblige l’employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.</span><span class="sxs-lookup"><span data-stu-id="25b5c-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="25b5c-117">Conseils en matière de politique</span><span class="sxs-lookup"><span data-stu-id="25b5c-117">Policy tips</span></span>
<span data-ttu-id="25b5c-118">Voici quelques suggestions qui peuvent vous aider lors de la création de nouvelles politiques de gestion des dépenses :</span><span class="sxs-lookup"><span data-stu-id="25b5c-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="25b5c-119">Les politiques sont à date d’entrée en vigueur, ce qui signifie qu’une politique ne prendra pas effet si elle est créée avec une date postérieure à la date à laquelle la dépense a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="25b5c-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="25b5c-120">Par exemple, vous pouvez créer une nouvelle politique afin d’appliquer une dépense de repas maximale de 50 USD.</span><span class="sxs-lookup"><span data-stu-id="25b5c-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="25b5c-121">Toutes les dépenses existantes saisies avant ne seront pas comparées à cette politique.</span><span class="sxs-lookup"><span data-stu-id="25b5c-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="25b5c-122">Lors de la création d’une politique pour une catégorie de dépenses pouvant être détaillée, pensez à ajouter une condition pour le type de ligne de dépenses.</span><span class="sxs-lookup"><span data-stu-id="25b5c-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="25b5c-123">Certaines politiques, telles que l’exigence d’un reçu, peuvent ne pas avoir de sens pour les lignes détaillées.</span><span class="sxs-lookup"><span data-stu-id="25b5c-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="25b5c-124">Dans ce cas, la politique est appliquée uniquement à la ligne d’en-tête ou à une ligne non détaillée.</span><span class="sxs-lookup"><span data-stu-id="25b5c-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="25b5c-125">Les politiques de gestion des dépenses sont évaluées par défaut par rapport à l’entité source.</span><span class="sxs-lookup"><span data-stu-id="25b5c-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="25b5c-126">Pour les scénarios intersociétés, vous pouvez définir la stratégie à évaluer par rapport à l’entité de destination (entité emprunteuse) à la place.</span><span class="sxs-lookup"><span data-stu-id="25b5c-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="25b5c-127">Pour exécuter les politiques sur l’entité de destination, activez la fonctionnalité **Évaluer la politique de dépenses par rapport à l’entité juridique emprunteuse** dans l’espace de travail **Gestion des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="25b5c-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="25b5c-128">Quand évaluer les politiques</span><span class="sxs-lookup"><span data-stu-id="25b5c-128">When to evaluate policies</span></span>

<span data-ttu-id="25b5c-129">Dans les paramètres de gestion des dépenses, vous pouvez choisir d’évaluer les politiques de gestion des dépenses lorsqu’une ligne est enregistrée ou lorsqu’une note de frais est soumise.</span><span class="sxs-lookup"><span data-stu-id="25b5c-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="25b5c-130">Si vous choisissez d’évaluer le moment où une ligne est enregistrée, les utilisateurs auront une meilleure visibilité sur ce qu’ils doivent faire pour compléter leur note de frais en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="25b5c-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="25b5c-131">Sinon, vous pouvez retarder l’évaluation de la politique et gagner du temps en validant à la fin, lors de la soumission au workflow.</span><span class="sxs-lookup"><span data-stu-id="25b5c-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
