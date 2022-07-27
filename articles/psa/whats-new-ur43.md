---
title: Nouveautés ou modifications de la mise à jour (version 43) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915313"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Nouveautés ou modifications de la mise à jour (version 43) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 43, V3. Cette version a le numéro de build V3.10.74.200 et est généralement disponible via une mise à jour automatique en mai 2022.

## <a name="update-release-43"></a>Mise à jour (version 43)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.


**Temps et dépenses**

- Lors de l’importation d’entrées de temps à partir de réservations ou d’affectations de ressources, la référence à la ressource réservable associée n’est pas conservée.
- Lorsque la grille de saisie du temps est étendue en plein écran, la navigation dans la grille avec la touche de tabulation ne fonctionne pas.
- Lors de la soumission d’une entrée de temps créée par un autre utilisateur, le champ **Proposé par** est incorrectement renseigné avec l’utilisateur qui a créé la feuille de temps.