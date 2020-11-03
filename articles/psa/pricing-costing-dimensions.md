---
title: Page d'accueil Dimensions de tarification et des coûts
description: Cette rubrique présente les dimensions de tarification.
author: rumant
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
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075781"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="0c871-103">Page d'accueil Dimensions de tarification et des coûts</span><span class="sxs-lookup"><span data-stu-id="0c871-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="0c871-104">Les dimensions utilisées pour définir la tarification et le coût de la main-d’œuvre dans les organisations basées sur des projets sont influencées par les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="0c871-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="0c871-105">Personnes effectuant un travail similaire à leur expérience, leur rôle ou leur géographie</span><span class="sxs-lookup"><span data-stu-id="0c871-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="0c871-106">Travail à effectuer similaire en termes de complexité ou d’heure de la journée</span><span class="sxs-lookup"><span data-stu-id="0c871-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="0c871-107">Étant donné la nature classique de ces attributs du travail et des personnes nécessaires pour effectuer le travail, deux types de valeurs de dimension Tarification sont disponibles dans Project Service Automation :</span><span class="sxs-lookup"><span data-stu-id="0c871-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="0c871-108">**Jeux d’options**  : attributs qui sont des énumérations fixes d’un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="0c871-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="0c871-109">**Valeurs basées sur l’entité**  : attributs qui peuvent avoir un ensemble varié de valeurs qui sont finies, mais qui peuvent changer avec le temps.</span><span class="sxs-lookup"><span data-stu-id="0c871-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="0c871-110">Dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="0c871-110">Pricing dimensions</span></span>

<span data-ttu-id="0c871-111">Expéditions PSA avec un ensemble par défaut de dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="0c871-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="0c871-112">Vous pouvez consulter ces derniers en accédant à **Project Service** > **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="0c871-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="0c871-113">Dans l'enregistrement du paramètre, dans l'onglet **Dimensions de tarification basées sur un montant** , vérifiez que le rôle, **msdyn_resourcecategory** et l'unité d'organisation d'allocation des ressources, **msdyn_organizationalunit** , contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="0c871-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="0c871-114">Vous pourrez ainsi configurer le prix et le coût de chaque combinaison de rôle et d'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="0c871-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Capture d'écran des paramètres de Project Service avec « Applicable aux ventes » en surbrillance](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="0c871-116">Si vous avez utilisé les champs prédéfinis du rôle et de l'unité d'organisation comme dimensions de tarification avant la version 3 de PSA, il n'existera pas de modification observable.</span><span class="sxs-lookup"><span data-stu-id="0c871-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="0c871-117">Vous pouvez continuer à utiliser Project Service comme d'habitude.</span><span class="sxs-lookup"><span data-stu-id="0c871-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="0c871-118">Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0c871-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="0c871-119">Pour plus d'informations, consultez les rubriques suivantes, toutefois notez que vous devez exécuter les procédures dans l'ordre indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="0c871-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="0c871-120">Créer des champs et des entités personnalisés</span><span class="sxs-lookup"><span data-stu-id="0c871-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="0c871-121">Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles</span><span class="sxs-lookup"><span data-stu-id="0c871-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="0c871-122">Configurer des champs personnalisés comme dimensions de tarification </span><span class="sxs-lookup"><span data-stu-id="0c871-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="0c871-123">Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="0c871-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="0c871-124">Tarification du temps des ressources humaines</span><span class="sxs-lookup"><span data-stu-id="0c871-124">Pricing human resource time</span></span>
<span data-ttu-id="0c871-125">Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="0c871-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="0c871-126">Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.</span><span class="sxs-lookup"><span data-stu-id="0c871-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="0c871-127">D'autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0c871-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="0c871-128">Les champs, tels que **Catégorie de transaction** ( **msdyn_transactioncategory** ) et **Ressource pouvant être réservée** ( **bookableresource** ) sont des exemples des dimensions possibles.</span><span class="sxs-lookup"><span data-stu-id="0c871-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="0c871-129">Choisissez si votre dimension de tarification doit être une table ou un jeu d'options.</span><span class="sxs-lookup"><span data-stu-id="0c871-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="0c871-130">Si vous prévoyez de changer des valeurs d’une dimension qui dépasseront 10 ou 12 et si vous avez besoin d’autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d’options.</span><span class="sxs-lookup"><span data-stu-id="0c871-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="0c871-131">Tenir à jour un jeu d’options, tel qu’ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu’ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs professionnels.</span><span class="sxs-lookup"><span data-stu-id="0c871-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="0c871-132">L'exemple suivant présente des taux de factures configurés en fonction du rôle et de l'unité d'organisation d'allocation des ressources à laquelle la ressource appartient.</span><span class="sxs-lookup"><span data-stu-id="0c871-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="0c871-133">Les taux de coûts sont généralement basés sur la bande du salaire de l'employé et l'unité d'organisation à laquelle il appartient.</span><span class="sxs-lookup"><span data-stu-id="0c871-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="0c871-134">Dans cet exemple, les tables de taux de factures et de taux de coûts ressemblent au suivant.</span><span class="sxs-lookup"><span data-stu-id="0c871-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="0c871-135">**Exemple de taux de factures**</span><span class="sxs-lookup"><span data-stu-id="0c871-135">**Sample bill rates**</span></span>

| <span data-ttu-id="0c871-136">Rôle</span><span class="sxs-lookup"><span data-stu-id="0c871-136">Role</span></span>        | <span data-ttu-id="0c871-137">Unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="0c871-137">Org Unit</span></span>    |<span data-ttu-id="0c871-138">Unité</span><span class="sxs-lookup"><span data-stu-id="0c871-138">Unit</span></span>      |<span data-ttu-id="0c871-139">Prix</span><span class="sxs-lookup"><span data-stu-id="0c871-139">Price</span></span>      |<span data-ttu-id="0c871-140">Devise</span><span class="sxs-lookup"><span data-stu-id="0c871-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0c871-141">Développeur</span><span class="sxs-lookup"><span data-stu-id="0c871-141">Developer</span></span>   | <span data-ttu-id="0c871-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0c871-142">Contoso US</span></span>  |<span data-ttu-id="0c871-143">Hour</span><span class="sxs-lookup"><span data-stu-id="0c871-143">Hour</span></span> | <span data-ttu-id="0c871-144">200</span><span class="sxs-lookup"><span data-stu-id="0c871-144">200</span></span>|<span data-ttu-id="0c871-145">USD</span><span class="sxs-lookup"><span data-stu-id="0c871-145">USD</span></span>     |
| <span data-ttu-id="0c871-146">Développeur</span><span class="sxs-lookup"><span data-stu-id="0c871-146">Developer</span></span>   | <span data-ttu-id="0c871-147">Contoso Inde</span><span class="sxs-lookup"><span data-stu-id="0c871-147">Contoso India</span></span> |<span data-ttu-id="0c871-148">Hour</span><span class="sxs-lookup"><span data-stu-id="0c871-148">Hour</span></span>|   <span data-ttu-id="0c871-149">112</span><span class="sxs-lookup"><span data-stu-id="0c871-149">112</span></span>|<span data-ttu-id="0c871-150">USD</span><span class="sxs-lookup"><span data-stu-id="0c871-150">USD</span></span>     |


<span data-ttu-id="0c871-151">**Exemple de taux de coûts**</span><span class="sxs-lookup"><span data-stu-id="0c871-151">**Sample cost rates**</span></span>

| <span data-ttu-id="0c871-152">Bande de salaire</span><span class="sxs-lookup"><span data-stu-id="0c871-152">Salary Band</span></span>     | <span data-ttu-id="0c871-153">Unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="0c871-153">Org Unit</span></span>    |<span data-ttu-id="0c871-154">Unité</span><span class="sxs-lookup"><span data-stu-id="0c871-154">Unit</span></span>      |<span data-ttu-id="0c871-155">Prix</span><span class="sxs-lookup"><span data-stu-id="0c871-155">Price</span></span>      |<span data-ttu-id="0c871-156">Devise</span><span class="sxs-lookup"><span data-stu-id="0c871-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0c871-157">Ma société_Band1</span><span class="sxs-lookup"><span data-stu-id="0c871-157">My company_Band1</span></span> | <span data-ttu-id="0c871-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0c871-158">Contoso US</span></span>  |<span data-ttu-id="0c871-159">Hour</span><span class="sxs-lookup"><span data-stu-id="0c871-159">Hour</span></span> | <span data-ttu-id="0c871-160">145</span><span class="sxs-lookup"><span data-stu-id="0c871-160">145</span></span>|<span data-ttu-id="0c871-161">USD</span><span class="sxs-lookup"><span data-stu-id="0c871-161">USD</span></span>     |
| <span data-ttu-id="0c871-162">Ma société_Band2</span><span class="sxs-lookup"><span data-stu-id="0c871-162">My company_Band2</span></span> | <span data-ttu-id="0c871-163">Contoso Inde</span><span class="sxs-lookup"><span data-stu-id="0c871-163">Contoso India</span></span> |<span data-ttu-id="0c871-164">Hour</span><span class="sxs-lookup"><span data-stu-id="0c871-164">Hour</span></span>|   <span data-ttu-id="0c871-165">67</span><span class="sxs-lookup"><span data-stu-id="0c871-165">67</span></span>|<span data-ttu-id="0c871-166">USD</span><span class="sxs-lookup"><span data-stu-id="0c871-166">USD</span></span>     |