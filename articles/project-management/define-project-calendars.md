---
title: Définir des calendriers de projet
description: Cette rubrique fournit des informations sur la façon d’appliquer un modèle de calendrier à un projet pour suivre la planification du projet.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981297"
---
# <a name="define-project-calendars"></a><span data-ttu-id="31702-103">Définir des calendriers de projet</span><span class="sxs-lookup"><span data-stu-id="31702-103">Define project calendars</span></span>

<span data-ttu-id="31702-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="31702-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31702-105">Pour créer et gérer un projet, vous devez appliquer un modèle de calendrier au projet.</span><span class="sxs-lookup"><span data-stu-id="31702-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="31702-106">Le modèle de calendrier définit les attributs de projet suivants :</span><span class="sxs-lookup"><span data-stu-id="31702-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="31702-107">Heures de travail, y compris l’heure de début et l’heure de fin</span><span class="sxs-lookup"><span data-stu-id="31702-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="31702-108">Jours de travail</span><span class="sxs-lookup"><span data-stu-id="31702-108">Working days</span></span>
- <span data-ttu-id="31702-109">Exceptions de calendrier, par exemple les jours non ouvrés</span><span class="sxs-lookup"><span data-stu-id="31702-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="31702-110">Le modèle de calendrier appliqué à un projet est une copie du modèle de calendrier défini dans les paramètres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31702-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="31702-111">Si vous modifiez le modèle de calendrier, ces modifications ne se propagent pas aux heures de travail du projet.</span><span class="sxs-lookup"><span data-stu-id="31702-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="31702-112">Pour modifier les heures de travail du projet, un nouveau modèle doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="31702-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="31702-113">Pour créer un modèle de calendrier pour votre organisation, il existe deux exigences clés :</span><span class="sxs-lookup"><span data-stu-id="31702-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="31702-114">Définissez les heures de travail souhaitées du modèle à l’aide d’une ressource réservable nouvelle ou existante.</span><span class="sxs-lookup"><span data-stu-id="31702-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="31702-115">Créez un nouveau modèle de calendrier et associez le modèle à la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="31702-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="31702-116">**Définir les heures de travail du modèle**</span><span class="sxs-lookup"><span data-stu-id="31702-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="31702-117">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="31702-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="31702-118">Créez une nouvelle ressource à référencer dans le modèle de calendrier ou sélectionnez une ressource existante.</span><span class="sxs-lookup"><span data-stu-id="31702-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="31702-119">Sélectionnez l’onglet **Heures de travail** de la ressource et suivez les instructions dans [Définition des heures de travail pour une ressource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) pour configurer les règles du calendrier.</span><span class="sxs-lookup"><span data-stu-id="31702-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="31702-120">**Créer un modèle de calendrier**</span><span class="sxs-lookup"><span data-stu-id="31702-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="31702-121">Accédez à **Paramètres** \> **Modèle de calendrier**.</span><span class="sxs-lookup"><span data-stu-id="31702-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="31702-122">Sélectionnez **Nouveau** et entrez un nom, une description et une ressource de modèle.</span><span class="sxs-lookup"><span data-stu-id="31702-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="31702-123">Lorsqu’une ressource est référencée dans un modèle de calendrier, une copie du calendrier de la ressource est associée au modèle de calendrier.</span><span class="sxs-lookup"><span data-stu-id="31702-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="31702-124">Si vous modifiez les heures de travail du modèle de calendrier, ces modifications ne se propagent pas au modèle de calendrier.</span><span class="sxs-lookup"><span data-stu-id="31702-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="31702-125">Vous pouvez désormais associer le modèle de travail à un modèle de calendrier de projet.</span><span class="sxs-lookup"><span data-stu-id="31702-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

