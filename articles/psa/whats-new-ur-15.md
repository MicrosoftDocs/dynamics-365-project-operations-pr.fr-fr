---
title: Nouveautés ou modifications de la mise à jour (version 15) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 15) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949316"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="5c2c7-103">Mise à jour (version 15) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="5c2c7-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5c2c7-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="5c2c7-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="5c2c7-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5c2c7-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5c2c7-107">Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="5c2c7-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5c2c7-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5c2c7-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 15) de PSA V3.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="5c2c7-110">Cette version a le numéro de build V3.10.5.28 et est généralement disponible par mise à jour automatique en janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="5c2c7-111">Mise à jour (version 15)</span><span class="sxs-lookup"><span data-stu-id="5c2c7-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="5c2c7-112">Améliorations</span><span class="sxs-lookup"><span data-stu-id="5c2c7-112">Enhancements</span></span>

- <span data-ttu-id="5c2c7-113">Gestion du projet</span><span class="sxs-lookup"><span data-stu-id="5c2c7-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5c2c7-114">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="5c2c7-114">Bug fixes</span></span>

- <span data-ttu-id="5c2c7-115">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="5c2c7-115">Time and Expense</span></span>

  - <span data-ttu-id="5c2c7-116">Correction : ajoutez la gestion des erreurs de chargement dans la vue Rapprochement.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="5c2c7-117">Correction : centre des ressources du projet : renommez **Montant** pour réduire l’ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="5c2c7-118">Correction : ajustez la vue **Copier les colonnes d’entrée de temps** pour inclure le type.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="5c2c7-119">Correction : la modification de la durée de l’entrée de temps dans la vue grille à l’aide de nombres décimaux entraîne une erreur inconnue pour certains nombres.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="5c2c7-120">Gestion du projet</span><span class="sxs-lookup"><span data-stu-id="5c2c7-120">Project Management</span></span>

  - <span data-ttu-id="5c2c7-121">Correction : le menu déroulant pour **Utiliser en mode Suivi** se développe désormais en fonction de la largeur des options.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="5c2c7-122">Correction : lors de la gestion de projets dans le fuseau horaire +13, les calculs des tâches peuvent afficher des résultats inexacts.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="5c2c7-123">Correction : l’option **Heure de fin du membre de l’équipe** a été corrigée lors de l’utilisation d’un calendrier de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="5c2c7-124">Correction : réactivez le **BPF** dans le formulaire principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="5c2c7-125">Correction : le calcul des affectations n’ignore plus un jour.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="5c2c7-126">Correction : une nouvelle bannière de notification a été ajoutée au formulaire de projet lorsque le fuseau horaire diffère entre l’utilisateur et le projet.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="5c2c7-127">Ventes</span><span class="sxs-lookup"><span data-stu-id="5c2c7-127">Sales</span></span>

  - <span data-ttu-id="5c2c7-128">Correction : la recherche de catégorie d’estimation des dépenses peut être utilisée pour filtrer les doublons.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="5c2c7-129">Correction : le code dans **PluginDomain.ExecuteInTryCatchBlock(..)** ne cache plus l’origine de l’exception.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="5c2c7-130">Correction : un message d’erreur ne s’affiche plus dans **Recherche de projet** dans le formulaire **Ligne de devis** lorsqu’il y a plus de 1000 projets.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="5c2c7-131">Correction : la grille **Estimations** pour les estimations de main-d’œuvre et les estimations de dépense affiche désormais le symbole de devise correct.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="5c2c7-132">Correction : une fois qu’une organisation met à jour PSA de la version 14 vers la version 15, l’onglet **Planning** n’apparaît plus comme vide dans le formulaire **Projet**.</span><span class="sxs-lookup"><span data-stu-id="5c2c7-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]