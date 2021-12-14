---
title: Nouveautés de novembre 2021 - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de novembre 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e8560e7c7d6bae1bb2fda389a63bde1c57654bcb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827278"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Nouveautés de novembre 2021 - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.26.0.145, 4.26.0.148 ou 4.26.0.150
  
## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Les interfaces de programmation d’applications (API) de la Planification de projets prennent désormais en charge la possibilité de créer et de supprimer des compartiments de projet

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-in-dataverse"></a>Project Operations dans Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2358236 | La correction de facture doit permettre des corrections qui ont des lignes à prix zéro. |
| Gestion des ressources | 2410072 | Autoriser la configuration d’une ressource affectée à la tâche en tant que chef de projet. |
| Facturation et tarification | 2430234 | Correction d’un problème de calcul des performances de coût. |
| Temps et dépenses | 2436978 | Permettre à l’heure d’être saisie au format hh:mm. |
| Facturation et tarification | 2448623 | Autoriser la mise à jour des tarifs après leur association à une unité d’organisation. |
| Temps et dépenses | 2460396 | Autoriser la suppression d’une entrée de temps en effaçant la cellule. |
| Facturation et tarification | 2467386 | Autoriser la suppression d’un projet comportant une tâche, même lorsque la tâche est associée à un devis remporté. |
| Temps et dépenses | 2461744 | La vue **Mes approbations ayant échoué** ne contient que les approbations de projet à la phase **Envoyé**. |
| Temps et dépenses | 2464082 | Supprimer le lien entre les approbations de projet et l’ensemble d’approbations lorsqu’un statut cible correspond. |
| Temps et dépenses | 2468108 | Le travail de planification ne doit pas définir de statut **Traitement en cours** pour l’ensemble d’approbations. |
| Temps et dépenses | 2471503 | Supprimer les ensembles d’approbation datant de sept jours. |
| Facturation et tarification | 2480687 | La référence de ligne de devis ne doit pas être supprimée lorsqu’un jalon de ligne de devis est créé. |
