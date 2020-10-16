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
# <a name="submit-a-resource-request"></a><span data-ttu-id="22498-104">Envoyer une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="22498-104">Submit a resource request</span></span>

<span data-ttu-id="22498-105">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="22498-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="22498-106">Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="22498-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="22498-107">La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.</span><span class="sxs-lookup"><span data-stu-id="22498-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="22498-108">Dans Dynamics 365 Project Operations, dans la page **Projets**, sélectionnez l’onglet **Équipe** pour afficher une liste des ressources réservables.</span><span class="sxs-lookup"><span data-stu-id="22498-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="22498-109">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="22498-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="22498-110">Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="22498-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="22498-111">Une fois la demande traitée, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d’une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="22498-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="22498-112">Sinon, le gestionnaire de ressources propose une ressource nommée, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="22498-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
