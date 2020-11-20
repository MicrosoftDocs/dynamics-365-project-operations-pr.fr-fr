---
title: Devis – Concepts clé – Simplifié
description: Cette rubrique offre des informations sur l’utilisation des devis de projet dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178003"
---
# <a name="quotes---key-concepts---lite"></a>Devis – Concepts clé – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Les concepts clés suivants doivent être pris en compte avant de commencer à utiliser des devis de projet dans Dynamics 365 Project Operations :

## <a name="contracting-unit"></a>Unité contractuelle

L’unité contractuelle représente la division ou le cabinet qui est propriétaire de la livraison du projet. Vous pouvez configurer les coûts des ressources de l’unité contractuelle. Lorsque vous spécifiez le coût de ressource pour une ressource de l’unité contractuelle, vous pourrez également définir différents taux de coût pour les ressources dont cette unité contractuelle emprunte, ou d’autres divisions ou cabinets au sein de l’entreprise. Ceux-ci sont appelés prix de transfert, emprunt de ressources ou prix de change. Lorsque vous configurez le coût d’emprunt de ressources auprès d’autres divisions, vous pouvez également choisir de configurer ces taux de coût dans la devise de la division de prêt.

## <a name="cost-currency"></a>Devise du coût

La devise de coût de Project Operations est la devise dans laquelle les coûts sont déclarés. Cette devise est dérivée de la devise attachée au champ **Unité contractuelle** sur le devis, le contrat et le projet. Les coûts peuvent être enregistrés dans n’importe quelle devise par rapport à un projet. Cependant, il existe une conversion de devise entre les coûts de devise enregistrés dans la devise de coût du projet.

Étant donné que les taux de change de la plateforme CDS ne peuvent pas entrer en vigueur à la date, les totaux à l’écran du coût peuvent changer au fil du temps si vous mettez à jour les taux de change. Cependant, les coûts enregistrés dans la base de données restent inchangés, car les montants sont stockés dans la devise dans laquelle ils ont été engagés.

## <a name="sales-currency"></a>Devise de vente

La devise de vente dans Project Operations est la devise dans laquelle les montants des ventes estimés et réels sont enregistrés et affichés. C’est également la devise dans laquelle le client est facturé pour la transaction. Sur un devis de projet, la devise de vente est par défaut celle de l’enregistrement client ou compte et peut être modifiée lors de la création du devis. Une fois le devis enregistré, la devis de vente ne peut pas être modifiée. Les tarifs des produits et des projets par défaut sont basés sur la devise de vente du devis.

Contrairement aux coûts, les valeurs de vente ne peuvent être enregistrées que dans la devise de vente.

## <a name="billing-method"></a>Mode de facturation

Les projets ont généralement des modèles de contrats à frais fixes et basés sur la consommation. Ceci est représenté dans Project Operations comme **Mode de facturation** et a deux valeurs, temps et matériel, et prix fixe.

- **Temps et matériel :** Il s’agit d’un modèle de contrat basé sur la consommation dans lequel chaque coût encouru est soutenu par les revenus correspondants. Au fur et à mesure que vous estimez ou engagez plus de coûts, les ventes estimées et réelles correspondantes augmenteront également. Vous pouvez spécifier des limites à ne pas dépasser sur les lignes de devis qui utilisent ce mode de facturation. Cela plafonnera les revenus réels. Les revenus estimés ne sont pas affectés par les limites à ne pas dépasser.
- **Prix fixe :** Il s’agit d’un modèle de contrat à honoraires fixes qui indique que les valeurs de vente seront indépendantes des coûts engagés. La valeur des ventes est fixe et ne change pas lorsque vous estimez ou engagez des coûts supplémentaires.

## <a name="project-price-lists"></a>Tarifs des projets

Les tarifs de projet sont des tarifs qui sont utilisés pour les prix par défaut, et non les taux de coût, pour le temps, les dépenses et d’autres composants liés au projet. Il peut y avoir plusieurs tarifs et chacun peut avoir sa propre date de validité pour chaque devis de projet. Le chevauchement des dates de validité sur les tarifs du projet n’est pas pris en charge par Project Operations.

## <a name="product-price-lists"></a>Tarifs des produits

Les tarifs de produits sont des tarifs utilisés pour les prix par défaut, et non les taux de coût, pour les lignes basées sur les produits d’un devis. Il n’existe qu’un seul tarif par devis.

## <a name="transaction-classes"></a>Classes de transaction

Project Operations prend en charge quatre types de classes de transactions :

- Durée
- Dépense
- Matériel
- Frais

Les valeurs de coût et de vente peuvent être estimées et engagées sur des classes de transactions Temps, Dépenses et Matériel. Les Frais sont une catégorie de transactions à revenus uniquement.

## <a name="work-entities-and-billing-entities"></a>Entités de travail et entités de facturation

Les entités qui représentent le travail sont Projets et Tâches. Les entités qui représentent la facturation sont Lignes de devis et Lignes de contrat. Vous pouvez lier différentes entités de travail aux options de facturation en les associant à Lignes de devis ou de contrat.

## <a name="multi-customer-deals"></a>Transactions multi-clients

Les transactions multi-clients se produisent lorsqu’il y a plus d’un client à facturer. Les exemples courants comprennent :

- **Entreprises OEM et leurs partenaires :** Les partenaires et revendeurs vendent un produit avec des services à valeur ajoutée. Il s’agit généralement d’un scénario où, lors d’une transaction particulière avec un client, l’OEM propose de financer une partie du projet. 

- **Projets du secteur public :** Plusieurs organismes d’une administration locale acceptent de financer un projet et sont facturés selon une répartition préalablement convenue. Par exemple, un rectorat et la ville ou le département acceptent de financer la construction d’une piscine.

## <a name="invoice-schedules"></a>Planifications de facture

Les planifications de facture sont spécifiques à chaque ligne de devis et sont également facultatifs. Les planifications de facture sont créées en fonction de certaines dates de début et de fin et de la fréquence de facturation. Les planifications de facture sont utilisées à l’étape du contrat lorsque le processus de création automatique de facture est configuré. À la phase de devis, les planifications sont facultatives. Lorsque les planifications de facture sont créées à la phase **Devis**, elles sont copiées dans le contrat de projet créé lorsqu’un devis de projet est remporté.

## <a name="changes-from-dynamics-365-sales-quote"></a>Modifications par rapport au devis Dynamics 365 Sales :

Les devis Project Operations sont basés sur les devis Dynamics 365 Sales. Cependant, il existe des différences importantes dans les fonctionnalités dont vous devez être conscient :

- Les actions **Réviser** et **Activer** ne sont pas prises en charge.
- Les devis Project Operations ont deux types de lignes différents. L’une est destinée aux projets et l’autre aux produits.
- Les devis Project Operations ont leurs propres éléments de formulaire et d’interface utilisateur, des règles métier, une logique métier dans les plug-ins et des scripts côté client qui les rendent uniques à partir des devis de vente.

Pour ces raisons, il n’est pas recommandé d’utiliser de manière interchangeable un devis de vente et un devis Project Operations.
