---
title: Workflow de gestion des dépenses
description: Cette rubrique explique comment utiliser le système de workflow dans Microsoft Dynamics 365 Finance, pour mettre en place un processus de révision des notes de frais dans la gestion des dépenses.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005203"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="6b040-103">Workflow de gestion des dépenses</span><span class="sxs-lookup"><span data-stu-id="6b040-103">Expense management workflow</span></span>

<span data-ttu-id="6b040-104">Vous pouvez utiliser le système de workflow pour mettre en place un processus de révision des notes de frais dans la gestion des dépenses.</span><span class="sxs-lookup"><span data-stu-id="6b040-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="6b040-105">Vous pouvez configurer un workflow qui utilise les critères suivants pour déterminer qui approuve les notes de frais :</span><span class="sxs-lookup"><span data-stu-id="6b040-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="6b040-106">La hiérarchie de reporting des employés et les limites d’approbation prédéfinies</span><span class="sxs-lookup"><span data-stu-id="6b040-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="6b040-107">Approbation à plusieurs niveaux qui prend en charge les approbateurs intermédiaires et un approbateur final</span><span class="sxs-lookup"><span data-stu-id="6b040-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="6b040-108">Dimensions financières et responsabilité du projet</span><span class="sxs-lookup"><span data-stu-id="6b040-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="6b040-109">Affectation à des utilisateurs ou groupes d’utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="6b040-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="6b040-110">Les approbations de workflow peuvent être créées pour les notes de frais, les demandes de voyage, les avances de fonds et le recouvrement de la taxe sur la valeur ajoutée (TVA).</span><span class="sxs-lookup"><span data-stu-id="6b040-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="6b040-111">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6b040-111">**Example**</span></span>

<span data-ttu-id="6b040-112">Le processus suivant est un exemple de workflow de gestion des dépenses pour une note de frais.</span><span class="sxs-lookup"><span data-stu-id="6b040-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="6b040-113">Un employé crée et enregistre une note de frais.</span><span class="sxs-lookup"><span data-stu-id="6b040-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="6b040-114">L’employé envoit la note de frais pour approbation.</span><span class="sxs-lookup"><span data-stu-id="6b040-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="6b040-115">L’approbateur est identifié en fonction des règles qui ont été définies lors de la configuration du workflow.</span><span class="sxs-lookup"><span data-stu-id="6b040-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="6b040-116">L’approbateur reçoit une notification indiquant qu’une note de frais est prête pour approbation.</span><span class="sxs-lookup"><span data-stu-id="6b040-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="6b040-117">L’approbateur examine la note de frais et vérifie que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="6b040-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="6b040-118">Les dépenses ne violent aucune politique de dépenses.</span><span class="sxs-lookup"><span data-stu-id="6b040-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="6b040-119">Si une dépense enfreint une politique, l’approbateur vérifie que la note de frais comprend une justification commerciale valide.</span><span class="sxs-lookup"><span data-stu-id="6b040-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="6b040-120">Les reçus électroniques sont joints à la note de frais.</span><span class="sxs-lookup"><span data-stu-id="6b040-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="6b040-121">L’approbateur approuve la note de frais.</span><span class="sxs-lookup"><span data-stu-id="6b040-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="6b040-122">La note de frais est affectée au coordonnateur des comptes fournisseurs pour validation.</span><span class="sxs-lookup"><span data-stu-id="6b040-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="6b040-123">L’une des étapes suivantes se produit, selon que la comptabilisation automatique est configurée :</span><span class="sxs-lookup"><span data-stu-id="6b040-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="6b040-124">Si la validation automatique est configurée, la note de frais est traitée pour le paiement et le statut de la note de frais est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6b040-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="6b040-125">Si la validation automatique n’est pas configurée, le coordonnateur de la comptabilité fournisseur vérifie que tous les reçus originaux ont été soumis et que les reçus sont alignés avec les dépenses sur la note de frais.</span><span class="sxs-lookup"><span data-stu-id="6b040-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="6b040-126">Tous les codes de taxe saisis dans la note de frais doivent également être vérifiés comme étant corrects.</span><span class="sxs-lookup"><span data-stu-id="6b040-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="6b040-127">Une fois ces exigences vérifiées, le rapport de dépenses est affiché.</span><span class="sxs-lookup"><span data-stu-id="6b040-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="6b040-128">Une fois la note de frais validée, le paiement est autorisé pour la note de frais et l’employé est remboursé.</span><span class="sxs-lookup"><span data-stu-id="6b040-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]