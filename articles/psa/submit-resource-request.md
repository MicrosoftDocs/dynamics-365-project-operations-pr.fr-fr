---
title: Envoi d'une demande de ressource
description: Cette rubrique donne des informations sur l'envoi d'une demande pour une ressource de projet.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075833"
---
# <a name="submitting-a-resource-request"></a>Envoi d'une demande de ressource

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.

1. Dans Project Service Automation (PSA), dans la page **Projets** , cliquez sur l'onglet **Équipe** pour afficher la liste des ressources réservables. 
2. Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.

![Envoi d'une demande de ressource](media/RM-how-to-18.png)

Le statut de la demande du membre de l'équipe générique passe à **Envoyé**.

Une fois la demande traitée par le gestionnaire de ressources, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d'une ressource nommée. Sinon, la ressource générique reste dans l'équipe et le statut de la demande passe à **Révision nécessaire** , si le gestionnaire de ressources a proposé une ressource nommée.
