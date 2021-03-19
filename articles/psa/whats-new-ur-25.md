---
title: Nouveautés ou modifications de la mise à jour (version 25) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 25) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280440"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="197a4-103">Nouveautés ou modifications de la mise à jour (version 25) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="197a4-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="197a4-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="197a4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="197a4-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="197a4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="197a4-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="197a4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="197a4-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="197a4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="197a4-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="197a4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="197a4-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour Project Service Automation V3, Version mise à jour 25. Cette version possède le numéro de build V 3.10.43.76 et est à disposition générale via une mise à jour autonome effectuée en octobre 2020.</span><span class="sxs-lookup"><span data-stu-id="197a4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="197a4-110">Mise à jour (version 25)</span><span class="sxs-lookup"><span data-stu-id="197a4-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="197a4-111">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="197a4-111">Bug fixes</span></span>

<span data-ttu-id="197a4-112">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="197a4-112">**Time and Expense**</span></span>

<span data-ttu-id="197a4-113">L’incident suivant a été résolu :</span><span class="sxs-lookup"><span data-stu-id="197a4-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="197a4-114">Graphique d’entrées de temps comportant des données supplémentaires basées sur un intervalle trop grand en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="197a4-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="197a4-115">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="197a4-115">**Resource Management**</span></span>

<span data-ttu-id="197a4-116">L’incident suivant a été résolu :</span><span class="sxs-lookup"><span data-stu-id="197a4-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="197a4-117">Ajout d’un code Package Deployer pour ignorer l’importation du dispositif Universal Resource Scheduling si un dispositif de version ultérieure existe déjà.</span><span class="sxs-lookup"><span data-stu-id="197a4-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="197a4-118">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="197a4-118">**Project Management**</span></span>

<span data-ttu-id="197a4-119">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="197a4-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="197a4-120">Correction des écarts d’arrondi et de taux de change entraînant un coût prévisionnel incorrect dans la grille de suivi du projet.</span><span class="sxs-lookup"><span data-stu-id="197a4-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="197a4-121">Prend en charge la possibilité d’afficher deux ou plusieurs grilles de réaction sur le formulaire **Projet**.</span><span class="sxs-lookup"><span data-stu-id="197a4-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="197a4-122">Fourniture de validation pour traiter la possibilité d’attribuer une tâche après la date de fin du calendrier, ce qui génère un échec d’affectation de ressources.</span><span class="sxs-lookup"><span data-stu-id="197a4-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="197a4-123">Amélioration de la gestion des erreurs pour résoudre l’exception de référence null générée à partir des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="197a4-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="197a4-124">Plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="197a4-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="197a4-125">**PreValidateProjectTaskCreate** lorsqu’une tâche de projet est créée sans projet associé</span><span class="sxs-lookup"><span data-stu-id="197a4-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="197a4-126">Plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="197a4-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="197a4-127">Plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="197a4-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="197a4-128">Plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="197a4-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="197a4-129">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="197a4-129">**Sales**</span></span>

<span data-ttu-id="197a4-130">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="197a4-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="197a4-131">Amélioration de la gestion des erreurs pour résoudre les exceptions de référence null générées à partir de **Copier le projet : Gestion des estimations HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="197a4-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="197a4-132">**Non prêt pour la facturation** sur une **Réplication de facturation pour le temps et le matériel** n’efface pas le statut de facturation.</span><span class="sxs-lookup"><span data-stu-id="197a4-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="197a4-133">Correction de l’étiquetage des boutons **Prix** dans les onglets **Prix du rôle** et **Articles de catalogue**.</span><span class="sxs-lookup"><span data-stu-id="197a4-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]