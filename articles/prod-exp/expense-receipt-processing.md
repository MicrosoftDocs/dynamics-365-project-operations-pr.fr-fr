---
title: Traitement des reçus de dépenses
description: Cette rubrique fournit des informations sur le traitement de la reconnaissance optique de caractères (OCR) pour les reçus. Cette fonctionnalité est conçue pour améliorer l'expérience utilisateur lors de la création de notes de frais dans Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075898"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="70824-104">Traitement des reçus de dépenses</span><span class="sxs-lookup"><span data-stu-id="70824-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70824-105">La saisie des dépenses a été améliorée grâce à l'introduction du traitement de reconnaissance optique de caractères (OCR) pour les reçus.</span><span class="sxs-lookup"><span data-stu-id="70824-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="70824-106">Cette fonctionnalité est conçue pour améliorer l'expérience utilisateur lors de la création de notes de frais.</span><span class="sxs-lookup"><span data-stu-id="70824-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="70824-107">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="70824-107">Key features</span></span>

- <span data-ttu-id="70824-108">Le nom du prestataire, la date et le montant total sont extraits des reçus.</span><span class="sxs-lookup"><span data-stu-id="70824-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="70824-109">La fonctionnalité essaie de faire correspondre les reçus non joints aux transactions de dépenses non jointes.</span><span class="sxs-lookup"><span data-stu-id="70824-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="70824-110">Les utilisateurs peuvent créer des transactions de dépenses saisies manuellement à partir des reçus.</span><span class="sxs-lookup"><span data-stu-id="70824-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="70824-111">Exemples d’utilisation</span><span class="sxs-lookup"><span data-stu-id="70824-111">Usage examples</span></span>

<span data-ttu-id="70824-112">Pour joindre automatiquement des reçus qui incluent des transactions par carte de crédit lors de la création d'une note de frais, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="70824-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="70824-113">Ouvrez l'espace de travail **Gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="70824-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="70824-114">Vérifiez que l'onglet **Reçus** contient bien des reçus non joints.</span><span class="sxs-lookup"><span data-stu-id="70824-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="70824-115">Vous pouvez également télécharger des reçus sur l'onglet **Reçus**.</span><span class="sxs-lookup"><span data-stu-id="70824-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="70824-116">Vérifiez que l'onglet **Dépenses** contient bien des dépenses non jointes.</span><span class="sxs-lookup"><span data-stu-id="70824-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="70824-117">En règle générale, l'administrateur des dépenses importe ces dépenses à partir d'un fournisseur de cartes de crédit.</span><span class="sxs-lookup"><span data-stu-id="70824-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="70824-118">Sélectionnez **Nouvelle note de frais**.</span><span class="sxs-lookup"><span data-stu-id="70824-118">Select **New expense report**.</span></span> <span data-ttu-id="70824-119">Notez que vous pouvez désormais inclure les dépenses et les reçus également lorsque vous créez une note de frais.</span><span class="sxs-lookup"><span data-stu-id="70824-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="70824-120">Si vous ajoutez à la fois des dépenses et des reçus, un rapprochement automatique des reçus et des dépenses est déclenché.</span><span class="sxs-lookup"><span data-stu-id="70824-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="70824-121">Pour créer une dépense ou faire correspondre une dépense à partir d'un reçu, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="70824-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="70824-122">Sur une note de frais, sur l'onglet **Reçus** , joignez un reçu en sélectionnant **Ajouter des reçus**.</span><span class="sxs-lookup"><span data-stu-id="70824-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="70824-123">Sous l'image téléchargée du reçu, notez les options **Créer** et **Faire correspondre**.</span><span class="sxs-lookup"><span data-stu-id="70824-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="70824-124">Sélectionnez **Créer** pour créer une transaction de dépense saisie manuellement et remplir les valeurs extraites du reçu.</span><span class="sxs-lookup"><span data-stu-id="70824-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="70824-125">Si vous sélectionnez **Faire correspondre** , le système essaie de faire correspondre une dépense existante au reçu.</span><span class="sxs-lookup"><span data-stu-id="70824-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="70824-126">Installation</span><span class="sxs-lookup"><span data-stu-id="70824-126">Installation</span></span>

<span data-ttu-id="70824-127">Cette fonction fonctionne en combinaison avec la fonction **Rapports de dépenses repensés** pour aider à simplifier l'expérience de dépenses.</span><span class="sxs-lookup"><span data-stu-id="70824-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="70824-128">Cette fonctionnalité n'est disponible que pour les environnements de niveau 2+, qui sont Sandbox et Production.</span><span class="sxs-lookup"><span data-stu-id="70824-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="70824-129">Pour utiliser ces fonctionnalités avancées de gestion des dépenses, installez le complément Service de gestion des dépenses pour Microsoft Dynamics 365 Finance et activez les fonctionnalités dans votre instance.</span><span class="sxs-lookup"><span data-stu-id="70824-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="70824-130">Vous pouvez accéder au complément depuis votre projet dans Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="70824-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="70824-131">Connectez-vous à LCS et ouvrez l'environnement souhaité.</span><span class="sxs-lookup"><span data-stu-id="70824-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="70824-132">Accédez à **Télécharger avec informations détaillées**.</span><span class="sxs-lookup"><span data-stu-id="70824-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="70824-133">Sélectionnez **Maintenir à jour** , ou faites défiler vers le bas jusqu'au raccourci **Compléments d'environnement**.</span><span class="sxs-lookup"><span data-stu-id="70824-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="70824-134">Sélectionnez **Installez un nouveau complément**.</span><span class="sxs-lookup"><span data-stu-id="70824-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="70824-135">Sélectionnez **Service de gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="70824-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="70824-136">Suivez le guide d'installation et acceptez les termes et conditions.</span><span class="sxs-lookup"><span data-stu-id="70824-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="70824-137">Sélectionnez **Installer**.</span><span class="sxs-lookup"><span data-stu-id="70824-137">Select **Install**.</span></span>

<span data-ttu-id="70824-138">Dans l'espace de travail **Gestion des fonctionnalités** , activez les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="70824-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="70824-139">Notes de frais réinventées</span><span class="sxs-lookup"><span data-stu-id="70824-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="70824-140">Correspondance automatique et création de dépenses à partir d'un reçu</span><span class="sxs-lookup"><span data-stu-id="70824-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="70824-141">Lorsque vous activez ces fonctionnalités, les actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="70824-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="70824-142">L'espace de travail **Gestion des dépenses** existant est remplacé par le nouvel espace de travail.</span><span class="sxs-lookup"><span data-stu-id="70824-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="70824-143">Un nouvel élément de menu pour la visibilité des champs de dépenses est ajouté.</span><span class="sxs-lookup"><span data-stu-id="70824-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="70824-144">Vous pouvez toujours ouvrir l'ancienne page **Notes de frais** en allant dans **Gestion des dépenses> Mes dépenses> Notes de frais**.</span><span class="sxs-lookup"><span data-stu-id="70824-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="70824-145">Les workflows et toutes les approbations vous dirigent toujours vers la page des notes de frais existantes.</span><span class="sxs-lookup"><span data-stu-id="70824-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="70824-146">Les reçus seront traités via Microsoft Azure Cognitive Services et les métadonnées seront extraites et ajoutées.</span><span class="sxs-lookup"><span data-stu-id="70824-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="70824-147">Une option est ajoutée, elle vous permet de créer une note de frais qui comprend des reçus non joints mis en correspondance.</span><span class="sxs-lookup"><span data-stu-id="70824-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="70824-148">Une option ajoutée aux notes de frais vous permet de créer une ligne de dépenses à partir d'un reçu ou de tenter de faire correspondre un reçu existant à une ligne de dépenses existante.</span><span class="sxs-lookup"><span data-stu-id="70824-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="70824-149">Pour plus d'informations sur la fonctionnalité repensée des notes de frais, voir [Notes de frais réinventées](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="70824-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="70824-150">Forums aux questions</span><span class="sxs-lookup"><span data-stu-id="70824-150">Frequently asked questions</span></span>

<span data-ttu-id="70824-151">**Microsoft utilise-t-il mes données pour ses modèles ?**</span><span class="sxs-lookup"><span data-stu-id="70824-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="70824-152">Non, Microsoft a créé un modèle général de Machine Learning pour son service de traitement des reçus.</span><span class="sxs-lookup"><span data-stu-id="70824-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="70824-153">Ce modèle n'est pas basé sur les reçus que vous téléchargez.</span><span class="sxs-lookup"><span data-stu-id="70824-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="70824-154">**Où cette fonctionnalité est-elle disponible et traitée ?**</span><span class="sxs-lookup"><span data-stu-id="70824-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="70824-155">Actuellement, elle est prise en charge aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="70824-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="70824-156">**Où vont mes reçus ?**</span><span class="sxs-lookup"><span data-stu-id="70824-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="70824-157">Finance contactera Cognitive Services pour extraire des données du champ.</span><span class="sxs-lookup"><span data-stu-id="70824-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="70824-158">Cognitive Services conservera une copie de votre reçu pendant 24 heures maximum pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="70824-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="70824-159">Une fois le traitement terminé, Cognitive Services supprimera le reçu.</span><span class="sxs-lookup"><span data-stu-id="70824-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="70824-160">Les reçus sont toujours stockés dans Finance.</span><span class="sxs-lookup"><span data-stu-id="70824-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="70824-161">Pour plus d'informations, consultez [Activer la compréhension des reçus avec la nouvelle fonctionnalité de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="70824-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
