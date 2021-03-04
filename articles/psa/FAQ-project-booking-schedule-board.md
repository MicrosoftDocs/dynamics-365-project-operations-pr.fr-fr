---
title: Créer une réservation de projet depuis le tableau Planification
description: Cette rubrique fournit des informations sur la création d’une réservation de projet dans le tableau de planification.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146525"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Créer une réservation de projet depuis le tableau Planification

[!include [banner](../includes/psa-now-project-operations.md)]

Vous pouvez réserver une ressource sur un projet directement sur l’onglet **Équipe** ou en générant un besoin en ressource générique depuis une attribution de membre d’équipe, puis en remplissant le besoin généré avec un membre de l’équipe du projet.

Vous pouvez également réserver une ressource sur un projet directement depuis le tableau Planification. Pour vous inscrire, trois méthodes s’offrent à vous.

- **Réserver à partir d’un besoin en ressource généré :** vous pouvez générer un besoin en ressources après avoir créé une ressource générique et attribué des tâches dans un projet.

- **Réserver à partir du besoin principal :** les besoins principaux apparaissent sur le tableau Planification sur l’onglet **Projet**. 

- **Réserver à partir d’un nouveau besoin en ressource :** vous pouvez créer un besoin en ressources du début et l’associer à un projet. Sur le tableau de Planification, le besoin en ressource apparaît sur l’onglet **Ouvrir les besoins**.

## <a name="book-from-a-generated-resource-requirement"></a>Réserver à partir d’un besoin en ressource généré

Vous pouvez créer une ressource générique et lui attribuer une ou plusieurs tâches dans un projet. Vous pouvez ensuite générer un besoin en ressource à partir du membre de l’équipe générique. 

1.  Dans le tableau de Planification, cette ressource s’affiche sur l’onglet **Ouvrir les besoins**. Vous devrez peut-être utiliser des filtres de colonne sur la grille si vous avez de nombreux besoins ouverts. 

    ![Onglet Ouvrir les besoins sur le tableau de planification](media/FAQ-Project-Booking-Schedule-Board-1.png "Capture d’écran du tableau Réservations et attributions")

2. Sélectionnez le besoin. L’onglet **Rechercher la disponibilité** s’affiche en haut de la ligne sélectionnée.
 
3. Lorsque vous sélectionnez l’onglet, le mode Assistant Planifier du Tableau de planification s’ouvre et filtre les ressources disponibles qui répondent au besoin en ressources. Après cela, vous pouvez réserver une ressource.

4. Vous pouvez également faire glisser-déplacer la ligne sélectionnée du bas du Tableau de planification vers une cellule de la ressource dans la grille au-dessus. Lorsque vous le déplacez, cette action génère l’ouverture du volet **Créer une réservation de ressource** sur la droite.

    Sélectionner **Réserver** réserve la ressource dans l’équipe du projet.

![Volet Créer une réservation de ressource](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Réserver à partir du besoin principal

La création d’un projet dans Project Service crée automatiquement un besoin en ressource appelé le besoin principal. Il s’agit d’un besoin vide qui est utilisé pour réserver rapidement une ressource avec le Tableau de planification sans générer de besoin ni en créer un de zéro. Étant donné que le besoin est vide, vous devez spécifier des dates ainsi que la méthode et les heures d’attribution, le cas échéant. 

1. Pour réserver une ressource avec le besoin principal sur le Tableau de planification, sélectionnez l’onglet **Projet**. Vous pouvez avoir besoin d’utiliser le filtre de colonne sur la colonne **Projet** si vous avez plusieurs projets.

   ![Filtres de colonne sur le tableau de planification](media/FAQ-Project-Booking-Schedule-Board-2.png "Capture d’écran du tableau Réservations et attributions")

2. Sélectionnez le besoin qui a uniquement le nom du projet comme nom et une durée de zéro (0).

3. Sélectionnez l’onglet **Rechercher la disponibilité** qui apparaît sur la ligne. Cela met le Tableau de planification en mode Assistant Planifier et affiche les ressources disponibles qui peuvent être réservées sur le projet.

4. Comme un **Besoin principal** consiste en un besoin vide avec une durée de zéro (0), vous devez définir la durée sur le volet **Créer une réservation de ressource** lors de la sélection et de la réservation d’une ressource.

5. Vous pouvez également sélectionner le **Besoin principal du projet** au bas du Tableau de planification et le faire glisser-déplacer sur une ressource pour le réserver.
 
    Comme le **Besoin principal** consiste en un besoin vide avec une durée de zéro (0), vous devez définir la durée sur le volet **Créer une réservation de ressource** lorsque vous sélectionnez et réservez une ressource.
 
    Lorsque vous réservez une ressource via le **Besoin principal** sur le Tableau de planification, vous l’ajoutez à l’équipe du projet sans aucune attribution.
 
## <a name="book-from-a-new-resource-requirement"></a>Réserver à partir d’un nouveau besoin en ressource
Effectuez les étapes suivantes pour réserver un nouveau besoin en ressources. 

1. Accédez à **Besoins en ressources**, puis sélectionnez **Nouveau** pour créer un besoin en ressources.

2. Dans l’onglet **Projet**, sélectionnez un projet pour associer le besoin au projet.
 
    Sur le Tableau de planification, ce nouveau besoin s’affiche comme **Besoin ouvert** que vous pouvez remplir.

3. Réservez la ressource pour l’ajouter à l’équipe du projet.

4. Maintenant que la ressource est réservée, vous devez attribuer des tâches manuellement.

