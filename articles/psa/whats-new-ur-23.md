---
title: Nouveautés ou modifications de la mise à jour (version 23) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 23) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150035"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="76850-103">Mise à jour (version 23) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="76850-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="76850-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="76850-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="76850-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="76850-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="76850-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="76850-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="76850-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="76850-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="76850-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="76850-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="76850-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 23) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="76850-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="76850-110">Cette version a le numéro de build V3.10.34.30 et est généralement disponible par mise à jour automatique en août 2020.</span><span class="sxs-lookup"><span data-stu-id="76850-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="76850-111">Mise à jour (version 23)</span><span class="sxs-lookup"><span data-stu-id="76850-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="76850-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="76850-112">Bug fixes</span></span>

<span data-ttu-id="76850-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="76850-113">**Time and Expense**</span></span>

<span data-ttu-id="76850-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="76850-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="76850-115">Gérer le cas limite dans **Supprimer membre de l’équipe de projet** pour fournir une exception significative.</span><span class="sxs-lookup"><span data-stu-id="76850-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="76850-116">L’importation des affectations entraîne un écran de suppression vide.</span><span class="sxs-lookup"><span data-stu-id="76850-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="76850-117">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="76850-117">**Resource Management**</span></span>

<span data-ttu-id="76850-118">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="76850-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="76850-119">La **carte des ressources de grille d’utilisation des ressources** présente des données incorrectes lorsque l’échelle de temps est supérieure à cinq jours.</span><span class="sxs-lookup"><span data-stu-id="76850-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="76850-120">Lorsque les clients créent une ressource réservable, le plug-in échoue par intermittence à ajouter automatiquement la ressource à un groupe Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="76850-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="76850-121">La vue **Rapprochement** n’affiche pas correctement les contours manuels dans la vue **Semaine** ou **Mois**.</span><span class="sxs-lookup"><span data-stu-id="76850-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="76850-122">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="76850-122">**Project Management**</span></span>

<span data-ttu-id="76850-123">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="76850-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="76850-124">Un nombre excessif d’entités **Récupération multiple pour les paramètres de l’utilisateur** entraîne une dégradation des performances des approbations de projet et d’autres opérations.</span><span class="sxs-lookup"><span data-stu-id="76850-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="76850-125">La recherche de ressources de grille **Planification des tâches** est limitée pour n’afficher qu’un maximum de cinq membres de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="76850-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="76850-126">La recherche de ressources de grille **Planification des tâches** ne filtre pas les ressources inactives.</span><span class="sxs-lookup"><span data-stu-id="76850-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="76850-127">Le mode manuel ne fonctionne pas comme prévu dans la structure de répartition du travail de planification de projet.</span><span class="sxs-lookup"><span data-stu-id="76850-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="76850-128">La grille **Planification des tâches** affiche **Catégories de transactions inactives**.</span><span class="sxs-lookup"><span data-stu-id="76850-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="76850-129">La grille **Affectation des ressources** ne s’arrondit pas correctement lorsqu’une tâche a plusieurs affectations.</span><span class="sxs-lookup"><span data-stu-id="76850-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="76850-130">Les valeurs d’arrondi sont différentes entre le coût planifié et le coût réel pour une seule tâche.</span><span class="sxs-lookup"><span data-stu-id="76850-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="76850-131">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="76850-131">**Sales**</span></span>

<span data-ttu-id="76850-132">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="76850-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="76850-133">Le fait de double-cliquer sur **Récupérer toutes les catégories de transactions** crée plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="76850-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
