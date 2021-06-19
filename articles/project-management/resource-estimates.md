---
title: Estimations financières du temps de ressources sur les projets
description: Cette rubrique fournit des informations sur le calcul des estimations financières pour le temps.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010783"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimations financières du temps de ressources sur les projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les estimations financières pour le temps sont calculées en fonction de trois facteurs : 

- Le type de membre d’équipe générique ou nommé affecté à chaque tâche de nœud terminal sur le plan de projet. 
- Le type ou la complexité du travail.
- La répartition de l’effort pour l’affectation de la ressource sur la tâche. 

Les deux premiers facteurs influencent le coût unitaire ou le taux de facturation de l’affectation d’une ressource. Le coût unitaire ou le taux de facturation d’une affectation de ressource est déterminé par les attributs de la ressource affectée. Ces attributs incluent l’unité d’organisation à laquelle appartient la ressource et le rôle standard de la ressource. Vous pouvez également ajouter des attributs personnalisés pertinents pour votre entreprise pour la ressource, comme le titre standard ou le niveau d’expérience, afin qu’ils aient une influence sur le coût unitaire ou le taux de facturation de l’affectation.
Outre les attributs de la ressource, les attributs du travail, tels que la tâche, peuvent également influencer le taux de facturation unitaire ou le taux de coût de l’affectation. Par exemple, lorsque certaines tâches sont plus complexes, l’affectation de la ressource à ces tâches spécifiques entraîne un coût unitaire ou un taux de facturation plus élevé que pour les tâches moins complexes.   

Le troisième facteur indique la quantité d’heures à ce taux. Lorsqu’une tâche s’étend sur deux périodes de prix, il est probable que la première partie de l’affectation de ressources pour cette tâche soit chiffrée et tarifée différemment de la deuxième partie de la tâche. L’estimation de l’effort sur chaque affectation de ressource est une valeur complexe stockée avec la répartition quotidienne de l’effort par jour.

Pour obtenir des instructions détaillées sur la configuration d’attributs personnalisés de travail et de ressources en tant que dimensions de tarification et de coût, voir [Vue d’ensemble des dimensions de tarification](../pricing-costing/pricing-dimensions-overview.md).

L’estimation financière de chaque affectation de ressources est calculée comme suit : **taux / h pour l’affectation multiplié par le nombre d’heures.**  Comme l’estimation de l’effort, l’estimation financière du coût et du revenu pour chaque affectation de ressource est une valeur complexe stockée avec la distribution quotidienne du montant en devise par jour. 

## <a name="summarizing-financial-estimates-for-time"></a>Synthèse des estimations financières pour le temps
Une estimation financière pour le temps passé sur une tâche de nœud terminal est la somme des estimations financières de toutes les affectations de ressources pour cette tâche.

Une estimation financière pour le temps passé sur une tâche récapitulative ou parent est la somme des estimations financières de toutes ses tâches enfants. Il s’agit du coût de main d’œuvre estimé sur le projet. 

![Estimations des ressources](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prix de revient et devise du prix de revient par défaut

Le prix de revient par défaut provient des tarifs joints à l’unité contractuelle du projet. La devise de coût d’un projet est toujours la devise de l’unité contractuelle du projet. Lors d’une affectation de ressource, l’estimation financière du coût est stockée dans la devise de coût du projet. Parfois, la devise dans laquelle le taux de coût est défini dans la liste de prix est différente de la devise de coût du projet. Dans ces cas, l’application convertit la devise dans laquelle le prix de revient est défini pour la devise du projet. Sur la grille **Estimations**, toutes les estimations de coût sont affichées et résumées dans la devise de coût du projet. 

## <a name="default-bill-rate-and-sales-currency"></a>Taux de facturation et devise des ventes par défaut

Le prix de vente par défaut provient des tarifs de projet joints au contrat de projet associé si la transaction est conclue, ou du devis de projet associé si l’opération est encore en phase de prévente. La devise de vente du projet est toujours la devise du devis de projet ou du contrat de projet. Lors d’une affectation de ressource, l’estimation financière des ventes est stockée dans la devise de vente du projet. À la différence du coût, le prix de vente défini dans le tarif ne peut jamais être différent de la devise de vente du projet. La conversion de devises n’est nécessaire dans aucun scénario. Sur la grille **Estimations**, toutes les estimations de ventes sont affichées et résumées dans la devise de vente du projet. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
