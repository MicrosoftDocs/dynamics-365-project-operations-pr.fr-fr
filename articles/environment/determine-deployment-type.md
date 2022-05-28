---
title: Déterminer votre type de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 280578b2710a0bccd1973b51b062fef7a2997780
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584133"
---
# <a name="determine-your-deployment-type"></a>Déterminer votre type de déploiement

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

> [!IMPORTANT]
> Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations en utilisant le [Flux d’installation guidée](https://aka.ms/provisionprojectoperations).
> Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation. Consultez les détails de déploiement pour terminer l’installation.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clients Dynamics existants utilisant Dynamics 365 Project Service Automation
Project Operations inclut les fonctionnalités fournies avec Project Service Automation. Une mise à niveau sera publiée pour ces clients dans la vague de lancement de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clients existants de Dynamics 365 Finance utilisant la gestion de projet et la comptabilité 

Les clients existants de Finance qui utilisent la fonctionnalité Gestion du projet et comptabilité peuvent continuer à l’utiliser tel qu’il est. Voir [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma).


## <a name="deployment-regions"></a>Régions de déploiement
Pour déterminer quelles régions prennent en charge le déploiement de Project Operations, voir [Disponibilité géographique pour Dynamics 365 et le rapport Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Sélectionnez **Afficher le rapport** et développez **Dynamics 365 > Applications d’opérations > Dynamics 365 Project Operations** pour afficher les régions prises en charge.

## <a name="deployment-types"></a>Types de déploiement
Project Operations prend en charge plusieurs options de déploiement pour répondre à vos besoins. Que vous soyez un client Dynamics 365 nouveau ou existant, Project Operations peut répondre à vos besoins.

Notre [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations) vous aidera à déterminer le bon déploiement. Les résultats vous guideront vers l’un des types de déploiement suivants :

- [Déploiement simplifié – Traiter la facturation pro forma](#lite)
- [Project Operations pour les scénarios basés sur les ressources/produits non stockés](#integrated)
- [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma)

Project Operations prend en charge les scénarios stockés/d’ordre de fabrication et les scénarios non stockés/basés sur les ressources dans le même environnement par le biais des configurations au niveau de l’entité juridique. Par exemple, Contoso peut utiliser les fonctionnalités stockées/ordre de fabrication dans son usine de fabrication aux États-Unis (entité juridique = Contoso Manufacturing, États-Unis). Contoso peut utiliser les fonctionnalités non stockées / basées sur les ressources dans son installation de maintenance Contoso Robotics Arms au Royaume-Uni (entité juridique = Contoso Robotics, Royaume-Uni).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Déploiement simplifié – Traiter la facturation pro forma

Le déploiement simplifié comprend les fonctionnalités suivantes :

- Processus de vente pour les projets qui étendent les expériences d’application Dynamics 365 Sales
- Planification de projet à l’aide de Microsoft Project pour le web
- Tarification multidimensionnelle
- Gestion unifiée des ressources
- Suivi du temps
- Dépenses de base
- Facturation pro forma pour révision et modifications par le chef de projet 

#### <a name="deployment-steps"></a>Étapes de déploiement
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](lite-preview-subscription-sign-up.md) et [Mettre en service un nouvel environnement](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations pour les scénarios basés sur les ressources/produits non stockés
Project Operations pour les scénarios de ressources/non stockés incluent les fonctionnalités suivantes :
 
- Processus de vente pour les projets qui étendent les applications Dynamics 365 Sales
- Planification de projet à l’aide de Microsoft Project pour le web
- Tarification multidimensionnelle
- Gestion des ressources unifiée
- Suivi du temps
- Dépenses de base
- Dépense complète
- OCR du reçu
- Facturation pro forma et client 
- Constatation du produit pour les projets

#### <a name="deployment-steps"></a>Étapes de déploiement
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](resource-sign-up-preview-subscription.md) et [Mettre en service un nouvel environnement](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication

- Planification de projet à l’aide du WBS
- Gestion des ressources
- Suivi du temps
- Dépense complète
- Récépissé OCR
- Facturation complète
- Constatation du produit
- Ordres de fabrication
- Support matériel stocké avec inventaire

#### <a name="deployment-steps"></a>Étapes de déploiement
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) et [Mettre en service un nouvel environnement](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]