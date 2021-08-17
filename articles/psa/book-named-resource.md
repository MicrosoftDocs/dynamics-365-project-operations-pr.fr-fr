---
title: Réserver des ressources nommées à partir des besoins en ressources.
description: Cette rubrique fournit des informations sur la réservation des ressources nommées pour un besoin en ressources générique.
author: JohnPBurrows
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
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000483"
---
# <a name="book-named-resources-from-resource-requirements"></a>Réserver des ressources nommées à partir des besoins en ressources.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vous pouvez réserver une ressource nommée pour remplacer une ressource génériques qui a un besoin en ressources.

1. Dans Project Service Automation (PSA), dans la page **Projets**, cliquez sur l’onglet **Équipe**.
2. Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Réserver**. Ou, ouvrez le besoin en ressources puis cliquez sur **Réserver**.


![Réservation d’un membre de l’équipe générique.](media/RM-how-to-14.png)


3. Dans la page **Assistant Planifier**, sélectionnez une ressource nommée à réserver sur votre équipe du projet, puis cliquez sur **Réserver**.

![Réservation d’un membre de l’équipe générique en utilisant l’Assistant Planifier.](media/RM-how-to-15.png)

Une fois la réservation effectuée et satisfaite par une ressource nommée, la ressource générique est remplacée par la ressource nommée.

![Membre de l’équipe nommé remplaçant un membre de l’équipe générique.](media/RM-how-to-16.png)

Les attributions sur la planification sont également mises à jour avec la ressource nommée.

![Membre de l’équipe nommé affecté aux tâches du projet.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Exécuter une ressource générique avec plusieurs ressources nommées
La satisfaction d’un besoin en ressource générique avec plusieurs ressources nommées est similaire à l’attribution d’une ressource nommée unique. Par exemple, il existe une tâche avec une durée de cinq jours et de 120 heures d’effort. Cette tâche ne peut pas être effectuée que par une ressource qui fonctionne un jour de huit heures classique sur une semaine de cinq jours. 

![Une tâche nécessite 120 heures d’effort sur cinq jours.](media/RM-how-to-21.png)

Le besoin est de 120 heures d’ingénierie robotique sur de cinq jours, soit 24 heures par jour.

![Besoin par jour.](media/RM-how-to-22.png)

Il s’agit d’un exemple où plusieurs ressources nommées sont nécessaires pour répondre à une demande de ressource générique. Vous devez réserver plusieurs ressources pour satisfaire le besoin.

![Réservation de plusieurs ressources pour satisfaire le besoin.](media/RM-how-to-23.png)

La principale différence dans ce scénario est que la ressource générique reste dans l’équipe attribuée à la tâche, et les membres de l’équipe de ressources nommés réservés ne sont pas attribués dans le cadre du poste. Le chef de projet peut affecter le travail si besoin aux ressources nommées. La vue **Rapprochement** peut aider un chef de projet à répartir les réservations entre plusieurs ressources à des affectations de tâche. Cela n’est pas effectué automatiquement, car dans les scénarios plus compliqués que l’exemple simple ci-dessus, comme celui où un groupe de tâches composent le besoin, la façon dont le chef de projet souhaite les affecter, doit être prise en compte par le système. Comme le système ne peut pas comprendre l’intention, il y a des chances que les hypothèses soient différentes de celles prévues et un résultat incorrect ou imprévisible se produise. Le résultat prévisible est que la ressource générique reste affectée jusqu’à ce que le chef de projet crée délibérément des attributions à l’aide de la vue **Rapprochement**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]