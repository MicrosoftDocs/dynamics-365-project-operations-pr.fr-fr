---
title: Nouveautés ou modifications dans Project Service Automation version 3.x, 1e partie 2020
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3, 1e partie 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280170"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nouveautés ou modifications dans Project Service Automation version 3, 1e partie 2020

[!include [banner](../includes/psa-now-project-operations.md)]

La rubrique présente les principales considérations relatives à la mise à niveau vers la dernière version de Project Service Automation (PSA) version 3.x, 1e partie 2020.

## <a name="time-entry"></a>Entrée de temps
L’expérience d’entrée de temps a été étendue pour offrir des fonctionnalités d’extension d’entrée de temps en scénarios clients. Cela inclut la possibilité d’ajouter des types d’entrée, qui entraînent désormais un comportement spécifique basé sur le nom du schéma du champ **Paramètres d’entrée de temps**, affiché en tant que **Source de temps**. Une nouvelle solution appelée Temps, dépense, statut et approbations (TESA) a été ajoutée pour prendre en charge cette fonctionnalité.

### <a name="upgrade-consideration"></a>Considération relative à la mise à niveau
Pour prendre en charge cette fonctionnalité, les rôles dans PSA ont été mis à jour pour inclure de nouveaux privilèges. Ces privilèges accordent un accès en lecture à la nouvelle entité, **Paramètres d’entrée de temps**.

Les utilisateurs qui doivent consigner le temps doivent disposer du rôle d’utilisateur **Utilisateur de l’entrée de temps**, en plus des rôles existants. Ce rôle inclut la nouvelle fonctionnalité et garantit que l’entrée de temps continuera de fonctionner.

En outre, si vous avez des modules d’application personnalisés incluant tous les formulaires de l’entité Entrée de temps, vous devrez supprimer le **Formulaire de création rapide d’entrée de temps TESA** du module.

### <a name="currently-extended-time-entry-changes"></a>Modifications d’entrée de temps actuellement étendues
Pour minimiser l’impact de l’entrée de temps sur les utilisateurs actuels, ce changement de rôle est la seule exigence nécessaire pour continuer à utiliser l’entrée de temps. Si vous avez créé des vues personnalisées ou des expériences d’entrée de temps distinctes, vous devez définir les champs **Paramètres d’entrée de temps** sur la valeur PSA correcte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]