---
title: Progression d’un projet et consommation des coûts
description: Cette rubrique propose des informations sur le suivi de la progression d’un projet et de la consommation des coûts.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075901"
---
# <a name="project-progress-and-cost-consumption"></a>Progression d’un projet et consommation des coûts

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La nécessité de suivre la progression par rapport à une planification varie par secteur d'activité. Certains secteurs d'activité suivent à un niveau granulaire, pendant que d'autres secteurs d'activité suivent à un niveau supérieur. Cette rubrique montre comment planifier afin de répondre aux besoins de votre organisation.

## <a name="effort-tracking-view"></a>Vue de suivi des efforts

La vue **Suivi des efforts** suit la progression des tâches dans la planification. Elle compare les heures d'effort réelles consacrées à une tâche aux heures d'effort prévues de la tâche. Project Service Automation utilise les formules suivantes pour calculer les mesures de suivi :

Initialement lors de la création de la tâche : le coût prévu sera défini sur l’estimation des coûts à l’achèvement. Une fois que les chiffres réels sont enregistrés sur la tâche, ce qui suit sera le calcul sur la vue Suivi de l’effort.

- Pourcentage de progression = Cumul des efforts réels consacrés ÷ Estimation à l’achèvement 
- Estimation avant achèvement = Estimation à l’achèvement - Cumul des efforts réels consacrés 
- Estimation à l’achèvement = Efforts restants + Cumul des efforts réels consacrés 
- Écart d'efforts escomptés = Efforts planifiés – EAA

Project Service Automation affiche une projection de l’écart d’efforts de la tâche. Si l'EAA excède les efforts planifiés, la tâche est prévue de prendre plus de temps qu'initialement planifié. Par conséquent, il est en retard. Si l'EAA est inférieure aux efforts planifiés, la tâche est prévue de prendre moins de temps qu'initialement planifié. Par conséquent, il est en avance.

## <a name="reprojecting-effort"></a>Nouvelle projection des efforts

Il arrive souvent qu'un chef de projet modifie les estimations initiales d'une tâche. Les nouvelles projections de projet sont une perception des estimations du chef de projet, vu l'état actuel de projet. Toutefois, il n'est pas recommandé que les chefs de projet modifient les numéros de référence, car la ligne de référence du projet représente la source fiable établie pour les estimations de planning et de coût du projet convenue par toutes les parties prenantes au projet.

Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peut utiliser un chef de projet :

- Remplacez l’Estimation avant achèvement par défaut par une nouvelle évaluation des efforts restants réels pour la tâche. 
- Remplacez le pourcentage de progression par défaut par une nouvelle évaluation de la progression réelle pour la tâche.

Chacune de ces méthode entraîne un nouveau calcul de l'Estimation avant achèvement, de l'EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l'écart d'efforts escomptés pour une tâche. L'Estimation avant achèvement, l'EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l'écart d'efforts.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Nouvelle projection des efforts sur les tâches récapitulatives

Les efforts sur les tâches récapitulatives ou les tâches de conteneur peuvent être de nouveau projetés. Que l’utilisateur refasse une projection à l’aide des efforts restants ou du pourcentage de progression sur les tâches récapitulatives, l’ensemble de calculs suivant commence :

- L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.
- Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine sur la tâche.
- Le nouvel EAA sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculé. 
- Les tâches enfants affectées jusqu’aux nœuds terminaux ont leur Estimation avant achèvement et pourcentage de progression recalculés selon la valeur de l’EAA. Cela entraîne une nouvelle projection pour l’écart d’efforts de la tâche. 
- Les EAA des tâches récapitulatives entièrement jusqu’au nœud racine sont recalculés.

### <a name="cost-tracking-view"></a>Vue Suivi du coût 

La vue **Suivi du coût** compare le coût réel consacré à une tâche au coût planifié. 

> [!NOTE]
> Cette vue affiche uniquement les coûts de main-d'œuvre et n'inclut pas les estimations des coûts des dépenses. 

Project Service Automation utilise les formules suivantes pour calculer les mesures de suivi :

Lorsqu’une tâche est créée, le coût planifié est égal à l’estimation des coûts à l’achèvement. Une fois que les chiffres réels sont enregistrés sur la tâche, ce qui suit sera le calcul sur la vue **Suivi** du coût.

 - Pourcentage des coûts consommés = Cumul des coûts réels consacrés ÷ Estimation des coûts à l’achèvement pour la tâche
 - Coût pour terminer = Estimation des coûts à l’achèvement – Cumul des coûts réels consacrés
 - Estimation des coûts à l’achèvement = Coût avant achèvement + Cumul des coûts réels consacrés
 - Écart de coûts projetés = Coûts planifiés - Estimation des coûts à l’achèvement

Une projection de l'écart de coûts est affiché sur la tâche. Si l’estimation des coûts à l’achèvement excède les coûts planifiés, la tâche devrait être plus coûteuse qu’initialement planifié. Par conséquent, sa tendance excède le budget. Si l’estimation des coûts à l’achèvement est inférieure aux coûts planifiés, la tâche devrait être moins coûteuse qu’initialement planifié et tend à être inférieure au budget.

## <a name="project-managers-reprojection-of-cost"></a>Nouvelle projection des coûts du chef de projet

Lorsque l’effort est de nouveau projeté, les coûts avant achèvement, l’estimation des coûts à l’achèvement, le pourcentage des coûts consommés et l’écart de coûts projeté sont tous recalculés dans la vue **Suivi du coût**.

## <a name="project-status-summary"></a>Résumé du statut du projet

Le suivi des données dans les vues **Suivi d’effort** et **Suivi du coût** affiche la progression et la consommation des coûts au niveau du nœud racine du projet, des tâches récapitulatives et des tâches de nœud terminal. La section **Statut** sur la page **Entité de projet** affiche un résumé du statut au niveau du projet.

## <a name="status-summary-fields"></a>Champs récapitulatifs du statut

Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global. Il utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant. Le champ **Commentaires** permet au chef de projet d’entrer des commentaires spécifiques relatifs au statut. Le champ **Statut mis à jour le** n’est pas modifiable et la valeur est un horodatage qui indique quand le statut a été mis à jour en dernier.

Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la date de suivi. Lorsque l’écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, vous pouvez définir ces champs sur **En avance**. Lorsque l’écart de planification et des coûts du nœud racine est négatif, vous pouvez les définir sur **En retard**.
