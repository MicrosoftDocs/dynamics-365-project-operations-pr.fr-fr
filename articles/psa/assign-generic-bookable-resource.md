---
title: Attribuez des ressources génériques pouvant être réservées à une tâche et à une équipe de projet
description: Cette rubrique fournit des informations sur la réservation de ressources génériques dans les tâches et les équipes de projet.
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127065"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="4b837-103">Attribuez des ressources génériques pouvant être réservées à une tâche et générez des besoins en ressources</span><span class="sxs-lookup"><span data-stu-id="4b837-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4b837-104">Outre la réservation et l’attribution des ressources nommées ou réelles à votre projet, vous pouvez attribuer des ressources génériques aux tâches de projet.</span><span class="sxs-lookup"><span data-stu-id="4b837-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="4b837-105">Ces ressources peuvent servir d’espaces réservés aux ressources nommées jusqu’à ce que vous soyez prêt à doter votre projet en personnel avec des ressources nommées.</span><span class="sxs-lookup"><span data-stu-id="4b837-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="4b837-106">Dans Project Service Automation (PSA), ouvrez la page **Projet** et sur l’onglet **Planification**, entrez le nom de la position de la ressources générique dans la cellule **Ressource** de la planification.</span><span class="sxs-lookup"><span data-stu-id="4b837-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="4b837-107">Sinon, cliquez sur l’icône **Ressource** dans la cellule pour ouvrir le sélecteur de ressources, puis entrez le nom de la ressource générique à créer.</span><span class="sxs-lookup"><span data-stu-id="4b837-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Création et affectation d’un membre de l’équipe générique](media/RM-how-to-9.png)

<span data-ttu-id="4b837-109">Cela ouvre le volet **Création rapide : Membre de l’équipe du projet**.</span><span class="sxs-lookup"><span data-stu-id="4b837-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="4b837-110">Entrez le rôle et l’unité d’organisation du membre de l’équipe de ressources génériques, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4b837-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Création rapide du membre de l’équipe générique](media/RM-how-to-10.png)

3. <span data-ttu-id="4b837-112">Après avoir créé le membre de l’équipe de ressources génériques, une tâche lui est attribuée.</span><span class="sxs-lookup"><span data-stu-id="4b837-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="4b837-113">Vous pouvez continuer d’attribuer cette ressource générique à d’autres tâches dans la planification de tâche.</span><span class="sxs-lookup"><span data-stu-id="4b837-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Attribution d’un membre de l’équipe générique existant aux tâches](media/RM-how-to-11.png)

4. <span data-ttu-id="4b837-115">Après avoir attribué la ressource générique, vous pouvez générer un besoin en ressources et le satisfaire en réservant ou en transmettant directement une demande de ressource à un gestionnaire des ressources.</span><span class="sxs-lookup"><span data-stu-id="4b837-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Génération d’un besoin pour un membre de l’équipe générique](media/RM-how-to-12.png)

<span data-ttu-id="4b837-117">Dans la grille des membre de l’équipe, en plus de pouvoir utiliser le sélecteur de ressources comme mentionné précédemment, vous pouvez ajouter les ressources génériques directement.</span><span class="sxs-lookup"><span data-stu-id="4b837-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="4b837-118">Les ressources sont ajoutées avec un besoin en ressources basé sur les dates de début/fin et la méthode d’allocation spécifiée dans le volet **Création rapide : Membre de l’équipe du projet**.</span><span class="sxs-lookup"><span data-stu-id="4b837-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="4b837-119">Vous pouvez voir une différence si vous ajoutez le membre de l’équipe générique directement, et que vous attribuez ensuite plus de tâches à la ressource générique qu’elle n’en dispose.</span><span class="sxs-lookup"><span data-stu-id="4b837-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="4b837-120">Cliquez sur **Générer un besoin** pour régénérer le besoin afin d’équilibrer les heures requises par rapport aux attributions.</span><span class="sxs-lookup"><span data-stu-id="4b837-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="4b837-121">Vous pouvez également cliquer sur le lien **Besoin en ressources** de la grille de l’équipe pour ouvrir le besoin et ajouter des compétences, des ressources préférées, etc..</span><span class="sxs-lookup"><span data-stu-id="4b837-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Besoin en ressource](media/RM-how-to-13.png)

