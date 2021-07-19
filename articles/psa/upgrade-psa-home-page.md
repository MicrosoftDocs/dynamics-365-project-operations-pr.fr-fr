---
title: Mettre à niveau la page d’accueil
description: Cette rubrique décrit où trouver des informations importantes concernant les fonctionnalités nouvelles et modifiées dans Dynamics 365 Project Service Automation, ainsi que le processus de mise à niveau vers la nouvelle version.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8fc820d8fa0e421cdc963f391133e7311de96982
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368518"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="84929-103">Mettre à niveau la page d’accueil</span><span class="sxs-lookup"><span data-stu-id="84929-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="84929-104">Mise à niveau de PSA version 2.x ou 1.x vers la version 3.x</span><span class="sxs-lookup"><span data-stu-id="84929-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="84929-105">Nouvelles instances</span><span class="sxs-lookup"><span data-stu-id="84929-105">New instances</span></span>

<span data-ttu-id="84929-106">À compter du 17 mai 2019, lorsque Project Service Automation est sélectionnée pendant la mise en service d’une nouvelle instance, la version 3.x est installée par défaut.</span><span class="sxs-lookup"><span data-stu-id="84929-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="84929-107">Instances existantes</span><span class="sxs-lookup"><span data-stu-id="84929-107">Existing instances</span></span>

<span data-ttu-id="84929-108">Auparavant, les clients qui disposent d’une instance de PSA version 2.x et devaient effectuer une mise à niveau vers la version 3.x, qui est la version basée sur l’interface Unified Client (UCI) de PSA, devaient contacter Support Microsoft et fournir les détails de leur instance, afin que le support puisse activer l’instance pour la mise à niveau vers la version 3.x.</span><span class="sxs-lookup"><span data-stu-id="84929-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="84929-109">À compter du 1er mars 2020, les clients qui disposent d’une instance de PSA version 2.x et doivent passer à la version 3.x, pourront mettre à niveau leurs instances directement à partir du portail d’administration sans avoir à contacter le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84929-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="84929-110">PSA version 3.x comprend des modifications importantes.</span><span class="sxs-lookup"><span data-stu-id="84929-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="84929-111">Elle est bâtie sur la structure Unified Interface pour offrir une expérience utilisateur améliorée.</span><span class="sxs-lookup"><span data-stu-id="84929-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="84929-112">L’application modifiée offre une interface utilisateur cohérente et uniforme et elle applique les principes de conception réactive pour un affichage optimal sur n’importe quelle taille d’écran ou n’importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="84929-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="84929-113">D’autres modifications ont été apportées dans l’application.</span><span class="sxs-lookup"><span data-stu-id="84929-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="84929-114">Parmi les zones qui ont été modifiées, on peut citer la tarification, la réservation et l’affectation de ressources, le temps, les dépenses et les approbations.</span><span class="sxs-lookup"><span data-stu-id="84929-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="84929-115">Avant de commencer le processus de mise à niveau, nous vous recommandons d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="84929-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="84929-116">Vérifiez si Dynamics 365 Field Service et Project Service Automation sont installées sur l’instance identifiée.</span><span class="sxs-lookup"><span data-stu-id="84929-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="84929-117">Si les deux solutions sont installées, vous devez prévoir de les mettre à niveau toutes les deux avant de recommencer à utiliser normalement l’instance.</span><span class="sxs-lookup"><span data-stu-id="84929-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="84929-118">Examinez attentivement les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="84929-118">Carefully review the following topics.</span></span> <span data-ttu-id="84929-119">Prendre connaissance et comprendre les modifications entre les versions vous aideront dans le processus de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="84929-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="84929-120">Ces rubriques donnent des informations sur les modifications majeures dans PSA, ainsi que les considérations et les recommandations pour la planification de votre mise à niveau vers la version 3.x.</span><span class="sxs-lookup"><span data-stu-id="84929-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="84929-121">Nouveautés ou modifications dans Project Service Automation version 3</span><span class="sxs-lookup"><span data-stu-id="84929-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="84929-122">Considérations relatives à la mise à niveau - Project Service Automation version 2.x ou 1.x vers la version 3.x</span><span class="sxs-lookup"><span data-stu-id="84929-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="84929-123">Mettez à niveau votre instance sandbox pour évaluer les modifications de votre implémentation avant de mettre à niveau votre instance de production.</span><span class="sxs-lookup"><span data-stu-id="84929-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="84929-124">Une fois que vous avez examiné les rubriques précédemment mentionnées et que vous êtes prêt à effectuer une mise à niveau vers PSA version 3.x ou la version basée sur UCI, envoyez une demande au Support Microsoft pour rendre la mise à niveau accessible à partir du Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="84929-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="84929-125">Dans votre demande, fournissez les détails de votre instance.</span><span class="sxs-lookup"><span data-stu-id="84929-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="84929-126">Anciennes versions de PSA (PSA version 2.x) dans une nouvelle instance créée</span><span class="sxs-lookup"><span data-stu-id="84929-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="84929-127">À compter du 17 mai 2019, toutes les nouvelles instances ont UCI comme client par défaut.</span><span class="sxs-lookup"><span data-stu-id="84929-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="84929-128">Afin de s’aligner sur cette modification, PSA version 3.x and Field Service version 8.x seront mises en service par défaut, car ces versions sont conçues pour fonctionner avec le client UCI.</span><span class="sxs-lookup"><span data-stu-id="84929-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="84929-129">À partir du 1er mars 2020, les clients de Dynamics PSA ne pourront plus créer un environnement avec des versions antérieures de PSA, par exemple PSA version 2.x ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="84929-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="84929-130">Tout nouvel environnement devra obtenir uniquement la version 3.x de PSA.</span><span class="sxs-lookup"><span data-stu-id="84929-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="84929-131">Pour optimiser l’expérience lorsque vous utilisez les anciennes versions des applications Field Service et PSA, accédez à la page **Paramètres système** et pour le champ, **Utiliser uniquement la nouvelle Unified Interface (recommandé)**, sélectionnez **Non**, car ces versions ne sont pas conçues pour être chargées correctement dans UCI.</span><span class="sxs-lookup"><span data-stu-id="84929-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="84929-132">Après avoir désactivé UCI, vous pouvez ouvrir et exécuter ces versions de Field Service et de PSA en utilisant l’ancien client Web.</span><span class="sxs-lookup"><span data-stu-id="84929-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]