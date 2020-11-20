---
title: Mettre à jour Estimé à Achèvement
description: Cette rubrique fournit des informations sur la mise à jour de la projection d’effort sur un projet.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127200"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="afb55-103">Mettre à jour Estimé à Achèvement</span><span class="sxs-lookup"><span data-stu-id="afb55-103">Update estimate at completion</span></span>

<span data-ttu-id="afb55-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="afb55-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="afb55-105">Il arrive souvent qu’un chef de projet modifie les estimations initiales d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="afb55-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="afb55-106">Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l’état actuel de projet.</span><span class="sxs-lookup"><span data-stu-id="afb55-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="afb55-107">Toutefois, il n’est pas recommandé que les chefs de projet modifient les numéros de référence, car la ligne de référence du projet représente la source fiable établie pour les estimations de planning et de coût du projet convenue par toutes les parties prenantes au projet.</span><span class="sxs-lookup"><span data-stu-id="afb55-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="afb55-108">Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peut utiliser un chef de projet :</span><span class="sxs-lookup"><span data-stu-id="afb55-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="afb55-109">Remplacez l’Estimation avant achèvement par défaut par une nouvelle évaluation des efforts restants réels pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="afb55-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="afb55-110">Remplacez le pourcentage de progression par défaut par une nouvelle évaluation de la progression réelle pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="afb55-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="afb55-111">Chacune de ces méthode entraîne un nouveau calcul de l’Estimation avant achèvement, de l’EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l’écart d’efforts escomptés pour une tâche.</span><span class="sxs-lookup"><span data-stu-id="afb55-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="afb55-112">L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.</span><span class="sxs-lookup"><span data-stu-id="afb55-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
