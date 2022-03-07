---
title: Nouveautés ou modifications de la mise à jour (version 30) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 30) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010423"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Nouveautés ou modifications de la mise à jour (version 30) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution.md).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 30) de Project Service Automation V3. Cette version a le numéro de build V3.10.51.61 et est généralement disponible via une mise à jour automatique en avril 2021.

## <a name="update-release-30"></a>Mise à jour (version 30)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Une erreur se produit lorsque vous créez et enregistrez une entrée de temps sur la page **Création rapide** si le champ **Rôle** est supprimé.
- Le filtre Entrée de temps applique l’opérateur de filtre incorrect.
- Les feuilles de temps copiées ne s’affichent pas automatiquement lorsque vous sélectionnez **Copier la semaine** sur le contrôle d’entrée de temps.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- Lorsque vous prolongez une réservation, le statut de réservation attribué à la réservation ferme est incorrect. La prolongation d’une réservation respecte le statut de réservation défini comme **Engagé** dans les métadonnées de configuration de la réservation.
- Lorsqu’aucun statut de réservation valide n’est spécifié, le message d’erreur n’est pas correctement localisé.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Les projets ne peuvent pas être créés dans une devise et inclure des tâches associées dans une autre devise.

**Vente**

Les problèmes suivants ont été résolus :

- Lorsqu’un tarif est copié, les prix ne sont pas mis à jour.
- La clôture d’un devis avec le statut Conclu échoue lorsque le détail du coût a une valeur d’origine.
- Sur l’entité **Tâche du projet**, le nom **Coût estimé** a été remplacé par **Coût prévu (base)**.
- Une exception de référence nulle est générée lorsque les factures sont créées ou supprimées.
