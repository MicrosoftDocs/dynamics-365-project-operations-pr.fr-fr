---
title: Unités et groupes d’unités
description: Cette rubrique fournit des informations sur la création d’unités et de groupes d’unités dans Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277335"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="02f6e-103">Unités et groupes d’unités</span><span class="sxs-lookup"><span data-stu-id="02f6e-103">Units and unit groups</span></span>

<span data-ttu-id="02f6e-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="02f6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="02f6e-105">Les unités sont les quantités ou les mesures selon lesquelles vous vendez vos produits ou services.</span><span class="sxs-lookup"><span data-stu-id="02f6e-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="02f6e-106">Par exemple, si vous vendez des fournitures de jardinage, vous pouvez vendre des graines par unités de paquets, de cartons et de palettes.</span><span class="sxs-lookup"><span data-stu-id="02f6e-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="02f6e-107">Un groupe d’unités est une combinaison de ces différentes unités.</span><span class="sxs-lookup"><span data-stu-id="02f6e-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="02f6e-108">Pour effectuer les étapes de cette rubrique, assurez-vous de disposer du rôle d’Administrateur système ou de gestionnaire de Sales Professional ou d’autorisations équivalentes..</span><span class="sxs-lookup"><span data-stu-id="02f6e-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="02f6e-109">Créer un groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="02f6e-109">Create a unit group</span></span>

1. <span data-ttu-id="02f6e-110">Sur le plan de site, sélectionnez **Unités**.</span><span class="sxs-lookup"><span data-stu-id="02f6e-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="02f6e-111">Sélectionnez **Nouveau**, et tapez le nom de l’unité dans la boîte de dialogue **Créer Unité de vente**.</span><span class="sxs-lookup"><span data-stu-id="02f6e-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="02f6e-112">Dans le champ **Unité principale**, entrez la plus petite unité de mesure courante dans laquelle le produit doit être vendu.</span><span class="sxs-lookup"><span data-stu-id="02f6e-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="02f6e-113">Par exemple, vous pouvez entrer « pièce » ou « once ».</span><span class="sxs-lookup"><span data-stu-id="02f6e-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="02f6e-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="02f6e-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="02f6e-115">Ajouter des unités à un groupe d’unités</span><span class="sxs-lookup"><span data-stu-id="02f6e-115">Add units to a unit group</span></span>

1. <span data-ttu-id="02f6e-116">Ouvrez un groupe d’unités et sur l’onglet **Association**, sélectionnez **Unités**.</span><span class="sxs-lookup"><span data-stu-id="02f6e-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="02f6e-117">Vous verrez que l’unité principale est déjà ajoutée.</span><span class="sxs-lookup"><span data-stu-id="02f6e-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="02f6e-118">Sélectionnez **Ajouter une nouvelle unité**, et sur la page **Création rapide : Unité**, entrez le nom de l’unité dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="02f6e-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="02f6e-119">Dans le champ **Quantité**, entrez la quantité que cette unité représentera.</span><span class="sxs-lookup"><span data-stu-id="02f6e-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="02f6e-120">Par exemple, si une boîte contient deux pièces, entrez « 2 ».</span><span class="sxs-lookup"><span data-stu-id="02f6e-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="02f6e-121">Dans le champ **Unité de base**, sélectionnez une unité de base pour établir la plus petite unité de mesure pour l’unité.</span><span class="sxs-lookup"><span data-stu-id="02f6e-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="02f6e-122">Par exemple, vous pouvez sélectionner « Pièce ».</span><span class="sxs-lookup"><span data-stu-id="02f6e-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="02f6e-123">Sélectionnez **Enregistrer** :</span><span class="sxs-lookup"><span data-stu-id="02f6e-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]