---
title: Types de phase du projet
description: Cette rubrique fournit des informations sur les phases du projet.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123049"
---
# <a name="project-stage-types"></a><span data-ttu-id="eaec7-103">Types de phase du projet</span><span class="sxs-lookup"><span data-stu-id="eaec7-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eaec7-104">Les phases d’un projet sont conçues pour refléter l’état du projet à mesure qu’il progresse.</span><span class="sxs-lookup"><span data-stu-id="eaec7-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="eaec7-105">Les personnalisations permettent de mettre à jour automatiquement les phases avec les flux des processus d’entreprise, Power Automate ou des extensions de plug-in.</span><span class="sxs-lookup"><span data-stu-id="eaec7-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="eaec7-106">Les phases suivantes sont définies dans le flux des processus d’entreprise par défaut :</span><span class="sxs-lookup"><span data-stu-id="eaec7-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="eaec7-107">Nouveau</span><span class="sxs-lookup"><span data-stu-id="eaec7-107">New</span></span>
- <span data-ttu-id="eaec7-108">Devis</span><span class="sxs-lookup"><span data-stu-id="eaec7-108">Quote</span></span>
- <span data-ttu-id="eaec7-109">Planifier</span><span class="sxs-lookup"><span data-stu-id="eaec7-109">Plan</span></span>
- <span data-ttu-id="eaec7-110">Livrer</span><span class="sxs-lookup"><span data-stu-id="eaec7-110">Deliver</span></span>
- <span data-ttu-id="eaec7-111">Fin</span><span class="sxs-lookup"><span data-stu-id="eaec7-111">Complete</span></span>
- <span data-ttu-id="eaec7-112">Fermer</span><span class="sxs-lookup"><span data-stu-id="eaec7-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="eaec7-113">Nouveau</span><span class="sxs-lookup"><span data-stu-id="eaec7-113">New</span></span>

<span data-ttu-id="eaec7-114">Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="eaec7-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="eaec7-115">Si le projet a été créé à partir d’un modèle, il peut posséder des données de planification, d’estimation ou d’équipe.</span><span class="sxs-lookup"><span data-stu-id="eaec7-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="eaec7-116">Sinon, il s’agit simplement d’un plan du projet, et les autres composants doivent être entrés.</span><span class="sxs-lookup"><span data-stu-id="eaec7-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="eaec7-117">Devis</span><span class="sxs-lookup"><span data-stu-id="eaec7-117">Quote</span></span>

<span data-ttu-id="eaec7-118">Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="eaec7-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="eaec7-119">Lorsque le projet est dans la phase **Devis**, l’onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.</span><span class="sxs-lookup"><span data-stu-id="eaec7-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="eaec7-120">Planifier</span><span class="sxs-lookup"><span data-stu-id="eaec7-120">Plan</span></span>

<span data-ttu-id="eaec7-121">Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**.</span><span class="sxs-lookup"><span data-stu-id="eaec7-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="eaec7-122">Lorsque le projet est dans la phase **Planifier**, la page **Entité du projet** affiche les détails du contrat.</span><span class="sxs-lookup"><span data-stu-id="eaec7-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="eaec7-123">Livrer</span><span class="sxs-lookup"><span data-stu-id="eaec7-123">Deliver</span></span>

<span data-ttu-id="eaec7-124">Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.</span><span class="sxs-lookup"><span data-stu-id="eaec7-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="eaec7-125">Fin</span><span class="sxs-lookup"><span data-stu-id="eaec7-125">Complete</span></span> 

<span data-ttu-id="eaec7-126">Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="eaec7-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="eaec7-127">En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="eaec7-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="eaec7-128">Fermer</span><span class="sxs-lookup"><span data-stu-id="eaec7-128">Close</span></span>

<span data-ttu-id="eaec7-129">Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="eaec7-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="eaec7-130">À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eaec7-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
