---
title: Nouveautés ou modifications de la mise à jour (version 18) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 18) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147200"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="951a4-103">Mise à jour (version 18) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="951a4-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="951a4-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="951a4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="951a4-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="951a4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="951a4-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="951a4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="951a4-107">Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="951a4-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="951a4-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="951a4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="951a4-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 18) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="951a4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="951a4-110">Cette version a le numéro de build V3.10.8.12 et est généralement disponible via une mise à jour automatique en avril 2020.</span><span class="sxs-lookup"><span data-stu-id="951a4-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="951a4-111">Mise à jour (version 18)</span><span class="sxs-lookup"><span data-stu-id="951a4-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="951a4-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="951a4-112">Bug fixes</span></span>

<span data-ttu-id="951a4-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="951a4-113">**Time and Expense**</span></span>

- <span data-ttu-id="951a4-114">Résolu : les flux **Rappeler**, **Demander** et **Annuler l’approbation** génèrent des exceptions avec des messages d’erreur peu explicites.</span><span class="sxs-lookup"><span data-stu-id="951a4-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="951a4-115">Résolu : lorsque le flux **Annuler l’approbation** échoue pour une dépense, une erreur d’exception pertinente n’est pas générée.</span><span class="sxs-lookup"><span data-stu-id="951a4-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="951a4-116">Résolu : la grille d’entrée de temps traite de manière incorrecte les jours non ouvrables en Australie après le passage à l’heure d’été en octobre.</span><span class="sxs-lookup"><span data-stu-id="951a4-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="951a4-117">Résolu : une logique par défaut incorrecte empêche la soumission des dépenses.</span><span class="sxs-lookup"><span data-stu-id="951a4-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="951a4-118">Résolu : en cas d’échec de l’approbation d’une entrée de temps, l’approbation reste à l’état **En attente**.</span><span class="sxs-lookup"><span data-stu-id="951a4-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="951a4-119">Résolu : erreurs SQL pour les approbations en bloc (blocage/expiration).</span><span class="sxs-lookup"><span data-stu-id="951a4-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="951a4-120">Résolu : problèmes de performances importants dans l’expérience utilisateur causés par la mise à jour des membres de l’équipe lors de l’approbation des entrées de temps.</span><span class="sxs-lookup"><span data-stu-id="951a4-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="951a4-121">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="951a4-121">**Project Management**</span></span>

- <span data-ttu-id="951a4-122">Résolu : la notification de fuseau horaire a été déplacée de la vue **Rapprochement** vers le formulaire principal **Projet**.</span><span class="sxs-lookup"><span data-stu-id="951a4-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="951a4-123">Résolu : le modèle de calendrier ne prend pas la valeur par défaut correcte lors de l’ouverture d’un nouveau formulaire de projet.</span><span class="sxs-lookup"><span data-stu-id="951a4-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="951a4-124">Résolu : pour les navigateurs basés sur Chrome, les utilisateurs ne peuvent pas sélectionner facilement des tâches prédécesseurs à supprimer.</span><span class="sxs-lookup"><span data-stu-id="951a4-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="951a4-125">Résolu : la création ou la copie d’un **Projet à partir d’un modèle vide** extrait des affectations non liées.</span><span class="sxs-lookup"><span data-stu-id="951a4-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="951a4-126">Résolu : dans des cas extrêmes spécifiques, la création d’une nouvelle affectation à partir de la grille des tâches entraîne la création d’enregistrements en double.</span><span class="sxs-lookup"><span data-stu-id="951a4-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="951a4-127">Résolu : en mode manuel, les utilisateurs ne peuvent pas mettre à jour les dates de début des tâches sur une valeur postérieure à la date actuelle enregistrée.</span><span class="sxs-lookup"><span data-stu-id="951a4-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="951a4-128">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="951a4-128">**Resource Management**</span></span>

- <span data-ttu-id="951a4-129">Résolu : la ligne du sous-total de la vue **Rapprochement** calcule de manière incorrecte l’écart des réservations après extension des réservations.</span><span class="sxs-lookup"><span data-stu-id="951a4-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="951a4-130">Résolu : la vue **Rapprochement** affiche de manière incorrecte les affectations de ressources lorsque la ressource réservable a un calendrier qui ne correspond pas au calendrier du projet.</span><span class="sxs-lookup"><span data-stu-id="951a4-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="951a4-131">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="951a4-131">**Sales**</span></span>

- <span data-ttu-id="951a4-132">Résolu : lorsque les entrées de temps sont réapprouvées (**Approuver > Annuler >** approuver à nouveau), une valeur réelle non facturable en double est créée.</span><span class="sxs-lookup"><span data-stu-id="951a4-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
