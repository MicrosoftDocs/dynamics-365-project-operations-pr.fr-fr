---
title: Créer des champs et des entités personnalisés comme dimensions de tarification
description: Cette rubrique fournit des informations sur la création de groupes d'options ou d'entités personnalisé(es).
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898258"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="59184-103">Créer des champs et des entités personnalisés comme dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="59184-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="59184-104">_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="59184-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="59184-105">Effectuez les étapes suivantes chaque fois que vous voulez créer un groupe d'options ou une entité personnalisé(e).</span><span class="sxs-lookup"><span data-stu-id="59184-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59184-106">Il est recommandé d'apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="59184-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="59184-107">Cette meilleure pratique importante procure la flexibilité nécessaire à l'avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance.</span><span class="sxs-lookup"><span data-stu-id="59184-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="59184-108">Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d'autres instances pour réutiliser votre configuration de tarification.</span><span class="sxs-lookup"><span data-stu-id="59184-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="59184-109">Créer une solution personnalisée pour les dimensions Tarification</span><span class="sxs-lookup"><span data-stu-id="59184-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="59184-110">Allez dans **Paramètres** > **Solutions**, puis cliquez sur **Nouveau** pour créer une solution.</span><span class="sxs-lookup"><span data-stu-id="59184-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="59184-111">Nommez la solution, **\<your organization name> dimensions tarification**, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59184-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="59184-112">Créer des champs et des jeux d'options personnalisés dans la solution de dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="59184-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="59184-113">Une dimension Tarification peut être un jeu d'options ou une entité.</span><span class="sxs-lookup"><span data-stu-id="59184-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="59184-114">Tous deux doivent être créés dans votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="59184-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="59184-115">Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="59184-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="59184-116">Dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="59184-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="59184-117">Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="59184-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="59184-118">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités**.</span><span class="sxs-lookup"><span data-stu-id="59184-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="59184-119">Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="59184-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="59184-120">Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59184-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="59184-121">Dimensions basées sur un jeu d'options</span><span class="sxs-lookup"><span data-stu-id="59184-121">Option set-based dimensions</span></span> 
<span data-ttu-id="59184-122">Vous pouvez créer deux dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="59184-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="59184-123">Utilisez **Emplacement de travail des ressources** pour suivre le prix du travail d'emplacement **Accueil** et du travail **Sur le site** et utilisez **Heures de travail des ressources** avec les valeurs **Régulier** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="59184-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="59184-124">Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="59184-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="59184-125">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Jeux d'options**.</span><span class="sxs-lookup"><span data-stu-id="59184-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="59184-126">Cliquez sur **Nouveau** pour créer un groupe d'options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59184-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="59184-127">Créer des données pour les dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="59184-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="59184-128">Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l'importation Microsoft Excel ou les appels de service.</span><span class="sxs-lookup"><span data-stu-id="59184-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="59184-129">Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="59184-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="59184-130">Si les données que vous voulez créer sont petites, comme dans l'exemple suivant, vous pouvez utiliser un formulaire standard.</span><span class="sxs-lookup"><span data-stu-id="59184-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="59184-131">Sélectionnez **Recherche avancée**, sélectionnez l'entité **Titre standard**, puis sélectionnez **Résultats**.</span><span class="sxs-lookup"><span data-stu-id="59184-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="59184-132">Toutes les lignes de l'entité **Titre standard** s'afficheront.</span><span class="sxs-lookup"><span data-stu-id="59184-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="59184-133">Sélectionnez **Nouveau**, dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59184-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="59184-134">Fermer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="59184-134">Close the form.</span></span> 
4. <span data-ttu-id="59184-135">Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».</span><span class="sxs-lookup"><span data-stu-id="59184-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="59184-136">Ajouter tous les entités requises et les composants associés à la solution Dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="59184-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="59184-137">Vous devrez ajouter les entités suivantes à votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="59184-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="59184-138">Utilisez la procédure ci-dessous pour apporter quelques modifications importantes au schéma dans la solution de tarification de sorte que les entités soient informées des nouvelles dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="59184-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="59184-139">Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="59184-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="59184-140">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.</span><span class="sxs-lookup"><span data-stu-id="59184-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="59184-141">Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="59184-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="59184-142">Chiffre réel</span><span class="sxs-lookup"><span data-stu-id="59184-142">Actual</span></span>
  - <span data-ttu-id="59184-143">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="59184-143">Bookable Resource</span></span>
  - <span data-ttu-id="59184-144">Ligne d'estimation</span><span class="sxs-lookup"><span data-stu-id="59184-144">Estimate Line</span></span>
  - <span data-ttu-id="59184-145">Détail de la ligne de facture</span><span class="sxs-lookup"><span data-stu-id="59184-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="59184-146">Ligne de journal</span><span class="sxs-lookup"><span data-stu-id="59184-146">Journal Line</span></span>
  - <span data-ttu-id="59184-147">Détail de la ligne de contrat du projet</span><span class="sxs-lookup"><span data-stu-id="59184-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="59184-148">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="59184-148">Project Team Member</span></span>
  - <span data-ttu-id="59184-149">Détail de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="59184-149">Quote Line Detail</span></span>
  - <span data-ttu-id="59184-150">Majoration du prix du rôle</span><span class="sxs-lookup"><span data-stu-id="59184-150">Role Price Markup</span></span>
  - <span data-ttu-id="59184-151">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="59184-151">Role Price</span></span> 
  - <span data-ttu-id="59184-152">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="59184-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="59184-153">Veillez à inclure tous les formulaires et vues pour chacune des entités sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="59184-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="59184-154">Lorsque vous êtes invité à inclure toutes les entités dépendantes des entités sélectionnées ci-dessus, cliquez sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="59184-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

