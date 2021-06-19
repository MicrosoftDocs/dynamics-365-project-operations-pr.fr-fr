---
title: Planifier un projet avec une structure de répartition du travail
description: Procédure de planification d’un projet avec une structure de répartition du travail dans Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008578"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planifier un projet avec une structure de répartition du travail (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Un calendrier de projet communique le travail à effectuer, quelles ressources exécuteront le travail, et le délai dans lequel le travail doit être effectué. Le calendrier de projet reflète toutes les tâches associées à l’exécution du projet dans les temps. L’une des premières étapes au cours de la phase d’initiation du projet est de proposer un calendrier de projet. Pour créer un calendrier de projet, vous devez créer une structure de répartition du travail.  
  
 Créez une structure de projet avec une structure de répartition du travail, qui vous aide à :  
  
- Diviser le travail en tâches gérables  
  
- Évaluer le temps requis pour effectuer une tâche  
  
- Définir des dépendances de tâche et la durée des tâches  
  
- Déterminer les rôles requis pour effectuer chaque tâche  
  
  Le calendrier de projet dans la structure de répartition du travail semble familier, et est complété par un diagramme de Gantt interactif.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Créer une structure de répartition du travail pour un projet  
 Créez une structure de répartition du travail pour représenter la séquence des tâches dans un projet. La structure de répartition du travail comprend des tâches, des exigences pour chaque tâche, et des informations sur le revenu et les coûts. Dans la structure de répartition du travail, vous pouvez ajouter :  
  
-   La séquence de tâches dans une hiérarchie  
  
-   D’autres tâches, le cas échéant, qui doivent être effectuées avant de commencer une tâche  
  
-   La date de début, la date de fin, et la durée d’une tâche  
  
-   Le nombre d’heures requises pour une tâche  
  
-   Toutes les compétences et formations requises des employés  
  
-   Les employés qui sont assignés à une tâche  
  
-   Le revenu et les coûts estimés  
  
## <a name="task-types"></a>Types de tâche  
Vous utiliserez les types de tâches suivantes lors de la création de votre structure de répartition du travail :  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nœud racine du projet**. | La tâche récapitulative de niveau supérieur du projet. Toutes les autres tâches du projet sont créées en dessous. Le nom de la tâche racine est le nom du projet. L’effort, les dates, et la durée du nœud racine sont basés sur les valeurs dans la hiérarchie en dessous. Vous ne pouvez pas modifier les propriétés de nœud racine ou supprimer le nœud racine. | 
| **Tâches récapitulatives ou de conteneur** | Une tâche récapitulative est une tâche qui a des sous-tâches. Une tâche récapitulative n’a pas d’efforts ou coûts de travail qui lui sont propres. Ses efforts et coûts de travail sont un cumul de ses sous-tâches. Vous pouvez modifier le nom d’une tâche récapitulative, mais vous ne pouvez pas modifier l’effort, les dates, ou la durée, car ils sont automatiquement calculés. La suppression d’une tâche récapitulative entraîne la suppression de la tâche et toutes ses sous-tâches.|  
| **Tâches de nœud terminal** | Une tâche de nœud terminal représente le travail le plus détaillé du projet. Elle possède un effort estimé, un nombre de ressources planifiées, des dates de début et de fin planifiées, et une durée.|

  
## <a name="task-hierarchy"></a>Hiérarchie de tâche  
 Vous avez les options suivantes lorsque vous créez une hiérarchie de tâche :  
  
- **Ajouter une tâche**.   Vous pouvez ajouter une tâche à un emplacement choisi dans la hiérarchie de tâche. Si vous ne sélectionnez pas d’emplacement, votre nouvelle tâche apparaît à la fin.  
  
- **Mettre une tâche en retrait**.   Mettez une tâche en retrait pour en faire un enfant de la tâche directement au-dessus.  
  
- **Mettre une tâche en retrait négatif**.   Mettez une tâche en retrait négatif pour qu’elle ne soit plus une sous-tâche de sa tâche parente d’origine.  
  
- **Monter et descendre**.   Déplacez des tâches vers le haut et le bas dans la hiérarchie de sa tâche parente. Le déplacement d’une tâche vers le haut ou le bas n’a aucun impact sur ses coûts, son effort, ses dates, ou sa durée.  
  
## <a name="task-attributes"></a>Attributs de tâche  
 Un nom de tâche décrit le travail devant être effectué. Vous utilisez divers attributs de tâche pour décrire la planification et les exigences en dotation de personnel pour la tâche.  
  
### <a name="schedule-attributes"></a>Attributs de planification

 - Attribuez des valeurs à **Heures d’effort**, **Nombre de ressources**, **Date de début**, **Date de fin** et **Durée** pour déterminer la planification de la tâche. 
 - **Effort** est une estimation des heures nécessaires pour terminer la tâche.
 - **Nombre de ressources** est une estimation que le responsable de projet saisit dans la tâche pour fournir la meilleure planification. 
 - **Durée** (en jours) affiche le nombre de jours de travail nécessaires pour terminer la tâche.  
  
### <a name="staffing-attributes"></a>Attributs de dotation de personnel

 - **Rôle**, **Unité d’organisation de ressources**, **Nombre de ressources** et **Ressources** décrivent les exigences en dotation de personnel pour la tâche. 
 - **Rôle** décrit le type de ressource nécessaire pour effectuer la tâche. 
 - **Unité d’organisation de ressources** indique l’unité d’organisation dont les ressources doivent provenir pour cette tâche ; cela a également un impact sur les estimations de coûts et de ventes de la tâche, puisque c’est pris en compte pour déterminer le prix de vente unitaire de la ressource. 
 - **Ressources** conserve une ressource générique ou une ressource nommée lorsqu’il en y a une.  
  
## <a name="task-dependencies"></a>Dépendances de tâche  
 Vous pouvez créer des relations de prédécesseur entre une ou plusieurs tâches dans la structure de répartition du travail. Vous pouvez définir une ou plusieurs valeurs pour le champ de prédécesseur sur les tâches pour afficher les tâches dont il sera dépendant. Lorsque vous attribuez une valeur de prédécesseur à une tâche, la tâche peut uniquement démarrer lorsque toutes les tâches de prédécesseur sont terminées. La définition de cette dépendance sur une tâche entraînera le recalcul de la date de début planifiée de la tâche comme la dernière date de fin de tous ses prédécesseurs. Les impacts associés au prédécesseur sur un programme ne sont pas limités par le mode de tâche défini sur la tâche.  
  
## <a name="task-mode"></a>Mode de tâche  
 Le mode de tâche est l’un des facteurs importants qui déterminent la planification des tâches de nœud terminal. Il existe deux modes de tâche pour chaque tâche : le mode de planification automatique et le mode de planification manuelle.  
  
-   **Planification automatique**   Lorsque vous définissez le mode de tâche sur Planifiée automatiquement, le moteur de planification de tâche s’appuie sur les règles de planification sur les attributs de tâche suivants pour déterminer la planification de la tâche :  
  
    -   Prédécesseurs  
  
    -   Effort  
  
    -   Nombre de ressources  
  
    -   Les dates de début et de fin  
  
-   **Mes règles de planification**.   La date de début d’une tâche de nœud terminal qui ne dispose pas de prédécesseurs par défaut à la date de début de planification du projet. La durée d’une tâche de nœud terminal est toujours calculée comme le nombre de jours ouvrables entre ses dates de début et de fin. Lorsqu’une tâche est planifiée automatiquement, le moteur de planification suit les règles ci-dessous :  
  
    -   Les dates de début et de fin d’une tâche doivent toujours être des jours ouvrables selon le calendrier de planification du projet  
  
    -   La date de début d’une tâche qui possède des prédécesseurs par défaut à la dernière date de fin de ses prédécesseurs  
  
    -   Effort = nombre de personnes * durée * heures dans un jour de travail standard du calendrier de projet  
  
-   **Planification manuelle**.   Dans certains cas, vous pourriez vouloir dévier de ces règles. Dans ces cas-là, vous pouvez définir le mode de tâche pour que la tâche soit planifiée manuellement. Le moteur de planification arrête de calculer les valeurs pour d’autres attributs de planification. La définition de prédécesseurs sur des tâches a un impact sur la date de début de la tâche dépendante.  
  
## <a name="create-a-work-breakdown-structure"></a>Créer une structure de répartition du travail  
  
1.  Accédez à **Project Service > Projets**.  
  
2.  Cliquez sur le projet sur lequel vous souhaitez travailler.  
  
3.  Dans la barre dans toute la partie supérieure de l’écran, sélectionnez la flèche vers le bas en regard du nom de projet, puis cliquez sur Structure de répartition du travail.  
  
4.  Pour ajouter une tâche, cliquez sur **Ajouter une tâche**. Renseignez les champs requis pour la tâche et cliquez sur **Enregistrer**.  
  
5.  Continuez d’ajouter des tâches jusqu’à ce que votre structure de répartition du travail soit complète. Lors de la création de votre structure de répartition du travail, vous pouvez procéder comme suit pour organiser les tâches :  
  
    -   Sélectionnez une tâche et cliquez sur **Retrait** pour la déplacer sous une autre tâche ou sur Retrait négatif pour la sortir d’un niveau.  
  
    -   Sélectionnez une tâche et cliquez sur **Monter** ou **Descendre** pour la déplacer vers le haut ou le bas dans la liste.  
  
    -   Cliquez sur **Masquer le diagramme de Gantt** pour masquer le diagramme de Gantt, puis cliquez sur **Afficher le diagramme de Gantt** pour l’afficher de nouveau.  
  
    -   Sélectionnez une période autre pour le diagramme de Gantt dans **Échelle de temps**.  
  
6.  Pour ajouter les rôles spécifiés dans votre structure de répartition du travail aux membres de l’équipe de projet, cliquez sur **Générer une équipe de projet**.  
  
7.  Cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l’écran lorsque vous avez fini d’apporter des modifications.  
  
### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]