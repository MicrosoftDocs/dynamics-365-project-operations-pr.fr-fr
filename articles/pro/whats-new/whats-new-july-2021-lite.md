---
title: Nouveautés de juillet 2021 - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de juillet 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009213"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Nouveautés de juillet 2021 - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Project Operations dans l’environnement Dataverse, version 4.12.0.148 ou 4.12.0.152.

## <a name="quality-updates"></a>Mises à jour qualité
| **Fonctionnalités**              | **Numéro de référence** | **Mise à jour qualité**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturation et tarification           | 2224046              | Le champ **Classe de transaction** est modifiable dans l’onglet **Détails de la ligne de devis**, mais est verrouillé si vous travaillez à partir de la page **Détails de la ligne de devis**.                                                                     |
| Facturation et tarification           | 2224400              | L’action **Fermer le devis comme conclu** échoue lorsqu’un devis n’a pas de jalons de date.                                                                                                                                    |
| Facturation et tarification           | 2234089              | Lorsque vous entrez manuellement une description de produit, celle-ci est effacée une fois que vous entrez une quantité pour une estimation de matériel.                                                                                                                         |
| Facturation et tarification           | 2234100              | La grille **Configuration de la facturation de tâches** n’inclut pas la colonne **Matériel** et sa valeur dans l’onglet **Facturation de tâches** du projet.                                                                                                       |
| Facturation et tarification           | 2277409              | L’ID produit n’est pas disponible dans le détail de la ligne de contrat pour une ligne de type de matériel.                                                                                                                                        |
| Facturation et tarification           | 2281728              | La création d’une ligne de contrat réévalue inutilement les chiffres réels, ce qui entraîne des augmentations significatives du volume de données et affecte les performances.                                                                                |
| Facturation et tarification           | 2298668              | Les lignes de journal associées à une dépense rappelée et supprimée ne sont pas supprimées.                                                                                                                                     |
| Facturation et tarification           | 2300192              | Lorsque plusieurs utilisateurs modifient une facture, il est possible de créer un nouveau détail de ligne de facture dans une facture confirmée.                                                                                   |
| Facturation et tarification           | 2301569              | Les factures ne peuvent pas être corrigées si une provision d’un montant de \$0 a été appliquée.                                                                                                                                        |
| Facturation et tarification           | 2307965              | Une erreur se produit si un prix de catégorie est créé avec des valeurs manquantes.                                                                                                                           |
| Facturation et tarification           | 2326870              | Une erreur se produit dans **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** si **producttypecode** a la valeur null.                                                                            |
| Facturation et tarification           | 2332732              | Une erreur se produit si un jalon de ligne de contrat est créé sans ligne de commande.                                                                                                                |
| Planification et suivi de projets | 2181094              | L’API de planification de projets prend désormais en charge les journaux PSS et les journaux d’ensembles d’opérations qui sont stockés pendant 90 jours.                                                                                                                  |
| Planification et suivi de projets | 2254201              | L’étiquette **Mode de planification** est mise à jour avec des détails qui décrivent la logique par défaut.                                                                                                                                      |
| Planification et suivi de projets | 2300252              | Le cache de réponse **openProject** est mis à jour et inclut le propriétaire du jeton dans la clé du cache, l’**URL de base** et l’**URL du segment** afin que l’**URL de demande** puisse toujours être recréée si l’**URL de base** change. |
| Planification et suivi de projets | 2301312              | **msdyn_membershipstatus** a été supprimé de la vue **Membre de l’équipe du projet**.                                                                                                                                        |
| Planification et suivi de projets | 2302759              | Les produits sont extraits inutilement dans les onglets **Affectations de ressources**, **Estimations** et **Estimations des dépenses**.                                                                                                        |
| Planification et suivi de projets | 2308050              | **CopyProject** échoue avec l’erreur, « Impossible d’obtenir le jeton pour parler au service distant ».                                                                                                                           |
| Planification et suivi de projets | 2322650              | La vue **Liste de tâches du projet** a été mise à jour pour afficher la date de la tâche par défaut.                                                                                                            |
| Planification et suivi de projets | 2327266              | **CopyProject** génère l’erreur « Clé introuvable dans le dictionnaire » lors de la copie des estimations.                                                                                                      |
| Planification et suivi de projets | 2328123              | **CopyProject** génère l’erreur, « Impossible d’obtenir le jeton pour parler au service distant ».                                                                                                                          |
| Planification et suivi de projets | 2336258              | **CopyProject** copie de manière incorrecte les noms de poste des ressources.                                                                                                                                                 |
| Facturation et tarification           | 2224476              | Le champ **Ressource réservable** n’est pas correctement défini par défaut sur l’utilisateur connecté dans la page **Utilisation de matériel**.                                                                                                            |
| Gestion des ressources           | 2277249              | Une erreur se produit lorsqu’une ressource requise qui n’est pas basée sur un projet est mise à jour.                                                                                                            |
| Gestion des ressources           | 2323869              | L’utilisation de ressources ne reconnaît pas correctement les ressources filtrées.                                                                                                                                             |
| Temps et dépenses              | 2176538              | Des opérateurs de filtre incorrects sont appliqués au contrôle **Entrée de temps**.                                                                                                                                                   |
| Temps et dépenses              | 2177462              | La suppression d’une entrée de temps dans la grille ne met pas à jour le statut des boutons **Soumettre**, **Rappeler**, **Supprimer** et **Modifier l’entrée** comme prévu.                                                                                        |
| Temps et dépenses              | 2299985              | **TimeEntriesImportFromResourceAssignment** ne maintient pas l’heure de début/fin des contours d’affectation.                                                                                                  |
| Temps et dépenses              | 2318426              | Une fois qu’une entrée de temps est envoyée, les champs verrouillés peuvent toujours être modifiés.                                                                                                                                   |
| Temps et dépenses              | 2323749              | Une erreur se produit lorsqu’une dépense est créée dans l’onglet **Associé** d’une ressource réservable.                                                                                                      |
| Temps et dépenses              | 2327678              | Lorsque vous créez une entrée de temps dans l’onglet **Associé** d’une ressource réservable, la ressource parent n’est pas transmise au contrôle d’entrée de temps.                                                                            |
| GÉNÉRAL                       | 2296857              | Suivi de la progression pour les tâches de longue durée.                                                                                                                                                                        |
| GÉNÉRAL                       | 2253682              | La solution de double écriture de Project Operations ne doit pas être installée lorsque le noyau de double écriture est installée dans un environnement sans la solution d’orchestration de la double écriture.                                                |
| GÉNÉRAL                       | 2316420              | La mise en service du noyau de Project Service échoue si la division de l’utilisateur de l’application est modifiée.                                                                                                                     |
| GÉNÉRAL                       | 2376405              | Correction d′un problème de mise à jour piloté par l′éditeur (la mise à jour de qualité est disponible dans la version 4.12.0.152)                                                                                                                     |
