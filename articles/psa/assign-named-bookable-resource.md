---
title: Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches
description: Cette rubrique fournit des informations sur le mode de réservation de ressources nommées dans les équipes de projet et leur attribution de tâches.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130170"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="7f938-103">Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches</span><span class="sxs-lookup"><span data-stu-id="7f938-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7f938-104">Vous pouvez ajouter une ressource nommée à votre équipe de projet en les réservant directement dans l’équipe.</span><span class="sxs-lookup"><span data-stu-id="7f938-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="7f938-105">Pour cela, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7f938-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="7f938-106">Dans Project Service Automation, accédez à **Projets**, puis sélectionnez pour ouvrir le projet que réservez.</span><span class="sxs-lookup"><span data-stu-id="7f938-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="7f938-107">Dans la page **Projet**, dans l’onglet **Équipe**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7f938-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Ajout d’un membre de l’équipe à partir de l’onglet d’équipe](media/RM-how-to-1.png)

3. <span data-ttu-id="7f938-109">Dans la boîte de dialogue **Création rapide : Membre de l’équipe de projet**, sélectionnez la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="7f938-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="7f938-110">Le champ **Rôle** se remplit avec le rôle par défaut de la ressource si elle en a un d’attribué.</span><span class="sxs-lookup"><span data-stu-id="7f938-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="7f938-111">Vous pouvez modifier le rôle si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7f938-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="7f938-112">Sélectionnez les dates de début et de fin auxquelles la ressource sera nécessaire et sélectionnez la méthode d’allocation de la capacité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7f938-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="7f938-113">Si vous voulez que le membre de l’équipe soit un approbateur de projet, sélectionnez **Oui** dans le champ **Approbateur du projet**.</span><span class="sxs-lookup"><span data-stu-id="7f938-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="7f938-114">Cela signifiera que le membre de l’équipe peut approuver les entrées de temps et de dépenses envoyées pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="7f938-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="7f938-115">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f938-115">Click **Save**.</span></span>

![Ajout d’un membre de l’équipe au formulaire de création rapide](media/RM-how-to-2.png)


<span data-ttu-id="7f938-117">Vous pouvez désormais attribuer la ressource réservée aux tâches sur le projet.</span><span class="sxs-lookup"><span data-stu-id="7f938-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="7f938-118">Dans la page **Projet**, cliquez sur l’onglet **Planification** pour attribuer des tâches à la nouvelle ressource.</span><span class="sxs-lookup"><span data-stu-id="7f938-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="7f938-119">Le sélecteur de ressources lancé à partir du champ **Ressources** dans la grille de tâches affichera les membres de l’équipe que vous pouvez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="7f938-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Attribution d’un membre de l’équipe à une tâche sur l’onglet de planification](media/RM-how-to-3.png)

<span data-ttu-id="7f938-121">Dans la version 3 de Project Service Automation (PSA), les réservations de ressources et les attributions de tâches ne sont pas couplées étroitement.</span><span class="sxs-lookup"><span data-stu-id="7f938-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="7f938-122">Cela signifie que si vous utilisez le sélecteur de ressources dans la planification, vous pouvez attribuer des tâches aux membres de l’équipe pour plus d’heures que leurs réservation n’en couvre.</span><span class="sxs-lookup"><span data-stu-id="7f938-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="7f938-123">Vous pouvez voir les différences entre les réservations et les attributions de membres de l’équipe sur l’onglet **Équipe** ou sur l’onglet **Rapprochement des ressources**. Vous pouvez également rapprocher les différences entre les réservations et les attributions pour les ressources à un niveau plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="7f938-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Onglet Rapprochement des ressources](media/RM-how-to-4.png)

<span data-ttu-id="7f938-125">Vous pouvez également utiliser le sélecteur de ressources sur l’onglet **Planification** pour rechercher et sélectionner les ressources réservables qui ne font pas déjà partie de l’équipe du projet.</span><span class="sxs-lookup"><span data-stu-id="7f938-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="7f938-126">Celles-ci sont affichées dans le sélecteur de ressources comme **Autres ressources**.</span><span class="sxs-lookup"><span data-stu-id="7f938-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Attribution d’une ressource non membre de l’équipe à une tâche](media/RM-how-to-5.png)

<span data-ttu-id="7f938-128">Une fois cette opération effectuée, la ressource est ajoutée à l’équipe du projet et attribuée à la tâche, mais aucune réservation n’est générée.</span><span class="sxs-lookup"><span data-stu-id="7f938-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membre de l’équipe avec des attributions mais aucune réservation](media/RM-how-to-6.png)

<span data-ttu-id="7f938-130">Vous pouvez utiliser la capacité d’extension de réservation de l’onglet **Rapprochement** ou le **Tableau de planification** pour réserver la capacité de la ressource sur le projet.</span><span class="sxs-lookup"><span data-stu-id="7f938-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Extension des réservations d’un membre de l’équipe sous l’onglet de rapprochement des ressources](media/RM-how-to-7.png)

<span data-ttu-id="7f938-132">Lorsqu’un membre de l’équipe est réservé sur votre projet, vous pouvez gérer les réservations ou utiliser le tableau de planification directement pour gérer ses réservations.</span><span class="sxs-lookup"><span data-stu-id="7f938-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
