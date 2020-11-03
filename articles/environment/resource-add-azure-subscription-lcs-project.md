---
title: Ajouter un abonnement Azure au projet LCS
description: Cette rubrique fournit des informations sur la connexion de votre abonnement Azure à un projet LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075611"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Ajouter un abonnement Azure au projet LCS

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les environnements hébergés dans le cloud doivent être déployés à l’aide d’un abonnement Azure existant. Cette rubrique explique comment connecter votre abonnement Azure existant à un projet LCS. 

## <a name="grant-admin-consent"></a>Accorder un consentement d’administrateur

1. Dans votre projet LCS, dans la section **Environnements** , sélectionnez **Paramètres Microsoft Azure**.

![Paramètres de l’application Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Sur la page **Paramètres du projet** , sur l’onglet **Connecteurs Azure** , sélectionnez **Autoriser**. Cela permet aux environnements d’être déployés dans ce projet.

![Connecteurs Azure](./media/2AzureConnectors.png)

3. Sélectionnez **Autoriser** à nouveau pour donner le consentement de l’administrateur.

![Accorder un consentement d’administrateur](./media/3GrantAdminConsent.png)

4. Acceptez la demande d’autorisation.

![Accepter la demande d’autorisation](./media/4AcceptPermissionRequest.png)

L’autorisation est maintenant terminée. 

![Autorisation réussie](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fournissez l’accès à Dynamics Deployment Services à votre abonnement Azure

1. Accédez à [Facturation Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) et sélectionnez votre abonnement. Dynamics Deployment Services doit accéder à cet abonnement pour pouvoir déployer des environnements.

![Détails de l’abonnement Azure](./media/6AzureSubscription.png)

2. Sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation, puis sélectionnez **Ajouter une attribution de rôle**.
3. Dans le curseur sur le côté droit, sélectionnez **Rôle Contributeur** , et dans la liste fournie, recherchez et sélectionnez **Dynamics Deployment Services**. 
4. Sélectionnez **Enregistrer**.

![Accès à l’abonnement](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Ajouter un connecteur d’abonnement à un projet LCS

1. Dans votre projet LCS, sur la page **Paramètres Microsoft Azure** , sélectionnez **Ajouter** pour ajouter un nouveau connecteur.
2. Entrer votre ID d’abonnement Azure. Vous pouvez trouver votre ID d’abonnement Azure dans le [portail Azure](https://ms.portal.azure.com/), sous **Paramètres** en bas à gauche de l’écran.
3. Dans le champ **Configurer pour utiliser Azure Resource Manager** , sélectionnez **Oui**.
4. Assurez-vous que le domaine du client AAD d’abonnement d’Azure correspond à l’abonnement Azure propriétaire du domaine que vous utilisez, puis sélectionnez **Suivant**.
5. Sur l’écran **Configuration Microsoft Azure** , sélectionnez **Suivant** pour confirmer. Si vous recevez une erreur sur cet écran, revenez à la section [Fournir l’accès à Dynamics Deployment Services à l’abonnement Azure](#provide) dans cette rubrique et assurez-vous que vous avez terminé toutes les étapes.
6. Téléchargez le certificat de gestion Azure dans un dossier local sur votre ordinateur, puis chargez-le sur le Portail de gestion Azure en accédant à **Paramètres** > **Certificats de gestion**. Ce certificat permettra à LCS de communiquer avec Azure en votre nom. Vous pouvez ignorer cette étape si votre utilisateur a accès à l’abonnement.
7. Cliquez sur **Suivant**.
8. Sélectionnez la région Azure dans laquelle déployer et sélectionnez un centre de données proche de l’endroit où vous prévoyez d’utiliser ce système.
9.  Cliquez sur **Se connecter**.

Vous avez connecté avec succès votre abonnement Azure. Vous pouvez maintenant déployer environnements hébergés dans le cloud Dynamics 365 Finance.


