---
title: Configurer les composants facturables d’une ligne de devis basée sur un projet
description: Cette rubrique fournit des informations sur les composants inclus, facturables et non facturables sur les lignes de devis basées sur un projet.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642540"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurer les composants facturables d’une ligne de devis basée sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une ligne de devis basée sur un projet peut inclure des composants et des composants facturables.

Les composants inclus sont soumis à la méthode de facturation, aux fractionnements client, aux limites à ne pas dépasser et aux paramètres de fréquence de facturation définis sur la ligne de devis basée sur un projet.
Un sous-ensemble des composants inclus peut être marqué comme facturable en utilisant **Type de facturation**. Vous pouvez sélectionner l'une des options suivantes dans le champ **Type de facturation** dans le contexte d'une ligne de devis :

   - Facturable
   - Non facturable

Les composants payants peuvent être définis sur les rôles et les catégories de transaction.

La tarification définie sur les rôles pour une ligne de devis de projet s'applique uniquement à la classe de transaction **Temps**. Si une ligne de devis de projet a le champ **Inclure le temps** = **Non**, l'onglet **Rôles facturables** n'est pas disponible.

La tarification définie sur les catégories de transaction pour une ligne de devis de projet s'applique uniquement à la classe de transaction **Dépense**. Si une ligne de devis de projet a le champ **Inclure la dépense** = **Non**, l'onglet **Catégories facturables** n'est pas disponible.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu’il soit facturable ou non facturable
Un rôle peut être facturable ou non sur une ligne de devis basée sur un projet. Le type de facturation d'un rôle peut être configuré sur l'onglet **Rôles facturables** d'une ligne de devis basée sur un projet. Pour ce faire, mettez à jour le **Type de facturation** dans la sous-grille **Rôles facturables**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable
Un catégorie de transaction peut être facturable ou non sur une ligne de devis basée sur un projet. Le type de facturation d'une transaction peut être configuré sur l'onglet **Catégories facturables** d'une ligne de devis basée sur un projet. Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**. 

## <a name="resolve-chargeability"></a>Résoudre la chargeabilité

Une estimation ou un réel créé pour le temps ne sera considéré comme facturable que si le temps est inclus sur la ligne de devis et si le rôle est configuré comme facturable.
Une estimation ou un réel créé pour une dépense ne sera considéré comme facturable que si la dépense est incluse sur la ligne de devis et si la catégorie de transaction est configurée comme facturable. Le tableau suivant montre la valeur par défaut de l'exigibilité chaque réel. Les valeurs par défaut sont basées sur les composants inclus et le type de facturation configuré sur la ligne de devis.

| Inclut le temps | Inclut la dépense | Rôle | Catégorie  | Tâche |
| --- | --- | --- | --- | --- |
| Oui | Oui | Facturable | Facturable | Facturation à l’heure actuelle : Facturable </br>Type de facturation sur une dépense réelle : facturable |
| Oui | Oui | Non facturable | Facturable | Facturation à l’heure actuelle : Non facturable </br>Type de facturation sur une dépense réelle : facturable |
| Oui | Oui | Non facturable | Non facturable | Facturation à l’heure actuelle : Non facturable </br>Type de facturation sur une dépense réelle : non facturable |
| No | Oui | Impossible à définir | Facturable | Facturation à l’heure actuelle : Non disponible </br>Type de facturation sur une dépense réelle : facturable |
| No | Oui | Impossible à définir | Non facturable | Facturation à l’heure actuelle : Non disponible </br>Type de facturation sur une dépense réelle : Non facturable |
| Oui | No | Facturable | Impossible à définir | Facturation à l’heure actuelle : Facturable </br>Type de facturation sur une dépense réelle : non disponible |
| Oui | No | Non facturable | Impossible à définir | Facturation à l’heure actuelle : Non facturable </br> Type de facturation sur une dépense réelle : non disponible |


[!INCLUDE[footer-include](../includes/footer-banner.md)]