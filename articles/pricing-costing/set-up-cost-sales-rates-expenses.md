---
title: Configurer les taux de coûts et de vente pour les dépenses
description: Cette rubrique fournit des informations sur la configuration des taux de coûts et de vente pour les catégories de transactions et des dépenses.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c5e7b1ab03a170ca95a005985a13aaff7494f95ca15cf1ce726674ae9a14222
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986218"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurer les taux de coûts et de vente pour les dépenses

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez configurer les prix de revient et de vente pour les catégories de transaction dans Dynamics 365 Project Operations. Étant donné que le coût de revient et les prix de vente sont conçus pour les dépenses, chaque catégorie de transaction qui les inclut doit également être configurée comme catégorie de dépenses. Cette configuration garantit la précision des fonctionnalités en aval. Le coût de revient et les prix de vente des catégories de transaction ne peuvent être répertoriés que dans une seule devise, qui doit être la devise de l’en-tête du tarif.

Pour configurer les taux de coûts et de vente pour les catégories de transaction, procédez comme suit. 

1. Accédez à **Ventes** > **Clients** > **Listes de prix**.
2. Sélectionnez **Nouveau** pour créer un nouveau tarif. 
3. Sur **Prix de la catégorie**, dans le menu de la sous-grille, sélectionnez **Nouveau prix de la catégorie**. 
4. Sur la page **Création rapide**, entrez la catégorie de transaction et l’unité pour lesquelles vous créez le nouveau prix.

Le tableau suivant répertorie les champs de l’onglet **Général** et de la page **Création rapide** d’une ligne de prix de catégorie que vous devez garder à l’esprit lorsque vous créez des prix de catégorie sur un tarif de vente ou de prix de revient.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Catégorie de transaction | Onglet **Général** et pages **Création rapide** | Sélectionnez la catégorie de transaction pour laquelle vous créez un prix de vente ou un prix de revient. | La catégorie de transaction sur l’estimation entrante ou les chiffres réels pour les dépenses sera mise en correspondance avec cette ligne pour établir le taux de coût ou de vente par défaut de la catégorie de transaction. |
| Planification d’unités | Onglet **Général** et pages **Création rapide** | La planification d’unités est par défaut celle de la catégorie de transaction. | Il n’y a pas d’impact en aval à partir de ce champ. |
| Unité | Onglet **Général** et pages **Création rapide** | Sélectionnez l’unité pour laquelle les taux sont définis. | L’unité sur l’estimation entrante ou les chiffres réels est comparée à l’unité sur cette ligne pour établir le taux par défaut sur l’estimation ou les chiffres réels des dépenses. |
| Mode de tarification | Onglet **Général** et pages **Création rapide** | Les valeurs possibles du champ **Mode de tarification** sont, **Prix unitaire**, **À prix coûtant** et **Majoration du coût**. | Lors de la configuration du prix, si vous sélectionnez **Prix unitaire**, le champ **Pourcentage** de la ligne de prix de la catégorie est verrouillé. Si **À prix coûtant** est sélectionné, les champs **Prix** et **Pourcentage** sont verrouillés sur le tarif de vente. Si vous sélectionnez **Majoration du coût**, le champ **Prix** est verrouillé dans le tarif de vente. Sur une ligne de chiffres réelles entrants pour les dépenses, le mode de facturation **À prix coûtant** ou **Majoration du coût** entraîne l’attribution dans la ligne de vente non facturée correspondante d’un prix égal au chiffre réel ou calculé du coût en tant que valeur de majoration du prix. |
| Tarif | Onglet **Général** et pages **Création rapide** | Configurez un taux unitaire pour la catégorie de transaction et la combinaison d’unité. Par exemple, les frais kilométriques sont de 10 USD par mile et de 8 USD par kilomètre. | Les frais kilométriques seront le taux par défaut sur le prix unitaire ou le coût de la ligne d’estimation entrante ou de chiffres réels pour une classe de transaction de dépenses.|
| Pourcentage | Onglet **Général** et pages **Création rapide** | Configurez un pourcentage du coût pour la catégorie de transaction et la combinaison d’unité. Par exemple, le taux de vente des billets d’avion devrait être majoré de 10 %% par rapport au coût des frais de billets d’avion engagés. | Ce pourcentage sur le coût n’est applicable sur un tarif de vente que lorsque le mode de tarification sélectionné est **Majoration sur le coût**. |
| Devise | Onglet **Général** et pages **Création rapide** | Par défaut, cette valeur provient de la devise de l’en-tête du tarif. Pour la tarification par catégorie de transaction, la devise ne peut pas être remplacée. | Cette devise est définie par défaut sur le prix unitaire de la ligne de chiffres réels entrants pour la classe de transaction de dépense pour le coût et les ventes. |

## <a name="pricing-methods-for-expenses"></a>Modes de tarification pour les dépenses

Lorsque vous configurez des prix par catégorie qui ne sont pertinents que dans le contexte de la tarification des dépenses, vous pouvez utiliser l’un des trois modes de tarification suivants :

- **Prix unitaire**
- **À prix coûtant**
- **Majoration du coût**

### <a name="price-per-unit"></a>Prix unitaire
Lorsque ce mode de tarification est sélectionné sur une ligne de prix de catégorie qui est liée à un tarif de vente, le prix est défini par défaut pour la combinaison de catégorie et d’unité à la fois dans l’estimation et dans les chiffres réels. Les estimation font référence aux lignes d’estimation du projet pour les dépenses, aux détails de la ligne du devis et aux détails de la ligne de contrat pour les dépenses.

### <a name="at-cost"></a>À prix coûtant
Lorsque ce mode de tarification est sélectionné sur la ligne de prix de catégorie qui est liée à un tarif de vente, le prix est défini par défaut pour la combinaison de catégorie et d’unité uniquement pour les chiffres réels. Par exemple, les chiffres réels de ventes non facturés pour la classe de transaction de dépenses. Le prix unitaire est défini sur les ventes non facturées réelles à partir du prix unitaire sur le coût réel de cette dépense. La définition du prix par défaut basé sur le coût n’est pas effectuée sur les estimations de projet pour les dépenses ou sur les détails de la ligne de devis et de la ligne de contrat pour les dépenses.

### <a name="markup-over-cost"></a>Majoration du coût
Lorsque ce mode de tarification est sélectionné sur la ligne de prix de catégorie qui est liée à un tarif de vente, le prix est défini par défaut pour la combinaison de catégorie et d’unité uniquement pour un chiffre réel de dépenses. Par exemple, les chiffres réels de ventes non facturés pour la classe de transaction de dépenses. Ce prix unitaire est défini sur les chiffres réels de ventes non facturés à une valeur calculée à partir du prix unitaire sur les chiffres réels de coût pour cette dépense après l’application du pourcentage de majoration défini. La définition du prix par défaut basé sur le coût n’est pas effectuée sur les estimations de projet pour les dépenses ou sur les détails de la ligne de devis et de la ligne de contrat pour les dépenses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
