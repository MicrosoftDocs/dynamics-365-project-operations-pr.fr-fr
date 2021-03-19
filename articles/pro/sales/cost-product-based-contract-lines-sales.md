---
title: Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié
description: Cette rubrique fournit des informations sur la création
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273690"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="df097-103">Lignes de contrat basées sur les produits pour évaluation des coûts – Simplifié</span><span class="sxs-lookup"><span data-stu-id="df097-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="df097-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="df097-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="df097-105">Les lignes de contrat basées sur les produits dans Dynamics 365 Project Operations incluent le champ **Prix de revient**, qui stocke le prix de revient du produit pour les calculs de rentabilité en aval.</span><span class="sxs-lookup"><span data-stu-id="df097-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="df097-106">Lorsqu'une ligne de contrat basée sur un produit est créée pour un produit de catalogue, le coût de la ligne est par défaut du champ **Coût standard** dans le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="df097-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="df097-107">Le champ **Coût standard** dans le catalogue de produits est configuré dans la devise de base de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="df097-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="df097-108">Lorsque le coût unitaire est par défaut sur la ligne du contrat, il est converti dans la devise de vente du contrat.</span><span class="sxs-lookup"><span data-stu-id="df097-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="df097-109">Coût unitaire sur une ligne du contrat selon les produits</span><span class="sxs-lookup"><span data-stu-id="df097-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="df097-110">Avoir un coût unitaire sur une ligne de contrat basée sur un produit permet des coûts différents pour un produit pour chaque vente.</span><span class="sxs-lookup"><span data-stu-id="df097-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="df097-111">Bien que cela ne soit pas toujours nécessaire, il existe certains scénarios dans lesquels le coût du produit peut être réduit pour le client par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="df097-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="df097-112">Prenons l’exemple du scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="df097-112">Consider the following scenario:</span></span>

<span data-ttu-id="df097-113">Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d’Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="df097-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="df097-114">Fabrikam fournit des services d'installation mais les bras robotiques sont de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="df097-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="df097-115">Si l’installation de bras robotiques chez Adatum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey Research, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="df097-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="df097-116">Dans ce cas, Fabrikam crée une ligne de contrat basée sur les produits pour Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="df097-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="df097-117">Un coût unitaire est inscrit pour ce contrat.</span><span class="sxs-lookup"><span data-stu-id="df097-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="df097-118">Le coût est différent du coût des bras robotiques de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="df097-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]