---
title: Planifications de projets
description: Cette rubrique donne des informations sur la création d'une planification.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075775"
---
# <a name="project-schedules"></a>Planifications de projets 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un calendrier de projet communique le travail à effectuer, quelles ressources exécuteront le travail, et le délai dans lequel le travail doit être terminé. Il reflète toutes les tâches associées à l'exécution du projet dans les temps. Dans Dynamics 365 Project Service Automation, vous créez un calendrier de projet en fractionnant le travail en tâches gérables, en évaluant le temps requis pour effectuer chaque tâche, en définissant des dépendances de tâches, en configurant des durées de tâches, et en évaluant les ressources génériques qui feront les tâches. Le calendrier du projet est créé sur l'onglet **Planification** de la page de projet.
 
## <a name="tasks"></a>Tâches

La première étape de création d'un calendrier de projet consiste de répartir le travail en parties gérables. La planification dans PSA prend en charge les fonctionnalités suivantes :

- Nœud racine du projet.
- Tâches récapitulatives ou de conteneur
- Tâches de nœud terminal

### <a name="project-root-node"></a>Nœud racine du projet.

Le nœud racine du projet est la tâche récapitulative générale du projet. Toutes les autres tâches du projet sont créées en dessous. Le nom du nœud racine est toujours défini sur le nom du projet. L'effort, les dates, et la durée du nœud racine sont récapitulés selon les valeurs dans la hiérarchie en dessous. Vous ne pouvez pas modifier les propriétés du nœud racine. Vous ne pouvez pas non plus supprimer le nœud racine.

### <a name="summary-or-container-tasks"></a>Tâches récapitulatives ou de conteneur 

Les tâches récapitulatives ont des sous-tâches ou des tâches de conteneur sous elles. Elles n'ont pas elles-mêmes d'effort ou coût de travail. Au lieu de cela, les efforts de travail et de coût sont un report de l'effort de travail et du coût de leur tâches de conteneur. La date de début de la tâche récapitulative est la date de début des tâches de conteneur, et la date de fin est la date de fin des tâches de conteneur. Le nom d'une tâche récapitulative peut être modifié, mais les propriétés de planification (effort, dates et durée) ne peuvent pas être modifiées. Si vous supprimez une tâche récapitulative, vous supprimez également toutes ses tâches de conteneur.

### <a name="leaf-node-tasks"></a>Tâches de nœud terminal

Les tâches de nœud terminal représentent le travail le plus granulaire du projet. Ils possèdent un effort estimé, des ressources, des dates de début et de fin planifiées, et une durée.
 
## <a name="creating-a-task-hierarchy"></a>Création d'une hiérarchie de tâches

Vous pouvez créer une hiérarchie de tâches avez les options suivantes :

- Bouton **Ajouter une tâche**
- Bouton **Mettre une tâche en retrait**
- Bouton **Mettre une tâche en retrait négatif**
- Boutons **Monter** et **Descendre**.
- Raccourcis clavier et accessibilité

### <a name="add-task"></a>Ajouter une tâche

Le bouton **Ajouter une tâche** vous permet de créer une tâche dans la hiérarchie. Si vous ne sélectionnez pas d'emplacement, la tâche est insérée à la fin. 

Un ID de planification est affecté à chaque tâche. L'ID de planification représente le degré de la tâche et sa place dans la hiérarchie. Il utilise la numérotation d'ensemble. Pour les tâches du premier niveau sous le nœud racine du projet, un schéma de numérotation de 1, 2, 3, etc., est utilisé. Pour les tâches sous le premier niveau, un schéma de numérotation de 1.1, 1.2, 1.3, etc., est utilisé.

### <a name="indent-task"></a>Mettre une tâche en retrait

Lorsqu'une tâche est mise en retrait, elle devient rapidement un enfant de la tâche directement supérieure à celle-ci. L'ID de planification de la tâche est alors recalculé de sorte qu'il soit basé sur l'ID de planification de son nouveau parent et suive le schéma de numérotation d'ensemble. La tâche parente est désormais une tâche récapitulative ou une tâche de conteneur. Par conséquent, elle devient un report de ses tâches enfants.

### <a name="outdent-task"></a>Mettre une tâche en retrait négatif 

Lorsqu'une tâche est mise en retrait négatif, ce n'est plus un enfant de la tâche qui était son parent. L'ID de planification est alors recalculé afin qu'il reflète le degré mis à jour de la tâche et sa place dans la hiérarchie. L'effort, le coût et les dates de la tâche parente précédente sont recalculés afin qu'ils n'incluent pas cette tâche.

### <a name="move-up-and-move-down"></a>Monter et Descendre 

Les boutons **Monter** et **Descendre** modifient la place d'une tâche dans la hiérarchie parente. Les modifications de ce type n'affectent pas l'effort, le coût, les dates, ou la durée de la tâche. Seul l'ID de la planification de la tâche est affecté. L'ID de planification est recalculé afin qu'il reflète la nouvelle place de la tâche dans la liste des tâches enfants du parent.

### <a name="accessibility-and-keyboard-shortcuts"></a>Raccourcis clavier et accessibilité

La grille **Planification** est entièrement accessible et peut être utilisée avec des lecteurs d'écran, tels que Narrateur, JAWS ou NVDA. Vous pouvez vous déplacer dans la zone de la grille à l'aide des flèches (comme dans Microsoft Excel), vous pouvez utiliser la touche Tabulation pour avancer dans les éléments d'interface utilisateur interactifs, et vous pouvez utiliser flèche vers le bas, la touche Entrée ou la barre d'espace pour sélectionner et appeler les menus déroulants. Les en-têtes de colonnes sont également interactifs. Vous pouvez masquer et afficher des colonnes, utiliser la touche Tabulation et les flèches pour vous déplacer dans les en-têtes de colonnes, puis utiliser les boutons d'action dans la barre d'outils. En outre, il est possible d'utiliser les raccourcis clavier suivants :

- **Actualiser**  : ALT+MAJ+F5
- **Ajouter**  : ALT+MAJ+Insert
- **Supprimer**  : ALT+MAJ+Suppr.
- **Monter/Descendre**  : ALT+MAJ+Flèches vers le haut/bas
- **Retrait/Retrait négatif**  : ALT_MAJ+Flèches de gauche/droite
- **Développer/Réduire les hiérarchies**  : ALT+MAJ+Touches Plus/Moins

## <a name="task-attributes"></a>Attributs de tâche

Un nom de tâche décrit le travail devant être effectué. Dans PSA, les attributs associés à une tâche décrivent la planification de la tâche et de ses exigences en dotation de personnel.

> ![Attributs de tâche](media/project-2.png)
 
### <a name="schedule-attributes"></a>Attributs de planification

Les attributs **Effort** , **Date de début** , **Date de fin** et **Durée** définissent la planification de la tâche.

Les attributs de planification supplémentaires comprennent :

- **Heures d'effort**  : Entrez une estimation des heures nécessaires pour exécuter la tâche. 
- **Durée**  : Spécifiez le nombre de jours ouvrables nécessaires pour exécuter la tâche.
- **ID de planification**  : Cet ID généré automatiquement est utilisé pour ordonner les tâches dans la hiérarchie. Les dépendances entre les tâches gèrent la commande réelle dans laquelle les tâches sont exécutées.
 
### <a name="staffing-attributes"></a>Attributs de dotation de personnel

Les attributs de dotation en personnel sont accessibles via le champ **Ressources** dans la planification. Vous pouvez rechercher une ressource existante, ou cliquer sur **Créer** , puis dans le volet **Création rapide** , ajoutez un membre de l'équipe du projet comme nouvelle ressource.

Les champs **Rôle** , **Unité d'allocation des ressources** et **Nom du poste** sont utilisés pour décrire les exigences en dotation de personnel de la tâche. Ces attributs de dotation en personnel, ainsi que la planification de tâche, sont utilisés pour rechercher les ressources disponibles pour effectuer cette tâche.

**Rôle**  : Spécifiez le type de ressource nécessaire pour effectuer la tâche.

**Unité d'allocation des ressources**  : Spécifiez l'unité à laquelle les ressources de la tâche doivent être affectées. Cet attribut n'affecte pas l'estimation des coûts et des ventes de la tâche si le taux de coût et de facture de la ressource sont définis selon les unités d'allocation des ressources.

**Nom de poste**  : Entrez un nom convivial pour la ressource générique qui sert d'espace réservé à la ressource qui effectuera le travail au final.

Le champ **Ressources** gère le nom de la place de la ressource générique ou de la ressource nommée lorsqu'une est trouvée.

Le champ **Catégorie** gère les valeurs qui indiquent un type de travail élargi dans lequel il est possible de regrouper la tâche. Ce champ n'affecte pas la planification ou la dotation en personnel. Il a utilisé uniquement pour la génération de rapports.

### <a name="task-dependencies"></a>Dépendances de tâche 

Vous pouvez utiliser la planification dans PSA pour créer une relation de prédécesseur entre les tâches. Le champ **Prédécesseur** sous **Tâches** prend une ou plusieurs valeurs pour identifier les tâches dont dépend une tâche. Lorsque vous attribuez des valeurs de prédécesseur à une tâche, la tâche peut démarrer uniquement une fois toutes les tâches de prédécesseur terminées. En raison de la dépendance, la date de début planifiée pour la tâche est redéfinie à la date où les tâches de prédécesseur sont terminées.

Le mode de tâche n'a aucun impact sur les mises à jour apportées aux dates de début et de fin des tâches de prédécesseur/dépendantes.

## <a name="task-mode"></a>Mode de tâche 

Le mode de tâche détermine la planification des tâches de nœud terminal. PSA prend en charge deux modes de tâche pour chaque tâche : la planification automatique et la planification manuelle.

### <a name="auto-scheduling"></a>Planification automatique 
 
Lorsque le mode de tâche est défini sur **Planifiée automatiquement** pour une tâche, le moteur de planification de tâche s'appuie sur les règles de planification sur les attributs de tâche pour déterminer la planification de la tâche.

#### <a name="scheduling-rules"></a>Règles de planification

Par défaut, si une tâche de nœud terminal ne dispose pas de prédécesseurs, sa date de début est définie sur celle planifiée pour le projet. La durée d'une tâche de nœud terminal est toujours calculée comme le nombre de jours ouvrables entre ses dates de début et de fin. Lorsqu'une tâche est planifiée automatiquement, le moteur de planification suit ces règles :

- Les dates de début et de fin de la tâche doivent toujours être des jours ouvrables selon le calendrier de planification du projet. 
- Pour chaque tâche qui possède des tâches de prédécesseur, la date de début est définie automatiquement sur la dernière date de fin de ses prédécesseurs.
- L'effort est calculé à l'aide de cette formule : Nombre de personnes × Durée × Heures dans une journée de travail standard dans le calendrier de projet.

### <a name="manual-scheduling"></a>Planification manuelle

Si les règles de la planification automatique ne répondent pas aux exigences, vous pouvez définir le mode de tâche sur la tâche **Planification manuelle**. Ce paramètre arrête le moteur de planification de calculer les valeurs d'autres attributs de planification. Quel que soit le mode de tâche, si vous définissez les prédécesseurs sur des tâches, vous affectez toujours la date de début de la tâche dépendante.
