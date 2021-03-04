---
title: Créer une structure de répartition du travail
description: Cette rubrique explique comment créer une structure de répartition du travail (WBS) incluant les commandes de base dans la nouvelle interface de planification.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841334"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Créer une structure de répartition du travail (WBS)

Un calendrier de projet communique le travail à effectuer, quelles ressources exécuteront le travail, et le délai dans lequel le travail doit être terminé. Le calendrier reflète toutes les tâches associées à l’exécution du projet dans les temps. Dans Dynamics 365 Project Operations, vous créez un calendrier de projet en :

  - Divisant le travail en tâches gérables.
  - Estimant le temps nécessaire pour effectuer chaque tâche.
  - Définissant des dépendances de la tâche.
  - Définissant les durées des tâches.
  - Estimant les ressources génériques qui effectueront les tâches. 

Le calendrier du projet est créé sur l’onglet **Planification** de la page **Projet**.

## <a name="tasks"></a>Tâches

La première étape de création d’un calendrier de projet consiste de répartir le travail en parties gérables. La planification dans Project Operations prend en charge les fonctionnalités suivantes :

- Tâches récapitulatives ou de conteneur
- Tâches de nœud terminal

### <a name="summary-tasks"></a>Tâches récapitulatives

Les tâches récapitulatives peuvent stocker d'autres tâches récapitulatives ou des tâches de nœud feuille. Elles n’ont pas elles-mêmes d’effort ou coût de travail. Au lieu de cela, les efforts de travail et de coût sont un report de l’effort de travail et du coût de leur tâches de conteneur. La date de début de la tâche récapitulative est la date de début des tâches de conteneur, et la date de fin est la date de fin des tâches de conteneur. Le nom d’une tâche récapitulative peut être modifié, mais les propriétés de planification, notamment effort, dates et durée, ne peuvent pas être modifiées. Si vous supprimez une tâche récapitulative, vous supprimez également toutes ses tâches de conteneur.

### <a name="leaf-node-tasks"></a>Tâches de nœud terminal

Les tâches de nœud terminal représentent le travail le plus granulaire du projet. Ils possèdent un effort estimé, des ressources, des dates de début et de fin planifiées, et une durée.

## <a name="create-a-task-hierarchy"></a>Création d’une hiérarchie de tâches

### <a name="add-a-task"></a>Ajout d’une tâche

Pour ajouter une ou plusieurs tâches, procédez comme suit.

1. Aller à **Projets** et sélectionnez et ouvrez l'enregistrement de projet pour lequel vous souhaitez créer une planification. 
2. Cliquez sur l'onglet **Tâches**. 
3. Sélectionnez **Ajouter une nouvelle tâche**, entrez un nom pour la tâche, puis appuyez sur Entrée.
2. Entrez un autre nom de tâche et appuyez à nouveau sur Entrée jusqu'à ce que vous ayez une liste complète des tâches.

### <a name="manage-hierarchy-of-a-task"></a>Gestion de la hiérarchie d'une tâche

Lorsqu’une tâche est mise en retrait, elle devient rapidement un enfant de la tâche directement supérieure à celle-ci. L’ID de planification de la tâche est alors recalculé de sorte qu’il soit basé sur l’ID de planification de son nouveau parent et suive le schéma de numérotation d’ensemble. La tâche parent est désormais une tâche récapitulative. Par conséquent, elle devient un report de ses tâches enfants. Lorsqu’une tâche est promue, ce n’est plus un enfant de la tâche qui était son parent. L’ID de planification est alors recalculé afin qu’il reflète le degré mis à jour de la tâche et sa place dans la hiérarchie. L’effort, le coût et les dates de la tâche parente précédente sont recalculés afin qu’ils n’incluent pas cette tâche.

Pour ajouter mettre en retrait ou promouvoir une tâche, procédez comme suit.

1. Sur la page **Projet**, sous l'onglet **Tâches** sous les **tâches récapitulatives**, sélectionnez les trois points verticaux à côté du nom de la tâche, puis sélectionnez **Créer une sous-tâche**. 
2. Sélectionnez la tâche à mettre en retrait ou à promouvoir. Pour sélectionner plusieurs tâches, sélectionnez une tâche, maintenez la touche Ctrl enfoncée, puis sélectionnez des tâches supplémentaires.
2. Choisissez **Mettre en retrait** ou **Promouvoir la sous-tâche** pour déplacer vers le haut ou vers le bas des tâches récapitulatives.

### <a name="move-tasks-up-and-down"></a>Monter et Descendre des tâches

Les tâches peuvent être déplacées à n'importe quel niveau de la structure de répartition du travail de l'une des deux manières suivantes :

- Sélectionnez une ou plusieurs tâches et faites-les glisser vers l'emplacement souhaité.
- Sélectionnez une ou plusieurs tâches, faites un clic droit et sélectionnez **Couper**, sélectionnez la cellule de destination dans la planification, puis cliquez avec le bouton droit et sélectionnez **Coller**.

## <a name="task-attributes"></a>Attributs de tâche

Un nom de tâche décrit le travail devant être effectué. Dans Project Operations, les attributs associés à une tâche décrivent la planification de la tâche et de ses exigences en dotation de personnel.

## <a name="schedule-attributes"></a>Attributs de planification

Les attributs **Effort**, **Date de début**, **Date de fin** et **Durée** définissent la planification de la tâche.

Le tableau suivant présente des attributs de planification supplémentaires.

| **Nom d'affichage final** | **Description finale** |
| --- | --- |
| Effort réalisé (en heures) | Travail terminé pour la tâche en heures. |
| Durée | Affiche la durée de la tâche en jours. |
| Effort total | Travail total pour la tâche en heures. |
| Terminer | Date et heure de fin. |
| % terminé | Pourcentage de réalisation de la tâche. |
| Compartiment du projet | Le tableau des tâches peut être regroupé par compartiment afin que chaque compartiment ait sa propre colonne. |
| Effort restant (en heures) | Travail restant pour la tâche en heures. |
| Démarrer | Date et heure de début. |
| Nom | Nom de la tâche. |
| ID | ID de la tâche dans la structure de répartition du travail. |

## <a name="staffing-attributes"></a>Attributs de dotation de personnel

Les attributs de dotation en personnel sont accessibles via le champ **Ressources** dans la planification. Vous pouvez rechercher une ressource existante, ou cliquer sur **Créer**, puis dans le volet **Création rapide**, ajoutez un membre de l’équipe du projet comme nouvelle ressource.

Les champs **Rôle**, **Unité d’allocation des ressources** et **Nom du poste** sont utilisés pour décrire les exigences en dotation de personnel de la tâche. Ces attributs de dotation en personnel, ainsi que la planification de tâche, sont utilisés pour rechercher les ressources disponibles pour effectuer cette tâche.

   - **Rôle** : Spécifiez le type de ressource nécessaire pour effectuer la tâche.
   - **Unité d’allocation des ressources** : Spécifiez l’unité à laquelle les ressources de la tâche doivent être affectées. Cet attribut n’affecte pas l’estimation des coûts et des ventes de la tâche si le taux de coût et de facture de la ressource sont définis selon les unités d’allocation des ressources.
   - **Nom de poste** : Entrez un nom pour la ressource générique qui sert d’espace réservé à la ressource qui effectuera le travail au final.

Le champ **Ressources** gère le nom de la place de la ressource générique ou de la ressource nommée lorsqu’une est trouvée.

Le champ **Catégorie** gère les valeurs qui indiquent un type de travail élargi dans lequel il est possible de regrouper la tâche. Ce champ n’affecte pas la planification ou la dotation en personnel. Au lieu de cela, le champ est utilisé uniquement pour la création de rapports.

## <a name="task-dependencies"></a>Dépendances de tâche

Vous pouvez utiliser la planification dans Project Operations pour créer une relation de prédécesseur entre les tâches. Le champ **Prédécesseur** utilise une ou plusieurs valeurs pour identifier les tâches dont dépend une tâche. Lorsque vous attribuez des valeurs de prédécesseur à une tâche, la tâche peut démarrer uniquement une fois toutes les tâches de prédécesseur terminées. En raison de la dépendance, la date de début planifiée pour la tâche est redéfinie à la date où les tâches de prédécesseur sont terminées.

Le mode de tâche n’a aucun impact sur les mises à jour apportées aux dates de début et de fin des tâches de prédécesseur/dépendantes.

## <a name="accessibility-and-keyboard-shortcuts"></a>Raccourcis clavier et accessibilité

La grille **Planification** est entièrement accessible et peut être utilisée avec des lecteurs d’écran, tels que Narrateur, JAWS ou NVDA. Vous pouvez vous déplacer dans la zone de la grille à l’aide des flèches (comme dans Microsoft Excel), vous pouvez utiliser la touche Tabulation pour avancer dans les éléments d’interface utilisateur interactifs, et vous pouvez utiliser flèche vers le bas, la touche Entrée ou la barre d’espace pour sélectionner et ouvrir les menus déroulants.


[!INCLUDE[footer-include](../includes/footer-banner.md)]