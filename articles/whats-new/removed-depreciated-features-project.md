---
title: Fonctionnalités supprimées ou obsolètes dans Dynamics 365 Project Operations
description: Cet article décrit les fonctions qui ont été supprimées, ou qu’il est prévu de supprimer de Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921483"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Fonctionnalités supprimées ou obsolètes dans Dynamics 365 Project Operations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock, le déploiement simplifié – Traiter la facturation pro forma et Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication_

Cet article décrit les fonctions qui ont été supprimées, ou qu’il est prévu de supprimer de Dynamics 365 Project Operations.

- Une fonctionnalité *supprimée* n’est plus disponible dans le produit.
- Une fonctionnalité *obsolète* n’est pas en développement actif et pourrait être supprimée lors d’une mise à jour future.

Cette liste est destinée à vous aider à prendre en compte ces suppressions et obsolescences pour votre propre planification.

> [!NOTE]
> Des informations détaillées sur les objets dans les applications de finances et d’opérations peuvent être consultés dans les [**États de référence technique**](/dynamics/s-e/global/axtechrefrep_61). Vous pouvez comparer les différentes versions de ces états pour en savoir plus sur les objets qui ont été modifiés ou supprimés de chaque version des applications de finances et d’opérations.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Fonctionnalités supprimées ou obsolètes dans la version de mars 2022 de Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Gestion et comptabilité des projets Paramètre « Toujours créer une transaction de régularisation »

| &nbsp; | &nbsp; |
|--------|--------|
| **Raison de l’abandon/suppression** | Les transactions d’ajustement sont nécessaires à des fins de vérification. Après l’obsolescence, ce paramètre sera masqué. Le système créera toujours des transactions d’ajustement, comme il le fait actuellement lorsque le paramètre est défini sur **Oui**. |
| **Remplacée par une autre fonctionnalité ?** | No |
| **Zones produit concernées** | Application |
| **Option de déploiement** | Project Operations pour les scénarios basés sur les produits stockés/fabriqués |
| **Statut** | Obsolète : d’ici le 1er mars 2023, nous masquerons le paramètre et modifierons le comportement du système afin que les transactions d’ajustement soient toujours créées. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Gestion et comptabilité des projets Paramètre « Utiliser la date d’ajustement comme nouvelle date de projet »

| &nbsp; | &nbsp; |
|--------|--------|
| **Raison de l’abandon/suppression** | Ce paramètre était à l’origine utilisé pour permettre des ajustements lorsqu’un période fiscale était fermée. Cependant, ce n’est plus nécessaire, car la date comptable de la transaction peut être modifiée à la première date de la période ouverte, si elle est configurée. La date du projet ne doit pas être modifiée, car elle représente la date à laquelle la transaction a eu lieu. |
| **Remplacée par une autre fonctionnalité ?** | No |
| **Zones produit concernées** | Application |
| **Option de déploiement** | Project Operations pour les scénarios basés sur les produits stockés/fabriqués |
| **Statut** | Obsolète : d’ici le 1er mars 2023, nous masquerons le paramètre et modifierons le comportement du système afin que la date du projet ne soit jamais changée lors des ajustements. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Workflow de demande de ressource dans Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication

| &nbsp; | &nbsp; |
|--------|--------|
| **Raison de l’abandon/suppression** | Obsolète en raison d’une faible utilisation et des limitations du volume de transactions. |
| **Remplacée par une autre fonctionnalité ?** | No |
| **Zones produit concernées** | Application |
| **Option de déploiement** | Project Operations pour les scénarios basés sur les produits stockés/fabriqués |
| **Statut** | Obsolète : d’ici le 1er mars 2023, nous désactiverons l’option permettant de demander des ressources pour le projet à l’aide du workflow. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Page de proposition de facture de projet sans vues En-tête et Lignes

| &nbsp; | &nbsp; |
|--------|--------|
| **Raison de l’abandon/suppression** | Obsolète en raison des améliorations apportées à la page qui a été introduite avec la clé de fonctionnalité **Utiliser les formulaires de proposition de facture de projet et de journal des factures avec la vue En-tête et lignes**. |
| **Remplacée par une autre fonctionnalité ?** | Oui |
| **Zones produit concernées** | Application |
| **Option de déploiement** | Project Operations pour les scénarios basés sur les produits stockés/fabriqués ; Project Operations pour les scénarios basés sur les ressources/produits non stockés |
| **Statut** | Obsolète : d’ici le 1er mars 2023, nous désactiverons la page précédente (ancienne) et activerons la fonctionnalité clé **Utiliser les formulaires de proposition de facture et de journal des factures de projet avec la vue En-tête et lignes** par défaut. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Fonctionnalités supprimées ou obsolètes dans la version de décembre 2021 de Project Operations

### <a name="collaboration-workspaces"></a>Espaces de travail de collaboration

[Créer un espace de travail de collaboration (Projet) ou créer un lien vers lui](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Raison de l’abandon/suppression** | Abandonné en raison d’une faible utilisation. Les clients utilisant Project Operations pour des scénarios basés sur les ressources/produits non stockés peuvent tirer parti de la [Collaboration avec les groupes Office](../project-management/collaboration-groups.md). |
| **Remplacée par une autre fonctionnalité ?** | No |
| **Zones produit concernées** | Application  |
| **Option de déploiement** | Project Operations pour les scénarios basés sur les produits stockés/fabriqués |
| **Statut** | Obsolète : d’ici le 1er décembre 2022, nous prévoyons de ne plus prendre en charge les espaces de travail de collaboration. |
