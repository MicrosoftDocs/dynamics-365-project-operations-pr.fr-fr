---
title: Nouveautés de mars 2022 – Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de mars 2022 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583747"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Nouveautés de mars 2022 – Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.30.0.99

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

- Sous-traitance : création de factures fournisseur et expériences de mise en correspondance

## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Temps et dépenses | 2388011 | Afficher les commentaires de rejet aux auteurs de saisie de temps lors de l’approbation groupée. |
| Planification et de suivi de projets | 2495294 | Les détails du projet ne doivent pas être modifiables sur la page **Détails de la tâche**. |
| Facturation et tarification | 2499605 | Les jalons de contrat créés à partir de jalons de devis sont marqués à tort en lecture seule. |
| Planification et de suivi de projets | 2506050 | L’ensemble d’opérations reste en attente pendant une heure s’il n’y a pas de modification à enregistrer. L’ensemble est alors faussement marqué comme **Échec**, alors qu’il devrait être achevé immédiatement. |
| Facturation et tarification | 2507401 | Les unités de contrat par défaut sont saisies de manière incorrecte sur les projets en raison d’une mise en cache incorrecte. |
| Facturation et tarification | 2541660 | **Validation de la création de la commande client** en double écriture ne doit concerner que les commandes basées sur un projet. |
| Facturation et tarification | 2552745 | La taxe n’est pas répartie entre les clients qui ont configuré des règles de facturation fractionnée. |
| Facturation et tarification | 2558859 | Messages d’erreur améliorés lors de la configuration des dimensions de tarification. |
| Facturation et tarification | 2558933 | **Importer à partir des estimations de projet** échoue lorsque **msdyn\_project** est ajouté en tant que dimension de tarification. |
| Facturation et tarification | 2559101 | La suppression des paramètres du projet n’est pas bloquée et pose des problèmes. |
| Gestion des opportunités | 2570390 | Le plug-in en double écriture force le type de compte sur les devis, les commandes et les opportunités à être défini sur **Client**, même lorsque ce type de compte n’est pas correct. |
| Facturation et tarification | 2586097 | Les chiffres réels du coût facturés fractionnés ne sont pas annulés lorsqu’un projet est supprimé d’une ligne de contrat de projet. |
| Facturation et tarification | 2589619 | La taxe sur le matériel hors catalogue est propagée aux ventes réelles non facturées et à la facture. |
| Gestion des opportunités | 2594015 | Un devis ne peut pas être clôturé comme gagné pour les clients qui ont des modalités de paiement **Net60**. |
| Planification et de suivi de projets | 2595841 | Dans Project for the Web, les utilisateurs reçoivent un message d’erreur concernant un **msdyn\_actualstart** manquant lorsqu’ils créent une nouvelle demande de ressources. |
| Temps et dépenses | 2602511 | Le champ **Rejeté par** pour les entrées de temps montre **Système** au lieu d’un utilisateur nommé comme rejeteur. |
| Temps et dépenses | 2602528 | Un approbateur de projet peut approuver du temps sur des projets pour lesquels il n’est pas répertorié en tant qu’approbateur. |
| Facturation et tarification | 2608550 | Une facture de correction peut être confirmée même s’il n’y a aucun changement par rapport à l’original. |

## <a name="removed-and-deprecated-features"></a>Fonctionnalités supprimées et obsolètes

La rubrique [Fonctionnalités supprimées ou obsolètes dans Project Operations](../../whats-new/removed-depreciated-features-project.md) décrit les fonctionnalités qui ont été supprimées ou obsolètes pour Dynamics 365 Project Operations.

- Une fonctionnalité supprimée n’est plus disponible dans le produit.
- Une fonction déconseillée n’est pas en développement actif et peut être supprimée dans une prochaine mise à jour.

Une annonce d’obsolescence apparaît dans la rubrique [Fonctionnalités supprimées ou obsolètes dans Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 mois avant le retrait.
