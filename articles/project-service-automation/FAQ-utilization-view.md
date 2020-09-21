---
title: Afficher l'utilisation facturable des ressources
description: Cette rubrique fournit des informations sur la vue d'utilisation des ressources.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167987"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="01dd9-103">Afficher l'utilisation facturable des ressources</span><span class="sxs-lookup"><span data-stu-id="01dd9-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="01dd9-104">La **Vue d'utilisation** sur la page **Utilisation des ressources Project Service** affiche l'utilisation imputable de chaque ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="01dd9-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="01dd9-105">Comme la vue est basée sur le tableau de planification, vous trouverez plusieurs fonctions identiques.</span><span class="sxs-lookup"><span data-stu-id="01dd9-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Capture d'écran de vue Utilisation](media/FAQ-utilization-1.png)
 

<span data-ttu-id="01dd9-107">Le calcul de l'utilisation facturable fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="01dd9-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="01dd9-108">Utilisation facturable = (Heures réelles facturables) / (Capacité ressource).</span><span class="sxs-lookup"><span data-stu-id="01dd9-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="01dd9-109">Les cellules représentent l'utilisation facturable calculée pour la période sélectionnée (jours, semaines ou mois).</span><span class="sxs-lookup"><span data-stu-id="01dd9-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="01dd9-110">Les couleurs de chaque cellule affichent l'utilisation facturable d'une ressource comparée à son utilisation facturable cible.</span><span class="sxs-lookup"><span data-stu-id="01dd9-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="01dd9-111">L'utilisation cible peut être définie sur le rôle par défaut de la ressource ou sur la ressource individuelle elle-même.</span><span class="sxs-lookup"><span data-stu-id="01dd9-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="01dd9-112">Le calcul prend en compte la ressource individuelle pour la première cible, puis le rôle par défaut de la ressource.</span><span class="sxs-lookup"><span data-stu-id="01dd9-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="01dd9-113">Définir la cible sur une ressource</span><span class="sxs-lookup"><span data-stu-id="01dd9-113">Set target on a resource</span></span>

1. <span data-ttu-id="01dd9-114">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="01dd9-115">Sélectionnez une ressource pour ouvrir l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="01dd9-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="01dd9-116">Dans l'onglet **Project Service**, vous pouvez définir l'utilisation cible de la ressource.</span><span class="sxs-lookup"><span data-stu-id="01dd9-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Capture d'écran de l'utilisation de l'onglet Project Service pour définir l'utilisation cible](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="01dd9-118">Définir l'utilisation cible sur un rôle</span><span class="sxs-lookup"><span data-stu-id="01dd9-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="01dd9-119">Accédez à **Ressources** \> **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="01dd9-120">Sélectionnez un rôle et ouvrez l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="01dd9-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="01dd9-121">Définissez l'utilisation cible du rôle.</span><span class="sxs-lookup"><span data-stu-id="01dd9-121">Set the target utilization for the role.</span></span>

> ![Capture d'écran de l'utilisation de Rôles de la ressource pour définir l'utilisation cible](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="01dd9-123">Calculer l'utilisation facturable d'une ressource</span><span class="sxs-lookup"><span data-stu-id="01dd9-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="01dd9-124">Pour calculer l'utilisation facturable d'une ressource, vous devez satisfaire certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="01dd9-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="01dd9-125">Définir le rôle par défaut d'une ressource individuelle</span><span class="sxs-lookup"><span data-stu-id="01dd9-125">Set default role for individual resource</span></span>

<span data-ttu-id="01dd9-126">D'abord, l'utilisation cible doit être définie sur la ressource individuelle ou les rôles de la ressource.</span><span class="sxs-lookup"><span data-stu-id="01dd9-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="01dd9-127">Si vous utilisez des rôles de ressource pour les cibles, chaque ressource individuelle doit avoir un rôle par défaut.</span><span class="sxs-lookup"><span data-stu-id="01dd9-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="01dd9-128">Pour définir cela, accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="01dd9-129">Sélectionnez une ressource, ouvrez l'enregistrement, puis sélectionnez l'onglet **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="01dd9-130">Dans la grille **Rôle de la ressource**, vérifiez qu'il existe un rôle pour la ressource et que **Est la valeur par défaut** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="01dd9-131">Modifier le type de facturation pour le rôle de ressource</span><span class="sxs-lookup"><span data-stu-id="01dd9-131">Change billing type for resource role</span></span>

<span data-ttu-id="01dd9-132">Les rôles de la ressource doivent être définis pour avec un type facturation **Facturable**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="01dd9-133">Accédez à **Ressources** \> **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="01dd9-134">Ouvrez l'enregistrement à mettre à jour, puis définissez la valeur par défaut du type de facturation sur **Facturable**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="01dd9-135">Définir des heures de travail pour le rôle de la ressource</span><span class="sxs-lookup"><span data-stu-id="01dd9-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="01dd9-136">La ressource doit avoir des heures ouvrées pour le calcul de la capacité.</span><span class="sxs-lookup"><span data-stu-id="01dd9-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="01dd9-137">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="01dd9-138">Sélectionnez une ressource pour ouvrir l'enregistrement, puis **Afficher les heures de travail**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="01dd9-139">Vous pouvez effectuer une mise à jour en bloc de la liste des ressources en appliquant un **Modèle d'heures de travail** de la vue **Liste des ressources**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="01dd9-140">Dépannage des heures réelles facturables</span><span class="sxs-lookup"><span data-stu-id="01dd9-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="01dd9-141">Les heures réelles facturables sont extraites de l'entité **Chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="01dd9-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="01dd9-142">Les chiffres réels avec un type de facturation **Facturable** sont inclus dans le calcul et pour cette raison, vous devez disposer de projets où les chiffres réels sont facturables.</span><span class="sxs-lookup"><span data-stu-id="01dd9-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="01dd9-143">Si vous ne voyez pas d'utilisation facturable, voici ce que vous pouvez vérifier :</span><span class="sxs-lookup"><span data-stu-id="01dd9-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="01dd9-144">La ressource dispose d'heures de travail définies pour la capacité.</span><span class="sxs-lookup"><span data-stu-id="01dd9-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="01dd9-145">La ressource a une cible d'utilisation définie individuellement ou un rôle par défaut qui lui est attribué.</span><span class="sxs-lookup"><span data-stu-id="01dd9-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="01dd9-146">Le rôle a une cible d'utilisation qui lui est définie.</span><span class="sxs-lookup"><span data-stu-id="01dd9-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="01dd9-147">Les chiffres réels ont un type de facturation **Facturable** pour la période pour laquelle vous prévoyez le calcul de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="01dd9-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="01dd9-148">Vérificiez ce qui suit si vous voyez des chiffres réels avec des types de facturation autres que facturables :</span><span class="sxs-lookup"><span data-stu-id="01dd9-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="01dd9-149">Le rôle utilisé sur le chiffre réel possède un type de facturation par défaut autre que facturable.</span><span class="sxs-lookup"><span data-stu-id="01dd9-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="01dd9-150">Le rôle sur la ligne de contrat du projet soutenant le projet a été défini sur non facturable.</span><span class="sxs-lookup"><span data-stu-id="01dd9-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="01dd9-151">Le projet ne dispose pas de ligne de contrat associée.</span><span class="sxs-lookup"><span data-stu-id="01dd9-151">The project does not have an associated contract line.</span></span>

