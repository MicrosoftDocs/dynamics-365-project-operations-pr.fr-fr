---
title: Nouveautés d’octobre 2022 - Déploiement simplifié de Project Operations
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version d’octobre 2022 du déploiement simplifié de Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806612"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Nouveautés d’octobre 2022 - Déploiement simplifié de Project Operations

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.57.0.176

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

| Fonctionnalités | Nom de la fonction | Plus d’informations |
| --- | --- | --- |
| Planification et suivi de projets | **Planification externe Project Operations**<br>Le mode de planification externe permet aux clients de créer, mettre à jour et supprimer de manière native des entités liées aux structures de répartition du travail (WBS) à l’aide des API Dataverse natives, mais sans les limites actuelles appliquées par Microsoft Project for the Web. | [Planification externe](/dynamics365/project-operations/project-management/external-scheduling) |
| Déploiement et configuration | <p>**Autoriser les clients à choisir le type de déploiement**<br>Les mises à jour pilotées par les produits (PDU) de Project Operations sont utilisées pour installer automatiquement la solution à double écriture de Project Operations lorsque les solutions de base à double écriture et d’orchestration sont installées dans l’environnement.</p><p>Cette fonctionnalité introduit un nouveau paramètre **Comportement de mise à niveau de la solution** dans les paramètres du projet. Lorsque ce paramètre est défini sur **Simplifié uniquement**, les mises à jour pilotées par les produits (PDU) de Project Operations n’installent plus automatiquement la solution à double écriture de Project Operations même si les solutions de base à double écriture et d’orchestration sont installées dans l’environnement. Ce comportement profitera aux clients qui prévoient d’utiliser des solutions à double écriture pour intégrer les commandes clients dans les applications de finances et d’opérations, mais qui souhaitent utiliser Project Operations en mode Simplifié (c’est-à-dire sans intégration dans les applications de finances et d’opérations).</p> | |

## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2316317 | Le système permet de créer des factures sans transactions facturables. |
| Facturation et tarification | 2737300 | Validez la disponibilité du champ Client avant d’accéder au formulaire. |
| Facturation et tarification | 2744948 | Ajoutez une vérification nulle pour la méthode de facturation. |
| Facturation et tarification | 2763515 | Traitement des erreurs de référence nulle lorsque le contrat de vente de la facture est manquant. |
| Facturation et tarification | 2844301 | La création de factures par lots échoue en raison d’une erreur. |
| Facturation et tarification | 2845869 | Stockage incorrect du service d’organisation. |
| Facturation et tarification | 2853729 | Les détails du rôle et du prix sont mis à jour lorsque le type de facturation est modifié. |
| Facturation et tarification | 2940350 | Lorsque les prix réels sont tarifés, seules les listes de prix actives doivent être saisies automatiquement. |
| Déploiement et configuration | 3001206 | L’entité msdyn\_replaylogheader empêche les mises à niveau des organisations clientes. |
| Gestion des opportunités | 2755582 | Traitement des exceptions de référence nulle dans l’assistant de règle de facturation fractionnée. |
| Gestion des opportunités | 2761477 | Lorsque la facturation fractionnée est utilisée, la suppression d’un jalon (en-tête) laisse des jalons orphelins. |
| Gestion des opportunités | 2767595 | Lorsqu’un enregistrement d’utilisation de matériel est ouvert dans le formulaire principal, la ressource réservable de l’enregistrement est remplacée par l’utilisateur actuellement connecté. |
| Planification et suivi de projets | 2790384 | Le délai d’attente OperationSet en attente est trop court. |
| Gestion des ressources | 2751560 | Unités organisationnelles préférées incohérentes dans les besoins en ressources. |
| Sous-traitance | 2907231 | L’étape de traitement des factures fournisseur ne peut pas avancer. |
| Temps et dépenses | 2867363 | Les enregistrements ne sortent pas de la vue Absences/Vacances pour approbation lorsqu’ils sont mis en file d’attente pour approbation. |
| Temps et dépenses | 2894405 | TESA : le répertoire POC inutilisé pose des problèmes de conformité. |
