---
title: Performance de la proposition de facture de projet
description: Cette rubrique fournit des informations sur les améliorations des performances des propositions de facture de projet.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573556"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="0d66e-103">Performance de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="0d66e-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0d66e-104">Lorsque vous créez une nouvelle proposition de facture, vous pouvez rencontrer des problèmes de performances à mesure que le nombre de projets et de sous-projets augmente.</span><span class="sxs-lookup"><span data-stu-id="0d66e-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="0d66e-105">Pour améliorer les performances, une fonctionnalité est disponible pour réduire le temps nécessaire à la création d’une nouvelle proposition de facture pour les transactions de projet validées.</span><span class="sxs-lookup"><span data-stu-id="0d66e-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="0d66e-106">Activer l’amélioration des performances de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="0d66e-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="0d66e-107">Pour activer la fonctionnalité d’amélioration des performances de la proposition de facture de projet, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0d66e-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="0d66e-108">Accédez à **Gestion des fonctionnalités** > **Tout**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="0d66e-109">Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="0d66e-110">Sélectionnez **Activer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="0d66e-111">Actualisez votre navigateur, puis créez une nouvelle proposition de facture.</span><span class="sxs-lookup"><span data-stu-id="0d66e-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="0d66e-112">Désactiver l’amélioration des performances de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="0d66e-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="0d66e-113">Procédez de la manière suivante pour désactiver l’amélioration des performances de la proposition de facture de projet.</span><span class="sxs-lookup"><span data-stu-id="0d66e-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="0d66e-114">Accédez à **Gestion des fonctionnalités** > **Tout**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="0d66e-115">Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="0d66e-116">Sélectionnez **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="0d66e-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="0d66e-117">Actualisez votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="0d66e-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="0d66e-118">Les performances de la proposition de facture ne peuvent pas être appliquées lorsque les règles de facturation sont activées ou que des processus par lots sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0d66e-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
