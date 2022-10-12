---
title: Nouveautés de septembre 2022 - Déploiement simplifié de Project Operations
description: Cet article fournit des informations sur les mises à jour qualité disponibles dans la version de septembre 2022 du déploiement simplifié de Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621258"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Nouveautés de septembre 2022 - Déploiement simplifié de Project Operations

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.46.0.60

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

| Fonctionnalités | Nom de la fonction | Plus d’informations |
| --- | --- | --- |
| Gestion des opportunités | **Révision et activation de devis**<br>Project Operations assure la prise en charge complète du processus de vente. Les devis de projet peuvent être activés pour représenter un état dans lequel le devis est en lecture seule et en cours de révision. Les devis activés peuvent être révisés pour créer de nouveaux devis qui ont un numéro de révision incrémenté. Les devis de projet ou les révisions de devis activés peuvent être fermés comme conclus ou perdus. | [Activer et réviser un devis de projet](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturation et tarification | **Prix par défaut indépendant du fuseau horaire**<br>Project Operations a introduit le concept d’une date indépendante du fuseau horaire pour tous les chiffres réels du projet. Un nouveau champ, **Date de la transaction**, est maintenant disponible sur les lignes de journal et les chiffres réels, et sera utilisé pour stocker la date à laquelle la transaction s’est produite, mais sans convertir cette date en temps universel coordonné. Cette date sera utilisée pour les processus en aval tels que les prix par défaut et la création de factures. | <p>[Déterminer les taux de coût pour les estimations et les réels du projet](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Déterminer les prix de vente pour les estimations et les chiffres réels du projet](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturation et tarification | **Remplacements de prix à la date d’effet dans Project Operations**<br>Les Remplacements de prix à la date d’effet fournissent un moyen de remplacer ou de modifier des prix spécifiques dans la liste de prix. | [Remplacements de prix avec date d’effet](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Temps et dépenses | **Approbateur global**<br>Cette fonctionnalité active les éditeurs de logiciels indépendants (ISV) et l’approbation centralisée, quel que soit le projet ou le statut des membres de l’équipe dans le projet. | [Sécurité et approbations](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2754422 | Les estimations de matériel et de dépense ne sont pas envoyées à Dynamics 365 Finance lorsque les projets sont copiés dans Dataverse. |
| Temps et dépenses | 2787409 | Un approbateur non valide peut approuver une entrée de temps hors projet. |
| Gestion des opportunités | 2788907 | Message d’erreur mis à jour sur la validation de l’unicité pour les lignes de commande incluant des balises. |
| Temps et dépenses | 2842253 | Gestion des exceptions nulles pour l’approbation du temps. |
| Facturation et tarification | 2844181 | L’impossibilité d’obtenir l’ID de corrélation bloque la création de la facture. |
| Facturation et tarification | 2876628 | QLD, CLD - La résolution de la liste de prix de l’estimation doit utiliser les champs de plage de dates hérités de la liste de prix. |
| Sous-traitance | 2893222 | Si aucun rôle n’est spécifié pour une ligne de sous-traitance, il devrait être possible de sélectionner cette ligne d’un membre de l’équipe pour n’importe quel rôle. |
