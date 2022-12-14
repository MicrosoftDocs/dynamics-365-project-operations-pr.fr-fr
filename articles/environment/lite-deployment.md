---
title: Déployer Project Operations – Simplifié
description: Cet article fournit des informations sur la façon d’installer Déploiement simplifié – Opter pour la facturation pro forma de Project Operations.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810975"
---
# <a name="deploy-project-operations-lite"></a>Déployer Project Operations – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_



Project Operations prend en charge plusieurs modèles de déploiement. Pour déterminer le meilleur modèle de déploiement, voir [Types de déploiement](determine-deployment-type.md).


> [!IMPORTANT]
> Ce déploiement, Déploiement simplifié – Traiter la facturation pro forma, se traduit par un **déploiement Dataverse uniquement de Project Operations**.

- [Installer Project Operations dans un nouvel environnement Dataverse](#new)
- [Installer dans un environnement Dataverse existant](#existing)
- [Installer dans un environnement Dataverse existant avec composants à double écriture](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations Simplifié dans un nouvel environnement Dataverse

1. En tant qu’[Administrateur général ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, créez un environnement Dataverse dans le [Centre d’administration PowerPlatform](https://admin.powerplatform.com). Veillez à ce que **Créer une base de données pour cet environnement** et **Applications Dynamics 365** soient activées. Pour plus d’informations, voir [Créer et gérer des environnements dans le centre d’administration Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Sélectionner **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations Simplifié dans un environnement Dataverse existant 
1. En tant qu’[administrateur général ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, localisez l’environnement dans le [centre d’administration PowerPlatform](https://admin.powerplatform.com) où vous souhaitez installer Project Operations.
1. Installez **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365. Pour plus d’informations, voir [Gérer les applications Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installer Project Operations Simplifié dans un environnement Dataverse existant où des solutions à double écriture sont déjà présentes

Si vous souhaitez continuer à exécuter Project Operations en mode déploiement simplifié, vous devez suivre ces étapes :

1. En tant qu’[administrateur général ou Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) avec une licence Project Operations, localisez l’environnement dans le [centre d’administration PowerPlatform](https://admin.powerplatform.com) où vous souhaitez installer Project Operations.
1. Installez **Microsoft Dynamics 365 Project Operations** à partir de la liste de déploiement des applications Dynamics 365. Pour plus d’informations, voir [Gérer les applications Dynamics 365](/power-platform/admin/manage-apps).
1. Étant donné que votre environnement comporte des composants à double écriture qui facilitent l’intégration aux applications de finances et d’opérations installées, l’installation de Project Operations installe également les fonctionnalités et les extensions requises pour intégrer les données liées au projet aux applications de finances et d’opérations. Étant donné que vous souhaitez exécuter Project Operations en mode déploiement simplifié, ces composants d’intégration doivent être supprimés, car ils créent des restrictions et une surcharge pour les scénarios de déploiement simplifié. Désinstallez manuellement les solutions **Double écriture Dynamics 365 Project Operations** et **Mappages d’entité en double écriture Dynamics 365 Project Operations** pour supprimer ces composants.
1. Accédez à **Project Operations -> Réglages -> Paramètres**. Ouvrez la page détaillée **Paramètre du projet** et définissez le champ **Comportement de mise à niveau de la solution** sur **Simplifié uniquement**. Cela garantit que les mises à niveau ultérieures de Project Operations ne ramèneront pas les composants d’intégration dans Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
