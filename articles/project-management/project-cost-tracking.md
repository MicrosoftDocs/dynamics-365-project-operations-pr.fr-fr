---
title: Suivi des coûts de projet
description: Cette rubrique fournit des informations sur la façon dont Project Operations suit la progression par rapport aux coûts de main-d’œuvre et aux dépenses d’un projet.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f724ee29728a363c58ed0e69087f4c18be89ea2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591447"
---
# <a name="labor-cost-tracking-on-projects"></a>Suivi des coûts de main-d’œuvre sur les projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations suit les estimations de main-d’œuvre et les dépenses avec la plus faible précision requise sur le plan de projet. L’estimation financière du coût de la main-d’œuvre est basée sur l’effort planifié et les ressources génériques ou nommées affectées à chaque tâche de nœud terminal dans le plan de projet. Lorsque le projet commence et que les gens commencent à indiquer le temps passé sur diverses tâches du projet, les dépenses réelles pour la main-d’œuvre sont résumées, ce qui lance un calcul des projections.

## <a name="labor-cost-tracking-view"></a>Vue du suivi des coûts de main-d’œuvre

Sur la page **Projets**, sur l’onglet **Suivi**, vous pouvez sélectionner **Suivi** > **Coût** pour ouvrir la vue **Suivi du coût** et voir la progression des dépenses de main-d’œuvre pour chaque tâche dans le plan de projet. Cette vue compare également le coût de main-d’œuvre réel consacré à une tâche au coût de main-d’œuvre planifié de la tâche. Project Operations utilise les formules suivantes pour calculer les mesures du coût de la main-d’œuvre :

- **Coût planifié** : Coût estimé de toutes les affectations de ressources sur chaque tâche de nœud terminal
- **Coût réel** : Somme de tous les chiffres réels de coût pour le temps enregistré sur la tâche
- **Pourcentage de consommation du coût** : Coût réel ÷ Coût estimé à achèvement
- **Coût restant** : Coût estimé à achèvement – Coût réel
- **Coût à achèvement** : Coût restant + Coût réel
- **Écart de coût** : Coût planifié – Coût estimé à achèvement

Chaque tâche montre une projection de l’écart de coûts sur la tâche. Si l’estimation des coûts à l’achèvement est supérieure au coût planifié, la tâche devrait dépasser le budget. Si l’estimation des coûts à l’achèvement est inférieure au coût planifié, la tâche devrait être en-dessous du budget.

>[!NOTE]
> Project Operations n’affiche que les coûts de main-d’œuvre sur la page **Projet** de l’onglet **Suivi**. Bien que le matériel et les dépenses puissent être estimés et suivis pour la consommation, ces coûts ne sont pas inclus dans les coûts indiqués sur l’onglet **Suivi**. Cet onglet est conçu pour fonctionner uniquement pour la reprojection des coûts de main-d’œuvre par la reprojection de l’effort.
Tous les montants de coût indiqués sont convertis dans la devise des coûts du projet à partir de la devise de prix de revient du projet utilisée pour déterminer le taux de coût. La devise de coût du projet est la devise de l’unité contractuelle du projet. Les valeurs de coût estimées pour le temps qui sont indiquées sur l’onglet **Estimations** de la page **Projet** peuvent ne pas correspondre au coût planifié sur l’onglet **Suivi**. La raison de cet écart est due aux différences dans la façon dont le coût estimé est résumé dans la grille **Estimations** et à la façon dont le coût planifié est calculé sur la grille **Suivi**. 
>
> - L’**onglet Estimations** calcule le coût estimé en utilisant la même devise que le taux de coût du tarif. Ensuite, le coût estimé dans la devise du tarif est converti en coût estimé dans la devise de coût du projet. Le coût estimé dans la devise du projet est arrondi à 2 décimales. La précision de la devise n’est appliquée à aucun moment de cette conversion. 
> - Sur l’onglet **Suivi**, le calcul des coûts planifiés suit un ordre de calcul légèrement différent qui implique que la précision de la devise soit appliquée en deux étapes : 
   ><ol>
   ><li>Le montant du coût estimé dans la devise du tarif est converti dans la devise de base (conversion 1).</li>
   ><li>Le montant du coût estimé dans la devise de base est converti dans la devise de coûts du projet (conversion 2). </li>
   ></ol>
   >La précision de la devise est appliquée au cours des deux étapes pour obtenir un coût planifié (sur l’onglet **Suivi**) qui s’écarte légèrement du coût estimé (sur la vue par **phases de temps** de l’onglet **Estimations**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reprojection des coûts sur les tâches de nœud terminal

Les coûts de main-d’œuvre sur une tâche de nœud terminal ne peuvent pas être directement reprojetés sur l’onglet **Suivi** de la **page Projet**. Cependant, vous pouvez utiliser la vue **Suivi de l’effort** pour reprojeter l’effort restant sur une tâche. Cela provoque un recalcul du coût restant de la tâche. Vous trouverez ci-dessous une description de ce fonctionnement.

1. Un chef de projet peut reprojeter l’effort sur les tâches en mettant à jour la valeur par défaut dans le champ **Effort restant** avec une nouvelle estimation de l’effort restant sur la tâche. La reprojection entraîne un recalcul de l’estimation de l’effort de la tâche à achèvement (EAA), du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’Estimation à achèvement (EAC), l’estimation avant achèvement et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.
2. À partir de la nouvelle valeur de l’effort restant sur la tâche, le système calcule le coût restant sur la vue **Suivi des coûts**. Pour calculer le coût restant en fonction de l’effort restant, le système calcule d’abord le coût moyen d’une heure d’effort sur la tâche en tant que coût planifié ou effort planifié. Le coût planifié est la somme du coût de toutes les affectations de ressources sur la tâche. Le coût moyen par heure est utilisé pour calculer le coût restant pour l’effort restant nouvellement projeté sur la tâche.
3. Le coût à achèvement et le pourcentage de consommation du coût de la tâche de nœud terminal sont recalculés.
4. La valeur coût à achèvement des tâches récapitulatives jusqu’au nœud racine est recalculée.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reprojection des coûts sur les tâches récapitulatives

Vous pouvez reprojeter les coûts de main-d’œuvre sur des tâches récapitulatives ou des tâches de conteneur. Cependant, vous ne pouvez pas reprojeter directement les coûts de main-d’œuvre sur une tâche récapitulative sur l’onglet **Suivi** de la page **Projet**. Comme pour les tâches de nœud terminal, la reprojection des tâches récapitulatives et des tâches de conteneur peut être effectuée à l’aide de la vue **Suivi de l’effort**. Dans cette vue, vous pouvez reprojeter l’effort restant sur une tâche récapitulative, ce qui provoque un recalcul du coût restant sur la tâche récapitulative. Vous trouverez ci-dessous une description de ce fonctionnement.

1. Un chef de projet peut reprojeter l’effort sur les tâches récapitulatives en mettant à jour la valeur par défaut du champ Effort restant avec une nouvelle estimation sur la tâche. Cette mise à jour entraîne un recalcul de l’estimation de l’effort de la tâche récapitulative, du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.
2. À partir de la nouvelle valeur de l’effort restant sur la tâche récapitulative, le système calcule le coût restant sur la vue **Suivi du coût**. Pour calculer le coût restant en fonction de l’effort restant, le système calcule d’abord le coût moyen d’une heure d’effort sur la tâche récapitulative en tant que coût planifié ou effort planifié. Le coût moyen par heure est utilisé pour calculer le coût de l’effort restant nouvellement projeté sur la tâche récapitulative.
3. Le coût à achèvement et le pourcentage de consommation du coût de la tâche récapitulative sont recalculés.
4. Le nouveau coût à achèvement est distribué aux tâches enfants dans la même proportion que le coût planifié d’origine sur la tâche.
5. La nouvelle valeur coût à achèvement sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculée. À partir de cette valeur, les tâches enfants affectées jusqu’aux nœuds terminaux verront leur coût restant et leur pourcentage de consommation de coût recalculés en fonction de la valeur du coût à achèvement. Cette valeur entraîne une nouvelle projection pour l’écart de coûts de la tâche. 


Le champ **Performances des coûts** peut être défini à partir des données de suivi. Lorsque l’écart de coût pour le nœud racine dans la vue **Suivi des coûts** est négatif, vous pouvez définir ce champ sur **Inférieur au budget**. Lorsque l’écart de coût pour le nœud racine est positif, vous pouvez définir la valeur sur **Supérieur au budget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
