---
title: Nouveautés ou modifications de la mise à jour (version 14) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 14) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124815"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="f5e07-103">Mise à jour (version 14) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="f5e07-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="f5e07-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f5e07-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f5e07-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f5e07-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f5e07-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f5e07-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f5e07-107">Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f5e07-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f5e07-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f5e07-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f5e07-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 14) de PSA V3.</span><span class="sxs-lookup"><span data-stu-id="f5e07-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="f5e07-110">Cette version a le numéro de build V3.10.4.21 et est disponible selon le calendrier suivant :</span><span class="sxs-lookup"><span data-stu-id="f5e07-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="f5e07-111">**Disponibilité générale (mise à jour automatique) :** janvier 2020</span><span class="sxs-lookup"><span data-stu-id="f5e07-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="f5e07-112">**Mise à jour automatique :** février 2020</span><span class="sxs-lookup"><span data-stu-id="f5e07-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="f5e07-113">Mise à jour (version 14)</span><span class="sxs-lookup"><span data-stu-id="f5e07-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="f5e07-114">Améliorations</span><span class="sxs-lookup"><span data-stu-id="f5e07-114">Enhancements</span></span>

- <span data-ttu-id="f5e07-115">Ventes</span><span class="sxs-lookup"><span data-stu-id="f5e07-115">Sales</span></span>

     - <span data-ttu-id="f5e07-116">Les valeurs de champ personnalisées dans **Détails de la ligne de devis** sont copiées dans **Détails de la ligne de contrat du projet** lorsqu’un devis est mis à jour sur **Fermé comme conclu**.</span><span class="sxs-lookup"><span data-stu-id="f5e07-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="f5e07-117">Les projets confirmés peuvent être **Fermés comme perdus**.</span><span class="sxs-lookup"><span data-stu-id="f5e07-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="f5e07-118">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="f5e07-118">Resource Management</span></span>

     - <span data-ttu-id="f5e07-119">Lors de l’extension des réservations, les utilisateurs seront invités par le biais d’une boîte de dialogue de confirmation à résumer les résultats de la réservation et à fournir un lien vers la fonctionnalité Gérer les réservations.</span><span class="sxs-lookup"><span data-stu-id="f5e07-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="f5e07-120">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="f5e07-120">Bug fixes</span></span>

- <span data-ttu-id="f5e07-121">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="f5e07-121">Time and Expense</span></span>

     - <span data-ttu-id="f5e07-122">Correction : amélioration de l’expérience utilisateur lorsque l’utilisateur n’a sélectionné aucune entrée à corriger.</span><span class="sxs-lookup"><span data-stu-id="f5e07-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="f5e07-123">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="f5e07-123">Resource Management</span></span>

     - <span data-ttu-id="f5e07-124">Correction : la réservation d’une ressource à plusieurs reprises remplace le nom de la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="f5e07-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="f5e07-125">Ventes</span><span class="sxs-lookup"><span data-stu-id="f5e07-125">Sales</span></span>

     - <span data-ttu-id="f5e07-126">Correction : le prix de vente total n’est calculé que lorsque l’utilisateur entre également un prix de revient pour les estimations de dépenses d’un projet.</span><span class="sxs-lookup"><span data-stu-id="f5e07-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="f5e07-127">Correction : la fermeture d’un devis comme **Conclu** échoue si le contrat de projet associé n’est pas à l’état **Brouillon**.</span><span class="sxs-lookup"><span data-stu-id="f5e07-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

