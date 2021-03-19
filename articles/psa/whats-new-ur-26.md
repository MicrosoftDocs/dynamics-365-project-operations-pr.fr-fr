---
title: Nouveautés ou modifications de la mise à jour (version 26) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 26) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280395"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="13f27-103">Mise à jour (version 26) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="13f27-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13f27-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="13f27-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="13f27-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="13f27-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="13f27-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="13f27-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13f27-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="13f27-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="13f27-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="13f27-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="13f27-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 26), V3 de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="13f27-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="13f27-110">Cette version a un numéro de build V3.10.44.59 et est généralement disponible via une mise à jour automatique en décembre 2020.</span><span class="sxs-lookup"><span data-stu-id="13f27-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="13f27-111">Mise à jour (version 26)</span><span class="sxs-lookup"><span data-stu-id="13f27-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13f27-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="13f27-112">Bug fixes</span></span>

<span data-ttu-id="13f27-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="13f27-113">**Time and Expense**</span></span>

<span data-ttu-id="13f27-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="13f27-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="13f27-115">Les utilisateurs peuvent modifier la tâche sur une entrée de temps qui a été approuvée/soumise.</span><span class="sxs-lookup"><span data-stu-id="13f27-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="13f27-116">Erreur « Référence d'objet non définie » lors de l'enregistrement d'une entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="13f27-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="13f27-117">L'importation des entrées de temps à partir des affectations de ressources crée des entrées de temps avec des valeurs DateHeure incorrectes.</span><span class="sxs-lookup"><span data-stu-id="13f27-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="13f27-118">Lorsque Project Service Automation et l'application Field Service sont toutes deux installés, le bouton **Nouveau** s'affiche deux fois sur la barre de commandes pour les entrées de temps dans l'application Field Service.</span><span class="sxs-lookup"><span data-stu-id="13f27-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="13f27-119">Les mises à jour des cellules **Autoriser unité** et **Groupe d’unités** fonctionnent désormais dans la grille **Estimations des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="13f27-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="13f27-120">Le formulaire **Mettre à jour l'entrée de temps Modifier** comprend **Chronologie**.</span><span class="sxs-lookup"><span data-stu-id="13f27-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="13f27-121">L'approbation du temps pour les entrées de temps hors projet bloque le système lors de la recherche d'un rôle d'approbateur de projet.</span><span class="sxs-lookup"><span data-stu-id="13f27-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="13f27-122">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="13f27-122">**Resource Management**</span></span>

<span data-ttu-id="13f27-123">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="13f27-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="13f27-124">Ajout de validation dans le plug-in **PostProjectCreate** pour vérifier une exigence principale avant d'en créer.</span><span class="sxs-lookup"><span data-stu-id="13f27-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="13f27-125">Le formulaire de création rapide **Membre de l'équipe de projet** lève une exception de référence nulle si des champs sont supprimés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="13f27-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="13f27-126">La génération d'exigences pendant 12 heures sur 1 an échouera.</span><span class="sxs-lookup"><span data-stu-id="13f27-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="13f27-127">Exception de référence nulle de message d'erreur améliorée lors de la création des besoins en ressources.</span><span class="sxs-lookup"><span data-stu-id="13f27-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="13f27-128">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="13f27-128">**Project Management**</span></span>

<span data-ttu-id="13f27-129">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="13f27-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="13f27-130">Amélioration de la validation pour traiter l'exception de référence nulle générée dans le plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="13f27-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="13f27-131">Les projets publiés par le complément de bureau Microsoft Project suppriment les affectations non attribuées.</span><span class="sxs-lookup"><span data-stu-id="13f27-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="13f27-132">Ajout d'une nouvelle validation lorsque la référence de projet d'une tâche n'est pas valide en raison d'une exception de référence nulle dans le plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="13f27-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="13f27-133">La grille Membre d'équipe n'affiche pas les affectations distinctes sur l'enregistrement des membres de l'équipe.</span><span class="sxs-lookup"><span data-stu-id="13f27-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="13f27-134">Ajout de nouveaux messages de validation et d'erreur en raison d'une exception de référence nulle dans le plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="13f27-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="13f27-135">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="13f27-135">**Sales**</span></span>

<span data-ttu-id="13f27-136">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="13f27-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="13f27-137">Lors de la sélection d'une ligne basée sur un projet dans un devis ou un contrat, le bouton **Suggestion** ne doit être visible que lors de la sélection d'une ligne basée sur un produit associée à un produit existant.</span><span class="sxs-lookup"><span data-stu-id="13f27-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="13f27-138">Split du privilège **Create_Product** à partir du privilège **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="13f27-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="13f27-139">La suppression d'une ligne de facture entraîne un échec de référence nul sur **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="13f27-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]