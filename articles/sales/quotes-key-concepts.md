---
title: Concepts propres aux devis basés sur des projets
description: Cet article fournit des informations sur les devis de projet dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824324"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Concepts propres aux devis basés sur des projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Avant de commencer à utiliser des devis de projet dans Microsoft Dynamics 365 Project Operations, vous devez connaître les concepts clés suivants.

## <a name="owning-company"></a>Société propriétaire

L’entreprise propriétaire représente l’entité juridique qui possède la livraison de projet. Le client sur le devis doit être un client valide dans cette entité juridique dans les applications de finance et d’opérations. La devise de la société propriétaire et la devise de l’unité contractante sélectionnée sur un devis basé sur un projet doivent correspondre.

## <a name="contracting-unit"></a>Unité contractante

Une unité contractuelle représente la division ou le cabinet qui est propriétaire de la livraison du projet. Vous pouvez configurer les coûts des ressources pour chaque unité contractante. Lorsque vous spécifiez les coûts de ressource pour une ressource de l’unité contractuelle, vous pouvez définir différents taux de coût pour les ressources dont cette unité contractuelle emprunte, ou d’autres divisions ou cabinets au sein de l’entreprise. Ceux-ci sont appelés prix de transfert, emprunt de ressources ou prix de change. Lorsque vous configurez le coût d’emprunt de ressources auprès d’autres divisions, vous pouvez configurer ces taux de coût dans la devise de la division de prêt.

## <a name="cost-currency"></a>Devise du coût

La devise de coût de Project Operations est la devise dans laquelle les coûts sont déclarés. Cette devise est dérivée de la devise attachée au champ **Unité contractuelle** sur le devis, le contrat et le projet. Les coûts peuvent être enregistrés dans n’importe quelle devise par rapport à un projet. Cependant, il existe une conversion de devise entre les coûts de devise enregistrés dans la devise de coût du projet.

Étant donné que les taux de change de la plateforme Dataverse ne peuvent pas entrer en vigueur à la date, les totaux à l’écran du coût peuvent changer au fil du temps si vous mettez à jour les taux de change. Cependant, les coûts enregistrés dans la base de données restent inchangés, car les montants sont stockés dans la devise dans laquelle ils ont été engagés.

## <a name="sales-currency"></a>Devise de vente

La devise de vente dans Project Operations est la devise dans laquelle les montants des ventes estimés et réels sont enregistrés et affichés. C’est également la devise dans laquelle le client est facturé pour la transaction. Sur un devis de projet, la devise de vente est par défaut celle de l’enregistrement client ou compte et peut être modifiée lors de la création du devis. Cependant, la devise de vente ne peut pas être modifiée une fois le devis enregistré. Les tarifs des produits et des projets par défaut sont basés sur la devise de vente du devis.

Contrairement aux coûts, les valeurs de vente ne peuvent être enregistrées **que** dans la devise de vente.

## <a name="billing-method"></a>Mode de facturation

Les projets ont généralement des modèles de contrats à frais fixes et basés sur la consommation. Dans Project Operations, le modèle de contrat d’un projet est représenté par la méthode de facturation. La méthode de facturation a deux valeurs : temps et matériel et prix fixe.

- **Temps et matériel :** Il s’agit d’un modèle de contrat basé sur la consommation dans lequel chaque coût encouru est soutenu par les revenus correspondants. Au fur et à mesure que vous estimez ou engagez plus de coûts, les ventes estimées et réelles correspondantes augmenteront également. Vous pouvez spécifier des limites à ne pas dépasser sur les lignes de devis qui utilisent ce mode de facturation. De cette façon, vous pouvez plafonner le revenu réel. Les revenus estimés ne sont pas affectés par les limites à ne pas dépasser.
- **Prix fixe** : un modèle de contrat à honoraires fixes qui indique que les valeurs de vente seront indépendantes des coûts engagés. La valeur des ventes est fixe et ne change pas lorsque vous estimez ou engagez des coûts supplémentaires.

## <a name="project-price-lists"></a>Tarifs des projets

Les tarifs de projet sont des tarifs qui sont utilisés pour les prix par défaut, et non les taux de coût, pour le temps, les dépenses et d’autres composants liés au projet. Il peut y avoir plusieurs tarifs et chacun peut avoir sa propre date de validité pour chaque devis de projet. Le chevauchement des dates données effectives n’est pas pris en charge pour les tarifs de projet dans Project Operations.

## <a name="product-price-lists"></a>Tarifs des produits

Les tarifs de produits sont des tarifs utilisés pour les prix par défaut, et non les taux de coût, pour les lignes basées sur les produits d’un devis. Il n’existe qu’un seul tarif par devis.

## <a name="transaction-classes"></a>Classes de transaction

Project Operations prend en charge quatre types de classes de transactions :

- Temps
- Dépenses
- Matière
- Frais

Les valeurs de coût et de vente peuvent être estimées et engagées dans les classes de transaction **Temps**, **Frais** et **Matière**. **Frais** est une classe de transaction de revenus uniquement.

## <a name="work-entities-and-billing-entities"></a>Entités de travail et entités de facturation

Les entités Projets et Tâches représentent le travail. Les entités qui représentent la facturation sont Lignes de devis et Lignes de contrat. Vous pouvez lier différentes entités de travail aux options de facturation en les associant à Lignes de devis ou de contrat.

## <a name="multi-customer-deals"></a>Transactions multi-clients

Les transactions multi-clients se produisent lorsqu’il y a plus d’un client à facturer. Voici quelques exemples type :

- **Entreprises OEM et leurs partenaires :** les partenaires et revendeurs vendent un produit avec des services à valeur ajoutée. Il s’agit généralement d’un scénario où, lors d’une transaction particulière avec un client, l’OEM propose de financer une partie du projet.
- **Projets du secteur public :** plusieurs organismes d’une administration locale acceptent de financer un projet et sont facturés selon une répartition préalablement convenue. Par exemple, un rectorat et la ville ou le département acceptent de financer la construction d’une piscine.

## <a name="invoice-schedules"></a>Planifications de facture

Les planifications de facture sont spécifiques à chaque ligne de devis et sont facultatifs. Les calendriers de facturation sont créés en fonction de certaines dates de début et de fin et de la fréquence de facturation. Les calendriers sont utilisés à l’étape du contrat, lorsque le processus de création automatique de facture est configuré. À la phase de devis, les planifications de facture sont facultatives. Lorsque les planifications de facture sont créées à la phase Devis, elles sont copiées dans le contrat de projet créé lorsqu’un devis de projet est remporté.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Différences par rapport aux devis Dynamics 365 Sales

Les devis Project Operations sont basés sur les devis Dynamics 365 Sales. Cependant, il existe des différences importantes dans les fonctionnalités dont vous devez être conscient :

- Les devis Project Operations comportent deux types de lignes différentes, l’une pour les projets et l’autre pour les produits.
- Les devis Project Operations ont leurs propres éléments de page et d’interface utilisateur, des règles métier, une logique métier dans les plug-ins et des scripts côté client qui les rendent uniques à partir des devis de vente.
- Dans Sales, vous pouvez joindre plusieurs commandes à un devis de vente. Dans Project Operations, vous pouvez joindre un seul contrat de projet à un devis de projet.
- Lorsque vous remportez un devis de vente, l’opportunité associée peut rester ouverte. Lorsqu’un devis de projet qui conclus, une opportunité associée est fermée.
- Un devis de vente ne comprend pas certains champs et les concepts qui se trouvent sur un devis de projet. Les champs incluent **Unité contractuelle**, **Gestionnaire de comptes** et **Nom du contact de facturation**.
- Les devis de vente et les devis de projet sont également identifiés par un champ basé sur un jeu de données nommé **Type**. Pour un devis de vente, ce champ a la valeur **Basé sur l’article**. Pour un devis de projet, il a la valeur **Basé sur le travail**.

En raison de ces différences, n’utilisez pas les factures de manière interchangeable dans Sales et Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
