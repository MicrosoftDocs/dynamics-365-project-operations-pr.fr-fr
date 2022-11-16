---
title: Planification externe
description: Cet article fournit des informations sur la planification externe.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736961"
---
# <a name="external-scheduling"></a>Planification externe

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Le mode de planification externe vous permet de créer, mettre à jour et supprimer de manière native des entités liées aux structures de répartition du travail (WBS), mais sans les limites actuelles appliquées par Microsoft Project for the Web. Il fournit également une validation limitée. Ce mode ne doit être utilisé que par les clients suivants :

- Clients disposant des outils nécessaires pour définir une WBS en dehors de la logique de planification fournie par Project Operations
- Les clients qui doivent gérer la hiérarchie des horaires, les dépendances ou la durée des tâches

> [!IMPORTANT]
> Les données qui ne sont pas correctement saisies dans les entités liées à WBS peuvent ne pas être affichées dans la grille de rapprochement des ressources, la grille des estimations, la grille de suivi ou la grille d’affectation des ressources.

## <a name="configuration"></a>configuration

Cette fonctionnalité est activée par défaut. Cependant, sur la page principale prête à l’emploi pour les projets, le champ associé n’est pas visible par défaut. Pour activer le champ, dans Maker Portal, ouvrez la page principale de l’entité de projet, sélectionnez le champ **Moteur de planification**, puis modifiez le champ sur **Visible par défaut**. Si vous n’utilisez pas la page principale du projet prête à l’emploi, modifiez votre page existante et ajoutez-y le champ **Moteur de planification**.

## <a name="settings"></a>Paramètres

Pour utiliser le mode de planification externe, vous devez d’abord créer un projet et sélectionner le moteur de planification **Planifié en externe** dans la liste déroulante de la page principale du projet. Une fois ce mode configuré pour un projet, il ne peut plus être modifié.

## <a name="viewing-the-wbs"></a>Affichage de la WBS

Si un projet est planifié en externe, l’accès à Project for the Web est restreint pour ce projet. Pour afficher la WBS, vous devez accéder à la grille de suivi, où la WBS complète est affichée.

## <a name="creating-and-editing-the-wbs"></a>Création et modification de la WBS

Si la planification externe est activée pour un projet, vous devez définir les données pour toutes les entités liées à la WBS, y compris les tâches, les membres de l’équipe, les affectations de ressources et les dépendances.

L’illustration suivante présente le modèle de données pour la planification de projet.

![Modèle de données de planification de projet.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Restrictions fonctionnelles

Les opérations suivantes ne sont pas autorisées sur les projets planifiés en externe.

### <a name="project-planning"></a>Planification de projet

- **Copier le projet** : cette opération n’est pas prise en charge sur les projets planifiés en externe.
- **Déplacer le projet** : les modifications apportées à la date de début d’un projet ne déplacent pas le début des tâches ou des affectations de ressources dans la WBS.
- **Mise à jour du chef de projet** : les modifications apportées au chef de projet sur la page principale du projet ne créent pas automatiquement un nouveau membre de l’équipe de projet tant que le projet n’aura pas été converti.
- **Mise à jour du modèle d’heures de travail du projet** : les modifications apportées au modèle d’heures de travail du projet ne recalculent pas le calendrier du projet.
- **Contours d’affectation des ressources** : la création d’affectations de ressources ne met pas automatiquement à jour le champ **mdyn\_PlannedWork**. Ce champ est utilisé pour stocker les contours de l’effort d’affectation des ressources. Si vous affichez l’effort échelonné dans le temps dans la grille d’affectation des ressources ou la grille de rapprochement des ressources, vous devez définir des contours d’affectation des ressources valides. Ces contours doivent être correctement formatés pour qu’ils déclenchent le calcul des contours de coûts et des contours de prix de vente. Nous vous recommandons de créer un projet de test planifié par Project for the Web, puis d’examiner les données associées pour confirmer les exigences et la mise en forme.

### <a name="resource-management"></a>Gestion des ressources

- **Exécution des ressources génériques** : l’exécution des ressources génériques n’est pas prise en charge pour les projets planifiés en externe. Les tentatives de répondre aux exigences ouvertes actives créent de nouveaux membres d’équipe de projet, mais cela ne supprime pas le membre d’équipe générique ni ne remplace le membre d’équipe générique sur les affectations de ressources existantes.
- **Supprimer un membre de l’équipe** : la suppression d’un membre de l’équipe ne supprime pas automatiquement les affectations de ressources.

### <a name="quoting-and-contracting"></a>Devis et contractualisation

- **Importation des détails de la ligne de devis et de la ligne de contrat** : lorsque les détails d’un devis ou d’une ligne de contrat sont importés d’un projet, l’application a été testée pour prendre en charge un maximum de 500 tâches dans la WBA, sur la base d’une limite de 20 affectations par tâche.

### <a name="actuals-and-invoicing"></a>Réels et facturation

- Bien qu’il n’y ait aucun changement dans les validations existantes entre la WBS et les transactions financières, il est important que vous vous conformiez au modèle de données prêt à l’emploi, pour vous assurer que toutes les transactions en aval s’exécutent comme prévu.
