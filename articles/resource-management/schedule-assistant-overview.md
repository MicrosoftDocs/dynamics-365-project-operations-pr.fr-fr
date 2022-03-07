---
title: Vue d’ensemble de l’Assistant Planifier
description: Cette rubrique fournit des informations sur l’utilisation de l’Assistant Planifier pour réserver des ressources.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279225"
---
# <a name="schedule-assistant-overview"></a>Vue d’ensemble de l’Assistant Planifier

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

L’Assistant Planifier permet de réserver des ressources en fonction des besoins définis par le chef de projet. L’Assistant Planifier s’appuie sur les paramètres fournis dans les besoins en ressources pour trouver la ressource. L’Assistant Planifier recommande des ressources qui correspondent aux exigences pertinentes, telles que les fenêtres horaires ou les compétences requises.

Une fois les ressources appropriées identifiées, le gestionnaire de ressources ou de projet peut réserver la ressource au travail.

## <a name="prerequisites"></a>Conditions préalables

L’Assistant Planifier fait partie de la solution Universal Resource Scheduling. Cette solution est incluse et installée avec Dynamics 365 Project Operations, Dynamics 365 Field Service et Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Besoin de mise en correspondance et ressources

Un besoin en ressources généré est basé sur des détails tels que :

-   Caractéristiques
-   Rôles
-   Divisions
-   Préférences de ressource
-   Contours d’effort
-   Fuseau horaire

L’Assistant Planifier utilise ces détails pour filtrer les ressources.

## <a name="launch-the-schedule-assistant"></a>Lancer l’Assistant de planification

L’Assistant Planifier est lancé de deux manières. Si vous utilisez le mode hybride, dans la grille des membres de l’équipe, vous pouvez sélectionner n’importe quel membre de l’équipe dont les besoins en ressources ne sont pas satisfaits, puis sélectionnez **Réserver**. Si vous utilisez le mode central, le gestionnaire de ressources recherche et sélectionne la ressource.

## <a name="schedule-assistant-filters"></a>Filtres de l’Assistant Planifier

Une fois l’Assistant Planifier exécuté, les détails des besoins en ressources sont affichés sous forme de valeurs filtrées dans le volet gauche. Le gestionnaire de ressources ou le chef de projet peut affiner les résultats en ajustant les filtres pour répondre aux besoins de planification.

Le volet de filtre affiche les options liées au travail, notamment :

-   Début et fin du travail
-   Caractéristiques
-   Rôles
-   Unités d’organisation
-   Société d’allocation de ressources
-   Types de ressources
-   Ressources privilégiées


[!INCLUDE[footer-include](../includes/footer-banner.md)]