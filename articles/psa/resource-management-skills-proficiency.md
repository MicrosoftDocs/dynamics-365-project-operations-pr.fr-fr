---
title: Modèles de qualifications et de compétences
description: Cette rubrique donne des informations sur l'utilisation des modèles de qualifications et de compétences.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075960"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="4a89c-103">Modèles de qualifications et de compétences</span><span class="sxs-lookup"><span data-stu-id="4a89c-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4a89c-104">Les compétences sont des caractéristiques de ressource partagées entre Dynamics 365 Project Service Automation et, le cas échéant Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="4a89c-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="4a89c-105">Pour maintenir le référentiel de compétences de Project Service Automation, accédez à **Ressources** \> **Qualifications de la ressource**.</span><span class="sxs-lookup"><span data-stu-id="4a89c-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Qualifications de la ressource](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="4a89c-107">Utilisez les modèles de compétences pour estimer des ressources</span><span class="sxs-lookup"><span data-stu-id="4a89c-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="4a89c-108">Les compétences des ressources sont estimées selon des modèles de compétences.</span><span class="sxs-lookup"><span data-stu-id="4a89c-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="4a89c-109">Les évaluations individuelles sont dans un modèle de compétences.</span><span class="sxs-lookup"><span data-stu-id="4a89c-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="4a89c-110">Pour créer un modèle de compétences, accédez à **Ressources** \> **Modèles de compétences** , puis sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="4a89c-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="4a89c-111">Dans le nouveau modèle d'évaluation, spécifiez la valeur d'évaluation minimale, la valeur d'évaluation maximale et l'entité qui est estimée.</span><span class="sxs-lookup"><span data-stu-id="4a89c-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="4a89c-112">Dans la sous-grille dans **Valeurs d'évaluation** , vous pouvez définir des valeurs d'évaluation différentes, du minimum au maximum.</span><span class="sxs-lookup"><span data-stu-id="4a89c-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Évaluations minimale et maximale définies](media/Resource-Management-image85.png)

<span data-ttu-id="4a89c-114">Ces valeurs d'évaluation sont affichées dans les filtres **Besoins en ressources** , **Tableau de planification** et **Assistant Planifier**.</span><span class="sxs-lookup"><span data-stu-id="4a89c-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>