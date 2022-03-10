---
title: Configurer les composants facturables d’une ligne de contrat de projet
description: Cette rubrique fournit des informations sur la configuration de composants inclus, payants et non facturables sur les lignes de contrat.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 51151089df67e2d164fc6315c1291f880917f43f1fba189304cb305ea973cecb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004038"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configurer les composants facturables d’une ligne de contrat de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une ligne de contrat basée sur un projet a le concept des composants inclus, facturables et non facturables.

Les composants inclus sont soumis à la méthode de facturation, aux fractionnements client, aux limites à ne pas dépasser et aux paramètres de fréquence de facturation définis sur la ligne de contrat basée sur le projet.

Un sous-ensemble des composants inclus peut être marqué comme payant en mettant à jour le champ **Type de facturation**.

Les composants payants peuvent être définis sur les rôles et les catégories de transaction.

Pour une ligne de contrat de projet, la tarification définie sur un rôle s’applique uniquement à la classe de transaction **Temps**. Si **Inclure le temps** est défini sur **Non** dans une ligne de contrat de projet, l’onglet **Rôles facturables** n’est pas disponible.

La tarification est définie sur les catégories de transaction pour une ligne de contrat de projet et s’applique uniquement à la classe de transaction **Dépense**. Si **Inclure les dépenses** est défini sur **Non** dans une ligne de contrat de projet, l’onglet **Catégories facturables** n’est pas disponible.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu’il soit facturable ou non facturable

Un rôle peut être facturable ou non facturable sur une ligne de contrat basée sur un projet spécifique.

Sous l’onglet **Rôles facturables** de la ligne de contrat basée sur un projet, dans la sous-grille **Catégories facturables**, dans le champ **Type de facturation**, mettez à jour le type de facturation d’un rôle.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable

Une catégorie de transaction peut être facturable ou non facturable sur une ligne de contrat basée sur un projet spécifique.

Sous l’onglet **Catégories facturables** de la ligne de contrat basée sur un projet, dans la sous-grille **Catégories facturables**, dans le champ **Type de facturation**, mettez à jour le type de facturation d’une transaction.

### <a name="resolve-chargeability"></a>Résoudre la chargeabilité

Une estimation ou un réel créé pour le temps ne sera considéré comme facturable que si Temps est inclus dans la ligne de contrat, et si le rôle est configuré comme facturable sur la ligne de contrat.

Une estimation ou un réel créé pour la dépense ne sera considéré comme facturable que si la dépense est incluse dans la ligne de contrat, et si la catégorie de transaction est configurée comme facturable sur la ligne de contrat.

| Inclut le temps | Inclut la dépense | Rôle | Catégorie | Tâche |
| --- | --- | --- | --- | --- |
| Oui | Oui | Facturable | Facturable | Facturation à l’heure actuelle : Facturable </br>Type de facturation sur une dépense réelle : facturable |
| Oui | Oui | Non facturable | Facturable | Facturation à l’heure actuelle : Non facturable </br>Type de facturation sur une dépense réelle : facturable |
| Oui | Oui | Non facturable | Non facturable | Facturation à l’heure actuelle : Non facturable </br>Type de facturation sur une dépense réelle : non facturable |
| No | Oui | Impossible à définir | Facturable | Facturation à l’heure actuelle : Non disponible </br>Type de facturation sur une dépense réelle : Facturable |
| No | Oui | Impossible à définir | Non facturable | Facturation à l’heure actuelle : Non disponible </br>Type de facturation sur une dépense réelle : Non facturable |
| Oui | No | Facturable | Impossible à définir | Facturation à l’heure actuelle : Facturable </br>Type de facturation sur une dépense réelle : non disponible |
| Oui | No | Non facturable | Impossible à définir | Facturation à l’heure actuelle : Non facturable </br> Type de facturation sur une dépense réelle : non disponible |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
