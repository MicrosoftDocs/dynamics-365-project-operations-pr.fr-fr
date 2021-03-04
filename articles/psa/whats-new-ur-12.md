---
title: Nouveautés ou modifications de la mise à jour (version 12) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 12) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143825"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="34c40-103">Mise à jour (version 12) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="34c40-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="34c40-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="34c40-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="34c40-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="34c40-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="34c40-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="34c40-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="34c40-107">Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="34c40-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="34c40-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="34c40-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="34c40-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 12) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="34c40-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="34c40-110">Cette version a le numéro de build V3.10.2.34 et est généralement disponible par mise à jour automatique en octobre 2019.</span><span class="sxs-lookup"><span data-stu-id="34c40-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="34c40-111">Mise à jour (version 12)</span><span class="sxs-lookup"><span data-stu-id="34c40-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="34c40-112">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="34c40-112">Bug fixes</span></span>

- <span data-ttu-id="34c40-113">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="34c40-113">Time and Expense</span></span>

    - <span data-ttu-id="34c40-114">Correction : les messages d’erreur d’entrée de temps ont été mis à jour avec un contexte plus pertinent.</span><span class="sxs-lookup"><span data-stu-id="34c40-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="34c40-115">Correction : la grille d’entrée de temps et le planning affichent correctement la barre de défilement verticale lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="34c40-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="34c40-116">Correction : les entrées de dépenses et de temps envoyées peuvent être approuvées.</span><span class="sxs-lookup"><span data-stu-id="34c40-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="34c40-117">Correction : le message de la boîte de dialogue de confirmation de l’annulation de l’approbation a été corrigé pour refléter le statut de l’approbation lorsqu’il passe de **Approuvé** à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="34c40-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="34c40-118">Correction : les champs **Prix**, **Unité** et **Quantité** sont désormais verrouillés sur l’enregistrement de dépenses une fois qu’il a été approuvé.</span><span class="sxs-lookup"><span data-stu-id="34c40-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="34c40-119">Gestion du projet</span><span class="sxs-lookup"><span data-stu-id="34c40-119">Project Management</span></span>

    - <span data-ttu-id="34c40-120">Correction : l’action **Nouveau** sur le formulaire principal **Membre de l’équipe** a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="34c40-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="34c40-121">Correction : les affectations de ressources ont été mises à jour pour tenir compte des erreurs d’arrondi inexact, qui entraînent un changement dans la date de fin d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="34c40-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="34c40-122">Correction : dans la grille des tâches, les erreurs côté serveur pertinentes seront signalées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="34c40-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="34c40-123">Correction : le nom du membre de l’équipe s’affiche désormais dans le sélecteur de personnes au lieu du nom du poste.</span><span class="sxs-lookup"><span data-stu-id="34c40-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="34c40-124">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="34c40-124">Resource Management</span></span>

    - <span data-ttu-id="34c40-125">Correction : les détails des ressources requises pour les projets créés à partir d’un modèle utilisent désormais le calendrier du projet.</span><span class="sxs-lookup"><span data-stu-id="34c40-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="34c40-126">Correction : les qualifications et les compétences affichent désormais par défaut les ressources requises créées pour le rôle au lieu des données de référence du rôle.</span><span class="sxs-lookup"><span data-stu-id="34c40-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="34c40-127">Ventes</span><span class="sxs-lookup"><span data-stu-id="34c40-127">Sales</span></span>

    - <span data-ttu-id="34c40-128">Correction : ID d’objet en double trouvés sur le formulaire principal **Contrat**.</span><span class="sxs-lookup"><span data-stu-id="34c40-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="34c40-129">Correction : la logique a été mise à jour pour rendre l’onglet **Analyse du devis** visible afin d’afficher la configuration des métadonnées de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="34c40-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="34c40-130">Correction : la date comptable de l’enregistrement réel provient désormais de la date de l’entrée de temps/dépenses au lieu de la date de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="34c40-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
