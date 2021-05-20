---
title: Vue d’ensemble des modes de gestion des ressources
description: Cette rubrique fournit des informations sur la fonctionnalité de gestion des ressources dans Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949946"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="fc094-103">Vue d’ensemble des modes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-103">Resource management modes overview</span></span>

<span data-ttu-id="fc094-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="fc094-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fc094-105">Dynamics 365 Project Operations prend en charge deux modes pour vous permettre d’exécuter le flux de réservations global.</span><span class="sxs-lookup"><span data-stu-id="fc094-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="fc094-106">Le mode de gestion est défini comme un paramètre de projet et peut être modifié si les besoins de votre entreprise changent.</span><span class="sxs-lookup"><span data-stu-id="fc094-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="fc094-107">Mode central</span><span class="sxs-lookup"><span data-stu-id="fc094-107">Central mode</span></span>
<span data-ttu-id="fc094-108">Pour les organisations qui centralisent l’affectation des ressources aux projets, le mode central permet de s’assurer que les chefs de projet peuvent définir les besoins en ressources au niveau du projet.</span><span class="sxs-lookup"><span data-stu-id="fc094-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="fc094-109">La satisfaction des besoins en ressources est déléguée à un gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="fc094-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="fc094-110">Les chefs de projet peuvent accepter ou refuser les ressources proposées par le gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="fc094-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mode central](./media/resource-management-central.png)

<span data-ttu-id="fc094-112">Pour gérer les ressources avec le mode central, voir :</span><span class="sxs-lookup"><span data-stu-id="fc094-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="fc094-113">Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="fc094-114">Réserver des ressources nommées à partir des besoins en ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="fc094-115">Envoyer une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="fc094-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="fc094-116">Répondre à une demande de ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="fc094-117">Accepter ou rejeter une ressource de projet proposée à partir d’une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="fc094-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="fc094-118">Modèle hybride</span><span class="sxs-lookup"><span data-stu-id="fc094-118">Hybrid mode</span></span>
<span data-ttu-id="fc094-119">Pour les organisations qui ont besoin de flexibilité dans l’allocation des ressources, le mode hybride permet aux chefs de projet et aux gestionnaires de ressources de réserver des ressources.</span><span class="sxs-lookup"><span data-stu-id="fc094-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mode hybride](./media/resource-management-hybrid.png)

<span data-ttu-id="fc094-121">En plus du processus du mode central pris en charge, consultez les rubriques suivantes pour gérer tous les autres flux de réservation pris en charge en mode hybride :</span><span class="sxs-lookup"><span data-stu-id="fc094-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="fc094-122">Réserver une ressource directement sur un projet :</span><span class="sxs-lookup"><span data-stu-id="fc094-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="fc094-123">Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches</span><span class="sxs-lookup"><span data-stu-id="fc094-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="fc094-124">Réserver une ressource à partir d’un besoins en ressource :</span><span class="sxs-lookup"><span data-stu-id="fc094-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="fc094-125">Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="fc094-126">Réserver des ressources nommées à partir des besoins en ressources</span><span class="sxs-lookup"><span data-stu-id="fc094-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]