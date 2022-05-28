---
title: Transactions commerciales dans Project Operations
description: Cette rubrique donne un aperçu du concept de transactions commerciales dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582201"
---
# <a name="business-transactions-in-project-operations"></a>Transactions commerciales dans Project Operations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dans Microsoft Dynamics 365 Project Operations, *transaction commerciale* est un concept abstrait qui n’est représenté par aucune entité. Toutefois, certains champs et processus communs dans les entités sont conçus pour utiliser le concept de transactions commerciales. Les entités suivantes utilisent ce concept :

- Détails de la ligne de devis
- Détails de la ligne de contrat
- Lignes d’estimation
- Lignes de journal
- Chiffres réels

Dans ces entités, Détails de la ligne de devis, Détails de la ligne de contrat et Lignes d’estimation sont mappés à la *phase d’estimation* au cours du cycle de vie du projet. Les entités Lignes de journal et Chiffres réels sont mappées à la *phase d’exécution* au cours du cycle de vie du projet.

Project Operations traite les enregistrements dans toutes les cinq entités comme des transactions commerciales. La seule différence est que les enregistrements dans les entités mappées à la phase d’estimation (Détails de la ligne de devis, Détails de la ligne de contrat et Lignes de devis) sont considérés comme des *prévisions financières*, alors que les enregistrements dans les entités mappées à la phase d’exécution (Lignes de journal et Chiffres réels) sont considérés comme des *faits financiers* qui se sont déjà produits.

Pour plus d’informations, voir [Estimations](../project-management/estimating-projects-overview.md) et [Chiffres réels](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concepts propres aux transactions commerciales

Les concepts suivants sont propres au concept des transactions commerciales :

- Type de transaction
- Classe de transaction
- Origine de la transaction
- Connexion de la transaction

### <a name="transaction-type"></a>Type de transaction

Le type de transaction représente la chronologie et le contexte de l’impact financier sur un projet. Il est défini par un jeu d’options avec les valeurs suivantes prises en charge dans Project Operations :

- Coût
- Contrat du projet
- Ventes non facturées
- Ventes facturées
- Ventes entre organisations
- Coût unitaire d’allocation des ressources

### <a name="transaction-class"></a>Classe de transaction

La classe de transaction représente les différents types de coûts encourus dans des projets. Il est défini par un jeu d’options avec les valeurs suivantes prises en charge dans Project Operations :

- Durée
- Dépense
- Matière
- Frais
- Jalon
- Taxes

> [!NOTE]
> La valeur **Jalon** est généralement utilisée par une logique métier pour la facturation à prix fixe dans Project Operations.

### <a name="transaction-origin"></a>Origine de la transaction

L’origine de la transaction est une entité qui stocke l’origine de chaque transaction commerciale pour faciliter la génération de rapports et la traçabilité. Au début de l’exécution du projet, chaque transaction commerciale crée une autre transaction commerciale qui, à son tour, créera une autre transaction commerciale, et ainsi de suite.

### <a name="transaction-connection"></a>Connexion de la transaction

Connexion de la transaction est une entité qui stocke la relation entre deux transactions commerciales similaires, telles que le coût et les chiffres réels associés aux ventes, ou des contrepassations de transaction déclenchées par les activités de facturation, telles que la confirmation de facture ou les corrections de facture.

Ensemble, les entités Origine de la transaction et Connexion de la transaction vous permettent de suivre les relations entre les transactions commerciales et les actions qui entraînent la création d’une transaction commerciale spécifique.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
