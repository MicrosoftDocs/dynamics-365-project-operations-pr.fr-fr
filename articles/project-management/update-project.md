---
title: Mettre à jour un projet
description: Cette rubrique offre des informations sur la mise à jour des projets dans Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131430"
---
# <a name="update-a-project"></a>Mettre à jour un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous trouverez ci-dessous un résumé des champs qui peuvent être mis à jour sur un projet après sa création et toutes les implications applicables des mises à jour.

## <a name="project-detail-fields"></a>Champs de détail du projet

- **Nom** : Titre du projet.
- **Description** : Vue d’ensemble du projet.
- **Client** : L’entreprise à laquelle le projet sera fourni.
- **Modèle de calendrier** : Heures de travail du projet. Lorsque le champ est modifié, la planification entière est recalculée.
- **Devise** : Devise du projet. Ce champ est par défaut basé sur la devise définie dans l’unité contractuelle. Lorsque l’unité contractuelle est mise à jour, le champ est également mis à jour.
- **Unité contractuelle** : Unité d’organisation qui représente le groupe de sociétés ou la division principalement responsables de remporter la vente et de gérer la prestation du travail et des services au client. 
- **Gestionnaire de projet** : Membre de l’équipe de projet qui a le pouvoir d’examiner et d’approuver les entrées de temps et les dépenses.

## <a name="estimate-fields"></a>Champs d’estimation

- **Date de début estimée** : Date à laquelle le projet commencera. Lorsque ce champ est mis à jour, toutes les tâches du projet seront déplacées proportionnellement à la nouvelle date de début.
- **Date de fin** : Date à laquelle le projet doit se terminer.
- **Effort** : Effort estimé du projet. Lorsque des tâches sont ajoutées au projet, ce champ n’est plus modifiable.
- **Coût estimé de la main-d’œuvre** : Coût estimé de la main-d’œuvre du projet. Lorsque des coûts de main-d’œuvre sont ajoutés au projet, ce champ n’est plus modifiable.
- **Dépenses estimées** : Dépenses estimées du projet. Lorsque des dépenses sont ajoutées au projet, ce champ n’est plus modifiable.

## <a name="project-actual-fields"></a>Champs des chiffres réels du projet
- **Début réel** : Date à laquelle le projet a commencé.
- **Fin réelle** : À mettre à jour lorsqu’un projet est terminé.

## <a name="project-status-fields"></a>Champs de statut du projet

- **Statut général du projet** : Intégrité globale du projet fournie par le chef de projet.
- **Commentaires** : Récit concernant l’intégrité actuelle du projet fourni par le chef de projet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]