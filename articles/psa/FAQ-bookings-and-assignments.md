---
title: Réservations des ressources et leur relation aux affectations de tâches
description: Cette rubrique fournit des informations sur comment gérer les ressources nommées, les réservations des ressources et les affectations de tâches et comment elles sont associées entre elles.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075927"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Réservations des ressources et leur relation aux affectations de tâches


Il existe deux manières dont les ressources nommées peuvent être réservées dans une équipe de projet et attribuées aux tâches du projet :

- La ressource peut être réservée directement dans un projet, puis être attribuée aux tâches du projet.
- Les tâches peuvent être attribuées à une ressource générique, qui est alors utilisée pour rechercher et remplacer la ressource générique par une ressource nommée. 

Dans les deux cas, le fait de réserver la ressource réserve la capacité de la ressource.

Le responsable de projet planifiant le projet possède le plan du projet et la planification. En utilisant la ressource générique pour l'affectation puis la génération d'une demande de ressource de là, le responsable de projet peut réserver des ressources sur le projet avec des cadres spécifiés dans le plan du projet. Il peut réserver des ressources sur un projet puis les attribuer aux tâches, mais il n'est pas possible d'aligner les cadres de réservation à ceux des tâches. Les réservations n'affectent pas la planification du projet.

Prenons un projet complexe avec de multiples tâches se chevauchant où plusieurs ressources du même type doivent travailler simultanément. Si une ressource a un cadre différents de celui de l'agrégat de leurs attributions, il est difficile de modifier les tâches pour qu'elles s'adaptent au cadre des réservations de leurs tâches respectives et de leurs cadres initiaux.

Dans l'exemple ci-dessous, l'effort total requis par la même ressource dans un groupe de quatre tâches est de 62 heures sur une période de deux semaines avec un cadre spécifique. Si la ressource Bob est réservée pendant 62 heures durant les mêmes deux semaines mais avec un autre cadre, le besoin et les réservations sont alignés.

| **Cadres des tâches**    | **Heures totales** | Lun 04/06 | Mar 05/06 | Mer 06/06 | Jeu 07/06 | Ven 08/06 | Sam 09/06 | Dim 10/06 | Lun 11/06 | Mar 12/06 | Mer 13/06 | Jeu 14/06 | Ven 15/06 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tâche 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tâche 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tâche 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tâche 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totaux**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilité de Bob
| **Réservation de la ressource** | **Heures totales** | Lun 04/06 | Mar 05/06 | Mer 06/06 | Jeu 07/06 | Ven 08/06 | Sam 09/06 | Dim 10/06 | Lun 11/06 | Mar 12/06 | Mer 13/06 | Jeu 14/06 | Ven 15/06 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Toutefois, il n'existe aucun moyen systématique pour attribuer le cadre d'heures réservées aux tâches sur une base quotidienne. Si le responsable de projet est prêt à modifier le calendrier du projet en fonction de la disponibilité de la ressource, alors il devra supprimer l'attribution et modifier toutes les tâches pour les faire correspondance au cadre de la réservation.

Dans le cas où une organisation a donné la tâche de planification du projet à un responsable de projet et à un gestionnaire des ressources, le responsable de projet définit la planification, et cela inclut la définition d'un cadre du travail requis. Le gestionnaire des ressources ne doit pas pouvoir affecter la planification sans que le responsable de projet le sache en modifiant des cadres de travail tout en réservant des ressources réelles. Si le gestionnaire de ressources accomplit quelque chose de différent de ce que le responsable de projet a demandé, ils doivent s'accorder sur les modifications nécessaires dans la planification du projet.

Étant donné que les réservations ou les attributions ne sont pas étroitement couplées, il est possible de réserver des cadres qui sont différents des cadres de tâches ou de modifier les attributions pour entraîner des circonstances où les réservations et les attributions ne sont plus alignées.

La **vue Rapprochement** permet au responsable de projet d'afficher les réservations et les attributions de chaque membre de l'équipe du projet. La vue utilise des couleurs et de l'ombrage pour afficher des différences entre des réservations et des attributions de membres de l'équipe. Selon ces informations, le responsable de projet peut prendre les mesures correctives nécessaires en étendant les réservations de la ressource pour les cas où il existe des attributions et aucune réservation ou annuler des réservations là où des ressources sont réservées mais sans attribution.

> [!NOTE]
> Si vous déplacez une tâche dont vous avez défini le cadre vous-même, ces cadres ne sont pas conservés. Les cadres sont régénérés selon le calendrier du projet pour tenir compte des modifications apportées aux heures ouvrées et aux jours non ouvrés. Ceci est intentionnel, car le système ne connaît pas l'intention du cadre d'origine et ne peut pas déterminer s'il est logique de conserver ce cadre dans une nouvelle période. Du fait que certaines réservations ou attributions sont déconnectées, les réservations conservent les cadres de réservation initiaux. Dans ce cas, vous devrez annuler et réserver à nouveau un nouveau cadre d'attribution.

