---
title: Concepts clés - Contrats de projet
description: Cette rubrique fournit des informations sur les concepts clés des contrats de projets dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4ab43a9de6b27f0f0e9b8cbe6ea8b613ce81e08d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075676"
---
# <a name="key-concepts---project-contracts"></a>Concepts clés - Contrats de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique fournit les concepts clés devant être pris en compte avant de commencer à utiliser des contrats de projet dans Dynamics 365 Project Operations :

## <a name="owning-company"></a>Société propriétaire

La société propriétaire équivaut au concept d'entité juridique du module **Gestion de projet et comptabilité** de Project Operations à partir de Dynamics 365 Finance. La société propriétaire représente l'entité juridique qui comptabilisera les coûts et les revenus générés par une transaction.

## <a name="contracting-unit"></a>Unité contractuelle

L'unité contractuelle représente la division ou le cabinet qui est propriétaire de la livraison du projet. Vous pouvez configurer les coûts des ressources de l’unité contractuelle. Lorsque vous spécifiez le coût de la ressource pour une ressource, vous pourrez également définir différents taux de coût pour les ressources. Cette unité contractante emprunte ces ressources à d'autres divisions ou pratiques au sein de l'entreprise. Les taux de coûts pour les ressources sont appelés prix de transfert, emprunt de ressources ou prix de change. Lorsque vous configurez les taux des coûts pour emprunter des ressources auprès d'autres divisions, utilisez la devise de la division de prêt.

## <a name="cost-currency"></a>Devise du coût

La devise de coût est la devise dans laquelle les coûts sont déclarés sur l'écran. Cette devise est dérivée de la devise attachée au champ **Unité contractuelle** sur le contrat et le projet. Les coûts peuvent être enregistrés dans n’importe quelle devise par rapport à un projet. Cependant, il existe une conversion de devise entre les coûts de devise enregistrés dans la devise de coût du projet en cas d'indication sur l'écran.

Étant donné que les taux de change de la plateforme Common Data Service (CDS) ne peuvent pas entrer en vigueur à la date, les totaux à l'écran du coût peuvent changer au fil du temps si vous mettez à jour les taux de change. Cependant, les coûts enregistrés dans la base de données restent inchangés, car les montants sont stockés dans la devise dans laquelle ils ont été engagés.

## <a name="sales-currency"></a>Devise de vente

La devise de vente dans Project Operations est la devise dans laquelle les montants des ventes estimés et réels sont enregistrés et affichés. La devise de vente est également la devise dans laquelle le client est facturé pour la transaction. Sur un contrat de projet, la devise de vente est par défaut celle de l'enregistrement client ou compte et peut être modifiée lors de la création du contrat. Lorsqu'un contrat est créé en clôturant un devis comme gagné, la devise du contrat est par défaut la devise du devis.

Lorsque vous créez un contrat de projet à partir de zéro, le champ **Devise de vente** ne peut pas être modifié. Les tarifs des produits et des projets par défaut sont basés sur cette devise dans le contrat.

Contrairement aux coûts, les valeurs de vente ne peuvent être enregistrées que dans la devise de vente.

## <a name="billing-method"></a>Mode de facturation

Il y a généralement deux types de modèles de contrats pour les projets à frais fixes et basés sur la consommation. Ces modèles sont représentés dans Project Operations comme des méthodes de facturation avec deux valeurs possibles :

- Temps et matériel : Un modèle de contrat basé sur la consommation dans lequel chaque coût encouru est soutenu par les revenus correspondants. Au fur et à mesure que vous estimez ou engagez plus de coûts, les ventes estimées et réelles correspondantes augmenteront également. Spécifiez les limites à ne pas dépasser sur les lignes de contrat qui ont cette méthode de facturation qui plafonne les revenus réels. Les revenus estimés ne sont pas affectés par les limites à ne pas dépasser.
- Prix fixe : Un modèle de contrat à honoraires fixes qui indique que les valeurs de vente seront indépendantes des coûts engagés. La valeur des ventes est fixe et ne change pas lorsque vous estimez ou engagez des coûts supplémentaires.

## <a name="project-price-lists"></a>Tarifs des projets

Les tarifs de projet sont utilisés pour les prix par défaut, et non les taux de coût, pour le temps, les dépenses et d'autres composants liés au projet. Il peut y avoir plusieurs listes de prix. Chaque tarif a sa propre date de validité pour chaque contrat de projet. Le chevauchement des dates de validité sur les tarifs du projet n'est pas pris en charge par Project Operations.

Lorsqu'un contrat de projet est créé en remportant un devis de projet, les listes de prix de projet sont copiées avec le nom et la date du contrat inclus. La copie de ces informations constitue une tarification personnalisée pour les composants du projet sur ce contrat de projet.

## <a name="transaction-classes"></a>Classes de transaction

Project Operations prend en charge quatre types de classes de transactions :

- Durée
- Dépense
- Matériel
- Frais

Les valeurs de coût et de vente peuvent être estimées et engagées sur des classes de transactions Temps, Dépenses et Matériel. Les Frais sont une catégorie de transactions à revenus uniquement.

## <a name="work-entities-and-billing-entities"></a>Entités de travail et entités de facturation

Les entités qui représentent le travail sont des projets et des tâches. Les entités qui représentent les aspects de facturation sont des lignes de contrat. Vous pouvez lier différentes entités de travail aux options de facturation en les associant aux lignes de contrat.

## <a name="multi-customer-deals"></a>Transactions multi-clients

Les transactions multi-clients se produisent lorsqu'il y a plusieurs clients sur une affaire. Les exemples courants comprennent :

- Les entreprises OEM et leurs partenaires : les partenaires et les revendeurs vendent un produit avec certains services à valeur ajoutée, impliquant généralement un accord particulier avec un client. L'OEM propose de financer une partie du projet. 

- Projets du secteur public : Plusieurs organismes d’une administration locale acceptent de financer un projet et sont facturés selon une répartition préalablement convenue. Par exemple, le rectorat et le gouvernement local acceptent de financer la construction d'une piscine.

## <a name="invoice-schedules"></a>Planifications de facture

Les calendriers de facturation sont spécifiques à chaque ligne de contrat et sont nécessaires pour que la facturation automatique fonctionne. Les planifications de facture sont créées en fonction de certaines dates de début et de fin et de la fréquence de facturation. Les planifications sont utilisées à l'étape du contrat lorsque le processus de création automatique de facture est configuré. Lorsqu'un contrat de projet est créé à partir d'un devis, la planification de facture est copiée vers le contrat de projet depuis le devis.

## <a name="changes-from-dynamics-365-sales-orders"></a>Modifications par rapport aux commandes Dynamics 365 Sales

Les contrats Project Operations sont basés sur les commandes dans Dynamics 365 Sales. Cependant, il existe d'importants écarts et différences dans les fonctionnalités. Les contrats Project Operations ont leurs propres éléments de formulaire et d'interface utilisateur, des règles métier, une logique métier dans les plug-ins et des scripts côté client qui les rendent uniques à partir des commandes. Pour ces raisons, n'utilisez pas une commande client ni un contrat Project Operations de manière interchangeable.
