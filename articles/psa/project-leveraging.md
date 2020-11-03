---
title: Estimations des ventes et projets
description: Cette rubrique indique comment tirer parti de la planification et des estimations dans le processus de vente.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075758"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="2cab5-103">Estimations des ventes et projets</span><span class="sxs-lookup"><span data-stu-id="2cab5-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2cab5-104">Durant le processus de vente, vous pouvez créer des estimations de vente en liant un projet à un devis.</span><span class="sxs-lookup"><span data-stu-id="2cab5-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="2cab5-105">De cette façon, l'estimation déterministe peut se produire pendant le processus de vente, pour bénéficier des fonctionnalités de planification et d'estimation du projet.</span><span class="sxs-lookup"><span data-stu-id="2cab5-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="2cab5-106">Si la vente est réalisée, la planification utilisée pour l'estimation de ventes peut être utilisée comme base affiner davantage le plan du projet.</span><span class="sxs-lookup"><span data-stu-id="2cab5-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="2cab5-107">Lien d'un projet à une ligne de devis</span><span class="sxs-lookup"><span data-stu-id="2cab5-107">Linking a project to a quote line</span></span>

<span data-ttu-id="2cab5-108">Lorsque vous créez une ligne de devis basée sur un projet, vous pouvez créer un projet ou associer un projet existant sur la page **Ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="2cab5-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulaire Ligne de devis](media/project-8.png)
 
<span data-ttu-id="2cab5-110">Lorsque vous créez un projet à partir des détails de la ligne de devis, vous pouvez bénéficier des modèles de projets.</span><span class="sxs-lookup"><span data-stu-id="2cab5-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="2cab5-111">Les modèles de projet sont des projets modèles qui représentent des plans de projet standard et des estimations financières qui sont courantes dans une organisation.</span><span class="sxs-lookup"><span data-stu-id="2cab5-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="2cab5-112">Ils peuvent également représenter des copies de plans et d'estimations de projets pour des projets passés.</span><span class="sxs-lookup"><span data-stu-id="2cab5-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Détails de la ligne de devis](media/project-9.png)
  
<span data-ttu-id="2cab5-114">Lors de la création de votre projet depuis le devis, le projet est automatiquement associé à la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="2cab5-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="2cab5-115">Composants des estimations dans un projet</span><span class="sxs-lookup"><span data-stu-id="2cab5-115">Components of estimates in a project</span></span>

<span data-ttu-id="2cab5-116">Une planification vous permet de diviser le travail en tâches, de gérer une hiérarchie des tâches, de déterminer les ressources nécessaires pour effectuer une tâche, et d'attribuer une estimation de l'effort requis pour effectuer une tâche.</span><span class="sxs-lookup"><span data-stu-id="2cab5-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="2cab5-117">Vous pouvez définir des estimations des efforts et de la planification de travail à l'aide de champs sur l'onglet **Planification** de la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="2cab5-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="2cab5-118">Étant donné que les tarifs sont associées au projet, des estimations financières sont calculées en utilisant le coût et les prix de vente définis dans les tarifs.</span><span class="sxs-lookup"><span data-stu-id="2cab5-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="2cab5-119">Importation d'estimations depuis un projet dans un devis</span><span class="sxs-lookup"><span data-stu-id="2cab5-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="2cab5-120">Après avoir défini des estimations de projet, vous pouvez les importer dans la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="2cab5-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="2cab5-121">Dans la page **Détails de la ligne de devis** , sélectionnez **Importer à partir des estimations** sur le ruban pour synthétiser les estimations du projet selon le type de transaction, le rôle ou le niveau de tâche.</span><span class="sxs-lookup"><span data-stu-id="2cab5-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
