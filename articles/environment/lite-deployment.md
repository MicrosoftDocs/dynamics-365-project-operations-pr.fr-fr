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
# <a name="deploy-project-operations---lite"></a>Déployer Project Operations – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations prend en charge plusieurs modèles de déploiement. Pour déterminer le meilleur modèle de déploiement, voir [Types de déploiement](determine-deployment-type.md).


> [!IMPORTANT]
> Ce déploiement, Déploiement simplifié – Traiter la facturation pro forma, se traduit par un **déploiement Common Data Service uniquement de Project Operations**.

- [Installer Project Operations dans un nouvel environnement CDS](#new)
- [Installer dans un environnement CDS existant](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Installer Project Operations dans un nouvel environnement CDS

1. En tant qu’[administrateur général ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, créez un environnement CDS dans le [Centre d’administration PowerPlatform](https://admin.powerplatform.com). Assurez-vous que **Base de données CDS** et **Applications Dynamics 365** sont activés. Pour plus d’informations, voir [Créer et gérer des environnements dans le centre d’administration Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Sélectionner **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Installer Project Operations dans un environnement CDS existant

1. En tant qu’[administrateur général ou Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, localisez l’environnement dans le [centre d’administration PowerPlatform](https://admin.powerplatform.com) où vous souhaitez installer Project Operations.
2. Installez **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365. Pour plus d’informations, voir [Gérer les applications Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]