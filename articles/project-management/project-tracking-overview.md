---
title: Vue d’ensemble du suivi des projets
description: Cette rubrique propose des informations sur comment suivre la progression d’un projet et de la consommation des coûts.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907360"
---
# <a name="project-tracking-overview"></a>Vue d’ensemble du suivi des projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

La nécessité de suivre la progression par rapport à une planification varie par secteur d’activité. Certains secteurs d’activité suivent à un niveau granulaire, là où d’autres secteurs d’activité suivent à un niveau supérieur. Cette rubrique montre comment planifier afin de répondre aux besoins de votre organisation.

## <a name="effort-tracking-view"></a>Vue de suivi des efforts

La vue **Suivi de l’effort** suit la progression des tâches dans le calendrier en comparant les heures d’effort réelles consacrées à une tâche aux heures d’effort planifiées de la tâche. Dynamics 365 Project Operations utilise les formules suivantes pour calculer les mesures de suivi :

- **Pourcentage de progression** : Cumul des efforts réels consacrés ÷ Estimation à l’achèvement 
- **Estimation avant achèvement** : Efforts planifiés – Cumul des efforts réels consacrés 
- **Estimation à l’achèvement** : Efforts restants + Cumul des efforts réels consacrés 
- **Écart d’efforts escomptés** : Efforts planifiés – EAA

Project Operations affiche une projection de l’écart d’efforts de la tâche. Si l’EAA excède les efforts planifiés, la tâche est prévue de prendre plus de temps qu’initialement planifié, et est en retard. Si l’EAA est inférieur aux efforts planifiés, la tâche est prévue de prendre moins de temps qu’initialement planifié, et est en avance.

## <a name="reprojecting-effort"></a>Nouvelle projection des efforts

Les chefs de projet modifient souvent les estimations initiales d’une tâche. Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l’état actuel de projet. Cependant, nous ne recommandons pas aux chefs de projet de modifier les chiffres de référence. Cela est dû au fait que les chefs de projet modifient les numéros de référence, car la ligne de référence du projet représente la source fiable établie pour les estimations de planning et de coût du projet convenue par toutes les parties prenantes au projet.

Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peut utiliser un chef de projet :

- Remplacez l’Estimation avant achèvement par défaut par une nouvelle évaluation des efforts restants réels pour la tâche. 
- Remplacez le pourcentage de progression par défaut par une nouvelle évaluation de la progression réelle pour la tâche.

Chacune de ces approches entraîne un nouveau calcul de l’Estimation avant achèvement, de l’EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l’écart d’efforts escomptés pour une tâche. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nouvelle projection des efforts sur les tâches récapitulatives

Les efforts sur les tâches récapitulatives ou les tâches de conteneur peuvent être de nouveau projetés. Que l’utilisateur refasse une projection à l’aide des efforts restants ou du pourcentage de progression sur les tâches récapitulatives, l’ensemble de calculs suivant commence :

- L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.
- Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine sur la tâche.
- Le nouvel EAA sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculé. 
- Les tâches enfants affectées jusqu’aux nœuds terminaux ont leur Estimation avant achèvement et pourcentage de progression recalculés selon la valeur de l’EAA. Cela entraîne une nouvelle projection pour l’écart d’efforts de la tâche. 
- Les EAA des tâches récapitulatives entièrement jusqu’au nœud racine sont recalculés.

### <a name="cost-tracking-view"></a>Vue Suivi du coût 

La vue **Suivi du coût** compare le coût réel consacré à une tâche au coût planifié sur une tâche. 

> [!NOTE]
> Cette vue affiche uniquement les coûts de main-d’œuvre et n’inclut pas les estimations des coûts des dépenses. Project Operations utilise les formules suivantes pour calculer les mesures de suivi :

- **Pourcentage des coûts consommés** : Cumul des coûts réels consacrés ÷ Estimation des coûts à l’achèvement
- **Coût pour terminer** : Coûts planifiés – Cumul des coûts réels consacrés
- **EAA** : Coût restant + Cumul des coûts réels consacrés
- **Écart de coûts projetés** : Coûts planifiés – EAA

Une projection de l’écart de coûts est affiché sur la tâche. Si l’EAA excède les coûts planifiés, la tâche est prévue d’être plus coûteux qu’initialement planifié. Par conséquent, sa tendance excède le budget. Si l’EAA est inférieur aux coûts planifiés, la tâche est prévue d’être moins coûteuse qu’initialement planifié. Par conséquent, sa tendance est inférieure au budget.

## <a name="project-managers-reprojection-of-cost"></a>Nouvelle projection des coûts du chef de projet

Lorsque l’effort est de nouveau projeté, l’Estimation avant achèvement, l’EAA (Estimé à Achèvement), le pourcentage des coût consommés et l’écart de coûts projeté sont tous recalculés dans la vue **Suivi du coût**.

## <a name="project-status-summary"></a>Résumé du statut du projet

Le suivi des données dans les vues **Suivi d’effort** et **Suivi du coût** affiche la progression et la consommation des coûts au niveau du nœud racine du projet, des tâches récapitulatives et des tâches de nœud terminal. La section **Statut** sur la page **Entité de projet** affiche un résumé du statut au niveau du projet.

## <a name="status-summary-fields"></a>Champs récapitulatifs du statut

Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global. Il utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant. Le champ **Commentaires** permet au chef de projet d’entrer des commentaires spécifiques relatifs au statut. Le champ **Statut mis à jour le** n’est pas modifiable et la valeur est un horodatage qui indique quand le statut a été mis à jour en dernier.

Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la date de suivi. Lorsque l’écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, vous pouvez définir ces champs sur **En avance**. Lorsque l’écart de planification et des coûts du nœud racine est négatif, vous pouvez les définir sur **En retard**.
