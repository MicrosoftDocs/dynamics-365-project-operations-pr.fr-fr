---
title: S’inscrire à l’abonnement à la version préliminaire – Simplifié
description: Cette rubrique fournit des informations sur la façon de souscrire et de déployer le déploiement simplifié de Project Operations – Traiter la facturation pro forma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175888"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>S’inscrire à l’abonnement à la version préliminaire – Simplifié 

Cette rubrique explique des informations sur la façon de souscrire à l’offre de version préliminaire du partenaire et de déployer Dynamics 365 Project Operations Déploiement simplifié – Traiter la facturation pro forma.

> [!NOTE]
> Ce processus changera dans les prochaines versions de Project Operations.

## <a name="prerequisites"></a>Conditions préalables

- Vous recevrez un e-mail vous invitant à participer à la version préliminaire. Vous pouvez demander une version préliminaire sur le [site web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure.
- Passez en revue tous les termes et conditions.

## <a name="subscribe"></a>S’abonner

Lorsque vous recevez une approbation d’une [demande de version préliminaire](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), vous recevez deux offres de Microsoft par e-mail. Ces offres vous permettent de déployer la version préliminaire de Project Operations :

- Dynamics 365 Project Operations (CRM) – Version d’essai
- Office 365 Project Operations - Version d’essai

> [!IMPORTANT]
> Une seule personne, l’administrateur du client, dans une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Version d’essai 

Avant de commencer, assurez-vous que vous êtes connecté(e) à un navigateur avec le compte de travail de l’utilisateur dans le client où vous souhaitez la version préliminaire de Project Operations.

1. Utilisez le premier code promotionnel **Dynamics 365 Project Operations (CRM) - Version d’essai** en le collant dans l’URL du navigateur.

![Accepter l’offre](./media/16RedeemFirstOfferNew.png)

2. Confirmez votre commande.
![Confirmer la commande](./media/17ConfirmOrderNew.png)

Vous verrez la confirmation que l’offre a été utilisée avec succès.

![Confirmation](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Version d’essai

Répétez les mêmes étapes que pour le premier code d’offre. Assurez-vous d’ajouter le deuxième code d’offre en utilisant le même compte d’utilisateur que celui utilisé avec le premier code d’offre.

## <a name="assign-licenses"></a>Attribuer des licences

> [!IMPORTANT]
> Vous aurez besoin d’un accès administratif au portail Microsoft 365 de votre organisation pour terminer les étapes suivantes.


1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.

![Page d’accueil du centre d’administration](./media/14AdminPortal.png)

2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.

![Attribuer des licences](./media/15AssignLicenses.png)

3. Vérifiez que les licences **Dynamics 365 Project Operations (CRM) - Version préliminaire** et **Office 365 Project Operations - Version préliminaire** sont sélectionnées. 
4. Sélectionnez **Enregistrer les modifications**.

## <a name="create-a-new-cds-environment"></a>Créer un environnement CDS

1. Mettez en service un nouvel environnement de déploiement CDS Project Operations en suivant les instructions de la rubrique [Modèle de déploiement CDS](lite-deployment.md). Lorsque vous sélectionnez le type d’environnement, assurez-vous d’utiliser la **Version d’essai (basé sur un abonnement)**.
![Nouvel environnement](./media/19CreateEnvironment.png)

2. Sélectionnez le paramètre **Activer les applications Dynamics 365**, puis laissez **Déployer automatiquement ces applications** vide.  
3. Sélectionnez **Enregistrer** pour créer l’environnement.

![Ajouter une base de données](./media/20CreateEnvironment1.png)

4. Une fois l’environnement créé, installez la solution **Microsoft Dynamics 365 Project Operations**. 

![Installer la solution](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installez une configuration CDS et des données de démonstration de configuration

Installez la configuration CDS et configurez les données de démonstration en suivant les instructions de la rubrique [Appliquer la configuration de démonstration et les données de configuration](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]