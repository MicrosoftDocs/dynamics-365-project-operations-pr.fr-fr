---
title: Copier un projet
description: Cette rubrique fournit des informations sur la copie des projets dans Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908099"
---
# <a name="copy-a-project"></a>Copier un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Avec Dynamics 365 Project Operations, vous pouvez créer rapidement des projets en utilisant l’action **Copier un projet** sur le formulaire **Projets**. Pour copier un projet, sélectionnez un projet, puis sélectionnez **Copier**. L’action copiera :

- les propriétés du projet ;
- la structure de répartition du travail ;
- les membres de l’équipe du projet ;
- les estimations de projets ;
- les estimations de dépense du projet.

## <a name="project-properties"></a>Propriétés du projet

Lorsque le projet est copié, les valeurs des champs suivants sont copiées :

- Nom
- Description
- Client
- Modèle de calendrier
- Devise
- Unité contractuelle
- Manager du projet
- Statut
- Statut du projet global
- Commentaires
- Estimations
- Date de début estimée
- Date de fin
- Effort (en heures)
- Coût estimé de la main d’œuvre
- Coût estimé des dépenses

## <a name="work-breakdown-structure"></a>Structure de répartition du travail

Lorsque le projet est copié, toute la structure de répartition du travail chargée en ressources est copiée. Les ressources nommées sont remplacées par des ressource génériques. Si les ressources nommées n’ont pas les mêmes heures de travail que la ressource générique, la planification sera recalculée et la durée des tâches peut changer.

## <a name="project-team-members"></a>les membres de l’équipe du projet ;

Lorsqu’une équipe de projet est copiée à partir du projet source, les ressources génériques sont copiées. Les affectations de ressources génériques sont également gérées comme elles l’étaient dans le projet source. Les ressources nommées seront converties en membres génériques de l’équipe.

## <a name="estimates"></a>Estimations

Lorsque le projet est copié, les lignes d’estimation des ressources et des dépenses sont copiées à partir du projet source.