---
title: Copier un projet
description: Cette rubrique fournit des informations sur la copie des projets dans Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131790"
---
# <a name="copy-a-project"></a>Copier un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Avec Dynamics 365 Project Operations, vous pouvez créer rapidement des projets en sélectionnant **Copier un projet** sur le formulaire **Projets**. Pour copier un projet, ouvrez le projet que vous souhaitez copier, puis sélectionnez **Copier le projet**. L’action copiera :

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

Pour plus d’informations sur l’accès par programme à Copier le projet, voir [Développer des modèles de projet avec Copier le projet](dev-copy-project.md).
