---
title: Listes de prix par défaut
description: Cet article explique comment copier des listes de prix de revient et de ventes par défaut dans Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410259"
---
# <a name="default-price-lists"></a>Listes de prix par défaut

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

## <a name="sales-price-lists"></a>Tarifs de vente

Chaque devis et contrat de projet dans Dynamics 365 Project Operations contient une liste de prix de vente par défaut. 

### <a name="price-list-default-on-project-quotes"></a>Liste de prix par défaut sur les devis de projet
Le système effectue le processus suivant pour déterminer le tarif par défaut sur un devis de projet :

1. Le système examine les listes de prix qui sont jointes aux listes de prix de projet du compte. 
1. Si aucune liste de prix de projet n'est associée à l’enregistrement de compte, le système examine les listes de prix de vente attachées aux paramètres de projet qui correspondent à la devise du devis de projet.
1. Ensuite, le système vérifie la date de validité des listes de prix qui correspondent à la plage de dates du devis de projet. Spécifiquement, la date de création du devis.
1. S’il existe plusieurs listes de prix en vigueur à la date du devis de projet, toutes les listes de prix par défaut figurent dans le devis de projet.
1. Si aucun tarif n’est en vigueur pour la date du devis de projet, il n’y a pas de tarif de projet par défaut dans le devis de projet. Un message d’avertissement apparaîtra sur le devis du projet. Le message indique que les chiffres réels et les estimations du projet ne seront pas facturés car aucun tarif de projet n’est jointe.

### <a name="price-list-default-on-project-contracts"></a>Liste de prix par défaut sur les contrats de projet 
Le système effectue le processus suivant pour déterminer le tarif par défaut sur un devis de contrat :

1. Si le contrat est créé à partir d’un devis, les listes de prix du projet sur le devis sont copiées séparément et jointes au contrat de projet.
1. Si le contrat est créé à partir de zéro, le système examine les listes de prix qui sont jointes aux listes de prix de projet du compte. Si des listes de prix de projet ne sont pas associées à l’enregistrement de compte, le système examine les listes de prix de vente attachées aux paramètres de projet qui correspondent à la devise du contrat de projet.
1. Ensuite, le système vérifie la date de validité des listes de prix qui correspondent à la plage de dates du contrat de projet. Spécifiquement, la date de création du contrat.
1. S’il existe plusieurs listes de prix en vigueur à la date du contrat, toutes les listes de prix par défaut figurent dans le devis de contrat.
1. Si aucun tarif n’est en vigueur pour la date du contrat, il n’y a pas de tarif de projet par défaut dans le contrat. Un message d’avertissement apparaîtra sur le contrat du projet. Le message indique que les chiffres réels et les estimations du projet ne seront pas facturés car aucun tarif de projet n’est jointe.

## <a name="cost-price-lists"></a>Listes des prix de revient

Les listes de prix de revient n’utilisent par défaut aucune entité dans Project Operations. La détermination du prix de revient à utiliser pour les coûts du projet se fait toujours sur une base par transaction. Le système effectue le processus suivant pour déterminer le tarif à utiliser pour les coûts de projet :

1. Le système examine les tarifs joints à l’unité d’organisation contractante du projet.
1. Ensuite, le système examine la date de validité des listes de prix qui correspondent à la date du devis entrant ou de la ligne réelle.

    - *Contexte d’estimation* fait référence aux trois contextes d’estimation dans Project Operations :

        - Ligne d’estimation de projet
        - Détail de la ligne de devis
        - Détails de la ligne de contrat

    - *Contexte réel* fait référence aux trois sources de chiffres réels dans Project Operations :

       - Lignes de journal de saisie créées manuellement ou lignes de journal de correction créées dans un journal de correction
       - Lignes de journal créées lors de la soumission des journaux d’utilisation du temps, des dépenses ou du matériel
       - Détail de la ligne de facture

    Lorsque Project Operations correspond à la date d’effet du détail de la ligne de journal entrant ou de la ligne de facture dans le champ *Contexte réel*, il utilise le champ **Date de transaction**.

    - S’il existe plusieurs listes de prix valables pour la date de l’estimation entrante ou réelle, le tarif créé le plus récemment est sélectionnée.
    - S’il n’y a pas de tarif joint à l’unité d’organisation contractante du projet, le système examine les listes de prix de revient jointes aux paramètres de projet qui correspondent à la devise du devis de projet.

## <a name="enable-multi-currency-cost-price-list"></a>Activer la liste des prix de revient en devises multiples

Ce paramètre se trouve sur **Réglages** \> **Paramètres**. La valeur par défaut est **Non**.

Lorsque ce paramètre est activé (c’est-à-dire que la valeur est définie sur **Oui**), le système se comporte de la manière suivante :

- Il permet d’associer les listes de prix de revient dans toute devise à l’unité d’organisation. Par exemple, une liste de prix de revient dans la devise EUR peut être associée à une unité organisationnelle dans la devise USD. Le système continuera à valider que les listes de prix de revient qui sont jointes à une unité organisationnelle n’ont pas de dates d’effet qui se chevauchent.
- Il valide que les listes de prix de revient qui sont jointes aux paramètres du projet n’ont pas de dates d’effet qui se chevauchent, même si elles ont des devises différentes. Ce comportement diffère du comportement par défaut (c’est-à-dire le comportement lorsque la valeur est définie sur **Non**). Dans le comportement par défaut, seules les listes de prix de revient qui ont la **même** devise sont validées pour une validité de dates sans chevauchement.
- Pour un contexte de transaction entrante, il détermine la liste de prix de revient en fonction de la date d’effet uniquement. Ce comportement diffère du comportement par défaut, où le système sélectionne la liste de prix de revient qui correspond à la fois à la devise du projet et à la date d’effet.

En raison de ces changements de comportement, les clients de Project Operations pourront maintenir une liste de prix de revient globale qui sera pertinente pour l’ensemble de l’entreprise. Ils n’auront pas besoin d’avoir des listes de prix dans chaque devise d’opérations. La liste de prix globale aura une date d’effet et permettra de configurer des taux de coût dans n’importe quelle devise pour une combinaison spécifique de valeurs de dimension de tarification. La devise de la liste de prix de revient est utilisée uniquement pour saisir des valeurs par défaut lorsque les enregistrements d’élément **Tarifs des rôles**, **Prix par catégorie** et **Tarifs** sont créés. Elle ne sera pas utilisée pour déterminer les tarifs.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
