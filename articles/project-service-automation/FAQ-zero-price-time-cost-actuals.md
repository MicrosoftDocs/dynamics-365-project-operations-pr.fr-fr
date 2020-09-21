---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des heures ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels de coût des heures.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168158"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="b2a8a-103">Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des heures ?</span><span class="sxs-lookup"><span data-stu-id="b2a8a-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b2a8a-104">Cette FAQ s'applique aux chiffres réels où la classe de transaction est définie sur Heures et le type de transaction est Coût.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="b2a8a-105">Les trois vérifications suivantes vous aideront à résoudre la définition de la valeur par défaut du prix sur 0 sur les chiffres réels de coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="b2a8a-106">Vérification 1 : Identifier les prix de revient du projet</span><span class="sxs-lookup"><span data-stu-id="b2a8a-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="b2a8a-107">Rechercher le projet dans le champ de projet du chiffre réel puis accédez à la page de projet.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="b2a8a-108">Cliquez sur le lien de l'unité contractuelle dans le champ.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="b2a8a-109">Dans la page Unité contractuelle, vérifiez si l'unité contractuelle possède un tarif dans la grille des prix de revient.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="b2a8a-110">S'il existe plusieurs tarifs, vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="b2a8a-111">Project Service prend en charge un seul tarif par unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="b2a8a-112">Supprimez tous les tarifs de cette entité jusqu'à ce qu'il n'en reste qu'un joint dans la grille des Prix de revient de l'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="b2a8a-113">En l'absence de tarifs joints à l'unité d'organisation, prenez note de la devise de l'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="b2a8a-114">Accédez à Project Service puis à Paramètres et ouvrez l'onglet Tarifs. Vérifiez s'il existe des tarifs avec le contexte défini sur Coût et une devise correspondant à la devise de l'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="b2a8a-115">Si aucun tarif ne correspond à ces critères, vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="b2a8a-116">Veillez à disposer d'au moins un tarif dont le contexte est défini sur Coût et dont la devise correspond à la devise de l'unité d'organisation.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="b2a8a-117">Si plusieurs tarifs correspondent à ces critères, continuez de lire ce document pour effectuer d'autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="b2a8a-118">Vérification 2 : L'un des tarifs identifiés ci-dessus sont-ils valides à la date spécifique du chiffre réel du coût des heures ?</span><span class="sxs-lookup"><span data-stu-id="b2a8a-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="b2a8a-119">Pour que Project Service prenne en compte un tarif pour le prix par défaut, ce tarif doit être applicable à la date du chiffre réel coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="b2a8a-120">Vérifiez les points suivants pour voir si les tarifs identifiés ci-dessus s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="b2a8a-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="b2a8a-121">Vérifiez si les dates de début et de fin sur l'onglet général des tarifs joints ne sont pas vides.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="b2a8a-122">Si les dates de début et de fin sur les tarifs identifiés ci-dessus sont vides, vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="b2a8a-123">Prenez note du champ de date de début sur votre chiffre réel de coût des heures et vérifiez si l'un des tarifs identifiés s'applique à cette date.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="b2a8a-124">Par exemple, la date du chiffre réel du coût des heures doit se situer entre la date de début et la date de fin sur les tarifs.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="b2a8a-125">Si aucun tarif ne couvre cette date dans le chiffre réel du coût des heures, vous avez le isolé problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="b2a8a-126">Modifiez les dates de début et de fin des tarifs pour vous assurer que les tarifs couvrent la date du chiffre réel du coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="b2a8a-127">Si plusieurs tarifs couvrent la date dans le chiffre réel du coût des heures, vous avez le isolé problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="b2a8a-128">Vous pouvez résoudre ce problème en modifiant les dates de début et de fin des tarifs afin qu'il ne reste qu'un seul tarif qui s'appliquent à la date du chiffre réel du coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="b2a8a-129">S'il n'existe qu'un tarif qui s'applique à cette date du chiffre réel du coût des heures, passez à la vérification suivante dans ce document.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="b2a8a-130">Une fois que vous avez terminé les corrections nécessaires, recréez l'entrée de l'heure, approuvez- la, et vérifiez que les chiffres réels du coût des heures affichent un prix valide.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="b2a8a-131">Vérification 3 : Existe-t-il un prix dans les tarifs pour les dimensions de tarification du chiffre réel du coût des heures ?</span><span class="sxs-lookup"><span data-stu-id="b2a8a-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="b2a8a-132">Si vous avez terminé la Vérification 1 et la Vérification 2, vous devez maintenant avoir un seul tarif qui s'applique à la date du chiffre réel du coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="b2a8a-133">Ouvrez ce tarif et accédez l'onglet Prix du rôle. Vérifiez qu'il existe une ligne dans la grille pour les dimensions de tarification sur le chiffre réel du coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="b2a8a-134">S'il n'y a aucune ligne dans la grille des prix de rôle pour les dimensions de tarification dans le chiffre réel du coût des heures, cela signifie que vous avez isolé le problème.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="b2a8a-135">Créez une ligne dans la grille Prix du rôle pour les dimensions de tarification dans votre chiffre réel du coût des heures.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="b2a8a-136">Une fois cette opération terminée, recréez l'entrée de l'heure, approuvez-la, et vérifiez que les chiffres réels du coût des heures affichent un prix valide.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="b2a8a-137">Si vous ne voyez toujours pas de prix valide sur votre chiffre réel du coût des heures après avoir terminé les trois vérifications ci-dessus, entrez un ticket du support technique.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



