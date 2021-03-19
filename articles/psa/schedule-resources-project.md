---
title: Planifier des ressources pour un projet
description: Procédure de planification de ressources pour un projet dans Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282645"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="ec7ca-103">Planifier des ressources pour un projet (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ec7ca-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ec7ca-104">Vous pouvez afficher la disponibilité des ressources afin d’avoir une vue globale de la façon dont les ressources sont réservées, ou vous pouvez filtrer la vue par compétences, équipe, emplacement, et d’autres options.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="ec7ca-105">Le tableau de planification affiche la liste des ressources et leurs disponibilités.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="ec7ca-106">Sélectionnez un mode d’affichage pour afficher la disponibilité par **Heure**, **Jour**, **Semaine** ou **Mois**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="ec7ca-107">Avant d’utiliser le tableau de planification, il est important de le configurer.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="ec7ca-108">Pour plus d’informations, consultez [Configurer le tableau de planification (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="ec7ca-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="ec7ca-109">Si vous utilisez une nouvelle version, pour la disponibilité des ressources, consultez [Afficher la disponibilité des ressources](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="ec7ca-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="ec7ca-110">Pour utiliser la fonctionnalité de réservation du tableau de planification, le géocodage et les services d’emplacement, vous devez activer des cartes.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="ec7ca-111">Dans le menu principal, sélectionnez **Planification des ressources** > **Administration**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="ec7ca-112">Cliquez sur **Paramètres de planification**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="ec7ca-113">Ouvrez l’enregistrement et faites défiler la liste jusqu’à la section **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="ec7ca-114">Dans le champ **Se connecter aux cartes**, choisissez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="ec7ca-115">Acceptez les conditions et enregistrez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="ec7ca-116">Dans le menu principal, sélectionnez **Project Service** > **Tableau de planification**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="ec7ca-117">À ce stade, il existe plusieurs méthodes permettant de planifier manuellement un besoin en réservation.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="ec7ca-118">Choisissez la méthode qui fonctionne pour vous.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="ec7ca-119">Trouver des ressources disponibles</span><span class="sxs-lookup"><span data-stu-id="ec7ca-119">Find available resources</span></span>

1.  <span data-ttu-id="ec7ca-120">Dans la liste **Besoins en réservations**, cliquez avec le bouton droit sur une réservation non planifiée et choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec7ca-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="ec7ca-121">Choisissez **Recherche de disponibilité - Ressources actuelles** pour rechercher une ressource disponible dans la liste du tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="ec7ca-122">Choisissez **Recherche de disponibilité - Toutes les ressources** pour rechercher une ressource disponible dans les ressources du système.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="ec7ca-123">Une fois cette opération effectuée, les filtres affichent les options pour les besoins en réservation sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="ec7ca-124">Lorsqu’une plage horaire disponible s’affiche, cliquez avec le bouton droit sur la plage horaire dans le tableau de planification et choisissez **Réserver ici**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="ec7ca-125">Ou, glissez-déplacez les besoins en réservation vers la plage horaire disponible.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="ec7ca-126">Réserver une ressource à l’aide de la vue quotidienne et rechercher les ressources sous-réservées</span><span class="sxs-lookup"><span data-stu-id="ec7ca-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="ec7ca-127">Dans le tableau de planification, sélectionnez **Mode d’affichage** et sélectionnez **Jours**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="ec7ca-128">Une vue de grille s’affiche avec le nombre d’heures pendant lesquelles une ressource est réservée par jour et les jours de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="ec7ca-129">Cliquez sur le nom de la ressource que vous souhaitez réserver, puis sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="ec7ca-130">Dans la boîte de dialogue **Réservation de ressource (créer)**, choisissez le projet pour lequel vous souhaitez réserver la ressource ainsi que la méthode de réservation et les dates de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="ec7ca-131">Une fois que vous avez terminé, sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="ec7ca-132">Afficher le tableau de planification</span><span class="sxs-lookup"><span data-stu-id="ec7ca-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="ec7ca-133">Sélectionnez un besoin en réservation non planifié dans la liste en bas.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="ec7ca-134">Déplacez le besoin en réservation vers une ressource/plage horaire disponible dans le tableau de planification.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="ec7ca-135">Une fois que vous avez terminé, sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="ec7ca-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="ec7ca-136">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="ec7ca-136">Additional resources</span></span>  
 [<span data-ttu-id="ec7ca-137">Guide du gestionnaire de ressources</span><span class="sxs-lookup"><span data-stu-id="ec7ca-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]