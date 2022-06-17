---
title: Nouveautés de juin 2022 - Déploiement simplifié de Project Operations
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de juin 2022 du déploiement simplifié de Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959408"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Nouveautés de juin 2022 - Déploiement simplifié de Project Operations

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.43.0.77

## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Sous-traitance | 2708885 | Correction du message d’erreur qui s’affiche quand un utilisateur crée un enregistrement d’en-tête de réservation de ressource réservable dans lequel aucune ressource réservable n’est renseignée. |
| Planification et de suivi de projets | 2629441 | Correction de la logique de déclenchement du workflow pour éviter une boucle infinie à la mise à jour des tâches du projet. |
| Temps et dépenses | 2641209 | Les importations d’entrées de temps à partir d’affectations/réservations doivent conserver une référence de ressource réservable. |
| Planification et de suivi de projets | 2651148 | L’en-tête du document de projet doit être protégé.|
| Planification et de suivi de projets | 2653145 | Ajout de validations pour garantir qu’un enregistrement de projet ne peut pas être créé avec des caractères non valides dans son nom. |
| Temps et dépenses | 2654710 | Correction du filtrage sur la page **Approbations**. |
| Facturation et tarification | 2667805 | Ajout de validations pour empêcher la création de chiffres réels des ventes facturées si les chiffres réels des ventes non facturées n’existent pas. |
| Facturation et tarification | 2668378 | Ajout de validations pour empêcher l’ajout d’une dimension de tarification personnalisée à moins qu’un nom logique et un nom de champ ne soient renseignés. |
| Temps et dépenses | 2700428 | Amélioration de la logique des approbations pour garantir que d’autres ensembles d’approbations pour le projet peuvent être traités même si l’un des ensembles d’approbations est bloqué dans des tâches système. |
