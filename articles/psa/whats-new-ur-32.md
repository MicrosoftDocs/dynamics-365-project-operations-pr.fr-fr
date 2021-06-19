---
title: Nouveautés ou modifications de la mise à jour (version 32) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 32) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129663"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="2fd6e-103">Nouveautés ou modifications de la mise à jour (version 32) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="2fd6e-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2fd6e-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="2fd6e-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2fd6e-106">Elle est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2fd6e-107">Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="2fd6e-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2fd6e-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 32) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="2fd6e-110">Cette version porte le numéro de build V3.10.53.108 et est généralement disponible via une mise à jour automatique en juin 2021.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="2fd6e-111">Mise à jour (version 32)</span><span class="sxs-lookup"><span data-stu-id="2fd6e-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2fd6e-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="2fd6e-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="2fd6e-113">GÉNÉRAL</span><span class="sxs-lookup"><span data-stu-id="2fd6e-113">General</span></span>

- <span data-ttu-id="2fd6e-114">Lorsqu’une mise à niveau majeure échoue, seuls les principaux points d’entrée de l’application doivent être bloqués, afin de garantir que les entités partagées sont toujours accessibles.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="2fd6e-115">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="2fd6e-115">Time and Expense</span></span>

<span data-ttu-id="2fd6e-116">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="2fd6e-117">**TimeEntriesImportFromResourceAssignment** ne conserve pas les heures de début et de fin des secteurs de profil de l’affectation des ressources.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="2fd6e-118">Lorsque vous sélectionnez **Ouvrir l’entrée** dans la grille **Entrée de temps**, vous pouvez être empêché de sélectionner d’autres formulaires.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="2fd6e-119">Pendant que vous importez des affectations dans des entrées de temps, la requête de code client peut générer une longue URL qui fait échouer la requête.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="2fd6e-120">Dans la grille **Entrée de temps**, après la suppression d’une valeur d’une cellule, le focus ne reste pas dans la grille.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="2fd6e-121">Le bouton **Rejeter** a été retiré de la vue **Traitement des approbations** pour les approbations modernes.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="2fd6e-122">La stabilité et les performances de l’approbation en bloc des entrées de temps sont affectées par des blocages et l’incapacité à gérer correctement les personnalisations liées à l’entité **Entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="2fd6e-123">Planification de projet</span><span class="sxs-lookup"><span data-stu-id="2fd6e-123">Project Planning</span></span>

- <span data-ttu-id="2fd6e-124">Une exception de référence Null est générée lorsque vous mettez à jour un projet qui a une valeur Null dans le champ **Unité contractuelle**.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="2fd6e-125">**Actualiser les totaux du projet** calcule incorrectement le coût restant et les ventes restantes sur un projet.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="2fd6e-126">Des calculs de tarification redondants affectent les performances liées aux mises à jour des profils d’affectation des ressources.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="2fd6e-127">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="2fd6e-127">Resource Management</span></span>

<span data-ttu-id="2fd6e-128">L’incident suivant a été résolu :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="2fd6e-129">Lorsque la capacité de calendrier d’une ressource réservable est supérieure à 1, Project Service Automation reconnaît à tort la capacité comme 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2fd6e-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="2fd6e-130">Par conséquent, une boucle infinie se produit dans la vue de planification.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="2fd6e-131">Vente</span><span class="sxs-lookup"><span data-stu-id="2fd6e-131">Sales</span></span>

<span data-ttu-id="2fd6e-132">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="2fd6e-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="2fd6e-133">Lorsqu’une ligne de journal est créée avec un type de transaction personnalisé, l’exception de référence Null suivante se produit : *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="2fd6e-134">Les rôles et catégories qui sont désactivés avant la copie d’un devis ne doivent pas être ajoutés aux rôles et catégories facturables du devis nouvellement copié.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="2fd6e-135">La date du document et la date comptable ne sont pas alignées avec la date de début qui est indiquée sur un détail de ligne de facture créé directement sur une facture provisoire.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="2fd6e-136">Des exceptions de référence Null sont générées dans les scénarios liés à l’inactivation de rôles et de catégories avant la copie d’un devis.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="2fd6e-137">L’action **Mettre à jour les prix** de la page **Projets** ne met pas à jour les estimations de dépenses et les estimations du matériel.</span><span class="sxs-lookup"><span data-stu-id="2fd6e-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
