---
title: Considérations relatives à la mise à niveau de la structure de répartition du travail
description: Cette rubrique donne des informations sur la mise à niveau de la structure de répartition du travail de Project Service Automation version 2.x vers la version 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149540"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Considérations relatives à la mise à niveau de la structure de répartition du travail

[!include [banner](../includes/psa-now-project-operations.md)]

Cette rubrique donne des informations sur la mise à niveau de la structure de répartition du travail de Project Service Automation version 2.x vers la version 3.x. Cette rubrique définit l’état d’intégrité d’un projet dans Project Service Automation (PSA) qui est nécessaire pour une mise à niveau réussie. Elle fournit également des informations sur les situations de blocage courantes qui provoquent l’échec de la mise à niveau. Pour plus d’informations sur la définition de tâches de projet et leurs fonctions dans une planification de projet, consultez [Planifications de projets](project-creating.md).

## <a name="key-entities"></a>Entités clés
Pour une structure de répartition du travail précise qui est déjà chargée avec des ressources, les entités suivantes sont nécessaires :

- [Projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Équipe du projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tâche du projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Affectations de ressources](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dépendance de la tâche du projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Ressources réservables](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Pour définir une structure de répartition du travail chargée avec des ressources, vous devez effectuer les étapes suivantes :

1. Créer un projet. Pour plus d’informations sur la création d’un projet, consultez [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Créer une ou plusieurs tâches. Pour plus d’informations sur la création d’une tâche, consultez [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Définir les dépendances de tâche. Pour plus d’informations, voir [Dépendance des tâches du projet](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Affecter les membres de l’équipe du projet au projet. Pour plus d’informations, consultez [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Affecter les membres de l’équipe du projet aux tâches. Pour plus d’informations, consultez [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relations entre les membres de l’équipe du projet

Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :
- Tous les membres de l’équipe du projet doivent être associés à une ressource réservable.
- Tous les membres de l’équipe du projet doivent être associés au même projet. 

## <a name="project-task-relationships"></a>Relations entre les tâches du projet
Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :

- Les tâches connexes doivent être associées au même projet.
- Chaque tâche de ligne doit avoir une tâche parente.
- Chaque tâche doit avoir un projet parent.

### <a name="valid-conditions"></a>Conditions valides

- Toutes les durées de tâche doivent être supérieures ou égales à (>=) une heure et inférieures à 1 800 000 minutes (1 250 jours).*
- Toutes les tâches doivent avoir une date de début qui n’est pas antérieure au 01/01/2000.*
- Toutes les tâches doivent avoir une date de début qui ne dépasse pas 17 ans à compter de la date du jour.*
- Toutes les tâches doivent avoir une date de début antérieure ou égale à la date de fin.
- Tous les types de transaction dans les classifications (Dépenses, Matériel, Taxes et Temps) doivent avoir des valeurs pour **Unité par défaut** et **Groupe d’unités**.
- Les formats de date avec des lettres doivent être évités.

### <a name="potential-mitigation-steps"></a>Étapes d’atténuation potentielles
- Utilisez la recherche avancée pour identifier les tâches du projet qui ne contiennent pas d’ID de projet.
- Utilisez la recherche avancée pour identifier les tâches du projet dont la durée planifiée est supérieure à > 1 800 000.
- Avant d’apporter des modifications aux données, vous devez rechercher les personnalisations associées à l’entité qui ont pu aboutir à la génération des données dans un état incorrect. Ces personnalisations doivent être traitées avant de procéder à toute mise à jour des données.
- Pour les tâches identifiées qui sont devenues orphelines, pensez à supprimer ces tâches si elles sont inutiles ou si elles doivent être associées au projet parent correct.
- Pour les tâches dont la durée est supérieure à 1 250 jours, pensez à ajouter plusieurs tâches pour représenter la durée totale, si possible.

> [!NOTE]
> Les éléments signalés par un astérisque (\*) ont des limites dues au fait que la gestion de la relation client (CRM) ne prend en charge que 7 320 extensions de périodicité. Vous devez rester en dessous de cette limite.

## <a name="resource-assignment-relationships"></a>Relations entre les affectations de ressources
Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :

- Toutes les affectations de ressources dans une structure de répartition du travail doivent être associées au même projet.
- Toutes les affectations de ressources dans une structure de répartition du travail doivent être associées aux membres de l’équipe du projet dans le même projet.

### <a name="potential-mitigation-steps"></a>Étapes d’atténuation potentielles
- Identifiez toutes les tâches qui ne remplissent pas les conditions décrites ci-dessus.  
- Les affectations de ressources qui ne sont plus valides doivent être supprimées.

## <a name="project-task-dependency-relationships"></a>Relations entre les dépendances de tâche du projet
Pour garantir une mise à niveau réussie, les relations suivantes doivent être correctement maintenues :

- Toutes les dépendances de tâche du projet doivent être associées au même projet.
- Une tâche ne peut pas avoir la même dépendance référencée plusieurs fois.


[!INCLUDE[footer-include](../includes/footer-banner.md)]