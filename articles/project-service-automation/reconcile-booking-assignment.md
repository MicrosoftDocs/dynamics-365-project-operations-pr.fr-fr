---
title: Rapprochement des réservations et attributions
description: Cette rubrique fournit des informations sur les chiffres réels.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 614352ba-dbd8-4fa5-8225-d54f9ec0e218
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 27fc7b6abb4c9a7a761059a2f392f13bc0dd14f9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168134"
---
# <a name="reconcile-bookings-and-assignments"></a>Rapprochement des réservations et attributions

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les réservations de projet d'un membre de l'équipe du projet et les attributions de tâches du projet sont légèrement couplées. Par conséquent, une ressource peut contenir des affectations de tâches qui ne correspondent pas aux réservations et des réservations qui ne correspondent pas aux affectations des tâches. Idéalement, les réservations et attributions de projet sont alignées, de sorte que les ressources aient une capacité engagée à effectuer leurs affectations des tâches. Toutefois, la réalité est que des réservations peuvent se produire selon la disponibilité, et que les horaires des tâches peuvent changer à mesure que le projet poursuit son cycle de vie. Par conséquent, le couplage léger vous offre de la souplesse.

En raison du couplage léger des réservations de projet et des affectations des tâches, un onglet **Rapprochement** est inclus dans l'entité du projet. Cet onglet permet aux chefs de projet de rapprocher les réservations des membres de l'équipe et leurs affectations pour leur équipe de projet.

Pour chaque membre de l'équipe nommé, l'onglet **Rapprochement** affiche des réservations et attributions jusqu'à l'affectation de tâches individuelles. Il affiche les heures dans cellules pouvant représenter des périodes allant des mois jusqu'à des jours.

Dans le champ **Échelle de temps**, vous pouvez sélectionner **Mois**, **Semaine** ou **jour**. Par défaut, **Semaine** est sélectionné. Cependant, vous pouvez modifier la vue par défaut en sélectionnant le bouton **Paramètres**. Lorsque l'onglet **Rapprochement** est ouvert, il affiche la date du jour, mais vous pouvez utiliser le contrôle Calendrier pour avant ou reculer dans le temps. Lorsqu'un projet a une date de début qui est future, l'onglet affiche cette date quand il s'est ouvert. Le contrôle Calendrier possède également des options vous permettant de passer aux dates de début et de fin du projet.

Vous pouvez utiliser des contrôles de développeur sur chaque ressource pour afficher les détails des réservations de la ressource. Vous pouvez également développer les attributions de chaque ressource au niveau de la tâche individuelle.

Le partie inférieure de l'onglet **Rapprochement** affiche un total net général pour le projet, et l'onglet contient également une colonne totale. Pour chaque ressource, l'onglet identifie la distinction entre les réservations d'un membre de l'équipe sur un projet et un report des affectations de tâches de ce membre de l'équipe. Idéalement, la différence doit être de 0 (zéro). En d'autres termes, il ne doit exister aucune différence entre les réservations de la ressource et ses attributions de tâches. Toutes les différences sont désignées par couleurs et ombrage pour indiquer deux conditions :

- **Pénurie de réservation** – Des pénuries de réservation se produisent lorsque la ressource a plus d'affectations que de réservations. Cette capacité n'ayant pas été réservée, un chef de projet peut corriger cette condition en étendant les réservations de la ressource pour compenser le manque.
- **Réservations en trop** - Une réservation excessive se produit lorsque la ressource a été réservée pour le projet, mais n'a pas été affectée à des tâches. Cette condition peut être acceptable si, par exemple, la ressource a été réservée avant l'affectation des tâches. En revanche, dans d'autres cas, la ressource peut ne pas être planifiée pour être affectée. Dans ce genre de situation, le chef de projet doit envisager d'annuler les réservations de la ressource, de sorte que la capacité puisse être utilisée pour un autre projet.

> [!NOTE]
> La légende de ces conditions peut être masquée pour laisser plus de place pour la grille. Dans ce cas, vous pouvez rendre la légende visible en sélectionnant le bouton **Paramètres**.

Dans certains cas, lorsque le champ **Échelle de temps** est défini à niveau supérieur à **Jour**, des différences peuvent être calculées comme 0 (zéro). Par exemple, au niveau du **Mois**, la différence nette d'une ressource peut être de 0 (zéro) pour indiquer que les réservations sont égales aux attributions. Toutefois, si vous observez le temps au niveau de la **Semaine**, vous pouvez voir des attributions de 0 (zéro) heure et des réservations de 40 heures au cours de la première semaine du mois, et des attributions de 40 heures et des réservations de 0 (zéro) heure dans la deuxième semaine du mois. Bien que les totaux des réservations et des attributions du mois soient égaux, ils peuvent différer par semaine.

Lorsque vous affichez des niveaux de temps supérieurs, l'onglet **Rapprochement** affiche un indicateur de cellule pour vous informer qu'il existe des différences à des niveaux de temps inférieurs. Par exemple, dans l'illustration qui suit, un indicateur de cellule apparaît dans la cellule du mois d'octobre 2018 pour la ressource nommée Élise Flamand. Par conséquent, vous pouvez voir que, même si les réservations et les affectations de la ressource sont égales lorsqu'elles sont agrégées au niveau du **Mois**, elles ne correspondent pas aux niveaux inférieurs.

![Réservations et attributions différentes](media/reconcile-assignments-01.JPG)

Double-cliquez sur une cellule pour effectuer un zoom avant au niveau inférieur suivant et afficher la différence. Par exemple, si vous double-cliquez sur la différence d'octobre 2018 pour Élise Flamand, vous effectuez un zoom avant au niveau de la **Semaine**. Vous pouvez alors visualiser que la ressource a des réservations de 16 heures mais aucune attribution au cours des deux premières semaines d'octobre, et 16 heures d'attributions mais aucune réservation au cours de la semaine troisième d'octobre.

![Réservations et attributions différentes](media/reconcile-assignments-02.JPG)

Vous pouvez cliquer avec le bouton droit sur une cellule pour effectuer un zoom arrière au niveau supérieur suivant. Vous pouvez également désactiver l'indicateur de cellule en sélectionnant le bouton **Paramètres**. 

Vous pouvez également utiliser les boutons **Précédent** et **Suivant** au-dessus de la grille pour vous déplacer à travers les différences de votre projet. Pour utiliser ces boutons, vous devez d'abord sélectionner une ressource. Sélectionnez **Suivant** pour accéder à la prochaine différence entre les réservations et osent les affectations de cette ressource. Sélectionnez **Précédent** pour accéder à la différence précédente.

Dans les cas où vous avez des affectations de tâches pour une ressource mais aucune réservation, vous pouvez sélectionner la pénurie de réservation et cliquer sur **Étendre la réservation**. Vous pouvez alors visualiser la réservation nécessaire pour faire face à la pénurie de ressource. Vous pouvez également afficher les réservations de la ressource sur le projet en cours et d'autres projets. Sélectionnez **OK** pour créer la réservation pour la ressource se soucier de la disponibilité actuelle. Le chef de projet ou le gestionnaire de ressources peut ensuite utiliser le Tableau de planification pour gérer tous les cas où une ressource est devenue surréservée au-delà de sa capacité, car ses réservations ont été étendues.

## <a name="managing-with-time-zones"></a>Gestion avec les fuseaux horaires
Pour garantir des résultats précis et prévisibles lors de l'utilisation de la fonctionnalité Étendre la réservation, deux conditions préalables essentielles doivent être remplies :  

- L'utilisateur doit configurer le fuseau horaire de son appareil de manière à ce qu'il corresponde au fuseau horaire défini dans les paramètres de personnalisation de votre système.
 
  ![Paramètres de fuseau horaire dans Windows 10](media/reconcile-assignments-03.png)

  ![Paramètres de fuseau horaire dans les paramètres de personnalisation](media/reconcile-assignments-04.png)
 
- La ressource réservable doit avoir au moins une minute de temps de travail qui se chevauche avec les profils utilisés pour définir l'extension demandée. Par exemple, l'exemple suivant présente des ressources de révision dont les heures de travail se situent entre 9h00 et 19h00. 

  ![Comparaison de profils de ressource](media/reconcile-assignments-05.png)

Le tableau suivant présente :

- Un modèle de calendrier de projet.
- Ressource A : cette ressource a le même calendrier et se trouve dans le même fuseau horaire que le projet. L'heure de début des réservations sera 9h00.
- Ressource B : cette ressource se trouve dans un fuseau horaire différent du projet et commence donc à 7h00 dans son fuseau horaire. Cependant, les réservations commenceront à 9h00, car il s'agit de l'heure de début la plus proche du profil d'affectation.
- Ressources C et D : ces ressources se trouvent également dans des fuseaux horaires différents, à la fois différents l'un de l'autre et du projet, et leurs réservations commencent au plus tôt à leurs heures de début disponibles respectives.

|Entité  |Calendrier  |
|-|-|
|Modèle de calendrier de projet   | ![calendrier du projet](media/reconcile-assignments-06.png) |
|Ressource A  | ![Calendrier de la ressource A](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Calendrier de la ressource B](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Calendrier de la ressource C](media/reconcile-assignments-08.png) |
|Ressource D  | ![Calendrier de la ressource D](media/reconcile-assignments-09.png)  |
 
Lorsque vous accédez à la vue Rapprochement, les affectations de ressources et les pénuries de réservation associées s'affichent.
 ![Vue Rapprochement avant l'extension](media/reconcile-assignments-10.png)

Une fois que la fonctionnalité Étendre la réservation a été exécutée sur chaque ressource, les réservations sont correctement étendues pour chaque ressource. En effet, les heures de travail de chaque ressource se chevauchent avec les profls de la pénurie.
 ![Vue Rapprochement après l'extension de la réservation](media/reconcile-assignments-11.png) 

Cependant, un examen plus approfondi des détails des réservations montre des différences dans l'heure de début des réservations. Les réservations commenceront au plus tôt à l'heure de début du profil d'affectation et au plus tôt à l'heure de début disponible de la ressource.
 ![Nouvelles réservations des ressources dans le tableau de planification](media/reconcile-assignments-12.png)
