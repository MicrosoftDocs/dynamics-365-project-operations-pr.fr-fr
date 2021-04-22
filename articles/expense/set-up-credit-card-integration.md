---
title: Configurer l’intégration des cartes de crédit
description: Cette rubrique explique comment utiliser les transactions par carte de crédit liées aux dépenses.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866680"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="fda86-103">Configurer l’intégration des cartes de crédit</span><span class="sxs-lookup"><span data-stu-id="fda86-103">Set up credit card integration</span></span>

<span data-ttu-id="fda86-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="fda86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fda86-105">Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d’être automatiquement importées selon un calendrier récurrent.</span><span class="sxs-lookup"><span data-stu-id="fda86-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="fda86-106">Les transactions peuvent également être importées manuellement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="fda86-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="fda86-107">Les transactions par carte de crédit sont importées via l’entité de données des transactions par carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="fda86-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="fda86-108">Importer des transactions par carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fda86-108">Import credit card transactions</span></span>

<span data-ttu-id="fda86-109">Pour importer des transactions par carte de crédit, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fda86-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="fda86-110">Sur la page **Transactions par carte de crédit**, sélectionnez **Importer des transactions**.</span><span class="sxs-lookup"><span data-stu-id="fda86-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="fda86-111">Si vous ouvrez la gestion des données pour la première fois, le système doit mettre à jour la liste des entités de données avant de pouvoir continuer.</span><span class="sxs-lookup"><span data-stu-id="fda86-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="fda86-112">Dans le champ **Nom**, entrez une description unique pour la tâche d’importation.</span><span class="sxs-lookup"><span data-stu-id="fda86-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="fda86-113">Dans le champ **Format des données source**, sélectionnez le format du fichier contenant les transactions par carte de crédit à importer.</span><span class="sxs-lookup"><span data-stu-id="fda86-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="fda86-114">Sélectionnez **Télécharger**, puis recherchez et sélectionnez le fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="fda86-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="fda86-115">Une fois le fichier téléchargé, validez le mappage du fichier de transaction par carte de crédit et les colonnes de l’entité de données de transactions par carte de crédit en sélectionnant le lien **Afficher la mise en correspondance** sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="fda86-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="fda86-116">S’il y a des erreurs de mappage ou si vous devez modifier le mappage, effectuez les changements de mappage à partir de l’onglet **Visualisation cartographique** ou de l’onglet **Détails de la mise en correspondance**.</span><span class="sxs-lookup"><span data-stu-id="fda86-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="fda86-117">Pour automatiser les transactions par carte de crédit, sélectionnez **Créer une tâche de données répétitive**.</span><span class="sxs-lookup"><span data-stu-id="fda86-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="fda86-118">Vous pouvez ensuite définir la récurrence qui définit la fréquence à laquelle les transactions par carte de crédit doivent être importées.</span><span class="sxs-lookup"><span data-stu-id="fda86-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="fda86-119">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="fda86-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="fda86-120">Pour importer le fichier sélectionné à présent, sélectionnez **Importer**.</span><span class="sxs-lookup"><span data-stu-id="fda86-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="fda86-121">Si des erreurs se produisent lors de l’importation, vous pouvez afficher le journal d’exécution ou les données intermédiaires pour voir les erreurs que vous devez corriger pour garantir une importation réussie.</span><span class="sxs-lookup"><span data-stu-id="fda86-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="fda86-122">Si vous devez importer plusieurs formats de fichier, vous devez créer des tâches d’importation distinctes pour chaque type de format.</span><span class="sxs-lookup"><span data-stu-id="fda86-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="fda86-123">Réaffecter les transactions par carte de crédit pour les employés licenciés</span><span class="sxs-lookup"><span data-stu-id="fda86-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="fda86-124">Lorsqu’un employé est licencié, son compte Services de domaine Active Directory (AD DS) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="fda86-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="fda86-125">Cependant, il peut y avoir des transactions par carte de crédit actives qui doivent encore être passées en charges et remboursées.</span><span class="sxs-lookup"><span data-stu-id="fda86-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="fda86-126">Sur la page **Transactions par carte de crédit**, vous pouvez réaffecter l’employé pour toute transaction par carte de crédit pour laquelle l’employé associé ne fait plus partie de la société.</span><span class="sxs-lookup"><span data-stu-id="fda86-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="fda86-127">Sélectionnez une ou plusieurs transactions par carte de crédit, puis sélectionnez **Réaffecter les transactions**.</span><span class="sxs-lookup"><span data-stu-id="fda86-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="fda86-128">Vous pouvez ensuite sélectionner un autre employé auquel affecter les transactions par carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="fda86-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="fda86-129">Une fois que les transactions par carte de crédit ont été réaffectées, elles peuvent être sélectionnées pour une note de frais et payées selon le processus habituel de remboursement des notes de frais.</span><span class="sxs-lookup"><span data-stu-id="fda86-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="fda86-130">Supprimer les transactions par carte de crédit</span><span class="sxs-lookup"><span data-stu-id="fda86-130">Delete credit card transactions</span></span> 

<span data-ttu-id="fda86-131">Parfois, après l’importation de transactions par carte de crédit, certaines transactions peuvent devoir être supprimées.</span><span class="sxs-lookup"><span data-stu-id="fda86-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="fda86-132">Cela peut être dû au fait que des transactions sont en double ou que les données peuvent ne pas être exactes.</span><span class="sxs-lookup"><span data-stu-id="fda86-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="fda86-133">Les administrateurs peuvent utiliser la fonctionnalité **Supprimer les transactions par carte de crédit** pour sélectionner et supprimer les transactions par carte de crédit **qui ne sont pas attachées** à une note de frais.</span><span class="sxs-lookup"><span data-stu-id="fda86-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="fda86-134">Accédez à **Tâches périodiques** > **Supprimer les transactions par carte de crédit**.</span><span class="sxs-lookup"><span data-stu-id="fda86-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="fda86-135">Sélectionnez **Filtrer** et fournissez des informations pour identifier les enregistrements à inclure.</span><span class="sxs-lookup"><span data-stu-id="fda86-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="fda86-136">Sélectionnez **OK** pour supprimer les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="fda86-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
