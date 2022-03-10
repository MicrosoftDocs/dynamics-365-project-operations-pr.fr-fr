---
title: Nouveautés de juin 2021 - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de juin 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e418057e695d4a7686c278bb8ca865bddbdacfb19da88860bb35dd39ab852091
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009168"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Nouveautés de juin 2021 - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Project Operations dans l’environnement Dataverse, version 4.11.0.156 ou 4.11.0.164.

## <a name="quality-updates"></a>Mises à jour qualité

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2281417 | Correction du problème concernant l’échec de l’action de création automatique de factures par le biais de la planification de factures. |
| Facturation et tarification | 2287835 |   Amélioration des performances de confirmation de factures. |
| Gestion des opportunités | 2222555 | L’imputabilité des estimations de matériel doit être correctement copiée dans les détails de la ligne de devis lors de l’utilisation de l’option **Importer à partir de l’estimation du projet**. |
| Gestion des opportunités | 2223427 | Les personnalisations sont désormais autorisées pour l’action, **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestion des opportunités | 2277528 | Correction du calcul de la valeur du jalon de facturation pour les lignes de contrat du projet avec plusieurs clients. |
| Planification et suivi de projets | 2226110 | Correction du problème intermittent avec la fonction **Générer une demande** dans la grille **Équipe du projet**. |
| Planification et suivi de projets | 2208109 | Les utilisateurs ne peuvent pas créer un projet dans une devise avec des tâches associées dans une autre devise. |
| Planification et suivi de projets | 2258228 | La liste de champs autorisés à modifier avec les entités de **Planification** qui utilisent l’API de planification a été mise à jour. |
| Planification et suivi de projets | 2293989 | Les paramètres de langue et régionaux corrects doivent être transmis à la grille **Tâches du projet**.|
| Gestion des ressources | 2220493 | Correction de l’expérience utilisateur dans la grille **Tâche** lorsque vous marquez rapidement une demande de ressource comme terminée. |
| Gestion des ressources | 2330496 | Correction du problème de chargement du **Tableau de planification**. (La mise à jour de qualité est disponible dans la version 4.11.0.164) |
| Temps et dépenses | 2194431 | La grille **Entrée de temps** doit respecter le début de la semaine comme défini dans les **Paramètres du système**. |
| Temps et dépenses | 2277311 | Une fois que vous supprimez la valeur dans une cellule de la grille **Entrée de temps**, le curseur reste dans la grille. |
