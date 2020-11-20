---
title: Gérer des devis de projet
description: Cette rubrique fournit des informations sur les devis de projet.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177823"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="19f75-103">Gérer des devis de projet</span><span class="sxs-lookup"><span data-stu-id="19f75-103">Manage project quotes</span></span>

<span data-ttu-id="19f75-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="19f75-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="19f75-105">Dans Dynamics 365 Project Operations, les devis de projet sont conçus pour aider à créer des propositions pour le travail de projet.</span><span class="sxs-lookup"><span data-stu-id="19f75-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="19f75-106">La structure d’un devis de projet dans Project Operations est modelée pour les propositions de projet avec les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="19f75-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="19f75-107">Lignes de devis qui identifient les composants discrets du travail qui seront présentés comme des composants de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="19f75-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="19f75-108">Détails de la ligne de devis qui identifient et estiment le travail pour chaque composant de haut niveau ou ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="19f75-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="19f75-109">La planification ou les estimations de date et les aspects financiers du travail sont liés à cette ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="19f75-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="19f75-110">Des modèles contractuels et des composants facturables sont configurés pour chaque ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="19f75-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="19f75-111">Cette configuration permet d’estimer la répartition des revenus, des dépenses et de la rentabilité pour chaque ligne de devis et le devis global.</span><span class="sxs-lookup"><span data-stu-id="19f75-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="19f75-112">Afficher tous les devis basés sur un projet</span><span class="sxs-lookup"><span data-stu-id="19f75-112">View all project-based quotes</span></span>

<span data-ttu-id="19f75-113">Une liste de tous les devis de projet peut être consultée sur la page de liste **Devis**.</span><span class="sxs-lookup"><span data-stu-id="19f75-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="19f75-114">Accédez à **Ventes** > **Devis**.</span><span class="sxs-lookup"><span data-stu-id="19f75-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="19f75-115">Une liste de tous vos devis de projet dans le système s’affiche.</span><span class="sxs-lookup"><span data-stu-id="19f75-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="19f75-116">Utilisez le **Commutateur de vue** pour sélectionner d’autres vues filtrées de devis.</span><span class="sxs-lookup"><span data-stu-id="19f75-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="19f75-117">À l’aide de critères de filtre personnalisés, vous pouvez configurer vos propres vues et options de navigation.</span><span class="sxs-lookup"><span data-stu-id="19f75-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="19f75-118">Les devis peuvent être créés ou supprimés à partir de cette page de liste ou des pages de détails.</span><span class="sxs-lookup"><span data-stu-id="19f75-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
