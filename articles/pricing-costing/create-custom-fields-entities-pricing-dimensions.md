---
title: Créer des champs et des entités personnalisés comme dimensions de tarification
description: Cette rubrique fournit des informations sur la création de groupes d’options ou d’entités personnalisé(es).
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642810"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="f2b31-103">Créer des champs et des entités personnalisés comme dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="f2b31-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="f2b31-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f2b31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2b31-105">Effectuez les étapes suivantes lorsque vous voulez créer un jeu d'options ou une entité personnalisés à utiliser comme dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="f2b31-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="f2b31-106">Pour plus d’informations, voir [Vue d’ensemble des dimensions de tarification](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2b31-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f2b31-107">Il est recommandé d’apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="f2b31-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="f2b31-108">Cette bonne pratique importante offre une flexibilité à l'avenir pour mettre à jour ou supprimer les modifications selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="f2b31-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="f2b31-109">Cela vous aidera également à réutiliser votre travail et facilitera le portage de ces modifications vers une autre instance. Après avoir effectué toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d'autres instances pour réutiliser votre configuration de tarification.</span><span class="sxs-lookup"><span data-stu-id="f2b31-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="f2b31-110">Créer des champs et des jeux d'options personnalisés dans la solution de dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="f2b31-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="f2b31-111">Une dimension Tarification peut être un jeu d’options ou une entité.</span><span class="sxs-lookup"><span data-stu-id="f2b31-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="f2b31-112">Tous deux doivent être créés dans votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="f2b31-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="f2b31-113">Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d’options.</span><span class="sxs-lookup"><span data-stu-id="f2b31-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="f2b31-114">Dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="f2b31-114">Entity-based dimensions</span></span>
<span data-ttu-id="f2b31-115">Pour créer des dimensions basées sur une entité, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f2b31-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="f2b31-116">Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="f2b31-117">Dans l’Explorateur de solutions, dans le volet de navigation de gauche, sélectionnez **Entités**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="f2b31-118">Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="f2b31-119">Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Définition de l'entité Titre standard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="f2b31-121">Dimensions basées sur un jeu d’options</span><span class="sxs-lookup"><span data-stu-id="f2b31-121">Option set-based dimensions</span></span> 
<span data-ttu-id="f2b31-122">Vous pouvez créer deux dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="f2b31-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="f2b31-123">Utilisez **Emplacement de travail des ressources** pour suivre le prix de l'emplacement de travail **Accueil** et le travail **Sur site**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="f2b31-124">Utilisez **Heures de travail des ressources** avec les valeurs **Régulières** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="f2b31-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="f2b31-125">Le graphique suivant fournit une vue de la dimension **Emplacement de travail des ressources**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimension Tarification basée sur un jeu d'options appelé Emplacement de travail de la ressource](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="f2b31-127">Le graphique suivant fournit une vue de la dimension **Heures de travail des ressources**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimension Tarification basée sur un jeu d'options appelé Heures de travail de la ressource](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="f2b31-129">Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f2b31-130">Dans l’Explorateur de solutions, dans le volet de navigation de gauche, sélectionnez **Jeux d’options**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="f2b31-131">Cliquez sur **Nouveau** pour créer un groupe d’options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="f2b31-132">Créer des données pour les dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="f2b31-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="f2b31-133">Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l’importation Microsoft Excel ou les appels de service.</span><span class="sxs-lookup"><span data-stu-id="f2b31-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="f2b31-134">Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="f2b31-135">Si les données que vous voulez créer sont petites, comme dans l’exemple suivant, vous pouvez utiliser un formulaire standard.</span><span class="sxs-lookup"><span data-stu-id="f2b31-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="f2b31-136">Sélectionnez **Recherche avancée**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="f2b31-137">Sélectionnez l’entité **Titre standard**, puis cliquez sur **Résultats**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="f2b31-138">Toutes les lignes de l’entité **Titre standard** s’afficheront.</span><span class="sxs-lookup"><span data-stu-id="f2b31-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="f2b31-139">Sélectionnez **Nouveau**, dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f2b31-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="f2b31-140">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="f2b31-140">Close the page.</span></span> 
5. <span data-ttu-id="f2b31-141">Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».</span><span class="sxs-lookup"><span data-stu-id="f2b31-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Exemple de données pour l'entité Titre standard](media/ST-data.png)
