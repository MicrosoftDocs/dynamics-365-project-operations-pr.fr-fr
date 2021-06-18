---
title: Nouveautés ou modifications dans Project Service Automation version 3.x, 1e partie 2020
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3, 1e partie 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996833"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="23e64-103">Nouveautés ou modifications dans Project Service Automation version 3, 1e partie 2020</span><span class="sxs-lookup"><span data-stu-id="23e64-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="23e64-104">La rubrique présente les principales considérations relatives à la mise à niveau vers la dernière version de Project Service Automation (PSA) version 3.x, 1e partie 2020.</span><span class="sxs-lookup"><span data-stu-id="23e64-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="23e64-105">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="23e64-105">Time entry</span></span>
<span data-ttu-id="23e64-106">L’expérience d’entrée de temps a été étendue pour offrir des fonctionnalités d’extension d’entrée de temps en scénarios clients.</span><span class="sxs-lookup"><span data-stu-id="23e64-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="23e64-107">Cela inclut la possibilité d’ajouter des types d’entrée, qui entraînent désormais un comportement spécifique basé sur le nom du schéma du champ **Paramètres d’entrée de temps**, affiché en tant que **Source de temps**.</span><span class="sxs-lookup"><span data-stu-id="23e64-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="23e64-108">Une nouvelle solution appelée Temps, dépense, statut et approbations (TESA) a été ajoutée pour prendre en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="23e64-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="23e64-109">Considération relative à la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="23e64-109">Upgrade consideration</span></span>
<span data-ttu-id="23e64-110">Pour prendre en charge cette fonctionnalité, les rôles dans PSA ont été mis à jour pour inclure de nouveaux privilèges.</span><span class="sxs-lookup"><span data-stu-id="23e64-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="23e64-111">Ces privilèges accordent un accès en lecture à la nouvelle entité, **Paramètres d’entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="23e64-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="23e64-112">Les utilisateurs qui doivent consigner le temps doivent disposer du rôle d’utilisateur **Utilisateur de l’entrée de temps**, en plus des rôles existants.</span><span class="sxs-lookup"><span data-stu-id="23e64-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="23e64-113">Ce rôle inclut la nouvelle fonctionnalité et garantit que l’entrée de temps continuera de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="23e64-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="23e64-114">En outre, si vous avez des modules d’application personnalisés incluant tous les formulaires de l’entité Entrée de temps, vous devrez supprimer le **Formulaire de création rapide d’entrée de temps TESA** du module.</span><span class="sxs-lookup"><span data-stu-id="23e64-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="23e64-115">Modifications d’entrée de temps actuellement étendues</span><span class="sxs-lookup"><span data-stu-id="23e64-115">Currently extended time entry changes</span></span>
<span data-ttu-id="23e64-116">Pour minimiser l’impact de l’entrée de temps sur les utilisateurs actuels, ce changement de rôle est la seule exigence nécessaire pour continuer à utiliser l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="23e64-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="23e64-117">Si vous avez créé des vues personnalisées ou des expériences d’entrée de temps distinctes, vous devez définir les champs **Paramètres d’entrée de temps** sur la valeur PSA correcte.</span><span class="sxs-lookup"><span data-stu-id="23e64-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]