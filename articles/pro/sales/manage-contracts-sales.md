---
title: Gérer les contrats de projets
description: Cette rubrique fournit des informations sur l’affichage de contrats basés sur un projet.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003088"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="8c263-103">Gérer les contrats de projets</span><span class="sxs-lookup"><span data-stu-id="8c263-103">Manage project contracts</span></span>

<span data-ttu-id="8c263-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="8c263-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c263-105">Les contrats de projet dans Dynamics 365 Project Operations capturent et gèrent les engagements contractuels et les détails de facturation d’un projet.</span><span class="sxs-lookup"><span data-stu-id="8c263-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="8c263-106">La structure d’un contrat de projet dans Project Operations est adaptée au travail basé sur un projet avec les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="8c263-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="8c263-107">Des lignes de contrat qui identifient les composants discrets du travail, qui seront présentés comme des composants de haut niveau sur une facture de projet.</span><span class="sxs-lookup"><span data-stu-id="8c263-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="8c263-108">Des détails de ligne de contrat qui identifient et estiment le travail pour chaque composant de haut niveau ou ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="8c263-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="8c263-109">L’estimation comprend la planification et les aspects financiers du travail lié à la ligne du contrat.</span><span class="sxs-lookup"><span data-stu-id="8c263-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="8c263-110">Des modèles de contrat et des composants facturables sont configurés pour chaque ligne de contrat qui contient les modalités de facturation pour chaque ligne de contrat et le contrat d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="8c263-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="8c263-111">Afficher tous les contrats basés sur les projets</span><span class="sxs-lookup"><span data-stu-id="8c263-111">View all project-based contracts</span></span>

<span data-ttu-id="8c263-112">Une liste de tous les contrats de projet peut être consultée sur la page de liste **Contrats**.</span><span class="sxs-lookup"><span data-stu-id="8c263-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="8c263-113">Accédez à **Ventes** > **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="8c263-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="8c263-114">Une liste de tous vos contrats de projet dans le système s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8c263-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="8c263-115">Sélectionnez le **Commutateur de vue** (la flèche déroulante à côté du nom de la vue) pour sélectionner d’autres vues filtrées.</span><span class="sxs-lookup"><span data-stu-id="8c263-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="8c263-116">Vous pouvez créer vos propres vues à l’aide de critères de filtre personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8c263-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="8c263-117">Les contrats peuvent être créés ou supprimés à partir de cette page de liste ou des pages de détails.</span><span class="sxs-lookup"><span data-stu-id="8c263-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]