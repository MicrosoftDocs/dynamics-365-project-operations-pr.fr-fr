---
title: Réservations et Affectations
description: Cette rubrique fournit des informations sur les différences entre les réservations de ressources et les affectations de ressources.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279900"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="ac25f-103">Réservations et Affectations</span><span class="sxs-lookup"><span data-stu-id="ac25f-103">Bookings vs assignments</span></span>

<span data-ttu-id="ac25f-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="ac25f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac25f-105">Les réservations sont l’allocation ferme ou provisoire des ressources sur un projet.</span><span class="sxs-lookup"><span data-stu-id="ac25f-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ac25f-106">Les réservations fixes consomment la capacité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="ac25f-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ac25f-107">Les réservations représentent des concepts organisationnels pour les équipes, afin qu’elles puissent comprendre comment les ressources seront impliquées dans divers projets.</span><span class="sxs-lookup"><span data-stu-id="ac25f-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="ac25f-108">Dynamics 365 Project Operations prend en compte les réservations en tant que concept au niveau du projet.</span><span class="sxs-lookup"><span data-stu-id="ac25f-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="ac25f-109">Contrairement aux réservations, les affectations désignent l’engagement de ressources sur des tâches de projet dans le calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="ac25f-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ac25f-110">Les ressources peuvent être nommées ou génériques.</span><span class="sxs-lookup"><span data-stu-id="ac25f-110">The resources can be named or generic.</span></span>  <span data-ttu-id="ac25f-111">Lorsqu'un besoin en ressources est dérivé des affectations de tâches de projet, Project Operations utilise les contours d'effort de l'affectation de ressources pour créer les contours des détails des besoins en ressources.</span><span class="sxs-lookup"><span data-stu-id="ac25f-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="ac25f-112">Cependant, une référence aux affectations de ressources n'est pas conservée.</span><span class="sxs-lookup"><span data-stu-id="ac25f-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="ac25f-113">Les mises à jour des réservations dérivées des besoins en ressources ne mettent pas à jour les affectations de ressources.</span><span class="sxs-lookup"><span data-stu-id="ac25f-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="ac25f-114">En règle générale, la somme des réservations pour une ressource est égale à la somme des affectations de la ressource sur une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="ac25f-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="ac25f-115">Toutefois, Project Operations n’applique pas cette mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="ac25f-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="ac25f-116">La vue **Rapprochement** affiche au chef de projet des emplacements où les réservations et les affectations d’une ressource ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="ac25f-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]