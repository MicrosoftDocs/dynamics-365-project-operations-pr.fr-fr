---
title: Vue d’ensemble de Project Service Automation
description: Cette rubrique offre des informations sur Dynamics 365 Project Service Automation vers la solution d’intégration Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d2eace497f4291022da0775cca7cda7d600df7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271080"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="73116-103">Vue d’ensemble de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="73116-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="73116-104">La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Dynamics 365 Finance et Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="73116-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="73116-105">Les modèles d’intégration disponibles avec la fonctionnalité d’intégration de données permettent le flux de projets, les contrats de projet, les projets, les lignes de contrat de projet, les tâches de projets, les catégories de transaction de dépenses, les estimations d’heures et les estimations de dépense depuis Project Service Automation vers Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="73116-106">Si vous utilisez la version 7.3.0, vous devez installer KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="73116-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="73116-107">Vous pourrez alors intégrer des projets à prix fixe.</span><span class="sxs-lookup"><span data-stu-id="73116-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="73116-108">Si vous utilisez la version 7.3.0 et si vous importez des transactions de frais à partir de Project Service Automation, vous devez installer KB 4345320 afin d’inclure ces frais dans la facture du projet.</span><span class="sxs-lookup"><span data-stu-id="73116-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="73116-109">Si vous utilisez la version 8.0, vous serez en mesure d’utiliser l’intégration des tâches de projet, les catégories de transactions de dépenses, les estimations d’heures, les estimations de dépenses et le verrouillage des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="73116-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="73116-110">Si vous utilisez la version 8.0.1 ou une version ultérieure, vous pourrez synchroniser les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="73116-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="73116-111">Avant de pouvoir intégrer Project Service Automation Finance, vous devez configurer les paramètres d’intégration de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="73116-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="73116-112">Pour plus d’informations, consultez [Paramètres d’intégration de Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="73116-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="73116-113">Cette solution d’intégration permet une synchronisation directe dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="73116-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="73116-114">Gérez les contrats de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-115">Créer des projets dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-116">Gérez les lignes de contrat de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-117">Gérez les jalons de lignes de contrat de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-118">Gérez les tâches de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-119">Gérez les catégories de transaction des dépenses dans Finance et synchronisez-les directement de Finance vers Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="73116-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="73116-120">Créer des estimations des heures de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-121">Créer des estimations des dépenses de projet dans Project Service Automation et synchronisez-les directement de Project Service Automation à Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="73116-122">Créez les heures de projet, les dépenses et les frais réels dans Project Service Automation, et créez des transactions de projet dans le journal d’intégration de Project Service Automation afin qu’elles soient publiées dans Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="73116-123">Synchronisation des données</span><span class="sxs-lookup"><span data-stu-id="73116-123">Data synchronization</span></span>

<span data-ttu-id="73116-124">L’illustration suivante montre comment les données sont synchronisées dans le cadre de l’intégration entre Project Service Automation et Finance.</span><span class="sxs-lookup"><span data-stu-id="73116-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="73116-125">Tous les modèles ne sont pas actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="73116-125">Not all templates are currently available.</span></span> <span data-ttu-id="73116-126">Les modèles seront publiés au fur et à mesure qu’ils seront terminés.</span><span class="sxs-lookup"><span data-stu-id="73116-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="73116-127">[![Intégration de Project Service Automation avec Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="73116-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="73116-128">Configuration requise pour Finance</span><span class="sxs-lookup"><span data-stu-id="73116-128">System requirements for Finance</span></span>

<span data-ttu-id="73116-129">Pour utiliser la solution d’intégration Project Service Automation vers Finance, vous devez installer Enterprise Edition 7.3 avec Platform update 12 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="73116-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="73116-130">Configuration système requise pour Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="73116-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="73116-131">Pour utiliser la solution d’intégration Project Service Automation vers Finance, vous devez installer les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="73116-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="73116-132">Dynamics 365 Project Service Automation version 9.0.0.0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="73116-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="73116-133">Solution Prospect en disponibilités pour Dynamics 365 Sales, version 1.14.0.0 (v14) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="73116-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="73116-134">Solution de Project Service Automation vers Finance pour Dynamics 365 Project Service Automation version 1.0.0.0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="73116-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="73116-135">Installer la solution d’intégration Project Service Automation vers Finance dans votre instance Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="73116-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="73116-136">Téléchargez la solution d’intégration Project Service Automation vers Finance à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) et suivez les instructions fournies avec la solution.</span><span class="sxs-lookup"><span data-stu-id="73116-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]