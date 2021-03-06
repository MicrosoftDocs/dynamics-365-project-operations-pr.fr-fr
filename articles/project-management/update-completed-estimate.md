---
title: Mettre à jour Estimé à Achèvement
description: Cette rubrique fournit des informations sur la mise à jour de la projection d'effort sur un projet.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897763"
---
# <a name="update-estimate-at-completion"></a>Mettre à jour Estimé à Achèvement

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Il arrive souvent qu'un chef de projet modifie les estimations initiales d'une tâche. Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l'état actuel de projet. Toutefois, il n'est pas recommandé que les chefs de projet modifient les numéros de référence, car la ligne de référence du projet représente la source fiable établie pour les estimations de planning et de coût du projet convenue par toutes les parties prenantes au projet.

Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peut utiliser un chef de projet :

- Remplacez l'Estimation avant achèvement par défaut par une nouvelle évaluation des efforts restants réels pour la tâche. 
- Remplacez le pourcentage de progression par défaut par une nouvelle évaluation de la progression réelle pour la tâche.

Chacune de ces méthode entraîne un nouveau calcul de l'Estimation avant achèvement, de l'EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l'écart d'efforts escomptés pour une tâche. L'Estimation avant achèvement, l'EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l'écart d'efforts.
