---
title: Ajouter un abonnement Azure à un projet LCS
description: Cette rubrique fournit des informations sur la connexion de votre abonnement Azure à un projet LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e4502c1dec3bfeed083186b2d053549fefc9339609946c8da919b46e0e56cc79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986668"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Ajouter un abonnement Azure à un projet LCS

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les environnements hébergés dans le cloud doivent être déployés à l’aide d’un abonnement Azure existant. Cette rubrique explique comment connecter votre abonnement Azure existant à un projet LCS. 

## <a name="grant-admin-consent"></a>Accorder un consentement d’administrateur

1. Dans votre projet LCS, dans la section **Environnements**, sélectionnez **Paramètres Microsoft Azure**.

![Paramètres Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Sur la page **Paramètres du projet**, sur l’onglet **Connecteurs Azure**, sélectionnez **Autoriser**. Cela permet aux environnements d’être déployés dans ce projet.

![Connecteurs Azure.](./media/2AzureConnectors.png)

3. Sélectionnez **Autoriser** à nouveau pour donner le consentement de l’administrateur.

![Donnez le consentement de l’administrateur.](./media/3GrantAdminConsent.png)

4. Acceptez la demande d’autorisation.

![Acceptez la demande d’autorisation.](./media/4AcceptPermissionRequest.png)

L’autorisation est maintenant terminée. 

![Autorisation réussie.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Fournissez l’accès à Dynamics Deployment Services à votre abonnement Azure

1. Accédez à [Facturation Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) et sélectionnez votre abonnement. Dynamics Deployment Services doit accéder à cet abonnement pour pouvoir déployer des environnements.

![Détails de l’abonnement Azure.](./media/6AzureSubscription.png)

2. Sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation, puis sélectionnez **Ajouter une attribution de rôle**.
3. Dans le curseur sur le côté droit, sélectionnez **Rôle Contributeur**, et dans la liste fournie, recherchez et sélectionnez **Dynamics Deployment Services**. 
4. Sélectionnez **Enregistrer**.

![Accès à l’abonnement.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Ajouter un connecteur d’abonnement à un projet LCS

1. Dans votre projet LCS, sur la page **Paramètres Microsoft Azure**, sélectionnez **Ajouter** pour ajouter un nouveau connecteur.
2. Entrer votre ID d’abonnement Azure. Vous pouvez trouver votre ID d’abonnement Azure dans le [portail Azure](https://ms.portal.azure.com/), sous **Paramètres** en bas à gauche de l’écran.
3. Dans le champ **Configurer pour utiliser Azure Resource Manager**, sélectionnez **Oui**.
4. Assurez-vous que le domaine du client AAD d’abonnement d’Azure correspond à l’abonnement Azure propriétaire du domaine que vous utilisez, puis sélectionnez **Suivant**.
5. Sur l’écran **Configuration Microsoft Azure**, sélectionnez **Suivant** pour confirmer. Si vous recevez une erreur sur cet écran, revenez à la section [Fournir l’accès à Dynamics Deployment Services à l’abonnement Azure](#provide) dans cette rubrique et assurez-vous que vous avez terminé toutes les étapes.
6. Téléchargez le certificat de gestion Azure dans un dossier local sur votre ordinateur. Demandez à votre administrateur d’abonnement Azure de charger le certificat sur le Portail de gestion Azure en sélectionnant l’abonnement et en accédant à **Paramètres** > **Certificats de gestion**. Ce certificat permet à LCS de communiquer avec Azure en votre nom. Vous pouvez ignorer cette étape si votre utilisateur a accès à l’abonnement.
7. Cliquez sur **Suivant**.
8. Sélectionnez la région Azure dans laquelle déployer et sélectionnez un centre de données proche de l’endroit où vous prévoyez d’utiliser ce système.
9.  Cliquez sur **Se connecter**.

Vous avez connecté avec succès votre abonnement Azure. Vous pouvez maintenant déployer environnements hébergés dans le cloud Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
