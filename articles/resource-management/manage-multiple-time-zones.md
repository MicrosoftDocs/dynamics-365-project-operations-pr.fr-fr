---
title: Gérer les fuseaux horaires
description: Lorsqu’un projet est créé, son fuseau horaire est basé sur le fuseau horaire défini dans le modèle d’heures de travail appliqué.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279540"
---
# <a name="manage-time-zones"></a>Gérer les fuseaux horaires

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


## <a name="projects"></a>Projets

Lorsqu’un projet est créé, le fuseau horaire est basé sur le fuseau horaire défini dans le modèle d’heures de travail appliqué. Sur le **Projet** de, les dates sont toujours relatives au fuseau horaire de l’utilisateur connecté sur chaque onglet, à l’exception de l’onglet **Tâche**. Lorsque vous affichez la structure de répartition du travail, les dates seront toujours affichées dans le fuseau horaire du projet.

## <a name="tasks"></a>Tâches

Lorsqu’une tâche est créée, l’heure de début, l’heure de fin et les heures/jour sont contrôlés par les heures de travail du projet. Par exemple, si une tâche est créée avec un projet dont le fuseau horaire est -8 HCP et a les heures de travail suivantes : 9 h 00 à 17 h 00 du lundi au vendredi, toute tâche créée sans affectation respectera l’heure de début et heure de fin du calendrier du projet.

## <a name="manage-resources-with-time-zones"></a>Gérer les ressources avec les fuseaux horaires

Pour des résultats précis et prévisibles lors de l’utilisation de **Prolonger la réservation**, deux conditions préalables essentielles doivent être remplies :  

- L’utilisateur doit configurer le fuseau horaire de son appareil pour qu’il corresponde au fuseau horaire défini dans les **Paramètres de personnalisation** du système.
 
  ![Paramètres de fuseau horaire dans Windows 10](media/reconcile-assignments-03.png)

  ![Paramètres de fuseau horaire dans les paramètres de personnalisation](media/reconcile-assignments-04.png)
 
- La ressource réservable doit avoir au moins une minute de temps de travail qui se chevauche avec les profils utilisés pour définir l’extension demandée. Par exemple, les ressources suivantes avec des heures de travail comprises entre 9 h 00 et 19 h 00. 

  ![Comparaison de profils de ressource](media/reconcile-assignments-05.png)

Le tableau suivant présente :

- Un modèle de calendrier de projet
- Ressource A : cette ressource a le même calendrier et se trouve dans le même fuseau horaire que le projet. L’heure de début des réservations sera 9h00.
- Ressource B : Cette ressource est située dans un fuseau horaire différent de celui du projet et commence à 7 h 00 dans leur fuseau horaire. Cependant, les réservations commenceront à 9h00, car il s’agit de l’heure de début la plus proche du profil d’affectation.
- Ressources C et D : Les ressources sont situées dans des fuseaux horaires différents, tous deux différents les uns des autres et du projet, et leurs réservations ne commencent pas avant leurs heures de début disponibles respectives.

|Entité  |Calendrier  |
|-|-|
|Modèle de calendrier de projet   | ![calendrier du projet](media/reconcile-assignments-06.png) |
|Ressource A  | ![Calendrier de la ressource A](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Calendrier de la ressource B](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Calendrier de la ressource C](media/reconcile-assignments-08.png) |
|Ressource D  | ![Calendrier de la ressource D](media/reconcile-assignments-09.png)  |
 
Lorsque vous accédez à la vue **Rapprochement**, les affectations de ressources et les pénuries de réservation associées sont affichées.

![Vue Rapprochement avant l’extension](media/reconcile-assignments-10.png)

Une fois que la fonctionnalité d’extension de réservation a été utilisée pour chaque ressource, les réservations sont prolongées avec succès pour chaque ressource, car les heures de travail de chaque ressource chevauchent les contours de la pénurie.

![Vue Rapprochement après l’extension de la réservation](media/reconcile-assignments-11.png) 

Notez qu’un examen plus approfondi des détails des réservations montre des différences dans l’heure de début des réservations. Les réservations commencent au plus tôt à l’heure de début du contour d’affectation et au plus tôt à l’heure de début disponible de la ressource.

![Nouvelles réservations des ressources dans le tableau de planification](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]