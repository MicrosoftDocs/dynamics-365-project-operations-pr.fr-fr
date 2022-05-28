---
title: Déployer Project Operations – Simplifié
description: Cette rubrique fournit des informations sur la façon d’installer le déploiement simplifié de Project Operations – Traiter la facturation pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580729"
---
# <a name="deploy-project-operations---lite"></a>Déployer Project Operations – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_



Project Operations prend en charge plusieurs modèles de déploiement. Pour déterminer le meilleur modèle de déploiement, voir [Types de déploiement](determine-deployment-type.md).


> [!IMPORTANT]
> Ce déploiement, Déploiement simplifié – Traiter la facturation pro forma, se traduit par un **déploiement Dataverse uniquement de Project Operations**.

- [Installer Project Operations dans un nouvel environnement Dataverse](#new)
- [Installer dans un environnement Dataverse existant](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations dans un nouvel environnement Dataverse

1. En tant qu’[Administrateur général ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, créez un environnement Dataverse dans le [Centre d’administration PowerPlatform](https://admin.powerplatform.com). Veillez à ce que **Créer une base de données pour cet environnement** et **Applications Dynamics 365** soient activées. Pour plus d’informations, voir [Créer et gérer des environnements dans le centre d’administration Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Sélectionner **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations dans un environnement Dataverse existant
1. Veillez à ce que l’environnement n’ait pas été configuré avec la [double écriture](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), car l’installation installera alors les fonctionnalités [Project Operations pour les scénarios basés sur les ressources/produits non stockés](project-operations-integrated-deployment-overview.md).
2. En tant qu’[administrateur général ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, localisez l’environnement dans le [centre d’administration PowerPlatform](https://admin.powerplatform.com) où vous souhaitez installer Project Operations.
3. Installez **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365. Pour plus d’informations, voir [Gérer les applications Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
