---
title: Envoyer une demande de ressource
description: Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961702"
---
# <a name="submit-a-resource-request"></a>Envoyer une demande de ressource

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.

1. Dans Dynamics 365 Project Operations, dans la page **Projets**, sélectionnez l’onglet **Équipe** pour afficher une liste des ressources réservables. 
2. Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.

Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.

Une fois la demande traitée, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d’une ressource nommée. Sinon, le gestionnaire de ressources propose une ressource nommée, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**.
