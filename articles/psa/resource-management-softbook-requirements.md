---
title: Besoins en réservations temporaires
description: Cette rubrique fournit des informations sur la façon de réserver provisoirement des besoins.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124095"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="65d11-103">Besoins en réservations temporaires</span><span class="sxs-lookup"><span data-stu-id="65d11-103">Soft-book requirements</span></span>

<span data-ttu-id="65d11-104">Un besoin en ressources peut être réservé de manière ferme.</span><span class="sxs-lookup"><span data-stu-id="65d11-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="65d11-105">Une réservation ferme crée une proposition qui consomme la capacité d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="65d11-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="65d11-106">La proposition est alors renvoyée au demandeur l’approbation.</span><span class="sxs-lookup"><span data-stu-id="65d11-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="65d11-107">Une réservation provisoire ajoute temporairement une ressource à une équipe du projet et a un statut différent sur le Tableau de planification, mais elle ne consomme pas la capacité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="65d11-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="65d11-108">Pour réserver provisoirement une ressource à partir du Tableau de planification, définissez le champ **Statut de la réservation** sur **Temporaire**.</span><span class="sxs-lookup"><span data-stu-id="65d11-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Statut de réservation défini sur Temporaire](media/Resource-Management-image77.png)

<span data-ttu-id="65d11-110">Lorsque l’onglet **Équipe** se trouve dans la vue **Membres de l’équipe nommés**, la ressource apparaît dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="65d11-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="65d11-111">Les heures réservées temporairement sont stockées dans la colonne **Heures réservées temporairement**.</span><span class="sxs-lookup"><span data-stu-id="65d11-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Heures réservées temporairement dans la vue Membres de l’équipe nommés](media/Resource-Management-image78.png)

<span data-ttu-id="65d11-113">Les membres de l’équipe réservés temporairement peuvent être attribués à des tâches.</span><span class="sxs-lookup"><span data-stu-id="65d11-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membre de l’équipe réservé temporairement attribué à une tâche](media/Resource-Management-image79.png)

<span data-ttu-id="65d11-115">Dans l’onglet **Rapprochement**, aucune réservation n’est affichée pour une ressource réservée temporairement, car l’onglet **Rapprochement** considère uniquement les réservations fermes.</span><span class="sxs-lookup"><span data-stu-id="65d11-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Ressource réservée temporairement sans réservation sous l’onglet Rapprochement](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="65d11-117">Vous ne pouvez pas réserver temporairement une ressource d’un besoin généré par un membre de l’équipe générique.</span><span class="sxs-lookup"><span data-stu-id="65d11-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="65d11-118">Dans le Tableau de planification, des couleurs différentes sont utilisées pour les réservations temporaires d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="65d11-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Réservations temporaires sur le Tableau de planification](media/Resource-Management-image81.png)

<span data-ttu-id="65d11-120">Pour convertir une réservation temporaire en une réservation ferme, dans le Tableau de planification, cliquez avec le bouton droit sur la réservation temporaire, puis sélectionnez **Modifier le statut** \> **Réservation ferme** \> **Ferme**.</span><span class="sxs-lookup"><span data-stu-id="65d11-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Modification du statut de réservation sur Ferme](media/Resource-Management-image82.png)

<span data-ttu-id="65d11-122">La réservation est modifiée, et le statut change sur le Tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="65d11-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="65d11-123">Étant donné que le statut de réservation est désormais **Ferme**, la ressource apparaît comme réservée, et sa capacité et sa disponibilité sont ajustées.</span><span class="sxs-lookup"><span data-stu-id="65d11-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="65d11-124">Vous pouvez utiliser la même méthode pour annuler une réservation ferme ou une réservation temporaire sur le Tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="65d11-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="65d11-125">Pour convertir une ressource réservée temporairement en réservation ferme, sur l’onglet **Équipe** du projet, sélectionnez la ressource, puis sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="65d11-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Commande Confirmer](media/Resource-Management-image83.png)
