---
title: Utiliser un champ existant dans Project Service comme dimension de tarification
description: Cette rubrique donne des informations sur l'utilisation de champs Project Service existants comme dimensions de tarification.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281565"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="e974e-103">Utiliser un champ existant dans Project Service comme dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="e974e-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e974e-104">Project Service Automation (PSA) a plusieurs champs dans l'entité **Chiffres réels** qui peuvent être utilisés comme dimensions de tarification pour la tarification basée sur des ressources dans les organisations de projet.</span><span class="sxs-lookup"><span data-stu-id="e974e-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="e974e-105">Par exemple, un champ courant est **Ressource réservable**.</span><span class="sxs-lookup"><span data-stu-id="e974e-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="e974e-106">Les petites entreprises qui ont moins de 20 à 30 ressources facturables peuvent estimer qu’il est plus simple d’avoir des taux de facturation et de coût spécifiques à chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="e974e-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="e974e-107">Toutefois, avec l'augmentation de la main d'œuvre facturable, des taux spécifiques peut devenir irréaliste à maintenir car les taux de coût et de facturation des ressources commencent à varier à mesure que les ressources sont promues, ont plus d'expérience ou acquièrent des compétences différentes.</span><span class="sxs-lookup"><span data-stu-id="e974e-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="e974e-108">Comme cette approche fonctionne toujours pour les entreprises d'une certaine taille, consultez [Utiliser une ressource réservable comme dimension de tarification](bookable-resource-pricing-dimension.md) pour comprendre comment un champ Project Service existant peut être utilisé comme dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="e974e-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="e974e-109">Un autre exemple est le champ Catégorie de transaction.</span><span class="sxs-lookup"><span data-stu-id="e974e-109">Another example is that of transaction category.</span></span> <span data-ttu-id="e974e-110">Les clients et les responsables de l'implémentation utilisent la catégorie de transaction dans PSA pour classer le travail et utilisent le champ pour évaluer le prix et le coût selon la catégorie de travail.</span><span class="sxs-lookup"><span data-stu-id="e974e-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="e974e-111">Pour plus d'informations, consultez [Utiliser une catégorie de transaction comme dimension de tarification](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="e974e-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]