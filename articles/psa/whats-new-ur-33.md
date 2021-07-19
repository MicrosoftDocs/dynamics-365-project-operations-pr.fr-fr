---
title: Nouveautés ou modifications de la mise à jour (version 33) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 33) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334533"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="06348-103">Nouveautés ou modifications de la mise à jour (version 33) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="06348-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="06348-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="06348-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="06348-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="06348-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="06348-106">Elle est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="06348-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="06348-107">Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="06348-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="06348-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="06348-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="06348-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 33) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="06348-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="06348-110">Cette version a le numéro de build V3.10.54.98 et est généralement disponible par le biais d’une mise à jour automatique en juillet 2021.</span><span class="sxs-lookup"><span data-stu-id="06348-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="06348-111">Mise à jour (version 33)</span><span class="sxs-lookup"><span data-stu-id="06348-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="06348-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="06348-112">Bug fixes</span></span>

<span data-ttu-id="06348-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="06348-113">**Time and Expense**</span></span>

<span data-ttu-id="06348-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="06348-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="06348-115">Deux champs verrouillés, **msdyn_description** et **msdyn_externaldescription** sont modifiables après envoi.</span><span class="sxs-lookup"><span data-stu-id="06348-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="06348-116">Un message d’erreur s’affiche si une dépense est créée qui n’est pas liée à un projet.</span><span class="sxs-lookup"><span data-stu-id="06348-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="06348-117">Lorsqu’une entrée de temps est créée, le rôle de ressource est défini par défaut sur un rôle inactif.</span><span class="sxs-lookup"><span data-stu-id="06348-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="06348-118">Les lignes de journal associées à une dépense rappelée et supprimée ne sont pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="06348-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="06348-119">Dans le **Formulaire de création rapide d’entrée de temps**, mettez à jour la vue **Liste de tâches du projet** pour remplacer la date affichée par défaut par la date de début de la tâche.</span><span class="sxs-lookup"><span data-stu-id="06348-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="06348-120">Lorsque vous créez une entrée de temps dans l’onglet **Associé** de la ressource réservable, l’entrée de temps est créée de manière incorrecte pour l’utilisateur connecté au lieu de la ressource réservable parent.</span><span class="sxs-lookup"><span data-stu-id="06348-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="06348-121">De nouveaux champs sont ajoutés à la boîte de dialogue **MDD d’approbation en bloc**.</span><span class="sxs-lookup"><span data-stu-id="06348-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="06348-122">**Planification de projet**</span><span class="sxs-lookup"><span data-stu-id="06348-122">**Project planning**</span></span>

<span data-ttu-id="06348-123">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="06348-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="06348-124">Faibles performances de création de projets lorsque les modèles d’heures de travail du projet sont appliqués avec des calendriers complexes.</span><span class="sxs-lookup"><span data-stu-id="06348-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="06348-125">Lorsque la date de début est postérieure à la date de fin, une erreur s’affiche dans le modèle de copie de projet en raison des différences dans le composant de temps de chaque champ.</span><span class="sxs-lookup"><span data-stu-id="06348-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="06348-126">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="06348-126">**Resource management**</span></span>

<span data-ttu-id="06348-127">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="06348-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="06348-128">Un paramètre incorrect est utilisé dans la requête d’utilisation de ressources et le XML génère des résultats de filtre incorrects dans la grille **Utilisation de ressources**.</span><span class="sxs-lookup"><span data-stu-id="06348-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="06348-129">La confirmation **Étendre les réservations** affiche une date de fin incorrecte pour les réservations.</span><span class="sxs-lookup"><span data-stu-id="06348-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="06348-130">**Vente**</span><span class="sxs-lookup"><span data-stu-id="06348-130">**Sales**</span></span>

<span data-ttu-id="06348-131">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="06348-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="06348-132">Un message d’erreur s’affiche si un prix de catégorie est créé avec des valeurs manquantes.</span><span class="sxs-lookup"><span data-stu-id="06348-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="06348-133">Un message d’erreur s’affiche si un jalon de ligne de contrat est créé sans ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="06348-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
