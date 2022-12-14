---
title: Concepts uniques aux contrats de projet
description: Cet article fournit des informations sur les concepts clés des contrats de projet.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8776188add2094bbf64530b361bb7fd029ab19ba
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825702"
---
# <a name="concepts-unique-to-project-contracts"></a>Concepts uniques aux contrats de projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_



Cet article fournit les concepts clés à connaître avant de commencer à utiliser les contrats de projet dans Dynamics 365 Project Operations :

## <a name="contracting-unit"></a>Unité contractuelle

L’unité contractuelle représente la division ou le cabinet qui est propriétaire de la livraison du projet. Vous pouvez configurer les coûts des ressources pour chaque unité contractante. Lorsque vous spécifiez le coût d’une ressource, vous pouvez également définir différents taux de coût pour les ressources. Cette unité contractante emprunte ces ressources à d’autres divisions ou pratiques au sein de l’entreprise. Les taux de coûts pour les ressources sont appelés prix de transfert, emprunt de ressources ou prix de change. Lorsque vous configurez les taux des coûts pour emprunter des ressources auprès d’autres divisions, utilisez la devise de la division de prêt.

## <a name="cost-currency"></a>Devise du coût

La devise de coût est la devise dans laquelle les coûts sont déclarés sur l’écran. Cette devise est dérivée de la devise attachée au champ **Unité contractuelle** sur le contrat et le projet. Les coûts peuvent être enregistrés dans n’importe quelle devise par rapport à un projet. Cependant, il existe une conversion de devise entre les coûts de devise enregistrés dans la devise de coût du projet en cas d’indication sur l’écran.

Étant donné que les taux de change de la plateforme Common Data Service (CDS) ne peuvent pas entrer en vigueur à la date, les totaux à l’écran du coût peuvent changer au fil du temps si vous mettez à jour les taux de change. Cependant, les coûts enregistrés dans la base de données restent inchangés, car les montants sont stockés dans la devise dans laquelle ils ont été engagés.

## <a name="sales-currency"></a>Devise de vente

La devise de vente dans Project Operations est la devise dans laquelle les montants des ventes estimés et réels sont enregistrés et affichés. La devise de vente est également celle dans laquelle la transaction est facturée au client. Sur un contrat de projet, la devise de vente est par défaut celle de l’enregistrement client ou compte et peut être modifiée lors de la création du contrat. Lorsqu’un contrat est créé en clôturant un devis comme gagné, la devise du contrat est par défaut la devise du devis.

Lorsque vous créez un contrat de projet à partir de zéro, le champ **Devise de vente** ne peut pas être modifié. Les tarifs des produits et des projets par défaut sont basés sur cette devise dans le contrat.

Contrairement aux coûts, les valeurs de vente ne peuvent être enregistrées que dans la devise de vente.

## <a name="billing-method"></a>Mode de facturation

Il y a généralement deux types de modèles de contrats pour les projets à frais fixes et basés sur la consommation. Ces modèles sont représentés dans Project Operations comme des méthodes de facturation avec deux valeurs possibles :

- Temps et matériel : Un modèle de contrat basé sur la consommation dans lequel chaque coût encouru est soutenu par les revenus correspondants. Au fur et à mesure que vous estimez ou engagez plus de coûts, les ventes estimées et réelles correspondantes augmenteront également. Spécifiez les limites à ne pas dépasser sur les lignes de contrat qui ont cette méthode de facturation qui plafonne les revenus réels. Les revenus estimés ne sont pas affectés par les limites à ne pas dépasser.
- Prix fixe : Un modèle de contrat à honoraires fixes qui indique que les valeurs de vente seront indépendantes des coûts engagés. La valeur des ventes est fixe et ne change pas lorsque vous estimez ou engagez des coûts supplémentaires.

## <a name="project-price-lists"></a>Tarifs des projets

Les tarifs de projet sont utilisés pour les prix par défaut, et non les taux de coût, pour le temps, les dépenses et d’autres composants liés au projet. Il peut y avoir plusieurs listes de prix. Chaque tarif a sa propre date de validité pour chaque contrat de projet. Le chevauchement des dates de validité sur les tarifs du projet n’est pas pris en charge par Project Operations.

Lorsqu’un contrat de projet est créé en remportant un devis de projet, les listes de prix de projet sont copiées avec le nom et la date du contrat inclus. La copie de ces informations constitue une tarification personnalisée pour les composants du projet sur ce contrat de projet.

## <a name="product-price-lists"></a>Tarifs des produits

Les tarifs de produits sont utilisés pour les prix par défaut, et non les taux de coût, pour les lignes basées sur les produits d’un contrat. Il n’existe qu’un seul tarif par contrat.

## <a name="transaction-classes"></a>Classes de transaction

Project Operations prend en charge quatre types de classes de transactions :

- Temps
- Dépenses
- Matière
- Frais

Les valeurs de coût et de vente peuvent être estimées et engagées sur des classes de transactions Temps, Dépenses et Matériel. Les Frais sont une catégorie de transactions à revenus uniquement.

## <a name="work-entities-and-billing-entities"></a>Entités de travail et entités de facturation

Les entités qui représentent le travail sont des projets et des tâches. Les entités qui représentent les aspects de facturation sont des lignes de contrat. Vous pouvez lier différentes entités de travail à des options de facturation en les liant à des lignes de contrat.

## <a name="multi-customer-deals"></a>Transactions multi-clients

Les transactions multi-clients se produisent lorsqu’il y a plusieurs clients sur une affaire. Voici quelques exemples courants :

- Les entreprises OEM et leurs partenaires : les partenaires et les revendeurs vendent un produit avec certains services à valeur ajoutée, impliquant généralement un accord particulier avec un client. L’OEM propose de financer une partie du projet. 

- Projets du secteur public : Plusieurs organismes d’une administration locale acceptent de financer un projet et sont facturés selon une répartition préalablement convenue. Par exemple, le rectorat et le gouvernement local acceptent de financer la construction d’une piscine.

## <a name="invoice-schedules"></a>Planifications de facture

Les calendriers de facturation sont spécifiques à chaque ligne de contrat et sont nécessaires pour que la facturation automatique fonctionne. Les calendriers de facturation sont créés en fonction de certaines dates de début et de fin et de la fréquence de facturation. Les calendriers sont utilisés à l’étape du contrat, lorsque le processus de création automatique de facture est configuré. Lorsqu’un contrat de projet est créé à partir d’un devis, la planification de facture est copiée vers le contrat de projet depuis le devis.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Modifications du contrat Dynamics 365 Sales

Les contrats Project Operations sont basés sur les contrats Dynamics 365 Sales. Cependant, il existe d’importants écarts et différences dans les fonctionnalités dont vous devez être conscient :

- Les contrats Project Operations comportent deux types de lignes différentes, l’une pour les projets et l’autre pour les produits.
- Les contrats Project Operations ont leurs propres éléments de formulaire et d’interface utilisateur, des règles métier, une logique métier dans les plug-ins et des scripts côté client qui les rendent uniques à partir des contrats de vente.

Pour ces raisons, vous ne devez pas utiliser un contrat de vente et un contrat de projet de manière interchangeable.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
