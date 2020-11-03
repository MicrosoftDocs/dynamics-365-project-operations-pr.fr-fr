---
title: Définir les qualifications et les compétences
description: Cette rubrique donne des informations sur la définition de modèles de qualifications et de compétences pour évaluer des ressources.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075684"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="f1c02-103">Définir les qualifications et les compétences</span><span class="sxs-lookup"><span data-stu-id="f1c02-103">Define skills and proficiencies</span></span>

<span data-ttu-id="f1c02-104">_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f1c02-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1c02-105">Les compétences sont des caractéristiques de ressource partagées entre Dynamics 365 Project Operations et, le cas échéant Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="f1c02-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="f1c02-106">Pour maintenir le référentiel de compétences de Project Operations, accédez à **Ressources** \> **Qualifications de la ressource**.</span><span class="sxs-lookup"><span data-stu-id="f1c02-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f1c02-107">Utilisez les modèles de compétences pour estimer des ressources</span><span class="sxs-lookup"><span data-stu-id="f1c02-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f1c02-108">Les compétences des ressources sont estimées selon des modèles de compétences.</span><span class="sxs-lookup"><span data-stu-id="f1c02-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f1c02-109">Les évaluations individuelles sont dans un modèle de compétences.</span><span class="sxs-lookup"><span data-stu-id="f1c02-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f1c02-110">Pour créer un modèle de compétences, accédez à **Ressources** \> **Modèles de compétences** , puis sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f1c02-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="f1c02-111">Dans le nouveau modèle d'évaluation, spécifiez la valeur d'évaluation minimale, la valeur d'évaluation maximale et l'entité qui est estimée.</span><span class="sxs-lookup"><span data-stu-id="f1c02-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f1c02-112">Dans la sous-grille dans **Valeurs d'évaluation** , vous pouvez définir des valeurs d'évaluation différentes, du minimum au maximum.</span><span class="sxs-lookup"><span data-stu-id="f1c02-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="f1c02-113">Ces valeurs d'évaluation sont affichées dans les filtres **Besoins en ressources** , **Tableau de planification** et **Assistant Planifier**.</span><span class="sxs-lookup"><span data-stu-id="f1c02-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
