---
title: Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié
description: Cette rubrique fournit des informations sur la configuration des taux de coûts et de vente pour les articles d’un catalogue de produits.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004316"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="d81e2-103">Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié</span><span class="sxs-lookup"><span data-stu-id="d81e2-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="d81e2-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="d81e2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d81e2-105">La configuration de la tarification des articles du catalogue de produits dans Dynamics 365 Project Operations est la même que dans Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d81e2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d81e2-106">Dans Project Operations, les produits ne peuvent pas être estimés ou utilisés sur des projets, de sorte que les prix du catalogue de produits n’ont pas besoin d’être définis sur les tarifs de projet pour les devis et les contrats.</span><span class="sxs-lookup"><span data-stu-id="d81e2-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="d81e2-107">Utilisez le champ **Prix du produit** d’un devis, d’un contrat ou d’un compte pour configurer les prix du catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="d81e2-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="d81e2-108">Ne configurez pas les prix du catalogue de produits dans les tarifs du projet.</span><span class="sxs-lookup"><span data-stu-id="d81e2-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="d81e2-109">Les tarifs de projet sont exclusifs à Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d81e2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="d81e2-110">La logique métier spécifique à l’application copie les tarifs d’un devis vers un contrat.</span><span class="sxs-lookup"><span data-stu-id="d81e2-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="d81e2-111">Il en résulte un tarif spécifique au contrat.</span><span class="sxs-lookup"><span data-stu-id="d81e2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="d81e2-112">L’opération de copie peut retarder le processus d’obtention d’un devis si le tarif du projet sur le devis devient trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="d81e2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="d81e2-113">Les tarifs des produits ne sont pas copiés pour créer des tarifs personnalisés sur les contrats.</span><span class="sxs-lookup"><span data-stu-id="d81e2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="d81e2-114">Comme aucune copie n’est impliquée, les performances du processus de devis ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="d81e2-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]