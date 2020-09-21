---
title: Nouveautés ou modifications dans Project Service Automation version 3.x, 1e partie 2020
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3, 1e partie 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168044"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Nouveautés ou modifications dans Project Service Automation version 3, 1e partie 2020
La rubrique présente les principales considérations relatives à la mise à niveau vers la dernière version de Project Service Automation (PSA) version 3.x, 1e partie 2020.

## <a name="time-entry"></a>Entrée de temps
L'expérience d'entrée de temps a été étendue pour offrir des fonctionnalités d'extension d'entrée de temps en scénarios clients. Cela inclut la possibilité d'ajouter des types d'entrée, qui entraînent désormais un comportement spécifique basé sur le nom du schéma du champ **Paramètres d'entrée de temps**, affiché en tant que **Source de temps**.

### <a name="upgrade-consideration"></a>Considération relative à la mise à niveau
Pour prendre en charge cette fonctionnalité, les rôles dans PSA ont été mis à jour pour inclure de nouveaux privilèges. Ces privilèges accordent un accès en lecture à la nouvelle entité, **Paramètres d'entrée de temps**.

Les utilisateurs qui doivent consigner le temps doivent disposer du rôle d'utilisateur **Utilisateur de l'entrée de temps**, en plus des rôles existants. Ce rôle inclut la nouvelle fonctionnalité et garantit que l'entrée de temps continuera de fonctionner.

### <a name="currently-extended-time-entry-changes"></a>Modifications d'entrée de temps actuellement étendues
Pour minimiser l'impact de l'entrée de temps sur les utilisateurs actuels, ce changement de rôle est la seule exigence nécessaire pour continuer à utiliser l'entrée de temps. Si vous avez créé des vues personnalisées ou des expériences d'entrée de temps distinctes, vous devez définir les champs **Paramètres d'entrée de temps** sur la valeur PSA correcte.
