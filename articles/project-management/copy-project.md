---
title: Copier un projet
description: Cette rubrique donne des informations sur la copie de projets dans Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091251"
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

## <a name="project-properties"></a>les propriétés du projet ;

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
- Date de début estimée : il s’agit de la date à laquelle le projet est créé à partir de la copie.
- Date de fin estimée : cette date est ajustée en fonction de la date de début du nouveau projet créé à partir de la copie.
- Effort (en heures)
- Coût de main d’œuvre estimé
- Coût des dépenses estimé
- Coût matière estimé

> [!NOTE]
> La copie d’un projet est une opération de longue haleine. Les enregistrements de projet, leurs attributs pertinents et de nombreuses entités associées sont également copiés. En raison de la longueur de l’opération, une fois la copie commencée, la page du projet cible est verrouillée pour modification jusqu’à ce que l’opération de copie soit terminée.

## <a name="work-breakdown-structure"></a>Structure de répartition du travail

Lorsque le projet est copié, toute la structure de répartition du travail chargée en ressources est copiée. Les ressources nommées sont remplacées par des ressource génériques. Si les ressources nommées n’ont pas les mêmes heures de travail que la ressource générique, la planification sera recalculée et la durée des tâches peut changer.

## <a name="project-team-members"></a>les membres de l’équipe du projet ;

Lorsqu’une équipe de projet est copiée à partir du projet source, les ressources génériques sont copiées. Les affectations de ressources génériques sont également gérées comme elles l’étaient dans le projet source. Les ressources nommées seront converties en membres génériques de l’équipe.

## <a name="estimates"></a>Estimations

Lorsque le projet est copié, les lignes d’estimation des ressources, des dépenses et du matériel sont copiées à partir du projet source. 

Pour plus d’informations sur l’accès par programme à Copier le projet, voir [Développer des modèles de projet avec Copier le projet](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
