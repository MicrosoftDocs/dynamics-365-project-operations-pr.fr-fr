---
title: Modes de planification
description: Cet article fournit des informations sur les modes de planification.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923645"
---
# <a name="scheduling-modes"></a>Modes de planification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Dynamics 365 Project Operations permet aux organisations de définir la manière dont elles gèrent les modifications apportées aux variables clés dans les tâches au sein de la structure de répartition du travail. En fonction des besoins spécifiques de l’organisation, les chefs de projet peuvent apporter des modifications au mode de planification lors de la création d’un projet.

Il existe trois modes de planification disponibles dans Project Operations :

  - Durée fixe (mode par défaut)
  - Effort fixe (*Travail*)
  - Unités fixes

Les valeurs impactées par la définition d’un mode de planification spécifique sont déterminées par la formule suivante :

  Effort = Durée x Unités

Lorsque vous définissez le mode de planification d’un projet, vous définissez l’une de ces valeurs, qui ne peut alors pas être modifiée. Le fait de conserver cette valeur en tant que constante donne la priorité à cette valeur, ce qui avertit le système de ne pas la modifier lorsque les deux autres valeurs changent. Le tableau suivant fournit des informations sur les impacts liés à la sélection d’un mode spécifique.

| **Dans cette tâche**             | **Si vous révisez les unités**   | **Si vous révisez la durée** | **Si vous révisez l’effort**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tâche avec unités fixes     | La durée est recalculée. | L’effort est recalculé.    | La durée est recalculée. |
| Tâche avec effort fixe    | La durée est recalculée. | Les unités sont recalculées.    | La durée est recalculée. |
| Tâche avec durée fixe  | L’effort est recalculé.   | L’effort est recalculé.    | Les unités sont recalculées.   |

Pour plus d’informations sur les implications d’un mode donné, voir [Modifier le type de tâche pour obtenir une planification plus précise](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Dans l’article, le terme **Travail** est utilisé à la place de **Effort**.

## <a name="change-the-organizations-scheduling-mode"></a>Changer le mode de planification de l’organisation

Procédez comme suit pour définir le mode de planification d’une organisation.

1. Accédez à **Paramètres** \> **Général** \> **Paramètres**, puis sélectionnez le paramètre du projet. 
2. Sur la page **Paramètres du projet**, sélectionnez le mode de planification par défaut pour l’organisation, puis définissez si le chef de projet peut remplacer le paramètre lors de la création d’un projet.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Modifier le paramètre du mode de planification sur un projet

Si une organisation autorise le chef de projet à remplacer le mode de planification par défaut, le chef de projet peut effectuer cette modification lorsqu’il crée un nouveau projet. Cependant, une fois le projet enregistré, le mode de planification ne peut pas être modifié.

## <a name="copied-projects"></a>Projets copiés

Étant donné qu’un projet est créé lorsque l’action de copie de projet est effectuée, le chef de projet ne peut pas définir le mode de planification. Le projet de destination utilisera toujours par défaut le mode défini au niveau de l’organisation.

## <a name="copied-tasks"></a>Tâches copiées

Lorsqu’une tâche est copiée d’un projet à un autre, la tâche hérite du mode de planification du projet de destination.
