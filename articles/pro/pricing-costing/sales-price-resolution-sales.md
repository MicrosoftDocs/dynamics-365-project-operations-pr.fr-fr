---
title: Déterminer les prix de vente pour les estimations et les chiffres réels de projet
description: Cet article fournit des informations sur la façon dont les prix de vente sur les estimations de projet et les chiffres réels sont déterminés.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475181"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Déterminer les prix de vente pour les estimations et les chiffres réels de projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Pour déterminer les prix de vente dans les estimations et les chiffres réels dans Microsoft Dynamics 365 Project Operations, le système utilise d’abord la date et la devise du devis entrant ou du contexte des chiffres réels pour déterminer les tarifs de vente. Dans le contexte des chiffres réels en particulier, le système utilise le champ **Date de la transaction** pour déterminer quels tarifs sont applicables. La valeur **Date de la transaction** de l’estimation entrante ou réelle est comparée aux valeurs **Date de début effective (sans fuseau horaire)** et **Date de fin effective (sans fuseau horaire)** sur la liste de prix. Une fois les tarifs de vente déterminés, le système définit le taux de vente ou le taux de facturation.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Détermination des taux de vente sur les lignes réelles et estimées pour le temps

Contexte de devis pour **Temps** fait référence à :

- Détails de la ligne de devis pour **Temps**.
- Détails de la ligne de contrat pour **Temps**.
- Attributions de ressources sur un projet.

Le contexte de chiffres réels pour **Temps** fait référence à :

- Lignes de journal de saisie et de correction pour **Temps**.
- Lignes de journal créées lorsqu’une entrée de temps est soumise.
- Détails de la ligne de facture pour **Temps**. 

Une fois le tarif des ventes déterminé, le système exécute les étapes suivantes pour saisir le taux de facturation par défaut.

1. Le système associe la combinaison des champs **Rôle** et **Unité d’allocation des ressources** dans le contexte d’estimation ou réel pour que **Temps** corresponde aux lignes de prix du rôle sur le tarif. Cette correspondance suppose que les dimensions de tarification prêtes à l’emploi sont utilisées pour les taux de facturation. Si vous avez configuré la tarification sur d’autres champs que **Rôle** et **Unité d’allocation des ressources** ou sur des champs supplémentaires, c’est cette combinaison qui sera utilisée pour récupérer une ligne de prix de rôle correspondante.
1. Si le système trouve une ligne de prix de rôle qui a un taux de facturation pour la combinaison des champs **Rôle** et **Unité d’allocation des ressources**, ce taux de facturation est celui par défaut.
1. Si le système ne parvient pas à faire correspondre les valeurs des champs **Rôle** et **Unité d’allocation des ressources**, il récupère les lignes de prix de rôle dont les valeurs correspondent au champ **Rôle**, sauf les valeurs nulles du champ **Unité des ressources**. Une fois que le système a trouvé un enregistrement de prix de rôle correspondant, il utilisera par défaut le taux de facturation par défaut. Cette correspondance suppose une configuration prête à l’emploi pour la priorité relative de **Rôle** par rapport à **Unité d’allocation des ressources** comme dimension de tarification des ventes.

> [!NOTE]
> Si vous configurez une hiérarchisation différente des champs **Rôle** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle dont les valeurs correspondent à chaque valeur de dimension de prix par ordre de priorité. Les lignes qui ont des valeurs nulles pour ces dimensions viennent en dernier.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Détermination des taux de vente sur les lignes réelles et estimées pour les dépenses

Contexte de devis pour **Dépense** fait référence à :

- Détails de la ligne de devis pour **Dépense**.
- Détails de la ligne de contrat pour **Dépense**.
- Lignes d’estimation de dépense sur un projet.

Le contexte de chiffres réels pour **Dépense** fait référence à :

- Lignes de journal de saisie et de correction pour **Dépense**.
- Lignes de journal créées lorsqu’une entrée de dépense est soumise.
- Détails de la ligne de facturation pour **Dépense**. 

Une fois le tarif des ventes résolu, le système exécute les étapes suivantes pour définir le prix de vente unitaire par défaut.

1. Le système utilise une combinaison des champs **Catégorie** et **Unité** sur la ligne d’estimation pour qu’une **Dépense** corresponde aux lignes de prix de la catégorie sur le tarif qui a été résolu.
1. Si le système trouve une ligne de prix de catégorie qui a un taux de vente pour la combinaison de champs **Catégorie** et **Unité**, alors le taux de vente est défini par défaut.
1. Si le système trouve une ligne de prix de catégorie correspondante, la méthode de tarification peut être utilisée pour le prix de vente par défaut. Le tableau ci-dessous montre le comportement par défaut des prix des dépenses dans Project Operations.

    | Context | Mode de tarification | Prix par défaut |
    | --- | --- | --- |
    | Estimation | Prix unitaire | Basé sur la ligne de prix de la catégorie. |
    |        | À prix coûtant | 0.00 |
    |        | Majoration du coût | 0.00 |
    | Réel | Prix unitaire | Basé sur la ligne de prix de la catégorie. |
    |        | À prix coûtant | Basé sur les chiffres réels du coût associé. |
    |        | Majoration du coût | Appliquer une majoration telle que définie par la ligne de prix de catégorie sur les chiffres réels du coût associé. |

1. Si le système ne correspond pas aux valeurs **Catégorie** et **Unité**, le taux de vente est défini sur **0** (zéro) par défaut.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Détermination des taux de vente sur les lignes de chiffres réels et d’estimation pour le matériel

Contexte de devis pour **Matériel** fait référence à :

- Détails de la ligne de devis pour **Matériel**.
- Détails de la ligne de contrat pour **Matériel**.
- Lignes d’estimation du matériel du projet.

Le contexte de chiffres réels pour **Matériel** fait référence à :

- Lignes de journal de saisie et de correction pour **Matériel**.
- Lignes de journal créées lorsqu’un journal d’utilisation du matériel est soumis.
- Détails de la ligne de facturation pour **Matériel**. 

Une fois le tarif des ventes résolu, le système exécute les étapes suivantes pour définir le prix de vente unitaire par défaut.

1. Le système utilise la combinaison des champs **Produit** et **Unité** sur la ligne d’estimation pour que le **matériel** corresponde aux lignes d’élément tarifaire dans la liste de prix qui a été résolue.
1. Si le système trouve une ligne d’élément tarifaire qui a un taux de vente pour la combinaison des champs **Produit** et **Unité** et que la méthode de tarification est **Montant en devise**, le prix de vente spécifié sur la ligne de tarif est utilisé. 
1. Si les valeurs **Produit** et **Unité** des champs ne correspondent pas ou si la méthode de tarification est différente du champ **Montant en devise**, le taux de vente est défini sur **0** (zéro) par défaut. Ce problème se produit, car Project Operations ne prend en charge que la méthode de tarification **Montant en devise** pour les matériaux utilisés sur un projet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
