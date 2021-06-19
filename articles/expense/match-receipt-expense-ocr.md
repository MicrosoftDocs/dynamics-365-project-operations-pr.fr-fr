---
title: Capturer un reçu à l’aide d’OCR
description: Cette rubrique fournit des informations sur le traitement de la reconnaissance optique de caractères (OCR) pour les reçus.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c7fa8a805acbf7c75edd49c4c49aa159493f525
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002008"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="493db-103">Capturer un reçu à l’aide d’OCR</span><span class="sxs-lookup"><span data-stu-id="493db-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="493db-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="493db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="493db-105">La saisie des dépenses a été améliorée grâce à l’introduction du traitement de reconnaissance optique de caractères (OCR) pour les reçus.</span><span class="sxs-lookup"><span data-stu-id="493db-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="493db-106">Cette fonctionnalité est conçue pour améliorer l’expérience utilisateur lors de la création de notes de frais.</span><span class="sxs-lookup"><span data-stu-id="493db-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="493db-107">Fonctionnalités clés</span><span class="sxs-lookup"><span data-stu-id="493db-107">Key features</span></span>

- <span data-ttu-id="493db-108">Le système extrait le nom du prestataire, la date et le montant total des reçus.</span><span class="sxs-lookup"><span data-stu-id="493db-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="493db-109">Le système essaiera de faire correspondre les reçus non joints aux transactions de dépenses non jointes.</span><span class="sxs-lookup"><span data-stu-id="493db-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="493db-110">Vous pouvez créer des transactions de dépenses saisies manuellement à partir des reçus.</span><span class="sxs-lookup"><span data-stu-id="493db-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="493db-111">Joindre des reçus à une note de frais</span><span class="sxs-lookup"><span data-stu-id="493db-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="493db-112">Pour joindre automatiquement des reçus qui incluent des transactions par carte de crédit lors de la création d’une note de frais, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="493db-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="493db-113">Ouvrez l’espace de travail **Gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="493db-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="493db-114">Vérifiez que l’onglet **Reçus** contient bien des reçus non joints.</span><span class="sxs-lookup"><span data-stu-id="493db-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="493db-115">Vous pouvez également télécharger des reçus sur l’onglet **Reçus**.</span><span class="sxs-lookup"><span data-stu-id="493db-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="493db-116">Vérifiez que l’onglet **Dépenses** contient bien des dépenses non jointes.</span><span class="sxs-lookup"><span data-stu-id="493db-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="493db-117">En règle générale, l’administrateur des dépenses importe ces dépenses à partir d’un fournisseur de cartes de crédit.</span><span class="sxs-lookup"><span data-stu-id="493db-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="493db-118">Sélectionnez **Nouvelle note de frais**.</span><span class="sxs-lookup"><span data-stu-id="493db-118">Select **New expense report**.</span></span> <span data-ttu-id="493db-119">Notez que vous pouvez désormais inclure les dépenses et les reçus également lorsque vous créez une note de frais.</span><span class="sxs-lookup"><span data-stu-id="493db-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="493db-120">Si vous ajoutez à la fois des dépenses et des reçus, un rapprochement automatique des reçus et des dépenses est déclenché.</span><span class="sxs-lookup"><span data-stu-id="493db-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="493db-121">Créer ou faire correspondre des reçus à une note de frais</span><span class="sxs-lookup"><span data-stu-id="493db-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="493db-122">Pour créer une dépense ou faire correspondre une dépense à partir d’un reçu, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="493db-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="493db-123">Sur une note de frais, sur l’onglet **Reçus**, joignez un reçu en sélectionnant **Ajouter des reçus**.</span><span class="sxs-lookup"><span data-stu-id="493db-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="493db-124">Sous l’image téléchargée du reçu, notez les options **Créer** et **Faire correspondre**.</span><span class="sxs-lookup"><span data-stu-id="493db-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="493db-125">Sélectionnez **Créer** pour créer une transaction de dépense saisie manuellement et remplir les valeurs extraites du reçu.</span><span class="sxs-lookup"><span data-stu-id="493db-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="493db-126">Si vous sélectionnez **Faire correspondre**, le système essaie de faire correspondre une dépense existante au reçu.</span><span class="sxs-lookup"><span data-stu-id="493db-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="493db-127">Installation</span><span class="sxs-lookup"><span data-stu-id="493db-127">Installation</span></span>

<span data-ttu-id="493db-128">Pour utiliser ces fonctionnalités avancées de gestion des dépenses, installez le complément Service de gestion des dépenses pour Microsoft Dynamics 365 Finance et activez les fonctionnalités dans votre instance.</span><span class="sxs-lookup"><span data-stu-id="493db-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="493db-129">Vous pouvez accéder au complément depuis votre projet dans Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="493db-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="493db-130">Connectez-vous à LCS et ouvrez l’environnement souhaité.</span><span class="sxs-lookup"><span data-stu-id="493db-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="493db-131">Accédez à **Télécharger avec informations détaillées**.</span><span class="sxs-lookup"><span data-stu-id="493db-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="493db-132">Sélectionnez **Maintenir à jour**, ou faites défiler vers le bas jusqu’au raccourci **Compléments d’environnement**.</span><span class="sxs-lookup"><span data-stu-id="493db-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="493db-133">Sélectionnez **Installez un nouveau complément**.</span><span class="sxs-lookup"><span data-stu-id="493db-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="493db-134">Sélectionnez **Service de gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="493db-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="493db-135">Suivez le guide d’installation et acceptez les termes et conditions.</span><span class="sxs-lookup"><span data-stu-id="493db-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="493db-136">Sélectionnez **Installer**.</span><span class="sxs-lookup"><span data-stu-id="493db-136">Select **Install**.</span></span>

<span data-ttu-id="493db-137">Dans l’espace de travail **Gestion des fonctionnalités**, activez les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="493db-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="493db-138">Notes de frais réinventées</span><span class="sxs-lookup"><span data-stu-id="493db-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="493db-139">Correspondance automatique et création de dépenses à partir d’un reçu</span><span class="sxs-lookup"><span data-stu-id="493db-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="493db-140">Lorsque vous activez ces fonctionnalités, les actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="493db-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="493db-141">L’espace de travail **Gestion des dépenses** existant est remplacé par le nouvel espace de travail.</span><span class="sxs-lookup"><span data-stu-id="493db-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="493db-142">Un nouvel élément de menu pour la visibilité des champs de dépenses est ajouté.</span><span class="sxs-lookup"><span data-stu-id="493db-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="493db-143">Vous pouvez toujours ouvrir l’ancienne page **Notes de frais** en allant dans **Gestion des dépenses> Mes dépenses> Notes de frais**.</span><span class="sxs-lookup"><span data-stu-id="493db-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="493db-144">Les workflows et toutes les approbations vous dirigent toujours vers la page des notes de frais existantes.</span><span class="sxs-lookup"><span data-stu-id="493db-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="493db-145">Les reçus seront traités via Microsoft Azure Cognitive Services et les métadonnées seront extraites et ajoutées.</span><span class="sxs-lookup"><span data-stu-id="493db-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="493db-146">Une option est ajoutée, elle vous permet de créer une note de frais qui comprend des reçus non joints mis en correspondance.</span><span class="sxs-lookup"><span data-stu-id="493db-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="493db-147">Une option ajoutée aux notes de frais vous permet de créer une ligne de dépenses à partir d’un reçu ou de tenter de faire correspondre un reçu existant à une ligne de dépenses existante.</span><span class="sxs-lookup"><span data-stu-id="493db-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="493db-148">Forums aux questions</span><span class="sxs-lookup"><span data-stu-id="493db-148">Frequently asked questions</span></span>

<span data-ttu-id="493db-149">**Microsoft utilise-t-il mes données pour ses modèles ?**</span><span class="sxs-lookup"><span data-stu-id="493db-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="493db-150">Non, Microsoft a créé un modèle général de Machine Learning pour son service de traitement des reçus.</span><span class="sxs-lookup"><span data-stu-id="493db-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="493db-151">Ce modèle n’est pas basé sur les reçus que vous téléchargez.</span><span class="sxs-lookup"><span data-stu-id="493db-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="493db-152">**Où cette fonctionnalité est-elle disponible et traitée ?**</span><span class="sxs-lookup"><span data-stu-id="493db-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="493db-153">Actuellement, elle est prise en charge aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="493db-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="493db-154">**Où vont mes reçus ?**</span><span class="sxs-lookup"><span data-stu-id="493db-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="493db-155">Finance contactera Cognitive Services pour extraire des données du champ.</span><span class="sxs-lookup"><span data-stu-id="493db-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="493db-156">Cognitive Services conservera une copie de votre reçu pendant 24 heures maximum pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="493db-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="493db-157">Une fois le traitement terminé, Cognitive Services supprimera le reçu.</span><span class="sxs-lookup"><span data-stu-id="493db-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="493db-158">Les reçus sont toujours stockés dans Finance.</span><span class="sxs-lookup"><span data-stu-id="493db-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="493db-159">Pour plus d’informations, consultez [Activer la compréhension des reçus avec la nouvelle fonctionnalité de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="493db-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
