---
title: Créer une solution pour les dimensions de tarification personnalisées
description: Cette rubrique donne des informations sur la manière de créer des solutions pour les dimensions de tarification personnalisées.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010333"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="57522-103">Créer une solution pour les dimensions de tarification personnalisées</span><span class="sxs-lookup"><span data-stu-id="57522-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="57522-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="57522-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="57522-105">Tous les changements de dimension Tarification personnalisée doivent se faire dans une solution distincte.</span><span class="sxs-lookup"><span data-stu-id="57522-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="57522-106">Cette meilleure pratique importante procure la flexibilité nécessaire pour mettre à jour ou supprimer des modifications si nécessaire, elle permet une réutilisation de votre travail, et facilite le déplacement des modifications vers d’autres instances.</span><span class="sxs-lookup"><span data-stu-id="57522-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="57522-107">Après avoir apporté toutes les modifications requises, exportez cette solution en tant que solution **Gérée** et importez-la dans d’autres instances en vue d’une réutilisation.</span><span class="sxs-lookup"><span data-stu-id="57522-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="57522-108">Créer une solution pour les dimensions de tarification personnalisées</span><span class="sxs-lookup"><span data-stu-id="57522-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="57522-109">Sélectionnez **Paramètres** > **Solutions**, puis sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="57522-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="57522-110">Nommez la solution,*dimensions de tarification <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="57522-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="57522-111">Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="57522-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Création d’une solution de dimension de tarification personnalisée](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="57522-113">Ajouter tous les entités requises et les composants associés à la solution Dimension Tarification</span><span class="sxs-lookup"><span data-stu-id="57522-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="57522-114">Ajoutez les entités Project Service suivantes à votre solution de tarification pour apporter des modifications de schéma importantes à la solution de tarification.</span><span class="sxs-lookup"><span data-stu-id="57522-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="57522-115">Une fois cette procédure terminée, les entités reconnaissent les nouvelles dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="57522-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="57522-116">Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **<*nom de votre organisation*> dimensions de tarification**.</span><span class="sxs-lookup"><span data-stu-id="57522-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="57522-117">Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.</span><span class="sxs-lookup"><span data-stu-id="57522-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="57522-118">Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :</span><span class="sxs-lookup"><span data-stu-id="57522-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="57522-119">**Réel**</span><span class="sxs-lookup"><span data-stu-id="57522-119">**Actual**</span></span>
   - <span data-ttu-id="57522-120">**Ressource pouvant être réservée**</span><span class="sxs-lookup"><span data-stu-id="57522-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="57522-121">**Ligne d’estimation**</span><span class="sxs-lookup"><span data-stu-id="57522-121">**Estimate Line**</span></span>
   - <span data-ttu-id="57522-122">**Tâche du projet**</span><span class="sxs-lookup"><span data-stu-id="57522-122">**Project Task**</span></span>
   - <span data-ttu-id="57522-123">**Détail de la ligne de facture**</span><span class="sxs-lookup"><span data-stu-id="57522-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="57522-124">**Ligne de journal**</span><span class="sxs-lookup"><span data-stu-id="57522-124">**Journal Line**</span></span>
   - <span data-ttu-id="57522-125">**Détail de la ligne de contrat du projet**</span><span class="sxs-lookup"><span data-stu-id="57522-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="57522-126">**Membre de l’équipe du projet**</span><span class="sxs-lookup"><span data-stu-id="57522-126">**Project Team Member**</span></span>
   - <span data-ttu-id="57522-127">**Détail de la ligne de devis**</span><span class="sxs-lookup"><span data-stu-id="57522-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="57522-128">**Majoration du prix du rôle**</span><span class="sxs-lookup"><span data-stu-id="57522-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="57522-129">**Prix du rôle**</span><span class="sxs-lookup"><span data-stu-id="57522-129">**Role Price**</span></span>
   - <span data-ttu-id="57522-130">**Entrée de temps**</span><span class="sxs-lookup"><span data-stu-id="57522-130">**Time Entry**</span></span>
 
   ![Ajouter des entités existantes à la solution de dimensions de tarification personnalisée](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="57522-132">Pour chaque entité, examinez les composants ajoutés et la liste finale des actifs d’entité pour chaque entité.</span><span class="sxs-lookup"><span data-stu-id="57522-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="57522-133">Incluez tous les formulaires et toutes les vues pour chacune des entités sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="57522-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entités ajoutées](./media/solution-component-selection.png)


5.  <span data-ttu-id="57522-135">Lorsque vous êtes invité à inclure des entités dépendantes pour les entités sélectionnées, sélectionnez **Non, ne pas inclure les composants requis.**</span><span class="sxs-lookup"><span data-stu-id="57522-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inclure des entités dépendantes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]