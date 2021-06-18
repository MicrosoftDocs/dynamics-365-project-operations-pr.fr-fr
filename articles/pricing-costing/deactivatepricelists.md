---
title: Désactiver les tarifs
description: Cette rubrique explique comment désactiver ou supprimer des tarifs inutilisés ou anciens.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001333"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="470e1-103">Désactiver les tarifs</span><span class="sxs-lookup"><span data-stu-id="470e1-103">Deactivate price lists</span></span> 

<span data-ttu-id="470e1-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="470e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="470e1-105">Pour supprimer des tarifs anciens ou inutilisés de Dynamics 365 Project Operations, vous devez effectuer deux étapes.</span><span class="sxs-lookup"><span data-stu-id="470e1-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="470e1-106">Supprimez ou effacez le tarif de pages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="470e1-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="470e1-107">Désactivez ou supprimez le tarif des tarifs actifs sur la page **Tarifs**.</span><span class="sxs-lookup"><span data-stu-id="470e1-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="470e1-108">Vous devez effectuer les deux étapes pour supprimer complètement un tarif.</span><span class="sxs-lookup"><span data-stu-id="470e1-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="470e1-109">Il n’est pas suffisant d’effectuer seulement l’étape 2, qui consiste à supprimer ou désactiver directement le tarif de la vue Tarifs actifs.</span><span class="sxs-lookup"><span data-stu-id="470e1-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="470e1-110">Vous devez également supprimer l’association de ce tarif de tous les endroits mentionnés à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="470e1-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="470e1-111">Supprimer le tarif de pages spécifiques</span><span class="sxs-lookup"><span data-stu-id="470e1-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="470e1-112">Pour supprimer un tarif de Project Operations, accédez aux pages suivantes :</span><span class="sxs-lookup"><span data-stu-id="470e1-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="470e1-113">Page **Paramètres du projet** > Onglet **Tarifs**</span><span class="sxs-lookup"><span data-stu-id="470e1-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="470e1-114">Page **Unité d’organisation** > Grille **Tarifs**</span><span class="sxs-lookup"><span data-stu-id="470e1-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="470e1-115">Page **Compte** > Grille **Tarifs du projet**</span><span class="sxs-lookup"><span data-stu-id="470e1-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="470e1-116">Page **Devis de projet** > Grille **Tarifs du projet** : s’applique à tous les devis de projet actifs.</span><span class="sxs-lookup"><span data-stu-id="470e1-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="470e1-117">Page **Contrats de projets** > Grille **Tarifs du projet** : s’applique à tous les contrats de projets actifs.</span><span class="sxs-lookup"><span data-stu-id="470e1-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="470e1-118">Pour chaque page, vous devez sélectionner le tarif que vous souhaitez supprimer, puis sélectionner **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="470e1-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="470e1-119">Supprimer ou désactiver le tarif de la page Tarifs</span><span class="sxs-lookup"><span data-stu-id="470e1-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="470e1-120">Pour supprimer un tarif des tarifs actifs, accédez à **Ventes** > **Clients** > **Tarifs**.</span><span class="sxs-lookup"><span data-stu-id="470e1-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="470e1-121">Sélectionnez le tarif que vous souhaitez supprimer, puis sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="470e1-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="470e1-122">Si le tarif est référencé sur des transactions existantes, vous ne pourrez pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="470e1-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="470e1-123">Dans ce cas, vous pouvez désactiver le tarif pour qu’il n’apparaisse dans aucune vue.</span><span class="sxs-lookup"><span data-stu-id="470e1-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="470e1-124">Pour désactiver le tarif, sélectionnez-le à nouveau, puis sélectionnez **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="470e1-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
