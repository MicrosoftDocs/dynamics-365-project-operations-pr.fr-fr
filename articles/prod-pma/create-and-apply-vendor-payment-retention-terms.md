---
title: Créer et appliquer les conditions de rétention des paiements des fournisseurs
description: Cette rubrique fournit des informations sur la configuration et la gestion des conditions de rétention pour les paiements des fournisseurs.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075877"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="00ae1-103">Créer et appliquer les conditions de rétention des paiements des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="00ae1-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="00ae1-104">La configuration des conditions de rétention des paiements fournisseur pour un projet est utile lorsque votre organisation souhaite conserver une partie des paiements effectués à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="00ae1-105">Par exemple, lorsque vous souhaitez suspendre le paiement à un fournisseur jusqu'à ce que les produits livrés répondent à vos attentes.</span><span class="sxs-lookup"><span data-stu-id="00ae1-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="00ae1-106">Les conditions de rétention des paiements fournisseur peuvent être spécifiées lorsque vous négociez un contrat fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="00ae1-107">Créer les conditions de rétention des paiements des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="00ae1-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="00ae1-108">Vous pouvez saisir le pourcentage du paiement fournisseur pour la rétention et le pourcentage des montants précédemment retenus à débloquer.</span><span class="sxs-lookup"><span data-stu-id="00ae1-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="00ae1-109">Les montants sont automatiquement conservés sur les factures des fournisseurs jusqu'à ce que le contrat atteigne l'état d'achèvement spécifié.</span><span class="sxs-lookup"><span data-stu-id="00ae1-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="00ae1-110">Après avoir configuré les conditions de rétention, vous pouvez les appliquer à n'importe quel projet pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="00ae1-111">Procédez comme suit pour configurer et gérer les conditions de rétention des paiements fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="00ae1-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="00ae1-112">Accédez à **Gestion de projets et comptabilité** > **Rétention** > **Conditions de rétention des paiements fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="00ae1-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="00ae1-113">Sélectionnez **Nouveau** pour ajouter une nouvelle condition de rétention de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="00ae1-114">La valeur **ID de règle** du nouveau terme est automatiquement saisie.</span><span class="sxs-lookup"><span data-stu-id="00ae1-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="00ae1-115">Entrez une brève description dans le champ **Description** et sur le raccourci **Termes** , sélectionnez **Ajouter une ligne** pour saisir des valeurs de terme pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="00ae1-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="00ae1-116">**Pourcentage d'unités livrées**  : Saisissez un pourcentage d'achèvement pour la condition.</span><span class="sxs-lookup"><span data-stu-id="00ae1-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="00ae1-117">Les montants sont automatiquement conservés sur les factures des fournisseurs jusqu'au stade d'achèvement du projet est égal au pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="00ae1-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="00ae1-118">Par exemple, si vous entrez 50,00, les montants sont conservés jusqu'à ce que le projet soit achevé à 50 %.</span><span class="sxs-lookup"><span data-stu-id="00ae1-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="00ae1-119">**Pourcentage de conservation**  : Saisissez un pourcentage du montant de la facture fournisseur à conserver.</span><span class="sxs-lookup"><span data-stu-id="00ae1-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="00ae1-120">Par exemple, si vous entrez 10,00, 10 % du montant d'une facture fournisseur sont conservés jusqu'à ce que le projet atteigne le pourcentage d'achèvement défini dans le **champ Pourcentage d'unités livrées**.</span><span class="sxs-lookup"><span data-stu-id="00ae1-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="00ae1-121">**Pourcentage à libérer**  : Sélectionnez **Ajouter une ligne** pour saisir un pourcentage de tout montant précédemment retenu à débloquer pour le niveau d'achèvement de projet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="00ae1-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="00ae1-122">Si vous avez plusieurs jalons pour différents niveaux d'achèvement de projet, entrez une ligne de condition de rétention fournisseur distincte pour chaque règle de rétention.</span><span class="sxs-lookup"><span data-stu-id="00ae1-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="00ae1-123">Chaque ligne peut spécifier un pourcentage de rétention et un pourcentage de publication différents pour chaque niveau désigné d'achèvement de projet.</span><span class="sxs-lookup"><span data-stu-id="00ae1-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="00ae1-124">Après avoir créé les conditions de rétention pour un fournisseur, vous pouvez les appliquer à un projet.</span><span class="sxs-lookup"><span data-stu-id="00ae1-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="00ae1-125">Appliquer les conditions de rétention des fournisseurs à un projet</span><span class="sxs-lookup"><span data-stu-id="00ae1-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="00ae1-126">Accédez à **Gestion de projets et comptabilité** > **Projets** > **Tous les projets** et ouvrez un projet à partir de la page de liste des projets.</span><span class="sxs-lookup"><span data-stu-id="00ae1-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="00ae1-127">Dans le raccourci **Accords fournisseur** , cliquez sur **Ajouter une ligne**.</span><span class="sxs-lookup"><span data-stu-id="00ae1-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="00ae1-128">Dans le **champ Code compte** , sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="00ae1-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="00ae1-129">**Table**  : Les conditions de rétention des fournisseurs s'appliquent à un seul fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="00ae1-130">**Groupe**  : Les conditions de rétention des fournisseurs s'appliquent à tous les fournisseurs d'un groupe de fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="00ae1-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="00ae1-131">**Tous**  : Les conditions de rétention des fournisseurs s'appliquent à tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="00ae1-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="00ae1-132">Dans le **champ Fournisseur/Groupe de fournisseurs** , sélectionnez le fournisseur ou le groupe de fournisseurs auquel s'appliquent les conditions de rétention des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="00ae1-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="00ae1-133">Si vous avez sélectionné **Tout** à l'étape précédente, ce champ n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00ae1-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="00ae1-134">Dans le champ **Conditions de rétention des fournisseurs** , sélectionnez les conditions de conservation que vous avez créées lors de la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="00ae1-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="00ae1-135">Si le projet a également des conditions de paiement au moment du paiement (PWP) définies pour le fournisseur, entrez le pourcentage de seuil pour le projet dans le champ **Pourcentage de seuil PWP**.</span><span class="sxs-lookup"><span data-stu-id="00ae1-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="00ae1-136">Les conditions de rétention du fournisseur sont également affichées sur les bons de commande que vous créez pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="00ae1-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
