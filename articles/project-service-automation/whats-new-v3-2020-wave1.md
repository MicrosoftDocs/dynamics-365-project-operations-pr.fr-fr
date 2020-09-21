---
title: Nouveautés ou modifications dans Project Service Automation version 3.x, 1e partie 2020
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3, 1e partie 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168044"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="54cd3-103">Nouveautés ou modifications dans Project Service Automation version 3, 1e partie 2020</span><span class="sxs-lookup"><span data-stu-id="54cd3-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="54cd3-104">La rubrique présente les principales considérations relatives à la mise à niveau vers la dernière version de Project Service Automation (PSA) version 3.x, 1e partie 2020.</span><span class="sxs-lookup"><span data-stu-id="54cd3-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="54cd3-105">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="54cd3-105">Time entry</span></span>
<span data-ttu-id="54cd3-106">L'expérience d'entrée de temps a été étendue pour offrir des fonctionnalités d'extension d'entrée de temps en scénarios clients.</span><span class="sxs-lookup"><span data-stu-id="54cd3-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="54cd3-107">Cela inclut la possibilité d'ajouter des types d'entrée, qui entraînent désormais un comportement spécifique basé sur le nom du schéma du champ **Paramètres d'entrée de temps**, affiché en tant que **Source de temps**.</span><span class="sxs-lookup"><span data-stu-id="54cd3-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="54cd3-108">Considération relative à la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="54cd3-108">Upgrade consideration</span></span>
<span data-ttu-id="54cd3-109">Pour prendre en charge cette fonctionnalité, les rôles dans PSA ont été mis à jour pour inclure de nouveaux privilèges.</span><span class="sxs-lookup"><span data-stu-id="54cd3-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="54cd3-110">Ces privilèges accordent un accès en lecture à la nouvelle entité, **Paramètres d'entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="54cd3-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="54cd3-111">Les utilisateurs qui doivent consigner le temps doivent disposer du rôle d'utilisateur **Utilisateur de l'entrée de temps**, en plus des rôles existants.</span><span class="sxs-lookup"><span data-stu-id="54cd3-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="54cd3-112">Ce rôle inclut la nouvelle fonctionnalité et garantit que l'entrée de temps continuera de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="54cd3-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="54cd3-113">Modifications d'entrée de temps actuellement étendues</span><span class="sxs-lookup"><span data-stu-id="54cd3-113">Currently extended time entry changes</span></span>
<span data-ttu-id="54cd3-114">Pour minimiser l'impact de l'entrée de temps sur les utilisateurs actuels, ce changement de rôle est la seule exigence nécessaire pour continuer à utiliser l'entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="54cd3-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="54cd3-115">Si vous avez créé des vues personnalisées ou des expériences d'entrée de temps distinctes, vous devez définir les champs **Paramètres d'entrée de temps** sur la valeur PSA correcte.</span><span class="sxs-lookup"><span data-stu-id="54cd3-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
