---
title: Souscrire un abonnement à la version préliminaire – Simplifié
description: Cette rubrique fournit des informations sur la façon de souscrire un abonnement et de déployer le scénario Déploiement simplifié de Project Operations – Opter pour la facturation pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587997"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Souscrire un abonnement à la version préliminaire – Simplifié 

Cette rubrique explique comment souscrire à l’offre d’évaluation et déployer le scénario Déploiement simplifié de Dynamics 365 Project Operations - Opter pour la facturation pro forma.

> [!NOTE]
> Ce processus changera dans les prochaines versions de Project Operations.

## <a name="prerequisites"></a>Conditions préalables
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure. Vous pouvez créer un client pendant la première acceptation de l’offre.

> [!IMPORTANT]
> Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.
> 
> Les évaluations sont à usage unique dans le client. Vous ne pouvez exécuter une évaluation qu’une seule fois. Nous vous recommandons de créer un nouveau client pour les besoins de l’évaluation.

### <a name="dynamics-365-project-operations-trial"></a>Évaluation de Dynamics 365 Project Operations 

Avant de commencer, assurez-vous que vous êtes connecté(e) à un navigateur avec le compte de travail de l’utilisateur dans le client où vous souhaitez la version préliminaire de Project Operations.

1. Accédez à [Évaluation de Project Operations](https://aka.ms/try-po) pour accepter le premier code d’offre, **Dynamics 365 Project Operations**.
2. Confirmez votre commande.

  Vous verrez que l’offre de confirmation a été acceptée avec succès.

## <a name="assign-licenses"></a>Attribuer des licences

> [!IMPORTANT]
> Vous aurez besoin d’un accès administratif au portail Microsoft 365 de votre organisation pour terminer les étapes suivantes.


1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.
2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.
3. Vérifiez que la licence **Dynamics 365 Project Operations** est sélectionnée. 
4. Sélectionnez **Enregistrer les modifications**.

## <a name="create-a-new-dataverse-environment"></a>Créez un environnement Dataverse

1. Mettez en service un nouvel environnement de déploiement de Project Operations Dataverse en suivant les instructions de la rubrique, [Modèle de déploiement Dataverse](lite-deployment.md). Lorsque vous sélectionnez le type d’environnement, assurez-vous d’utiliser la **Version d’essai (basé sur un abonnement)**.

  ![Nouvel environnement.](./media/19CreateEnvironment.png)

2. Sélectionnez le paramètre **Activer les applications Dynamics 365**, puis laissez **Déployer automatiquement ces applications** vide.  
3. Sélectionnez **Enregistrer** pour créer l’environnement.

  ![Ajoutez une base de données.](./media/20CreateEnvironment1.png)

4. Une fois l’environnement créé, installez la solution **Microsoft Dynamics 365 Project Operations**. 

![Installez la solution.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installez une configuration CDS et des données de démonstration de configuration

Installez la configuration CDS et configurez les données de démonstration en suivant les instructions de la rubrique [Appliquer la configuration de démonstration et les données de configuration](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
