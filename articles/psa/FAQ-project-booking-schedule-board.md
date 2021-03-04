---
title: Créer une réservation de projet depuis le tableau Planification
description: Cette rubrique fournit des informations sur la création d’une réservation de projet dans le tableau de planification.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146525"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="e536c-103">Créer une réservation de projet depuis le tableau Planification</span><span class="sxs-lookup"><span data-stu-id="e536c-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e536c-104">Vous pouvez réserver une ressource sur un projet directement sur l’onglet **Équipe** ou en générant un besoin en ressource générique depuis une attribution de membre d’équipe, puis en remplissant le besoin généré avec un membre de l’équipe du projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="e536c-105">Vous pouvez également réserver une ressource sur un projet directement depuis le tableau Planification.</span><span class="sxs-lookup"><span data-stu-id="e536c-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="e536c-106">Pour vous inscrire, trois méthodes s’offrent à vous.</span><span class="sxs-lookup"><span data-stu-id="e536c-106">There are three ways to do this:</span></span>

- <span data-ttu-id="e536c-107">**Réserver à partir d’un besoin en ressource généré :** vous pouvez générer un besoin en ressources après avoir créé une ressource générique et attribué des tâches dans un projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="e536c-108">**Réserver à partir du besoin principal :** les besoins principaux apparaissent sur le tableau Planification sur l’onglet **Projet**.</span><span class="sxs-lookup"><span data-stu-id="e536c-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="e536c-109">**Réserver à partir d’un nouveau besoin en ressource :** vous pouvez créer un besoin en ressources du début et l’associer à un projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="e536c-110">Sur le tableau de Planification, le besoin en ressource apparaît sur l’onglet **Ouvrir les besoins**.</span><span class="sxs-lookup"><span data-stu-id="e536c-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="e536c-111">Réserver à partir d’un besoin en ressource généré</span><span class="sxs-lookup"><span data-stu-id="e536c-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="e536c-112">Vous pouvez créer une ressource générique et lui attribuer une ou plusieurs tâches dans un projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="e536c-113">Vous pouvez ensuite générer un besoin en ressource à partir du membre de l’équipe générique.</span><span class="sxs-lookup"><span data-stu-id="e536c-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="e536c-114">Dans le tableau de Planification, cette ressource s’affiche sur l’onglet **Ouvrir les besoins**. Vous devrez peut-être utiliser des filtres de colonne sur la grille si vous avez de nombreux besoins ouverts.</span><span class="sxs-lookup"><span data-stu-id="e536c-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="e536c-115">![Onglet Ouvrir les besoins sur le tableau de planification](media/FAQ-Project-Booking-Schedule-Board-1.png "Capture d’écran du tableau Réservations et attributions")</span><span class="sxs-lookup"><span data-stu-id="e536c-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e536c-116">Sélectionnez le besoin.</span><span class="sxs-lookup"><span data-stu-id="e536c-116">Select the requirement.</span></span> <span data-ttu-id="e536c-117">L’onglet **Rechercher la disponibilité** s’affiche en haut de la ligne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e536c-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="e536c-118">Lorsque vous sélectionnez l’onglet, le mode Assistant Planifier du Tableau de planification s’ouvre et filtre les ressources disponibles qui répondent au besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="e536c-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="e536c-119">Après cela, vous pouvez réserver une ressource.</span><span class="sxs-lookup"><span data-stu-id="e536c-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="e536c-120">Vous pouvez également faire glisser-déplacer la ligne sélectionnée du bas du Tableau de planification vers une cellule de la ressource dans la grille au-dessus.</span><span class="sxs-lookup"><span data-stu-id="e536c-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="e536c-121">Lorsque vous le déplacez, cette action génère l’ouverture du volet **Créer une réservation de ressource** sur la droite.</span><span class="sxs-lookup"><span data-stu-id="e536c-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="e536c-122">Sélectionner **Réserver** réserve la ressource dans l’équipe du projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-122">Selecting **Book** books the resource onto the project team.</span></span>

![Volet Créer une réservation de ressource](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="e536c-124">Réserver à partir du besoin principal</span><span class="sxs-lookup"><span data-stu-id="e536c-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="e536c-125">La création d’un projet dans Project Service crée automatiquement un besoin en ressource appelé le besoin principal.</span><span class="sxs-lookup"><span data-stu-id="e536c-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="e536c-126">Il s’agit d’un besoin vide qui est utilisé pour réserver rapidement une ressource avec le Tableau de planification sans générer de besoin ni en créer un de zéro.</span><span class="sxs-lookup"><span data-stu-id="e536c-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="e536c-127">Étant donné que le besoin est vide, vous devez spécifier des dates ainsi que la méthode et les heures d’attribution, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e536c-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="e536c-128">Pour réserver une ressource avec le besoin principal sur le Tableau de planification, sélectionnez l’onglet **Projet**. Vous pouvez avoir besoin d’utiliser le filtre de colonne sur la colonne **Projet** si vous avez plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="e536c-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="e536c-129">![Filtres de colonne sur le tableau de planification](media/FAQ-Project-Booking-Schedule-Board-2.png "Capture d’écran du tableau Réservations et attributions")</span><span class="sxs-lookup"><span data-stu-id="e536c-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e536c-130">Sélectionnez le besoin qui a uniquement le nom du projet comme nom et une durée de zéro (0).</span><span class="sxs-lookup"><span data-stu-id="e536c-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="e536c-131">Sélectionnez l’onglet **Rechercher la disponibilité** qui apparaît sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="e536c-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="e536c-132">Cela met le Tableau de planification en mode Assistant Planifier et affiche les ressources disponibles qui peuvent être réservées sur le projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="e536c-133">Comme un **Besoin principal** consiste en un besoin vide avec une durée de zéro (0), vous devez définir la durée sur le volet **Créer une réservation de ressource** lors de la sélection et de la réservation d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="e536c-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="e536c-134">Vous pouvez également sélectionner le **Besoin principal du projet** au bas du Tableau de planification et le faire glisser-déplacer sur une ressource pour le réserver.</span><span class="sxs-lookup"><span data-stu-id="e536c-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="e536c-135">Comme le **Besoin principal** consiste en un besoin vide avec une durée de zéro (0), vous devez définir la durée sur le volet **Créer une réservation de ressource** lorsque vous sélectionnez et réservez une ressource.</span><span class="sxs-lookup"><span data-stu-id="e536c-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="e536c-136">Lorsque vous réservez une ressource via le **Besoin principal** sur le Tableau de planification, vous l’ajoutez à l’équipe du projet sans aucune attribution.</span><span class="sxs-lookup"><span data-stu-id="e536c-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="e536c-137">Réserver à partir d’un nouveau besoin en ressource</span><span class="sxs-lookup"><span data-stu-id="e536c-137">Book from a new resource requirement</span></span>
<span data-ttu-id="e536c-138">Effectuez les étapes suivantes pour réserver un nouveau besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="e536c-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="e536c-139">Accédez à **Besoins en ressources**, puis sélectionnez **Nouveau** pour créer un besoin en ressources.</span><span class="sxs-lookup"><span data-stu-id="e536c-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="e536c-140">Dans l’onglet **Projet**, sélectionnez un projet pour associer le besoin au projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="e536c-141">Sur le Tableau de planification, ce nouveau besoin s’affiche comme **Besoin ouvert** que vous pouvez remplir.</span><span class="sxs-lookup"><span data-stu-id="e536c-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="e536c-142">Réservez la ressource pour l’ajouter à l’équipe du projet.</span><span class="sxs-lookup"><span data-stu-id="e536c-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="e536c-143">Maintenant que la ressource est réservée, vous devez attribuer des tâches manuellement.</span><span class="sxs-lookup"><span data-stu-id="e536c-143">Now that the resource is booked, you must assign tasks manually.</span></span>

