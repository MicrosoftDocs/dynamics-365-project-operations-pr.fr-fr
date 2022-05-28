---
title: Suivi des efforts de projet
description: Cette rubrique propose des informations sur le suivi de l’effort d’un projet et de la progression du travail.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593793"
---
# <a name="project-effort-tracking"></a>Suivi des efforts de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

La nécessité de suivre la progression par rapport à une planification varie par secteur d’activité. Certains secteurs d’activité suivent à un niveau granulaire, là où d’autres secteurs d’activité suivent à un niveau supérieur. Cette rubrique montre comment planifier afin de répondre aux besoins de votre organisation.

## <a name="effort-tracking-view"></a>Vue de suivi des efforts

La vue **Suivi de l’effort** suit la progression des tâches dans le calendrier en comparant les heures d’effort réelles consacrées à une tâche aux heures d’effort planifiées de la tâche. Dynamics 365 Project Operations utilise les formules suivantes pour calculer les mesures de suivi :

- **Pourcentage de progression** : Cumul des efforts réels consacrés ÷ Estimation à l’achèvement 
- **Effort restant** : Effort à achèvement estimé – Cumul des efforts réels consacrés 
- **Estimation à l’achèvement** : Efforts restants + Cumul des efforts réels consacrés 
- **Écart par rapport à l’effort projeté** : Effort planifié - Estimation de l’effort final

Project Operations affiche une projection de l’écart d’effort pour la tâche. Si l’estimation de l’effort final est supérieure à l’effort planifié, la tâche devrait prendre plus de temps que prévu initialement et est en retard sur le calendrier. Si l’EAA est inférieur aux efforts planifiés, la tâche est prévue de prendre moins de temps qu’initialement planifié, et est en avance.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reprojection de l’effort sur les tâches de nœud terminal

Les chefs de projet modifient souvent les estimations initiales d’une tâche. Les nouvelles projections de projet sont la perception d’un chef de projet des estimations, compte tenu de l’état actuel d’un projet. Cependant, nous ne recommandons pas aux chefs de projet de modifier les chiffres de l’effort planifié. En effet, l’effort planifié du projet représente la source fiable établie pour la planification du projet et l’estimation des coûts, et toutes les parties prenantes du projet l’ont accepté.

Un chef de projet peut reprojeter l’effort sur les tâches en mettant à jour l’**effort restant** par défaut avec une nouvelle estimation sur la tâche. Cette mise à jour entraîne un recalcul de l’estimation finale de la tâche, du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’estimation de l’effort final, l’estimation avant achèvement et le pourcentage d’avancement pour les tâches récapitulatives sont également recalculés et produisent une nouvelle projection de l’écart d’effort.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nouvelle projection de l’effort pour les tâches récapitulatives

Les efforts sur les tâches récapitulatives ou les tâches de conteneur peuvent être de nouveau projetés. Les chefs de projet peuvent mettre à jour l’effort restant sur les tâches récapitulatives. La mise à jour de l’effort restant déclenche l’ensemble de calculs suivant dans l’application :

- La valeur EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.
- Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine sur la tâche.
- Le nouvel EAA sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculé. 
- Les tâches enfants affectées jusqu’aux nœuds terminaux voient leur effort restant et leur pourcentage de progression recalculés selon la valeur EAA. Cela entraîne une nouvelle projection pour l’écart d’efforts de la tâche. 
- Les EAA des tâches récapitulatives entièrement jusqu’au nœud racine sont recalculés.
- L’effort approuvé sur une tâche récapitulative est la somme de l’effort approuvé sur toutes les tâches enfants plus l’effort approuvé sur la tâche récapitulative.
- L’effort restant sur la tâche récapitulative est la somme de l’effort restant sur toutes les tâches enfants moins l’effort approuvé sur la tâche récapitulative.

## <a name="project-status-summary"></a>Résumé du statut du projet

Le suivi des données dans les vues **Suivi des efforts** et **Suivi des coûts** affiche l’avancement et la consommation des coûts au niveau du nœud racine du projet, des tâches récapitulatives et des tâches de nœud terminal. La section **Statut** sur la page **Entité de projet** affiche un résumé du statut au niveau du projet.

## <a name="status-summary-fields"></a>Champs récapitulatifs du statut

Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global. Il utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant. Le champ **Commentaires** permet au chef de projet d’entrer des commentaires spécifiques relatifs au statut. Le champ **Statut mis à jour le** n’est pas modifiable et la valeur est un horodatage qui indique quand le statut a été mis à jour en dernier.

Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la date de suivi. Lorsque l’écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, vous pouvez définir ces champs sur **En avance**. Lorsque l’écart de planification et l’écart de coût pour le nœud racine sont négatifs, vous pouvez les définir sur **En retard**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
