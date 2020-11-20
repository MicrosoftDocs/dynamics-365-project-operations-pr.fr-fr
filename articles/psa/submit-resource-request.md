---
title: Envoi d’une demande de ressource
description: Cette rubrique donne des informations sur l’envoi d’une demande pour une ressource de projet.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131261"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="95456-103">Envoi d’une demande de ressource</span><span class="sxs-lookup"><span data-stu-id="95456-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="95456-104">Vous pouvez envoyer un besoin en ressources généré en tant que demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="95456-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="95456-105">La demande est ensuite envoyée à un gestionnaire de ressources pour traitement.</span><span class="sxs-lookup"><span data-stu-id="95456-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="95456-106">Dans Project Service Automation (PSA), dans la page **Projets**, cliquez sur l’onglet **Équipe** pour afficher la liste des ressources réservables.</span><span class="sxs-lookup"><span data-stu-id="95456-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="95456-107">Sélectionnez la ressource générique qui a un besoin en ressources dans la liste, puis cliquez sur **Envoyer la demande**.</span><span class="sxs-lookup"><span data-stu-id="95456-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Envoi d’une demande de ressource](media/RM-how-to-18.png)

<span data-ttu-id="95456-109">Le statut de la demande du membre de l’équipe générique passe à **Envoyé**.</span><span class="sxs-lookup"><span data-stu-id="95456-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="95456-110">Une fois la demande traitée par le gestionnaire de ressources, la ressource générique est remplacée par une ressource nommée si le gestionnaire de ressources traite la demande avec la réservation d’une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="95456-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="95456-111">Sinon, la ressource générique reste dans l’équipe et le statut de la demande passe à **Révision nécessaire**, si le gestionnaire de ressources a proposé une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="95456-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
