---
title: Acheter du matériel non stocké à l’aide d’une facture fournisseur en attente
description: Cette rubrique explique comment enregistrer les factures fournisseur en attente.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993787"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="62204-103">Acheter du matériel non stocké à l’aide d’une facture fournisseur en attente</span><span class="sxs-lookup"><span data-stu-id="62204-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="62204-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="62204-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62204-105">Lorsqu’une entreprise achète du matériel non stocké pour un projet, les coûts peuvent être immédiatement comptabilisés dans le projet.</span><span class="sxs-lookup"><span data-stu-id="62204-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="62204-106">Par example, Contoso Robotics États-Unis réalise un projet de renouvellement d’équipement et a besoin de licences logicielles.</span><span class="sxs-lookup"><span data-stu-id="62204-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="62204-107">Ces licences sont obtenues auprès d’un fournisseur tiers.</span><span class="sxs-lookup"><span data-stu-id="62204-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="62204-108">À l’aide de Dynamics 365 Finance, le commis à la comptabilité fournisseur enregistre une facture fournisseur en attente et attribue les coûts de licence directement au projet de renouvellement de l’équipement.</span><span class="sxs-lookup"><span data-stu-id="62204-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="62204-109">Avant d’utiliser la fonctionnalité décrite dans cette rubrique, passez en revue et appliquez les configurations requises.</span><span class="sxs-lookup"><span data-stu-id="62204-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="62204-110">Pour plus d’informations, consultez [Activer le matériel non stocké et les factures fournisseur en attente](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="62204-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="62204-111">Publier une facture fournisseur en attente liée au projet</span><span class="sxs-lookup"><span data-stu-id="62204-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="62204-112">Les factures fournisseur en attente peuvent être enregistrées sur la page **Factures fournisseur en attente** (**Comptabilité fournisseur** > **Factures** > **Factures fournisseur en attente**).</span><span class="sxs-lookup"><span data-stu-id="62204-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="62204-113">Procédez comme suit pour valider une facture fournisseur en attente liée au projet :</span><span class="sxs-lookup"><span data-stu-id="62204-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="62204-114">Accédez à **Comptabilité fournisseur** > **Factures** et sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="62204-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="62204-115">Dans le champ **Compte de facturation**, sélectionnez un fournisseur et dans le champ **Nombre**, saisissez l’identification de la facture fournisseur.</span><span class="sxs-lookup"><span data-stu-id="62204-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="62204-116">Ajoutez une ligne à la facture fournisseur et dans le champ **Numéro d’article**, sélectionnez l’article non stocké acheté auprès du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="62204-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="62204-117">Les lignes de facture fournisseur basées sur une catégorie d’approvisionnement ne peuvent pas être comptabilisées dans le projet.</span><span class="sxs-lookup"><span data-stu-id="62204-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="62204-118">Ajoutez la quantité achetée.</span><span class="sxs-lookup"><span data-stu-id="62204-118">Add the quantity purchased.</span></span> <span data-ttu-id="62204-119">Le système renseignera le prix unitaire en fonction de la configuration du prix de l’article non stocké.</span><span class="sxs-lookup"><span data-stu-id="62204-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="62204-120">Vérifiez le montant total et les autres détails requis sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="62204-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="62204-121">Sur les détails de la ligne, sur l’onglet **Projet**, sélectionnez l’ID du projet dans lequel cet élément sera enregistré.</span><span class="sxs-lookup"><span data-stu-id="62204-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="62204-122">Si vous le souhaitez, sélectionnez le numéro d’activité et mettez à jour la catégorie de projet et la propriété de ligne.</span><span class="sxs-lookup"><span data-stu-id="62204-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="62204-123">Validez la facture fournisseur en attente.</span><span class="sxs-lookup"><span data-stu-id="62204-123">Post pending vendor invoice.</span></span> <span data-ttu-id="62204-124">Lorsque la facture est validée, le système enregistre :</span><span class="sxs-lookup"><span data-stu-id="62204-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="62204-125">Le montant du solde fournisseur.</span><span class="sxs-lookup"><span data-stu-id="62204-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="62204-126">Le montant de la taxe de vente.</span><span class="sxs-lookup"><span data-stu-id="62204-126">The sales tax amount.</span></span>
    - <span data-ttu-id="62204-127">Le coût par rapport au projet est enregistré dans le compte d’intégration d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="62204-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="62204-128">La transaction réelle du projet dans Dataverse.</span><span class="sxs-lookup"><span data-stu-id="62204-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="62204-129">La transaction est traitée davantage à l’aide de la [feuille intégration Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="62204-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="62204-130">La validation de cette feuille déplace le montant du compte d’intégration d’approvisionnement vers le compte de coûts du projet.</span><span class="sxs-lookup"><span data-stu-id="62204-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
