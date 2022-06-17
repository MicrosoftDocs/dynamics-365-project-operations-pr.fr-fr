---
title: Nouveautés ou modifications de la mise à jour (version 35) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912835"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Nouveautés ou modifications de la mise à jour (version 35) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 35, V3. Cette version a le numéro de build V3.10.56.110 et est généralement disponible par le biais d’une mise à jour automatique en septembre 2021.

## <a name="update-release-35"></a>Mise à jour (version 35)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Temps et dépenses**

- L’approbateur du projet reçoit une erreur de privilège de lecture lorsqu’il approuve les entrées de dépenses avec un rôle **Approbateur du projet**.
- L’approbateur du projet reçoit une erreur de privilège d’écriture sur **msdyn_projectapproval** lorsqu’il annule une entrée de temps approuvée avec un rôle **Approbateur du projet**.
- Lorsque vous sélectionnez **Copier la semaine** dans une entrée de temps dans le module d’application Dynamics 365 pour téléphones - Hub des ressources du projet, l’erreur suivante se produit : "......\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE. »
- La stratégie **Réessayer** approuve automatiquement les entrées qui ont été précédemment rejetées.
- La sous-grille **Ensembles d’approbations** affiche les actions de ruban non applicables.
- Les icônes sont manquantes pour **Tâche du projet** et **Rôle de la ressource** sur l’entité **Entrée de temps**.
- Lorsque vous importez des affectations de ressources, les entrées de temps importées n’ont pas la durée correcte pour les affectations créées via des tâches en mode manuel.
- **Supprimer** est manquant sur la page **Recherche avancée pour les enregistrements de saisie de temps**.
- **Enregistrer** est manquant sur la page **Informations d’entrée de temps**. Ce problème empêche l’enregistrement des modifications lorsque la page est fermée.

**Planification de projet**

- Les grilles **Affectation de ressource** et **Rapprochement des ressources** ne trient pas les attributs groupés par ordre alphabétique.
- Les tâches ne peuvent pas être créées si le comportement de date est personnalisé pour **Date uniquement**.

**Gestion des ressources**

- Si Dynamics 365 Field Service et Project Service Automation sont tous les deux installés, des problèmes de superposition surviennent lorsque **Vue associée Besoin en ressources** est associée à une page principale.
- Le fait de double-cliquer sur **Enregistrer** dans la boîte de dialogue **Création rapide de membre d’équipe** empêche la création du besoin en ressources.

**Vente**

- Une exception est levée si vous supprimez une tâche associée à un devis dont le statut est **Conclu**.
