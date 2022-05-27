---
title: Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches
description: Cette rubrique fournit des informations sur le mode de réservation de ressources nommées dans les équipes de projet et leur attribution de tâches.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575347"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Réservation de ressources pouvant être réservées nommées à une équipe de projet et lui attribuer des tâches 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vous pouvez ajouter une ressource nommée à votre équipe de projet en les réservant directement dans l’équipe. Pour cela, procédez comme suit :

1. Dans Project Service Automation, accédez à **Projets**, puis sélectionnez pour ouvrir le projet que réservez.
2. Dans la page **Projet**, dans l’onglet **Équipe**, cliquez sur **Nouveau**. 

![Ajout d’un membre de l’équipe à partir de l’onglet Équipe.](media/RM-how-to-1.png)

3. Dans la boîte de dialogue **Création rapide : Membre de l’équipe de projet**, sélectionnez la ressource réservable. Le champ **Rôle** se remplit avec le rôle par défaut de la ressource si elle en a un d’attribué. Vous pouvez modifier le rôle si nécessaire. 
4. Sélectionnez les dates de début et de fin auxquelles la ressource sera nécessaire et sélectionnez la méthode d’allocation de la capacité de la ressource. 
5. Si vous voulez que le membre de l’équipe soit un approbateur de projet, sélectionnez **Oui** dans le champ **Approbateur du projet**. Cela signifiera que le membre de l’équipe peut approuver les entrées de temps et de dépenses envoyées pour ce projet. 
6. Cliquez sur **Enregistrer**.

![Ajout d′un membre de l′équipe au formulaire de création rapide.](media/RM-how-to-2.png)


Vous pouvez désormais attribuer la ressource réservée aux tâches sur le projet. Dans la page **Projet**, cliquez sur l’onglet **Planification** pour attribuer des tâches à la nouvelle ressource. Le sélecteur de ressources lancé à partir du champ **Ressources** dans la grille de tâches affichera les membres de l’équipe que vous pouvez sélectionner.

![Attribution d’un membre de l’équipe à une tâche sur l’onglet Planification.](media/RM-how-to-3.png)

Dans la version 3 de Project Service Automation (PSA), les réservations de ressources et les attributions de tâches ne sont pas couplées étroitement. Cela signifie que si vous utilisez le sélecteur de ressources dans la planification, vous pouvez attribuer des tâches aux membres de l’équipe pour plus d’heures que leurs réservation n’en couvre.
Vous pouvez voir les différences entre les réservations et les attributions de membres de l’équipe sur l’onglet **Équipe** ou sur l’onglet **Rapprochement des ressources**. Vous pouvez également rapprocher les différences entre les réservations et les attributions pour les ressources à un niveau plus détaillé.

![Onglet Rapprochement des ressources.](media/RM-how-to-4.png)

Vous pouvez également utiliser le sélecteur de ressources sur l’onglet **Planification** pour rechercher et sélectionner les ressources réservables qui ne font pas déjà partie de l’équipe du projet. Celles-ci sont affichées dans le sélecteur de ressources comme **Autres ressources**.

![Attribution d’une ressource non membre de l’équipe à une tâche.](media/RM-how-to-5.png)

Une fois cette opération effectuée, la ressource est ajoutée à l’équipe du projet et attribuée à la tâche, mais aucune réservation n’est générée.

![Membre de l’équipe avec des attributions mais aucune réservation.](media/RM-how-to-6.png)

Vous pouvez utiliser la capacité d’extension de réservation de l’onglet **Rapprochement** ou le **Tableau de planification** pour réserver la capacité de la ressource sur le projet.

![Extension des réservations d’un membre de l’équipe sous l’onglet Rapprochement des ressources.](media/RM-how-to-7.png)

Lorsqu’un membre de l’équipe est réservé sur votre projet, vous pouvez gérer les réservations ou utiliser le tableau de planification directement pour gérer ses réservations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
