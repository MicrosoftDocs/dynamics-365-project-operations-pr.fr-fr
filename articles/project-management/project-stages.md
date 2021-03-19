---
title: Phases du projet
description: Cette rubrique fournit des informations sur les phases de projet disponibles dans Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286785"
---
# <a name="project-stages"></a><span data-ttu-id="889d2-103">Phases du projet</span><span class="sxs-lookup"><span data-stu-id="889d2-103">Project stages</span></span>

<span data-ttu-id="889d2-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="889d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="889d2-105">Les phases d’un projet sont conçues pour refléter l’état du projet à mesure qu’il progresse.</span><span class="sxs-lookup"><span data-stu-id="889d2-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="889d2-106">Les personnalisations permettent de mettre à jour automatiquement les phases avec les flux des processus d’entreprise, Power Automate ou des extensions de plug-in.</span><span class="sxs-lookup"><span data-stu-id="889d2-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="889d2-107">Les phases suivantes sont définies dans le flux des processus d’entreprise par défaut :</span><span class="sxs-lookup"><span data-stu-id="889d2-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="889d2-108">Nouveau</span><span class="sxs-lookup"><span data-stu-id="889d2-108">New</span></span>
- <span data-ttu-id="889d2-109">Devis</span><span class="sxs-lookup"><span data-stu-id="889d2-109">Quote</span></span>
- <span data-ttu-id="889d2-110">Plan</span><span class="sxs-lookup"><span data-stu-id="889d2-110">Plan</span></span>
- <span data-ttu-id="889d2-111">Livrer</span><span class="sxs-lookup"><span data-stu-id="889d2-111">Deliver</span></span>
- <span data-ttu-id="889d2-112">Fin</span><span class="sxs-lookup"><span data-stu-id="889d2-112">Complete</span></span>
- <span data-ttu-id="889d2-113">Fermer</span><span class="sxs-lookup"><span data-stu-id="889d2-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="889d2-114">Nouveau</span><span class="sxs-lookup"><span data-stu-id="889d2-114">New</span></span>

<span data-ttu-id="889d2-115">Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="889d2-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="889d2-116">Si le projet a été créé à partir d’un modèle, il peut posséder des données de planification, d’estimation ou d’équipe.</span><span class="sxs-lookup"><span data-stu-id="889d2-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="889d2-117">Sinon, il s’agit d’un plan du projet, et les autres composants doivent être entrés.</span><span class="sxs-lookup"><span data-stu-id="889d2-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="889d2-118">Devis</span><span class="sxs-lookup"><span data-stu-id="889d2-118">Quote</span></span>

<span data-ttu-id="889d2-119">Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="889d2-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="889d2-120">Lorsque le projet est dans la phase **Devis**, l’onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.</span><span class="sxs-lookup"><span data-stu-id="889d2-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="889d2-121">Planifier</span><span class="sxs-lookup"><span data-stu-id="889d2-121">Plan</span></span>

<span data-ttu-id="889d2-122">Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**.</span><span class="sxs-lookup"><span data-stu-id="889d2-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="889d2-123">Lorsque le projet est dans la phase **Planifier**, la page **Entité du projet** affiche les détails du contrat.</span><span class="sxs-lookup"><span data-stu-id="889d2-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="889d2-124">Livrer</span><span class="sxs-lookup"><span data-stu-id="889d2-124">Deliver</span></span>

<span data-ttu-id="889d2-125">Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.</span><span class="sxs-lookup"><span data-stu-id="889d2-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="889d2-126">Fin</span><span class="sxs-lookup"><span data-stu-id="889d2-126">Complete</span></span> 

<span data-ttu-id="889d2-127">Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="889d2-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="889d2-128">En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="889d2-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="889d2-129">Fermer</span><span class="sxs-lookup"><span data-stu-id="889d2-129">Close</span></span>

<span data-ttu-id="889d2-130">Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="889d2-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="889d2-131">À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="889d2-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]