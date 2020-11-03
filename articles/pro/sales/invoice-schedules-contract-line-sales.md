---
title: Création de planifications de factures sur une ligne de contrat basée sur un projet
description: Cette rubrique fournit des informations sur le mode de création de planifications de factures et de jalons pour les lignes de contrat.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2183b915dd2f67e03964246cb0689003e48363f7
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075974"
---
# <a name="creating-invoice-schedules-on-a-project-based-contract-line"></a>Création de planifications de factures sur une ligne de contrat basée sur un projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Vous pouvez créer une planification de factures sur une ligne de contrat basée sur un projet. La facturation n'est autorisée qu'après l'obtention du contrat et la création d'un contrat de projet. Une planification de facture permet de créer automatiquement des ébauches de factures pour une ligne de contrat basée sur un projet. Si toutefois vous ne créez que manuellement des factures, vous pouvez ignorer la création de planifications de factures sur les lignes de contrat.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Créer une planification de facture de temps et de matériel pour une ligne de contrat

Lorsqu'une ligne de contrat basée sur un projet a une méthode de facturation du temps et des articles, vous pouvez créer une planification de facture basée sur la date. Pour générer automatiquement une planification de facture basée sur la date, procédez comme suit.

1. Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.
2. Accédez à l'enregistrement du contrat de projet et à l'onglet **Résumé** , dans le champ **Date de livraison requise** , sélectionnez une date.
3. Ouvrez le contrat **Temps et matériel** pour lequel vous créez une planification de facture basée sur la date. 
4. Sur l'onglet **Planification de facture** , sélectionnez la date de début de facturation et la fréquence de facturation.
5. Sur la sous-grille, sélectionnez **Générer une planification de facture**. La planification de facture est générée avec les champs **Date d'exécution de la facture** , **Date limite de transaction** et **Statut d'exécution** définis de la manière suivante :

    - **Date d'exécution de la facture**  : Cette date est dictée en fonction de la fréquence de facturation.
    - **Date limite de transaction**  : Veille de la date d'exécution de la facture.
    - **Statut d'exécution**  : Automatiquement défini sur **Ne pas exécuter**. Lorsque la tâche de création automatique de facture s'exécute pour une certaine date d'exécution de facture, ce champ est mis à jour sur **Exécution réussie** ou **Échec de l'exécution**.


## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Créer une planification de facture à prix fixe pour une ligne de contrat

Lorsque la ligne de contrat a une méthode de facturation Fixe, vous pouvez créer une planification de facture basée sur des jalons. Effectuez les étapes suivantes pour générer une planification de facture basée sur des jalons pour un ensemble fixe de jalons qui sont également répartis pour la période calendaire.

1. Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.
2. Accédez à l'enregistrement du contrat de projet et à l'onglet **Résumé** , dans le champ **Date de livraison requise** , sélectionnez une date.
3. Ouvrez la ligne de contrat à **prix fixe** pour laquelle vous créez la planification de jalon. Sur l'onglet **Facturation des jalons** , sélectionnez la date de début de facturation et la fréquence de facturation. 
4. Sur la sous-grille, sélectionnez **Générer des jalons périodiques**. La planification de facture est générée avec les champs **Nom du jalon** , **Date de jalon** et **Montant du jalon** définis comme suit :

    - **Nom du jalon**  : Cette date est dictée en fonction de la fréquence de facturation.
    - **Date du jalon**  : Cette date est dictée en fonction de la fréquence de facturation.
    - **Montant du jalon**  : Ce montant est calculé en divisant le montant du contrat sur la ligne de contrat selon le projet par le nombre de jalons dicté par la fréquence et le début de la facturation et les dates de livraison demandées.

    Si la ligne de contrat a une valeur dans le champ **Montant estimé de la taxe** , alors ce champ est également réparti sur chaque jalon de manière égale lors de la génération de jalons périodiques.

Les jalons de facturation doivent être égaux à la valeur contractuelle de la ligne de contrat. Si ce n'est pas le cas, vous recevrez une erreur sur la page **Ligne de contrat**. Vous pouvez corriger l'erreur en vérifiant que les jalons de facturation totalisent la valeur contractuelle de la ligne en créant, modifiant ou supprimant des jalons. Une fois les modifications apportées, actualisez la page pour supprimer l'erreur.

### <a name="manually-create-milestones"></a>Créer manuellement des jalons

Vous pouvez générer des jalons à prix fixe manuellement lorsqu'ils ne sont pas périodiquement fractionnés. Procédez comme suit pour créer manuellement un jalon.

1. Ouvrez la ligne de contrat à prix fixe pour laquelle vous créez un jalon et dans l'onglet **Planification de facture** , sur la sous-grille, sélectionnez **+ Créer un nouveau jalon de ligne de contrat**. 
2. Sur la page **Création de jalons** , entrez les informations requises en vous basant sur le tableau suivant.

| Champ | Emplacement | Pertinence, objectif et conseils | Impact en aval |
| --- | --- | --- | --- |
| Nom du jalon | Création rapide | Champ de texte pour le nom du jalon. | Ceci est propagé au jalon de la ligne de contrat de projet et la facture. |
| Tâche du projet | Création rapide | Si le jalon est lié à la tâche de projet, utilisez cette référence pour ajouter une logique personnalisée et définir le statut du jalon en fonction du statut de la tâche. | L'application n'a pas d'impact en aval de cette référence à une tâche. |
| Date du jalon | Création rapide | Définissez la date à laquelle le processus de création automatique de facture doit rechercher le statut de ce jalon pour le prendre en compte pour la facturation. | Ceci est propagé au jalon de la ligne de contrat de projet et la facture. |
| Statut de la facture | Création rapide | Lorsqu'un jalon est créé, ce statut est toujours défini sur **Non prêt pour la facturation** ou **Non démarré**. | Ceci est propagé au jalon de la ligne de contrat de projet et la facture. |
| Montant de la ligne | Création rapide | Montant ou valeur du jalon qui sera facturé au client. | Ceci est propagé au jalon de la ligne de contrat de projet et la facture. |
| Taxes | Création rapide | Le montant de la taxe appliqué sur le jalon. | Ceci est propagé au jalon de la ligne de contrat de projet et la facture. |

3. Sélectionnez **Enregistrer et fermer**.
| Montant de la ligne | Création rapide | Montant ou valeur du jalon qui sera facturé au client | Ceci est propagé à la ligne de contrat Projet Jalon et à la facture | | Taxe | Création rapide | Montant de la taxe qui sera appliqué sur le jalon | Ceci est propagé à la ligne de contrat Projet Jalon et à la facture |
