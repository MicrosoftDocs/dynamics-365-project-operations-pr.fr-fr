---
title: Gérer des opportunités basées sur des projets
description: Cette rubrique fournit des informations sur la manière d’utiliser des opportunités liées à des projets.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118470"
---
# <a name="manage-project-based-opportunities"></a>Gérer des opportunités basées sur des projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Pour les entreprises basées sur des projets, leurs opérations de livraison sont généralement réparties dans plusieurs pays et zones géographiques. Le coût de l’exécution et de la livraison du projet peut varier en fonction de la zone géographique ou de la division qui gère la livraison. De plus, cela peut avoir un impact sur les marges de la transaction. La livraison de services basés sur des projets implique généralement de grandes quantités de temps de ressources humaines, des dépenses considérables pour les déplacements, les frais de matériel et d’autres dépenses.

Les opportunités basées sur des projets dans Dynamics 365 Project Operations sont conçues avec des extensions pour Dynamics 365 Sales. La rubrique fournit des détails sur les différents champs et la logique métier inclus dans les fonctionnalités supplémentaires requises par les entreprises basées sur des projets pour gérer les opportunités basées sur des projets.

## <a name="view-all-project-based-opportunities"></a>Afficher toutes les opportunités basées sur des projets

Une liste de toutes les opportunités basées sur des projets peut être consultée sur la page de liste **Opportunité**. 

1. Accédez à **Ventes** > **Opportunités**.
2. Utilisez le **Commutateur de vue** pour sélectionner d’autres vues filtrées des opportunités. Vous pouvez créer vos propres vues avec des critères de filtre personnalisés pour configurer ces vues et options de navigation.

Les opportunités de projet peuvent être créées ou supprimées à partir de cette page de liste ou de la page des détails.

## <a name="business-process-flow-for-project-based-deals"></a>Flux des processus d’entreprise pour les offres basées sur des projets

Les flux des processus d’entreprise suivants sont pris en charge pour les transactions basées sur des projets dans Project Operations :

- Processus d’entreprise prospect-opportunité
- Processus de vente Opportunité

### <a name="lead-to-opportunity-business-process"></a>Processus d’entreprise prospect-opportunité 
Le processus d’entreprise prospect-opportunité prend en charge les phases suivantes :

| Étape | Entité mappée | Fonctionnalité |
| --- | --- | --- |
| Qualifier | Prospect | Qualifiez le prospect pour créer un compte, un contact et une opportunité. |
| Développer | Opportunité | Développez l’opportunité pour ajouter plus d’informations sur le travail impliqué, les principales parties prenantes et la concurrence. |
| Proposer | Opportunité | Développez la proposition et obtenez l’approbation de l’équipe de vérification interne. |
| Fermer | Opportunité | Concluez l’opportunité pour fermer la transaction. |

### <a name="opportunity-sales-process"></a>Processus de vente Opportunité
Le processus de vente Opportunité dans Project Operations est une extension du flux des processus de vente Opportunité dans l’application Sales. Ce processus d’entreprise est prêt à l’emploi et conçu pour prendre en charge les étapes suivantes d’une opportunité basée sur un projet.

| Étape | Entité mappée | Fonctionnalité |
| --- | --- | --- |
| Qualifier | Opportunité | Qualifiez le prospect pour créer un compte, un contact et une opportunité. |
| Proposer | Devis | Développez la proposition à l’aide de devis de projet et obtenez l’approbation de l’équipe de vérification interne. |
| Contrat | Contrat du projet | Remportez le devis pour créer le contrat et commencer l’exécution et la livraison du projet. |
| Fermer | Contrat du projet | Terminez le travail avec succès et fermez le contrat de projet. |

> [!NOTE]
> Si votre transaction basée sur un projet a démarré avec un Prospect, le processus d’entreprise prospect-opportunité est prioritaire.
>
> Si votre transaction basée sur un projet a démarré avec une Opportunité, le processus de vente Opportunité est prioritaire.

Vous pouvez modifier le flux des processus d’entreprise du produit ou créer vos propres flux des processus d’entreprise pour suivre votre processus de vente selon les besoins. Pour plus d’informations sur le flux des processus d’entreprise, voir [Vue d’ensemble des flux de processus d’entreprise](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]