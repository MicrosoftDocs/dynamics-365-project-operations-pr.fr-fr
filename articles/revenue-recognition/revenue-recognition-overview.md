---
title: Vue d’ensemble de la constatation du produit
description: Cette rubrique fournit des informations sur la constatation du produit dans Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013753"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="08e8b-103">Vue d’ensemble de la constatation du produit</span><span class="sxs-lookup"><span data-stu-id="08e8b-103">Revenue recognition overview</span></span>

<span data-ttu-id="08e8b-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="08e8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="08e8b-105">Dans Dynamics 365 Project Operations, les principes de constatation du produit varient en fonction de la méthode de facturation choisie pour un projet ou une partie du projet.</span><span class="sxs-lookup"><span data-stu-id="08e8b-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="08e8b-106">Cette rubrique fournit des informations sur la constatation du produit dans Project Operations.</span><span class="sxs-lookup"><span data-stu-id="08e8b-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="08e8b-107">Transactions comptabilisées utilisant une méthode de facturation des temps et matières</span><span class="sxs-lookup"><span data-stu-id="08e8b-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="08e8b-108">La constatation des coûts et des revenus est liée.</span><span class="sxs-lookup"><span data-stu-id="08e8b-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="08e8b-109">Le coût de transaction et les ventes non facturées sont enregistrés à l’aide du [Journal d’intégration Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="08e8b-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="08e8b-110">Le profil de coût et de revenu du projet détermine si les transactions de vente non facturées sont validées dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="08e8b-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="08e8b-111">Si **Régulariser revenus** est sélectionné, le système utilise les comptes **Valeur des ventes TEC** et **Valeur des ventes des revenus régularisés** lors de la validation.</span><span class="sxs-lookup"><span data-stu-id="08e8b-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="08e8b-112">Voici un exemple de ce mode :</span><span class="sxs-lookup"><span data-stu-id="08e8b-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08e8b-113">Type de transaction</span><span class="sxs-lookup"><span data-stu-id="08e8b-113">Transaction type</span></span> | <span data-ttu-id="08e8b-114">Débit/crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-114">Debit/Credit</span></span> | <span data-ttu-id="08e8b-115">Montant</span><span class="sxs-lookup"><span data-stu-id="08e8b-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08e8b-116">Valeur des ventes TEC</span><span class="sxs-lookup"><span data-stu-id="08e8b-116">WIP Sales value</span></span> | <span data-ttu-id="08e8b-117">Débit</span><span class="sxs-lookup"><span data-stu-id="08e8b-117">Debit</span></span> | <span data-ttu-id="08e8b-118">100</span><span class="sxs-lookup"><span data-stu-id="08e8b-118">100</span></span> |
  | <span data-ttu-id="08e8b-119">Valeur des ventes des revenus régularisés</span><span class="sxs-lookup"><span data-stu-id="08e8b-119">Accrued revenue sales value</span></span> | <span data-ttu-id="08e8b-120">Crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-120">Credit</span></span> | <span data-ttu-id="08e8b-121">100</span><span class="sxs-lookup"><span data-stu-id="08e8b-121">100</span></span> |

- <span data-ttu-id="08e8b-122">Le produit est constaté lors de la facturation.</span><span class="sxs-lookup"><span data-stu-id="08e8b-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="08e8b-123">Le système utilise le compte **Revenu facturé** lors de la validation.</span><span class="sxs-lookup"><span data-stu-id="08e8b-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="08e8b-124">Voici un exemple de ce mode :</span><span class="sxs-lookup"><span data-stu-id="08e8b-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08e8b-125">Type de transaction</span><span class="sxs-lookup"><span data-stu-id="08e8b-125">Transaction type</span></span> | <span data-ttu-id="08e8b-126">Débit/crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-126">Debit/Credit</span></span> | <span data-ttu-id="08e8b-127">Montant</span><span class="sxs-lookup"><span data-stu-id="08e8b-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08e8b-128">Solde client</span><span class="sxs-lookup"><span data-stu-id="08e8b-128">Customer balance</span></span> | <span data-ttu-id="08e8b-129">Débit</span><span class="sxs-lookup"><span data-stu-id="08e8b-129">Debit</span></span> | <span data-ttu-id="08e8b-130">120</span><span class="sxs-lookup"><span data-stu-id="08e8b-130">120</span></span> |
  | <span data-ttu-id="08e8b-131">Taxe due</span><span class="sxs-lookup"><span data-stu-id="08e8b-131">Sales tax payable</span></span> | <span data-ttu-id="08e8b-132">Crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-132">Credit</span></span> | <span data-ttu-id="08e8b-133">20</span><span class="sxs-lookup"><span data-stu-id="08e8b-133">20</span></span> |
  | <span data-ttu-id="08e8b-134">Revenu facturé</span><span class="sxs-lookup"><span data-stu-id="08e8b-134">Invoiced Revenue</span></span> | <span data-ttu-id="08e8b-135">Crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-135">Credit</span></span> | <span data-ttu-id="08e8b-136">100</span><span class="sxs-lookup"><span data-stu-id="08e8b-136">100</span></span> |

- <span data-ttu-id="08e8b-137">Si des revenus ont été régularisés lors de la validation des ventes non facturées, le système annulera les revenus régularisés lors de la facturation.</span><span class="sxs-lookup"><span data-stu-id="08e8b-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="08e8b-138">Type de transaction</span><span class="sxs-lookup"><span data-stu-id="08e8b-138">Transaction type</span></span> | <span data-ttu-id="08e8b-139">Débit/crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-139">Debit/Credit</span></span> | <span data-ttu-id="08e8b-140">Montant</span><span class="sxs-lookup"><span data-stu-id="08e8b-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08e8b-141">Valeur des ventes TEC</span><span class="sxs-lookup"><span data-stu-id="08e8b-141">WIP Sales value</span></span> | <span data-ttu-id="08e8b-142">Crédit</span><span class="sxs-lookup"><span data-stu-id="08e8b-142">Credit</span></span> | <span data-ttu-id="08e8b-143">100</span><span class="sxs-lookup"><span data-stu-id="08e8b-143">100</span></span> |
  | <span data-ttu-id="08e8b-144">Valeur des ventes des revenus régularisés</span><span class="sxs-lookup"><span data-stu-id="08e8b-144">Accrued revenue sales value</span></span> | <span data-ttu-id="08e8b-145">Débit</span><span class="sxs-lookup"><span data-stu-id="08e8b-145">Debit</span></span> | <span data-ttu-id="08e8b-146">100</span><span class="sxs-lookup"><span data-stu-id="08e8b-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="08e8b-147">Transactions comptabilisées utilisant une méthode de facturation à prix fixe</span><span class="sxs-lookup"><span data-stu-id="08e8b-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="08e8b-148">La constatation des coûts et des revenus est séparée.</span><span class="sxs-lookup"><span data-stu-id="08e8b-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="08e8b-149">Le coût de transaction est validé à l’aide du [Journal d’intégration Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="08e8b-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="08e8b-150">Les transactions de vente non facturées ne sont pas créées.</span><span class="sxs-lookup"><span data-stu-id="08e8b-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="08e8b-151">Le revenu peut être reconnu lors de la facturation si le profil de coût et de revenu du projet **Principe utilisé pour les calculs d’achèvement de projet** est défini sur **Pas de TEC**.</span><span class="sxs-lookup"><span data-stu-id="08e8b-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="08e8b-152">Utilisez ce mode uniquement pour des projets simples à court terme.</span><span class="sxs-lookup"><span data-stu-id="08e8b-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="08e8b-153">Le produit peut être constaté à l’aide d’estimations de revenus à prix fixe, avec la méthode **Contrat complété** ou **Reconnaissance des revenus en pourcentage d’achèvement**.</span><span class="sxs-lookup"><span data-stu-id="08e8b-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08e8b-154">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="08e8b-154">Additional resources</span></span>
[<span data-ttu-id="08e8b-155">Configurer la comptabilité des projets facturables</span><span class="sxs-lookup"><span data-stu-id="08e8b-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="08e8b-156">Projets d’estimation de revenus à prix fixe</span><span class="sxs-lookup"><span data-stu-id="08e8b-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="08e8b-157">Gérer les estimations de revenus</span><span class="sxs-lookup"><span data-stu-id="08e8b-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="08e8b-158">Coût pour compléter les méthodes</span><span class="sxs-lookup"><span data-stu-id="08e8b-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]