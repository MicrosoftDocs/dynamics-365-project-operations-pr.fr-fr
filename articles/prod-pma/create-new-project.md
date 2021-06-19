---
title: Créer un projet
description: Cette rubrique donne des informations sur la création d’un nouveau projet.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006238"
---
# <a name="create-a-new-project"></a><span data-ttu-id="04292-103">Créer un projet</span><span class="sxs-lookup"><span data-stu-id="04292-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04292-104">Procédez comme suit pour créer un projet.</span><span class="sxs-lookup"><span data-stu-id="04292-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="04292-105">Sur la page **Gestion de projet**, sélectionnez **Nouveau projet**, et saisissez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04292-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="04292-106">**Type de projet :** Temps et matériel</span><span class="sxs-lookup"><span data-stu-id="04292-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="04292-107">**Nom du projet :** Mise à niveau XYZ Phase 2</span><span class="sxs-lookup"><span data-stu-id="04292-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="04292-108">**Groupe de projets :** TM\_TEC</span><span class="sxs-lookup"><span data-stu-id="04292-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="04292-109">**ID de contrat du projet :** 00000002</span><span class="sxs-lookup"><span data-stu-id="04292-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="04292-110">Sélectionnez **Créer un projet**.</span><span class="sxs-lookup"><span data-stu-id="04292-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="04292-111">Attribuer une ressource à un projet</span><span class="sxs-lookup"><span data-stu-id="04292-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="04292-112">Sur la page **Employés**, dans la liste **Employés**, sélectionnez l’enregistrement pour l’employé pour lequel vous avez précédemment configuré des compétences, et ouvrez l’enregistrement de l’employé.</span><span class="sxs-lookup"><span data-stu-id="04292-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="04292-113">Dans le volet Actions, sur l’onglet **Projet**, dans le groupe **Configuration**, sélectionnez **Attribuer les projets**.</span><span class="sxs-lookup"><span data-stu-id="04292-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="04292-114">Sur la page **Affectations de projets de validation de ressources**, sur l’onglet **Projets**, dans le champ **Ajouter le projet aux projets sélectionnés**, filtrez sur le projet **Mise à niveau XYZ Phase 2**.</span><span class="sxs-lookup"><span data-stu-id="04292-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="04292-115">Dans le volet **Projets restants**, sélectionnez un projet, puis sélectionnez le bouton fléché pour l’ajouter au volet **Projets sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="04292-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="04292-116">Vous pouvez également attribuer des catégories à une ressource selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="04292-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="04292-117">Le type de catégorie est soit **Coût** soit **Revenu**.</span><span class="sxs-lookup"><span data-stu-id="04292-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="04292-118">Le type de catégorie est déterminé par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="04292-118">The category type is determined by your organization.</span></span> <span data-ttu-id="04292-119">Si aucune catégorie n’est affectée à une ressource, Finance recherche la catégorie par défaut sur les prix horaires pour le coût et le revenu.</span><span class="sxs-lookup"><span data-stu-id="04292-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="04292-120">Configurer les caractéristiques des ressources et des rôles du projet</span><span class="sxs-lookup"><span data-stu-id="04292-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="04292-121">Un chef de projet peut utiliser la fonctionnalité de ressources de projet pour créer les rôles requis pour le projet.</span><span class="sxs-lookup"><span data-stu-id="04292-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="04292-122">Les rôles peuvent être utilisés si les ressources confirmées sont toujours inconnues lorsque les ressources sont réservées.</span><span class="sxs-lookup"><span data-stu-id="04292-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="04292-123">Les rôles peuvent être temporairement réservés en tant que ressources planifiées, afin que vous puissiez poursuivre les étapes de planification du projet.</span><span class="sxs-lookup"><span data-stu-id="04292-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="04292-124">[![Exemple de rôle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="04292-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="04292-125">**Scénario :** Contoso a été engagé pour mener à bien un projet en régie qui comporte une charte de projet approuvée.</span><span class="sxs-lookup"><span data-stu-id="04292-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="04292-126">Le chef de projet junior est toujours en train de compléter la portée du projet.</span><span class="sxs-lookup"><span data-stu-id="04292-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="04292-127">Le responsable des ressources identifie actuellement des ressources spécifiques qui seront réservées pour travailler sur le nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="04292-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="04292-128">En raison de la nature critique du projet, le commanditaire a demandé le chef de projet senior comme l’un des rôles.</span><span class="sxs-lookup"><span data-stu-id="04292-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="04292-129">Le responsable des ressources doit acquérir la nouvelle ressource et définir le rôle dans le système au cas où le chef de projet junior aurait besoin des informations sur la ressource lors de la planification du projet.</span><span class="sxs-lookup"><span data-stu-id="04292-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="04292-130">Les étapes suivantes montrent comment le responsable des ressources peut configurer le rôle de chef de projet principal et y associer des caractéristiques de ressource.</span><span class="sxs-lookup"><span data-stu-id="04292-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="04292-131">Plus tard, le rôle peut être utilisé pour rechercher des ressources disponibles qui correspondent aux compétences de ressources requises.</span><span class="sxs-lookup"><span data-stu-id="04292-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="04292-132">Sur la page **Configurer les rôles**, sélectionnez **Nouveau**, et saisissez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04292-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="04292-133">**ID de rôle :** chef de projet senior</span><span class="sxs-lookup"><span data-stu-id="04292-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="04292-134">**Description :** chef de projet senior</span><span class="sxs-lookup"><span data-stu-id="04292-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="04292-135">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="04292-135">Select **Create**.</span></span>
3. <span data-ttu-id="04292-136">Sélectionnez le rôle **Chef de projet senior**, puis **Configurer les caractéristiques**.</span><span class="sxs-lookup"><span data-stu-id="04292-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="04292-137">Dans le champ **Type de caractéristique**, sélectionnez **Compétence**.</span><span class="sxs-lookup"><span data-stu-id="04292-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="04292-138">Dans le champ **Caractéristiques disponibles**, entrez la compétence à rechercher.</span><span class="sxs-lookup"><span data-stu-id="04292-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="04292-139">Dans le champ **Type de caractéristique**, sélectionnez **Certificat**.</span><span class="sxs-lookup"><span data-stu-id="04292-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="04292-140">Dans le champ **Caractéristiques disponibles**, entrez le type de certificat à rechercher.</span><span class="sxs-lookup"><span data-stu-id="04292-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="04292-141">Attribuer une ressource de projet à un projet</span><span class="sxs-lookup"><span data-stu-id="04292-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="04292-142">Sur la page **Tous les projets**, sélectionnez le projet **Mise à niveau XYZ Phase 2**.</span><span class="sxs-lookup"><span data-stu-id="04292-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="04292-143">Sur l’onglet **Équipe de projet et planification**, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="04292-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="04292-144">Dans le champ **Rôle**, sélectionnez **Membre de l’équipe**.</span><span class="sxs-lookup"><span data-stu-id="04292-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="04292-145">Sélectionnez **Réserver depuis le calendrier**.</span><span class="sxs-lookup"><span data-stu-id="04292-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="04292-146">Sur la page **Disponibilité des ressources**, sélectionnez **Paramètres d’affichage**.</span><span class="sxs-lookup"><span data-stu-id="04292-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="04292-147">Sur la page **Ajuster les paramètres d’affichage**, entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04292-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="04292-148">**Format d’affichage de la plage de dates :** Journée</span><span class="sxs-lookup"><span data-stu-id="04292-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="04292-149">**Afficher les descriptions de disponibilité :** Oui</span><span class="sxs-lookup"><span data-stu-id="04292-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="04292-150">**Afficher la capacité restante :** Oui</span><span class="sxs-lookup"><span data-stu-id="04292-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="04292-151">Dans la liste des ressources, sélectionnez une ressource.</span><span class="sxs-lookup"><span data-stu-id="04292-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="04292-152">Sélectionnez **Réservation ferme** et **Capacité maximale**.</span><span class="sxs-lookup"><span data-stu-id="04292-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="04292-153">Attribuer une ressource à un rôle par défaut</span><span class="sxs-lookup"><span data-stu-id="04292-153">Assign a resource to a default role</span></span>

<span data-ttu-id="04292-154">Pour aider les responsables de ressources ou les chefs de projets à explorer davantage les ressources qui peuvent être réservées pour un projet.</span><span class="sxs-lookup"><span data-stu-id="04292-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="04292-155">Vous pouvez associer un rôle par défaut à une ressource existante ou à une ressource nouvellement acquise.</span><span class="sxs-lookup"><span data-stu-id="04292-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="04292-156">Par exemple, lorsque Daniel a été embauché, il avait l’expérience et les compétences nécessaires pour remplir le rôle d’analyste d’affaires.</span><span class="sxs-lookup"><span data-stu-id="04292-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="04292-157">Le responsable de ressources a attribué ce rôle comme rôle par défaut de Daniel.</span><span class="sxs-lookup"><span data-stu-id="04292-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="04292-158">Par conséquent, le responsable des ressources a ajouté Daniel à un groupe d’analystes d’affaires disponibles pour travailler sur des projets.</span><span class="sxs-lookup"><span data-stu-id="04292-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="04292-159">Lors de la réservation de ressources, les chefs de projet peuvent filtrer les ressources de rôle disponibles pour travailler sur des projets.</span><span class="sxs-lookup"><span data-stu-id="04292-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="04292-160">Ils peuvent utiliser ces informations comme un critère lorsqu’ils effectuent une analyse de décision multicritères pendant l’exécution des ressources.</span><span class="sxs-lookup"><span data-stu-id="04292-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="04292-161">Ils peuvent également ajouter d’autres caractéristiques de ressources au filtre pour rechercher des ressources qui ont des compétences, une formation et une expérience spécifiques pour un projet donné.</span><span class="sxs-lookup"><span data-stu-id="04292-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="04292-162">**Scénario :** Un projet approuvé a démarré et le rôle de chef de projet principal a été réservé en tant que ressource planifiée pendant la phase de planification du projet.</span><span class="sxs-lookup"><span data-stu-id="04292-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="04292-163">Le responsable des ressources a maintenant acquis une ressource pour remplir le rôle de chef de projet senior.</span><span class="sxs-lookup"><span data-stu-id="04292-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="04292-164">Sur la page **Liste des ressources**, sélectionnez **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="04292-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="04292-165">Sur la page **Rôle de la ressource**, sélectionnez **Nouveau**, et saisissez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04292-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="04292-166">**Efficace :** saisissez la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="04292-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="04292-167">**Expiration :** saisissez **Jamais**.</span><span class="sxs-lookup"><span data-stu-id="04292-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="04292-168">**Rôle** : saisissez **Chef de projet senior**.</span><span class="sxs-lookup"><span data-stu-id="04292-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="04292-169">Cliquez sur **Enregistrer** puis fermez la page.</span><span class="sxs-lookup"><span data-stu-id="04292-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="04292-170">Sur l’onglet **Compétences**, ajoutez la compétence **ProjectMgmt** et le certificat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="04292-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]