---
title: Créer un modèle d’heures de travail
description: Cette rubrique décrit la procédure de création d’un modèle d’heures de travail dans Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997193"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="e773a-103">Créer un modèle d’heures de travail (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e773a-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e773a-104">Pour créer et gérer un projet, vous devez appliquer un modèle de calendrier au projet.</span><span class="sxs-lookup"><span data-stu-id="e773a-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="e773a-105">Le modèle de calendrier définit les attributs de projet suivants :</span><span class="sxs-lookup"><span data-stu-id="e773a-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="e773a-106">Heures de travail, y compris l’heure de début et l’heure de fin</span><span class="sxs-lookup"><span data-stu-id="e773a-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="e773a-107">Jours de travail</span><span class="sxs-lookup"><span data-stu-id="e773a-107">Working days</span></span>
- <span data-ttu-id="e773a-108">Exceptions de calendrier, par exemple les jours non ouvrés</span><span class="sxs-lookup"><span data-stu-id="e773a-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="e773a-109">Le modèle de calendrier appliqué à un projet est une copie du modèle de calendrier défini dans les paramètres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e773a-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="e773a-110">Si vous modifiez le modèle de calendrier, ces modifications ne se propagent pas aux heures de travail du projet.</span><span class="sxs-lookup"><span data-stu-id="e773a-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="e773a-111">Pour modifier les heures de travail du projet, un nouveau modèle doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="e773a-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="e773a-112">Pour créer un modèle de calendrier pour votre organisation, il existe deux exigences clés :</span><span class="sxs-lookup"><span data-stu-id="e773a-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="e773a-113">Définissez les heures de travail souhaitées du modèle à l’aide d’une ressource réservable nouvelle ou existante.</span><span class="sxs-lookup"><span data-stu-id="e773a-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="e773a-114">Créez un nouveau modèle de calendrier et associez le modèle à la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="e773a-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="e773a-115">**Définir les heures de travail du modèle**</span><span class="sxs-lookup"><span data-stu-id="e773a-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="e773a-116">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="e773a-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="e773a-117">Créez une nouvelle ressource à référencer dans le modèle de calendrier ou sélectionnez une ressource existante.</span><span class="sxs-lookup"><span data-stu-id="e773a-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="e773a-118">Sélectionnez l’onglet **Heures de travail** de la ressource et suivez les instructions dans [Définition des heures de travail pour une ressource](/dynamics365/field-service/set-work-hours-resource.md) pour configurer les règles du calendrier.</span><span class="sxs-lookup"><span data-stu-id="e773a-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="e773a-119">**Créer un modèle de calendrier**</span><span class="sxs-lookup"><span data-stu-id="e773a-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="e773a-120">Accédez à **Paramètres** \> **Modèle de calendrier**.</span><span class="sxs-lookup"><span data-stu-id="e773a-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="e773a-121">Sélectionnez **Nouveau** et entrez un nom, une description et une ressource de modèle.</span><span class="sxs-lookup"><span data-stu-id="e773a-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="e773a-122">Lorsqu’une ressource est référencée dans un modèle de calendrier, une copie du calendrier de la ressource est associée au modèle de calendrier.</span><span class="sxs-lookup"><span data-stu-id="e773a-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="e773a-123">Si vous modifiez les heures de travail du modèle de calendrier, ces modifications ne se propagent pas au modèle de calendrier.</span><span class="sxs-lookup"><span data-stu-id="e773a-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="e773a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e773a-124">See Also</span></span>  
 [<span data-ttu-id="e773a-125">Configurer des ressources</span><span class="sxs-lookup"><span data-stu-id="e773a-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
