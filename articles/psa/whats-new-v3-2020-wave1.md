---
title: Nouveautés ou modifications dans Project Service Automation version 3.x, 1e partie 2020
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3, 1e partie 2020.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577877"
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
