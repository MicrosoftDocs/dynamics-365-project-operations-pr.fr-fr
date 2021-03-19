---
title: Vue d’ensemble de l’Assistant Planifier
description: Cette rubrique fournit des informations sur l’utilisation de l’Assistant Planifier pour réserver des ressources.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279225"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="2129d-103">Vue d’ensemble de l’Assistant Planifier</span><span class="sxs-lookup"><span data-stu-id="2129d-103">Schedule assistant overview</span></span>

<span data-ttu-id="2129d-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="2129d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2129d-105">L’Assistant Planifier permet de réserver des ressources en fonction des besoins définis par le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="2129d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="2129d-106">L’Assistant Planifier s’appuie sur les paramètres fournis dans les besoins en ressources pour trouver la ressource.</span><span class="sxs-lookup"><span data-stu-id="2129d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="2129d-107">L’Assistant Planifier recommande des ressources qui correspondent aux exigences pertinentes, telles que les fenêtres horaires ou les compétences requises.</span><span class="sxs-lookup"><span data-stu-id="2129d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="2129d-108">Une fois les ressources appropriées identifiées, le gestionnaire de ressources ou de projet peut réserver la ressource au travail.</span><span class="sxs-lookup"><span data-stu-id="2129d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2129d-109">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2129d-109">Prerequisites</span></span>

<span data-ttu-id="2129d-110">L’Assistant Planifier fait partie de la solution Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="2129d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="2129d-111">Cette solution est incluse et installée avec Dynamics 365 Project Operations, Dynamics 365 Field Service et Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="2129d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="2129d-112">Besoin de mise en correspondance et ressources</span><span class="sxs-lookup"><span data-stu-id="2129d-112">Matching requirements and resources</span></span>

<span data-ttu-id="2129d-113">Un besoin en ressources généré est basé sur des détails tels que :</span><span class="sxs-lookup"><span data-stu-id="2129d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="2129d-114">Caractéristiques</span><span class="sxs-lookup"><span data-stu-id="2129d-114">Characteristics</span></span>
-   <span data-ttu-id="2129d-115">Rôles</span><span class="sxs-lookup"><span data-stu-id="2129d-115">Roles</span></span>
-   <span data-ttu-id="2129d-116">Divisions</span><span class="sxs-lookup"><span data-stu-id="2129d-116">Business units</span></span>
-   <span data-ttu-id="2129d-117">Préférences de ressource</span><span class="sxs-lookup"><span data-stu-id="2129d-117">Resource preferences</span></span>
-   <span data-ttu-id="2129d-118">Contours d’effort</span><span class="sxs-lookup"><span data-stu-id="2129d-118">Effort contours</span></span>
-   <span data-ttu-id="2129d-119">Fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="2129d-119">Time zone</span></span>

<span data-ttu-id="2129d-120">L’Assistant Planifier utilise ces détails pour filtrer les ressources.</span><span class="sxs-lookup"><span data-stu-id="2129d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="2129d-121">Lancer l’Assistant de planification</span><span class="sxs-lookup"><span data-stu-id="2129d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="2129d-122">L’Assistant Planifier est lancé de deux manières.</span><span class="sxs-lookup"><span data-stu-id="2129d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="2129d-123">Si vous utilisez le mode hybride, dans la grille des membres de l’équipe, vous pouvez sélectionner n’importe quel membre de l’équipe dont les besoins en ressources ne sont pas satisfaits, puis sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="2129d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="2129d-124">Si vous utilisez le mode central, le gestionnaire de ressources recherche et sélectionne la ressource.</span><span class="sxs-lookup"><span data-stu-id="2129d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="2129d-125">Filtres de l’Assistant Planifier</span><span class="sxs-lookup"><span data-stu-id="2129d-125">Schedule assistant filters</span></span>

<span data-ttu-id="2129d-126">Une fois l’Assistant Planifier exécuté, les détails des besoins en ressources sont affichés sous forme de valeurs filtrées dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="2129d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="2129d-127">Le gestionnaire de ressources ou le chef de projet peut affiner les résultats en ajustant les filtres pour répondre aux besoins de planification.</span><span class="sxs-lookup"><span data-stu-id="2129d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="2129d-128">Le volet de filtre affiche les options liées au travail, notamment :</span><span class="sxs-lookup"><span data-stu-id="2129d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="2129d-129">Début et fin du travail</span><span class="sxs-lookup"><span data-stu-id="2129d-129">Work start and end</span></span>
-   <span data-ttu-id="2129d-130">Caractéristiques</span><span class="sxs-lookup"><span data-stu-id="2129d-130">Characteristics</span></span>
-   <span data-ttu-id="2129d-131">Rôles</span><span class="sxs-lookup"><span data-stu-id="2129d-131">Roles</span></span>
-   <span data-ttu-id="2129d-132">Unités d’organisation</span><span class="sxs-lookup"><span data-stu-id="2129d-132">Organizational units</span></span>
-   <span data-ttu-id="2129d-133">Société d’allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="2129d-133">Resourcing company</span></span>
-   <span data-ttu-id="2129d-134">Types de ressources</span><span class="sxs-lookup"><span data-stu-id="2129d-134">Resource types</span></span>
-   <span data-ttu-id="2129d-135">Ressources privilégiées</span><span class="sxs-lookup"><span data-stu-id="2129d-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]