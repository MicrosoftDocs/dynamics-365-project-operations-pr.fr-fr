---
title: Créer des planifications de factures sur une ligne de contrat basée sur un projet – Simplifié
description: Cette rubrique fournit des informations sur la création de planifications de factures et de jalons de facturation.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581971"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Créer des planifications de factures sur une ligne de contrat basée sur un projet – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez joindre une planification de facture à une ligne de contrat basée sur un projet. La facturation n’est autorisée qu’une fois le contrat remporté pour créer un contrat de projet. Les planifications de factures permettent de créer automatiquement des brouillons de factures pour une ligne de contrat basée sur un projet. Si vous prévoyez de toujours créer des factures manuellement, vous pouvez ignorer la création de planifications de facture sur une ligne de contrat basée sur un projet ou sur une ligne de contrat.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Créer une planification de facture de temps et de matériel pour une ligne de contrat basée sur un projet

Lorsqu’une ligne de contrat basée sur un projet a une méthode de facturation du temps et des articles, vous pouvez créer une planification de facture basée sur la date. Pour générer automatiquement une planification de facture basée sur la date, procédez comme suit.

1. Accéder à **Paramètres** > **Fréquences de facturation** pour configurer la fréquence de facturation.
2. Ouvrez le contrat de projet et sous l’onglet **Synthèse**, définissez la date de livraison demandée.
3. Ouvrez la ligne de contrat Temps et matériel pour laquelle vous souhaitez créer une planification de facture basée sur une date. 
4. Sous l’onglet **Planification de facture**, sélectionnez une date de début de facturation et la fréquence de facturation. 
5. Sur la sous-grille, sélectionnez **Générer une planification de facture**.

    Le système génère la planification de facture avec les informations de champ suivantes :

    - **Date d’exécution de la facture** est définie sur la date basée sur la fréquence de facturation.
    - **Date limite de transaction** est définie sur la veille de la **Date d’exécution de la facture**.
    - **Statut d’exécution** est automatiquement défini sur **Ne pas exécuter**. Lorsque la tâche de création automatique de facture s’exécute pour une certaine **Date d’exécution de la facture**, ce champ est mis à jour sur **Exécution réussie** ou **Échec de l’exécution**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Créer une planification de facture à prix fixe pour une ligne de contrat basée sur un projet

Lorsqu’une ligne de contrat basée sur un projet a une méthode de facturation à prix fixe, vous pouvez créer une planification de facture basée sur des jalons. Effectuez les étapes suivantes pour générer automatiquement une planification de facture basée sur des jalons pour un ensemble fixe de jalons qui se répartissent de manière égale sur la période calendaire.

1. Accéder à **Paramètres** > **Fréquences de facturation** pour configurer la fréquence de facturation.
2. Ouvrez le contrat de projet et sous l’onglet **Synthèse**, définissez la date de livraison demandée.
3. Ouvrez la ligne de contrat à prix fixe sur laquelle vous devez créer une planification de jalon. 
4. Sous l’onglet **Planification de facture (jalons de facturation)**, sélectionnez la date de début de facturation et la fréquence de facturation. 
5. Sur la sous-grille, sélectionnez **Générer des jalons périodiques**.

    Le système génère la planification de facture avec les informations de jalon suivantes :

    - **Nom du jalon** est défini sur la date qui est dictée sur la base de la fréquence de facturation.
    - **Date du jalon** est définie sur la date qui est dictée sur la base de la fréquence de facturation.
    - **Montant du jalon** est calculé en divisant le montant du contrat sur la ligne du contrat basé sur le projet par le nombre de jalons tel que dicté par la fréquence, le début de la facturation et les dates de livraison demandées.
    - Si la valeur du champ **Montant d’estimation des taxes** est définie dans la ligne de contrat, ce champ est également réparti à chaque jalon de manière égale lors de la génération de jalons périodiques.

Les jalons de facturation doivent être égaux à la valeur contractuelle de la ligne de contrat basée sur le projet. S’ils ne sont pas égaux, une erreur se produit. Vous pouvez régler ce problème en vérifiant que les jalons de facturation sont égaux au total de la valeur contractuelle de la ligne en créant, modifiant ou supprimant des jalons. Une fois les modifications apportées, actualisez la page.

### <a name="manually-create-milestones"></a>Créer manuellement des jalons

Les jalons à prix fixe peuvent être générés manuellement lorsqu’ils ne sont pas périodiquement fractionnés. Pour créer un jalon manuellement, suivez les étapes suivantes.

1. Ouvrez la ligne de contrat à prix fixe sur laquelle vous souhaitez créer un jalon. 
2. Sous l’onglet **Planification de facture**, dans la sous-grille, sélectionnez **+ Créer un jalon de ligne de contrat**.
3. Dans le formulaire **Création de jalons**, saisissez les informations requises en vous basant sur le tableau suivant. 

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Nom du jalon | Création rapide | Champ de texte pour le nom du jalon. | Ce champ est inclus dans le jalon de la ligne de contrat de projet et la facture. |
| Tâche du projet | Création rapide | Si le jalon est lié à une tâche de projet, utilisez cette référence pour ajouter une logique personnalisée et définir le statut du jalon selon le statut de la tâche. | Il n’y a pas d’impact en aval de cette référence sur une tâche. |
| Date du jalon | Création rapide | La date à laquelle le processus de création automatique de facture doit rechercher le statut de ce jalon pour le prendre en compte pour la facturation. | Ceci est inclus dans le jalon de la ligne de contrat de projet et la facture. |
| Statut de la facture | Création rapide | Lorsque le jalon est créé, ce statut est toujours défini sur **Non prêt pour la facturation** ou **Non démarré**. | Ceci est inclus dans le jalon de la ligne de contrat de projet et la facture. |
| Montant de la ligne | Création rapide | Le montant ou la valeur du jalon qui sera facturé au client. | Ce champ est inclus dans le jalon de la ligne de contrat de projet et la facture. |
| Taxes | Création rapide | Le montant de la taxe appliqué sur le jalon. | Ceci est inclus dans le jalon de la ligne de contrat de projet et la facture. |

4. Sélectionnez **Enregistrer et fermer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]