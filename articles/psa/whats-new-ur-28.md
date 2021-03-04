---
title: Nouveautés ou modifications de la mise à jour (version 28) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 28) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150620"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nouveautés ou modifications de la mise à jour (version 28) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour Project Service Automation V3, Version mise à jour 28. Cette version possède le numéro de build V3.10.46.32 et est à disposition générale via une mise à jour autonome effectuée en janvier 2021.

## <a name="update-release-28"></a>Mise à jour (version 28)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Les utilisateurs peuvent utiliser **Modification groupée** pour mettre à jour les entrées de temps qui ont été approuvées et soumises.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Dans les cas où le GUID de la tâche est interprété comme un nombre, les tâches ne peuvent pas être ouvertes pour modification à l'aide de **Modifier la tâche** dans le ruban sur la page **Structure de répartition du travail**.

**Ventes**

Les problèmes suivants ont été résolus :

- Une exception de référence nulle est générée lorsque le plug-in **GetEstimatesForProject** est appelé.
- **Marquer prêt à facturer** sur la grille des jalons ne met à jour que partiellement les attributs, sauf pour l'attribut **InvoiceStatus**, qui est mis à jour.



[!INCLUDE[footer-include](../includes/footer-banner.md)]