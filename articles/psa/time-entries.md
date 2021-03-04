---
title: Créer des entrées de temps
description: Cette rubrique donne des informations sur la création d’entrées de temps.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149675"
---
# <a name="create-time-entries"></a><span data-ttu-id="131a4-103">Créer des entrées de temps</span><span class="sxs-lookup"><span data-stu-id="131a4-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="131a4-104">Dans les versions précédentes de Dynamics 365 Project Service Automation, les entrées de temps étaient créées chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="131a4-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="131a4-105">Dans la version 3 de Project Service Automation, les entrées de temps sont créées chaque jour.</span><span class="sxs-lookup"><span data-stu-id="131a4-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="131a4-106">Toutefois, une fois que quelques entrées de temps ont été créées, vous pouvez les copier en bloc ou en créer d’autres en bloc.</span><span class="sxs-lookup"><span data-stu-id="131a4-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="131a4-107">Créer une entrée de temps</span><span class="sxs-lookup"><span data-stu-id="131a4-107">Create a time entry</span></span>

<span data-ttu-id="131a4-108">Pour créer une entrée de temps, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="131a4-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="131a4-109">Dans la page **Entrées de temps**, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="131a4-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="131a4-110">Dans la boîte de dialogue **Création rapide : Entrée de temps**, entrez la durée de l’entrée de temps en minutes, heures ou jours.</span><span class="sxs-lookup"><span data-stu-id="131a4-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="131a4-111">La durée doit être entrée dans l’un des formats suivants : *x* minutes, *x* heures ou *x* jours.</span><span class="sxs-lookup"><span data-stu-id="131a4-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="131a4-112">Les heures et les jours peuvent également être entrés sous forme de valeurs décimales, par exemple *x,x* heures » ou *x,x* jours.</span><span class="sxs-lookup"><span data-stu-id="131a4-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="131a4-113">Sélectionnez le type d’entrée de temps et le projet pour lequel vous créez l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="131a4-114">Dans le champ **Tâche du projet**, recherchez la tâche pour cette entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="131a4-115">Si vous créez une entrée de temps pour une tâche qui n’est pas affectée à un utilisateur, dans le champ **Tâche du projet**, sélectionnez le bouton **Rechercher**, sélectionnez **Modifier la vue**, puis sélectionnez **Toutes les tâches du projet actives** pour répertorier toutes les tâches.</span><span class="sxs-lookup"><span data-stu-id="131a4-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="131a4-116">Entrez une description, si nécessaire, puis sélectionnez **Enregistrer et fermer**.</span><span class="sxs-lookup"><span data-stu-id="131a4-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="131a4-117">Une fois l’entrée de temps créée et stockée, vous pouvez la modifier dans la grille d’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="131a4-118">La grille d’entrée de temps prend en charge deux formats :</span><span class="sxs-lookup"><span data-stu-id="131a4-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="131a4-119">Vous pouvez créer des entrées de temps au format **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="131a4-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="131a4-120">Ce format est ensuite converti en heures et fractions.</span><span class="sxs-lookup"><span data-stu-id="131a4-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="131a4-121">Vous pouvez entrer des heures et des fractions directement.</span><span class="sxs-lookup"><span data-stu-id="131a4-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="131a4-122">Notez que les fractions d’une heure ne sont pas des minutes.</span><span class="sxs-lookup"><span data-stu-id="131a4-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="131a4-123">Par conséquent, 1,5 heure représente 1 heure et 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="131a4-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="131a4-124">La même règle s’applique aux fractions d’un jour.</span><span class="sxs-lookup"><span data-stu-id="131a4-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="131a4-125">Un jour est égal à 24 heures, et 0,5 jour représente 12 heures.</span><span class="sxs-lookup"><span data-stu-id="131a4-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="131a4-126">Création d’entrées de temps en bloc</span><span class="sxs-lookup"><span data-stu-id="131a4-126">Bulk create time entries</span></span>

<span data-ttu-id="131a4-127">Une fois que quelques entrées de temps ont été créées, vous pouvez les copier pour créer des entrées de temps supplémentaires en bloc.</span><span class="sxs-lookup"><span data-stu-id="131a4-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="131a4-128">Dans la page **Entrées de temps**, sélectionnez **Copier la semaine**.</span><span class="sxs-lookup"><span data-stu-id="131a4-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="131a4-129">Dans le groupe de champs **À partir de la période**, dans les champs **Date de début** et **Date de fin**, définissez la plage de dates à partir de laquelle copier les entrées de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="131a4-130">Dans le groupe de champs **Vers la période**, dans le champ **Date de début**, spécifiez la date pour laquelle créer des entrées de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="131a4-131">Sélectionnez **Copier** pour créer une copie des entrées de temps correspondant au jour de la semaine spécifiée dans le groupe de champs **Vers la période**.</span><span class="sxs-lookup"><span data-stu-id="131a4-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="131a4-132">Par exemple, l’entrée de temps pour le lundi de la semaine dernière est copiée dans le lundi de la semaine spécifiée dans le groupe de champs **Vers la période**.</span><span class="sxs-lookup"><span data-stu-id="131a4-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="131a4-133">Importer des données pour les entrées de temps</span><span class="sxs-lookup"><span data-stu-id="131a4-133">Import data for time entries</span></span>

<span data-ttu-id="131a4-134">Vous pouvez importer des données à partir des réservations et des affectations du projet.</span><span class="sxs-lookup"><span data-stu-id="131a4-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="131a4-135">Lorsque vous importez des données, vous pouvez spécifier la plage de dates des réservations à importer, puis sélectionner explicitement les réservations devant être créées comme entrées de temps **Brouillon**.</span><span class="sxs-lookup"><span data-stu-id="131a4-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="131a4-136">Fonctionnalités de regroupement, de tri, de recherche et de filtrage</span><span class="sxs-lookup"><span data-stu-id="131a4-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="131a4-137">Vous pouvez regrouper et filtrer des entrées de temps en fonction des dimensions spécifiées dans les colonnes.</span><span class="sxs-lookup"><span data-stu-id="131a4-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="131a4-138">Dans le champ **Regrouper par**, sélectionnez la dimension à utiliser pour filtrer des entrées de temps.</span><span class="sxs-lookup"><span data-stu-id="131a4-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="131a4-139">Vous pouvez également trier les enregistrements d’entrée de temps dans l’ordre croissant ou décroissant à l’aide de la flèche de tri des en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="131a4-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="131a4-140">En outre, vous pouvez afficher ou masquer les entrées en sélectionnant le bouton **Filtrer** sur les en-têtes de colonne, puis, dans la zone **Rechercher**, entrez le texte à utiliser pour rechercher des entrées de temps par nom de projet, tâche de projet, entrée de temps ou ressource.</span><span class="sxs-lookup"><span data-stu-id="131a4-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
