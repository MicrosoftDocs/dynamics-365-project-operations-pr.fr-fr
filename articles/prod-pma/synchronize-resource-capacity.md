---
title: Synchroniser une capacité de ressource
description: Cette rubrique fournit des informations sur la synchronisation de la capacité d’une ressource entre les calendriers et les projets.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997508"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="cfcc8-103">Synchroniser une capacité de ressource</span><span class="sxs-lookup"><span data-stu-id="cfcc8-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfcc8-104">Les processus de synchronisation des ressources permettent de garantir que les informations du calendrier et du calendrier de base se retrouvent dans la planification des ressources du projet.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="cfcc8-105">Si le calendrier est modifié, les processus apportent les mises à jour nécessaires à la planification des ressources du projet.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="cfcc8-106">Les processus contribuent également à améliorer les performances, car les informations sur les ressources du calendrier sont synchronisées à l’avance.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="cfcc8-107">Par conséquent, les mises à jour des informations de planification des ressources se produisent plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="cfcc8-108">Nous vous recommandons de planifier les processus comme un lot au lieu d’un à la fois.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="cfcc8-109">Sinon, il y a un risque que quelqu’un oublie les dates incluses lors de la dernière synchronisation des informations.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="cfcc8-110">Si les dates inclusives ne sont pas utilisées, des intervalles peuvent se produire lors de la synchronisation des dates.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronisation du calendrier](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="cfcc8-112">Synchroniser les reports de la capacité d’une ressource</span><span class="sxs-lookup"><span data-stu-id="cfcc8-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="cfcc8-113">Le processus de synchronisation est conçu pour synchroniser toutes les informations du calendrier des ressources.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="cfcc8-114">Ces informations incluent des informations de calendrier de base sur les modifications apportées à la table de capacité du calendrier des ressources du projet.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="cfcc8-115">Si de nouvelles ressources sont ajoutées dans le projet, la synchronisation permet de garantir que les informations de calendrier mises à jour sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="cfcc8-116">Cette synchronisation peut être effectuée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="cfcc8-117">Nous vous recommandons d’utiliser un lot.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-117">We recommend that you use a batch.</span></span> <span data-ttu-id="cfcc8-118">Les options sont disponibles lors de la synchronisation des réservations de capacité.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="cfcc8-119">Sélectionnez **Gestion de projet et comptabilité** &gt; **Périodique** &gt; **Synchronisation de la capacité** &gt; **Synchroniser les cumuls de capacité des ressources**.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="cfcc8-120">Définissez les options dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="cfcc8-121">Option</span><span class="sxs-lookup"><span data-stu-id="cfcc8-121">Option</span></span>      | <span data-ttu-id="cfcc8-122">Description</span><span class="sxs-lookup"><span data-stu-id="cfcc8-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="cfcc8-123">Code de période</span><span class="sxs-lookup"><span data-stu-id="cfcc8-123">Period code</span></span> | <span data-ttu-id="cfcc8-124">Sélectionnez éventuellement le code d’intervalle de dates du grand livre général pour définir les dates de début et de fin du processus de synchronisation pour les cumuls de capacité de ressources.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="cfcc8-125">Date de début</span><span class="sxs-lookup"><span data-stu-id="cfcc8-125">Start date</span></span>  | <span data-ttu-id="cfcc8-126">Entrez la date de début du processus de synchronisation pour les cumuls de capacité des ressources.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="cfcc8-127">Date de fin</span><span class="sxs-lookup"><span data-stu-id="cfcc8-127">End date</span></span>    | <span data-ttu-id="cfcc8-128">Entrez la date de fin du processus de synchronisation pour les cumuls de capacité des ressources.</span><span class="sxs-lookup"><span data-stu-id="cfcc8-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="cfcc8-129">[![Processus de la synchronisation](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="cfcc8-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]