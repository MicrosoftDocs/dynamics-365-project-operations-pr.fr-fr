---
title: Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés
description: Cette rubrique fournit des informations sur la façon de s’abonner et de déployer des scénarios basés sur les ressource/non-stockés Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075626"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique explique comment souscrire à l’offre de version préliminaire/partenaire et déployer l’environnement Project Operations pour les scénarios basés sur les ressources/non stockés.

## <a name="prerequisites"></a>Conditions préalables

- Vous recevrez un e-mail vous invitant à participer à la version préliminaire. Vous pouvez demander une version préliminaire sur le [site web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure.
- Le déploiement d’un environnement Finance nécessite un abonnement Azure valide qui sera facturé par environnement. Vous pouvez utiliser l’abonnement existant de votre organisation ou utiliser un [Essai Azure](https://azure.microsoft.com/en-us/free/) pour commencer. L’environnement CDS sera fourni gratuitement pendant une période limitée de 30 jours.

## <a name="subscribe"></a>S'abonner

Lorsque vous recevez une approbation à votre [demande de version préliminaire](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), vous recevez trois offres de Microsoft par e-mail. Ces offres vous permettent de déployer la version préliminaire de Project Operations :

- Dynamics 365 Project Operations (CRM) – Version d’essai
- Office 365 Project Operations - Version d'essai
- Dynamics 365 Finance - Version d’essai

> [!IMPORTANT]
> Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Version d’essai 

Avant de commencer, assurez-vous que vous êtes connecté(e) à un navigateur avec le compte de travail de l'utilisateur dans le client où vous souhaitez la version préliminaire de Project Operations.

1. Utilisez le premier code promotionnel **Dynamics 365 Project Operations (CRM) - Version d'essai** en le collant dans l'URL du navigateur.

![Accepter l’offre](./media/16RedeemFirstOfferNew.png)

2. Confirmez votre commande.

![Confirmer la commande](./media/17ConfirmOrderNew.png)

Vous verrez la confirmation que l'offre a été utilisée avec succès.

![Confirmation](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Version d'essai

Répétez les mêmes étapes que pour le premier code d'offre. Assurez-vous d'ajouter le deuxième code d'offre en utilisant le même compte d'utilisateur que celui utilisé avec le premier code d'offre.

### <a name="dynamics-365-finance-preview-trial"></a>Version d’essai Dynamics 365 Finance

Répétez les mêmes étapes avec la dernière offre de l'e-mail de bienvenue.

## <a name="assign-licenses"></a>Attribuer des licences

> [!IMPORTANT]
> Vous aurez besoin d'un accès administratif au portail Microsoft 365 de votre organisation pour terminer les étapes suivantes.

1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.

![Page d’accueil du centre d’administration](./media/14AdminPortal.png)

2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.

![Attribuer des licences](./media/15AssignLicenses.png)

3. Vérifiez que les licences **Dynamics 365 Project Operations (CRM) - Version préliminaire** et **Office 365 Project Operations - Version préliminaire** ont été sélectionnées et sélectionnez **Enregistrer les modifications**.

> [!NOTE]
> L’offre d’essai Finance n’a pas besoin d’être attribuée à un utilisateur.

## <a name="start-a-new-project-in-lcs"></a>Commencer un nouveau projet dans LCS

Créez un projet LCS comme décrit dans la rubrique, [Démarrer un nouveau projet dans LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Ajouter un abonnement Azure à un projet LCS

Pour terminer cette tâche, suivez les étapes du sujet, [Ajouter un abonnement Azure au projet LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Déployer l’environnement de démonstration Finance avec Project Operations pour les scénarios basés sur des ressources/non stockés

Suivez les instructions de la rubrique [Mettre en service un nouvel environnement](resource-provision-new-environment.md) pour terminer le déploiement. Utilisez le type de déploiement [d’environnement de démonstration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pour la version préliminaire. 

## <a name="install-cds-setup-and-configuration-data"></a>Installer la configuration de la démonstration et les données de configuration CDS

Installez les données d’installation et de configuration CDS comme décrit dans la rubrique [Configurer et appliquer les données de configuration dans Common Data Service](resource-apply-pro-setup-config-data.md).
Effectuez cette étape uniquement après le déploiement de l'environnement de démonstration Finance et une fois que les données de démonstration dans FO sont prêtes.
