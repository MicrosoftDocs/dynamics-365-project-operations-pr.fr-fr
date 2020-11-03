---
title: Configurer les composants facturables d’une ligne de devis
description: Cette rubrique fournit des informations sur la configuration de composants payants et non facturables sur une ligne de devis basée sur un projet.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075861"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurer les composants facturables d’une ligne de devis

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une ligne de devis basée sur un projet a le concept des composants *inclus* et *payant*.

Les composants inclus sont soumis à :

  - Méthode de facturation et répartition des clients
  - Limites à ne pas dépasser 
  - Paramètres de fréquence de facturation définis sur la ligne de devis basée sur le projet

Un sous-ensemble des composants inclus peut être marqué comme payant à l'aide du champ **Type de facturation**. Le champ **Type de facturation** est un ensemble d'options qui autorise les valeurs suivantes dans le contexte d'une ligne de devis :

  - Facturable
  - Non facturable

Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.

La tarification est définie sur les tâches pour une ligne de devis et s'applique à toutes les classes de transaction incluses sur cette ligne. Si le champ **Inclure les tâches** est défini sur **Projet entier** ou laissé vide, l'onglet **Tâches payantes** n'est pas disponible.

La tarification est définie sur les rôles pour une ligne de devis et s'applique uniquement à la classe de transaction **Temps**. Si le champ **Inclure le temps** est défini sur **Non** dans une ligne de devis de projet, l'onglet **Rôles facturables** n'est pas disponible.

La tarification est définie sur les catégories de transaction pour une ligne de devis et s'applique uniquement à la classe de transaction **Dépense**. Si le champ **Inclure les dépenses** est défini sur **Non** dans une ligne de devis de projet, l'onglet **Catégories facturables** n'est pas disponible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une tâche de projet pour qu'elle soit facturable ou non facturable

Une tâche de projet peut être facturable ou non dans le contexte d'une ligne de devis spécifique à un projet, ce qui rend possible la configuration suivante :

Si une ligne de devis basée sur un projet comprend **Temps** et la tâche **T1** , la tâche est associée à la ligne de devis comme facturable. S'il y a une deuxième ligne de devis qui inclut **Dépenses** , vous pouvez associer la tâche **T1** sur la ligne de devis comme non facturable. Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses enregistrées sur la tâche sont non facturables.

Le type de facturation d'une tâche peut être configuré dans l'onglet **Tâches payantes** d'une ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Tâches de la ligne de devis**. Vous pouvez également mettre à jour le type de facturation d'une tâche de projet dans le champ **Type de facturation** de la sous-grille de la configuration de la facturation des tâches d'un projet qui affiche les lignes de devis associées à une tâche.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu'il soit facturable ou non facturable

Un rôle peut être payant ou non dans le contexte d'une ligne de devis spécifique à un projet.

Le type de facturation d'un rôle peut être configuré dans l'onglet **Rôles facturables** d'une ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable

Une catégorie de transaction peut être facturable ou non facturable sur une ligne de devis spécifique.

Le type de facturation d'une transaction peut être configuré dans l'onglet **Catégories facturables** d'une ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.

### <a name="resolve-chargeability"></a>Résoudre la chargeabilité
Une estimation ou un réel créé pour le temps ne sera considéré comme facturable que si **Temps** est inclus dans la ligne de devis, et si **Tâche** et **Rôle** sont configurés comme facturables sur la ligne de devis.

Une estimation ou un réel créé pour la dépense ne sera considéré comme facturable que si **Dépense** est inclus dans la ligne de devis, et si **Tâche** et **Catégorie de transaction** sont configurés comme facturables sur la ligne de devis.

| Inclut le temps | Inclut la dépense | Tâches incluses | Rôle | Catégorie  | Tâche | Facturation |
| --- | --- | --- | --- | --- | --- | --- |
| Oui | Oui | Projet entier | Facturable | Facturable | Impossible à définir | Facturation à l'heure actuelle : Facturable </br>Type de facturation sur les dépenses réelles : facturable |
| Oui | Oui | Tâches sélectionnées uniquement | Facturable | Facturable | Facturable | Facturation à l'heure actuelle : Facturable</br>Type de facturation sur les dépenses réelles : facturable |
| Oui | Oui | Tâches sélectionnées uniquement | Non facturable | Facturable | Facturable | Facturation à l'heure actuelle : Non facturable</br>Type de facturation sur les dépenses réelles : facturable |
| Oui | Oui | Tâches sélectionnées uniquement | Facturable | Facturable | Non facturable | Facturation à l'heure actuelle : Non facturable</br> Type de facturation sur les dépenses réelles : non facturable |
| Oui | Oui | Tâches sélectionnées uniquement | Non facturable | Facturable | Non facturable | Facturation à l'heure actuelle : Non facturable</br> Type de facturation sur les dépenses réelles : non facturable |
| Oui | Oui | Tâches sélectionnées uniquement | Non facturable | Non facturable | Facturable | Facturation à l'heure actuelle : Non facturable</br> Type de facturation sur les dépenses réelles : non facturable |
| No | Oui | Projet entier | Impossible à définir | Facturable | Impossible à définir | Facturation à l'heure actuelle : Non disponible </br>Type de facturation sur les dépenses réelles : facturable |
| No | Oui | Projet entier | Impossible à définir | Non facturable | Impossible à définir | Facturation à l'heure actuelle : Non disponible </br>Type de facturation sur les dépenses réelles : non facturable |
| Oui | No | Projet entier | Facturable | Impossible à définir | Impossible à définir | Facturation à l'heure actuelle : Facturable</br>Type de facturation sur les dépenses réelles : non disponible |
| Oui | No | Projet entier | Non facturable | Impossible à définir | Impossible à définir | Facturation à l'heure actuelle : Non facturable </br>Type de facturation sur les dépenses réelles : non disponible |
