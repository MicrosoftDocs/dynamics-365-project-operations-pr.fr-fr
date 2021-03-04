---
title: Planifications de facture sur une ligne de devis selon les projets
description: Cette rubrique fournit des informations sur la création de planifications de factures et de jalons pour les lignes de devis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b69742915fe79ee59e7fdcf317000cea79c5929
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180819"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Planifications de facture sur une ligne de devis selon les projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Une ligne de devis selon les projets donne la possibilité d’exprimer une planification de facture. Ceci est facultatif lors de la phase de devis, car l’application ne prend pas en charge la facturation d’un projet lorsqu’il est lié à une ligne de devis. La facturation n’est autorisée qu’une fois le devis obtenu. Le seul impact en aval de la création d’une planification de facture pendant la phase de devis est que cette planification de facture est copiée dans la ligne de contrat basée sur le projet. Si vous ne créez pas de planification de facture pendant la phase de devis, vous pourrez le faire sur la ligne du contrat selon le projet.

Dans l’ensemble, le but des planifications de facture est de permettre la création automatique de projets de factures pour une ligne de contrat selon un projet. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Créer une planification de facture de temps et de matériel pour une ligne de devis selon un projet

Lorsque la méthode de facturation pour une ligne de devis selon un projet est Heure et matériel, le système génère une planification de facture basée sur la date. Pour générer automatiquement une planification de facture basée sur la date, procédez comme suit.

1. Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.
2. Sur la page **Citations**, ouvrez le devis du projet et sur l’onglet **Résumé**, définissez une date de livraison demandée.
3. Ouvrez la ligne de devis Heure et matériel pour laquelle vous devez créer une planification de facture basée sur la date. 
4. Sur l’onglet **Planification de facture**, sélectionnez des valeurs dans les champs **Début de la facturation** et **Fréquence de facturation**. 
5. Sur la sous-grille, sélectionnez **Générer une planification de facture**.
6. L’application génère la planification de facture avec les champs **Date d’exécution de la facture**, **Date limite de transaction**, et **Statut d’exécution** définis de la manière suivante :

    - **Date d’exécution de la facture** est défini sur la date qui est dictée en fonction de la fréquence de facturation.
    - **Date limite de transaction** est défini sur la veille de la **Date d’exécution de la facture**.
    - **Statut d’exécution** est automatiquement défini sur **Ne pas exécuter**. Lorsque la tâche de création automatique de facture s’exécute pour une certaine date d’exécution de facture, elle met à jour ce champ sur **Exécution réussie** ou **Échec de l’exécution**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Créer une planification de facture à prix fixe pour une ligne de devis selon un projet

Lorsque la ligne de devis selon un projet a une méthode de facturation **Fixe**, le système crée une planification de facture basée sur des jalons. Effectuez les étapes suivantes pour générer automatiquement cette planification pour un ensemble fixe de jalons qui sont également répartis pour la période calendaire.

1. Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.
2. Sur la page **Citations**, ouvrez le devis du projet et sur l’onglet **Résumé**, définissez une date de livraison demandée.
3. Ouvrez la ligne de devis à prix fixe pour laquelle vous devez créer une planification de jalon. 
4. Sur l’onglet **Planification de facture**, sélectionnez des valeurs dans les champs **Début de la facturation** et **Fréquence de facturation**. 
5. Sur la sous-grille, sélectionnez **Générer des jalons périodiques**.
6. L’application génère la planification de facture avec un nom de jalon, une date et un montant.

    - Le nom du jalon est défini sur la date qui est dictée en fonction de la fréquence de facturation.
    - La date du jalon est défini sur la date qui est dictée en fonction de la fréquence de facturation.
    - Le montant du jalon est calculé en divisant le montant du devis sur la ligne de devis selon le projet par le nombre de jalons dicté par la fréquence et le début de la facturation et les dates de livraison demandées.
    - Si la ligne de devis a également un montant de taxe estimé, cette valeur est répartie de manière égale entre chaque jalon lors de la génération de jalons périodiques.

### <a name="manually-create-milestones"></a>Créer manuellement des jalons

Les jalons à prix fixe peuvent également être générés manuellement lorsqu’ils ne sont pas périodiquement fractionnés. Pour créer manuellement un jalon :

Ouvrez la ligne de devis à prix fixe où vous devez créer un jalon. Sous l’onglet **Planification de facture**, dans la sous-grille, sélectionnez **+ Créer un jalon de ligne de devis** et saisissez les informations requises selon le tableau suivant.

| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Nom du jalon | Création rapide | Nom du jalon. | Ceci est propagé au jalon de la ligne de contrat de projet et à la facture |
| Tâche du projet | Création rapide | Si le jalon est lié à la tâche de projet, vous pouvez utiliser cette référence pour ajouter une logique personnalisée et définir le statut du jalon en fonction du statut de la tâche. | L’application n’a pas d’impact en aval de cette référence à une tâche. |
| Date du jalon | Création rapide | Définissez la date à laquelle le processus de création automatique de facture doit rechercher le statut de ce jalon pour le prendre en compte pour la facturation. | Ceci est propagé au jalon de la ligne de contrat de projet et à la facture. |
| Statut de la facture | Création rapide | Lorsqu’un jalon est créé, ce statut est toujours défini sur **Non prêt pour la facturation**. | Ceci est propagé au jalon de la ligne de contrat de projet et à la facture. |
| Montant de la ligne | Création rapide | Montant ou valeur du jalon qui sera facturé au client. | Ceci est propagé au jalon de la ligne de contrat de projet et à la facture. |
| Taxes | Création rapide | Montant de taxe qui sera appliqué au jalon. | Ceci est propagé au jalon de la ligne de contrat de projet et à la facture. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]