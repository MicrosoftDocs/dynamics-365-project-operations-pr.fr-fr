---
title: Nouveautés ou modifications de la mise à jour (version 47) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477231"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Nouveautés ou modifications de la mise à jour (version 47) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 45, V3. Cette version a le numéro de build V3.10.78.8 et est généralement disponible par le biais d’une mise à jour automatique en juillet 2022.

## <a name="update-release-47"></a>Mise à jour (version 47)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Gestion des ressources**
- Une validation a été mise à jour pour garantir que les utilisateurs ne peuvent pas déclencher une exception de référence nulle lorsqu’ils tentent de créer un membre de l’équipe de projet sans **Ressource réservable**.
