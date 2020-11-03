---
title: Vue d’ensemble des modes de gestion des ressources
description: Cette rubrique fournit des informations sur la fonctionnalité Gestion des ressources dans Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075628"
---
# <a name="resource-management-modes-overview"></a>Vue d’ensemble des modes de gestion des ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Dynamics 365 Project Operations prend en charge deux modes afin que vous puissiez exécuter le flux de réservation global. Le mode de gestion est défini comme un paramètre de projet et peut être modifié si les besoins de votre entreprise changent.    

## <a name="central-mode"></a>Mode central
Pour les organisations qui centralisent l’affectation des ressources aux projets, le mode central permet de s’assurer que les chefs de projet peuvent définir les besoins en ressources au niveau du projet. La satisfaction des besoins en ressources est déléguée à un gestionnaire de ressources. Les chefs de projet peuvent accepter ou refuser les ressources proposées par le gestionnaire de ressources.

![Mode central](./media/resource-management-central.png)

Pour gérer les ressources avec le mode central, voir :

- [Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Réserver des ressources nommées à partir des besoins en ressources](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Envoyer une demande de ressource](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Répondre à une demande de ressources](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Accepter ou rejeter une ressource de projet proposée à partir d’une demande de ressource](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modèle hybride
Pour les organisations qui ont besoin de flexibilité dans l’allocation des ressources, le mode hybride permet aux chefs de projet et aux gestionnaires de ressources de réserver des ressources.

![Mode hybride](./media/resource-management-hybrid.png)

En plus du processus du mode central pris en charge, consultez les rubriques suivantes pour gérer tous les autres flux de réservation pris en charge en mode hybride :

Réserver une ressource directement sur un projet :
- [Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Réserver une ressource à partir d’un besoins en ressource :
- [Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Réserver des ressources nommées à partir des besoins en ressources](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
