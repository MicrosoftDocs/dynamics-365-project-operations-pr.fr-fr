---
title: Nouveautés ou modifications de la mise à jour (version 19) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 19) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949136"
---
# <a name="project-service-automation-update-release-19-v3"></a>Mise à jour (version 19) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 19) de PSA V3. Cette version a le numéro de build V3.10.30.41 et est généralement disponible via une mise à jour automatique en mai 2020.

## <a name="update-release-19"></a>Mise à jour (version 19)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus : 

- Les erreurs dérivées des importations d’entrée de temps ne sont pas affichées correctement.
- La grille d’entrée de temps ne prend pas en charge le comportement du champ **Date uniquement**.
- Les ressources du projet ne peuvent pas créer une dépense avec un projet.

**Gestion du projet**

Les problèmes suivants ont été résolus : 

-  La tâche petit-enfant crée une estimation incorrecte de l’effort lors du calcul du coût final.

**Ventes**

Les problèmes suivants ont été résolus : 

- L’action **Recalculer** ne fonctionne pas avec les détails de la ligne de contrat ou les détails de la ligne de devis.
- **Mettre à jour les prix** est manquant pour les estimations des dépenses.
-  Les clients ne peuvent pas sélectionner des raisons de statut de contrat personnalisées dans la page **Contrat du projet**.
- Les clients constatent une dégradation des performances lors de la création de tarifs personnalisés à partir d’un devis.
- Les clients constatent une incohérence dans les valeurs par défaut pour **unité** sur les pages **Détails de la ligne de devis** et **Détails de la ligne de contrat**.
- L’ajout d’éléments de catégorie de transaction non facturables à une ligne de contrat facturable ne respecte pas le type de facturation **Non facturable** de la catégorie de transaction.
- Les clients ne peuvent pas utiliser les nouveaux rôles et la nouvelle catégorie ajoutés sur les contrats déjà créés.
- Ls clients constatent une dégradation des performances. Récupération inutile dans PreValidateProjectTeamMemberUpdate.cs
- Les rôles définis comme non facturables dans la liste **Catégories de ressource** doivent être ajoutés à l’onglet **Rôles facturables** en tant que **Non facturables** sur la ligne de contrat d’un projet.
- Les clients peuvent constater une dégradation des performances lors de la création d’un projet, car **GetBookableResourceIdFromUser** récupère toutes les colonnes de ressources réservables au lieu de l’ID principal.
- L’entité **TransactionType** ne dispose pas du plug-in de mise à jour avant validation qui empêche les utilisateurs d’entrer **Units** et **UnitGroups** qui ne sont pas valides pour les types de transaction.
- L’étape **Supprimer** ne fonctionne pas pour l’importation d’entrées de temps.


[!INCLUDE[footer-include](../includes/footer-banner.md)]