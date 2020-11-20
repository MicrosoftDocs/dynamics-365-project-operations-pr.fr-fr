---
title: Envoyer une demande de ressource
description: Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128820"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="a2c7d-104">Envoyer une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="a2c7d-104">Submit a resource request</span></span>

<span data-ttu-id="a2c7d-105">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="a2c7d-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a2c7d-106">Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a2c7d-107">La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a2c7d-108">Dans Dynamics 365 Project Operations, dans la page **Projets**, sélectionnez l’onglet **Équipe** pour afficher une liste des ressources réservables.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="a2c7d-109">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="a2c7d-110">Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a2c7d-111">Une fois la demande traitée, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d’une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="a2c7d-112">Sinon, le gestionnaire de ressources propose une ressource nommée, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="a2c7d-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
