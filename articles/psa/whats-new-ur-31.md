---
title: Nouveautés ou modifications de la mise à jour (version 31) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 31) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586755"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Nouveautés ou modifications de la mise à jour (version 31) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 31) de Project Service Automation V3. Cette version a le numéro de build V3.10.52.77 et est généralement disponible via une mise à jour automatique en mai 2021.

## <a name="update-release-31"></a>Mise à jour (version 31)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Les boutons de commande du contrôle d’entrée de temps sur la page **Ressource réservable** prêtaient à confusion.
- Une exception de référence nulle était générée dans **Project.SetTrackingFields** lors de l’approbation d’une entrée de temps.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- **Créer un membre d’équipe** n’affiche pas correctement le paramètre de métadonnées de configuration de la réservation pour **Statut Réservation par défaut validée**.
- Lors de la mise à niveau de PSA 1.X vers 3.X, le processus de mise à niveau échoue à l’étape **UpgradeResourceRequirements**.


**Vente**

Les problèmes suivants ont été résolus :

- Le revenu réel convertit les montants dans la devise du projet dans la grille de suivi.
- La devise par défaut n’est pas claire lors de la création de lignes de journal, de lignes de devis et de lignes de contrats dans des scénarios où la devise de base d’une organisation diffère de la devise du projet.
- La requête **En attente de validation du journal de correction** ne filtre pas par projet.
- Les ventes restantes sont calculées de manière incorrecte sur un projet.
- Les devis basés sur un contact échouent lorsqu’ils sont créés sans tarif.
- Aucun indicateur de traitement ne s’affiche lorsque vous sélectionnez **Confirmer la facture**.
- Aucun indicateur de traitement ne s’affiche lorsque vous sélectionnez **Créer la facture**.
- La fermeture d’un devis avec le statut Perdu n’annule pas les réservations.







