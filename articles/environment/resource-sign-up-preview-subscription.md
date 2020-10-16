---
title: Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés
description: Cette rubrique fournit des informations sur la façon de s’abonner et de déployer des scénarios basés sur les ressource/non-stockés Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948852"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Inscrivez-vous aux abonnements aux versions préliminaires de Project Operations pour les scénarios de ressources/non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique explique comment souscrire à l’offre de version préliminaire/partenaire et déployer l’environnement Project Operations pour les scénarios basés sur les ressources/non stockés.

## <a name="prerequisites"></a>Conditions préalables

- Vous recevrez un e-mail vous invitant à participer à la version préliminaire. Vous pouvez demander une version préliminaire sur le [site web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure.
- Le déploiement d’un environnement Finance nécessite un abonnement Azure valide qui sera facturé par environnement. Vous pouvez utiliser l’abonnement existant de votre organisation ou utiliser un [Essai Azure](https://azure.microsoft.com/en-us/free/) pour commencer. L’environnement CDS sera fourni gratuitement pendant une période limitée de 30 jours.

## <a name="subscribe"></a>S’abonner

Lorsque vous recevez une approbation à votre [demande de version préliminaire](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), vous recevez deux offres de Microsoft par e-mail. Ces offres vous permettent de déployer la version préliminaire de Project Operations :

- Dynamics 365 Project Operations – Version d’essai
- Version d’essai Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Version d’essai

1. Utilisez la première offre, **version d’essai Dynamics 365 Project Operations**, avec l’URL fournie dans votre e-mail de bienvenue.

![Première offre](./media/1FirstOffer.png)

2. Vérifiez que vous êtes connecté en tant qu’utilisateur appartenant à l’organisation qui s’abonnera au service.
3. Continuez à utiliser l’offre. 
4. Sélectionnez **Oui, ajoutez-le à mon compte**.

![Accepter l’offre](./media/2RedeemFirstOffer.png)

![Confirmer l’offre](./media/3ConfirmFirstOffer.png)

![Offre utilisée](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Version d’essai Dynamics 365 Finance

Répétez les mêmes étapes avec la deuxième offre de l’e-mail de bienvenue.

## <a name="assign-licenses"></a>Attribuer des licences

> [!IMPORTANT]
> Vous aurez besoin d’un accès administratif au portail Office 365 de votre organisation pour terminer les étapes suivantes.

1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.

![Portail d’administration d’Office](./media/5OfficeAdminPortal.png)

2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.

![Attribuer des licences](./media/6AssignLicenses.png)

3. Vérifiez que la licence Project Operations a été sélectionnée et sélectionnez **Enregistrer les modifications**. 

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

