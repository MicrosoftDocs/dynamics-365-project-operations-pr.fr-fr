---
title: Nouveautés d’août 2021 - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version d’août 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323503"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Nouveautés d’août 2021 - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.13.0.152 de Project Operations dans l’environnement Dataverse

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- **Ensembles d’approbation** : Les ensembles d’approbation regroupent les demandes d’approbation de temps, de dépenses ou d’utilisation de matériel en sous-ensembles d’opérations plus petits. Ce regroupement permet de traiter les approbations par projet, dans un ordre spécifique et permet d’effectuer de nouvelles tentatives et de séquencer. Le regroupement des demandes améliore la fiabilité et la traçabilité du traitement de gros volumes d’approbations. Pour en savoir plus, consultez [Ensembles d’approbations](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2295625 | Le nom du jalon doit être copié du calendrier de facturation dans le détail de la ligne de facture. |
| Facturation et tarification | 2316323 | La remise ne doit pas être modifiable sur une facture proforma dans Project Operations pour les scénarios basés sur les ressources. |
| Gestion des opportunités | 2338619 | Les règles métier **Opportunité** et **Devis** doivent être invoquées uniquement sur les pages. |
| Gestion des ressources | 2316523 | Le fait d’utiliser **Envoyer une demande** à partir d’une exigence de ressource à laquelle est attaché un rôle ne doit pas afficher d’erreur. |
| Gestion des ressources | 2326885 | La création d’un besoin en ressources via un projet ne doit pas afficher d’erreur. |
| Temps et dépenses | 2335584 | Flux de tâches obsolètes dans l’entrée de temps. |
| Temps et dépenses | 2336884 | Le bouton d’entrée de temps **Copier la semaine** ne doit pas uniquement fonctionner pour l’utilisateur actuel. |