---
title: Création d’une facture pro forma manuelle
description: Cette rubrique fournit des informations sur la création d'une facture pro forma manuelle dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075969"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="0cee3-103">Création d’une facture pro forma manuelle</span><span class="sxs-lookup"><span data-stu-id="0cee3-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="0cee3-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="0cee3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cee3-105">Dans Dynamics 365 Project Operations, les factures pro forma peuvent être créées manuellement si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0cee3-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="0cee3-106">Vous pouvez créer manuellement une facture pro forma à partir de la page de liste **Contrats de projet** ou depuis la page de détails **Contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="0cee3-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="0cee3-107">Page de liste Contrats du projet</span><span class="sxs-lookup"><span data-stu-id="0cee3-107">Project Contracts list page</span></span>

<span data-ttu-id="0cee3-108">Dans la page de liste **Contrats du projet** , sélectionnez un ou plusieurs contrats de projet et créez des factures pour tous les enregistrements sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0cee3-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="0cee3-109">Le système vérifie lequel des contrats de projet sélectionnés a un arriéré **Prêt à facturer** daté avant la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="0cee3-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="0cee3-110">À partir de ces contrats, le système crée des projets de factures pro forma.</span><span class="sxs-lookup"><span data-stu-id="0cee3-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="0cee3-111">Si un contrat de projet a plusieurs clients, il peut y avoir une facture créée par client et plusieurs factures par contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="0cee3-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="0cee3-112">Toutes les factures de projet créées sont disponibles sur la page **Facture** dans la section **Facturation** de la zone **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="0cee3-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="0cee3-113">Page Détails du contrat de projet</span><span class="sxs-lookup"><span data-stu-id="0cee3-113">Project Contract details page</span></span>

<span data-ttu-id="0cee3-114">Une facture pro forma peut également être créée à partir de la page de détails **Contrat de projet** , qui crée la facture pour ce contrat de projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="0cee3-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="0cee3-115">Le système vérifie que le contrat de projet a un arriéré **Prêt à facturer** qui est daté avant la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="0cee3-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="0cee3-116">À partir de ces contrats, le système crée des projets de factures pro forma en fonction du nombre de clients sur chaque ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="0cee3-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="0cee3-117">Lorsqu'une seule facture pro forma est créée, la page **Facture** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="0cee3-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="0cee3-118">S'il y a plusieurs factures créées pour ce contrat de projet, la page de liste **Factures** s'ouvre pour afficher toutes les factures créées.</span><span class="sxs-lookup"><span data-stu-id="0cee3-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
