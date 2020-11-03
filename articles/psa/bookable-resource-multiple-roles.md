---
title: Estimation des ventes et des coûts d’un projet lorsqu’une ressource pouvant être réservée répond à plusieurs rôles dans un projet
description: Cette rubrique donne des informations sur la manière dont les dimensions Tarification peuvent être utilisées pour soutenir la tarification et les coûts d’une ressource qui répond à plusieurs rôles dans un projet.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075792"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="9302f-103">Estimation des ventes et des coûts d’un projet lorsqu’une ressource pouvant être réservée répond à plusieurs rôles dans un projet</span><span class="sxs-lookup"><span data-stu-id="9302f-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="9302f-104">Les entreprises basées sur des projets ont souvent besoin d’une seule ressource pour exécuter plusieurs rôles dans un projet.</span><span class="sxs-lookup"><span data-stu-id="9302f-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="9302f-105">Chacun de ces rôles pourrait être évalué différemment en termes de prix et de coût. Autrement dit, le même temps de la ressource dans le projet pourrait obtenir une autre estimation financière en fonction des taux de facturation et de coût pour chacun des rôles.</span><span class="sxs-lookup"><span data-stu-id="9302f-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="9302f-106">Project Service Automation permet de configurer les valeurs sur l’enregistrement de membre de l’équipe pour la ressource désignée et permet également différents remplacements sur chacune des tâches auxquelles le membre de l’équipe est attribué.</span><span class="sxs-lookup"><span data-stu-id="9302f-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="9302f-107">L’exemple suivant explique comment le simple remplacement de cette valeur permet à une ressource d’avoir plusieurs rôles sur un projet avec différents taux de facturation et de coût.</span><span class="sxs-lookup"><span data-stu-id="9302f-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="9302f-108">Créer des tâches</span><span class="sxs-lookup"><span data-stu-id="9302f-108">Create tasks</span></span>
<span data-ttu-id="9302f-109">Créez deux tâches de projet pour 40 heures chacune. Nous les appellerons Tâche A et Tâche B. Sélectionnez la Tâche A comme prédécesseur à la Tâche B.</span><span class="sxs-lookup"><span data-stu-id="9302f-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="9302f-110">Configurer le rôle et l’unité organisationnelle pour un membre de l’équipe de projet générique</span><span class="sxs-lookup"><span data-stu-id="9302f-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="9302f-111">Sur la page **Programme** , sélectionnez la ligne **Tâche** pour la Tâche A.</span><span class="sxs-lookup"><span data-stu-id="9302f-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="9302f-112">Dans le champ **Ressources** , sélectionnez **Créer** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="9302f-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="9302f-113">Sur la page **Créer rapidement un membre d’équipe** , spécifiez les attributs du membre générique de l’équipe qui peut effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="9302f-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="9302f-114">Sélectionnez le rôle et l’unité organisationnelle appropriés, puis sélectionnez **Enregistrer et fermer**.</span><span class="sxs-lookup"><span data-stu-id="9302f-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="9302f-115">Un membre de l’équipe générique est créé et affecté à cette tâche.</span><span class="sxs-lookup"><span data-stu-id="9302f-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="9302f-116">Répétez ces étapes pour la Tâche B et veillez à ce que le rôle et l’unité organisationnelle sur le membre de l’équipe générique créés pour la Tâche B soit différents de ceux de la Tâche A.</span><span class="sxs-lookup"><span data-stu-id="9302f-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="9302f-117">Configurer un rôle et une unité organisationnelle pour une tâche de projet</span><span class="sxs-lookup"><span data-stu-id="9302f-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="9302f-118">Après avoir créé la Tâche A, sélectionnez la tâche, puis sélectionnez **Modifier la tâche**.</span><span class="sxs-lookup"><span data-stu-id="9302f-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="9302f-119">Sur la page **Détails de la tâche** , recherchez les champs **Rôle** et **Unité organisationnelle** , ajoutez les valeurs nécessaires d’une ressource qui effectuerait cette tâche.</span><span class="sxs-lookup"><span data-stu-id="9302f-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="9302f-120">Si vous exécutez ces scénarios avec les données de démonstration Project Service Automation, sélectionnez **Consultant** pour le rôle et **Fabrikam US** comme unité organisationnelle.</span><span class="sxs-lookup"><span data-stu-id="9302f-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="9302f-121">Sélectionnez Tâche B, puis sélectionnez **Modifier la tâche**.</span><span class="sxs-lookup"><span data-stu-id="9302f-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="9302f-122">Sur la page **Détails de la tâche** , recherchez les champs **Rôle** et **Unité organisationnelle** , ajoutez les valeurs nécessaires d’une ressource qui effectuerait cette tâche.</span><span class="sxs-lookup"><span data-stu-id="9302f-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="9302f-123">Veillez à ce que les valeurs des champs **Rôle** et **Unité organisationnelle** soient différents pour la Tâche B par rapport à la Tâche A.</span><span class="sxs-lookup"><span data-stu-id="9302f-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="9302f-124">Si vous exécutez ces scénarios avec les données de démonstration Project Service Automation, sélectionnez **Technicien réseau** pour le rôle et **Fabrikam US** comme unité organisationnelle.</span><span class="sxs-lookup"><span data-stu-id="9302f-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="9302f-125">Enregistrez et fermez la page **Détails de la tâche**.</span><span class="sxs-lookup"><span data-stu-id="9302f-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="9302f-126">Membre de l’équipe et comportement d’estimations</span><span class="sxs-lookup"><span data-stu-id="9302f-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="9302f-127">Sur la page **Détails de la tâche** , sur le champ **Membre de l’équipe** , sélectionnez les deux membres de l’équipe générique, puis sélectionnez **Générer des besoins**.</span><span class="sxs-lookup"><span data-stu-id="9302f-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="9302f-128">Cela génère des besoins en ressource.</span><span class="sxs-lookup"><span data-stu-id="9302f-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="9302f-129">Sélectionnez la ligne du membre de l’équipe pour le champ **Consultant** , puis sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="9302f-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="9302f-130">Le tableau de bord de planification ouvre et réserve une ressource pour ce besoin.</span><span class="sxs-lookup"><span data-stu-id="9302f-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="9302f-131">Sélectionnez la ligne du membre de l’équipe pour le champ **Technicien réseau** , puis sélectionnez **Réserver**.</span><span class="sxs-lookup"><span data-stu-id="9302f-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="9302f-132">Le tableau de bord de planification ouvre et réserve la même ressource pour ce besoin.</span><span class="sxs-lookup"><span data-stu-id="9302f-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="9302f-133">Grille du membre de l’équipe</span><span class="sxs-lookup"><span data-stu-id="9302f-133">Team Member grid</span></span> 
<span data-ttu-id="9302f-134">Dans la grille **Membre de l’équipe** , notez que les deux enregistrements de membre de l’équipe générique ont été supprimés et remplacés par une ressource.</span><span class="sxs-lookup"><span data-stu-id="9302f-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="9302f-135">Il existe un ensemble de valeurs pour cette ressource qui affiche un ensemble de valeurs par défaut pour les champs **Rôle** et **Unité organisationnelle**.</span><span class="sxs-lookup"><span data-stu-id="9302f-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="9302f-136">Lorsque vous développez la ligne de cet enregistrement Membre de l’équipe, vous pouvez voir différentes affectations sur l’enregistrement du membre de l’équipe pour ces deux tâches.</span><span class="sxs-lookup"><span data-stu-id="9302f-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="9302f-137">Chaque ligne d’affectation a des valeurs spécifiques à la tâche pour **Rôle** et **Unité organisationnelle**.</span><span class="sxs-lookup"><span data-stu-id="9302f-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="9302f-138">Grille des estimations</span><span class="sxs-lookup"><span data-stu-id="9302f-138">Estimates grid</span></span> 
<span data-ttu-id="9302f-139">Lorsque vous accédez à la grille **Estimations** , vous observerez que les deux affectations pour la même ressource ont des tarifs différents.</span><span class="sxs-lookup"><span data-stu-id="9302f-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="9302f-140">L’affectation de la ressource sur la Tâche A est tarifée en utilisant la valeur d’attribut **Rôle** de **Consultant**.</span><span class="sxs-lookup"><span data-stu-id="9302f-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="9302f-141">L’affectation de la même ressource sur la Tâche B est tarifée en utilisant la valeur d’attribut **Rôle** de **Technicien réseau**.</span><span class="sxs-lookup"><span data-stu-id="9302f-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





