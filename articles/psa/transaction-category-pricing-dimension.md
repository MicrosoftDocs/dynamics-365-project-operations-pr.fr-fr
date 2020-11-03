---
title: Utiliser une catégorie de transaction comme dimension de tarification
description: Cette rubrique donne des informations sur l'utilisation d'une catégorie de transaction comme dimension de tarification.
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
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075824"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="3a75e-103">Utiliser une catégorie de transaction comme dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="3a75e-103">Use transaction category as a pricing dimension</span></span>
<span data-ttu-id="3a75e-104">Cette rubrique indique comment utiliser une catégorie de transaction comme dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="3a75e-104">This topic shows how to use a transaction category as a pricing dimension.</span></span> <span data-ttu-id="3a75e-105">Avant de commencer, si vos n'avez pas déjà créé une solution Dimension de tarification, vous devez en créer une.</span><span class="sxs-lookup"><span data-stu-id="3a75e-105">Before you begin, if you have not already created a pricing dimension solution, you will need to create a new one.</span></span> <span data-ttu-id="3a75e-106">Si vous disposez déjà d'une solution Dimension de tarification, vous pouvez apporter vos modifications dans cette solution.</span><span class="sxs-lookup"><span data-stu-id="3a75e-106">If you already have a pricing dimension solution, then you can make your changes in that solution.</span></span> <span data-ttu-id="3a75e-107">Si vous n'avez pas créé de solution Dimension de tarification pour votre organisation, effectuez les procédures décrites dans la rubrique [Créer des champs et des entités personnalisés](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="3a75e-107">If you have not created a new pricing dimension solution for your organization, complete the procedures in the [Create custom fields and entities](create-custom-fields-entities.md) topic.</span></span>

## <a name="add-transaction-category-to-forms-and-views"></a><span data-ttu-id="3a75e-108">Ajouter une catégorie de transaction aux formulaires et vues</span><span class="sxs-lookup"><span data-stu-id="3a75e-108">Add transaction category to forms and views</span></span>
<span data-ttu-id="3a75e-109">Pour rendre la catégorie de transaction visible dans l'interface utilisateur de la solution Dimension de tarification, vous devez parcourir tous les formulaires et vues des principales entités et ajouter ces champs aux formulaires et vues de ces entités.</span><span class="sxs-lookup"><span data-stu-id="3a75e-109">To make transaction category visible in the UI in the pricing dimension solution, you will need to walk through all the forms and views of the key entities and add these fields to the forms and views of those entities.</span></span>
<span data-ttu-id="3a75e-110">Le tableau suivant présente une liste complète des formulaires et vues prédéfinis, répertoriés par entité, qui doivent être mis à jour avec les nouveaux champs.</span><span class="sxs-lookup"><span data-stu-id="3a75e-110">The following table is a comprehensive list of the out-of-the box forms and views, listed by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="3a75e-111">S'il existe des vues ou formulaires supplémentaires dans vos personnalisations de ces entités, ajoutez-y également les nouveaux champs.</span><span class="sxs-lookup"><span data-stu-id="3a75e-111">If there any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

|  <span data-ttu-id="3a75e-112">Entité</span><span class="sxs-lookup"><span data-stu-id="3a75e-112">Entity</span></span>        | <span data-ttu-id="3a75e-113">Formulaires</span><span class="sxs-lookup"><span data-stu-id="3a75e-113">Forms</span></span>     |<span data-ttu-id="3a75e-114">Vues</span><span class="sxs-lookup"><span data-stu-id="3a75e-114">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="3a75e-115">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="3a75e-115">Role Price</span></span>|<span data-ttu-id="3a75e-116">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-116">• Information</span></span> |<span data-ttu-id="3a75e-117">• Prix de la catégorie de ressource actifs</span><span class="sxs-lookup"><span data-stu-id="3a75e-117">• Active Resource Category Prices</span></span><br> <span data-ttu-id="3a75e-118">• Vue associée Prix de la catégorie de ressource</span><span class="sxs-lookup"><span data-stu-id="3a75e-118">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="3a75e-119">Majoration du prix du rôle</span><span class="sxs-lookup"><span data-stu-id="3a75e-119">Role Price Markup</span></span>|<span data-ttu-id="3a75e-120">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-120">• Information</span></span>|<span data-ttu-id="3a75e-121">• Majorations du prix du rôle actives</span><span class="sxs-lookup"><span data-stu-id="3a75e-121">• Active Role Price Markup</span></span><br><span data-ttu-id="3a75e-122">• Vue associée Majoration du prix du rôle</span><span class="sxs-lookup"><span data-stu-id="3a75e-122">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="3a75e-123">Détail de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="3a75e-123">Quote line detail</span></span>|<span data-ttu-id="3a75e-124">• Informations sur le projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-124">• Project Information</span></span><br><span data-ttu-id="3a75e-125">• Création rapide de projets</span><span class="sxs-lookup"><span data-stu-id="3a75e-125">• Project Quick Create</span></span>|<span data-ttu-id="3a75e-126">• Détail de la ligne de devis active</span><span class="sxs-lookup"><span data-stu-id="3a75e-126">• Active Quote Line Detail</span></span><br><span data-ttu-id="3a75e-127">• Détails de la ligne de devis combinée</span><span class="sxs-lookup"><span data-stu-id="3a75e-127">• Combined Quote Line Details</span></span><br><span data-ttu-id="3a75e-128">• Vue associée Détail de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="3a75e-128">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="3a75e-129">Détail de la ligne de contrat du projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-129">Project Contract line detail</span></span>|<span data-ttu-id="3a75e-130">• Informations sur le projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-130">• Project Information</span></span><br><span data-ttu-id="3a75e-131">• Création rapide de projets</span><span class="sxs-lookup"><span data-stu-id="3a75e-131">• Project Quick Create</span></span>|<span data-ttu-id="3a75e-132">• Détails de la ligne de contrat combinée</span><span class="sxs-lookup"><span data-stu-id="3a75e-132">• Combined Contract line Details</span></span><br><span data-ttu-id="3a75e-133">• Détails de la ligne de contrat active</span><span class="sxs-lookup"><span data-stu-id="3a75e-133">• Active Contract Line Details</span></span><br><span data-ttu-id="3a75e-134">• Vue associée Détails de la ligne de contrat</span><span class="sxs-lookup"><span data-stu-id="3a75e-134">• Contract Line Detail associated view</span></span>|
|  <span data-ttu-id="3a75e-135">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-135">Project Task</span></span>|<span data-ttu-id="3a75e-136">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-136">• Information</span></span><br><span data-ttu-id="3a75e-137">• Nouveau formulaire</span><span class="sxs-lookup"><span data-stu-id="3a75e-137">• New Form</span></span>||
|  <span data-ttu-id="3a75e-138">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-138">Project Team Member</span></span>|<span data-ttu-id="3a75e-139">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-139">• Information</span></span><br><span data-ttu-id="3a75e-140">• Nouveau formulaire</span><span class="sxs-lookup"><span data-stu-id="3a75e-140">• New Form</span></span>|<span data-ttu-id="3a75e-141">• Membres de l'équipe du projet actifs</span><span class="sxs-lookup"><span data-stu-id="3a75e-141">• Active Project Team Members</span></span><br><span data-ttu-id="3a75e-142">• Membres de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-142">• Project Team Members</span></span><br><span data-ttu-id="3a75e-143">• Vue associée Membres de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="3a75e-143">• Project Team members associated View</span></span>|
|  <span data-ttu-id="3a75e-144">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="3a75e-144">Time Entry</span></span>|<span data-ttu-id="3a75e-145">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-145">• Information</span></span><br><span data-ttu-id="3a75e-146">• Créer une entrée de temps</span><span class="sxs-lookup"><span data-stu-id="3a75e-146">• Create Time Entry</span></span>|<span data-ttu-id="3a75e-147">• Mes entrées de temps par date</span><span class="sxs-lookup"><span data-stu-id="3a75e-147">• My Time Entries By Date</span></span><br><span data-ttu-id="3a75e-148">• Mes entrées de temps pour cette semaine</span><span class="sxs-lookup"><span data-stu-id="3a75e-148">• My time Entries for this week</span></span><br><span data-ttu-id="3a75e-149">• Entrées des temps pour approbation</span><span class="sxs-lookup"><span data-stu-id="3a75e-149">• Time entries for approval</span></span>|
|  <span data-ttu-id="3a75e-150">Ligne de journal</span><span class="sxs-lookup"><span data-stu-id="3a75e-150">Journal Line</span></span>|<span data-ttu-id="3a75e-151">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-151">• Information</span></span><br><span data-ttu-id="3a75e-152">• Création rapide</span><span class="sxs-lookup"><span data-stu-id="3a75e-152">• Quick create</span></span>|<span data-ttu-id="3a75e-153">• Lignes de journal actives</span><span class="sxs-lookup"><span data-stu-id="3a75e-153">• Active journal lines</span></span><br><span data-ttu-id="3a75e-154">• Vue associée Ligne de journal</span><span class="sxs-lookup"><span data-stu-id="3a75e-154">• Journal Line associated view</span></span>|
|  <span data-ttu-id="3a75e-155">Détail de la ligne de facture</span><span class="sxs-lookup"><span data-stu-id="3a75e-155">Invoice Line Detail</span></span>|<span data-ttu-id="3a75e-156">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-156">• Information</span></span><br><span data-ttu-id="3a75e-157">• Création rapide</span><span class="sxs-lookup"><span data-stu-id="3a75e-157">• Quick create</span></span>|<span data-ttu-id="3a75e-158">• Détails de la ligne de facture active</span><span class="sxs-lookup"><span data-stu-id="3a75e-158">• Active Invoice Line Details</span></span><br><span data-ttu-id="3a75e-159">• Transactions facturables</span><span class="sxs-lookup"><span data-stu-id="3a75e-159">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="3a75e-160">• Transactions gratuites</span><span class="sxs-lookup"><span data-stu-id="3a75e-160">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="3a75e-161">• Vue associée Détails de la ligne de facture</span><span class="sxs-lookup"><span data-stu-id="3a75e-161">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="3a75e-162">• Transactions non facturables</span><span class="sxs-lookup"><span data-stu-id="3a75e-162">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="3a75e-163">Chiffre réel</span><span class="sxs-lookup"><span data-stu-id="3a75e-163">Actual</span></span>|<span data-ttu-id="3a75e-164">• Informations</span><span class="sxs-lookup"><span data-stu-id="3a75e-164">• Information</span></span><br><span data-ttu-id="3a75e-165">• Chiffres réels actifs</span><span class="sxs-lookup"><span data-stu-id="3a75e-165">• Active Actuals</span></span>|<span data-ttu-id="3a75e-166">• Vue associée Chiffre réel</span><span class="sxs-lookup"><span data-stu-id="3a75e-166">• Actual Associated view</span></span>|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="3a75e-167">Configurer une catégorie de transaction comme dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="3a75e-167">Set up transaction category as a pricing dimension</span></span>

1. <span data-ttu-id="3a75e-168">Dans l'interface Web, accédez à **Project Service** > **Paramètres** > **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3a75e-168">In the web interface, go to **Project Service** > **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="3a75e-169">Dans la page **Paramètres** , sous l'onglet **Dimensions de tarification basées sur le montant** , notez que la grille de l'onglet affiche les enregistrements de l'entité **Dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="3a75e-169">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, note the grid on the tab shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="3a75e-170">Ajoutez **Catégorie de transaction** à cette liste et définissez les champs **Applicable aux coûts** et **Applicable aux ventes** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3a75e-170">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields set to **Yes**.</span></span>
4. <span data-ttu-id="3a75e-171">Dans le champ **Type de dimension** , sélectionnez **Basé sur le montant** , puis sélectionnez la priorité de la **Catégorie de transaction** pour les coûts et les ventes.</span><span class="sxs-lookup"><span data-stu-id="3a75e-171">In the **Dimension Type** field, select **Amount-based** , and then select the priority for **Transaction Category** related to cost and sales.</span></span>