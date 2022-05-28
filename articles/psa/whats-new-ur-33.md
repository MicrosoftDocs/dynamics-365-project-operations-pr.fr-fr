---
title: Nouveautés ou modifications de la mise à jour (version 33) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 33) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601475"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Nouveautés ou modifications de la mise à jour (version 33) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 33) de Project Service Automation V3. Cette version a le numéro de build V3.10.54.98 et est généralement disponible par le biais d’une mise à jour automatique en juillet 2021.

## <a name="update-release-33"></a>Mise à jour (version 33)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Deux champs verrouillés, **msdyn_description** et **msdyn_externaldescription** sont modifiables après envoi.
- Un message d’erreur s’affiche si une dépense est créée qui n’est pas liée à un projet.
- Lorsqu’une entrée de temps est créée, le rôle de ressource est défini par défaut sur un rôle inactif.
- Les lignes de journal associées à une dépense rappelée et supprimée ne sont pas supprimées.
- Dans le **Formulaire de création rapide d’entrée de temps**, mettez à jour la vue **Liste de tâches du projet** pour remplacer la date affichée par défaut par la date de début de la tâche.
- Lorsque vous créez une entrée de temps dans l’onglet **Associé** de la ressource réservable, l’entrée de temps est créée de manière incorrecte pour l’utilisateur connecté au lieu de la ressource réservable parent.
- De nouveaux champs sont ajoutés à la boîte de dialogue **MDD d’approbation en bloc**.

**Planification de projet**

Les problèmes suivants ont été résolus :
- Faibles performances de création de projets lorsque les modèles d’heures de travail du projet sont appliqués avec des calendriers complexes.
- Lorsque la date de début est postérieure à la date de fin, une erreur s’affiche dans le modèle de copie de projet en raison des différences dans le composant de temps de chaque champ.

**Gestion des ressources**

Les problèmes suivants ont été résolus :
- Un paramètre incorrect est utilisé dans la requête d’utilisation de ressources et le XML génère des résultats de filtre incorrects dans la grille **Utilisation de ressources**.
- La confirmation **Étendre les réservations** affiche une date de fin incorrecte pour les réservations.

**Vente**

Les problèmes suivants ont été résolus :
- Un message d’erreur s’affiche si un prix de catégorie est créé avec des valeurs manquantes.
- Un message d’erreur s’affiche si un jalon de ligne de contrat est créé sans ligne de commande.
