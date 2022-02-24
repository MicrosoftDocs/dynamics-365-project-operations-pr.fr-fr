---
title: Nouveautés d’avril 2021 – Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version d’avril 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 868d6daf8ac3ad9ef4245cef3c74a735137d3903
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994088"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Nouveautés d’avril 2021 – Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.9.0.221 de Project Operations dans l’environnement Dataverse 

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Matériel non stocké pour les projets. Les fonctionnalités clés comprennent :
  - Estimation et tarification du matériel non stocké pendant le cycle de vente d’un projet. Pour plus d’informations, consultez [Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Suivi de l’utilisation du matériel non stocké lors de la livraison de projet. Pour plus d’informations, consultez [Enregistrer l’utilisation du matériel sur les projets et les tâches du projet](../../material/material-usage-log.md).
  - Facturation des coûts du matériel non stocké utilisé. Pour plus d’informations, consultez [Gérer la réplication de facturation – Simplifié](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Les nouvelles API dans Dynamics 365 Dataverse autorisent les opérations de création, de mise à jour et de suppression avec des **Entités de planification**. Pour plus d’informations, consultez [Utiliser les API de planification pour effectuer des opérations avec des entités de planification](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Mises à jour qualité

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2224568 | Ajout d’une logique pour permettre les personnalisations qui impliquent l’appel du plug-in de confirmation de facture. |
| Facturation et tarification | 2101098 | Amélioration de la logique des champs par défaut pour les factures proforma : **Adresse de facturation**, **Nom de facturation** et **Modalités de paiement** proviennent désormais par défaut de l’enregistrement client du contrat de projet correspondant. |
| Facturation et tarification | 2021413 | Mise à jour des champs **Coût réel** et **Ventes** sur l’entité **Tâche** pour inclure les valeurs de ventes des dépenses non facturées et facturées sur les tâches. |
| Facturation et tarification | 2182110 | Lors de la copie d’un contrat de projet, l’ID de ligne de contrat est régénéré dans le contrat de projet de destination afin de garantir qu’il est unique. |
| Gestion des opportunités | 2186741 | Ajout de validations pour garantir que le champ **Origine** et le champ **Type de transaction** ne peuvent pas être mis à jour pour les détails de la ligne de devis existante. |
| Gestion des opportunités | 2191353 | Les jalons ne doivent pas être créés sur une ligne de contrat de temps et de matériel. |
| Gestion des opportunités | 2216956 | Résolution des problèmes avec **Mettre à jour les prix**. |
| Planification et suivi | 2182979 | La fonction de copie de projet a été améliorée pour garantir que les lignes d’estimation des dépenses sont copiées à partir du projet d’origine. |
| Planification et suivi | 2184144 | La fonction de copie de projet a été améliorée pour garantir que le nom de la position de la ressource est copié à partir du projet d’origine. |
| Planification et suivi | 2184799 | Copie de projet : contrôle renforcé pour garantir que la date de début estimée ne peut pas être modifiée pendant la copie. |
| Planification et suivi | 2185134 | Copie de projet : la date de début estimée du projet de destination est définie sur la date du jour. |
| Planification et suivi | 2196373 | Copie de projet : assurez-vous que les enregistrements du chef de projet et des membres de l’équipe ne sont pas dupliqués dans l’équipe du projet. |
| Planification et suivi | 2211833 | Copie de projet : les affectations de ressources sont copiées de la tâche du projet source vers le projet de destination. |
| Planification et suivi | 2186541 | Résolution des problèmes dans la grille **Estimations** lors du regroupement par ressource. |
| Planification et suivi | 2166906 | La catégorie de transaction d’une tâche doit être copiée dans l’entité **Attribution de ressource**. |
| Gestion des ressources | 2125362 | Correction de problèmes liés à la création d’un membre d’équipe générique à l’aide d’une méthode d’allocation basée sur les heures. |
| Temps et dépenses | 2113603 | Correction du problème lié à la personnalisation lors de la suppression des attributs de la page **Entrée de temps**. Le système vérifie maintenant si l’attribut existe sur la page avant d’y accéder à l’aide d’un script. |
| Temps et dépenses | 2204377 | Les feuilles de temps copiées doivent s’afficher automatiquement lorsque vous sélectionnez **Copier la semaine** lors de l’entrée de temps. |
| Temps et dépenses | 2209059 | Le champ **Statut** peut être modifié pour les entrées de temps Dynamics 365 Field Service. |
