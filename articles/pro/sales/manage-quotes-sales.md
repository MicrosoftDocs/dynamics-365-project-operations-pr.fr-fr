---
title: Gérer des devis de projet
description: Cette rubrique fournit des informations sur les devis de projet.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8e0b20d4780a14edc3c242e261e22d4905f783a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994808"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="212fa-103">Gérer des devis de projet</span><span class="sxs-lookup"><span data-stu-id="212fa-103">Manage project quotes</span></span>

<span data-ttu-id="212fa-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="212fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="212fa-105">Dans Dynamics 365 Project Operations, les devis de projet sont conçus pour aider à créer des propositions de travail de projet.</span><span class="sxs-lookup"><span data-stu-id="212fa-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="212fa-106">La structure d’un devis de projet dans Project Operations est conçue pour les propositions de projet avec les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="212fa-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="212fa-107">Des lignes de devis qui identifient les composants discrets du travail, qui seront présentés comme des composants de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="212fa-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="212fa-108">Des détails de ligne de devis qui identifient et estiment le travail pour chaque composant de haut niveau ou ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="212fa-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="212fa-109">Un programme ou des estimations de date et les aspects financiers du travail sont liés à cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="212fa-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="212fa-110">Des modèles de sous-traitance et des composants facturables sont configurés pour chaque ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="212fa-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="212fa-111">Cette configuration permet d’estimer la répartition des revenus, des dépenses et de la rentabilité pour chaque ligne de devis et le devis global.</span><span class="sxs-lookup"><span data-stu-id="212fa-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="212fa-112">Afficher tous les devis basés sur un projet</span><span class="sxs-lookup"><span data-stu-id="212fa-112">View all project-based quotes</span></span>

<span data-ttu-id="212fa-113">Une liste de tous les devis de projet peut être consultée sur la page de liste **Devis**.</span><span class="sxs-lookup"><span data-stu-id="212fa-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="212fa-114">Accédez à **Ventes** > **Devis**.</span><span class="sxs-lookup"><span data-stu-id="212fa-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="212fa-115">Une liste de tous vos devis de projet dans le système s’affiche.</span><span class="sxs-lookup"><span data-stu-id="212fa-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="212fa-116">Utilisez le **Commutateur de vue** pour sélectionner d’autres vues filtrées de devis.</span><span class="sxs-lookup"><span data-stu-id="212fa-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="212fa-117">À l’aide de critères de filtre personnalisés, vous pouvez configurer vos propres vues et options de navigation.</span><span class="sxs-lookup"><span data-stu-id="212fa-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="212fa-118">Les devis peuvent être créés ou supprimés à partir de cette page de liste ou des pages de détails.</span><span class="sxs-lookup"><span data-stu-id="212fa-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]