---
title: Éliminer une estimation de projet
description: Cette rubrique fournit des informations sur l’élimination d’une estimation de projet une fois qu’elle est terminée.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006913"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="33df9-103">Éliminer une estimation de projet</span><span class="sxs-lookup"><span data-stu-id="33df9-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33df9-104">Les estimations du projet fournissent une vue financière de la tâche qui est prévue et planifiée pour un projet.</span><span class="sxs-lookup"><span data-stu-id="33df9-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="33df9-105">Pour travailler avec des devis pour un projet, vous devez attacher le projet à un projet d’estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="33df9-106">Un projet d’estimation est toujours basé sur un projet existant, cependant plusieurs projets peuvent faire référence à un seul projet d’estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="33df9-107">Seuls les projets à prix fixe et d’investissement peuvent être associés à des projets d’estimation, et ces projets doivent appartenir au même groupe de projets que le projet d’estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="33df9-108">Pour éliminer un projet d’estimation, il doit être complet.</span><span class="sxs-lookup"><span data-stu-id="33df9-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="33df9-109">Les étapes suivantes expliquent comment éliminer une estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="33df9-110">Accédez à **Gestion de projets et comptabilité** > **Tous les projets** et ouvrez le projet.</span><span class="sxs-lookup"><span data-stu-id="33df9-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="33df9-111">Dans l’onglet **Gérer**, sélectionnez **Estimations** et sur la page **Estimation**, sélectionnez **Éliminer**.</span><span class="sxs-lookup"><span data-stu-id="33df9-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="33df9-112">Sur la page **Éliminer l’estimation** de l’onglet **Général**, définissez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="33df9-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="33df9-113">**Code de période** : Sélectionnez le code de période pour choisir les projets d’estimation appropriés.</span><span class="sxs-lookup"><span data-stu-id="33df9-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="33df9-114">**Date estimée** : Sélectionnez la date d’estimation appropriée pour l’élimination.</span><span class="sxs-lookup"><span data-stu-id="33df9-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="33df9-115">**Éliminer avec les avertissements WIP** : Activez cette option pour fournir une notification lorsqu’une estimation associée à un travail en cours (WIP) sera éliminée.</span><span class="sxs-lookup"><span data-stu-id="33df9-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="33df9-116">Lorsque cette option n’est pas activée, l’élimination ne peut pas continuer s’il existe des transactions non estimées.</span><span class="sxs-lookup"><span data-stu-id="33df9-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="33df9-117">Cette option n’est disponible que lorsque l’élimination est appliquée à un projet d’estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="33df9-118">Il n’est pas disponible si vous utilisez des écritures périodiques.</span><span class="sxs-lookup"><span data-stu-id="33df9-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="33df9-119">Ce paramètre fonctionne avec les paramètres de l’onglet **Estimation** dans la page **Paramètres du projet**, dans le groupe de champs **Autoriser l’élimination lorsqu’il existe des transactions non estimées**.</span><span class="sxs-lookup"><span data-stu-id="33df9-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="33df9-120">**Définir l’étape sur Terminé** : Activez cette option pour définir l’étape du projet d’estimation sur **Terminé** après avoir exécuté l’élimination.</span><span class="sxs-lookup"><span data-stu-id="33df9-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="33df9-121">**Imprimer la liste des devis** : Sélectionnez les informations à inclure lors de l’impression de la liste d’estimations.</span><span class="sxs-lookup"><span data-stu-id="33df9-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="33df9-122">**Afficher l’infolog** : Activez cette option pour afficher l’infolog.</span><span class="sxs-lookup"><span data-stu-id="33df9-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="33df9-123">**Date de validation** : Choisissez la date de validation comptable de l’estimation.</span><span class="sxs-lookup"><span data-stu-id="33df9-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="33df9-124">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="33df9-124">Select **OK**.</span></span>
5. <span data-ttu-id="33df9-125">Une fois le processus d’élimination terminé, le projet d’estimation éliminé est affiché avec une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="33df9-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="33df9-126">Si vous n’aviez pas l’intention d’éliminer une estimation, vous pouvez sélectionner l’estimation éliminée, puis **Élimination inverse**.</span><span class="sxs-lookup"><span data-stu-id="33df9-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]