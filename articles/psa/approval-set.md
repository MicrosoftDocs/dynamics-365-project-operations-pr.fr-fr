---
title: Ensembles d’approbations
description: Cette rubrique fournit des informations sur l’ensemble d’approbation, les demandes et les sous-ensembles de ces opérations.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116868"
---
# <a name="approval-sets"></a><span data-ttu-id="024f5-103">Ensembles d’approbations</span><span class="sxs-lookup"><span data-stu-id="024f5-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="024f5-104">Les ensembles d’approbation regroupent les demandes d’approbation en sous-ensembles d’opérations plus petits.</span><span class="sxs-lookup"><span data-stu-id="024f5-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="024f5-105">Ce regroupement permet à Project de traiter les approbations dans l’ordre et permet le séquençage et les nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="024f5-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="024f5-106">Le regroupement améliore la fiabilité et la traçabilité du traitement des approbations pour de gros volumes d’approbations.</span><span class="sxs-lookup"><span data-stu-id="024f5-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="024f5-107">Les ensembles d’approbation indiquent l’état de traitement global de leurs enregistrements associés.</span><span class="sxs-lookup"><span data-stu-id="024f5-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="024f5-108">Lorsqu’un enregistrement d’approbation est traité à l’aide d’un ensemble d’approbations, l’enregistrement passe de **Envoyé** à **Approuvé**, et est dissocié de l’ensemble d’approbations.</span><span class="sxs-lookup"><span data-stu-id="024f5-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="024f5-109">Si un enregistrement échoue lorsqu’il est soumis à l’approbation, l’enregistrement conserve le statut **Envoyé** et l’ensemble d’approbations est marqué comme ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="024f5-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="024f5-110">L’ensemble d’approbations consigne le message d’erreur de l’échec.</span><span class="sxs-lookup"><span data-stu-id="024f5-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="024f5-111">Traitement des approbations et des ensembles d’approbations</span><span class="sxs-lookup"><span data-stu-id="024f5-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="024f5-112">Les approbations mises en file d’attente pour traitement sont visibles dans la vue **Approbations en cours de traitement**.</span><span class="sxs-lookup"><span data-stu-id="024f5-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="024f5-113">Le système essaie de traiter toutes les entrées plusieurs fois de manière asynchrone, y compris en retentant une approbation si les tentatives précédentes ont échoué.</span><span class="sxs-lookup"><span data-stu-id="024f5-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="024f5-114">Le champ **Durée de vie de l’ensemble d’approbations** consigne le nombre de tentatives restantes pour traiter l’ensemble avant qu’il ne soit marqué comme ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="024f5-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="024f5-115">Approbations et ensembles d’approbations ayant échoué</span><span class="sxs-lookup"><span data-stu-id="024f5-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="024f5-116">La vue **Approbations ayant échoué** répertorie toutes les approbations qui nécessitent une intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="024f5-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="024f5-117">Ouvrez les journaux d’ensemble d’approbations associés pour identifier la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="024f5-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="024f5-118">Le fait de sélectionner **Réessayer** incrémente le compteur de durée de vie de l’ensemble d’approbations, remet l’ensemble d’approbations au statut de **Traitement en cours**, et tente de traiter les enregistrements restants.</span><span class="sxs-lookup"><span data-stu-id="024f5-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="024f5-119">Configurer les ensembles d’approbation</span><span class="sxs-lookup"><span data-stu-id="024f5-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="024f5-120">Activer la fonctionnalité Ensembles d’approbation</span><span class="sxs-lookup"><span data-stu-id="024f5-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="024f5-121">Avant d’activer la fonctionnalité Ensembles d’approbations, vérifiez qu’aucune approbation n’est en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="024f5-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="024f5-122">Accédez à la page **Paramètres du projet** et sélectionnez **Contrôle de fonctionnalité** > **Activer les approbations modernes**.</span><span class="sxs-lookup"><span data-stu-id="024f5-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="024f5-123">Désactiver la fonctionnalité Ensembles d’approbation</span><span class="sxs-lookup"><span data-stu-id="024f5-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="024f5-124">Avant de désactiver la fonctionnalité Ensembles d’approbations, vérifiez qu’aucune approbation n’est en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="024f5-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="024f5-125">Accédez à la page **Paramètres du projet** et sélectionnez **Contrôle de fonctionnalité** > **Désactiver les approbations modernes**.</span><span class="sxs-lookup"><span data-stu-id="024f5-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="024f5-126">Configuration du seuil asynchrone</span><span class="sxs-lookup"><span data-stu-id="024f5-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="024f5-127">Lorsque des ensembles d’approbation sont créés, le traitement passe à l’arrière-plan lorsque le nombre sélectionné d’enregistrements destinés à l’approbation dépasse le seuil indiqué.</span><span class="sxs-lookup"><span data-stu-id="024f5-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="024f5-128">Utilisez le champ **Seuil asynchrone** pour configurer le moment où le traitement des approbations doit être exécuté de manière synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="024f5-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="024f5-129">Les valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="024f5-129">Valid values are:</span></span>

  - <span data-ttu-id="024f5-130">Zéro : toutes les demandes doivent être traitées de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="024f5-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="024f5-131">Nombres supérieurs à zéro : les approbations sont traitées de manière asynchrone uniquement lorsque le nombre d’approbations soumises dépasse cette valeur.</span><span class="sxs-lookup"><span data-stu-id="024f5-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
