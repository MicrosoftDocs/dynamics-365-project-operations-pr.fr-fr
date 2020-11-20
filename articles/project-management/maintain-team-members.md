---
title: Préserver les membres de l’équipe
description: Cette rubrique fournit des informations sur la réservation de ressources nommées dans les équipes de projet et leur attribution de tâches.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131520"
---
# <a name="maintain-team-members"></a><span data-ttu-id="69763-103">Préserver les membres de l’équipe</span><span class="sxs-lookup"><span data-stu-id="69763-103">Maintain team members</span></span>

<span data-ttu-id="69763-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="69763-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69763-105">Vous pouvez ajouter une ressource nommée à votre équipe de projet en les réservant directement dans l’équipe.</span><span class="sxs-lookup"><span data-stu-id="69763-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="69763-106">Dans Dynamics 365 Project Operations, accédez à **Projets**, puis sélectionnez pour ouvrir le projet que réservez.</span><span class="sxs-lookup"><span data-stu-id="69763-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="69763-107">Dans la page **Projet**, dans l’onglet **Équipe**, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="69763-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="69763-108">Dans la boîte de dialogue **Création rapide : Membre de l’équipe de projet**, sélectionnez la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="69763-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="69763-109">Le champ **Rôle** se remplit avec le rôle par défaut de la ressource si elle en a un d’attribué.</span><span class="sxs-lookup"><span data-stu-id="69763-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="69763-110">Vous pouvez changer de rôle.</span><span class="sxs-lookup"><span data-stu-id="69763-110">You can change the role.</span></span> 
4. <span data-ttu-id="69763-111">Sélectionnez les dates de début et de fin auxquelles la ressource sera nécessaire et sélectionnez la méthode d’allocation de la capacité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="69763-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="69763-112">Sélectionnez **Oui** dans le champ **Approbateur du projet** si vous voulez que le membre de l’équipe soit un approbateur de projet.</span><span class="sxs-lookup"><span data-stu-id="69763-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="69763-113">Le membre de l’équipe peut approuver les entrées de temps et de dépenses envoyées pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="69763-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="69763-114">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="69763-114">Select **Save**.</span></span>

<span data-ttu-id="69763-115">Vous pouvez désormais attribuer la ressource réservée aux tâches sur le projet.</span><span class="sxs-lookup"><span data-stu-id="69763-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="69763-116">Dans la page **Projet**, sur l’onglet **Planification**, attribuez des tâches à la nouvelle ressource.</span><span class="sxs-lookup"><span data-stu-id="69763-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="69763-117">Le sélecteur de ressources lancé à partir du champ **Ressources** dans la grille de tâches affichera les membres de l’équipe que vous pouvez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="69763-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="69763-118">Dans Project Operations, les réservations de ressources et les affectations de tâches ne sont pas étroitement liées.</span><span class="sxs-lookup"><span data-stu-id="69763-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="69763-119">Si vous utilisez le sélecteur de ressources dans la planification, vous pouvez attribuer des tâches aux membres de l’équipe pour plus d’heures que leurs réservation n’en couvre.</span><span class="sxs-lookup"><span data-stu-id="69763-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="69763-120">Les différences entre les réservations et les affectations des membres de l’équipe sont indiquées sur les onglets **Équipe** et **Rapprochement des ressources**.</span><span class="sxs-lookup"><span data-stu-id="69763-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="69763-121">Vous pouvez également rapprocher les différences entre les réservations et les affectations de ressources à un niveau plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="69763-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="69763-122">Utilisez le sélecteur de ressources sur l’onglet **Planification** pour rechercher et sélectionner les ressources réservables qui ne font pas déjà partie de l’équipe du projet.</span><span class="sxs-lookup"><span data-stu-id="69763-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="69763-123">Ces ressources sont affichées dans le sélecteur de ressources comme **Autres ressources**.</span><span class="sxs-lookup"><span data-stu-id="69763-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="69763-124">Une fois que vous effectuez une sélection, la ressource est ajoutée à l’équipe du projet et attribuée à la tâche, mais aucune réservation n’est générée.</span><span class="sxs-lookup"><span data-stu-id="69763-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="69763-125">Vous pouvez utiliser la capacité d’extension de réservation de l’onglet **Rapprochement** ou le **Tableau de planification** pour réserver la capacité de la ressource sur le projet.</span><span class="sxs-lookup"><span data-stu-id="69763-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="69763-126">Lorsqu’un membre de l’équipe est réservé sur votre projet, vous pouvez **Gérer les réservations** ou utiliser le **Tableau de planification** directement pour gérer ses réservations.</span><span class="sxs-lookup"><span data-stu-id="69763-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
