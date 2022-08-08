---
title: Déployer manuellement l’application Project Operations Dataverse avec prise en charge de la double écriture
description: Cet article explique comment déployer manuellement l’application Project Operations Dataverse afin qu’elle prenne en charge la double écriture.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a25e2a59f1c069057c6689825ce52b13d842af71
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028561"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Déployer manuellement l’application Project Operations Dataverse avec prise en charge de la double écriture

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article explique comment déployer manuellement Microsoft Dynamics 365 Project Operations dans Microsoft Dataverse afin qu’elle prenne en charge la double écriture. Project Operations détecte la configuration de l’environnement et ajoute une prise en charge supplémentaire pour la double écriture si les conditions préalables sont remplies.

Pendant le déploiement à travers Microsoft Dynamics Lifecycle Services (LCS), si vous avez suivi les instructions de cet article, vous pouvez ignorer le déploiement de l’intégration Microsoft Power Platform (anciennement connue sous le nom d’environnement Common Data Service).

Le processus de déploiement de Project Operations dans Dataverse pour qu’il prenne en charge la double écriture comporte quatre étapes principales :

1. [Créer un nouvel environnement dans Dataverse qui prend en charge la double écriture](#create).
2. [Ajouter les conditions préalables de la double écriture à l’environnement](#prerequisites).
3. [Ajouter l’application Project Operations Dataverse](#dataverse).
4. [Lier vos environnements](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Créer un nouvel environnement dans Dataverse qui prend en charge la double écriture

Pour effectuer cette procédure, vous devez vous connecter en tant qu’administrateur.

1. Ouvrez le [Centre d’administration de Power Platform](https://admin.powerplatform.com) et connectez-vous en tant qu’administrateur.
2. Créez un nouvel environnement et nommez-le.
3. Sélectionnez le type d’environnement. Si vous avez souscrit à l’offre d’évaluation, sélectionnez **Évaluation (basée sur l’abonnement)**.
4. Confirmez la région de déploiement.
5. Activez l’option **Créer une base de données pour cet environnement**. 
6. Confirmez la langue, puis confirmez que la devise correspond à la devise de vos applications de finances et d’opérations.
7. Activez l’option **Applications Dynamics 365** et confirmez que le champ **Déployer automatiquement ces applications** est défini sur **Aucun**.
8. Ajoutez un groupe de sécurité, si cela est nécessaire.
9. Sélectionnez **Enregistrer** pour créer l’environnement.
10. Attendez que le déploiement soit terminé et que l’environnement atteigne l’état **Prêt**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Ajouter les conditions préalables de la double écriture à l’environnement

La prise en charge de la double écriture comprend des champs supplémentaires qui sont ajoutés aux entités clés, telles que l’entité **Société**. Si vous ajoutez la prise en charge de la double écriture à un environnement existant, vous devrez peut-être mettre à jour les données pour activer la prise en charge. Pour plus d’informations sur l’amorçage des données, consultez [Amorcer les données de la société](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Pour plus d’informations sur la double écriture, consultez [Configuration système requise pour la double écriture](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Effectuez cette procédure pour ajouter les conditions préalables de la double écriture à votre environnement.

1. Ouvrez l’environnement que vous venez de créer, puis accédez à **Ressource** \> **Applications Dynamics 365**.
2. Sélectionnez **Solution principale de double écriture** dans la liste des applications et installez-la.
3. Attendez que l’installation soit terminée. Sélectionnez ensuite **Solution d’orchestration de l’application de double écriture** dans la liste des applications et installez-la.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Ajouter l’application Project Operations Dataverse

Vous pouvez effectuer cette procédure uniquement si vous avez effectué les procédures précédentes avant d’installer Project Operations. Pendant l’installation, le système analyse la configuration de l’environnement et ajoute la prise en charge de la double écriture si nécessaire.

1. Ouvrez l’environnement que vous avez créé précédemment, puis accédez à **Ressource** \> **Applications Dynamics 365**.
2. Sélectionnez **Microsoft Dynamics 365 Project Operations** dans la liste des applications et installez-la.

## <a name="link-your-environments"></a><a name="link"></a>Lier vos environnements

Une fois l’environnement Dataverse déployé, vous pouvez configurer le lien dans vos applications de finances et d’opérations. Suivez les étapes décrites dans [Utiliser l’Assistant de double écriture pour lier vos environnements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
