---
title: Déployer Project Operations – Simplifié
description: Cette rubrique fournit des informations sur la façon d’installer le déploiement simplifié de Project Operations – Traiter la facturation pro forma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642180"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="66f6d-103">Déployer Project Operations – Simplifié</span><span class="sxs-lookup"><span data-stu-id="66f6d-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="66f6d-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="66f6d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66f6d-105">Project Operations prend en charge plusieurs modèles de déploiement.</span><span class="sxs-lookup"><span data-stu-id="66f6d-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="66f6d-106">Pour déterminer le meilleur modèle de déploiement, voir [Types de déploiement](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="66f6d-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="66f6d-107">Ce déploiement, Déploiement simplifié – Traiter la facturation pro forma, se traduit par un **déploiement Common Data Service uniquement de Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="66f6d-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="66f6d-108">Installer Project Operations dans un nouvel environnement CDS</span><span class="sxs-lookup"><span data-stu-id="66f6d-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="66f6d-109">Installer dans un environnement CDS existant</span><span class="sxs-lookup"><span data-stu-id="66f6d-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="66f6d-110">Installer Project Operations dans un nouvel environnement CDS</span><span class="sxs-lookup"><span data-stu-id="66f6d-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="66f6d-111">En tant qu’[administrateur général ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, créez un environnement CDS dans le [Centre d’administration PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="66f6d-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="66f6d-112">Assurez-vous que **Base de données CDS** et **Applications Dynamics 365** sont activés.</span><span class="sxs-lookup"><span data-stu-id="66f6d-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="66f6d-113">Pour plus d’informations, voir [Créer et gérer des environnements dans le centre d’administration Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="66f6d-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="66f6d-114">Sélectionner **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66f6d-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="66f6d-115">Installer Project Operations dans un environnement CDS existant</span><span class="sxs-lookup"><span data-stu-id="66f6d-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="66f6d-116">En tant qu’[administrateur général ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, localisez l’environnement dans le [centre d’administration PowerPlatform](https://admin.powerplatform.com) où vous souhaitez installer Project Operations.</span><span class="sxs-lookup"><span data-stu-id="66f6d-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="66f6d-117">Installez **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66f6d-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="66f6d-118">Pour plus d’informations, voir [Gérer les applications Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="66f6d-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


