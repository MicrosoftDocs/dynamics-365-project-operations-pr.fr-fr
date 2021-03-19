---
title: Créer une facture pro forma manuelle – Simplifié
description: Cette rubrique fournit des informations sur la création d’une facture pro forma manuelle dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274185"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="07769-103">Créer une facture pro forma manuelle – Simplifié</span><span class="sxs-lookup"><span data-stu-id="07769-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="07769-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="07769-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="07769-105">Dans Dynamics 365 Project Operations, les factures pro forma peuvent être créées manuellement, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="07769-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="07769-106">Vous pouvez créer manuellement une facture pro forma à partir de la page de liste **Contrats de projet** ou depuis la page de détails **Contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="07769-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="07769-107">Page de liste Contrats du projet</span><span class="sxs-lookup"><span data-stu-id="07769-107">Project Contracts list page</span></span>

<span data-ttu-id="07769-108">Dans la page de liste **Contrats du projet**, sélectionnez un ou plusieurs contrats de projet et créez des factures pour tous les enregistrements sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="07769-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="07769-109">Le système vérifie lequel des contrats de projet sélectionnés a un arriéré **Prêt à facturer** daté avant la date d’aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="07769-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="07769-110">À partir de ces contrats, le système crée des projets de factures pro forma.</span><span class="sxs-lookup"><span data-stu-id="07769-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="07769-111">Si un contrat de projet a plusieurs clients, il peut y avoir une facture créée par client et plusieurs factures par contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="07769-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="07769-112">Toutes les factures de projet créées sont disponibles sur la page **Facture** dans la section **Facturation** de la zone **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="07769-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="07769-113">Page Détails du contrat de projet</span><span class="sxs-lookup"><span data-stu-id="07769-113">Project Contract details page</span></span>

<span data-ttu-id="07769-114">Une facture pro forma peut également être créée à partir de la page de détails **Contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="07769-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="07769-115">Le système vérifie si le contrat de projet dispose d’un backlog **Prêt pour la facturation** daté d’avant la date du jour.</span><span class="sxs-lookup"><span data-stu-id="07769-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="07769-116">À partir de ces contrats, le système crée des factures pro forma provisoires en fonction du nombre de clients sur chaque ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="07769-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="07769-117">Lorsqu’une seule facture pro forma est créée, la page **Facture** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="07769-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="07769-118">Si plusieurs factures ont été créées pour le contrat de projet concerné, la page de liste **Factures** s’ouvre pour afficher toutes les factures créées.</span><span class="sxs-lookup"><span data-stu-id="07769-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]