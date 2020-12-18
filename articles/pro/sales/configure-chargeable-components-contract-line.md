---
title: Configurer les composants facturables d’une ligne de contrat basée sur un projet – Simplifié
description: Cette rubrique fournit des informations sur l’ajout de composants facturables aux lignes de contrat dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513876"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Configurer les composants facturables d’une ligne de contrat basée sur un projet – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une ligne de contrat basée sur un projet a les composants *inclus* et *payant*.

Les composants inclus sont des composants soumis à :

  - Méthode de facturation et répartition des clients
  - Limites à ne pas dépasser 
  - Paramètres de fréquence de facturation définis sur la ligne de contrat basée sur le projet

Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**. Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de contrat :

  - Facturable
  - Non facturable

Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.

La tarification est définie sur les tâches pour une ligne de contrat de projet et s’applique à toutes les classes de transaction incluses sur la ligne. Si le champ **Inclure les tâches** sur une ligne de contrat est vide ou est défini sur **Projet entier**, l’onglet **Tâches payantes** n’est pas disponible.

La tarification est définie sur les rôles pour une ligne de contrat de projet s’applique uniquement à la classe de transaction **Temps**. Si le champ **Inclure le temps** sur une ligne de contrat est défini sur **Non**, l’onglet **Rôles facturables** ne sera pas disponible.

La tarification est définie sur les catégories de transaction pour une ligne de contrat de projet et s’applique uniquement à la classe de transaction **Dépense**. Si le champ **Inclure les dépenses** sur une ligne de contrat est défini sur **Non**, l’onglet **Catégories facturables** ne sera pas disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable

Une tâche de projet peut être facturable ou non sur une ligne de contrat spécifique, ce qui rend possible la configuration suivante :

Si une ligne de contrat basée sur un projet comprend **Temps** et une certaine tâche, **T1** y est associé comme payant. S’il y a une deuxième ligne de contrat qui inclut **Dépenses**, vous pouvez associer la tâche T1 sur la ligne de contrat comme non facturable. Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses sont non facturables.

Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de contrat en mettant à jour le champ **Type de facturation** dans la sous-grille des tâches de la ligne de contrat. Vous pouvez également mettre à jour le champ **Type de facturation** dans la sous-grille Configuration de la facturation de la tâche d’un projet qui affiche les lignes de contrat associées à une tâche.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu’il soit facturable ou non facturable

Un rôle peut être facturable ou non facturable sur une ligne de contrat spécifique.

Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles payants** d’une ligne de contrat. Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable

Une catégorie de transaction peut être facturable ou non facturable sur une ligne de contrat spécifique.

Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** d’une ligne de contrat basée sur un projet. Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.

### <a name="resolve-chargeability"></a>Résoudre la chargeabilité

Une estimation ou un réel créé pour le temps ne sera considéré comme facturable que si **Temps** est inclus dans la ligne de contrat, et si **Tâche** et **Rôle** sont configurés comme facturables sur la ligne de contrat.

Une estimation ou un réel créé pour la dépense ne sera considéré comme facturable que si la **dépense** est incluse dans la ligne de contrat, et si les catégories de transaction **Tâche** et **Transaction** sont configurées comme facturables sur la ligne de contrat.


| Inclut le temps | Inclut la dépense | Inclut les tâches | Rôle           | Catégorie        | Tâche                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Oui           | Oui              | Projet entier | Facturable     | Facturable     | Facturation à l’heure actuelle: **Facturable** </br> Type de facturation sur les dépenses réelles : **Facturable**           |
| Oui           | Oui              | Tâches sélectionnées | Facturable     | Facturable     | Facturation à l’heure actuelle: **Facturable** </br> Type de facturation sur les dépenses réelles : **Facturable**           |
| Oui           | Oui              | Tâches sélectionnées | Non facturable | Facturable     | Facturation à l’heure actuelle: **Non facturable** </br> Type de facturation sur les dépenses réelles : **Facturable**       |
| Oui           | Oui              | Tâches sélectionnées | Facturable     | Facturable     | Facturation à l’heure actuelle: **Non facturable** </br> Type de facturation sur les dépenses réelles :   **Non facturable** |
| Oui           | Oui              | Tâches sélectionnées | Non facturable | Facturable     | Facturation à l’heure actuelle: **Non facturable** </br> Type de facturation sur les dépenses réelles :   **Non facturable** |
| Oui           | Oui              | Tâches sélectionnées | Non facturable | Non facturable | Facturation à l’heure actuelle: **Non facturable** </br> Type de facturation sur les dépenses réelles :   **Non facturable** |
| No            | Oui              | Projet entier | Impossible à définir   | Facturable     | Facturation à l’heure actuelle: **Non disponible**</br>Type de facturation sur les dépenses réelles : **Facturable**          |
| No            | Oui              | Projet entier | Impossible à définir   | Non facturable | Facturation à l’heure actuelle: **Non disponible**</br> Type de facturation sur les dépenses réelles : **Non facturable**     |
| Oui           | No               | Projet entier | Facturable     | Impossible à définir   | Facturation à l’heure actuelle: **Facturable** </br> Type de facturation sur les dépenses réelles : **Non disponible**        |
| Oui           | No               | Projet entier | Non facturable | Impossible à définir   | Facturation à l’heure actuelle: **Non facturable** </br>Type de facturation sur les dépenses réelles : **Non disponible**   |
