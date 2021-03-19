---
title: Réserver des ressources nommées à partir des besoins en ressources.
description: Cette rubrique fournit des informations sur la réservation des ressources nommées pour un besoin en ressources générique.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291031"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="7c124-103">Réserver des ressources nommées à partir des besoins en ressources.</span><span class="sxs-lookup"><span data-stu-id="7c124-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7c124-104">Vous pouvez réserver une ressource nommée pour remplacer une ressource génériques qui a un besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="7c124-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="7c124-105">Dans Project Service Automation (PSA), dans la page **Projets**, cliquez sur l’onglet **Équipe**.</span><span class="sxs-lookup"><span data-stu-id="7c124-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="7c124-106">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="7c124-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="7c124-107">Ou, ouvrez le besoin en ressources puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="7c124-107">Or, open the resource requirement and then click **Book**.</span></span>


![Réservation d’un membre de l’équipe générique](media/RM-how-to-14.png)


3. <span data-ttu-id="7c124-109">Dans la page **Assistant Planifier**, sélectionnez une ressource nommée à réserver sur votre équipe du projet, puis cliquez sur **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="7c124-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Réservation d’un membre de l’équipe générique en utilisant l’Assistant Planifier](media/RM-how-to-15.png)

<span data-ttu-id="7c124-111">Une fois la réservation effectuée et satisfaite par une ressource nommée, la ressource générique est remplacée par la ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="7c124-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membre de l’équipe nommé remplaçant un membre de l’équipe générique](media/RM-how-to-16.png)

<span data-ttu-id="7c124-113">Les attributions sur la planification sont également mises à jour avec la ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="7c124-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membre de l’équipe nommé affecté aux tâches du projet](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="7c124-115">Exécuter une ressource générique avec plusieurs ressources nommées</span><span class="sxs-lookup"><span data-stu-id="7c124-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="7c124-116">La satisfaction d’un besoin en ressource générique avec plusieurs ressources nommées est similaire à l’attribution d’une ressource nommée unique.</span><span class="sxs-lookup"><span data-stu-id="7c124-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="7c124-117">Par exemple, il existe une tâche avec une durée de cinq jours et de 120 heures d’effort.</span><span class="sxs-lookup"><span data-stu-id="7c124-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="7c124-118">Cette tâche ne peut pas être effectuée que par une ressource qui fonctionne un jour de huit heures classique sur une semaine de cinq jours.</span><span class="sxs-lookup"><span data-stu-id="7c124-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Une tâche nécessite 120 heures d’effort sur de cinq jours](media/RM-how-to-21.png)

<span data-ttu-id="7c124-120">Le besoin est de 120 heures d’ingénierie robotique sur de cinq jours, soit 24 heures par jour.</span><span class="sxs-lookup"><span data-stu-id="7c124-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Besoin par jour](media/RM-how-to-22.png)

<span data-ttu-id="7c124-122">Il s’agit d’un exemple où plusieurs ressources nommées sont nécessaires pour répondre à une demande de ressource générique.</span><span class="sxs-lookup"><span data-stu-id="7c124-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="7c124-123">Vous devez réserver plusieurs ressources pour satisfaire le besoin.</span><span class="sxs-lookup"><span data-stu-id="7c124-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Réservation de plusieurs ressources pour satisfaire le besoin](media/RM-how-to-23.png)

<span data-ttu-id="7c124-125">La principale différence dans ce scénario est que la ressource générique reste dans l’équipe attribuée à la tâche, et les membres de l’équipe de ressources nommés réservés ne sont pas attribués dans le cadre du poste.</span><span class="sxs-lookup"><span data-stu-id="7c124-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="7c124-126">Le chef de projet peut affecter le travail si besoin aux ressources nommées.</span><span class="sxs-lookup"><span data-stu-id="7c124-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="7c124-127">La vue **Rapprochement** peut aider un chef de projet à répartir les réservations entre plusieurs ressources à des affectations de tâche.</span><span class="sxs-lookup"><span data-stu-id="7c124-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="7c124-128">Cela n’est pas effectué automatiquement, car dans les scénarios plus compliqués que l’exemple simple ci-dessus, comme celui où un groupe de tâches composent le besoin, la façon dont le chef de projet souhaite les affecter, doit être prise en compte par le système.</span><span class="sxs-lookup"><span data-stu-id="7c124-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="7c124-129">Comme le système ne peut pas comprendre l’intention, il y a des chances que les hypothèses soient différentes de celles prévues et un résultat incorrect ou imprévisible se produise.</span><span class="sxs-lookup"><span data-stu-id="7c124-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="7c124-130">Le résultat prévisible est que la ressource générique reste affectée jusqu’à ce que le chef de projet crée délibérément des attributions à l’aide de la vue **Rapprochement**.</span><span class="sxs-lookup"><span data-stu-id="7c124-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]