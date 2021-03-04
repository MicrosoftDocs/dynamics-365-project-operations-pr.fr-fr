---
title: Configurer l’intégration de Project Operations par entité juridique
description: Cette rubrique fournit des informations sur la configuration de l’intégration par entité juridique dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122880"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurer l’intégration de Project Operations par entité juridique 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique vous explique comment configurer Dynamics 365 Project Operations par entité juridique.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Activer les clés de fonctionnalités dans Dynamics 365 Finance

Effectuez les étapes suivantes pour activer les fonctionnalités requises.

1. Dans Dynamics 365 Finance, accédez à l’espace de travail **Gestion des données**.
2. Dans **Liste des fonctionnalités**, recherchez et activez les fonctionnalités suivantes :
  
    - **Activer plusieurs lignes de contrat pour un projet**
    - **Activer Project Operations sur Dynamics 365 Customer Engagement**

> [!NOTE]
> Si vous ne voyez pas **Clés de fonctionnalités** dans la liste, assurez-vous que vous disposez de la version minimale requise pour Finance (version de l’application 10.0.13 avec toutes les mises à jour de qualité appliquées, ou version ultérieure). Sélectionnez **Rechercher les mises à jour** pour actualiser la liste des fonctionnalités.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Définir le scénario de déploiement Project Operations pour une entité juridique

Vous pouvez activer Project Operations sur Dynamics 365 Customer Engagement au niveau d’une entité juridique. Vous pouvez avoir une entité juridique utilisant Project Operations sur Dynamics 365 Customer Engagement pour les scénarios d’ordre non stocké / basé sur les ressources. Dans le même environnement, vous pouvez avoir une autre entité juridique utilisant Project Operations pour les scénarios d’ordre stocké / de fabrication.

1. Dans Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres globaux de gestion et comptabilité des projets**.
2. Dans la liste des entités juridiques disponibles, sélectionnez les entités pour lesquelles plusieurs lignes de contrat et les fonctionnalités Project Operations sur Dynamics 365 Customer Engagement seront activées. Laissez non sélectionnées les entités juridiques qui utiliseront Project Operations pour les scénarios d’ordre stocké / de fabrication.

> [!NOTE]
> Une entité juridique ne peut être sélectionnée que si elle n’a aucun projet existant.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurer Paramètres de gestion et comptabilité des projets

Chaque entité juridique utilisant Project Operations sur Dynamics 365 Customer Engagement nécessite un ensemble de paramètres par défaut. Ces paramètres sont configurés sur l’onglet **Project Operations** sur la page **Paramètres de gestion et comptabilité des projets**. Les paramètres sont :

  - **Valeurs par défaut du type de facturation** : Project Operations utilise un ensemble fixe de valeurs par défaut du type de facturation qui doivent être mappées aux propriétés de ligne Finance. Créez un enregistrement pour chaque type de facturation : **Non spécifié**, **Facturable**, **Non facturable**, **Gratuit** et **Non disponible**.
  - **Valeurs par défaut de la catégorie de projet** : sélectionnez les catégories de projet par défaut à utiliser pour chaque type de transaction. Ces valeurs par défaut seront utilisées dans le **Journal d’intégration de Project Operations** et dans les estimations où aucune catégorie de transaction n’est spécifiée pour les chiffres réels du projet.
  - **Prévisions** : sélectionnez le modèle de prévision à utiliser pour les estimations de temps et de dépenses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]