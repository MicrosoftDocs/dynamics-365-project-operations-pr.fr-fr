---
title: Estimations basées sur la ressource
description: Cette rubrique fournit des informations sur le calcul des estimations des ressources dans Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075660"
---
# <a name="resource-estimates"></a><span data-ttu-id="2da25-103">Estimations basées sur la ressource</span><span class="sxs-lookup"><span data-stu-id="2da25-103">Resource estimates</span></span>

<span data-ttu-id="2da25-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="2da25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2da25-105">Les estimations des ressources proviennent d’efforts échelonnés dans le temps qui sont définis dans la structure de répartition du travail avec les dimensions de tarification applicables.</span><span class="sxs-lookup"><span data-stu-id="2da25-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="2da25-106">En règle générale, le calcul est **taux/h pour chaque rôle x heures.**</span><span class="sxs-lookup"><span data-stu-id="2da25-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="2da25-107">L’effort échelonné pour chaque ressource est stocké dans l’enregistrement d’affectation de ressource.</span><span class="sxs-lookup"><span data-stu-id="2da25-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="2da25-108">La tarification est stockée dans un tarif prédéfini.</span><span class="sxs-lookup"><span data-stu-id="2da25-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="2da25-109">La conversion des unités est appliquée en fonction du tarif applicable.</span><span class="sxs-lookup"><span data-stu-id="2da25-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimations des ressources](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="2da25-111">Prix de revient et devise du prix de revient par défaut</span><span class="sxs-lookup"><span data-stu-id="2da25-111">Default cost price and cost currency</span></span>

<span data-ttu-id="2da25-112">Les prix de revient proviennent par défaut de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="2da25-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="2da25-113">Taux de facturation et devise des ventes par défaut</span><span class="sxs-lookup"><span data-stu-id="2da25-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="2da25-114">Les prix de vente sont appliqués une fois par transaction.</span><span class="sxs-lookup"><span data-stu-id="2da25-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="2da25-115">La hiérarchie des tarifs de vente par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="2da25-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="2da25-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="2da25-116">Organization</span></span>
2. <span data-ttu-id="2da25-117">Client</span><span class="sxs-lookup"><span data-stu-id="2da25-117">Customer</span></span>
3. <span data-ttu-id="2da25-118">Devis/contrat</span><span class="sxs-lookup"><span data-stu-id="2da25-118">Quote/contract</span></span>
