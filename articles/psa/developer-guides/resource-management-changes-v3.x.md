---
title: Modifications de la gestion des ressources (Project Service Automation 3.x)
description: Cette rubrique fournit des informations sur les modifications du secteur de la gestion des ressources.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075931"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Modifications de la gestion des ressources (Project Service Automation 3.x)

Les sections de cette rubrique fournissent des informations sur les modifications apportées au secteur de la gestion des ressources de Dynamics 365 Project Service Automation version 3.x.

## <a name="project-estimates"></a>Estimations de projets

Au lieu d'être basées sur l'entité **msdyn\_projecttask** ( **Tâche du projet** ), les estimations de projet sont basées sur l'entité **msdyn\_resourceassignment** ( **Attribution de ressource** ). Les affectation de ressources sont devenues la « source fiable » pour la planification et la tarification d'une tâche.

## <a name="line-tasks"></a>Tâches de ligne

Dans PSA 3.x, les tâches de ligne sont obsolètes (déconseillées). Les attributions indiquent maintenant la totalité de la tâche au lieu des tâches de ligne.

L'exemple suivant explique comment une tâche nommée « Tâche de ligne » est attribuée aux membres de l'équipe A et B dans les précédentes versions de PSA et dans PSA 3.x.

- **Avant PSA 3.x :**

    - Tâche de test

        - Tâche de test – Tâche de ligne 1

            - Attribution à A

        - Tâche de test – Tâche de ligne 2

            - Attribution à B

- **PSA 3.x :**

    - Tâche de test

        - Attribution à A
        - Attribution à B

## <a name="unassigned-assignment"></a>Attribution non attribuée

Dans PSA 3.x, une attribution non attribuée est une attribution attribuée à un membre de l'équipe **NULL** et à une ressource **NULL**. Les attributions non attribuées peuvent se produire dans certains scénarios suivants :

- Si une tâche a été créée, mais qu'elle n'a pas encore été attribuée à un membre de l'équipe, une attribution non attribuée est toujours créée. 
- Si tous les cessionnaires d'une tâche sont supprimés, une attribution non attribuée est recréée pour cette tâche.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Champs de planification de l'entité Tâche du projet

Les champs de l'entité **msdyn\_projecttask** ont été rendus obsolètes ou migrés vers l'entité **msdyn\_resourceassignment** , ou ils sont maintenant référencés à partir de l'entité **msdyn\_projectteam** ( **Membre de l'équipe du projet** ).

| Champ obsolète sur msdyn\_projecttask (Tâche du projet) | Nouveau champ sur msdyn\_resourceassignment (Attribution des ressources) | Commentaire |
|---|---|---|
| msdyn\_assignedresources | Aucune | |
| msdyn\_assignedteammembers | Aucune | |
| msdyn\_numberofresources | Aucune | |
| msdyn\_scheduledhours | Aucune | |
| msdyn\_effortcontour | msdyn\_plannedwork | Le format de la structure de données JavaScript Object Notation (JSON) stockée dans le champ a été modifié. |

## <a name="schedule-contour"></a>Profil de la planification

Le profil de la planification est stockée dans le champ **Travail planifié** ( **msdyn\_plannedwork** ) de chaque entité **Attribution de ressource** ( **msdyn\_resourceassignment** ).

### <a name="structure"></a>Structure

La nouvelle structure du profil de la planification est composée de secteurs de temps flexibles qui sont définis pour chaque jour de la planification. Chaque secteurs de temps contient les propriétés suivantes :

- **Début**  : Le début des heures de travail du jour, selon le calendrier de projet.
- **Fin**  : La fin des heures de travail du jour, selon le calendrier de projet.
- **Heures**  : Le nombre d'heures qui sont attribuées ce jour-là.

**Exemple**

Cet exemple utilise un calendrier de projet où la journée de travail est de 9 h 00 à 17 h 00 dans le fuseau horaire UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Planification automatique et planification manuelle

Si une tâche est planifiée automatiquement, les heures sont chargées à l'avance, et la durée de la tâche peut être réduite.

**Exemple**

La tâche suivante est programmée automatiquement pour 18 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Si une tâche est planifiée manuellement, les heures sont distribuées à part égales à toutes les dates.

**Exemple**

La tâche suivante est programmée manuellement pour 18 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unité d'attribution

L'unité d'attribution a été rendue obsolète dans PSA 3.x. Les heures d'effort de tâche sont maintenant divisées à parts égales, par jour, parmi toutes les ressources affectées.

**Exemple**

Dans cet exemple, la tâche est attribué à deux ressources et est planifiée automatiquement pour 36 heures sur une période de trois jours (3 décembre 2018 au 5 décembre 2018).

- Attribution 1 :

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Attribution 2 :

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensions de tarification

Dans PSA 3.x, les champs de dimension de tarification spécifiques aux ressources (comme **Rôle** et **Unité d'organisation** ) ont été supprimés de l'entité **msdyn\_projecttask**. Ces champs peuvent désormais être récupérés auprès du membre de l'équipe de projet correspondant ( **msdyn\_projectteam** ) de l'attribution de ressource ( **msdyn\_resourceassignment** ) lorsque des estimations de projet sont générées. Un nouveau champ, **msdyn\_organizationalunit** , a été ajouté à l'entité **msdyn\_projectteam**.

| Champ obsolète sur msdyn\_projecttask (Tâche du projet) | Champ de msdyn\_projectteam (Membre de l'équipe de projet) qui est utilisé à la place |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Profils

Les champs de profil de tarification et d'estimation ont été rendus obsolètes dans l'entité **msdyn\_projecttask**. Ils ont été déplacés vers l'entité **msdyn\_resourceassignment**.

| Champ obsolète sur msdyn\_projecttask (Tâche du projet) | Nouveau champ sur msdyn\_resourceassignment (Attribution des ressources) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Les champs suivants ont été ajoutés à l'entité **msdyn\_resourceassignment**  :

* msdyn\_plannedcost
* msdyn\_plannedsales

Les champs suivants des coûts et ventes planifiés, réels et restants sont inchangés sur l'entité **msdyn\_projecttask**  :

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
