---
title: Nouveautés ou modifications de la mise à jour (version 29) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 29) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010468"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="30527-103">Nouveautés ou modifications de la mise à jour (version 29) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="30527-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="30527-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="30527-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="30527-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="30527-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="30527-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="30527-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="30527-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30527-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="30527-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="30527-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="30527-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 29) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="30527-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="30527-110">Cette version a un numéro de build V3.10.47.7 et est généralement disponible via une mise à jour automatique en février 2021.</span><span class="sxs-lookup"><span data-stu-id="30527-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="30527-111">Mise à jour (version 29)</span><span class="sxs-lookup"><span data-stu-id="30527-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="30527-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="30527-112">Bug fixes</span></span>

<span data-ttu-id="30527-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="30527-113">**Time and Expense**</span></span>

<span data-ttu-id="30527-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="30527-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="30527-115">Les utilisateurs ne peuvent pas voir les heures de travail enregistrées pendant les jours non ouvrables dans la grille d’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="30527-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="30527-116">Les entrées de dépenses approuvées peuvent être modifiées dans la grille.</span><span class="sxs-lookup"><span data-stu-id="30527-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="30527-117">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="30527-117">**Project Management**</span></span>

<span data-ttu-id="30527-118">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="30527-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="30527-119">Logique de validation manquante pour garantir que les heures d’effort d’attribution de ressources ne peuvent pas être négatives.</span><span class="sxs-lookup"><span data-stu-id="30527-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="30527-120">L’action personnalisée, **AssignResourcesForTask** met à jour tous les champs au lieu des champs modifiés uniquement.</span><span class="sxs-lookup"><span data-stu-id="30527-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="30527-121">Lors de la copie d’un projet dans un environnement avec des plug-ins ou des workflows enregistrés dans l’événement **CreateProject**, l’attribut **msdyn_bulkgenerationstatus** n’est pas mis à jour si **CopyWBSToProject** échoue.</span><span class="sxs-lookup"><span data-stu-id="30527-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="30527-122">Lorsque vous développez le calendrier du projet, les jours ouvrables ne sont pas triés dans l’ordre croissant, ce qui entraîne l’échec de certaines mises à jour de tâches du projet.</span><span class="sxs-lookup"><span data-stu-id="30527-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="30527-123">La modification du gestionnaire de projet dans un projet existant déclenche la logique par défaut de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="30527-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="30527-124">**Vente**</span><span class="sxs-lookup"><span data-stu-id="30527-124">**Sales**</span></span>

<span data-ttu-id="30527-125">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="30527-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="30527-126">L’onglet **Performance du contrat** sur la page **Contrat** échoue silencieusement pendant l’initialisation lorsqu’aucune ligne de contrat n’est présente.</span><span class="sxs-lookup"><span data-stu-id="30527-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>