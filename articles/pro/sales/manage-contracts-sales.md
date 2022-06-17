---
title: Gérer les contrats de projets
description: Cet article fournit des informations sur l’affichage des contrats basés sur un projet.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: acf1331068ccd1cbbf6a63f85c1bc424889f67e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917251"
---
# <a name="manage-project-contracts"></a>Gérer les contrats de projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les contrats de projet dans Dynamics 365 Project Operations capturent et gèrent les engagements contractuels et les détails de facturation d’un projet. La structure d’un contrat de projet dans Project Operations est adaptée au travail basé sur un projet avec les composants suivants :

- Des lignes de contrat qui identifient les composants discrets du travail, qui seront présentés comme des composants de haut niveau sur une facture de projet.
- Des détails de ligne de contrat qui identifient et estiment le travail pour chaque composant de haut niveau ou ligne de contrat. L’estimation comprend la planification et les aspects financiers du travail lié à la ligne du contrat.
- Des modèles de contrat et des composants facturables sont configurés pour chaque ligne de contrat qui contient les modalités de facturation pour chaque ligne de contrat et le contrat d’ensemble.

## <a name="view-all-project-based-contracts"></a>Afficher tous les contrats basés sur les projets

Une liste de tous les contrats de projet peut être consultée sur la page de liste **Contrats**. 

1. Accédez à **Ventes** > **Contacts**. Une liste de tous vos contrats de projet dans le système s’affiche. 
2. Sélectionnez le **Commutateur de vue** (la flèche déroulante à côté du nom de la vue) pour sélectionner d’autres vues filtrées. Vous pouvez créer vos propres vues à l’aide de critères de filtre personnalisés.

Les contrats peuvent être créés ou supprimés à partir de cette page de liste ou des pages de détails.

> [!NOTE]
> Les contrats auxquels sont associés des projets, des tâches, des estimations, des journaux et/ou des chiffres réels ne peuvent pas être supprimés. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
