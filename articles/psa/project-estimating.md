---
title: Revenu et coûts du projet
description: Cette rubrique fournit des informations sur l'évaluation des coûts et des revenus du projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 9862b6c69596f5b998cf40691f8478bb87251583
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075770"
---
# <a name="project-costs-and-revenue"></a>Revenu et coûts du projet

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les estimations du projet fournissent une vue financière de la tâche qui est prévue et planifiée dans la planification du projet. L'onglet **Estimations** sur la page **Projets** affiche l'impact du coût et du revenu du travail que vous envisagez. Il fournit également des informations sur de nombreuses dimensions prédéfinies. 

> ![Onglet Estimations](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Valeurs de coût et de vente du projet

Les tarifs définissent le coût et les taux de facturation pour les rôles dans un projet. Vous pouvez déterminer l'impact du coût et du revenu sur le travail, selon les rôles associés au nom de l'emplacement et la ressource nommée attribuée à une tâche. Si des tâches n'ont aucune attribution (génériques ou nommées), vous ne pouvez pas obtenir d'estimations des coûts ou des ventes. Les valeurs des coûts et des ventes tiennent compte de la date définie dans les tarifs.

### <a name="default-cost-price"></a>Prix de revient par défaut  

Chaque projet appartient à une organisation. Cette organisation s'affiche dans le champ **Unité contractuelle** dans le projet. Les tarifs associés à l'unité contractuelle sont utilisés pour déterminer le prix de revient unitaire. Pour déterminer les prix de revient corrects des rôles pour la date définie sur les lignes d'estimations, recherchez la combinaison de rôle, d'unité et d'unité d'organisation dans la liste de prix de revient. 

Pour que leurs prix de revient puissent être calculés, toutes les tâches doivent être attribuées à une ressource. Toutes les tâches non affectées ont un prix de revient de 0,00.

Si la combinaison de rôle, d'unité et d'unité d'organisation ne renvoie pas de prix de revient des tarifs de l'unité contractuelle, le système ignore l'unité. Au lieu de cela, il recherche la combinaison de rôle et d'unité d'organisation seulement. Si un prix de revient est trouvé, des facteurs de conversion sont utilisés pour le convertir dans l'unité sélectionnée dans la ligne d'estimation.

Si la combinaison de rôle et d'unité d'organisation ne renvoie pas de prix de revient, le système ignore l'unité d'organisation. Au lieu de cela, il recherche la combinaison de rôle et d'unité pour définir le prix par défaut (après conversion).

Si le système ne trouve pas de prix pour le rôle, le prix de revient sur la ligne d'estimation est défini par défaut sur **0,00**. Tous les montants de coût sur les lignes d'estimation du coût du projet sont enregistrés dans la devise de l'unité contractuelle.

> [!NOTE]
> Par défaut, Microsoft Dynamics 365 stocke les montants des coûts dans votre devise de base. Toutefois, les montants des coûts qui s'affichent sur l'onglet **Estimations** sont dans la devise de l'unité contractuelle.  

### <a name="default-sales-price"></a>Prix de vente par défaut 

Les tarifs de vente sont déterminés par l'entité de vente à laquelle le projet est attaché ou par le client du projet. Lorsqu'une entité de vente, telle que Opportunité, Devis ou Contrat, est associée au projet, le prix de vente de l'entité de vente est déterminé par les tarifs associés au devis ou au contrat. Si le devis ou le contrat contient des tarifs personnalisés, le tarif est utilisé par défaut pour les estimations du projet. S'il n'y a aucune association avec les entités de ventes, le tarif de vente par défaut des paramètres est utilisé comme tarif de ventes par défaut du projet mappé par la devise client définie sur le projet.

Chaque ligne d'estimation a une unité d'allocation des ressources qui lui est associée. L'unité d'allocation des ressources indique l'unité d'organisation à partir de laquelle les ressources sont réservées pour exécuter la tâche. Pour déterminer le prix de vente des rôles associés, recherchez la combinaison de rôle, d'unité et d'unité d'allocation des ressources dans le tarif de ventes. S'il n'y a aucune attribution de la tâche, le prix de vente de la tâche est 0,00.

Si la combinaison de rôle, d'unité et d'unité d'allocation des ressources ne renvoie pas de prix de vente des tarifs de ventes, le système ignore l'unité. Au lieu de cela, il recherche la combinaison de rôle et d'unité d'allocation des ressources seulement. Si un prix de ventes est trouvé, des facteurs de conversion sont utilisés pour le convertir dans l'unité sélectionnée dans la ligne d'estimation des ventes. 

Si la combinaison de rôle et d'unité d'allocation des ressources ne renvoie pas de prix de vente des tarifs de ventes, le système ignore l'unité d'allocation des ressources. Au lieu de cela, il recherche la combinaison de rôle et d'unité pour définir le prix par défaut (après conversion).

Si le système ne trouve pas de prix pour le rôle, le prix de ventes sur la ligne d'estimation est défini par défaut sur **0,00**.

L'onglet **Estimations** offre une vue de grille montrant les lignes d'estimation. La grille contient des colonnes pour l'unité, le prix de revient total et le prix de ventes total, comme présenté dans l'illustration qui suit. 

> ![Vue de grille de l'onglet Estimations](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Vue par phases de temps des estimations du projet

La vue par phases de temps des estimations du projet affiche les estimations de données de la vue de grille entre la chronologie, à une échelle de temps que vous sélectionnez. Par défaut, les données d'estimation sont pivotées sur la dimension **Rôle**.

> ![Vue par phases de temps pour les estimations du projet](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Allocation de l'effort estimé basée sur le mode de tâche

Dans la vue par phases de temps, vous distribuez l'effort total estimé pour la tâche en allouant un certain nombre d'heures d'effort par période de temps à l'échelle de temps sélectionnée. Le mode de tâche détermine comment l'effort est alloué pendant la durée de la tâche. Les deux types d'allocation sont **Égale** et **Basée sur les heures de travail**.

### <a name="work-hours-based-allocation"></a>Allocation basée sur les heures de travail
 
Dans le mode tâche de planification automatique, les heures par défaut quotidiennes des ressources de la tâche sont définies au taux horaire de travail complet. Cela s'applique lors de l'allocation de l'effort en le fractionnant sur la durée de la tâche dans la vue par phases de temps. Par exemple, si vous estimez qu'une tâche sera effectuée par une seule ressource, échelle de temps **Jour** , l'effort alloué par jour ne dépassera pas les heures de travail par jour définies dans le calendrier du projet. Par conséquent, l'allocation d'effort garantit toujours que les ressources sont estimées pour une utilisation pendant la journée complète.

### <a name="even-allocation"></a>Répartition Égale

Dans le mode de tâche planifiée manuellement, les heures de travail du calendrier de projet ne sont pas utilisées. Au lieu de cela, la planification de tâche est basée sur les informations d'utilisateur. Pour ces tâches, l'allocation d'effort par période de temps à l'échelle de temps sélectionnée n'a aucun facteur de limitation. Tous les efforts de la tâche sont divisés équitablement et alloués à chaque période de temps à l'échelle de temps sélectionnée. Par conséquent, le modèle de tâche défini sur la tâche détermine la distribution ou l'allocation de l'effort par période de temps dans les estimations par phases de temps.

## <a name="grouping-and-time-phasing-options"></a>Options de groupement et d'échelonnement

La vue par phases de temps vous explique la distribution des estimations d'effort, de coût et de vente sur une base quotidienne, hebdomadaire, mensuelle ou annuelle. Par défaut, les données d'estimation sont pivotées sur la dimension **Rôle**. Cependant, vous pouvez utiliser l'option **Regrouper par** pour pivoter sur deux autres dimensions : **Catégorie** et **Ressource**.

Dans la vue de grille et la vue par phases de temps, vous pouvez sélectionner les champs à afficher. Les totaux de bloc d'heures sont affichés en bas du projet. Ils affichent l'effort, le coût et les ventes totaux estimés pour le jour, la semaine, le mois, ou l'année. Le prix de revient et le prix de ventes par défaut dépendent de la date. En d'autres termes, ils changent pour chaque ressource, selon la vue par phases de temps sélectionnée.

## <a name="expense-estimates"></a>Estimations de dépenses

Le bouton **Ajouter une nouvelle estimation de dépense** dans la vue de grille vous permet d'enregistrer toutes les dépenses encourues par le projet, mais qui ne sont pas directement liées au travail. Vous pouvez enregistrer les estimations des dépenses pour une tâche spécifique ou le projet entier. Sélectionnez les catégories de dépenses et la date envisagée où supporter les dépenses. Si la liste des prix de revient et le tarif de ventes associés ont des prix par défaut (ou des pourcentages de majoration définis pour les catégories de dépenses), ceux-ci sont entrés automatiquement sur la ligne d'estimation lorsque l'association a lieu.
