---
title: Estimer les ventes et les coûts du projet lorsqu’une ressource réservable remplit plusieurs rôles sur un projet
description: Cette rubrique fournit des informations sur l’utilisation des dimensions de tarification pour prendre en charge la tarification et le coût pour une ressource qui remplit plusieurs rôles sur un projet.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f8b84de740a3d610e49acea8fa13885b977b440c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590711"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimer les ventes et les coûts du projet lorsqu’une ressource réservable remplit plusieurs rôles sur un projet 

[!include [banner](../includes/psa-now-project-operations.md)]

Les entreprises basées sur des projets ont souvent besoin d’une seule ressource pour remplir plusieurs rôles sur un projet. Chacun de ces rôles pourrait être évalué différemment en termes de prix et de coût. Autrement dit, le même temps de la ressource dans le projet pourrait obtenir une autre estimation financière en fonction des taux de facturation et de coût pour chacun des rôles. Project Service Automation permet de configurer les valeurs sur l’enregistrement de membre de l’équipe pour la ressource désignée et permet également différents remplacements sur chacune des tâches auxquelles le membre de l’équipe est attribué.

L’exemple suivant explique comment le simple remplacement de cette valeur permet à une ressource d’avoir plusieurs rôles sur un projet avec différents taux de facturation et de coût.

## <a name="create-tasks"></a>Créer des tâches
Créez deux tâches de projet pour 40 heures chacune. Nous les appellerons Tâche A et Tâche B. Sélectionnez la Tâche A comme prédécesseur à la Tâche B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurer le rôle et l’unité organisationnelle pour un membre de l’équipe de projet générique

1. Sur la page **Programme**, sélectionnez la ligne **Tâche** pour la Tâche A. 
2. Dans le champ **Ressources**, sélectionnez **Créer** dans la liste déroulante.
3. Sur la page **Créer rapidement un membre d’équipe**, spécifiez les attributs du membre générique de l’équipe qui peut effectuer cette tâche.
4. Sélectionnez le rôle et l’unité organisationnelle appropriés, puis sélectionnez **Enregistrer et fermer**. Un membre de l’équipe générique est créé et affecté à cette tâche. 

Répétez ces étapes pour la Tâche B et veillez à ce que le rôle et l’unité organisationnelle sur le membre de l’équipe générique créés pour la Tâche B soit différents de ceux de la Tâche A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurer un rôle et une unité organisationnelle pour une tâche de projet

1. Après avoir créé la Tâche A, sélectionnez la tâche, puis sélectionnez **Modifier la tâche**.
2. Sur la page **Détails de la tâche**, recherchez les champs **Rôle** et **Unité organisationnelle**, ajoutez les valeurs nécessaires d’une ressource qui effectuerait cette tâche. 

  > [!NOTE]
  > Si vous exécutez ces scénarios avec les données de démonstration Project Service Automation, sélectionnez **Consultant** pour le rôle et **Fabrikam US** comme unité organisationnelle.

3. Sélectionnez Tâche B, puis sélectionnez **Modifier la tâche**.
4. Sur la page **Détails de la tâche**, recherchez les champs **Rôle** et **Unité organisationnelle**, ajoutez les valeurs nécessaires d’une ressource qui effectuerait cette tâche. Assurez-vous que les valeurs des champs **Rôle** et **Unité organisationnelle** sont différents pour la tâche B des valeurs pour la tâche A. 

  > [!NOTE]
  > Si vous exécutez ces scénarios avec les données de démonstration Project Service Automation, sélectionnez **Technicien réseau** pour le rôle et **Fabrikam US** comme unité organisationnelle.

5. Enregistrez et fermez la page **Détails de la tâche**. 

## <a name="team-member-and-estimates-behavior"></a>Membre de l’équipe et comportement des estimations 

1. Sur la page **Détails de la tâche**, sur le champ **Membre de l’équipe**, sélectionnez les deux membres de l’équipe générique, puis sélectionnez **Générer des besoins**. 
2. Sélectionnez la ligne du membre de l’équipe pour le champ **Consultant**, puis sélectionnez **Réserver**. Le tableau de bord de planification ouvre et réserve une ressource pour ce besoin.
3. Sélectionnez la ligne du membre de l’équipe pour le champ **Technicien réseau**, puis sélectionnez **Réserver**. Le tableau de bord de planification ouvre et réserve la même ressource pour ce besoin.

### <a name="team-member-grid"></a>Grille du membre de l’équipe 
Dans la grille **Membre de l’équipe**, notez que les deux enregistrements de membre de l’équipe générique ont été supprimés et remplacés par une ressource. Il existe un ensemble de valeurs pour cette ressource qui affiche un ensemble de valeurs par défaut pour les champs **Rôle** et **Unité organisationnelle**.
Lorsque vous développez la ligne de cet enregistrement Membre de l’équipe, vous pouvez voir différentes affectations sur l’enregistrement du membre de l’équipe pour ces deux tâches. Chaque ligne d’affectation a des valeurs spécifiques à la tâche pour **Rôle** et **Unité organisationnelle**. 

### <a name="estimates-grid"></a>Grille des estimations 
Lorsque vous accédez à la grille **Estimations**, vous observerez que les deux affectations pour la même ressource ont des tarifs différents.
L’affectation de la ressource sur la Tâche A est tarifée en utilisant la valeur d’attribut **Rôle** de **Consultant**. L’affectation de la même ressource sur la Tâche B est tarifée en utilisant la valeur d’attribut **Rôle** de **Technicien réseau**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
