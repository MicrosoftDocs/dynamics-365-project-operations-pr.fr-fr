---
title: Résoudre les prix de vente pour les estimations et les chiffres réels de projet
description: Cette rubrique fournit des informations sur la résolution des prix de vente sur les estimations et les chiffres réels de projet.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8aa731d48a3ce39dfbf4fc1e5934b0844caf2953
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575716"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Résoudre les prix de vente pour les estimations et les chiffres réels de projet

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

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Résolution des taux de vente sur les lignes de chiffres réels et d’estimation pour le matériel

Dans Project Operations, les lignes d’estimation pour le matériel sont utilisées pour désigner les détails de la ligne de devis et de contrat pour le matériel et les lignes d’estimation de matériel du projet.

Une fois le tarif des ventes résolu, le système exécute les étapes suivantes pour définir le prix de vente unitaire par défaut.

1. Le système utilise la combinaison des champs **Produit** et **Unité** sur la ligne d’estimation pour que le matériel corresponde aux lignes d’élément tarifaire dans la liste de prix qui a été résolue.
2. Si le système trouve une ligne d’élément tarifaire qui a un taux de vente pour la combinaison des champs **Produit** et **Unité** et que la méthode de tarification est **Montant en devise**, le prix de vente spécifié sur la ligne de tarif est utilisé.
3. Si les valeurs des champs **Produit** et **Unité** ne correspondent pas, le taux de vente par défaut est égal à zéro.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
