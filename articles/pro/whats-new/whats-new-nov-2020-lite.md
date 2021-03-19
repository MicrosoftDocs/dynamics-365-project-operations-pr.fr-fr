---
title: Nouveautés de novembre 2020 – Déploiement simplifié de Project Operations – Traiter la facturation pro forma
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de novembre 2020 du déploiement simplifié de Project Operations – Traiter la facturation pro forma.
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eb7c15fa937d508fa30ed2c04a6aa9cb117ef011
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272070"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Nouveautés de novembre 2020 – Déploiement simplifié de Project Operations – Traiter la facturation pro forma

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Le tableau suivant répertorie les mises à jour de la version 4.4.0.70 de Project Operations dans l’environnement CDS.

| Fonctionnalités                 | Numéro de référence | Mise à jour qualité                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Gestion des opportunités       | 2036993          | La ligne d’estimation et les lignes de contrat d’affectation de ressources sont mises à jour sur les devis gagnants lorsque le type de ligne de devis est **Toutes les tâches**.                                                 |
|   Gestion des opportunités       | 2071514          | Impossible de créer une facture pour un jalon à prix fixe sur un contrat pour lequel la facturation basée sur les tâches est activée.                                                                          |
| Facturation et tarification          | 2070392          | Les lignes de contrat de projet sur la facture augmentent à chaque fois que **Actualiser les transactions de facture** est sélectionné.                                                                       |
| Planification de projet             | 2043336          | Impossible de supprimer un enregistrement de membre de l’équipe de projet.                                                                                                                                    |
| Planification de projet             | 2046013          | Comportement incohérent des colonnes d’indicateur Estimations pendant le chargement par rapport au changement de type de phase de temps.                                                                                   |
| Planification de projet             | 2046647          | Les heures de début et de fin sont décalées d’une heure lorsque les besoins en ressources sont générés par les membres de l’équipe de projet.                                                                      |
| Planification de projet             | 2053879          | (À compter du prochain déploiement de CDS) PublishUnassignedAssignments interrompt une tentative d’enregistrement d’une tâche lorsque l’erreur « La valeur transmise pour ConditionOperator.In est vide ». |
| Planification de projet             | 2055501          | Laisser la **Date de début du projet** vide provoque un échec de la planification.                                                                                                      |
| Planification de projet             | 2066817          | Impossible de créer une ressource générique à l’aide du sélecteur de personnes dans l’onglet **Tâches**.                                                                                               |
| Planification de projet             | 2067034          | Le bouton **Afficher les détails** n’est pas disponible sur la page **Détails de la tâche**.                                                                                                         |
| Gestion des ressources          | 2046667          | Les membres génériques de l’équipe ne sont pas supprimés même une fois que toutes les ressources sont satisfaites.                                                                                                     |
| Temps et entrée rapide de dépenses | 2047499          | Le bouton **Nouveau** sur la page Saisie de l’heure ouvre la page **Nouvelle signature de courrier électronique**.                                                                                               |
| Temps et entrée rapide de dépenses | 2059859          | Une fenêtre contextuelle inattendue s’ouvre lors de la création d’une entrée de dépense.                                                                                                                         |
| Autres                        | 2044181          | [Désinstallation du bon de commande] - L’erreur « Enregistrement non disponible » se produit lorsque vous essayez de désinstaller **msdyn_ProjectServiceCore_Patch** et les solutions principales du service de projet msdyn.        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]