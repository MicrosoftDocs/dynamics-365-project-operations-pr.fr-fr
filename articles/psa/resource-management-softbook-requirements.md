---
title: Besoins en réservations temporaires
description: Cet article fournit des informations sur la façon de réserver provisoirement des besoins.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 8192047639823bc594803d6d10759be28f6db3ed
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928935"
---
# <a name="soft-book-requirements"></a>Besoins en réservations temporaires

[!include [banner](../includes/psa-now-project-operations.md)]

Un besoin en ressources peut être réservé de manière ferme. Une réservation ferme crée une proposition qui consomme la capacité d’une ressource. La proposition est alors renvoyée au demandeur l’approbation. Une réservation provisoire ajoute temporairement une ressource à une équipe du projet et a un statut différent sur le Tableau de planification, mais elle ne consomme pas la capacité de la ressource. Pour réserver provisoirement une ressource à partir du Tableau de planification, définissez le champ **Statut de la réservation** sur **Temporaire**.

![Statut de la réservation défini sur Temporaire.](media/Resource-Management-image77.png)

Lorsque l’onglet **Équipe** se trouve dans la vue **Membres de l’équipe nommés**, la ressource apparaît dans celle-ci. Les heures réservées temporairement sont stockées dans la colonne **Heures réservées temporairement**.

![Heures réservées temporairement dans la vue Membres de l’équipe nommés.](media/Resource-Management-image78.png)

Les membres de l’équipe réservés temporairement peuvent être attribués à des tâches.

![Membre de l’équipe réservé temporairement attribué à une tâche.](media/Resource-Management-image79.png)

Dans l’onglet **Rapprochement**, aucune réservation n’est affichée pour une ressource réservée temporairement, car l’onglet **Rapprochement** considère uniquement les réservations fermes.

![Ressource réservée temporairement sans réservation sous l’onglet Rapprochement.](media/Resource-Management-image80.png)

> [!NOTE]
> Vous ne pouvez pas réserver temporairement une ressource d’un besoin généré par un membre de l’équipe générique.

Dans le Tableau de planification, des couleurs différentes sont utilisées pour les réservations temporaires d’une ressource.

![Réservations temporaires dans le Tableau de planification.](media/Resource-Management-image81.png)

Pour convertir une réservation temporaire en une réservation ferme, dans le Tableau de planification, cliquez avec le bouton droit sur la réservation temporaire, puis sélectionnez **Modifier le statut** \> **Réservation ferme** \> **Ferme**.

![Modification du statut de la réservation sur Ferme.](media/Resource-Management-image82.png)

La réservation est modifiée, et le statut change sur le Tableau de planification. Étant donné que le statut de réservation est désormais **Ferme**, la ressource apparaît comme réservée, et sa capacité et sa disponibilité sont ajustées.

Vous pouvez utiliser la même méthode pour annuler une réservation ferme ou une réservation temporaire sur le Tableau de planification.

Pour convertir une ressource réservée temporairement en réservation ferme, sur l’onglet **Équipe** du projet, sélectionnez la ressource, puis sélectionnez **Confirmer**.

![Commande Confirmer.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
