---
title: Création de solutions personnalisées pour les dimensions Tarification
description: Cette rubrique explique comment créer une solution personnalisée lors de la création de dimensions Tarification personnalisées.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144636"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="92490-103">Création de solutions personnalisées pour les dimensions Tarification</span><span class="sxs-lookup"><span data-stu-id="92490-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="92490-104">Tous les changements de dimension Tarification personnalisée doivent se faire dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="92490-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="92490-105">Cette meilleure pratique importante procure la flexibilité nécessaire à l'avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance.</span><span class="sxs-lookup"><span data-stu-id="92490-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="92490-106">Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d’autres instances pour réutiliser votre configuration de tarification.</span><span class="sxs-lookup"><span data-stu-id="92490-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="92490-107">Sélectionnez **Paramètres** > **Solutions**, puis sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="92490-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="92490-108">Nommez la solution, **\<your organization name> dimensions tarification**, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="92490-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Création d'une solution personnalisée pour les dimensions Tarification](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="92490-110">Ajouter tous les entités requises et les composants associés à la solution Dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="92490-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="92490-111">Vous devrez ajouter les entités Project Service suivantes à votre solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="92490-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="92490-112">Exécutez la procédure ci-dessous pour apporter quelques modifications importantes au schéma dans la solution de tarification de sorte que les entités soient informées des nouvelles dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="92490-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="92490-113">Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="92490-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="92490-114">Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.</span><span class="sxs-lookup"><span data-stu-id="92490-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="92490-115">Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="92490-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="92490-116">Réel</span><span class="sxs-lookup"><span data-stu-id="92490-116">Actual</span></span>
- <span data-ttu-id="92490-117">Ressource pouvant être réservée</span><span class="sxs-lookup"><span data-stu-id="92490-117">Bookable Resource</span></span>
- <span data-ttu-id="92490-118">Ligne d'estimation</span><span class="sxs-lookup"><span data-stu-id="92490-118">Estimate Line</span></span>
- <span data-ttu-id="92490-119">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="92490-119">Project Task</span></span>
- <span data-ttu-id="92490-120">Détail de la ligne de facture</span><span class="sxs-lookup"><span data-stu-id="92490-120">Invoice Line Detail</span></span>
- <span data-ttu-id="92490-121">Ligne de journal</span><span class="sxs-lookup"><span data-stu-id="92490-121">Journal Line</span></span>
- <span data-ttu-id="92490-122">Détail de la ligne de contrat du projet</span><span class="sxs-lookup"><span data-stu-id="92490-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="92490-123">Membre de l'équipe du projet</span><span class="sxs-lookup"><span data-stu-id="92490-123">Project Team Member</span></span>
- <span data-ttu-id="92490-124">Détail de la ligne de devis</span><span class="sxs-lookup"><span data-stu-id="92490-124">Quote Line Detail</span></span>
- <span data-ttu-id="92490-125">Majoration du prix du rôle</span><span class="sxs-lookup"><span data-stu-id="92490-125">Role Price Markup</span></span>
- <span data-ttu-id="92490-126">Prix du rôle</span><span class="sxs-lookup"><span data-stu-id="92490-126">Role Price</span></span> 
- <span data-ttu-id="92490-127">Entrée de temps</span><span class="sxs-lookup"><span data-stu-id="92490-127">Time Entry</span></span> 

> ![Ajouter des entités existantes à la solution Dimensions de tarification](media/Existing-entities-to-PD-solution.png)

> ![Sélectionner les composants de solution](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="92490-130">Veillez à inclure tous les formulaires et vues pour chacune des entités sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="92490-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="92490-131">Lorsque vous êtes invité à inclure toutes les entités dépendantes des entités sélectionnées, cliquez sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="92490-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ne pas inclure tous les composants associés](media/Do-not-include-required.png)


