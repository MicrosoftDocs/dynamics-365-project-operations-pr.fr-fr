---
title: Estimer les ventes et les coûts du projet lorsqu'une ressource réservable remplit plusieurs rôles sur un projet
description: Cette rubrique explique comment utiliser les dimensions de tarification pour prendre en charge les estimations de tarification et de coût pour une ressource qui remplit plusieurs rôles sur un projet.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531421"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimer les ventes et les coûts du projet lorsqu'une ressource réservable remplit plusieurs rôles sur un projet 

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés, le déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication_ 

Les entreprises basées sur des projets ont souvent besoin d'une seule ressource pour remplir plusieurs rôles sur un projet. Chaque rôle peut être tarifé et budgétisé différemment. Cela signifie que le temps consacré à la même ressource sur un projet peut obtenir une estimation financière différente en fonction de la facture et des taux de coût pour chaque rôle. Vous pouvez configurer les valeurs de l'enregistrement de membre de l'équipe pour la ressource nommée avec différents remplacements sur chacune des tâches auxquelles le membre de l'équipe est affecté.

L'exemple suivant vous explique comment le simple remplacement d'une valeur permet à une ressource d'avoir plusieurs rôles sur un projet avec des coûts et des taux de facturation différents.

## <a name="create-tasks"></a>Créer des tâches
Pour créer des tâches, vous devez ajouter des tâches, ainsi que des tâches récapitulatives, après quoi vous devez attribuer la tâche avant d'ajouter la durée de la tâche. 

### <a name="add-tasks-and-summary-tasks"></a>Ajouter des tâches et des tâches récapitulatives
Pour ajouter une tâche, procédez comme suit.

1. Accédez à **Projets** et ouvrez le projet auquel vous souhaitez ajouter des tâches.
2. Sélectionnez **Ajouter une nouvelle tâche**. Nommez la tâche et appuyez sur **Entrée**.
3. Entrez un autre nom de tâche et appuyez sur **Entrée**. Recommencez jusqu'à ce que vous ayez une liste complète des tâches.
3. Pour mettre en retrait les tâches sous les tâches **récapitulatives**, sélectionnez les trois points verticaux à côté du nom de la tâche, puis sélectionnez **Créer une sous-tâche**. 

  > [!TIP]
  > Pour sélectionner plusieurs tâches, sélectionnez une tâche, maintenez la touche **Ctrl** enfoncée, puis sélectionnez une autre tâche.
  >
  > Vous pouvez également choisir **Promouvoir la sous-tâche** pour retirer des tâches des tâches **récapitulatives**.

### <a name="assign-tasks"></a>Attribuer des tâches

Pour attribuer des tâche, procédez comme suit.

1. Dans la colonne **Affecté à** pour une tâche, sélectionnez l'icône de personne.
2. Choisissez un membre de l'équipe dans la liste ou saisissez du texte pour rechercher un nom.

### <a name="add-task-duration-and-columns"></a>Ajouter une durée de tâche et des colonnes

Il est souvent plus simple de commencer par construire votre projet avec une durée. Pour ajouter une durée de tâche, procédez comme suit.

1. Dans la colonne **Durée** d'une tâche, tapez le nombre de jours qui seront nécessaires pour accomplir la tâche. Si vous souhaitez utiliser une autre unité de temps, entrez un nombre plus le mot **heures**, **semaines** ou **mois**.
2. Si vous souhaitez que votre tâche apparaisse comme un jalon en forme de losange dans la vue **Chronologie**, dans la colonne **Durée**, entrez **0 jours**.
3. Appuyez sur **Entrée** pour passer au champ **Durée** de la tâche suivante et continuez à saisir les durées.

  > [!NOTE]
  > Vous ne pouvez pas entrer une durée pour les tâches récapitulatives.

Vous pouvez ajouter des colonnes à votre projet pour fournir plus de détails. Pour ce faire, sélectionnez **Ajouter une colonne**. 

Pour plus d’informations, voir [Créer un projet](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurer le rôle et l'unité d'organisation d'un membre d'équipe de projet générique
Effectuez les étapes suivantes pour configurer un rôle et une unité d’organisation pour un membre d'équipe générique.

1. Sur la page **Tâches**, sélectionnez la ligne **Tâche** de la **Tâche A**. 
2. Dans **Affecté à**, sélectionnez **Ajouter une ressource générique**. Cela ouvre la page **Création rapide d'un membre de l'équipe**.
3. Sur la page **Créer rapidement un membre d’équipe**, spécifiez les attributs du membre générique de l’équipe qui peut effectuer cette tâche.
4. Sélectionnez le rôle et l’unité organisationnelle appropriés, puis sélectionnez **Enregistrer et fermer**. Un membre de l’équipe générique est créé et affecté à cette tâche. 
5. Répétez les étapes 1 à 4 pour la **Tâche B**. Cependant, la **Tâche B** doit avoir un rôle et une unité d’organisation différents de ceux de la **Tâche A** pour le membre d'équipe générique. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurer le rôle et l'unité d'organisation d'une tâche de projet
Pour configurer un rôle et une unité d’organisation pour une tâche, procédez comme suit.

1. Après avoir créé la **Tâche A**, sélectionnez la tâche, puis sélectionnez l' icône **i** pour ouvrir le volet **Détails de la tâche**. 
2. Sur le volet **Détails de la tâche**, faites défiler vers le bas et sélectionnez **Afficher les détails** pour ouvrir la page **Détails de la tâche**.
3. Sur la page **Détails de la tâche**, dans **Rôle** et **Unité d’organisation**, ajoutez les valeurs requises pour exécuter cette tâche pour la ressource. 

  > [!NOTE]
  > Si vous terminez ce scénario à l'aide des données de démonstration Project Operations, sélectionnez **Consultant Lead** comme rôle et **Fabrikam États-Unis** comme unité d’organisation.

4. Sélectionnez **Tâche B** et sélectionnez la tâche.
5. Sélectionnez l' icône **i** pour ouvrir le volet **Détails de la tâche**. 
6. Sur le volet **Détails de la tâche**, faites défiler vers le bas et sélectionnez **Afficher les détails** pour ouvrir la page **Détails de la tâche**.
7. Sur la page **Détails de la tâche**, dans **Rôle** et **Unité d’organisation**, ajoutez les valeurs requises pour une ressource qui exécuterait cette tâche. Les valeurs de **Rôle** et **Unité d'organisation** pour la **Tâche B** doivent être différents de celles de la **Tâche A**. 

  > [!NOTE]
  > Si vous terminez ce scénario à l'aide des données de démonstration Project Operations, sélectionnez **Technicien réseau** comme rôle et **Fabrikam États-Unis** comme unité d’organisation.

8. Enregistrez et fermez la page **Détails de la tâche**. 

## <a name="team-member-and-estimates-behavior"></a>Membre de l'équipe et comportement des estimations 
Pour comprendre le comportement dans la grille **Membre de l'équipe** et les estimations, procédez comme suit.

1. Sur la grille **Membre de l'équipe**, sélectionnez les deux membres d'équipe générique, puis sélectionnez **Générer des exigences**. Cela génère des besoins en ressource. 
2. Sélectionnez la ligne du membre de l’équipe pour le champ **Consultant**, puis sélectionnez **Réserver**. Le tableau de planification s'ouvre avec une liste de ressources. Sélectionnez une ressource, puis sélectionnez **Réserver** pour réserver la ressource de cette exigence.
3. Sélectionnez la ligne du membre de l’équipe pour le champ **Technicien réseau**, puis sélectionnez **Réserver**. Le tableau de planification s'ouvre avec une liste de ressources. Sélectionnez la même ressource que ci-dessus, puis sélectionnez **Réserver** pour réserver la ressource de cette exigence.

### <a name="team-member-grid"></a>Grille du membre de l’équipe 

Sur la grille **Membre de l'équipe**, les deux enregistrements de membre d'équipe générique sont supprimés et remplacés par une seule ressource. Il existe un ensemble de valeurs pour cette ressource, qui est un ensemble de valeurs par défaut pour **Rôle** et **Unité d'organisation**.

Lorsque vous développez la ligne pour cet enregistrement de membre de l'équipe, vous pouvez voir des affectations distinctes sur l'enregistrement de membre de l'équipe pour les deux tâches. Chaque ligne d’affectation a des valeurs spécifiques à la tâche pour **Rôle** et **Unité organisationnelle**. 

### <a name="estimates-grid"></a>Grille des estimations 

Sur la grille **Estimations**, les deux affectations pour la même ressource sont tarifées différemment. L’affectation de la ressource sur la **Tâche A** est tarifée en utilisant la valeur d’attribut **Rôle** de **Chargé de conseil**. L’affectation de la même ressource sur la **Tâche B** est tarifée en utilisant la valeur d’attribut **Rôle** de **Technicien réseau**.
