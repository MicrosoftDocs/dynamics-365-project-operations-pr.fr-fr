---
title: Nouveautés ou modifications de la mise à jour (version 28) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 28) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150620"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="fa60c-103">Nouveautés ou modifications de la mise à jour (version 28) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="fa60c-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fa60c-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fa60c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fa60c-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="fa60c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fa60c-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fa60c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fa60c-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fa60c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fa60c-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fa60c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fa60c-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour Project Service Automation V3, Version mise à jour 28. Cette version possède le numéro de build V3.10.46.32 et est à disposition générale via une mise à jour autonome effectuée en janvier 2021.</span><span class="sxs-lookup"><span data-stu-id="fa60c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="fa60c-110">Mise à jour (version 28)</span><span class="sxs-lookup"><span data-stu-id="fa60c-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fa60c-111">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="fa60c-111">Bug fixes</span></span>

<span data-ttu-id="fa60c-112">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="fa60c-112">**Time and Expense**</span></span>

<span data-ttu-id="fa60c-113">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="fa60c-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="fa60c-114">Les utilisateurs peuvent utiliser **Modification groupée** pour mettre à jour les entrées de temps qui ont été approuvées et soumises.</span><span class="sxs-lookup"><span data-stu-id="fa60c-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="fa60c-115">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="fa60c-115">**Project Management**</span></span>

<span data-ttu-id="fa60c-116">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="fa60c-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="fa60c-117">Dans les cas où le GUID de la tâche est interprété comme un nombre, les tâches ne peuvent pas être ouvertes pour modification à l'aide de **Modifier la tâche** dans le ruban sur la page **Structure de répartition du travail**.</span><span class="sxs-lookup"><span data-stu-id="fa60c-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="fa60c-118">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="fa60c-118">**Sales**</span></span>

<span data-ttu-id="fa60c-119">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="fa60c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="fa60c-120">Une exception de référence nulle est générée lorsque le plug-in **GetEstimatesForProject** est appelé.</span><span class="sxs-lookup"><span data-stu-id="fa60c-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="fa60c-121">**Marquer prêt à facturer** sur la grille des jalons ne met à jour que partiellement les attributs, sauf pour l'attribut **InvoiceStatus**, qui est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fa60c-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

