---
title: Suivi des ventes du projet
description: Cette rubrique fournit des informations sur la façon dont Project Operations suit la progression par rapport au revenu de la main d’œuvre d’un projet.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711043"
---
# <a name="project-sales-tracking"></a>Suivi des ventes du projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations suit les estimations de main-d’œuvre et de revenu avec la plus faible précision requise sur un plan de projet. L’estimation du revenu de la main-d’œuvre est basée sur l’effort planifié et les ressources génériques ou nommées affectées à chaque tâche de nœud terminal dans le plan de projet. Lorsque le projet commence et que les gens commencent à indiquer le temps passé sur diverses tâches du projet, le revenu réel pour la main-d’œuvre est résumé, ce qui lance un calcul des projections.

## <a name="labor-revenue-tracking-view"></a>Vue du suivi du revenu de la main d’œuvre

Sur la page **Projets**, sur l’onglet **Suivi**, vous pouvez sélectionner **Suivi** > **Coût** pour ouvrir la vue **Suivi du coût**. Ou vous pouvez sélectionner **Utiliser** > **Taux de facturation** pour ouvrir la vue **Suivi du revenu**, qui montre la progression du revenu de la main-d’œuvre sur chaque tâche dans le plan de projet. Cette vue compare également le revenu de la main-d’œuvre réel consacré à une tâche au revenu de la main-d’œuvre planifié de la tâche. Project Operations utilise les formules suivantes pour calculer les mesures du revenu de la main-d’œuvre :

- **Revenu planifié** : Valeurs de ventes estimées de toutes les affectations de ressources sur chaque tâche de nœud terminal
- **Revenu réel** : Somme de tous les chiffres réels de ventes non facturés pour le temps enregistré sur la tâche
- **% de revenu facturable** : Revenu réel ÷ Revenu final estimé
- **Revenu restant** : Revenu final estimé – Revenu réel
- **Revenu final estimé** : Revenu restant + Revenu réel
- **Écart de revenu** : Revenu planifié – Revenu final estimé


> [!NOTE]
> Project Operations n’affiche que les revenus de main-d’œuvre sur la page **Projet** de l’onglet **Suivi**. Bien que le matériel et les dépenses puissent être estimés et suivis pour la consommation, ces revenus ne sont pas inclus dans les revenus indiqués sur l’onglet **Suivi**. Cet onglet est conçu pour fonctionner uniquement pour la reprojection des revenus de main-d’œuvre par la reprojection de l’effort.  
> Tous les montants de revenu affichés sont convertis dans la devise de coût du projet. La devise de coût du projet est la devise de l’unité contractuelle du projet. Pour les projets à prix fixe, le chiffre d’affaires de la vue **Suivi du revenu de la main d’œuvre** n’est pas pertinent car les chiffres réels de ventes non facturées ne sont pas enregistrés lors de l’approbation du temps.
> Les valeurs de ventes estimées pour le temps qui sont affichées sur l’onglet **Estimation** du projet peuvent ne pas correspondre à la valeur de revenu prévue dans l’onglet **Suivi**. Deux raisons peuvent expliquer cet écart :
><ol>
   ><li> L’onglet <b>Estimations</b> affiche les revenus estimés dans la devise de vente, tandis que l’onglet <b>Suivi</b> affiche les revenus planifiés convertis dans la devise de coût. </li>
   ><li> Lorsque les ventes estimées sont converties dans la devise du contrat, comme indiqué sur l’onglet <b>Estimations</b>, dans la devise du projet, la conversion implique des étapes pouvant entraîner une perte de précision : </li>
><ol>
><li> Le montant des ventes estimé dans la devise du contrat est d’abord converti dans la devise de base (conversion 1).</li>
><li> Le montant des ventes estimé dans la devise de base est converti dans la devise de coûts du projet (conversion 2). </li>
></ol>
></ol>
> La précision de la devise est appliquée dans les deux étapes, ce qui entraîne un écart du revenu planifié dans la devise du projet par rapport aux ventes planifiées dans la devise du contrat.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reprojection des revenus sur les tâches de nœud terminal

Les revenus de main-d’œuvre sur une tâche de nœud terminal ne peuvent pas être directement reprojetés sur l’onglet **Suivi** de la page **Projet**. Cependant, vous pouvez utiliser la vue **Suivi de l’effort** pour reprojeter l’effort restant sur une tâche. Cela provoque un recalcul du revenu restant de la tâche. Vous trouverez ci-dessous une description de ce fonctionnement.

1. Un chef de projet peut reprojeter l’effort sur les tâches en mettant à jour la valeur par défaut dans le champ **Effort restant** avec une nouvelle estimation de l’effort restant sur la tâche. La reprojection entraîne un recalcul de l’estimation de l’effort de la tâche à achèvement (EAA), du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’Estimation à achèvement (EAC), l’estimation avant achèvement et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.
2. À partir de la nouvelle valeur de l’effort restant sur la tâche, le système calcule le revenu restant sur la vue **Suivi du revenu**. Pour calculer le revenu restant en fonction de l’effort restant, le système calcule d’abord le revenu moyen d’une heure d’effort sur la tâche en tant que revenu planifié ou effort planifié. Le revenu planifié est la somme du revenu de toutes les affectations de ressources sur la tâche. Le revenu moyen par heure est utilisé pour calculer le revenu restant pour l’effort restant nouvellement projeté sur la tâche.
3. Le revenu final estimé et le pourcentage de consommation du revenu de la tâche de nœud terminal sont recalculés.
4. La valeur de revenu final estimé des tâches récapitulatives jusqu’au nœud racine est recalculée.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reprojection des revenus sur les tâches récapitulatives

Vous pouvez reprojeter le revenu de main-d’œuvre sur des tâches récapitulatives ou des tâches de conteneur. Cependant, vous ne pouvez pas reprojeter directement les revenus de main-d’œuvre sur une tâche récapitulative sur l’onglet **Suivi** de la page **Projet**. Comme pour les tâches de nœud terminal, la reprojection des tâches récapitulatives et des tâches de conteneur peut être effectuée à l’aide de la vue **Suivi de l’effort**. Dans cette vue, vous pouvez reprojeter l’effort restant sur une tâche récapitulative, ce qui provoque un recalcul du revenu restant sur la tâche récapitulative. Vous trouverez ci-dessous une description de ce fonctionnement.

1. Un chef de projet peut reprojeter l’effort sur les tâches en mettant à jour la valeur par défaut dans le champ **Effort restant** avec une nouvelle estimation de l’**effort restant** sur la tâche. La reprojection entraîne un recalcul de l’estimation de la tâche à achèvement (EAA), du pourcentage de progression et de l’écart de l’effort projeté sur une tâche. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts.
2. À partir de la nouvelle valeur du champ **Effort restant** sur la tâche, le système calcule le revenu restant dans la vue **Suivi du revenu**. Pour calculer le revenu restant en fonction de l’effort restant, le système calcule d’abord le revenu moyen d’une heure d’effort sur la tâche en tant que revenu planifié ou effort planifié. Le revenu planifié est la somme du revenu de toutes les affectations de ressources sur la tâche. Ce revenu moyen par heure est alors utilisé pour calculer le revenu de l’effort restant nouvellement projeté sur la tâche.
3. Le revenu final estimé et le pourcentage de consommation du revenu de la tâche récapitulative sont recalculés.
4. La nouvelle valeur du revenu final estimé est distribuée aux tâches enfants dans la même proportion que le revenu planifié d’origine sur la tâche.
5. Le nouveau revenu final estimé sur chacune des tâches individuelles jusqu’aux tâches de nœud terminal est calculé. À partir de cette valeur, les tâches enfants affectées jusqu’aux nœuds terminaux verront leur revenu restant et leur pourcentage de consommation de revenu recalculés en fonction de la valeur du revenu final. Cela entraîne une nouvelle projection pour l’écart de revenu de la tâche. 
6. La valeur de revenu final estimé des tâches récapitulatives jusqu’au nœud racine est recalculée.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

