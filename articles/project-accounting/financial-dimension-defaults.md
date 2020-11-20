---
title: Valeurs par défaut d’une dimension financière
description: Cette rubrique fournit des informations sur la configuration des valeurs par défaut des dimensions financières.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131880"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="0ca5a-103">Valeurs par défaut d’une dimension financière</span><span class="sxs-lookup"><span data-stu-id="0ca5a-103">Financial dimension defaults</span></span>

<span data-ttu-id="0ca5a-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="0ca5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0ca5a-105">Dynamics 365 Project Operations utilise la structure de [Dimensions financières](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) dans Dynamics 365 Finance pour fournir des informations supplémentaires sur les transactions comptables et auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="0ca5a-106">Les dimensions financières par défaut peuvent être définies selon un client, une source de financement de projet, un jalon, une ligne de contrat de projet ou un projet.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="0ca5a-107">Définir les dimensions financières par défaut pour un client</span><span class="sxs-lookup"><span data-stu-id="0ca5a-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="0ca5a-108">Les valeurs par défaut des dimensions client sont spécifiées dans Finance.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="0ca5a-109">Effectuez les étapes suivantes pour définir les valeurs par défaut des dimensions.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="0ca5a-110">Accédez à **Comptabilité client** > **Clients** > **Tous les clients**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="0ca5a-111">Sur la page **Clients**, dans l’onglet **Dimensions financières**, définissez les valeurs de dimensions financières pour un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="0ca5a-112">Définir les dimensions financières par défaut pour des contrats de projet</span><span class="sxs-lookup"><span data-stu-id="0ca5a-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="0ca5a-113">Les contrats de projet sont créés et gérés dans Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="0ca5a-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="0ca5a-114">Les attributs comptables des contrats de projet sont définis dans le module **Gestion du projet et comptabilité** dans Finance.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="0ca5a-115">Définir les dimensions financières d’une source de financement de projet</span><span class="sxs-lookup"><span data-stu-id="0ca5a-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="0ca5a-116">Accédez à **Gestion du projet et comptabilité** > **Projets** > **Contrats de projet**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0ca5a-117">Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Contrat de projet**, sélectionnez **Afficher la comptabilité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0ca5a-118">Développez **Informations connexes** et sélectionnez l’onglet **Sources de financement**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="0ca5a-119">Définissez les valeurs par défaut d’une dimension financière.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="0ca5a-120">Notez que les dimensions financières par défaut proviennent du compte client.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="0ca5a-121">Définir les dimensions financières d’une ligne de contrat de projet</span><span class="sxs-lookup"><span data-stu-id="0ca5a-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="0ca5a-122">Accédez à **Gestion du projet et comptabilité** > **Projets** > **Contrats de projet**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0ca5a-123">Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Contrat de projet**, sélectionnez **Afficher la comptabilité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0ca5a-124">Développez **Informations connexes** et sélectionnez l’onglet **Lignes de contrat**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="0ca5a-125">Définissez les valeurs par défaut d’une dimension financière.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="0ca5a-126">Les valeurs par défaut des dimensions financières sont applicables et ne peuvent être utilisées qu’avec des lignes de contrat à prix fixe (jalon).</span><span class="sxs-lookup"><span data-stu-id="0ca5a-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="0ca5a-127">Ces valeurs par défaut sont utilisées pour les transactions de compte de projet et les lignes de facture connexes.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="0ca5a-128">Définir les dimensions financières par défaut pour des projets</span><span class="sxs-lookup"><span data-stu-id="0ca5a-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="0ca5a-129">Les projets sont créés et gérés dans CDS.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="0ca5a-130">Les attributs comptables des projets sont définis dans le module **Gestion du projet et comptabilité** dans Finance.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="0ca5a-131">Accédez à **Gestion du projet et comptabilité** > **Projets** > **Tous les projets**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="0ca5a-132">Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Projet**, sélectionnez **Afficher la comptabilité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0ca5a-133">Développez **Informations connexes** et sélectionnez l’onglet **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="0ca5a-134">Définissez les valeurs par défaut d’une dimension financière.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="0ca5a-135">Notez que ces dimensions financières par défaut proviennent du compte client.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="0ca5a-136">Si le projet est associé à une ligne de contrat ayant plusieurs clients de contrat de projet, le client principal est utilisé pour définir les valeurs par défaut des dimensions financières.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="0ca5a-137">Les dimensions financières par défaut du projet sont utilisées pour définir les valeurs par défaut de la ligne de journal des transactions de temps, de dépenses et de frais dans le **Journal d’intégration de Project Operations** et les lignes de facture de projets connexes.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
