---
title: Nouveautés de février 2021 – Déploiement léger de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de février 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3fc46ab3e82fdf7ae473202c5be737a3b8c86ab2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993998"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Nouveautés de février 2021 – Déploiement léger de Project Operations

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.7.0.95 de Project Operations dans l’environnement Dataverse

## <a name="quality-updates"></a>Mises à jour qualité

| **Zone Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| **Facturation et tarification** | 2053736 | Les détails de la ligne de facture sont désormais accessibles en accédant à **Facture** > **Informations connexes**. |
| **Facturation et tarification** | 2122613 | Les actions **Activer** et **Désactiver** ont été supprimées des entités d’association **Tarifs**. |
| **Facturation et tarification** | 2128606 | Résolution du problème avec **ullReferenceException** dans le plug-in **GetEstimatesForProject**. |
| **Déploiement et configuration** | 2140569 | La solution de projet ne doit pas être installée dans l’environnement Dataverse Teams. |
| **Déploiement et configuration** | 2086991 | Localisation de personnalisation restreinte des ressources web. |
| **Gestion des opportunités** | 2136794 | Afficher le message d’erreur correct lorsque le processus **Confirmer la facture** ou **Marquer la facture comme payée** échoue, |
| **Gestion des opportunités** | 2146376 | Le montant de la taxe corrigé dans un chiffre réel non facturable est créé à partir de la confirmation de facture. |
| **Planification et suivi de projets** | 2099879 | Le déploiement de l’environnement Dataverse doit créer une catégorie de transaction par défaut avec un ID statique et ne pas en générer une de manière aléatoire par environnement. |
| **Planification et suivi de projets** | 2128577 | Correction des privilèges d’utilisateur de Project Service pour mettre à jour la catégorie de transaction sur une affectation de ressource. |
| **Planification et suivi de projets** | 2164035 | Correction de problèmes avec la fonction **Copier le projet**. |
| **Saisie de l’heure** | 2129161 | Des restrictions plus strictes sont appliquées pour garantir que les utilisateurs ne peuvent pas modifier et mettre à jour une entrée de temps qui a été soumise ou approuvée. |
| **Saisie de l’heure** | 2103572 | L’approbation de temps pour les entrées de temps hors projet ne doit pas rechercher le rôle d’approbateur de projet. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]