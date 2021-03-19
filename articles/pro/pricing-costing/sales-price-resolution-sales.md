---
title: Résoudre des prix de vente pour les estimations et les chiffres réels – Simplifié
description: Cette rubrique fournit des informations sur la résolution des prix de revient des estimations et des chiffres réels.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25620704570fa702e1e5e09c83005be50f98f20a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274500"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Résoudre des prix de vente pour les estimations et les chiffres réels – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Lorsque les prix de vente dans les estimations et les chiffres réels sont résolus dans Dynamics 365 Project Operations, le système utilise d’abord la date et la devise du devis ou contrat du projet associé pour résoudre les tarifs de vente. Une fois le tarif de vente est résolu, le système résout le taux de vente ou le taux de facturation.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Résoudre les taux de vente sur les lignes réelles et estimées pour le temps

Dans Project Operations, les lignes d’estimation du temps sont utilisées pour indiquer la ligne de devis et les détails de la ligne de contrat pour le temps et les affectations de ressources sur le projet.

Une fois le tarif des ventes résolu, le système exécute les étapes suivantes pour définir le taux de facturation par défaut.

1. Le système utilise les champs **Rôle** et **Unité d’allocation des ressources** sur la ligne d’estimation pour Temps, afin de faire correspondre les lignes de prix de rôle dans le tarif résolu. Cette correspondance suppose que les dimensions de tarification prêtes à l’emploi sont utilisées pour les taux de facturation. Si vous avez configuré la tarification sur d’autres champs que **Rôle** et **Unité d’allocation des ressources** ou sur des champs supplémentaires, c’est cette combinaison qui sera utilisée pour récupérer une ligne de prix de rôle correspondante.
2. Si le système trouve une ligne de prix de rôle qui a un taux de facturation pour la combinaison des champs **Rôle** et **Unité d’allocation des ressources**, ce taux de facturation est celui par défaut.
3. Si le système ne parvient pas à faire correspondre les valeurs des champs **Rôle** et **Unité d’allocation de ressources**, alors il récupère les lignes de prix de rôle avec un rôle correspondant, sauf les valeurs nulles de **Unité d’allocation de ressources**. Une fois que le système a trouvé un enregistrement de prix de rôle correspondant, il utilisera par défaut le taux de facturation de cet enregistrement. Cette correspondance suppose une configuration prête à l’emploi pour la priorité relative de **Rôle** par rapport à **Unité d’allocation des ressources** comme dimension de tarification des ventes.

> [!NOTE]
> Si vous avez configuré une hiérarchisation différente des valeurs **Rôle** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle avec des valeurs correspondantes de chacune des valeurs de dimension de tarification par ordre de priorité avec les lignes qui ont des valeurs nulles pour ces dimensions venant en dernier.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Résoudre les taux de vente sur les lignes réelles et estimées pour les dépenses

Dans Project Operations, les lignes d’estimation des dépenses sont utilisées pour indiquer la ligne de devis et les détails de la ligne de contrat pour les dépenses et les lignes d’estimation de dépenses sur le projet.

Une fois le tarif des ventes résolu, le système exécute les étapes suivantes pour définir le prix de vente unitaire par défaut.

1. Le système utilise une combinaison des champs **Catégorie** et **Unités** sur la ligne d’estimation pour qu’une dépense corresponde aux lignes de prix de la catégorie sur le tarif qui a été résolu.
2. Si le système trouve une ligne de prix de catégorie qui a un taux de vente pour la combinaison de champs **Catégorie** et **Unité**, alors le taux de vente est défini par défaut.
3. Si le système trouve une ligne de prix de catégorie correspondante, la méthode de tarification peut être utilisée pour le prix de vente par défaut. Le tableau ci-dessous montre le comportement par défaut du prix des dépenses dans Project Operations.

    | Contexte | Mode de tarification | Prix par défaut |
    | --- | --- | --- |
    | Estimation | Prix unitaire | Basé sur la ligne de prix de la catégorie |
    | &nbsp; | À prix coûtant | 0.00 |
    | &nbsp; | Majoration du coût | 0.00 |
    | Réel | Prix unitaire | Basé sur la ligne de prix de la catégorie |
    | &nbsp; | À prix coûtant | Basé sur les chiffres réels du coût associé |
    | &nbsp; | Majoration du coût | Appliquer une majoration telle que définie par la ligne de prix de catégorie sur les chiffres réels du coût associé |

4. Si le système ne parvient pas à faire correspondre les valeurs des champs **Catégorie** et **Unité**, le taux de vente par défaut est zéro (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]