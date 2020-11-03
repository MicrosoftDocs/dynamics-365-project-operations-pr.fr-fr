---
title: Répondre aux besoins en ressources génériques
description: Cette rubrique fournit des informations sur le mode de réservation des ressources nommées pour un besoin en ressources générique.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075685"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="c1c96-103">Répondre aux besoins en ressources génériques</span><span class="sxs-lookup"><span data-stu-id="c1c96-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="c1c96-104">_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="c1c96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c1c96-105">Vous pouvez réserver une ressource nommée pour remplacer une ressource génériques qui a un besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="c1c96-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c1c96-106">Sur la page **Projets** , sélectionnez l'onglet **Équipe**.</span><span class="sxs-lookup"><span data-stu-id="c1c96-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="c1c96-107">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="c1c96-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="c1c96-108">Ou, ouvrez le besoin en ressources puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="c1c96-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="c1c96-109">Dans la page **Assistant Planifier** , sélectionnez une ressource nommée à réserver sur votre équipe du projet, puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="c1c96-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="c1c96-110">Une fois la réservation effectuée et satisfaite par une ressource nommée, la ressource générique est remplacée par la ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="c1c96-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="c1c96-111">Les attributions sur la planification sont également mises à jour avec la ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="c1c96-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c1c96-112">Exécuter une ressource générique avec plusieurs ressources nommées</span><span class="sxs-lookup"><span data-stu-id="c1c96-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c1c96-113">La satisfaction d'un besoin en ressource générique avec plusieurs ressources nommées est similaire à l'attribution d'une ressource nommée unique.</span><span class="sxs-lookup"><span data-stu-id="c1c96-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c1c96-114">Par exemple, il existe une tâche avec une durée de cinq jours et de 120 heures d'effort.</span><span class="sxs-lookup"><span data-stu-id="c1c96-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c1c96-115">Cette tâche ne peut pas être effectuée que par une ressource qui fonctionne un jour de huit heures classique sur une semaine de cinq jours.</span><span class="sxs-lookup"><span data-stu-id="c1c96-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="c1c96-116">Le besoin est de 120 heures d'ingénierie robotique sur de cinq jours, soit 24 heures par jour.</span><span class="sxs-lookup"><span data-stu-id="c1c96-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="c1c96-117">Il s'agit d'un exemple où plusieurs ressources nommées sont nécessaires pour répondre à une demande de ressource générique.</span><span class="sxs-lookup"><span data-stu-id="c1c96-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c1c96-118">Vous devez réserver plusieurs ressources pour satisfaire le besoin.</span><span class="sxs-lookup"><span data-stu-id="c1c96-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="c1c96-119">La principale différence dans ce scénario est que la ressource générique reste dans l'équipe attribuée à la tâche, et les membres de l'équipe de ressources nommés réservés ne sont pas attribués dans le cadre du poste.</span><span class="sxs-lookup"><span data-stu-id="c1c96-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c1c96-120">Le chef de projet peut affecter le travail si besoin aux ressources nommées.</span><span class="sxs-lookup"><span data-stu-id="c1c96-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c1c96-121">La vue **Rapprochement** peut aider un chef de projet à répartir les réservations entre plusieurs ressources à des affectations de tâche.</span><span class="sxs-lookup"><span data-stu-id="c1c96-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c1c96-122">Cela n'est pas effectué automatiquement, car dans les scénarios plus compliqués que l'exemple simple ci-dessus, comme celui où un groupe de tâches composent le besoin, la façon dont le chef de projet souhaite les affecter, doit être prise en compte par le système.</span><span class="sxs-lookup"><span data-stu-id="c1c96-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c1c96-123">Comme le système ne peut pas comprendre l'intention, les hypothèses seront sans doute différentes de celles prévues et un résultat incorrect ou imprévisible se produira.</span><span class="sxs-lookup"><span data-stu-id="c1c96-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="c1c96-124">Le résultat prévisible est que la ressource générique reste affectée jusqu'à ce que le chef de projet crée délibérément des attributions à l'aide de la vue **Rapprochement**.</span><span class="sxs-lookup"><span data-stu-id="c1c96-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


