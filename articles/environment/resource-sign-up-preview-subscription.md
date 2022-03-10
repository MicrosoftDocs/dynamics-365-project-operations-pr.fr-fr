---
title: Souscrire des abonnements à la version préliminaire de Project Operations pour les scénarios de ressources/hors stock
description: Cette rubrique fournit des informations sur la façon de souscrire un abonnement et de déployer des scénarios basés sur les ressources/hors stock Project Operations.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f47d5a29c0e40a49aed7b3e52c5d52a9c27b8dbc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323413"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Souscrire des abonnements à la version préliminaire de Project Operations pour les scénarios de ressources/hors stock

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Cette rubrique explique comment souscrire à l’offre d’évaluation et déployer l’environnement Project Operations pour les scénarios basés sur des ressources/hors stock.

## <a name="prerequisites"></a>Conditions préalables
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure. Vous pouvez créer un client pendant la première acceptation de l’offre. 
- Le déploiement d’un environnement Finance nécessite un abonnement Azure valide qui sera facturé par environnement. Vous pouvez utiliser l’abonnement existant de votre organisation ou utiliser un [Essai Azure](https://azure.microsoft.com/free/) pour commencer. L’environnement CDS sera fourni gratuitement pendant une période limitée de 30 jours.

> [!IMPORTANT]
> Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.
> 
> Les évaluations sont à usage unique dans le client. Vous ne pouvez exécuter une évaluation qu’une seule fois. Nous vous recommandons de créer un nouveau client pour les besoins de l’évaluation.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Essai en version préliminaire 

Avant de commencer, assurez-vous que vous êtes connecté(e) à un navigateur avec le compte de travail de l’utilisateur dans le client où vous souhaitez la version préliminaire de Project Operations.

1. Acceptez le premier code de l’offre, **Dynamics 365 Project Operations** ici [Évaluation de Project Operations](https://aka.ms/try-po).
2. Confirmez votre commande.

  Vous verrez la confirmation que l’offre a été utilisée avec succès.

### <a name="dynamics-365-finance-preview-trial"></a>Essai en version préliminaire de Dynamics 365 Finance

Accédez à [Essai en version préliminaire de Dynamics 365 for Finance](https://aka.ms/trypoche) et répétez les étapes de la section précédente avec l’offre, S’inscrire pour accéder à l’environnement hébergé dans le cloud.  

## <a name="assign-licenses"></a>Attribuer des licences

> [!IMPORTANT]
> Vous aurez besoin d’un accès administratif au portail Microsoft 365 de votre organisation pour terminer les étapes suivantes.

1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.

2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.

3. Vérifiez que la licence **Dynamics 365 Project Operations** a été sélectionnée et sélectionnez **Enregistrer les modifications**.

> [!NOTE]
> L’offre d’essai Finance n’a pas besoin d’être attribuée à un utilisateur.

## <a name="start-a-new-project-in-lcs"></a>Commencer un nouveau projet dans LCS

Créez un projet LCS comme décrit dans la rubrique, [Démarrer un nouveau projet dans LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Ajouter un abonnement Azure à un projet LCS

Pour terminer cette tâche, suivez les étapes du sujet, [Ajouter un abonnement Azure au projet LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Déployer l’environnement de démonstration Finance avec Project Operations pour les scénarios basés sur des ressources/hors stock

Suivez les instructions de la rubrique [Mettre en service un nouvel environnement](resource-provision-new-environment.md) pour terminer le déploiement. Utilisez le type de déploiement [d’environnement de démonstration](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pour la version préliminaire. 

## <a name="install-cds-setup-and-configuration-data"></a>Installer la configuration de la démonstration et les données de configuration CDS

Installez les données d’installation et de configuration CDS comme décrit dans la rubrique [Configurer et appliquer les données de configuration dans Common Data Service](resource-apply-pro-setup-config-data.md).
N’effectuez cette étape qu’une fois que l’environnement de démonstration de Finance est déployé et que les données de démonstration sont prêtes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
