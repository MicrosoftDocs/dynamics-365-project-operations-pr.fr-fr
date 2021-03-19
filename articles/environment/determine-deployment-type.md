---
title: Déterminer votre type de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479561"
---
# <a name="determine-your-deployment-type"></a>Déterminer votre type de déploiement

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

> [!IMPORTANT]
> Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations en utilisant le [Flux d’installation guidée](https://aka.ms/provisionprojectoperations).
> Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation. Consultez les détails de déploiement pour terminer l’installation.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clients Dynamics existants utilisant Dynamics 365 Project Service Automation
Project Operations inclut les fonctionnalités fournies avec Project Service Automation. Une mise à niveau sera publiée pour ces clients dans la vague de lancement de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clients Dynamics 365 Finance existants utilisant Gestion de projets et comptabilité 

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
- Gestion des ressources unifiée
- Suivi du temps
- Dépenses de base
- Facturation pro forma et client 

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
- OCR du reçu
- Facturation complète
- Comptabilisation de clôture
- Ordres de fabrication
- Prise en charge des matériaux

#### <a name="deployment-steps"></a>Étapes de déploiement
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) et [Mettre en service un nouvel environnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
