---
title: Afficher l’utilisation facturable des ressources
description: Cette rubrique fournit des informations sur la vue d’utilisation des ressources.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122160"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="54879-103">Afficher l’utilisation facturable des ressources</span><span class="sxs-lookup"><span data-stu-id="54879-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="54879-104">La **Vue d’utilisation** sur la page **Utilisation des ressources Project Service** affiche l’utilisation imputable de chaque ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="54879-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="54879-105">Comme la vue est basée sur le tableau de planification, vous trouverez plusieurs fonctions identiques.</span><span class="sxs-lookup"><span data-stu-id="54879-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Capture d’écran de vue Utilisation](media/FAQ-utilization-1.png)
 

<span data-ttu-id="54879-107">Le calcul de l’utilisation facturable fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="54879-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="54879-108">Utilisation facturable = (Heures réelles facturables) / (Capacité ressource).</span><span class="sxs-lookup"><span data-stu-id="54879-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="54879-109">Les cellules représentent l’utilisation facturable calculée pour la période sélectionnée (jours, semaines ou mois).</span><span class="sxs-lookup"><span data-stu-id="54879-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="54879-110">Les couleurs de chaque cellule affichent l’utilisation facturable d’une ressource comparée à son utilisation facturable cible.</span><span class="sxs-lookup"><span data-stu-id="54879-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="54879-111">L’utilisation cible peut être définie sur le rôle par défaut de la ressource ou sur la ressource individuelle elle-même.</span><span class="sxs-lookup"><span data-stu-id="54879-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="54879-112">Le calcul prend en compte la ressource individuelle pour la première cible, puis le rôle par défaut de la ressource.</span><span class="sxs-lookup"><span data-stu-id="54879-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="54879-113">Définir la cible sur une ressource</span><span class="sxs-lookup"><span data-stu-id="54879-113">Set target on a resource</span></span>

1. <span data-ttu-id="54879-114">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="54879-115">Sélectionnez une ressource pour ouvrir l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="54879-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="54879-116">Dans l’onglet **Project Service**, vous pouvez définir l’utilisation cible de la ressource.</span><span class="sxs-lookup"><span data-stu-id="54879-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Capture d’écran de l’utilisation de l’onglet Project Service pour définir l’utilisation cible](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="54879-118">Définir l’utilisation cible sur un rôle</span><span class="sxs-lookup"><span data-stu-id="54879-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="54879-119">Accédez à **Ressources** \> **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="54879-120">Sélectionnez un rôle et ouvrez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="54879-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="54879-121">Définissez l’utilisation cible du rôle.</span><span class="sxs-lookup"><span data-stu-id="54879-121">Set the target utilization for the role.</span></span>

> ![Capture d’écran de l’utilisation de Rôles de la ressource pour définir l’utilisation cible](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="54879-123">Calculer l’utilisation facturable d’une ressource</span><span class="sxs-lookup"><span data-stu-id="54879-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="54879-124">Pour calculer l’utilisation facturable d’une ressource, vous devez satisfaire certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="54879-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="54879-125">Définir le rôle par défaut d’une ressource individuelle</span><span class="sxs-lookup"><span data-stu-id="54879-125">Set default role for individual resource</span></span>

<span data-ttu-id="54879-126">D’abord, l’utilisation cible doit être définie sur la ressource individuelle ou les rôles de la ressource.</span><span class="sxs-lookup"><span data-stu-id="54879-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="54879-127">Si vous utilisez des rôles de ressource pour les cibles, chaque ressource individuelle doit avoir un rôle par défaut.</span><span class="sxs-lookup"><span data-stu-id="54879-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="54879-128">Pour définir cela, accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="54879-129">Sélectionnez une ressource, ouvrez l’enregistrement, puis sélectionnez l’onglet **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="54879-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="54879-130">Dans la grille **Rôle de la ressource**, vérifiez qu’il existe un rôle pour la ressource et que **Est la valeur par défaut** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="54879-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="54879-131">Modifier le type de facturation pour le rôle de ressource</span><span class="sxs-lookup"><span data-stu-id="54879-131">Change billing type for resource role</span></span>

<span data-ttu-id="54879-132">Les rôles de la ressource doivent être définis pour avec un type facturation **Facturable**.</span><span class="sxs-lookup"><span data-stu-id="54879-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="54879-133">Accédez à **Ressources** \> **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="54879-134">Ouvrez l’enregistrement à mettre à jour, puis définissez la valeur par défaut du type de facturation sur **Facturable**.</span><span class="sxs-lookup"><span data-stu-id="54879-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="54879-135">Définir des heures de travail pour le rôle de la ressource</span><span class="sxs-lookup"><span data-stu-id="54879-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="54879-136">La ressource doit avoir des heures ouvrées pour le calcul de la capacité.</span><span class="sxs-lookup"><span data-stu-id="54879-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="54879-137">Accédez à **Ressources** \> **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="54879-138">Sélectionnez une ressource pour ouvrir l’enregistrement, puis **Afficher les heures de travail**.</span><span class="sxs-lookup"><span data-stu-id="54879-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="54879-139">Vous pouvez effectuer une mise à jour en bloc de la liste des ressources en appliquant un **Modèle d’heures de travail** de la vue **Liste des ressources**.</span><span class="sxs-lookup"><span data-stu-id="54879-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="54879-140">Dépannage des heures réelles facturables</span><span class="sxs-lookup"><span data-stu-id="54879-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="54879-141">Les heures réelles facturables sont extraites de l’entité **Chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="54879-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="54879-142">Les chiffres réels avec un type de facturation **Facturable** sont inclus dans le calcul et pour cette raison, vous devez disposer de projets où les chiffres réels sont facturables.</span><span class="sxs-lookup"><span data-stu-id="54879-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="54879-143">Si vous ne voyez pas d’utilisation facturable, voici ce que vous pouvez vérifier :</span><span class="sxs-lookup"><span data-stu-id="54879-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="54879-144">La ressource dispose d’heures de travail définies pour la capacité.</span><span class="sxs-lookup"><span data-stu-id="54879-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="54879-145">La ressource a une cible d’utilisation définie individuellement ou un rôle par défaut qui lui est attribué.</span><span class="sxs-lookup"><span data-stu-id="54879-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="54879-146">Le rôle a une cible d’utilisation qui lui est définie.</span><span class="sxs-lookup"><span data-stu-id="54879-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="54879-147">Les chiffres réels ont un type de facturation **Facturable** pour la période pour laquelle vous prévoyez le calcul de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="54879-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="54879-148">Vérificiez ce qui suit si vous voyez des chiffres réels avec des types de facturation autres que facturables :</span><span class="sxs-lookup"><span data-stu-id="54879-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="54879-149">Le rôle utilisé sur le chiffre réel possède un type de facturation par défaut autre que facturable.</span><span class="sxs-lookup"><span data-stu-id="54879-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="54879-150">Le rôle sur la ligne de contrat du projet soutenant le projet a été défini sur non facturable.</span><span class="sxs-lookup"><span data-stu-id="54879-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="54879-151">Le projet ne dispose pas de ligne de contrat associée.</span><span class="sxs-lookup"><span data-stu-id="54879-151">The project does not have an associated contract line.</span></span>

