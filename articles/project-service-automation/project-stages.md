---
title: Phases du projet
description: Cette rubrique fournit des informations sur les phases du projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168021"
---
# <a name="project-stages"></a><span data-ttu-id="144c8-103">Phases du projet</span><span class="sxs-lookup"><span data-stu-id="144c8-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="144c8-104">Les phases d'un projet sont mises à jour pour refléter l'état du projet à mesure qu'il progresse.</span><span class="sxs-lookup"><span data-stu-id="144c8-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="144c8-105">Les flux des processus d'entreprise par défaut mettent automatiquement à jour certaines phases du projet pendant que d'autres sont mises à jour manuellement par le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="144c8-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="144c8-106">Les phases suivantes sont définies dans le flux des processus d'entreprise par défaut :</span><span class="sxs-lookup"><span data-stu-id="144c8-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="144c8-107">Nouveau</span><span class="sxs-lookup"><span data-stu-id="144c8-107">New</span></span>
- <span data-ttu-id="144c8-108">Devis</span><span class="sxs-lookup"><span data-stu-id="144c8-108">Quote</span></span>
- <span data-ttu-id="144c8-109">Planifier</span><span class="sxs-lookup"><span data-stu-id="144c8-109">Plan</span></span>
- <span data-ttu-id="144c8-110">Livrer</span><span class="sxs-lookup"><span data-stu-id="144c8-110">Deliver</span></span>
- <span data-ttu-id="144c8-111">Fin</span><span class="sxs-lookup"><span data-stu-id="144c8-111">Complete</span></span>
- <span data-ttu-id="144c8-112">Fermer</span><span class="sxs-lookup"><span data-stu-id="144c8-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="144c8-113">Nouveau</span><span class="sxs-lookup"><span data-stu-id="144c8-113">New</span></span>

<span data-ttu-id="144c8-114">Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="144c8-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="144c8-115">Si le projet a été créé à partir d'un modèle, il peut posséder des données de planification, d'estimation ou d'équipe.</span><span class="sxs-lookup"><span data-stu-id="144c8-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="144c8-116">Sinon, il s'agit simplement d'un plan du projet, et les autres composants doivent être entrés.</span><span class="sxs-lookup"><span data-stu-id="144c8-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="144c8-117">Devis</span><span class="sxs-lookup"><span data-stu-id="144c8-117">Quote</span></span>

<span data-ttu-id="144c8-118">Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="144c8-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="144c8-119">Lorsque le projet est dans la phase **Devis**, l'onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.</span><span class="sxs-lookup"><span data-stu-id="144c8-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="144c8-120">Planifier</span><span class="sxs-lookup"><span data-stu-id="144c8-120">Plan</span></span>

<span data-ttu-id="144c8-121">Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**.</span><span class="sxs-lookup"><span data-stu-id="144c8-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="144c8-122">Lorsque le projet est dans la phase **Planifier**, la page **Entité du projet** affiche les détails du contrat.</span><span class="sxs-lookup"><span data-stu-id="144c8-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="144c8-123">Livrer</span><span class="sxs-lookup"><span data-stu-id="144c8-123">Deliver</span></span>

<span data-ttu-id="144c8-124">Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.</span><span class="sxs-lookup"><span data-stu-id="144c8-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="144c8-125">Fin</span><span class="sxs-lookup"><span data-stu-id="144c8-125">Complete</span></span> 

<span data-ttu-id="144c8-126">Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="144c8-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="144c8-127">En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="144c8-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="144c8-128">Fermer</span><span class="sxs-lookup"><span data-stu-id="144c8-128">Close</span></span>

<span data-ttu-id="144c8-129">Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="144c8-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="144c8-130">À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="144c8-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
