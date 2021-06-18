---
title: Nouveautés de mars 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de mars 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dcf11d770082308d77b369c6f50aabb1ec7c1c86
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995663"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de mars 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

- Version 4.8.0.91 de Project Operations dans l’environnement Dataverse 
- Gestion de projets et comptabilité dans l’environnement Dynamics 365 Finance version 10.0.16 

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse


| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2133873 | Correction de l’affichage du symbole monétaire du **Prix de vente unitaire** dans la grille **Estimations des dépenses**. |
| Facturation et tarification | 2174616 | Lorsqu’un devis est conclu, la liste de prix personnalisée du contrat est référencée dans les détails de la ligne du contrat qui sont copiés à partir du devis. |
| Gestion des opportunités | 2167475 | Montant de taxe fixe dans la facture de correction à l’origine d’une entrée réelle non facturée. |
| Gestion des opportunités | 2176285 | Le montant de la taxe ne doit pas être copié depuis les détails du contrat de vente/de la ligne de devis vers les détails du contrat de coût/de la ligne de devis. |
| Gestion des opportunités | 2188079 | Une règle de facturation fractionnée ne doit pas être créée pour les contrats qui ne sont pas basés sur le travail. |
| Planification et suivi | 2125274 | Attribut **Carte de double écriture du projet** pour **Mappage de la date de début du projet** mis à jour de **msdyn\_taskearlieststart** vers **msdyn\_actualstart**. |
| Planification et suivi | 2138853 | La fonction de copie du projet a été mise à jour pour s’assurer que les lignes d’estimation des dépenses faisant référence aux tâches sont copiées dans le projet de destination. |
| Planification et suivi | 2154306 | Résolution des problèmes de suppression des estimations de dépenses dans Project Operations pour les scénarios basés sur les ressources. |
| Planification et suivi | 2173259 | La fonction de copie du projet a été mise à jour pour garantir que le message d’erreur **Copie de WBS** ne s’affiche pas dans certains scénarios. |
| Temps et dépenses | 2148910 | Résolution du problème d’affichage de la page **Modifier l’entrée** dans la grillle **Entrée de temps**. |
| Temps et dépenses | 2159798 | Contrôles plus stricts pour garantir que les entrées de dépenses approuvées ne peuvent pas être modifiées. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestion de projets et comptabilité dans Dynamics 365 Finance

Pour plus d’informations, voir [Nouveautés de janvier 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Mises à jour réglementaires

Pour plus d’informations sur les mises à jour réglementaires pour les applications Finance and Operations, consultez [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Une autre façon d’en savoir plus sur les mises à jour réglementaires consiste à vous connecter à LCS et à afficher les mises à jour réglementaires prévues à l’aide de l’outil de recherche de problèmes. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../includes/footer-banner.md)]