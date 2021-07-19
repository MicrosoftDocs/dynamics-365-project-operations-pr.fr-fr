---
title: Performance de la proposition de facture de projet
description: Cette rubrique fournit des informations sur les améliorations des performances des propositions de facture de projet.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269787"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="4d63d-103">Performance de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="4d63d-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d63d-104">Lorsque vous créez une nouvelle proposition de facture, vous pouvez rencontrer des problèmes de performances à mesure que le nombre de projets et de sous-projets augmente.</span><span class="sxs-lookup"><span data-stu-id="4d63d-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="4d63d-105">Pour améliorer les performances, une fonctionnalité est disponible pour réduire le temps nécessaire à la création d’une nouvelle proposition de facture pour les transactions de projet validées.</span><span class="sxs-lookup"><span data-stu-id="4d63d-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4d63d-106">Activer l’amélioration des performances de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="4d63d-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4d63d-107">Pour activer la fonctionnalité d’amélioration des performances de la proposition de facture de projet, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="4d63d-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="4d63d-108">Accédez à **Gestion des fonctionnalités** > **Tout**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4d63d-109">Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4d63d-110">Sélectionnez **Activer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="4d63d-111">Actualisez votre navigateur, puis créez une nouvelle proposition de facture.</span><span class="sxs-lookup"><span data-stu-id="4d63d-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4d63d-112">Désactiver l’amélioration des performances de la proposition de facture de projet</span><span class="sxs-lookup"><span data-stu-id="4d63d-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4d63d-113">Procédez de la manière suivante pour désactiver l’amélioration des performances de la proposition de facture de projet.</span><span class="sxs-lookup"><span data-stu-id="4d63d-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="4d63d-114">Accédez à **Gestion des fonctionnalités** > **Tout**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4d63d-115">Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4d63d-116">Sélectionnez **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="4d63d-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="4d63d-117">Actualisez votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="4d63d-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4d63d-118">Les performances de la proposition de facture ne peuvent pas être appliquées lorsque les règles de facturation sont activées.</span><span class="sxs-lookup"><span data-stu-id="4d63d-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="4d63d-119">Pendant le traitement par lots pour créer des propositions de facture, le nombre de sous-tâches fractionnera les tâches en un nombre maximal en fonction du nombre de contrats avec des transactions facturables, indépendamment de votre saisie.</span><span class="sxs-lookup"><span data-stu-id="4d63d-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="4d63d-120">Par exemple, si vous entrez **3** pour le nombre de sous-tâches pour la création de propositions de facture par lots et il n’y a que deux contrats avec des transactions facturables, seules deux sous-tâches sont créées.</span><span class="sxs-lookup"><span data-stu-id="4d63d-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
