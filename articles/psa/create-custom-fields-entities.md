---
title: Créer des champs et des entités personnalisés
description: Cette rubrique explique comment créer des jeux d'options et des entités dans votre propre solution dans la plateforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075809"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="8c95c-103">Créer des champs et des entités personnalisés</span><span class="sxs-lookup"><span data-stu-id="8c95c-103">Create custom fields and entities</span></span> 

<span data-ttu-id="8c95c-104">Effectuez les étapes suivantes chaque fois que vous voulez créer un jeu d'options ou une entité personnalisés sur la plateforme Power Apps.</span><span class="sxs-lookup"><span data-stu-id="8c95c-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="8c95c-105">Les procédures dans cette rubrique doivent être effectuées à l'aide de l'interface web Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="8c95c-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c95c-106">Il est recommandé d'apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="8c95c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8c95c-107">Cette meilleure pratique importante procure la flexibilité nécessaire à l'avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance.</span><span class="sxs-lookup"><span data-stu-id="8c95c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8c95c-108">Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d'autres instances pour réutiliser votre configuration de tarification.</span><span class="sxs-lookup"><span data-stu-id="8c95c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8c95c-109">Créer des champs et des jeux d'options personnalisés dans la solution de dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="8c95c-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8c95c-110">Une dimension Tarification peut être un jeu d'options ou une entité.</span><span class="sxs-lookup"><span data-stu-id="8c95c-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8c95c-111">Tous deux doivent être créés dans votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="8c95c-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8c95c-112">Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="8c95c-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8c95c-113">Dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="8c95c-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="8c95c-114">Dans PSA, cliquez sur **Paramètres** > **Solutions** , puis double-cliquez sur **Dimensions Tarification \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8c95c-115">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8c95c-116">Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="8c95c-117">Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Définition de l'entité Titre standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="8c95c-119">Dimensions basées sur un jeu d'options</span><span class="sxs-lookup"><span data-stu-id="8c95c-119">Option set-based dimensions</span></span> 
<span data-ttu-id="8c95c-120">Vous pouvez créer deux dimensions basées sur un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="8c95c-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="8c95c-121">Utilisez **Emplacement de travail des ressources** pour suivre le prix du travail d'emplacement **Accueil** et du travail **Sur le site** et utilisez **Heures de travail des ressources** avec les valeurs **Régulier** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="8c95c-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="8c95c-122">Dans PSA, cliquez sur **Paramètres** > **Solutions** , puis double-cliquez sur **Dimensions Tarification \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8c95c-123">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Jeux d'options**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8c95c-124">Cliquez sur **Nouveau** pour créer un jeu d'options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="8c95c-125">Dimension Tarification basée sur un jeu d'options appelé Emplacement de travail de la ressource</span><span class="sxs-lookup"><span data-stu-id="8c95c-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="8c95c-126">Dimension Tarification basée sur un jeu d'options appelé Heures de travail de la ressource</span><span class="sxs-lookup"><span data-stu-id="8c95c-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8c95c-127">Créer des données pour les dimensions basées sur une entité</span><span class="sxs-lookup"><span data-stu-id="8c95c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8c95c-128">Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l'importation Microsoft Excel ou les appels de service.</span><span class="sxs-lookup"><span data-stu-id="8c95c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8c95c-129">Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8c95c-130">Si les données que vous voulez créer sont petites, comme dans l'exemple suivant, vous pouvez utiliser un formulaire standard.</span><span class="sxs-lookup"><span data-stu-id="8c95c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8c95c-131">Dans PSA, cliquez sur **Recherche avancée**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="8c95c-132">Sélectionnez l’entité **Titre standard** , puis cliquez sur **Résultats**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="8c95c-133">Toutes les lignes de l'entité **Titre standard** s'afficheront.</span><span class="sxs-lookup"><span data-stu-id="8c95c-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="8c95c-134">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-134">Click **New**.</span></span> <span data-ttu-id="8c95c-135">Dans le champ **Nom** , entrez « Ingénieur système », puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8c95c-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="8c95c-136">Fermez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8c95c-136">Close the form.</span></span> 
4. <span data-ttu-id="8c95c-137">Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».</span><span class="sxs-lookup"><span data-stu-id="8c95c-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="8c95c-138">Exemple de données pour l'entité Titre standard</span><span class="sxs-lookup"><span data-stu-id="8c95c-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


