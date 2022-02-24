---
title: Suivi des efforts de projet
description: Cette rubrique propose des informations sur le suivi de l’effort d’un projet et de la progression du travail.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710937"
---
# <a name="project-effort-tracking"></a>Suivi des efforts de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

La nécessité de suivre la progression par rapport à une planification varie par secteur d’activité. Certains secteurs d’activité suivent à un niveau granulaire, là où d’autres secteurs d’activité suivent à un niveau supérieur. Cette rubrique montre comment planifier afin de répondre aux besoins de votre organisation.

## <a name="effort-tracking-view"></a>Vue de suivi des efforts

La vue **Suivi de l’effort** suit la progression des tâches dans le calendrier en comparant les heures d’effort réelles consacrées à une tâche aux heures d’effort planifiées de la tâche. Dynamics 365 Project Operations utilise les formules suivantes pour calculer les mesures de suivi :

- **Pourcentage de progression** : Cumul des efforts réels consacrés ÷ Estimation à l’achèvement 
- **Effort restant** : Effort à achèvement estimé – Cumul des efforts réels consacrés 
- **Estimation à l’achèvement** : Efforts restants + Cumul des efforts réels consacrés 
- **Écart d’efforts escomptés** : Efforts planifiés – EAA

Project Operations affiche une projection de l’écart d’efforts de la tâche. Si l’EAA excède les efforts planifiés, la tâche est prévue de prendre plus de temps qu’initialement planifié, et est en retard. Si l’EAA est inférieur aux efforts planifiés, la tâche est prévue de prendre moins de temps qu’initialement planifié, et est en avance.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reprojection de l’effort sur les tâches de nœud terminal

Les chefs de projet modifient souvent les estimations initiales d’une tâche. Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l’état actuel de projet. Cependant, nous ne recommandons pas aux chefs de projet de modifier les chiffres de l’effort planifié. En effet, l’effort planifié du projet représente la source fiable établie pour la planification du projet et l’estimation des coûts, et toutes les parties prenantes du projet l’ont accepté.

Un chef de projet peut reprojeter l’effort sur les tâches en mettant à jour l’**effort restant** par défaut avec une nouvelle estimation sur la tâche. Cette mise à jour entraîne un recalcul de l’estimation finale de la tâche, du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nouvelle projection des efforts sur les tâches récapitulatives

Les efforts sur les tâches récapitulatives ou les tâches de conteneur peuvent être de nouveau projetés. Les chefs de projet peuvent mettre à jour l’effort restant sur les tâches récapitulatives. La mise à jour de l’effort restant déclenche l’ensemble de calculs suivant dans l’application :

- La valeur EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.
- Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine sur la tâche.
- Le nouvel EAA sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculé. 
- Les tâches enfants affectées jusqu’aux nœuds terminaux voient leur effort restant et leur pourcentage de progression recalculés selon la valeur EAA. Cela entraîne une nouvelle projection pour l’écart d’efforts de la tâche. 
- Les EAA des tâches récapitulatives entièrement jusqu’au nœud racine sont recalculés.


## <a name="project-status-summary"></a>Résumé du statut du projet

Le suivi des données dans les vues **Suivi d’effort** et **Suivi du coût** affiche la progression et la consommation des coûts au niveau du nœud racine du projet, des tâches récapitulatives et des tâches de nœud terminal. La section **Statut** sur la page **Entité de projet** affiche un résumé du statut au niveau du projet.

## <a name="status-summary-fields"></a>Champs récapitulatifs du statut

Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global. Il utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant. Le champ **Commentaires** permet au chef de projet d’entrer des commentaires spécifiques relatifs au statut. Le champ **Statut mis à jour le** n’est pas modifiable et la valeur est un horodatage qui indique quand le statut a été mis à jour en dernier.

Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la date de suivi. Lorsque l’écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, vous pouvez définir ces champs sur **En avance**. Lorsque l’écart de planification et des coûts du nœud racine est négatif, vous pouvez les définir sur **En retard**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
