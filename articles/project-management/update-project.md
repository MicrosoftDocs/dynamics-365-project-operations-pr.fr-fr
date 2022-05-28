---
title: Créer et mettre à jour un projet
description: Cette rubrique offre des informations sur la mise à jour des projets dans Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592505"
---
# <a name="create-and-update-a-project"></a>Créer et mettre à jour un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

La rubrique suivante est un résumé des champs qui peuvent être mis à jour dans un projet après sa création. Cela inclut également toutes les implications applicables basées sur ces mises à jour.

## <a name="project-detail-fields"></a>Champs de détail du projet

- **Nom** : Titre du projet.
- **Description** : Vue d’ensemble du projet.
- **Client** : L’entreprise à laquelle le projet sera fourni.
- **Modèle de calendrier** : Heures de travail du projet. Lorsque le champ est modifié, l’intégralité de la planification est recalculée.
- **Devise** : Devise du projet. La valeur par défaut de ce champ est basée sur la devise définie dans l’unité contractuelle. Lorsque l’unité contractante est mise à jour, le champ est également mis à jour.
- **Unité contractuelle** : Unité d’organisation qui représente le groupe de sociétés ou la division principalement responsables de remporter la vente et de gérer la prestation du travail et des services au client.  Lorsque l’unité d’organisation du chef de projet n’est pas définie, ce champ prend par défaut la valeur définie dans les paramètres du projet.
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
