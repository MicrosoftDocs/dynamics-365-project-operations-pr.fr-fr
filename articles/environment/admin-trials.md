---
title: S’inscrire aux versions d’essai de Project Operations
description: cet article fournit des informations sur la façon de déployer un essai de Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 6a6986cfd6c01d1c22d37a10c8d824730fad2e9e
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029297"
---
# <a name="sign-up-for-project-operations-trials"></a>S’inscrire aux versions d’essai de Project Operations 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock, le déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication_ 



Cet article explique comment souscrire à l’offre partenaire en avant-première et déployer un environnement Dynamics 365 Project Operations.

Avec la nouvelle version d’essai de Project Operations, vous pouvez déployer automatiquement l’un des trois scénarios de déploiement pris en charge en remplissant un questionnaire qui recommande la meilleure approche de déploiement. Cet article fournit des informations sur :

- Utiliser votre offre d’essai.
- Lancer l’approvisionnement.
- Configurer la double écriture.
- En savoir plus sur Project Operations. 

Le tableau suivant présente les détails de la nouvelle offre d’essai.

| **Article de l’offre**               | **Détails**                                  |
|------------------------------|----------------------------------------------|
| Type d’offre                   | Ce type d’offre est régi par un administrateur, un administrateur client est donc requis pour pouvoir l’utiliser. |
| Utilisation de l’offre                    | Une fois par client                          |
| Durée de l’offre               | 30 jours civils                             |
| Rachats par client       | 1                                            |
| Extension                    | 1 extension, 30 jours civils               |
| Nombre d’environnements d’évaluation | 3                                            |


## <a name="admin-trial-details"></a>Détails de la version d’essai administrateur
Le tableau suivant répertorie les détails de la version d’essai et comment ils s’appliquent à chaque type de déploiement.

| **Article**                      | **Simplifié**                                     | **Matériaux hors stock** | **Matériaux stockés** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Données de configuration fournies           | Oui                                          | Oui                       | Oui (USSI)            |
| Données transactionnelles            | No                                           | No                        | No                    |
| Délai d’approvisionnement en minutes  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Conditions préalables
Les conditions préalables suivantes sont requises pour déployer une version d’essai de Dynamics 365 Project Operations.

- S’inscrire à [Dynamics 365 Project Operations - Essai en version préliminaire](https://www.aka.ms/try-po).
- L’utilisateur qui déploie la version préliminaire doit disposer des droits administrateur général du client Azure.

> [!IMPORTANT]
> Seul le client administrateur d’une organisation doit effectuer cette tâche. Si vous n’êtes pas abonné à cette version, attendez que votre organisation soit inscrite et que vous ayez reçu vos informations d’identification utilisateur.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Essai en version préliminaire 

Avant de commencer, connectez-vous à un navigateur avec le compte professionnel de l’utilisateur dans le client où vous voulez installer Project Operations en version préliminaire.

1. Utilisez le premier code promotionnel, **Dynamics 365 Project Operations - Essai en version préliminaire** en le collant dans l’URL du navigateur.

    ![Accepter l’offre](./media/16RedeemFirstOfferNew.png)

2. Confirmez votre commande.

    ![Confirmer la commande](./media/17ConfirmOrderNew.png)

  Vous verrez que l’offre de confirmation a été acceptée avec succès.

   ![Confirmation](./media/18OrderConfirmationNew.png)

  Vous serez redirigé vers le [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Questionnaire et approvisionnement

1.  Allez dans le [Centre d’administration Power Platform](https://admin.powerplatform.com/projectoperationstrial) et remplissez le questionnaire.  
2.  Passez en revue le type de déploiement recommandé et sélectionnez **Commencer l’installation** pour lancer l’approvisionnement.
3.  Examinez les conditions générales, puis sélectionnez **Démarrer**.

   Une fois l’approvisionnement démarré, vous êtes redirigé vers la liste des environnements dans le Centre d’administration Power Platform. Pendant l’approvisionnement, l’état de votre environnement est **Préparation de l’instance**.
 
  Une fois l’approvisionnement terminé, votre environnement est défini sur **Prêt**. L’approvisionnement de l’environnement inclut le déploiement des données de démonstration.
 
4.  Sélectionnez l’URL de l’environnement Microsoft Dataverse respectif et les URL des applications de finances et d’opérations pour valider le déploiement.

## <a name="configuring-dual-write"></a>Configuration de la double écriture
- Pour configurer les rôles de sécurité pour la double écriture, voir [Mettre à jour les paramètres de sécurité de Project Operations dans Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Pour accéder à la configuration à double écriture, accédez à l’instance de finance et opérations, puis accédez à **Gestion de données** > **Double écriture**.
- Pour configurer les mappages à double écriture, voir [Exécuter des mappages à double écriture Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Affecter des licences

Vous aurez besoin d’un accès administratif au portail Microsoft 365 de votre organisation pour terminer les étapes suivantes.

1. Accédez au [Centre d’administration Microsoft 365](https://portal.office.com/) pour attribuer les licences à vos utilisateurs.

   ![Page d’accueil du centre d’administration](./media/14AdminPortal.png)

2. Sur la page **Utilisateurs actifs**, sélectionnez les utilisateurs auxquels vous souhaitez attribuer une licence.

   ![Attribuer des licences](./media/15AssignLicenses.png)

3. Vérifiez que la licence **Dynamics 365 Project Operations en version préliminaire** a été sélectionnée et sélectionnez **Enregistrer les modifications**.

## <a name="additional-resources"></a>Ressources supplémentaires

Les ressources suivantes fournissent des conseils utiles lorsque vous commencez à utiliser Project Operations :

- [Série de vidéos : Présentation de Project Operations, présentations approfondies et feuille de route](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Déterminer votre type de déploiement](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Questions fréquentes

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Que se passe-t-il si j’ai besoin d’ALM ou d’ELM pour mon environnement d’applications de finances et d’opérations ?

- Pour les partenaires qui ont besoin de fonctionnalités complètes de gestion du cycle de vie de l’environnement, voir [Demande de licence de bac à sable partenaire](https://experience.dynamics.com/requestlicense) pour consulter l’offre du nouveau partenaire. 
- Pour les partenaires cherchant plus d’informations sur les droits d’utilisation interne, voir [Avantages du cloud et du logiciel des droits d’utilisation internes (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Puis-je prolonger mon essai au-delà de 30 jours ?
Pour prolonger votre essai, procédez comme suit.

1. Dans le **centre d’administration Microsoft 365**, accédez à **Facturation** > **Vos produits**.
2. Sélectionnez **Dynamics 365 Project Operations (CE) - Essai en version préliminaire**.
3. Sous **Date d’expiration**, sélectionnez **Prolonger le délai**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Puis-je passer du déploiement simplifié à un scénario de déploiement basé sur les ressources/non stocké ?
Actuellement, il n’y a pas de support pour mettre à niveau un environnement d’un déploiement simplifié vers un déploiement non stocké.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Puis-je accéder aux services Lifecycle Services (LCS) pour mes environnements Finance ?  
N° Pour ces versions d’essai, le déploiement est géré par le Centre d’administration Power Platform. L’accès à l’environnement Finance est restreint.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Puis-je installer ma version d’essai sur un environnement existant ?
Si vous disposez d’un environnement existant, vous serez autorisé à installer le déploiement simplifié sur un environnement Dataverse existant à partir du Centre d’administration Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]