---
title: Nouveautés de février 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de février 2021 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141307"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de février 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique s'applique aux composants et versions suivants de Dynamics 365 Project Operations :

- Project Operations dans l’environnement Dataverse 4.7.0.95
- Version 10.0.16 de gestion de projet et comptabilité dans l’environnement de Dynamics 365 Finance 

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Zone Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| **Facturation et tarification** | 2053736 | Les détails de la ligne de facture sont désormais accessibles en accédant à **Facture** > **Informations connexes**. |
| **Facturation et tarification** | 2122613 | Les actions **Activer** et **Désactiver** ont été supprimées des entités d'association **Tarifs**. |
| **Facturation et tarification** | 2128606 | Résolution du problème avec **ullReferenceException** dans le plug-in **GetEstimatesForProject**. |
| **Déploiement et configuration** | 2139346 | Résolution du problème d'importation de la solution **Dynamics365ProjectOperationsDualWrite** non gérée. |
| **Déploiement et configuration** | 2140569 | La solution de projet ne doit pas être installée dans l'environnement Dataverse Teams. |
| **Déploiement et configuration** | 2086991 | Localisation de personnalisation restreinte des ressources web. |
| **Gestion des opportunités** | 2136794 | Afficher le message d'erreur correct lorsque le processus **Confirmer la facture** ou **Marquer la facture comme payée** échoue, |
| **Gestion des opportunités** | 2139330 | La modification du chef de projet sur un projet ne doit pas réinitialiser la société propriétaire à la valeur par défaut. |
| **Gestion des opportunités** | 2146376 | Le montant de la taxe corrigé dans un chiffre réel non facturable est créé à partir de la confirmation de facture. |
| **Planification et suivi de projets** | 2099879 | Le déploiement de l'environnement Dataverse doit créer une catégorie de transaction par défaut avec un ID statique et ne pas en générer une de manière aléatoire par environnement. |
| **Planification et suivi de projets** | 2128577 | Correction des privilèges d'utilisateur de Project Service pour mettre à jour la catégorie de transaction sur une affectation de ressource. |
| **Planification et suivi de projets** | 2164035 | Correction de problèmes avec la fonction **Copier le projet**. |
| **Saisie de l’heure** | 2129161 | Des restrictions plus strictes sont appliquées pour garantir que les utilisateurs ne peuvent pas modifier et mettre à jour une entrée de temps qui a été soumise ou approuvée. |
| **Saisie de l’heure** | 2103572 | L'approbation de temps pour les entrées de temps hors projet ne doit pas rechercher le rôle d'approbateur de projet. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestion du projet et comptabilité dans Dynamics 365 Finance 

Pour plus d'informations sur la gestion de projet et la comptabilité dans Dynamics 365 Finance, voir [Nouveautés de janvier 2021 – Project Operations pour les scénarios basés sur les ressources/non stockés](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Mises à jour réglementaires

Pour plus d’informations sur les mises à jour réglementaires pour les applications Finance and Operations, consultez [Mises à jour réglementaires](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Une autre façon d'en savoir plus sur les mises à jour réglementaires consiste à vous connecter à Lifecycle Services (LCS) et à afficher les mises à jour réglementaires prévues à l'aide de l'outil de recherche de problèmes. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../includes/footer-banner.md)]