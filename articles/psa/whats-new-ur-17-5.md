---
title: Nouveautés ou modifications de la mise à jour (version 17.5) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 17.5) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075695"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="5ae83-103">Mise à jour (version 17.5) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="5ae83-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="5ae83-104">Nous sommes heureux d'annoncer la dernière mise à jour de l'application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5ae83-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5ae83-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="5ae83-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="5ae83-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5ae83-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5ae83-107">Pour effectuer une mise à jour vers cette version, visitez le centre d'administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5ae83-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5ae83-108">Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5ae83-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5ae83-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 17.5), V3.</span><span class="sxs-lookup"><span data-stu-id="5ae83-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="5ae83-110">Cette version a le numéro de build V3.10.7.32 et sera disponible partout par mise à jour automatique en mars 2020.</span><span class="sxs-lookup"><span data-stu-id="5ae83-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="5ae83-111">Mise à jour (version 17.5)</span><span class="sxs-lookup"><span data-stu-id="5ae83-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5ae83-112">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="5ae83-112">Bug fixes</span></span>


<span data-ttu-id="5ae83-113">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="5ae83-113">**Project Management**</span></span>

- <span data-ttu-id="5ae83-114">Résolu : Résolution des problèmes de synchronisation côté serveur qui se produisent avec les tâches de longue durée.</span><span class="sxs-lookup"><span data-stu-id="5ae83-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="5ae83-115">Résolu : Modèles d'heure de travail sur 24 heures modifiés, car un jour supplémentaire était ajouté aux tâches de manière inexacte.</span><span class="sxs-lookup"><span data-stu-id="5ae83-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="5ae83-116">Résolu : Modèles d'heures de travail +13 GMT modifiés, car des tâches étaient décalées un jour à l'avance de manière inexacte.</span><span class="sxs-lookup"><span data-stu-id="5ae83-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>
