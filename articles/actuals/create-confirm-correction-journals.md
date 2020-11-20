---
title: Créer et confirmer des journaux de correction
description: Cette rubrique donne des informations sur la création et la confirmation d’un journal de correction.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127745"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="8787a-103">Créer et confirmer des journaux de correction</span><span class="sxs-lookup"><span data-stu-id="8787a-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="8787a-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="8787a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8787a-105">Il peut arriver qu’une entrée de temps ou de dépense soit mal saisie.</span><span class="sxs-lookup"><span data-stu-id="8787a-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="8787a-106">Un consultant peut par exemple sélectionner la mauvaise date lors de la création d’une entrée de temps ou transposer les chiffres lors de la saisie d’une dépense.</span><span class="sxs-lookup"><span data-stu-id="8787a-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="8787a-107">Si un consultant ne peut pas mettre à jour les entrées soumises, un administrateur peut directement corriger l’entrée pour un projet.</span><span class="sxs-lookup"><span data-stu-id="8787a-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="8787a-108">Pour effectuer les procédures de cette rubrique, vous aurez besoin des autorisations Administrateur.</span><span class="sxs-lookup"><span data-stu-id="8787a-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="8787a-109">Corriger les entrées d’heure approuvées</span><span class="sxs-lookup"><span data-stu-id="8787a-109">Correct approved time entries</span></span>     

<span data-ttu-id="8787a-110">Effectuez les étapes suivantes pour corriger des entrées de temps individuellement ou en masse pour un projet.</span><span class="sxs-lookup"><span data-stu-id="8787a-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="8787a-111">Dans la zone **Ventes**, sélectionnez **Transactions**, puis **Heure approuvée**.</span><span class="sxs-lookup"><span data-stu-id="8787a-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="8787a-112">Dans la liste **Heure approuvée**, localisez et sélectionnez une ou plusieurs entrées d’heure approuvées à corriger.</span><span class="sxs-lookup"><span data-stu-id="8787a-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="8787a-113">Vous pouvez utiliser le filtre pour localiser les entrées associées.</span><span class="sxs-lookup"><span data-stu-id="8787a-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="8787a-114">Par exemple, vous pouvez filtrer sur un ID de projet et sélectionner toutes les entrées de temps approuvées ayant cet ID de projet.</span><span class="sxs-lookup"><span data-stu-id="8787a-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="8787a-115">Sélectionnez **Corriger les entrées**.</span><span class="sxs-lookup"><span data-stu-id="8787a-115">Select **Correct entries**.</span></span> <span data-ttu-id="8787a-116">Un nouveau journal de correction est automatiquement créé, avec le type **Correction de temps** attribué.</span><span class="sxs-lookup"><span data-stu-id="8787a-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="8787a-117">Les entrées que vous avez sélectionnées sont ajoutées au journal.</span><span class="sxs-lookup"><span data-stu-id="8787a-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="8787a-118">Sur la page **Nouveau journal**, entrez une **Description** pour votre journal de correction, puis sélectionnez l’onglet **Corrections d’entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="8787a-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="8787a-119">Dans la section **Nouvelles valeurs pour les entrées des temps**, mettez à jour les champs avec les informations correctes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8787a-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="8787a-120">Par exemple, vous pouvez modifier le projet affecté ou la ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="8787a-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="8787a-121">Sélectionnez **Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="8787a-121">Select **Preview**.</span></span> <span data-ttu-id="8787a-122">Sélectionnez **OK** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8787a-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="8787a-123">Sur l’onglet **Lignes de journal**, vous pouvez afficher la liste des valeurs réelles d’origine liées aux entrées de temps sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées.</span><span class="sxs-lookup"><span data-stu-id="8787a-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="8787a-124">Si des corrections supplémentaires doivent être apportées, répétez les étapes 5 et 6.</span><span class="sxs-lookup"><span data-stu-id="8787a-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="8787a-125">Tous les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les entrées des temps**.</span><span class="sxs-lookup"><span data-stu-id="8787a-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="8787a-126">Si les corrections sont correctes, sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="8787a-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="8787a-127">Sélectionnez **OK** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8787a-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="8787a-128">Revenez dans la zone **Ventes** et sélectionnez **Projets**, puis ouvrez le projet pour lequel vous venez de mettre à jour les entrées d’heure.</span><span class="sxs-lookup"><span data-stu-id="8787a-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="8787a-129">Sur la page **Projets**, dans l’onglet **Chiffres réels**, affichez les modifications que vous avez apportées.</span><span class="sxs-lookup"><span data-stu-id="8787a-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="8787a-130">Si l’onglet **Chiffres réels** n’est pas visible, sélectionnez **Association** > **Chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="8787a-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="8787a-131">Dans la liste **Vue associée Chiffre réel**, vous pouvez voir que les entrées d’heure d’origine qui ont été annulées sont toujours répertoriées, tout comme les entrées d’heure corrigées correspondantes.</span><span class="sxs-lookup"><span data-stu-id="8787a-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="8787a-132">Par exemple, dans le graphique suivant, deux éléments de ligne dont la quantité est 8,00 ont des débits répertoriés dans la colonne Montant.</span><span class="sxs-lookup"><span data-stu-id="8787a-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="8787a-133">En outre, deux éléments de ligne dont la quantité est -8,00 indiquent des montants crédités dans la colonne Montant.</span><span class="sxs-lookup"><span data-stu-id="8787a-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="8787a-134">Ces corrections ramènent la quantité à zéro.</span><span class="sxs-lookup"><span data-stu-id="8787a-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="8787a-135">Corriger les entrées de dépense approuvées</span><span class="sxs-lookup"><span data-stu-id="8787a-135">Correct approved expense entries</span></span>

<span data-ttu-id="8787a-136">Effectuez les étapes suivantes pour corriger une ou plusieurs entrées de dépense.</span><span class="sxs-lookup"><span data-stu-id="8787a-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="8787a-137">Dans la zone **Ventes** du volet de navigation de gauche, sous **Transactions**, sélectionnez **Dépenses approuvées**.</span><span class="sxs-lookup"><span data-stu-id="8787a-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="8787a-138">Dans la liste **Dépenses approuvées**, sélectionnez le projet que vous souhaitez corriger, puis sélectionnez **Corriger les entrées**.</span><span class="sxs-lookup"><span data-stu-id="8787a-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="8787a-139">Un nouveau journal de correction est automatiquement créé, avec le type **Correction de dépenses** attribué.</span><span class="sxs-lookup"><span data-stu-id="8787a-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="8787a-140">Sur la page **Nouveau journal**, entrez une **Description** pour la correction, et sur l’onglet **Correction des dépenses** dans la section **Nouvelles valeurs pour les dépenses**, sélectionnez les champs de données à corriger pour les lignes de dépenses sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8787a-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="8787a-141">Par exemple, vous pouvez affecter la dépense à un autre **Projet** ou corriger la **Catégorie de dépense**, la **Date de dépense**, ou la **Ressource réservable**.</span><span class="sxs-lookup"><span data-stu-id="8787a-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="8787a-142">Sélectionnez **Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="8787a-142">Select **Preview**.</span></span> <span data-ttu-id="8787a-143">Sélectionnez **OK** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8787a-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="8787a-144">Vérifiez les corrections sur l’onglet **Lignes de journal**. Vous pouvez afficher la liste des valeurs réelles d’origine liées aux entrées de dépense sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées.</span><span class="sxs-lookup"><span data-stu-id="8787a-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="8787a-145">Si les corrections sont correctes, sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="8787a-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="8787a-146">Sélectionnez **OK** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8787a-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="8787a-147">Si les valeurs ne s’affichent pas comme prévu, sélectionnez **Annuler** pour revenir à la liste **Dépenses approuvées**.</span><span class="sxs-lookup"><span data-stu-id="8787a-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="8787a-148">Répétez les étapes 2 et 5.</span><span class="sxs-lookup"><span data-stu-id="8787a-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="8787a-149">Les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les dépenses**.</span><span class="sxs-lookup"><span data-stu-id="8787a-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="8787a-150">Après avoir confirmé le journal de correction, revenez au projet ou aux projets que vous avez mis à jour pour afficher vos modifications.</span><span class="sxs-lookup"><span data-stu-id="8787a-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="8787a-151">Dans la page du projet, sur l’onglet **Chiffres réels**, passez en revue **Vue associée Chiffre réel**.</span><span class="sxs-lookup"><span data-stu-id="8787a-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="8787a-152">Les entrées originales et les entrées corrigées sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="8787a-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="8787a-153">Le graphique suivant montre les montants d’entrée des dépenses d’origine et ceux des dépenses corrigées correspondants.</span><span class="sxs-lookup"><span data-stu-id="8787a-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


