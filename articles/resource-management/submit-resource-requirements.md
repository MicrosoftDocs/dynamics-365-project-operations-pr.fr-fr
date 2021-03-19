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
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279135"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="a1b17-104">Envoyer une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="a1b17-104">Submit a resource request</span></span>

<span data-ttu-id="a1b17-105">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="a1b17-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1b17-106">Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="a1b17-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a1b17-107">La demande est ensuite envoyée à un gestionnaire de ressources pour exécution.</span><span class="sxs-lookup"><span data-stu-id="a1b17-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a1b17-108">Dans Dynamics 365 Project Operations, sur la page **Projets**, sélectionnez l’onglet **Équipe** pour afficher une liste des ressources réservables.</span><span class="sxs-lookup"><span data-stu-id="a1b17-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="a1b17-109">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="a1b17-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="a1b17-110">Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="a1b17-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a1b17-111">Une fois la demande satisfaite, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources répond à la demande en réservant une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="a1b17-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="a1b17-112">Sinon, le gestionnaire de ressources propose une ressource nommée, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="a1b17-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]