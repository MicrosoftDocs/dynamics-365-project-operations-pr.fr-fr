---
title: Gérer les fuseaux horaires
description: Lorsqu’un projet est créé, son fuseau horaire est basé sur le fuseau horaire défini dans le modèle d’heures de travail appliqué.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997733"
---
# <a name="manage-time-zones"></a><span data-ttu-id="11d0f-103">Gérer les fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="11d0f-103">Manage time zones</span></span>

<span data-ttu-id="11d0f-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="11d0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="11d0f-105">Projets</span><span class="sxs-lookup"><span data-stu-id="11d0f-105">Projects</span></span>

<span data-ttu-id="11d0f-106">Lorsqu’un projet est créé, le fuseau horaire est basé sur le fuseau horaire défini dans le modèle d’heures de travail appliqué.</span><span class="sxs-lookup"><span data-stu-id="11d0f-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="11d0f-107">Sur le **Projet** de, les dates sont toujours relatives au fuseau horaire de l’utilisateur connecté sur chaque onglet, à l’exception de l’onglet **Tâche**. Lorsque vous affichez la structure de répartition du travail, les dates seront toujours affichées dans le fuseau horaire du projet.</span><span class="sxs-lookup"><span data-stu-id="11d0f-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="11d0f-108">Tâches</span><span class="sxs-lookup"><span data-stu-id="11d0f-108">Tasks</span></span>

<span data-ttu-id="11d0f-109">Lorsqu’une tâche est créée, l’heure de début, l’heure de fin et les heures/jour sont contrôlés par les heures de travail du projet.</span><span class="sxs-lookup"><span data-stu-id="11d0f-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="11d0f-110">Par exemple, si une tâche est créée avec un projet dont le fuseau horaire est -8 HCP et a les heures de travail suivantes : 9 h 00 à 17 h 00 du lundi au vendredi, toute tâche créée sans affectation respectera l’heure de début et heure de fin du calendrier du projet.</span><span class="sxs-lookup"><span data-stu-id="11d0f-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="11d0f-111">Gérer les ressources avec les fuseaux horaires</span><span class="sxs-lookup"><span data-stu-id="11d0f-111">Manage resources with time zones</span></span>

<span data-ttu-id="11d0f-112">Pour des résultats précis et prévisibles lors de l’utilisation de **Prolonger la réservation**, deux conditions préalables essentielles doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="11d0f-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="11d0f-113">L’utilisateur doit configurer le fuseau horaire de son appareil pour qu’il corresponde au fuseau horaire défini dans les **Paramètres de personnalisation** du système.</span><span class="sxs-lookup"><span data-stu-id="11d0f-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Paramètres de fuseau horaire dans Windows 10](media/reconcile-assignments-03.png)

  ![Paramètres de fuseau horaire dans les paramètres de personnalisation](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="11d0f-116">La ressource réservable doit avoir au moins une minute de temps de travail qui se chevauche avec les profils utilisés pour définir l’extension demandée.</span><span class="sxs-lookup"><span data-stu-id="11d0f-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="11d0f-117">Par exemple, les ressources suivantes avec des heures de travail comprises entre 9 h 00 et 19 h 00.</span><span class="sxs-lookup"><span data-stu-id="11d0f-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparaison de profils de ressource](media/reconcile-assignments-05.png)

<span data-ttu-id="11d0f-119">Le tableau suivant présente :</span><span class="sxs-lookup"><span data-stu-id="11d0f-119">The following table shows:</span></span>

- <span data-ttu-id="11d0f-120">Un modèle de calendrier de projet</span><span class="sxs-lookup"><span data-stu-id="11d0f-120">A project calendar template</span></span>
- <span data-ttu-id="11d0f-121">Ressource A : cette ressource a le même calendrier et se trouve dans le même fuseau horaire que le projet.</span><span class="sxs-lookup"><span data-stu-id="11d0f-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="11d0f-122">L’heure de début des réservations sera 9h00.</span><span class="sxs-lookup"><span data-stu-id="11d0f-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="11d0f-123">Ressource B : Cette ressource est située dans un fuseau horaire différent de celui du projet et commence à 7 h 00 dans leur fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="11d0f-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="11d0f-124">Cependant, les réservations commenceront à 9h00, car il s’agit de l’heure de début la plus proche du profil d’affectation.</span><span class="sxs-lookup"><span data-stu-id="11d0f-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="11d0f-125">Ressources C et D : Les ressources sont situées dans des fuseaux horaires différents, tous deux différents les uns des autres et du projet, et leurs réservations ne commencent pas avant leurs heures de début disponibles respectives.</span><span class="sxs-lookup"><span data-stu-id="11d0f-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="11d0f-126">Entité</span><span class="sxs-lookup"><span data-stu-id="11d0f-126">Entity</span></span>  |<span data-ttu-id="11d0f-127">Calendrier</span><span class="sxs-lookup"><span data-stu-id="11d0f-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="11d0f-128">Modèle de calendrier de projet</span><span class="sxs-lookup"><span data-stu-id="11d0f-128">Project calendar template</span></span>   | ![calendrier du projet](media/reconcile-assignments-06.png) |
|<span data-ttu-id="11d0f-130">Ressource A</span><span class="sxs-lookup"><span data-stu-id="11d0f-130">Resource A</span></span>  | ![Calendrier de la ressource A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="11d0f-132">Ressource B</span><span class="sxs-lookup"><span data-stu-id="11d0f-132">Resource B</span></span>  |  ![Calendrier de la ressource B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="11d0f-134">Ressource C</span><span class="sxs-lookup"><span data-stu-id="11d0f-134">Resource C</span></span>  |  ![Calendrier de la ressource C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="11d0f-136">Ressource D</span><span class="sxs-lookup"><span data-stu-id="11d0f-136">Resource D</span></span>  | ![Calendrier de la ressource D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="11d0f-138">Lorsque vous accédez à la vue **Rapprochement**, les affectations de ressources et les pénuries de réservation associées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="11d0f-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vue Rapprochement avant l’extension](media/reconcile-assignments-10.png)

<span data-ttu-id="11d0f-140">Une fois que la fonctionnalité d’extension de réservation a été utilisée pour chaque ressource, les réservations sont prolongées avec succès pour chaque ressource, car les heures de travail de chaque ressource chevauchent les contours de la pénurie.</span><span class="sxs-lookup"><span data-stu-id="11d0f-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vue Rapprochement après l’extension de la réservation](media/reconcile-assignments-11.png) 

<span data-ttu-id="11d0f-142">Notez qu’un examen plus approfondi des détails des réservations montre des différences dans l’heure de début des réservations.</span><span class="sxs-lookup"><span data-stu-id="11d0f-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="11d0f-143">Les réservations commencent au plus tôt à l’heure de début du contour d’affectation et au plus tôt à l’heure de début disponible de la ressource.</span><span class="sxs-lookup"><span data-stu-id="11d0f-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nouvelles réservations des ressources dans le tableau de planification](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]