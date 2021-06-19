---
title: Concepts clés
description: Cette rubrique fournit des informations sur les concepts clés de la gestion des ressources dans Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 5f314e3a6cc70748628145f693fb81b598e568dc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008848"
---
# <a name="key-concepts"></a>Concepts clés

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Le tableau suivant définit les concepts clés utilisés dans l’application Dynamics 365 Project Service Automation.

| Concept                    | Définition |
|----------------------------|------------|
| Membre de l’équipe du projet        | Dans le cadre de l’équipe du projet, un membre de l’équipe du projet peut être une ressource nommée avec des réservations, une réservation nommée sans réservations, ou une ressource générique. Les ressources génériques n’ont pas de réservations, sont locales au projet, et ne disposent pas de contraintes de capacité dans les projets. |
| Ressource générique du projet   | Espace réservé de ressource qui vous permet de former une équipe et doter un plan de projet en personnel sans devoir connaître la ressource nommée. Le calendrier de projet est utilisé comme calendrier de la ressource générique. Les ressources génériques peuvent être ajoutées à une équipe de projet et être attribuées aux tâches. |
| Heures réservées               | Les heures de ressource sont réservées de manière ferme sur un projet pour s’assurer que la tâche du projet est terminé. Les heures réservées sont consommées à partir de la capacité générale de la ressource. Les réservations sont faites sur des ressources nommées uniquement, pas des ressources génériques. |
| Heures attribuées             | Les heures des ressources sont attribuées aux tâches dans la planification du projet. Les attributions peuvent être pour des ressources nommées ou des ressources génériques. Les attributions peuvent être indépendantes des réservations. |
| Heures requises             | Capacité nécessaire, mais qui n’est pas encore été satisfaite par une ressource nommée. Les heures requises s’appliquent uniquement aux membres de l’équipe génériques qui ont généré les besoins en ressources. |
| Demande                     | Charge de travail actuelle et entrante. Dans Project Service Automation, la demande s’affiche sous forme de besoins en ressources ou de demandes de ressources. |
| Besoin en ressource       | Entité utilisée pour la capturer les heures requises, les dates de début et de fin, les compétences, les critères géographiques, et autres dimensions de tarification pour les ressources nécessaires. Les besoins en ressources sont générés par les membres de l’équipe du projet ou créés individuellement. |
| Demande de ressources           | Entité utilisée comme « enveloppe » pour transmettre le besoin en ressources à exécuter par un gestionnaire des ressources. |
| Rôle par défaut de la ressource      | Rôle sous lequel une ressource est regroupée pour le calcul de l’utilisation. Cela suppose que la ressource a les compétences requises pour le rôle et répond à l’utilisation cible pour ce rôle. |
| Unité d’organisation des ressources | Unité d’organisation à laquelle une ressource est attribuée. |
| Profil                    | Tâche, besoin, ou heures d’attribution, car elles sont décomposés en répartition quotidienne. Par exemple, une tâche de cinq jours, 40 heures, peut être profilée en huit heures par jour pendant cinq jours. |
| Vue Rapprochement        | Vue qui affiche les réservations et les affectations pour chaque membre de l’équipe du projet. Cette vue permet au chef de projet de rechercher une différence entre les réservations ou les attributions, et de prendre des mesures correctives si une différence se produit. |
| Heures de travail                 | Entité qui est utilisée pour identifier la capacité de la ressource, et les heures chômées et non chômées. Cette entité est également appelée le calendrier de ressources. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]