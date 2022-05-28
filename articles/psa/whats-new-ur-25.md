---
title: Nouveautés ou modifications de la mise à jour (version 25) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 25) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581511"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Nouveautés ou modifications de la mise à jour (version 25) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour Project Service Automation V3, Version mise à jour 25. Cette version possède le numéro de build V 3.10.43.76 et est à disposition générale via une mise à jour autonome effectuée en octobre 2020.

## <a name="update-release-25"></a>Mise à jour (version 25)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

L’incident suivant a été résolu :

- Graphique d’entrées de temps comportant des données supplémentaires basées sur un intervalle trop grand en cours de récupération.

**Gestion des ressources**

L’incident suivant a été résolu :

- Ajout d’un code Package Deployer pour ignorer l’importation du dispositif Universal Resource Scheduling si un dispositif de version ultérieure existe déjà.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Correction des écarts d’arrondi et de taux de change entraînant un coût prévisionnel incorrect dans la grille de suivi du projet.
- Prend en charge la possibilité d’afficher deux ou plusieurs grilles de réaction sur le formulaire **Projet**.
- Fourniture de validation pour traiter la possibilité d’attribuer une tâche après la date de fin du calendrier, ce qui génère un échec d’affectation de ressources.
- Amélioration de la gestion des erreurs pour résoudre l’exception de référence null générée à partir des éléments suivants :

    - Plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** lorsqu’une tâche de projet est créée sans projet associé
    - Plug-in **PreProjectTeamMemberCreate**
    - Plug-in **PostProjectTeamMemberDelete**
    - Plug-in **PreValidateProjectTaskDelete**

**Ventes**

Les problèmes suivants ont été résolus :

- Amélioration de la gestion des erreurs pour résoudre les exceptions de référence null générées à partir de **Copier le projet : Gestion des estimations HelperResource**.
- **Non prêt pour la facturation** sur une **Réplication de facturation pour le temps et le matériel** n’efface pas le statut de facturation.
- Correction de l’étiquetage des boutons **Prix** dans les onglets **Prix du rôle** et **Articles de catalogue**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
