---
title: Nouveautés ou modifications de la mise à jour (version 32) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Project Service Automation version 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912881"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Nouveautés ou modifications de la mise à jour (version 32) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour version 32 de Project Service Automation V3. Cette version porte le numéro de build V3.10.53.108 et est généralement disponible via une mise à jour automatique en juin 2021.

## <a name="update-release-32"></a>Mise à jour (version 32)

### <a name="bug-fixes"></a>Corrections de bogues

#### <a name="general"></a>GÉNÉRAL

- Lorsqu’une mise à niveau majeure échoue, seuls les principaux points d’entrée de l’application doivent être bloqués, afin de garantir que les entités partagées sont toujours accessibles.

#### <a name="time-and-expense"></a>Temps et dépenses

Les problèmes suivants ont été résolus :

- **TimeEntriesImportFromResourceAssignment** ne conserve pas les heures de début et de fin des secteurs de profil de l’affectation des ressources.
- Lorsque vous sélectionnez **Ouvrir l’entrée** dans la grille **Entrée de temps**, vous pouvez être empêché de sélectionner d’autres formulaires.
- Pendant que vous importez des affectations dans des entrées de temps, la requête de code client peut générer une longue URL qui fait échouer la requête.
- Dans la grille **Entrée de temps**, après la suppression d’une valeur d’une cellule, le focus ne reste pas dans la grille.
- Le bouton **Rejeter** a été retiré de la vue **Traitement des approbations** pour les approbations modernes.
- La stabilité et les performances de l’approbation en bloc des entrées de temps sont affectées par des blocages et l’incapacité à gérer correctement les personnalisations liées à l’entité **Entrée de temps**.

#### <a name="project-planning"></a>Planification de projet

- Une exception de référence Null est générée lorsque vous mettez à jour un projet qui a une valeur Null dans le champ **Unité contractuelle**.
- **Actualiser les totaux du projet** calcule incorrectement le coût restant et les ventes restantes sur un projet.
- Des calculs de tarification redondants affectent les performances liées aux mises à jour des profils d’affectation des ressources.

#### <a name="resource-management"></a>Gestion des ressources

L’incident suivant a été résolu :

- Lorsque la capacité de calendrier d’une ressource réservable est supérieure à 1, Project Service Automation reconnaît à tort la capacité comme 0 (zéro). Par conséquent, une boucle infinie se produit dans la vue de planification.

#### <a name="sales"></a>Vente

Les problèmes suivants ont été résolus :

- Lorsqu’une ligne de journal est créée avec un type de transaction personnalisé, l’exception de référence Null suivante se produit : *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Les rôles et catégories qui sont désactivés avant la copie d’un devis ne doivent pas être ajoutés aux rôles et catégories facturables du devis nouvellement copié.
- La date du document et la date comptable ne sont pas alignées avec la date de début qui est indiquée sur un détail de ligne de facture créé directement sur une facture provisoire.
- Des exceptions de référence Null sont générées dans les scénarios liés à l’inactivation de rôles et de catégories avant la copie d’un devis.
- L’action **Mettre à jour les prix** de la page **Projets** ne met pas à jour les estimations de dépenses et les estimations du matériel.
