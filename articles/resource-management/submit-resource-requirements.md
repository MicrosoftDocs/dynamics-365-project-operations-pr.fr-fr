---
title: Envoyer une demande de ressource
description: Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource. La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014023"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="91569-104">Envoyer une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="91569-104">Submit a resource request</span></span>

<span data-ttu-id="91569-105">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="91569-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91569-106">Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="91569-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="91569-107">La demande est ensuite envoyée à un gestionnaire de ressources pour exécution.</span><span class="sxs-lookup"><span data-stu-id="91569-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="91569-108">Dans Dynamics 365 Project Operations, sur la page **Projets**, sélectionnez l’onglet **Équipe** pour afficher une liste des ressources réservables.</span><span class="sxs-lookup"><span data-stu-id="91569-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="91569-109">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="91569-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="91569-110">Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="91569-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="91569-111">Une fois la demande satisfaite, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources répond à la demande en réservant une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="91569-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="91569-112">Sinon, le gestionnaire de ressources propose une ressource nommée, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="91569-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]