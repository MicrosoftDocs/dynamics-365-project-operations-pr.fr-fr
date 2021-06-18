---
title: Listes de prix par défaut
description: Cette rubrique fournit des informations sur les ventes par défaut et les listes de prix de revient dans Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c204a8f0364a4be39974b101e834d4465b99f769
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000478"
---
# <a name="default-price-lists"></a>Listes de prix par défaut

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

## <a name="sales-price-lists"></a>Tarifs de vente

Chaque devis et contrat de projet dans Dynamics 365 Project Operations contient une liste de prix de vente par défaut. 

### <a name="price-list-default-on-project-quotes"></a>Liste de prix par défaut sur les devis de projet
Le système effectue le processus suivant pour déterminer le tarif par défaut sur un devis de projet :

1. Le système examine les listes de prix qui sont jointes aux listes de prix de projet du compte. 
2. Si des listes de prix de projet sont associées à l’enregistrement de compte, le système examine les listes de prix de vente attachées aux paramètres de projet qui correspondent à la devise du devis de projet.
3. Ensuite, le système vérifie la date de validité des listes de prix qui correspondent à la plage de dates du devis de projet. Spécifiquement, la date de création du devis.
4. S’il existe plusieurs listes de prix en vigueur à la date du devis de projet, toutes les listes de prix par défaut figurent dans le devis de projet.
5. Si aucun tarif n’est en vigueur pour la date du devis de projet, il n’y a pas de tarif de projet par défaut dans le devis de projet. Un message d’avertissement apparaîtra sur le devis du projet. Le message indique que les chiffres réels et les estimations du projet ne seront pas facturés car aucun tarif de projet n’est jointe.

### <a name="price-list-default-on-project-contracts"></a>Liste de prix par défaut sur les contrats de projet 
Le système effectue le processus suivant pour déterminer le tarif par défaut sur un devis de contrat :

1. Si le contrat est créé à partir d’un devis, les listes de prix du projet sur le devis sont copiées séparément et jointes au contrat de projet.
2. Si le contrat est créé à partir de zéro, le système examine les listes de prix qui sont jointes aux listes de prix de projet du compte. Si des listes de prix de projet ne sont pas associées à l’enregistrement de compte, le système examine les listes de prix de vente attachées aux paramètres de projet qui correspondent à la devise du contrat de projet.
4. Ensuite, le système vérifie la date de validité des listes de prix qui correspondent à la plage de dates du contrat de projet. Spécifiquement, la date de création du contrat.
5. S’il existe plusieurs listes de prix en vigueur à la date du contrat, toutes les listes de prix par défaut figurent dans le devis de contrat.
6. Si aucun tarif n’est en vigueur pour la date du contrat, il n’y a pas de tarif de projet par défaut dans le contrat. Un message d’avertissement apparaîtra sur le contrat du projet. Le message indique que les chiffres réels et les estimations du projet ne seront pas facturés car aucun tarif de projet n’est jointe.

## <a name="cost-price-lists"></a>Listes des prix de revient

Les listes de prix de revient n’utilisent par défaut aucune entité dans Project Operations. La détermination du prix de revient à utiliser pour les coûts du projet se fait toujours sur le moment. Le système effectue le processus suivant pour déterminer le tarif à utiliser pour les coûts de projet :

1. Le système examine d’abord les listes de prix attachées à l’unité d’organisation contractante du projet.
2. Le système examine ensuite la date de validité des listes de prix qui correspondent à la date du devis entrant ou de la ligne réelle. Dans cette situation, *ligne d’estimation* fait référence aux trois contextes d’estimation dans Project Operations :

    - Ligne d’estimation de projet
    - Détail de la ligne de devis
    - Détails de la ligne de contrat
  
3. S’il existe plusieurs listes de prix valables pour la date de l’estimation entrante ou réelle, le tarif créée le plus récemment est sélectionnée.
4. S’il n’y a pas de listes de prix attachées à l’unité d’organisation contractante du projet, le système examine les listes de prix de revient attachées aux paramètres de projet qui correspondent à la devise du devis de projet.
5. Ensuite, le système examine la date de validité des listes de prix qui correspondent à la date du devis entrant ou de la ligne réelle. 
6. S’il existe plusieurs listes de prix valables pour la date de l’estimation entrante ou réelle, le tarif créée le plus récemment est sélectionnée.
7. Si aucun tarif de revient associée aux paramètres du projet ne correspond à la devise et à la date de validité, le système définit par défaut le taux de coût sur zéro (0) sur le devis entrant ou la ligne réelle.


[!INCLUDE[footer-include](../includes/footer-banner.md)]