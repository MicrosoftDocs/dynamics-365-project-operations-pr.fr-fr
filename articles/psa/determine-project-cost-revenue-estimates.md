---
title: Déterminer les estimations de coût et de revenu du projet
description: Procédure de détermination des estimations de coût et de revenu du projet dans Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148820"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Déterminer les estimations de coût et de revenu du projet 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Les estimations du projet fournissent une vue financière de la tâche prévue et planifiée dans la structure de répartition du travail du projet. La vue des estimations vous informe de l'impact du coût et du revenu du travail planifié. La vue des estimations fournit un outil pour afficher les informations sur un nombre de dimensions prédéfinies pour vous informer au mieux de l’impact financier du projet.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Coût et valeur de vente du projet  
Les tarifs du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] définissent le coût et les taux de facturation pour les rôles que les projets utilisent. En fonction des rôles associés aux tâches dans la structure de répartition du travail du projet, vous pouvez déterminer l’impact du coût et du revenu du travail concerné.  
  
## <a name="cost-price-defaulting"></a>Prix de revient par défaut  
Chaque projet appartient à une organisation (indiquée dans **Unité propriétaire** dans le projet). Les tarifs associés à l’unité d’organisation propriétaire déterminent le prix de revient unitaire. Le [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] détermine les prix de revient des rôles en recherchant la combinaison de rôle, d’unité et d’unité d’organisation dans la liste de prix de revient pour obtenir le prix de revient approprié pour la date réelle sur les lignes d’estimation.  
  
Dans la combinaison de rôle, d'unité et d’unité d’organisation n’aboutit pas à un prix de revient à partir des tarifs de l’unité propriétaire, l’unité est ignorée en faveur de la combinaison de rôle et d’unité d’organisation. S’il y a un prix de revient, ce dernier est converti vers l’unité que vous avez sélectionnée sur la ligne d’estimation.  
  
Si la combinaison de rôle et d’unité d’organisation n’aboutit pas à un prix de revient, l’unité d’organisation est ignorée en faveur de la combinaison de rôle et d’unité, et le prix par défaut est appliqué après l’application de toute conversion, si nécessaire.  
  
 S’il n’y a pas de prix pour le rôle, les valeurs par défaut du prix de revient sont de 0,00 sur la ligne d’estimation.  
  
 Tous les montants de coût sur les lignes d’estimation du coût du projet sont dans la devise de l’unité d’organisation propriétaire.  
  
## <a name="sales-price-defaulting"></a>Prix de vente par défaut  
Les tarifs de vente sont basés sur l’entité de vente à laquelle le projet est associé. Les tarifs de vente associés au devis ou au contrat déterminent le prix de vente unitaire. Si le devis ou le contrat contient des tarifs personnalisés, il s’agira des tarifs de vente par défaut pour les estimations du projet. S’il n’y a aucune association avec les entités de vente, les tarifs de vente par défaut configurés dans les paramètres seront les tarifs par défaut du projet. Chaque ligne d’estimation est associée à une unité d’organisation des ressources pour indiquer l’unité d’organisation à partir de laquelle les ressources sont réservées pour exécuter la tâche. Le prix de vente des rôles associés est déterminé en recherchant la combinaison de rôle, d’unité, et d’unité d’organisation des ressources dans les tarifs de vente pour obtenir le prix de vente approprié pour la date réelle sur les lignes d’estimation.  
  
Si la combinaison de rôle, d’unité et d’unité d’organisation des ressources n’aboutit pas à un prix de vente depuis les tarifs, le système ignorera l’unité et recherchera la combinaison de rôle et d’unité d’organisation des ressources. S’il y a un prix de vente, ce dernier est converti vers l’unité que vous avez sélectionnée sur la ligne d’estimation de vente.  
  
Si le système ne trouve pas de prix pour le rôle, le prix de vente par défaut est de 0,00 sur la ligne d’estimation.  
  
La vue des estimations a une vue grille comportant une grille plate des lignes d’estimation avec le coût unitaire et total et le prix de vente.  
  
## <a name="time-phased-view-of-project-estimates"></a>Vue par phases de temps des estimations du projet  
Dans la vue par phases de temps pour les estimations de projet, les données des estimations de la vue grille sont pivotées par défaut par rôle, et la vue affiche une plage de données d’estimation sur la chronologie dans l’échelle de temps sélectionnée.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Allocation de l’effort estimé basée sur le mode de tâche  
Dans la vue par phases de temps, l’effort total estimé pour la tâche est distribué en allouant un certain nombre d’heures d’effort par période de temps de l’échelle de temps sélectionnée. Dans Project Service, le mode de tâche détermine comment l’effort est alloué pendant la durée de la tâche. Les deux types d’allocation sont basés sur des heures d’allocation et de travail égales. 
  
## <a name="work-hours-based-allocation"></a>Allocation basée sur les heures de travail  
Le mode de tâche de planification automatique pour une tâche régit le nombre de ressources estimées sur la tâche, elles sont estimées pour une utilisation pendant toutes les heures de travail par jour. Cela s’applique lors de l’allocation de l’effort en le fractionnant sur la durée des tâches dans la vue par phases de temps. Par exemple, sur une échelle de temps « Jour », pour une tâche destinée à être effectuée par une ressource, l’effort alloué par jour ne dépassera pas les heures de travail définies par jour dans le calendrier du projet. Par conséquent, l’allocation d’effort garantit toujours que les ressources sont estimées pour une utilisation pendant la journée complète.  
  
## <a name="even-distribution"></a>Distribution égale  
Le mode de tâche de planification manuelle ne tient pas compte des heures de travail, du calendrier du projet, ou du nombre de ressources définies sur la tâche. Le programme de tâche est basé sur les informations d’utilisateur. Pour ces tâches, l’allocation d’effort par période de temps de l’échelle de temps sélectionnée n’a aucun facteur de limitation. Tous les efforts de la tâche sont divisés équitablement et alloués à chaque période de temps sur l’échelle de temps sélectionnée.  
  
De cette façon, le modèle de tâche défini sur la tâche détermine la distribution ou l’allocation de l’effort par période de temps dans les estimations par phases de temps.  
  
## <a name="grouping-and-time-phasing-options"></a>Options de groupement et d’échelonnement  
Cette vue vous aide à comprendre la distribution des estimations d’effort, de coût et de vente sur une base quotidienne, hebdomadaire, mensuelle ou annuelle. L’option Grouper par permet de pivoter les données des estimations sur deux autres dimensions : catégorie et ressource. Dans la vue grille et la vue par phases de temps, vous pouvez sélectionner les champs à afficher. Le total pour chacun des blocs horaires est affiché dans la partie inférieure indiquant le total des efforts, coûts estimés et ventes pour le jour, la semaine, le mois ou l'année.  
  
Les prix de revient et de ventes par défaut dépendent de la date. Lorsque les tarifs pour les rôles changent, ce sera plus transparent dans la vue par phases de temps lorsque vous affichez les données d’estimation pivotées sur « ressource » et par phases de temps par semaine.  
  
## <a name="expense-estimates"></a>Estimations de dépenses  
Toutes les dépenses qui seront engagées dans le projet qui ne sont pas directement associées à la main d'œuvre peuvent être enregistrées dans des estimations de projet dans la vue grille. Vous pouvez le faire à l’aide de l’option **Ajouter l’estimation des dépenses** dans la vue grille. Les estimations des dépenses peuvent être enregistrées pour une tâche spécifique ou le projet entier. Vous pouvez choisir des catégories de dépenses sur ces lignes et choisir une date provisoire à laquelle la dépense devrait être engagée. Si le coût et les tarifs associés ont des prix par défaut, ou des pourcentages de majoration définis pour les catégories de dépenses, les valeurs seront transférées sur la ligne d’estimation sur l’association.  
  
### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../psa/project-manager-guide.md)
