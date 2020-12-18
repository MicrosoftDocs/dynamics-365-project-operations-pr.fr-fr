---
title: Nouveautés ou modifications de la mise à jour (version 26) de Project Service Automation (correctif logiciel), V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643260"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="495dd-102">Mise à jour (version 26) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="495dd-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="495dd-103">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="495dd-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="495dd-104">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="495dd-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="495dd-105">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="495dd-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="495dd-106">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="495dd-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="495dd-107">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="495dd-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="495dd-108">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 26), V3 de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="495dd-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="495dd-109">Cette version a un numéro de build V3.10.44.59 et est généralement disponible via une mise à jour automatique en décembre 2020.</span><span class="sxs-lookup"><span data-stu-id="495dd-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="495dd-110">Mise à jour (version 26)</span><span class="sxs-lookup"><span data-stu-id="495dd-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="495dd-111">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="495dd-111">Bug fixes</span></span>

<span data-ttu-id="495dd-112">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="495dd-112">**Time and Expense**</span></span>

<span data-ttu-id="495dd-113">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="495dd-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="495dd-114">Les utilisateurs peuvent modifier la tâche sur une entrée de temps qui a été approuvée/soumise.</span><span class="sxs-lookup"><span data-stu-id="495dd-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="495dd-115">Erreur « Référence d'objet non définie » lors de l'enregistrement d'une entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="495dd-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="495dd-116">L'importation des entrées de temps à partir des affectations de ressources crée des entrées de temps avec des valeurs DateHeure incorrectes.</span><span class="sxs-lookup"><span data-stu-id="495dd-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="495dd-117">Lorsque Project Service Automation et l'application Field Service sont toutes deux installés, le bouton **Nouveau** s'affiche deux fois sur la barre de commandes pour les entrées de temps dans l'application Field Service.</span><span class="sxs-lookup"><span data-stu-id="495dd-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="495dd-118">Les mises à jour des cellules **Autoriser unité** et **Groupe d’unités** fonctionnent désormais dans la grille **Estimations des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="495dd-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="495dd-119">Le formulaire **Mettre à jour l'entrée de temps Modifier** comprend **Chronologie**.</span><span class="sxs-lookup"><span data-stu-id="495dd-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="495dd-120">L'approbation du temps pour les entrées de temps hors projet bloque le système lors de la recherche d'un rôle d'approbateur de projet.</span><span class="sxs-lookup"><span data-stu-id="495dd-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="495dd-121">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="495dd-121">**Resource Management**</span></span>

<span data-ttu-id="495dd-122">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="495dd-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="495dd-123">Ajout de validation dans le plug-in **PostProjectCreate** pour vérifier une exigence principale avant d'en créer.</span><span class="sxs-lookup"><span data-stu-id="495dd-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="495dd-124">Le formulaire de création rapide **Membre de l'équipe de projet** lève une exception de référence nulle si des champs sont supprimés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="495dd-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="495dd-125">La génération d'exigences pendant 12 heures sur 1 an échouera.</span><span class="sxs-lookup"><span data-stu-id="495dd-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="495dd-126">Exception de référence nulle de message d'erreur améliorée lors de la création des besoins en ressources.</span><span class="sxs-lookup"><span data-stu-id="495dd-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="495dd-127">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="495dd-127">**Project Management**</span></span>

<span data-ttu-id="495dd-128">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="495dd-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="495dd-129">Amélioration de la validation pour traiter l'exception de référence nulle générée dans le plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="495dd-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="495dd-130">Les projets publiés par le complément de bureau Microsoft Project suppriment les affectations non attribuées.</span><span class="sxs-lookup"><span data-stu-id="495dd-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="495dd-131">Ajout d'une nouvelle validation lorsque la référence de projet d'une tâche n'est pas valide en raison d'une exception de référence nulle dans le plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="495dd-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="495dd-132">La grille Membre d'équipe n'affiche pas les affectations distinctes sur l'enregistrement des membres de l'équipe.</span><span class="sxs-lookup"><span data-stu-id="495dd-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="495dd-133">Ajout de nouveaux messages de validation et d'erreur en raison d'une exception de référence nulle dans le plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="495dd-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="495dd-134">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="495dd-134">**Sales**</span></span>

<span data-ttu-id="495dd-135">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="495dd-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="495dd-136">Lors de la sélection d'une ligne basée sur un projet dans un devis ou un contrat, le bouton **Suggestion** ne doit être visible que lors de la sélection d'une ligne basée sur un produit associée à un produit existant.</span><span class="sxs-lookup"><span data-stu-id="495dd-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="495dd-137">Split du privilège **Create_Product** à partir du privilège **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="495dd-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="495dd-138">La suppression d'une ligne de facture entraîne un échec de référence nul sur **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="495dd-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
