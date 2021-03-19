---
title: Attribuez des ressources génériques pouvant être réservées à une tâche et à une équipe de projet
description: Cette rubrique fournit des informations sur la réservation de ressources génériques dans les tâches et les équipes de projet.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291391"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Attribuez des ressources génériques pouvant être réservées à une tâche et générez des besoins en ressources 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Outre la réservation et l’attribution des ressources nommées ou réelles à votre projet, vous pouvez attribuer des ressources génériques aux tâches de projet. Ces ressources peuvent servir d’espaces réservés aux ressources nommées jusqu’à ce que vous soyez prêt à doter votre projet en personnel avec des ressources nommées. 

1. Dans Project Service Automation (PSA), ouvrez la page **Projet** et sur l’onglet **Planification**, entrez le nom de la position de la ressources générique dans la cellule **Ressource** de la planification. Sinon, cliquez sur l’icône **Ressource** dans la cellule pour ouvrir le sélecteur de ressources, puis entrez le nom de la ressource générique à créer.

![Création et affectation d’un membre de l’équipe générique](media/RM-how-to-9.png)

Cela ouvre le volet **Création rapide : Membre de l’équipe du projet**. 

2. Entrez le rôle et l’unité d’organisation du membre de l’équipe de ressources génériques, puis cliquez sur **Enregistrer**.

![Création rapide du membre de l’équipe générique](media/RM-how-to-10.png)

3. Après avoir créé le membre de l’équipe de ressources génériques, une tâche lui est attribuée. Vous pouvez continuer d’attribuer cette ressource générique à d’autres tâches dans la planification de tâche.

![Attribution d’un membre de l’équipe générique existant aux tâches](media/RM-how-to-11.png)

4. Après avoir attribué la ressource générique, vous pouvez générer un besoin en ressources et le satisfaire en réservant ou en transmettant directement une demande de ressource à un gestionnaire des ressources.

![Génération d’un besoin pour un membre de l’équipe générique](media/RM-how-to-12.png)

Dans la grille des membre de l’équipe, en plus de pouvoir utiliser le sélecteur de ressources comme mentionné précédemment, vous pouvez ajouter les ressources génériques directement. Les ressources sont ajoutées avec un besoin en ressources basé sur les dates de début/fin et la méthode d’allocation spécifiée dans le volet **Création rapide : Membre de l’équipe du projet**.

Vous pouvez voir une différence si vous ajoutez le membre de l’équipe générique directement, et que vous attribuez ensuite plus de tâches à la ressource générique qu’elle n’en dispose. Cliquez sur **Générer un besoin** pour régénérer le besoin afin d’équilibrer les heures requises par rapport aux attributions.

Vous pouvez également cliquer sur le lien **Besoin en ressources** de la grille de l’équipe pour ouvrir le besoin et ajouter des compétences, des ressources préférées, etc..

![Besoin en ressource](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]