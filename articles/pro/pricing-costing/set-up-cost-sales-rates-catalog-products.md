---
title: Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié
description: Cette rubrique fournit des informations sur la configuration des taux de coûts et de vente pour les articles d’un catalogue de produits.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176698"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="d3b92-103">Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié</span><span class="sxs-lookup"><span data-stu-id="d3b92-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="d3b92-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="d3b92-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d3b92-105">La configuration de la tarification des éléments d’un catalogue de produits dans Dynamics 365 Project Operations est la même que dans Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d3b92-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d3b92-106">Étant donné que les produits ne peuvent pas être estimés ou utilisés sur des projets dans Project Operations, il n’est pas nécessaire de configurer les prix du catalogue de produits sur les tarifs de projet pour les devis et les contrats.</span><span class="sxs-lookup"><span data-stu-id="d3b92-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="d3b92-107">Les prix du catalogue de produits doivent être configurés dans le champ **Prix du produit** d’un devis, d’un contrat ou d’un compte.</span><span class="sxs-lookup"><span data-stu-id="d3b92-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="d3b92-108">Ne configurez pas les prix du catalogue de produits dans les tarifs du projet pour ces entités.</span><span class="sxs-lookup"><span data-stu-id="d3b92-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="d3b92-109">Les tarifs de projet sont exclusifs à Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d3b92-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="d3b92-110">Il existe une logique métier spécifique à l’application qui copie les tarifs d’un devis vers un contrat.</span><span class="sxs-lookup"><span data-stu-id="d3b92-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="d3b92-111">Il en résulte un tarif spécifique au contrat.</span><span class="sxs-lookup"><span data-stu-id="d3b92-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="d3b92-112">L’opération de copie peut retarder le processus d’obtention d’un devis si le tarif du projet sur le devis devient trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="d3b92-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="d3b92-113">Les tarifs des produits ne sont pas copiés pour créer des tarifs personnalisés sur les contrats.</span><span class="sxs-lookup"><span data-stu-id="d3b92-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="d3b92-114">Cela signifie que les tarifs des produits n’ont pas d’impact sur les performances du processus d’obtention d’un devis.</span><span class="sxs-lookup"><span data-stu-id="d3b92-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
