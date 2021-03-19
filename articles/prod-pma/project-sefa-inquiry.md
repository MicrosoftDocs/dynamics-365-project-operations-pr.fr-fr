---
title: Demande de Programme des dépenses des subventions fédérales
description: Cette rubrique fournit des informations sur la demande de programme des dépenses de subventions fédérales.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288961"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="9fd2e-103">Demande de Programme des dépenses des subventions fédérales</span><span class="sxs-lookup"><span data-stu-id="9fd2e-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fd2e-104">Conformément à la circulaire A-133 du Bureau de la gestion et du budget (service du gouvernement américain), les organismes qui reçoivent des fonds fédéraux sont soumis à des obligations d'audit, également appelés audits uniques.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="9fd2e-105">Le processus de vérification sert à rendre compte des revenus et des dépenses des subventions fédérales de façon récurrente.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="9fd2e-106">Une partie du rapport d'audit unique comprend le Programme des dépenses des subventions fédérales (SEFA).</span><span class="sxs-lookup"><span data-stu-id="9fd2e-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="9fd2e-107">Le Programme des dépenses des subventions fédérales comprend le titre et le numéro du Catalogue d'assistance nationale fédérale (CFDA), le numéro de la subvention, l'année de la subvention, le nom de l'organisme fédéral fournissant les fonds et le nom de l'entité intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="9fd2e-108">La demande s'applique à une période déterminée.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="9fd2e-109">En règle générale, cette période est la même que la période des états financiers, c'est-à-dire un exercice.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="9fd2e-110">La demande inclut les subventions dont les dates de projection se situent dans la plage de dates sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="9fd2e-111">La colonne **Organisme donateur** de la demande montre le client de la subvention ou, dans le cas d'une subvention intermédiaire, l'organisme donateur.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="9fd2e-112">Pour une subvention intermédiaire, la colonne **Organisme intermédiaire** affiche le client de la subvention.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="9fd2e-113">Si la subvention n'est pas une subvention intermédiaire, la colonne **Organisme intermédiaire** est vide.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="9fd2e-114">Configurer les clusters CFDA</span><span class="sxs-lookup"><span data-stu-id="9fd2e-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="9fd2e-115">Vous devez configurer les clusters CFDA qui peuvent être associés à des numéros CFDA dans la demande de Programme des dépenses des subventions fédérales.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="9fd2e-116">Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Clusters du Catalogue d'assistance nationale fédérale**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="9fd2e-117">Sélectionnez **Nouveau** pour créer un cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="9fd2e-118">Entrez le nom du cluster.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="9fd2e-119">Sélectionnez **Enregistrer** pour appliquer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="9fd2e-120">Configurer les numéros CFDA</span><span class="sxs-lookup"><span data-stu-id="9fd2e-120">Set up CFDA numbers</span></span>

<span data-ttu-id="9fd2e-121">Vous devez configurer les numéros CFDA qui peuvent être ajoutés à des subventions et inclus dans la demande de Programme des dépenses des subventions fédérales.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="9fd2e-122">Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Numéros du Catalogue d'assistance nationale fédérale (CFDA)**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="9fd2e-123">Sélectionnez **Nouveau** pour créer un numéro CFDA.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="9fd2e-124">Dans la colonne **Numéro**, entrez le numéro CFDA.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="9fd2e-125">Appuyez sur la touche **Tabulation**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="9fd2e-126">Dans la colonne **Description**, tapez le titre CFDA.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="9fd2e-127">Appuyez sur la touche **Tabulation**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="9fd2e-128">Facultatif : dans le champ **Cluster du programme**, ajoutez le cluster CFDA approprié.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="9fd2e-129">Sélectionnez **Enregistrer** pour appliquer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="9fd2e-130">Mettre en place des subventions à déclarer pour la demande de Programme des dépenses des subventions fédérales</span><span class="sxs-lookup"><span data-stu-id="9fd2e-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="9fd2e-131">Accédez à **Gestion de projet et comptabilité \> Subventions \> Subventions** et sélectionnez une subvention existante.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="9fd2e-132">Sur le raccourci **Configurer**, dans le champ **Catalogue d’assistance nationale fédérale (CFDA)**, attribuez le numéro CFDA.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="9fd2e-133">Le numéro CFDA sur la subvention détermine le cluster CFDA pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="9fd2e-134">Sur le raccourci **Informations de contact**, entrez les informations relatives au donateur en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9fd2e-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="9fd2e-135">Dans le champ **Client subventionné**, saisissez le client responsable de la subvention.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="9fd2e-136">Pour une subvention existante, ces informations peuvent déjà être saisies.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="9fd2e-137">Indiquez si le client subventionné est le donateur.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="9fd2e-138">Si le client subventionné est le donateur, ne cochez pas la case **Intermédiaire**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="9fd2e-139">Si un autre client est le donateur et que le client subventionné est responsable des dépenses et du suivi de l'argent, cochez la case **Intermédiaire**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="9fd2e-140">Si vous avez coché la case **Intermédiaire** à l'étape précédente, dans le champ **Organisme donateur**, entrez le client qui a fourni la subvention.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="9fd2e-141">L'organisme donateur et le client de la subvention ne peuvent pas être le même client.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="9fd2e-142">Voici un exemple de subvention avec intermédiaire :</span><span class="sxs-lookup"><span data-stu-id="9fd2e-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="9fd2e-143">Le gouvernement fédéral a financé un projet d'infrastructure pour un État.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="9fd2e-144">Le gouvernement fédéral a donné l'argent à dépenser à l'État.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="9fd2e-145">Dans ce cas, le gouvernement fédéral est l'organisme donateur et l'État est le client subventionné.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="9fd2e-146">Lorsque vous activez la fonction pour la première fois, les numéros CFDA initiaux seront renseignés avec les numéros existants sur les subventions.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="9fd2e-147">Exclure les subventions des rapports SEFA en fonction du type de subvention</span><span class="sxs-lookup"><span data-stu-id="9fd2e-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="9fd2e-148">Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Types de subvention**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="9fd2e-149">Sur le raccourci **Informations par défaut**, cochez la case **Exclure du Programme des dépenses des subventions fédérales**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="9fd2e-150">Sélectionnez **Enregistrer** pour appliquer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="9fd2e-151">Exécuter la demande de Programme des dépenses des subventions fédérales</span><span class="sxs-lookup"><span data-stu-id="9fd2e-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="9fd2e-152">Accédez à **Gestion de projet et comptabilité \> Demandes et rapports \> Demande de subvention \> Programme des dépenses des subventions fédérales**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="9fd2e-153">Dans la section **Paramètres**, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fd2e-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="9fd2e-154">Dans le champ **Intervalle de dates**, sélectionnez le code de l'intervalle de dates.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="9fd2e-155">Alternativement, dans les champs **Date de début** et **Date de fin**, définissez l'intervalle de dates.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="9fd2e-156">Facultatif : pour inclure uniquement les transactions facturées en tant que revenus dans la demande, définissez l'option **Inclure uniquement les revenus facturés** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="9fd2e-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="9fd2e-157">Colonnes</span><span class="sxs-lookup"><span data-stu-id="9fd2e-157">Columns</span></span>

<span data-ttu-id="9fd2e-158">La demande de Programme des dépenses des subventions fédérales comprend les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fd2e-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="9fd2e-159">Nom du cluster du Catalogue d'assistance nationale fédérale (CFDA)</span><span class="sxs-lookup"><span data-stu-id="9fd2e-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="9fd2e-160">Organisme donateur</span><span class="sxs-lookup"><span data-stu-id="9fd2e-160">Grantor agency</span></span>
- <span data-ttu-id="9fd2e-161">Organisme intermédiaire</span><span class="sxs-lookup"><span data-stu-id="9fd2e-161">Pass-through agency</span></span>
- <span data-ttu-id="9fd2e-162">Nom de la subvention</span><span class="sxs-lookup"><span data-stu-id="9fd2e-162">Grant name</span></span>
- <span data-ttu-id="9fd2e-163">ID de subvention</span><span class="sxs-lookup"><span data-stu-id="9fd2e-163">Grant ID</span></span>
- <span data-ttu-id="9fd2e-164">ID de l'application de la subvention</span><span class="sxs-lookup"><span data-stu-id="9fd2e-164">Grant application ID</span></span>
- <span data-ttu-id="9fd2e-165">Catalogue d'assistance nationale fédérale (CFDA)</span><span class="sxs-lookup"><span data-stu-id="9fd2e-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="9fd2e-166">Reçus</span><span class="sxs-lookup"><span data-stu-id="9fd2e-166">Receipts</span></span>
- <span data-ttu-id="9fd2e-167">Dépenses</span><span class="sxs-lookup"><span data-stu-id="9fd2e-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]