---
title: Méthodes d’allocation des réservations dans Project Service Automation
description: Cet article fournit des informations sur les différentes moyens de réserver des répartitions.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dff11de0726004653233c6b90e194825c3850e0c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929165"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Méthodes d’allocation des réservations dans Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Que vous ajoutiez un membre d’équipe directement à un projet sur l’onglet **Équipe**, ou que vous réserviez une ressource pour un projet ou un besoin sur le tableau Planification, il existe quelques méthodes d’attribution de réservation que vous pouvez utiliser. Cet article explique comment chaque mode fonctionne, et quels sont ceux pouvant mener à la surréservation des ressources.

## <a name="full-capacity"></a>Capacité maximale 
Le mode Capacité maximale réserve la capacité totale de la ressource pour les dates de début et de fin spécifiées. Par exemple, si une ressource a un calendrier défini pour fonctionner huit heures par jour, cinq jours par semaine, définir une date de début et une date de fin couvrant cinq jours ouvrables réserve la ressource pendant 40 heures. La réservation se fait sans tenir compte de la capacité restante de la ressource. Si une ressource est déjà réservée sur d’autres projets pendant cette période, les 40 heures sont réservées en tant qu’heures supplémentaires, ce qui entraîne potentiellement des surréservations.

## <a name="remaining-capacity"></a>Capacité restante
Le mode Capacité restante est uniquement disponible si vous réservez directement dans un projet via le tableau de Planification. Ce mode réserve la capacité disponible de la ressource au sein de la plage de dates spécifiée. Par exemple, si une ressource a une capacité de 40 heures par semaine et a été déjà été réservée pour 10 heures, la réservation cette semaine-là entraîne une réservation des 30 heures de capacité restante cette semaine-là.

## <a name="percentage-capacity"></a>Capacité en pourcentage
Le mode Capacité en pourcentage réserve la ressource pour un pourcentage de la capacité aux dates de début et de fin spécifiées. Par exemple, si le calendrier d’une ressource est défini pour fonctionner huit heures par jour, cinq jours par semaine, définir une date de début et une date de fin couvrant cinq jours ouvrables à une capacité de 50 %% réserve la ressource pendant 20 heures. Les réservations individuelles par jour sont étalées à part égales sur la période, quatre heures par jour dans cet exemple. La réservation est effectuée sans considération pour la capacité restante de la ressource. Si la ressource est déjà réservée pendant cette période sur d’autres projets, les 20 heures sont réservées en tant qu’heures supplémentaires, ce qui entraîne potentiellement des surréservations.

## <a name="evenly-distribute-hours"></a>Heures distribuées de manière homogène
Le mode Heures distribuées de manière homogène réserve la ressource pour un nombre spécifique d’heures, en distribuant le temps de manière homogène par jour pendant la période spécifiée. Par exemple, si vous réservez une ressource pendant 20 heures sur une période de cinq jours, ce mode distribue les 20 heures en quatre heures par jour de manière homogène. La réservation est effectuée sans considération pour la capacité restante de la ressource. Si la ressource est déjà réservée pendant cette période sur d’autres projets, les 20 heures sont réservées en tant qu’heures supplémentaires, ce qui entraîne potentiellement des surréservations.

## <a name="front-load-hours"></a>Heures de chargement frontal
Le mode Heures de chargement frontal réserve la ressource pour un nombre spécifique d’heures, chargeant frontalement les heures par jour pendant la période spécifiée. Le chargement frontal consomme la capacité disponible de la ressource dans un ordre « premier arrivé, premier consommé ». Par exemple, si le planning de travail d’une ressource est de huit heures par jour, cinq jours par semaine, et qu’elle n’a aucune réservation actuelle, la réservation de la ressource pendant 20 heures sur une période de cinq jours ouvrables entraîne le modèle de réservation quotidien suivant : 

|         Réservations          |    Jour 1    |    Jour 2    |    Jour 3    |    Jour 4    |    Jour 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Réservations existantes    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nouvelle réservation          |    8        |    8        |    4        |    0        |    0        |    20       |

Le mode de chargement frontal prend en considération les réservations existantes et la capacité disponible. Par exemple, si la même ressource a déjà 20 heures réservées dans la semaine de travail, les nouvelles réservations consomment la capacité restante comme suit :

|   Réservations          | Jour 1 | Jour 2 | Jour 3 | Jour 4 | Jour 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Réservations existantes | 8     | 8     | 4     | 0     | 0     | 20    |
| Nouvelle réservation       | 0     | 0     | 4     | 8     | 8     | 20    |

Du fait que la capacité disponible est prise en compte, vous recevrez peut-être un message d’erreur si la ressource n’a plus de capacité restante pouvant être absorbée par la réservation. Avec ce mode, vous ne pouvez pas surréserver.

## <a name="none"></a>Aucune
Le mode Aucune est uniquement disponible si vous réservez depuis l’onglet **Équipe** dans un projet. Ce mode ajoute la ressource comme membre de l’équipe du projet mais ne crée aucune réservation qui absorbe la capacité de la ressource. Ce mode est utilisé lorsque le membre de l’équipe du responsable de projet par défaut est ajouté lorsqu’un projet est créé. L’utilisateur responsable de projet qui a créé le projet est ajouté par défaut au projet, afin que l’enregistrement d’entité de projet ait un propriétaire et qu’il y ait un approbateur sur le projet. Étant donné que cet utilisateur n’a pas de réservation, si vous souhaitez réserver la ressource, vous pouvez le supprimer puis le rajouter avec un autre mode d’attribution, ou ajouter la ressource aux tâches puis utiliser **Étendre les réservations** sous l’onglet **Rapprochement** pour créer des réservations pour les attributions.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Modes d’attribution entraînant une surréservation
Pour résumer, les modes d’attribution suivants entraînent une surréservation si la ressource est déjà engagée dans d’autres projets (ou pour d’autres ordres de travail et entités planifiables) :

- Capacité maximale
- Capacité du pourcentage
- Heures distribuées de manière homogène

Lorsque vous utilisez l’un de ces trois modes d’attribution, vous ne serez pas informé que la ressource est surréservée. Pour corriger la surréservation, vous devrez utiliser le tableau de Planification.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
