---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130215"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="cbeec-103">Réservations et Affectations</span><span class="sxs-lookup"><span data-stu-id="cbeec-103">Bookings vs assignments</span></span>

<span data-ttu-id="cbeec-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="cbeec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cbeec-105">Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet.</span><span class="sxs-lookup"><span data-stu-id="cbeec-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="cbeec-106">Les réservations fermes consomment la capacité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="cbeec-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="cbeec-107">Les réservations représentent des concepts organisationnels pour les équipes afin qu’elles comprennent comment les ressources seront engagées dans divers projets.</span><span class="sxs-lookup"><span data-stu-id="cbeec-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="cbeec-108">Dynamics 365 Project Operations considère les réservations comme un concept au niveau du projet.</span><span class="sxs-lookup"><span data-stu-id="cbeec-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="cbeec-109">Contrairement aux réservations, les attributions sont l’engagement de ressources aux tâches d’un projet dans la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="cbeec-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="cbeec-110">Les ressources peuvent être nommées ou génériques.</span><span class="sxs-lookup"><span data-stu-id="cbeec-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="cbeec-111">En règle générale, la somme des réservations d’une ressource sera égale à la somme des affectations de la ressource pour une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="cbeec-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="cbeec-112">Toutefois, Project Operations n’applique pas cette mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="cbeec-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="cbeec-113">La vue **Rapprochement** affiche au chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="cbeec-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
