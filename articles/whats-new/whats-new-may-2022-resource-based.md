---
title: Nouveautés de mai 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de mai 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921391"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de mai 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.42.0.70
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité
### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion des ressources | 2634019 | Amélioration des messages d’erreur pour les validations métier lors de l’ajout de membres d’équipe génériques en tant que ressources. |
| Planification et de suivi de projets | 2648515 | Mises à jour restreintes des champs **ID propriétaire**,**état** et **statut** dans les entités de planification. |
| Facturation et tarification | 2653167 | Le séparateur décimal de grille **Estimations** doit suivre les paramètres de format dans **Options personnelles**. |
| Facturation et tarification| 2662251 | Les valeurs dans les champs **Unité corrigée** et **Groupe d’unité** sont par défaut lors de la création d’enregistrements dans les estimations de matériaux. |
| Facturation et tarification| 2571408 | Les chiffres réels de ventes non facturées sont estampillés avec un ID de facture pro forma lors de la création d’une facture préliminaire. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services (LCS) et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
