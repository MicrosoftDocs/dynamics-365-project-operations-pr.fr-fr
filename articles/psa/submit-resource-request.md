---
title: Envoi d’une demande de ressource
description: Cet article donne des informations sur l’envoi d’une demande pour une ressource de projet.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c446dc0f99a5b9c9cdf3698cdf774cfd1e5d4d6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928843"
---
# <a name="submitting-a-resource-request"></a>Envoi d’une demande de ressource

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.

1. Dans Project Service Automation (PSA), dans la page **Projets**, cliquez sur l’onglet **Équipe** pour afficher la liste des ressources réservables. 
2. Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.

![Envoi d’une demande de ressource.](media/RM-how-to-18.png)

Le statut de la demande du membre d’équipe générique deviendra **Soumis**.

Une fois la demande traitée par le gestionnaire de ressources, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d’une ressource nommée. Sinon, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**, si le gestionnaire de ressources a proposé une ressource nommée.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
