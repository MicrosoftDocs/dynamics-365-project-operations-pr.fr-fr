---
title: Nouveautés ou modifications de la mise à jour (version 29) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 29) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 56cf47d207c7ee518d5d4b53866c3d6ddf1d1fb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587215"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Nouveautés ou modifications de la mise à jour (version 29) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 29) de Project Service Automation V3. Cette version a un numéro de build V3.10.47.7 et est généralement disponible via une mise à jour automatique en février 2021.

## <a name="update-release-29"></a>Mise à jour (version 29)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Les utilisateurs ne peuvent pas voir les heures de travail enregistrées pendant les jours non ouvrables dans la grille d’entrée de temps.
- Les entrées de dépenses approuvées peuvent être modifiées dans la grille.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Logique de validation manquante pour garantir que les heures d’effort d’attribution de ressources ne peuvent pas être négatives.
- L’action personnalisée, **AssignResourcesForTask** met à jour tous les champs au lieu des champs modifiés uniquement.
- Lors de la copie d’un projet dans un environnement avec des plug-ins ou des workflows enregistrés dans l’événement **CreateProject**, l’attribut **msdyn_bulkgenerationstatus** n’est pas mis à jour si **CopyWBSToProject** échoue.
- Lorsque vous développez le calendrier du projet, les jours ouvrables ne sont pas triés dans l’ordre croissant, ce qui entraîne l’échec de certaines mises à jour de tâches du projet.
- La modification du gestionnaire de projet dans un projet existant déclenche la logique par défaut de l’unité d’organisation.

**Vente**

Les problèmes suivants ont été résolus :

- L’onglet **Performance du contrat** sur la page **Contrat** échoue silencieusement pendant l’initialisation lorsqu’aucune ligne de contrat n’est présente.
