---
title: Vue d’ensemble de la facturation intersociétés
description: Cette rubrique fournit des informations et des exemples sur la facturation intersociétés pour les projets.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369373"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="b3ca5-103">Vue d’ensemble de la facturation intersociétés</span><span class="sxs-lookup"><span data-stu-id="b3ca5-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="b3ca5-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="b3ca5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b3ca5-105">Votre organisation peut avoir plusieurs divisions, filiales et autres entités juridiques qui se transfèrent des produits et des services pour des projets.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="b3ca5-106">L’entité juridique qui fournit le service ou le produit est appelée *entité juridique prêteuse*.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="b3ca5-107">L’entité juridique qui reçoit le service ou le produit est appelée *entité juridique emprunteuse*.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="b3ca5-108">L’illustration suivante présente un scénario typique dans lequel deux entités juridiques, Contoso Robotics USA (l’entité juridique emprunteuse) et Contoso Robotics UK (l’entité juridique prêteuse) partagent des ressources pour livrer un projet au client, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="b3ca5-109">Pour ce scénario, Contoso Robotics USA est engagé pour livrer le travail à Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Facturation intersociétés](./media/IntercompanyScenario.png) 

<span data-ttu-id="b3ca5-111">Dynamics 365 Project Operations utilise le flux suivant pour traiter les transactions intersociétés :</span><span class="sxs-lookup"><span data-stu-id="b3ca5-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="b3ca5-112">Les ressources de l’entité juridique prêteuse enregistrent les transactions de temps ou de dépenses intersociétés en comptabilisant le temps et les dépenses par rapport aux projets de l’entité juridique emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="b3ca5-113">Les coûts de temps et de dépenses sont enregistrés dans la société prêteuse en utilisant la liste de prix de revient unitaire de la société emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="b3ca5-114">Les transactions de vente non facturée intersociétés sont enregistrés dans la société prêteuse en utilisant la liste de prix de revient unitaire de la société emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="b3ca5-115">Le revenu non facturé est enregistré dans la société emprunteuse à l’aide du tarif de vente du contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="b3ca5-116">Le client peut être facturé lors de l’enregistrement des revenus non facturés.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="b3ca5-117">Le client n’a pas à attendre la fin du traitement des factures intersociétés.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="b3ca5-118">Les factures clients intersociétés sont créées périodiquement dans la société prêteuse.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="b3ca5-119">Les factures sont créées manuellement ou en utilisant un processus automatisé périodique.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="b3ca5-120">Une seule facture peut être créée pour chaque entité juridique emprunteuse ou des factures distinctes peuvent être créées par projet.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="b3ca5-121">Lorsque la facture client intersociétés est validée dans l’entité juridique emprunteuse, la facture fournisseur en attente correspondante est créée dans l’entité juridique emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="b3ca5-122">Les coûts de la facture fournisseur en attente seront enregistrés dans le livre auxiliaire du projet lorsque la facture est validée.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="b3ca5-123">Le diagramme suivant illustre la facturation intersociétés en ce qui concerne les événements comptables et les écritures attendues dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="b3ca5-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Flux intersociétés](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="b3ca5-125">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="b3ca5-125">Additional resources</span></span>

- [<span data-ttu-id="b3ca5-126">Configurer la facturation intersociétés</span><span class="sxs-lookup"><span data-stu-id="b3ca5-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="b3ca5-127">Enregistrer des transactions intersociétés</span><span class="sxs-lookup"><span data-stu-id="b3ca5-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="b3ca5-128">Créer des factures clients et fournisseurs intersociétés</span><span class="sxs-lookup"><span data-stu-id="b3ca5-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]