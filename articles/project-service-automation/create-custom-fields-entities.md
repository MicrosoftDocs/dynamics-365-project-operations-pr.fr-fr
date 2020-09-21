---
title: Créer des champs et des entités personnalisés
description: Cette rubrique explique comment créer des jeux d'options et des entités dans votre propre solution dans la plateforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168118"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="ccf9a-103">Créer des champs et des entités personnalisés</span><span class="sxs-lookup"><span data-stu-id="ccf9a-103">Create custom fields and entities</span></span> 

<span data-ttu-id="ccf9a-104">Effectuez les étapes suivantes chaque fois que vous voulez créer un jeu d'options ou une entité personnalisés sur la plateforme Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="ccf9a-105">Les procédures dans cette rubrique doivent être effectuées à l'aide de l'interface web Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="ccf9a-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccf9a-106">Il est recommandé d'apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="ccf9a-107">Cette meilleure pratique importante procure la flexibilité nécessaire à l'avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ccf9a-108">Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d'autres instances pour réutiliser votre configuration de tarification.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="ccf9a-109">Créer une solution personnalisée pour les dimensions Tarification</span><span class="sxs-lookup"><span data-stu-id="ccf9a-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="ccf9a-110">Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis cliquez sur **Nouveau** pour créer une solution.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="ccf9a-111">Nommez la solution, **\<nom de votre organisation> dimensions tarification**, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Création d'une solution personnalisée pour les dimensions Tarification](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="ccf9a-113">Créer des champs et des jeux d'options personnalisés dans la solution de dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="ccf9a-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="ccf9a-114">Une dimension Tarification peut être un jeu d'options ou une entité.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="ccf9a-115">Tous deux doivent être créés dans votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="ccf9a-116">Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="ccf9a-117">Dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="ccf9a-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="ccf9a-118">Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis double-cliquez sur **\<nom de votre organisation> dimensions Tarification**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="ccf9a-119">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="ccf9a-120">Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="ccf9a-121">Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Définition de l'entité Titre standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="ccf9a-123">Dimensions basées sur un jeu d'options</span><span class="sxs-lookup"><span data-stu-id="ccf9a-123">Option set-based dimensions</span></span> 
<span data-ttu-id="ccf9a-124">Vous pouvez créer deux dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="ccf9a-125">Utilisez **Emplacement de travail des ressources** pour suivre le prix du travail d'emplacement **Accueil** et du travail **Sur le site** et utilisez **Heures de travail des ressources** avec les valeurs **Régulier** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="ccf9a-126">Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis double-cliquez sur **\<nom de votre organisation> dimensions Tarification**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ccf9a-127">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Jeux d'options**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="ccf9a-128">Cliquez sur **Nouveau** pour créer un jeu d'options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="ccf9a-129">Dimension Tarification basée sur un jeu d'options appelé Emplacement de travail de la ressource</span><span class="sxs-lookup"><span data-stu-id="ccf9a-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="ccf9a-130">Dimension Tarification basée sur un jeu d'options appelé Heures de travail de la ressource</span><span class="sxs-lookup"><span data-stu-id="ccf9a-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="ccf9a-131">Créer des données pour les dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="ccf9a-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="ccf9a-132">Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l'importation Microsoft Excel ou les appels de service.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="ccf9a-133">Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="ccf9a-134">Si les données que vous voulez créer sont petites, comme dans l'exemple suivant, vous pouvez utiliser un formulaire standard.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="ccf9a-135">Dans PSA, cliquez sur **Recherche avancée**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="ccf9a-136">Sélectionnez l’entité **Titre standard**, puis cliquez sur **Résultats**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="ccf9a-137">Toutes les lignes de l'entité **Titre standard** s'afficheront.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="ccf9a-138">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-138">Click **New**.</span></span> <span data-ttu-id="ccf9a-139">Dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="ccf9a-140">Fermez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-140">Close the form.</span></span> 
4. <span data-ttu-id="ccf9a-141">Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».</span><span class="sxs-lookup"><span data-stu-id="ccf9a-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="ccf9a-142">Exemple de données pour l'entité Titre standard</span><span class="sxs-lookup"><span data-stu-id="ccf9a-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ccf9a-143">Ajouter tous les entités PSA requises et composants associés à la solution Dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="ccf9a-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="ccf9a-144">Vous devrez ajouter les entités Project Service suivantes à votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="ccf9a-145">Utilisez la procédure ci-dessous pour apporter quelques modifications importantes au schéma dans la solution de tarification de sorte que les entités soient informées des nouvelles dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="ccf9a-146">Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis double-cliquez sur **\<nom de votre organisation> dimensions Tarification**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ccf9a-147">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="ccf9a-148">Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccf9a-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="ccf9a-149">Chiffre réel</span><span class="sxs-lookup"><span data-stu-id="ccf9a-149">Actual</span></span>
- <span data-ttu-id="ccf9a-150">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="ccf9a-150">Bookable Resource</span></span>
- <span data-ttu-id="ccf9a-151">Ligne d'estimation</span><span class="sxs-lookup"><span data-stu-id="ccf9a-151">Estimate Line</span></span>
- <span data-ttu-id="ccf9a-152">Détail de la ligne de facture</span><span class="sxs-lookup"><span data-stu-id="ccf9a-152">Invoice Line Detail</span></span>
- <span data-ttu-id="ccf9a-153">Ligne de journal</span><span class="sxs-lookup"><span data-stu-id="ccf9a-153">Journal Line</span></span>
- <span data-ttu-id="ccf9a-154">Détail de la ligne de contrat du projet</span><span class="sxs-lookup"><span data-stu-id="ccf9a-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="ccf9a-155">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="ccf9a-155">Project Team Member</span></span>
- <span data-ttu-id="ccf9a-156">Détail de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="ccf9a-156">Quote Line Detail</span></span>
- <span data-ttu-id="ccf9a-157">Majoration du prix du rôle</span><span class="sxs-lookup"><span data-stu-id="ccf9a-157">Role Price Markup</span></span>
- <span data-ttu-id="ccf9a-158">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="ccf9a-158">Role Price</span></span> 
- <span data-ttu-id="ccf9a-159">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="ccf9a-159">Time Entry</span></span> 

> ![Ajouter des entités existantes à la solution Dimensions de tarification](media/Existing-entities-to-PD-solution.png)

> ![Sélectionner les composants de solution](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="ccf9a-162">Veillez à inclure tous les formulaires et vues pour chacune des entités sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="ccf9a-163">Lorsque vous êtes invité à inclure toutes les entités dépendantes des entités sélectionnées ci-dessus, cliquez sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="ccf9a-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ne pas inclure tous les composants associés](media/Do-not-include-required.png)


