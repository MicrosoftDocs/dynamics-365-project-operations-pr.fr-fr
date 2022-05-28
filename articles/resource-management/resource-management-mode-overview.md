---
title: Vue d’ensemble des modes de gestion des ressources
description: Cette rubrique fournit des informations sur la fonctionnalité de gestion des ressources dans Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: f30bac95b2beb92345cbe25332963c58d2bde4bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585053"
---
# <a name="resource-management-modes-overview"></a>Vue d’ensemble des modes de gestion des ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Dynamics 365 Project Operations prend en charge deux modes pour vous permettre d’exécuter le flux de réservations global. Le mode de gestion est défini comme un paramètre de projet et peut être modifié si les besoins de votre entreprise changent.    

## <a name="central-mode"></a>Mode central
Pour les organisations qui centralisent l’affectation des ressources aux projets, le mode central permet de s’assurer que les chefs de projet peuvent définir les besoins en ressources au niveau du projet. La satisfaction des besoins en ressources est déléguée à un gestionnaire de ressources. Les chefs de projet peuvent accepter ou refuser les ressources proposées par le gestionnaire de ressources.

![Mode central.](./media/resource-management-central.png)

Pour gérer les ressources avec le mode central, voir :

- [Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources](/dynamics365/project-service/assign-generic-bookable-resource)
- [Réserver des ressources nommées à partir des besoins en ressources](/dynamics365/project-service/book-named-resource)
- [Envoyer une demande de ressource](/dynamics365/project-service/submit-resource-request)
- [Répondre à une demande de ressources](/dynamics365/project-service/resource-management-fulfill-requests)
- [Accepter ou rejeter une ressource de projet proposée à partir d’une demande de ressource](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modèle hybride
Pour les organisations qui ont besoin de flexibilité dans l’allocation des ressources, le mode hybride permet aux chefs de projet et aux gestionnaires de ressources de réserver des ressources.

![Mode hybride.](./media/resource-management-hybrid.png)

En plus du processus du mode central pris en charge, consultez les rubriques suivantes pour gérer tous les autres flux de réservation pris en charge en mode hybride :

Réserver une ressource directement sur un projet :
- [Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches](/dynamics365/project-service/assign-named-bookable-resource)

Réserver une ressource à partir d’un besoins en ressource :
- [Attribuer des ressources génériques pouvant être réservées à une tâche et générer des besoins en ressources](/dynamics365/project-service/assign-generic-bookable-resource)
- [Réserver des ressources nommées à partir des besoins en ressources](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]