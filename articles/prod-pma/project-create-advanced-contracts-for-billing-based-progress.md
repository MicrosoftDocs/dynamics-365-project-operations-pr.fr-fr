---
title: Créer des contrats avancés pour la facturation selon la progression
description: Cette rubrique explique comment créer des contrats de projet afin que vous puissiez générer des factures pour les clients, en fonction d’un pourcentage du travail terminé.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999668"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="11ba0-103">Créer des contrats avancés pour la facturation selon la progression</span><span class="sxs-lookup"><span data-stu-id="11ba0-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="11ba0-104">Cette rubrique explique comment créer des contrats de projet afin que vous puissiez créer des factures pour les clients, en fonction d’un pourcentage du travail terminé.</span><span class="sxs-lookup"><span data-stu-id="11ba0-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="11ba0-105">Les montants des factures sont automatiquement calculés pour les catégories de budget de travail que vous définissez pour un projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="11ba0-106">Le délai de facturation est défini lorsque vous négociez le contrat de projet avec le client.</span><span class="sxs-lookup"><span data-stu-id="11ba0-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="11ba0-107">Utilisez les procédures de cette rubrique pour configurer un contrat, un projet associé et les règles de facturation qui calculent les montants de facture pour les catégories de budget de travail que vous définissez pour le projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="11ba0-108">Une fois que vous avez créé le contrat et le projet, vous pouvez configurer les détails du projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="11ba0-109">Par exemple, vous pouvez définir des activités et affecter des collaborateurs au projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="11ba0-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="11ba0-110">Example</span></span>

<span data-ttu-id="11ba0-111">Votre organisation est une entreprise de développement de logiciels.</span><span class="sxs-lookup"><span data-stu-id="11ba0-111">Your organization is a software development firm.</span></span> <span data-ttu-id="11ba0-112">Vous acceptez de développer un progiciel de comptabilité de paie pour un client pour un montant total de 20 000 dollars américains (USD).</span><span class="sxs-lookup"><span data-stu-id="11ba0-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="11ba0-113">Votre organisation accepte de facturer le client lorsque vous atteignez des pourcentages spécifiques du projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="11ba0-114">Vous configurez les catégories de projet suivantes pour le travail, afin de pouvoir les utiliser dans le processus de facturation :</span><span class="sxs-lookup"><span data-stu-id="11ba0-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="11ba0-115">Consultance</span><span class="sxs-lookup"><span data-stu-id="11ba0-115">Consulting</span></span>
- <span data-ttu-id="11ba0-116">Conception</span><span class="sxs-lookup"><span data-stu-id="11ba0-116">Design</span></span>
- <span data-ttu-id="11ba0-117">Installation</span><span class="sxs-lookup"><span data-stu-id="11ba0-117">Installation</span></span>

<span data-ttu-id="11ba0-118">Vous configurez également des règles de facturation qui calculent automatiquement les montants de facture pour le pourcentage de travail achevé pour chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="11ba0-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="11ba0-119">Le responsable du budget crée un budget pour les catégories de projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="11ba0-120">La quantité de travail achevé est automatiquement calculée en pourcentage du travail réel par rapport aux montants budgétés.</span><span class="sxs-lookup"><span data-stu-id="11ba0-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11ba0-121">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="11ba0-121">Prerequisites</span></span>

<span data-ttu-id="11ba0-122">Avant de créer un projet qui utilise des règles de facturation, vous devez configurer les séquences de numéros pour les règles de facturation et un journal des frais qui est utilisé pour valider les facturations en fonction de la progression.</span><span class="sxs-lookup"><span data-stu-id="11ba0-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="11ba0-123">Accédez à **Gestion et comptabilité des projets** \> **Configuration** \> **Paramètres de gestion et comptabilité des projets**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="11ba0-124">Sur la page **Paramètres de gestion et comptabilité des projets**, dans l’onglet **Séquences de numéros**, définissez la séquence de numéros à utiliser lors de la création des règles de facturation.</span><span class="sxs-lookup"><span data-stu-id="11ba0-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="11ba0-125">Accédez à **Gestion de projet et comptabilité** \> **Journaux** \> **Frais**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="11ba0-126">Sur la page **Journal des frais**, sélectionnez **Nouveau** et entrez le nom du journal.</span><span class="sxs-lookup"><span data-stu-id="11ba0-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="11ba0-127">Créer un contrat pour la facturation en fonction de la progression</span><span class="sxs-lookup"><span data-stu-id="11ba0-127">Create a contract for progress billings</span></span>

<span data-ttu-id="11ba0-128">Utilisez cette procédure pour créer un contrat de projet pour un projet à prix fixe.</span><span class="sxs-lookup"><span data-stu-id="11ba0-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="11ba0-129">Vous créez une facture de projet lorsque le travail terminé sur le projet atteint un pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="11ba0-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="11ba0-130">Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Contrats de projet**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="11ba0-131">Sur la page **Contrats de projet**, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="11ba0-132">Dans la boîte de dialogue **Nouveau contrat de projet**, définissez les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="11ba0-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="11ba0-133">**Nom**</span><span class="sxs-lookup"><span data-stu-id="11ba0-133">**Name**</span></span>
    - <span data-ttu-id="11ba0-134">**Type de financement**</span><span class="sxs-lookup"><span data-stu-id="11ba0-134">**Funding type**</span></span>
    - <span data-ttu-id="11ba0-135">**Source de financement**</span><span class="sxs-lookup"><span data-stu-id="11ba0-135">**Funding source**</span></span>
    - <span data-ttu-id="11ba0-136">**Devise de vente** - Par défaut, cette devise est utilisée pour les factures des clients associées au contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="11ba0-137">Cependant, vous pouvez modifier la devise de vente sur une facture client spécifique.</span><span class="sxs-lookup"><span data-stu-id="11ba0-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="11ba0-138">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-138">Select **OK**.</span></span> <span data-ttu-id="11ba0-139">Les informations sont copiées dans l’en-tête de la page **Contrats de projet**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="11ba0-140">Sur la page **Contrats de projet**, remplissez le reste des informations requises pour le projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="11ba0-141">Créer un projet pour la facturation en fonction de la progression</span><span class="sxs-lookup"><span data-stu-id="11ba0-141">Create a project for progress billings</span></span>

<span data-ttu-id="11ba0-142">Suivez ces étapes pour créer un projet et tous les sous-projets associés à un contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="11ba0-143">Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="11ba0-144">Sur la page **Tous les projets**, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="11ba0-145">Dans la boîte de dialogue **Nouveau projet**, dans le champ **Type de projet**, sélectionnez **Temps et matériel**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="11ba0-146">Sélectionnez un groupe de projets.</span><span class="sxs-lookup"><span data-stu-id="11ba0-146">Select a project group.</span></span> <span data-ttu-id="11ba0-147">Un groupe de projets définit les informations de validation pour les projets affectés au groupe.</span><span class="sxs-lookup"><span data-stu-id="11ba0-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="11ba0-148">Sélectionnez **Créer un projet**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-148">Select **Create project**.</span></span>
6. <span data-ttu-id="11ba0-149">Une fois le projet créé, définissez l’étape du projet sur **En cours**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="11ba0-150">Créer un budget pour un projet</span><span class="sxs-lookup"><span data-stu-id="11ba0-150">Create a budget for a project</span></span>

<span data-ttu-id="11ba0-151">Les catégories de budget sont utilisées pour calculer automatiquement les montants de factures pour le pourcentage de travail achevé pour chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="11ba0-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="11ba0-152">Suivez ces étapes pour créer des catégories de budget pour les coûts estimés.</span><span class="sxs-lookup"><span data-stu-id="11ba0-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="11ba0-153">Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="11ba0-154">Sur la page **Tous les projets**, sélectionnez et ouvrez le projet souhaité.</span><span class="sxs-lookup"><span data-stu-id="11ba0-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="11ba0-155">Sur la page **Projets**, dans le volet Actions, dans l’onglet **Planifier**, dans le groupe **Budget**, sélectionnez **Budget du projet**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="11ba0-156">Sur la page **Budget du projet**, entrez un coût estimé pour chaque catégorie du projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="11ba0-157">Créer des règles de facturation pour la facturation en fonction de la progression</span><span class="sxs-lookup"><span data-stu-id="11ba0-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="11ba0-158">Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Contrats de projet**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="11ba0-159">Dans la page de liste **Contrats de projets**, sélectionnez et ouvrez un contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="11ba0-160">Sur la page du contrat de projet, sur le raccourci **Règles de facturation**, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="11ba0-161">Sur la page **Règle de facturation**, dans le champ **Type de ligne**, sélectionnez **Progression**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="11ba0-162">Sur le raccourci **Détails de la ligne de règle de facturation**, dans le champ **Valeur du contrat**, saisissez la valeur totale du contrat.</span><span class="sxs-lookup"><span data-stu-id="11ba0-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="11ba0-163">Dans le champ **Catégorie**, sélectionnez la catégorie dans laquelle publier la transaction de frais.</span><span class="sxs-lookup"><span data-stu-id="11ba0-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="11ba0-164">Dans le champ **Projet**, sélectionnez le projet qui utilise cette règle de facturation.</span><span class="sxs-lookup"><span data-stu-id="11ba0-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="11ba0-165">Facultatif : affectez la règle de facturation à des projets supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="11ba0-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="11ba0-166">Sur le raccourci **Projet**, dans la section **Projets disponibles**, sélectionnez un projet, puis sélectionnez le bouton flèche droite pour ajouter le projet à la section **Projets sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="11ba0-167">Facultatif : calculez le pourcentage que le client retient des paiements sur une facture.</span><span class="sxs-lookup"><span data-stu-id="11ba0-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="11ba0-168">Sur le raccourci **Conditions de rétention des paiements**, sélectionnez la source de financement, puis, dans le champ **Pourcentage de rétention**, entrez le pourcentage de rétention.</span><span class="sxs-lookup"><span data-stu-id="11ba0-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="11ba0-169">Répétez ces étapes pour créer des règles de facturation supplémentaires pour le contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="11ba0-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]