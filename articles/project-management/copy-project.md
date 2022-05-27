---
title: Copier un projet
description: Cette rubrique donne des informations sur la copie de projets dans Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574427"
---
# <a name="copy-a-project"></a>Copier un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Avec Dynamics 365 Project Operations, vous pouvez rapidement créer de nouveaux projets en sélectionnant **Copier le projet** dans le formulaire **Projets**. Pour copier un projet, ouvrez le projet que vous souhaitez copier, puis sélectionnez **Copier le projet**. L’action copiera les éléments suivants :

- les propriétés du projet ; 
- Structure de répartition du travail
- Membres de l’équipe du projet
- Estimations de projets
- les estimations de dépense du projet.
- Estimations du matériel du projet
- Listes de contrôle du projet
- Compartiments du projet

## <a name="project-properties"></a>les propriétés du projet ;

Lorsque le projet est copié, les valeurs des champs suivants sont copiées.

| Champ | Project Operations pour matériaux non stockés | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nom  | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Customer | :heavy_check_mark: | :heavy_check_mark: | |
| Modèle de calendrier | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Devise | :heavy_check_mark: | :heavy_check_mark: | |
| Unité contractuelle | :heavy_check_mark: | :heavy_check_mark: | |
| Société propriétaire | :heavy_check_mark: | | |
| Manager du projet | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Statut du projet global | :heavy_check_mark: | :heavy_check_mark: | |
| Commentaires | :heavy_check_mark: | :heavy_check_mark: | |
| Estimations | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Date de début estimée</p><p><strong>Remarque :</strong> Ce champ spécifie la date à laquelle le projet est créé à partir de la copie. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Date de fin estimée</p><p><strong>Remarque :</strong> La date dans ce champ est ajustée en fonction de la date de début du projet créé à partir de la copie.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Effort (en heures) | :heavy_check_mark: | :heavy_check_mark: | |
| Coût de main d’œuvre estimé | :heavy_check_mark: | :heavy_check_mark: | |
| Coût des dépenses estimé | :heavy_check_mark: | :heavy_check_mark: | |
| Coût matière estimé | | :heavy_check_mark: | |

> [!NOTE]
> La copie d’un projet est une opération de longue haleine. Les enregistrements de projet, leurs attributs pertinents et de nombreuses entités associées sont également copiés. En raison de la longueur de l’opération, une fois la copie commencée, la page du projet cible est verrouillée pour modification jusqu’à ce que l’opération de copie soit terminée.

## <a name="work-breakdown-structure"></a>Structure de répartition du travail

Lorsque le projet est copié, toute la structure de répartition du travail chargée en ressources est copiée. Les ressources nommées sont remplacées par des ressource génériques. Si les ressources nommées n’ont pas les mêmes heures de travail que la ressource générique, le planning est recalculé et les durées des tâches peuvent changer.

## <a name="project-team-members"></a>Membres de l’équipe du projet

Lorsqu’une équipe de projet est copiée à partir du projet source, les ressources génériques sont copiées. Les affectations de ressources génériques sont également gérées comme elles l’étaient dans le projet source. Les ressources nommées seront converties en membres génériques de l’équipe.

> [!NOTE]
> Les membres de l’équipe et les affectations ne sont pas copiés dans Project for the Web.

## <a name="estimates"></a>Estimations

Lorsque le projet est copié, les lignes d’estimation des ressources, des dépenses et du matériel sont copiées à partir du projet source. 

Pour plus d’informations sur l’accès par programme à Copier le projet, voir [Développer des modèles de projet avec Copier le projet](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Devis et contrats

Les devis et les contrats ne sont pas associés au projet de destination.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
