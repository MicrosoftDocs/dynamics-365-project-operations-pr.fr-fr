---
title: Vue d’ensemble des dimensions de tarification
description: Cette rubrique fournit des informations sur les dimensions de tarification dans Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075847"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="d6c45-103">Vue d’ensemble des dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="d6c45-103">Pricing dimensions overview</span></span>

<span data-ttu-id="d6c45-104">_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="d6c45-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6c45-105">Les dimensions qui sont utilisées dans les ressources humaines pour définir la tarification et les coûts ont deux catégories :</span><span class="sxs-lookup"><span data-stu-id="d6c45-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d6c45-106">Personnes</span><span class="sxs-lookup"><span data-stu-id="d6c45-106">People</span></span>
- <span data-ttu-id="d6c45-107">Travail planifié</span><span class="sxs-lookup"><span data-stu-id="d6c45-107">Planned work</span></span>

<span data-ttu-id="d6c45-108">Pour cette raison, deux types de valeurs de dimension de tarification sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="d6c45-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="d6c45-109">**Jeux d'options**  : Dimensions qui sont des énumérations fixes d'un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="d6c45-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d6c45-110">**Valeurs basées sur une entité**  : Dimensions qui peuvent être un ensemble de valeurs varié.</span><span class="sxs-lookup"><span data-stu-id="d6c45-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d6c45-111">Dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="d6c45-111">Pricing dimensions</span></span>

<span data-ttu-id="d6c45-112">Dynamics 365 Project Operations est livré avec un ensemble par défaut de dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="d6c45-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d6c45-113">Vous pouvez les consulter en accédant à **Project Operations** > **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="d6c45-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="d6c45-114">Dans l'enregistrement du paramètre, dans l'onglet **Dimensions de tarification basées sur un montant** , vérifiez que le rôle, **msdyn_resourcecategory** et l'unité d'organisation d'allocation des ressources, **msdyn_organizationalunit** , contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d6c45-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d6c45-115">Si ces champs sont activés, vous pouvez alors configurer le prix et le coût de chaque combinaison de rôle et d'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="d6c45-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="d6c45-116">Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d6c45-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d6c45-117">Tarification du temps des ressources humaines</span><span class="sxs-lookup"><span data-stu-id="d6c45-117">Pricing human resource time</span></span>
<span data-ttu-id="d6c45-118">Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="d6c45-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d6c45-119">Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.</span><span class="sxs-lookup"><span data-stu-id="d6c45-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d6c45-120">D'autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d6c45-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d6c45-121">Les champs, tels que **Catégorie de transaction** ( **msdyn_transactioncategory** ) et **Ressource pouvant être réservée** ( **bookableresource** ) sont des exemples des dimensions possibles.</span><span class="sxs-lookup"><span data-stu-id="d6c45-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d6c45-122">Choisissez si votre dimension de tarification doit être une table ou un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="d6c45-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d6c45-123">Si vous prévoyez de changer des valeurs d'une dimension qui dépasseront 10 ou 12 et que vous avez besoin d'autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="d6c45-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d6c45-124">Tenir à jour un jeu d'options, tel qu'ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu'ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d6c45-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d6c45-125">L'exemple suivant présente des taux de factures configurés en fonction du rôle et de l'unité d'organisation d'allocation des ressources à laquelle la ressource appartient.</span><span class="sxs-lookup"><span data-stu-id="d6c45-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d6c45-126">Les taux de coûts sont généralement basés sur la bande du salaire de l'employé et l'unité d'organisation à laquelle il appartient.</span><span class="sxs-lookup"><span data-stu-id="d6c45-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d6c45-127">Dans cet exemple, les tables de taux de factures et de taux de coûts ressemblent au suivant.</span><span class="sxs-lookup"><span data-stu-id="d6c45-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d6c45-128">**Exemple de taux de factures**</span><span class="sxs-lookup"><span data-stu-id="d6c45-128">**Sample bill rates**</span></span>

| <span data-ttu-id="d6c45-129">Rôle</span><span class="sxs-lookup"><span data-stu-id="d6c45-129">Role</span></span>        | <span data-ttu-id="d6c45-130">Unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="d6c45-130">Org Unit</span></span>    |<span data-ttu-id="d6c45-131">Unité</span><span class="sxs-lookup"><span data-stu-id="d6c45-131">Unit</span></span>      |<span data-ttu-id="d6c45-132">Prix</span><span class="sxs-lookup"><span data-stu-id="d6c45-132">Price</span></span>      |<span data-ttu-id="d6c45-133">Devise</span><span class="sxs-lookup"><span data-stu-id="d6c45-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d6c45-134">Développeur</span><span class="sxs-lookup"><span data-stu-id="d6c45-134">Developer</span></span>   | <span data-ttu-id="d6c45-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d6c45-135">Contoso US</span></span>  |<span data-ttu-id="d6c45-136">Hour</span><span class="sxs-lookup"><span data-stu-id="d6c45-136">Hour</span></span> | <span data-ttu-id="d6c45-137">200</span><span class="sxs-lookup"><span data-stu-id="d6c45-137">200</span></span>|<span data-ttu-id="d6c45-138">USD</span><span class="sxs-lookup"><span data-stu-id="d6c45-138">USD</span></span>     |
| <span data-ttu-id="d6c45-139">Développeur</span><span class="sxs-lookup"><span data-stu-id="d6c45-139">Developer</span></span>   | <span data-ttu-id="d6c45-140">Contoso Inde</span><span class="sxs-lookup"><span data-stu-id="d6c45-140">Contoso India</span></span> |<span data-ttu-id="d6c45-141">Hour</span><span class="sxs-lookup"><span data-stu-id="d6c45-141">Hour</span></span>|   <span data-ttu-id="d6c45-142">112</span><span class="sxs-lookup"><span data-stu-id="d6c45-142">112</span></span>|<span data-ttu-id="d6c45-143">USD</span><span class="sxs-lookup"><span data-stu-id="d6c45-143">USD</span></span>     |


<span data-ttu-id="d6c45-144">**Exemple de taux de coûts**</span><span class="sxs-lookup"><span data-stu-id="d6c45-144">**Sample cost rates**</span></span>

| <span data-ttu-id="d6c45-145">Bande de salaire</span><span class="sxs-lookup"><span data-stu-id="d6c45-145">Salary Band</span></span>     | <span data-ttu-id="d6c45-146">Unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="d6c45-146">Org Unit</span></span>    |<span data-ttu-id="d6c45-147">Unité</span><span class="sxs-lookup"><span data-stu-id="d6c45-147">Unit</span></span>      |<span data-ttu-id="d6c45-148">Prix</span><span class="sxs-lookup"><span data-stu-id="d6c45-148">Price</span></span>      |<span data-ttu-id="d6c45-149">Devise</span><span class="sxs-lookup"><span data-stu-id="d6c45-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d6c45-150">Ma société_Band1</span><span class="sxs-lookup"><span data-stu-id="d6c45-150">My company_Band1</span></span> | <span data-ttu-id="d6c45-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d6c45-151">Contoso US</span></span>  |<span data-ttu-id="d6c45-152">Hour</span><span class="sxs-lookup"><span data-stu-id="d6c45-152">Hour</span></span> | <span data-ttu-id="d6c45-153">145</span><span class="sxs-lookup"><span data-stu-id="d6c45-153">145</span></span>|<span data-ttu-id="d6c45-154">USD</span><span class="sxs-lookup"><span data-stu-id="d6c45-154">USD</span></span>     |
| <span data-ttu-id="d6c45-155">Ma société_Band2</span><span class="sxs-lookup"><span data-stu-id="d6c45-155">My company_Band2</span></span> | <span data-ttu-id="d6c45-156">Contoso Inde</span><span class="sxs-lookup"><span data-stu-id="d6c45-156">Contoso India</span></span> |<span data-ttu-id="d6c45-157">Hour</span><span class="sxs-lookup"><span data-stu-id="d6c45-157">Hour</span></span>|   <span data-ttu-id="d6c45-158">67</span><span class="sxs-lookup"><span data-stu-id="d6c45-158">67</span></span>|<span data-ttu-id="d6c45-159">USD</span><span class="sxs-lookup"><span data-stu-id="d6c45-159">USD</span></span>     |
