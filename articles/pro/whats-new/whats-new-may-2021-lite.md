---
title: Nouveautés de mai 2021 – Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de mai 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060430"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Nouveautés de mai 2021 – Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

   - Version 4.10.0.186 de Project Operations dans l’environnement Dataverse.

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- [Modes de planification](../../project-management/scheduling-modes.md) : les chefs de projet peuvent désormais définir si un projet doit être géré en suivant le mode de planification à durée fixe, travail fixe ou unités fixes.

## <a name="quality-updates"></a>Mises à jour qualité

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2224568 | Ajout d’une logique pour permettre les personnalisations qui impliquent l’appel du plug-in de confirmation de facture. |
| Facturation et tarification | 2101098 | Amélioration de la logique des champs par défaut pour la facture pro forma. Ces champs sont notamment **Adresse de facturation**, **Nom de facturation** et **Modalités de paiement**. Les champs prennent désormais par défaut les valeurs de l’enregistrement client du contrat de projet correspondant. |
| Facturation et tarification | 2021413 | Mise à jour des champs **Coût réel** et **Ventes** sur l’entité **Tâche** pour inclure les valeurs de vente des dépenses non facturées et facturées sur les tâches. |
| Facturation et tarification | 2182110 | Lors de la copie d’un contrat de projet, l’ID de ligne de contrat est régénéré dans le contrat de projet de destination afin de garantir qu’il est unique. |
| Gestion des opportunités | 2186741 | Ajout de validations pour garantir que le champ **Origine** et le type de transaction ne peuvent pas être mis à jour pour les détails de la ligne de devis existante. |
| Gestion des opportunités | 2191353 | La création de jalons ne doit pas être autorisée sur une ligne de contrat de temps et de matériel. |
| Gestion des opportunités | 2216956 | Résolution des problèmes avec **Mettre à jour les prix**. |
| Planification et suivi | 2182979 | La fonction de copie de projet a été améliorée pour garantir que les lignes d’estimation des dépenses sont copiées à partir du projet d’origine. |
| Planification et suivi | 2184144 | La fonction de copie de projet a été améliorée pour garantir que le nom de la position de la ressource est copié à partir du projet d’origine. |
| Planification et suivi | 2184799 | Renforcement du contrôle lors de la copie d’un projet pour garantir que la date de début estimée ne peut pas être modifiée pendant la copie. |
| Planification et suivi | 2185134 | Pendant la copie d’un projet, la date de début estimée du projet de destination est définie sur la date du jour. |
| Planification et suivi | 2196373 | Assurez-vous que les enregistrements du chef de projet et des membres de l’équipe ne sont pas dupliqués dans l’équipe du projet lors de la copie d’un projet. |
| Planification et suivi | 2211833 | Les affectations de ressources sont copiées de la tâche du projet source vers le projet de destination. |
| Planification et suivi | 2186541 | Résolution des problèmes dans la grille **Estimations** lors du regroupement par **Ressource**. |
| Planification et suivi | 2166906 | La catégorie de transaction d’une tâche doit être copiée dans l’entité **Attribution de ressource**. |
| Gestion des ressources | 2125362 | Correction de problèmes liés à la création d’un membre d’équipe générique à l’aide de la méthode d’allocation basée sur les heures. |
| Temps et dépenses | 2113603 | Correction du problème lié à la personnalisation lors de la suppression des attributs de la page **Entrée de temps**. Le système vérifie si l’attribut existe sur la page avant d’y accéder à l’aide d’un script. |
| Temps et dépenses | 2204377 | Les feuilles de temps copiées doivent s’afficher automatiquement lorsque vous sélectionnez **Copier la semaine**. |
| Temps et dépenses | 2209059 | Le champ **Statut** est modifiable pour les entrées de temps de Dynamics 365 Field Service. |
