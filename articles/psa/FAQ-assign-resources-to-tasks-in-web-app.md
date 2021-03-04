---
title: Comment attribuer une ressource pouvant être réservée à une tâche dans l’application web
description: Vue d’ensemble des méthodes d’attribution des ressources pouvant être réservées.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146570"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Comment attribuer une ressource réservable à une tâche dans l’application web (application Project Service v2.x) ?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Il existe deux méthodes pour attribuer une ressource à une tâche dans Project Service. Vous pouvez réserver une ressource en tant que membre d’équipe et l’attribuer à une tâche. Ou, vous pouvez créer un membre d’équipe générique via l’attribution de rôle sur les tâches, générer une équipe, puis satisfaire les conditions de sauvegarde avec une ressource nommée.

Notez que si vous souhaitez attribuer une ressource réservable à une tâche, le membre de l’équipe de la ressource réservable doit disposer de suffisamment de réservations disponibles. Le statut de la réservation doit être de type de validation Réservation ferme et Statut validé. S’il n’y a pas suffisamment de réservations pour la ressource, Project Service supprime l’attribution et affiche le message d’erreur suivant :

*Impossible d’attribuer la ressource à la tâche - les ressources suivantes ne disposent pas de suffisamment d’heures réservées par rapport au projet*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Réserver une ressource en tant que membre d’équipe et l’attribuer à une tâche

Avec cette méthode vous ajoutez une ressource à l’équipe du projet puis attribuez des tâches à la ressource dans la planification du projet. Voici la méthode pour le faire :
1.  Dans la grille de membre de l’équipe, ajoutez un nouveau membre de l’équipe en sélectionnant **Nouveau**.
2.  Dans l’écran Création rapide de membre d’équipe, sélectionnez le nom de la ressource réservable et définissez un rôle.
3.  Sélectionnez les dates **De** et **À**.

    > [!div class="mx-imgBorder"] 
    > ![Capture d’écran de l’ajout d’un membre de l’équipe](media/FAQ-Resources-to-Tasks2-1.png "Capture d’écran de l’ajout d’un membre de l’équipe")
 
4.  Sélectionnez une des méthodes d’attribution suivantes pour réserver la ressource :
    - **Capacité maximale** réserve la capacité totale de la ressource pour les dates de début et de fin spécifiées.
    - **Capacité du pourcentage** réserva la ressource pour un pourcentage de la capacité de la ressource aux dates de début et de fin spécifiées.
    - **Par heure - Distribuer de manière homogène** réserve la ressource pour un nombre spécifique d’heures, la distribuant de manière homogène par jour pendant la période spécifiée.
    - **Par heure - Chargement frontal** réserve la ressource pour un nombre spécifique d’heures, chargeant frontalement les heures par jour pendant la période spécifiée.

    Ne sélectionnez pas **Aucun** car cela ajoute la ressource à l’équipe mais ne crée aucune réservation qui absorbe la capacité de la ressource.
5.  Sélectionnez **Enregistrer**.

    Notez que les heures de la réservation doivent être suffisantes pour correspondre aux plages d’heures et de dates de travail auxquelles vous attribuez cette ressource. Si elles ne sont pas alignées, vous ne pouvez pas attribuer la ressource à la tâche.

6.  Dans la structure de répartition du travail (WBS) de la tâche, cliquez sur la liste déroulante des cellules de la ressource. Puis : 

    1. Sélectionnez **Ajouter**.
    2. Sélectionnez le liste déroulante sous **Ressources** et sélectionnez le membre de l’équipe ajouté ci-dessus.
    3. Sélectionnez **OK**. Le membre de l’équipe est maintenant attribué à la tâche.

    > [!div class="mx-imgBorder"] 
    > ![Capture d’écran de l’ajout de ressources avec WBS](media/FAQ-Resources-to-Tasks2-2.png "Capture d’écran de l’ajout de ressources avec WBS")
 
Dans la grille du membre de l’équipe, vous verrez l’agrégat des heures attribuées de la ressource sous Heures attribuées. Il est inférieur ou égal aux heures réservées pour la ressource. 

> [!div class="mx-imgBorder"] 
> ![Capture d’écran des heures attribuées pour une ressource](media/FAQ-Resources-to-Tasks2-3.png "Capture d’écran des heures attribuées pour une ressource")
 
Si la tâche que vous tentez d’attribuer à la ressource commence après la date de fin des réservations de ressources, la ressource n’apparaîtra pas dans la liste déroulante.

Notez que vous pouvez attribuer une ressource à plus d’heures que ses heures réservées si la ressource dispose d’une capacité non attribuée restante. Dans ce cas la ressource sera uniquement partiellement attribuée jusqu’à leurs réservations. Vous pouvez voir ces heures de tâche non attribuées restantes en ajoutant la colonne Heures non dotées à la structure de distribution de travail.

Si les ressources sont attribuées à leurs heures réservées (leurs heures réservées sont égales à leurs heures attribuées), le message d’erreur suivant s’affichera lorsque vous essayez de leur attribuer d’autres tâches :

*Impossible d’attribuer la ressource à la tâche - les ressources suivantes ne disposent pas de suffisamment d’heures réservées par rapport au projet.*

En outre, le membre de l’équipe du responsable de projet par défaut ajouté à l’équipe lors de la création du projet est ajouté sans aucune réservation et ne peut être attribué à aucune tâche. Il n’apparaît pas dans la liste déroulante de la ressource pour les tâches.

Si vous voulez attribuer cette ressource, vous devez le supprimer de l’équipe puis l’ajouter à nouveau avec une méthode d’attribution autre que Aucune. La raison pour laquelle il est ajouté à l’équipe lorsque le projet est créé est parce qu’un projet contient au moins un approbateur de projet par défaut.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Créer un membre de l’équipe générique via l’attribution de rôle sur les tâches

Cette méthode vous assurer que les ressources ont suffisamment de réservations pour les tâches. Tout d’abord, créez un espace réservé ou une ressource générique qui décrit les caractéristiques de la ressource nommée que vous souhaitez travailler sur des tâches en générant une équipe après avoir attribué des rôles à des tâches. Voici la méthode pour le faire :

1. Dans la structure de répartition du travail, sélectionnez une tâche.
2. Sélectionnez l’icône de menu déroulant **Rôle attribué** dans la cellule de ressource.
3. Sélectionnez le menu déroulant **Rôle** et sélectionnez le rôle pour la ressource générique.
4. Sélectionnez **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Capture d’écran de l’utilisation de WBS pour ajouter une ressource](media/FAQ-Resources-to-Tasks2-4.png "Capture d’écran de l’utilisation de WBS pour ajouter une ressource")
 
Une fois que vous avez terminé d’attribuer des rôles aux tâches dans la WBS, sélectionnez **Générer une équipe de projet**. Project Service crée le nombre minimal de membres d’équipe génériques selon les rôles, les unités d’organisation d’allocation des ressources, et le calendrier de projet en regroupant les attributions des tâches.

> [!div class="mx-imgBorder"] 
> ![Capture d’écran de la génération de l’équipe du projet](media/FAQ-Resources-to-Tasks2-5.png "Capture d’écran de la génération de l’équipe du projet")
 
Dans la grille du membre de l’équipe, vous verrez des ressources de type de ressource générique avec le nom de rôle et de poste. Si deux ressources sont nécessaires pour qu’un rôle termine le travail, la fonctionnalité Générer une équipe crée deux membres d’équipe et utilise les noms de poste pour les distinguer.

> [!div class="mx-imgBorder"] 
> ![Capture d’écran de l’ajout de deux ressources génériques](media/FAQ-Resources-to-Tasks2-6.png "Capture d’écran de l’ajout de deux ressources génériques")
 
Vous pouvez ouvrir le besoin en ressources de sauvegarde pour le membre de l’équipe générique en sélectionnant le lien sous Besoin en ressources.

> [!div class="mx-imgBorder"] 
> ![Capture d’écran de l’ouverture des ressources de sauvegarde requises](media/FAQ-Resources-to-Tasks2-7.png "Capture d’écran de l’ouverture des ressources de sauvegarde requises")

Sélectionnez **Réserver** pour la ressource générique, puis utilisez le tableau de planification pour rechercher et réserver une ressource réelle. Vous pouvez également envoyer le besoin pour exécution par un gestionnaire des ressources en sélectionnant **Envoyer la demande**.

Lorsque la ressource générique est exécutée avec une ressource nommée, la ressource générique est supprimée de l’équipe et les attributions de tâches pour la ressource générique sont attribuées à la ressource nommée qui a renseigné le besoin en ressources de la ressource générique.
 

