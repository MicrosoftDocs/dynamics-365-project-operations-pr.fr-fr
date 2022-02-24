---
title: Copier un projet
description: Cette rubrique donne des informations sur la copie de projets dans Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479516"
---
# <a name="copy-a-project"></a>Copier un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Avec Dynamics 365 Project Operations, vous pouvez rapidement créer de nouveaux projets en sélectionnant **Copier le projet** dans le formulaire **Projets**. Pour copier un projet, ouvrez le projet que vous souhaitez copier, puis sélectionnez **Copier le projet**. L’action copiera :

- Propriétés du projet (la date de début estimée est copiée à partir du projet source)
- la structure de répartition du travail ;
- Membres de l’équipe du projet
- Estimations de projets
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
