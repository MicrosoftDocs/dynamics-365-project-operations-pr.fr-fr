---
title: Importer et gérer les transactions par carte de crédit
description: Cette rubrique explique comment importer et gérer les transactions par carte de crédit liées aux dépenses. Ces transactions peuvent être configurées de manière à être automatiquement importées selon un calendrier récurrent, ou elles peuvent être importées manuellement si nécessaire.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951071"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="487d4-104">Importer et gérer les transactions par carte de crédit</span><span class="sxs-lookup"><span data-stu-id="487d4-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="487d4-105">Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d'être automatiquement importées selon un calendrier récurrent.</span><span class="sxs-lookup"><span data-stu-id="487d4-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="487d4-106">Les transactions peuvent également être importées manuellement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="487d4-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="487d4-107">Les transactions par carte de crédit sont importées via l'entité de données Transactions par carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="487d4-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="487d4-108">Pour plus d'informations sur les entités de données, voir [Entités de données](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="487d4-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="487d4-109">Importer des transactions par carte de crédit</span><span class="sxs-lookup"><span data-stu-id="487d4-109">Import credit card transactions</span></span>

1. <span data-ttu-id="487d4-110">Sur la page **Transactions par carte de crédit**, sélectionnez **Importer des transactions**.</span><span class="sxs-lookup"><span data-stu-id="487d4-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="487d4-111">Si vous ouvrez la gestion des données pour la première fois, le système doit mettre à jour la liste des entités de données avant de pouvoir continuer.</span><span class="sxs-lookup"><span data-stu-id="487d4-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="487d4-112">Dans le champ **Nom**, entrez une description unique de la tâche d’importation.</span><span class="sxs-lookup"><span data-stu-id="487d4-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="487d4-113">Dans le champ **Format des données source**, sélectionnez le format du fichier contenant les transactions par carte de crédit à importer.</span><span class="sxs-lookup"><span data-stu-id="487d4-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="487d4-114">Sélectionnez **Télécharger**, puis recherchez et sélectionnez le fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="487d4-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="487d4-115">Une fois le fichier téléchargé, validez le mappage du fichier de transaction par carte de crédit et les colonnes de l’entité de données Transactions par carte de crédit en sélectionnant le lien **Afficher la mise en correspondance** sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="487d4-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="487d4-116">S’il y a des erreurs de mappage ou si vous devez modifier le mappage, effectuez les changements de mappage à partir de l’onglet **Visualisation cartographique** ou de l’onglet **Détails de la mise en correspondance**.</span><span class="sxs-lookup"><span data-stu-id="487d4-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="487d4-117">Pour automatiser les transactions par carte de crédit, sélectionnez **Créer une tâche de données répétitive**.</span><span class="sxs-lookup"><span data-stu-id="487d4-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="487d4-118">Vous pouvez ensuite définir la récurrence qui définit la fréquence à laquelle les transactions par carte de crédit doivent être importées.</span><span class="sxs-lookup"><span data-stu-id="487d4-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="487d4-119">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="487d4-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="487d4-120">Pour importer le fichier sélectionné à présent, sélectionnez **Importer**.</span><span class="sxs-lookup"><span data-stu-id="487d4-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="487d4-121">Si des erreurs se produisent lors de l’importation, vous pouvez afficher le journal d’exécution ou les données de préparation pour voir les erreurs que vous devez corriger pour garantir la réussite de l’importation.</span><span class="sxs-lookup"><span data-stu-id="487d4-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="487d4-122">Si vous devez importer plusieurs formats de fichier, vous devez créer des travaux d’importation distincts pour chaque type de format.</span><span class="sxs-lookup"><span data-stu-id="487d4-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="487d4-123">Réaffecter les transactions par carte de crédit pour les employés licenciés</span><span class="sxs-lookup"><span data-stu-id="487d4-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="487d4-124">Lorsqu’un employé est licencié, son compte Services de domaine Active Directory (AD DS) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="487d4-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="487d4-125">Cependant, il peut y avoir des transactions par carte de crédit actives qui doivent encore être passées en charges et remboursées.</span><span class="sxs-lookup"><span data-stu-id="487d4-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="487d4-126">À partir de la page **Transactions par carte de crédit**, vous pouvez réaffecter l’employé pour toute transaction par carte de crédit associée à l’employé qui a été licencié.</span><span class="sxs-lookup"><span data-stu-id="487d4-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="487d4-127">Sélectionnez une ou plusieurs transactions par carte de crédit, puis sélectionnez **Réaffecter les transactions**.</span><span class="sxs-lookup"><span data-stu-id="487d4-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="487d4-128">Vous pouvez ensuite sélectionner un autre employé auquel affecter les transactions par carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="487d4-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="487d4-129">Une fois que les transactions par carte de crédit ont été réaffectées, elles peuvent être sélectionnées pour une note de frais et payées selon le processus habituel de remboursement des notes de frais.</span><span class="sxs-lookup"><span data-stu-id="487d4-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]