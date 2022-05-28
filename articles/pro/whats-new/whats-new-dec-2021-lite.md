---
title: Nouveautés de décembre 2021 - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de décembre 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585375"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Nouveautés de décembre 2021 - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

### <a name="subcontract-management"></a>Gestion des sous-traitants 

- [Membres de l’équipe de projet en sous-traitance](../subcontracting/subcontracting-project-team-members.md) : un chef de projet peut créer des membres d’équipe nommés ou génériques avec des contrats et des lignes de sous-traitance pour influer sur la dotation en personnel et l’estimation.
- [Options de sous-traitance pour les membres de l’équipe de projet](../subcontracting/subcon-options.md) : lors du choix de dotation en personnel par des membres de l’équipe de projet nommés ou génériques, le chef de projet peut revoir les contrats de sous-traitance existants ou créer de nouveaux contrats de sous-traitance pour un ou plusieurs membres de l’équipe de projet. 
- [Estimation des coûts des affectations de ressources sous-traitées](../subcontracting/costing-subcon-ra.md) : l’estimation du coût du projet prendra en compte les affectations de ressources sous-traitées et les évaluera en utilisant les listes de tarifs d’achat associées aux contrats de sous-traitance. 
- [Configurer le Tableau de planification pour afficher les collaborateurss contractuels et la capacité sous-traitée](../subcontracting/configure-sb-subcon.md) : le tableau de planification dans Project Operations peut désormais être configuré pour rechercher et suggérer le type de collaborateur contractuel des ressources réservables et la capacité sous-traitée avec les employés. Cette configuration peut être appliquée lors de la recherche de ressources dans le contexte de la dotation en personnel d’un besoin spécifique du projet, ou lors d’une recherche en dehors du contexte d’un besoin du projet.
- [Dotation en personnel d’un projet avec des collaborateurs contractuels et une capacité sous-traitée](../subcontracting/staffing-cw.md) : les travailleurs contractuels peuvent désormais être réservés sur des projets en tirant parti de l’expérience du tableau de planification.
- [Enregistrement du temps, des dépenses et de l’utilisation des matériels sur les projets pour les composants sous-traités](../subcontracting/recording-subcon-actuals.md) : les collaborateurs contractuels peuvent enregistrer le temps et les dépenses, et les membres de l’équipe de projet peuvent également enregistrer l’utilisation des matériels achetés à l’aide d’un contrat de sous-traitance sur un projet. Cela se traduira par l’enregistrement des coûts précis sur les projets qui utilisent la capacité ou les matériels achetés.
- [Transitions d’état sur un contrat de sous-traitance](../subcontracting/subcon-states.md) : les contrats de sous-traitance peuvent être confirmés pour terminer la négociation avec le fournisseur, clôturés pour indiquer l’aboutissement de la livraison ou annulés pour indiquer la résiliation du contrat avec le fournisseur avant l’aboutissement de la livraison.

### <a name="task-planning"></a>Planification de tâche
- Amélioration de la résolution des problèmes pour les administrateurs système. Lorsqu’un utilisateur ne peut pas ouvrir un projet, l’administrateur peut examiner les erreurs non liées à la licence qui sont générées à partir de Project for the Web dans les [Journaux de planification du projet](../../project-management/schedule-api-logs.md).
- [Utiliser les listes de contrôle des tâches dans Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Dans Microsoft Project for the Web, vous pouvez ajouter une liste de contrôle à une tâche pour effectuer le suivi d’éléments spécifiques.

## <a name="quality-updates"></a>Mises à jour qualité

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Planification et suivi | 2392596 | Les API de planification autorisent désormais la mise à jour des champs **Effort restant**, **Effort terminé** et **% terminé**. |
| Planification et suivi | 2478497 | Les champs **Numéro d’activité** et **Identifiant de tâche** des API de planification peuvent être vides à la saisie car le système les remplira en suivant une numérotation automatisée.|
| Temps et dépenses | 2468135 | Le nombre de tentatives d’approbation est réduit de cinq à trois. |
| Temps et dépenses | 2468188 | Correction du problème avec le texte du journal dépassant la longueur maximale dans l’attribut **notetext** de l’entité **annotation**. |
