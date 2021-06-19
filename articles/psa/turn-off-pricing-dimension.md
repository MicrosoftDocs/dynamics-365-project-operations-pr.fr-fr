---
title: Désactiver une dimension de tarification
description: Cette rubrique indique comment configurer des dimensions de tarification dans la solution Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014293"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="b3864-103">Désactiver une dimension de tarification</span><span class="sxs-lookup"><span data-stu-id="b3864-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b3864-104">Vous devez peut-être vérifier et mettre à jour régulièrement votre stratégie de tarification.</span><span class="sxs-lookup"><span data-stu-id="b3864-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="b3864-105">Les mises à jour que vous effectuez peuvent nécessiter de désactiver une dimension de tarification existante et d’en créer une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="b3864-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="b3864-106">Par exemple, vous avez peut-être précédemment fixé le prix par **Rôle**, mais maintenant vous avez décidé de fixer le prix par **Expérience professionnelle**.</span><span class="sxs-lookup"><span data-stu-id="b3864-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="b3864-107">Cela peut nécessiter de désactiver la valeur **Rôle** comme dimension de tarification et de créer la valeur **Expérience professionnelle** comme nouvelle dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="b3864-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="b3864-108">La désactivation d’une dimension de tarification, qu’elle soit prédéfinie ou personnalisée, peut être effectuée en définissant les champs **Applicable aux coûts** et **Applicable aux ventes** de la dimension de tarification sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="b3864-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="b3864-109">Toutefois, lorsque vous effectuez cette action, vous pouvez recevoir le message d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="b3864-109">However, when you do this, you might receive the following error message.</span></span>

![Erreur de processus d’entreprise probablement lors de la désactivation d’une dimension de tarification](media/Business-Process-Error.png)


<span data-ttu-id="b3864-111">Ce message d’erreur indique que des enregistrements de prix ont été précédemment configurés pour la dimension désactivée.</span><span class="sxs-lookup"><span data-stu-id="b3864-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="b3864-112">Tous les enregistrements **Prix du rôle** et **Majoration du prix du rôle** qui font référence à une dimension doivent être supprimés avant que l’applicabilité de la dimension puisse être définie sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="b3864-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="b3864-113">Cette règle s’applique à la fois aux dimensions de tarification prédéfinies et aux dimensions de tarification personnalisées que vous avez peut-être créées.</span><span class="sxs-lookup"><span data-stu-id="b3864-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="b3864-114">La raison de cette validation est que Project Service a la contrainte que chaque enregistrement **Prix du rôle** doit avoir une combinaison unique de dimensions.</span><span class="sxs-lookup"><span data-stu-id="b3864-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="b3864-115">Par exemple, sur une liste de prix appelée **Taux de coût US 2018**, les lignes **Prix du rôle** suivantes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="b3864-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="b3864-116">Titre standard</span><span class="sxs-lookup"><span data-stu-id="b3864-116">Standard Title</span></span>         | <span data-ttu-id="b3864-117">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="b3864-117">Org Unit</span></span>    |<span data-ttu-id="b3864-118">Unité</span><span class="sxs-lookup"><span data-stu-id="b3864-118">Unit</span></span>   |<span data-ttu-id="b3864-119">Prix</span><span class="sxs-lookup"><span data-stu-id="b3864-119">Price</span></span>  |<span data-ttu-id="b3864-120">Devise</span><span class="sxs-lookup"><span data-stu-id="b3864-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="b3864-121">Ingénieur système</span><span class="sxs-lookup"><span data-stu-id="b3864-121">Systems Engineer</span></span>|<span data-ttu-id="b3864-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b3864-122">Contoso US</span></span>|<span data-ttu-id="b3864-123">heure</span><span class="sxs-lookup"><span data-stu-id="b3864-123">Hour</span></span>| <span data-ttu-id="b3864-124">100</span><span class="sxs-lookup"><span data-stu-id="b3864-124">100</span></span>|<span data-ttu-id="b3864-125">USD</span><span class="sxs-lookup"><span data-stu-id="b3864-125">USD</span></span>|
| <span data-ttu-id="b3864-126">Ingénieur senior système</span><span class="sxs-lookup"><span data-stu-id="b3864-126">Senior Systems Engineer</span></span>|<span data-ttu-id="b3864-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b3864-127">Contoso US</span></span>|<span data-ttu-id="b3864-128">heure</span><span class="sxs-lookup"><span data-stu-id="b3864-128">Hour</span></span>| <span data-ttu-id="b3864-129">150</span><span class="sxs-lookup"><span data-stu-id="b3864-129">150</span></span>| <span data-ttu-id="b3864-130">USD</span><span class="sxs-lookup"><span data-stu-id="b3864-130">USD</span></span>|


<span data-ttu-id="b3864-131">Lorsque vous désactivez la valeur **Titre standard** comme dimension de tarification et que le moteur de tarification de Project Service recherche un prix, il utilise uniquement la valeur **Unité d’organisation** dans le contexte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b3864-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="b3864-132">Si la valeur **Unité d’organisation** du contexte d’entrée est « Contoso US », le résultat n’est pas déterministe car les deux lignes correspondent.</span><span class="sxs-lookup"><span data-stu-id="b3864-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="b3864-133">Pour éviter ce scénario, lorsque vous créez des enregistrements **Prix du rôle**, Project Service valide que la combinaison de dimensions est unique.</span><span class="sxs-lookup"><span data-stu-id="b3864-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="b3864-134">Si la dimension est désactivée après la création des enregistrements **Prix du rôle**, cette contrainte peut être enfreinte.</span><span class="sxs-lookup"><span data-stu-id="b3864-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="b3864-135">Par conséquent, avant de désactiver une dimension, il est nécessaire de supprimer toutes les lignes **Prix du rôle** et **Majoration du prix du rôle** pour lesquelles cette valeur de dimension est renseignée.</span><span class="sxs-lookup"><span data-stu-id="b3864-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]