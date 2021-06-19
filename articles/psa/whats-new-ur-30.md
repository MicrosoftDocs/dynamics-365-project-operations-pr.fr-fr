---
title: Nouveautés ou modifications de la mise à jour (version 30) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 30) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010423"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="7828d-103">Nouveautés ou modifications de la mise à jour (version 30) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="7828d-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7828d-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7828d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7828d-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7828d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7828d-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7828d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7828d-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7828d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7828d-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="7828d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="7828d-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 30) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="7828d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="7828d-110">Cette version a le numéro de build V3.10.51.61 et est généralement disponible via une mise à jour automatique en avril 2021.</span><span class="sxs-lookup"><span data-stu-id="7828d-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="7828d-111">Mise à jour (version 30)</span><span class="sxs-lookup"><span data-stu-id="7828d-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7828d-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="7828d-112">Bug fixes</span></span>

<span data-ttu-id="7828d-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="7828d-113">**Time and Expense**</span></span>

<span data-ttu-id="7828d-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="7828d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="7828d-115">Une erreur se produit lorsque vous créez et enregistrez une entrée de temps sur la page **Création rapide** si le champ **Rôle** est supprimé.</span><span class="sxs-lookup"><span data-stu-id="7828d-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="7828d-116">Le filtre Entrée de temps applique l’opérateur de filtre incorrect.</span><span class="sxs-lookup"><span data-stu-id="7828d-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="7828d-117">Les feuilles de temps copiées ne s’affichent pas automatiquement lorsque vous sélectionnez **Copier la semaine** sur le contrôle d’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="7828d-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="7828d-118">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="7828d-118">**Resource Management**</span></span>

<span data-ttu-id="7828d-119">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="7828d-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="7828d-120">Lorsque vous prolongez une réservation, le statut de réservation attribué à la réservation ferme est incorrect.</span><span class="sxs-lookup"><span data-stu-id="7828d-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="7828d-121">La prolongation d’une réservation respecte le statut de réservation défini comme **Engagé** dans les métadonnées de configuration de la réservation.</span><span class="sxs-lookup"><span data-stu-id="7828d-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="7828d-122">Lorsqu’aucun statut de réservation valide n’est spécifié, le message d’erreur n’est pas correctement localisé.</span><span class="sxs-lookup"><span data-stu-id="7828d-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="7828d-123">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="7828d-123">**Project Management**</span></span>

<span data-ttu-id="7828d-124">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="7828d-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="7828d-125">Les projets ne peuvent pas être créés dans une devise et inclure des tâches associées dans une autre devise.</span><span class="sxs-lookup"><span data-stu-id="7828d-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="7828d-126">**Vente**</span><span class="sxs-lookup"><span data-stu-id="7828d-126">**Sales**</span></span>

<span data-ttu-id="7828d-127">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="7828d-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="7828d-128">Lorsqu’un tarif est copié, les prix ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7828d-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="7828d-129">La clôture d’un devis avec le statut Conclu échoue lorsque le détail du coût a une valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="7828d-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="7828d-130">Sur l’entité **Tâche du projet**, le nom **Coût estimé** a été remplacé par **Coût prévu (base)**.</span><span class="sxs-lookup"><span data-stu-id="7828d-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="7828d-131">Une exception de référence nulle est générée lorsque les factures sont créées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="7828d-131">A null reference exception is generated when invoices are created or deleted.</span></span>
