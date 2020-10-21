---
title: Types de déploiement
description: Cette rubrique offre des informations vous permettant de déterminer le type de déploiement adéquat de Project Operations pour votre entreprise.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948848"
---
# <a name="deployment-types"></a>Types de déploiement

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

> [!IMPORTANT]
> Après avoir acheté la licence, commencez ici pour déterminer le meilleur modèle de déploiement de Dynamics 365 Project Operations à l’aide du [Flux d’installation guidé](https://aka.ms/provisionprojectoperations).
> Une fois que vous avez terminé le flux d’installation guidée, vous serez dirigé vers le portail de gestion approprié pour terminer votre installation. Consultez les détails de déploiement ci-dessous pour terminer l’installation.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clients Dynamics existants utilisant Dynamics 365 Project Service Automation
Project Operations inclut les fonctionnalités fournies avec Project Service Automation. Un chemin d’accès à la mise à niveau sera publié pour ces clients à l’avenir.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clients Dynamics 365 Finance existants utilisant Gestion de projet et comptabilité 

Les clients Finance existants qui utilisent la fonctionnalité Gestion de projet et comptabilité peuvent continuer à l’utiliser tel quel. Voir [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma).

Project Operations prend en charge plusieurs options de déploiement pour répondre à vos besoins. Que vous soyez un client Dynamics 365 nouveau ou existant, Project Operations peut répondre à vos besoins.

Notre [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations) vous aidera à déterminer le bon déploiement. Les résultats vous guideront vers l’un des types de déploiement suivants :

- [Déploiement simplifié – Traiter la facturation pro forma](#lite)
- [Project Operations pour les scénarios basés sur les ressources/produits non stockés](#integrated)
- [Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication](#pma)

Project Operations prend en charge les scénarios stockés/d’ordre de fabrication et les scénarios non stockés/basés sur les ressources dans le même environnement par le biais des configurations au niveau de l’entité juridique. Par exemple, Contoso peut tirer parti des capacités stockées/d’ordre de production dans son usine de fabrication aux États-Unis (entité juridique = Contoso Manufacturing United States) et des capacités non stockées/basées sur les ressources dans son installation de maintenance Contoso Robotics Arms au Royaume-Uni (entité juridique = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Déploiement simplifié – Traiter la facturation pro forma
Le déploiement simplifié comprend les fonctionnalités suivantes :

- Planification de projet à l’aide de Microsoft Project pour le web
- Tarification multidimensionnelle
- Gestion des ressources unifiée
- Suivi du temps
- Dépenses de base
- Proposition de facture

### <a name="deployment-steps"></a>Étapes de déploiement :
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](lite-preview-subscription-sign-up.md) et [Mettre en service un nouvel environnement](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations pour les scénarios basés sur les ressources/produits non stockés
Project Operations pour les scénarios de ressources/non stockés incluent les fonctionnalités suivantes :
  
- Planification de projet à l’aide de Microsoft Project pour le web
- Tarification multidimensionnelle
- Gestion des ressources unifiée
- Suivi du temps
- Dépenses de base
- Dépense complète
- OCR du reçu
- Facturation complète
- Comptabilisation de clôture

### <a name="deployment-steps"></a>Étapes de déploiement :
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](resource-sign-up-preview-subscription.md) et [Mettre en service un nouvel environnement](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication

- Planification de projet à l’aide du WBS
- Gestion des ressources
- Suivi du temps
- Dépense complète
- OCR du reçu
- Facturation complète
- Comptabilisation de clôture
- Ordres de fabrication
- Prise en charge des matériaux

### <a name="deployment-steps"></a>Étapes de déploiement :
Déterminez le meilleur modèle de déploiement de Project Operations à l’aide du [Questionnaire de déploiement](https://aka.ms/provisionprojectoperations).

Pour ce déploiement, consultez [S’inscrire à l’abonnement à la version préliminaire](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) et [Mettre en service un nouvel environnement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



