---
title: Lignes de contrat selon les produits pour évaluation des coûts
description: Cette rubrique fournit des informations sur la création
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075971"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="84af4-103">Lignes de contrat selon les produits pour évaluation des coûts</span><span class="sxs-lookup"><span data-stu-id="84af4-103">Costing product-based contract lines</span></span>

<span data-ttu-id="84af4-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="84af4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="84af4-105">Les lignes de contrat basées sur les produits dans Dynamics 365 Project Operations incluent le champ **Prix de revient** , qui stocke le prix de revient du produit pour les calculs de rentabilité en aval.</span><span class="sxs-lookup"><span data-stu-id="84af4-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="84af4-106">Lorsqu'une ligne de contrat basée sur un produit est créée pour un produit du catalogue, le coût de la ligne de contrat basée sur le produit est par défaut celui du champ **Coût standard** dans le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="84af4-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="84af4-107">Le champ **Coût standard** dans le catalogue de produits est configuré dans la devise de base de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="84af4-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="84af4-108">Lorsque le coût unitaire est par défaut sur la ligne du contrat, il est converti dans la devise de vente du contrat.</span><span class="sxs-lookup"><span data-stu-id="84af4-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="84af4-109">Coût unitaire sur une ligne du contrat selon les produits</span><span class="sxs-lookup"><span data-stu-id="84af4-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="84af4-110">Avoir un coût unitaire sur une ligne de contrat basée sur un produit permet des coûts différents pour un produit pour chaque vente.</span><span class="sxs-lookup"><span data-stu-id="84af4-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="84af4-111">Bien que cela ne soit pas toujours nécessaire, il existe certains scénarios dans lesquels le coût du produit peut être réduit pour le client par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84af4-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="84af4-112">Prenons l'exemple du scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="84af4-112">Consider the following scenario:</span></span>

<span data-ttu-id="84af4-113">Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d'Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="84af4-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="84af4-114">Fabrikam fournit des services d'installation mais les bras robotiques sont fournis par Trey Research.</span><span class="sxs-lookup"><span data-stu-id="84af4-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="84af4-115">Si l'installation de bras robotiques chez Adatum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey Research, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="84af4-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="84af4-116">Dans ce cas, Fabrikam crée une ligne de contrat basée sur les produits pour Robotic Arms et saisit un coût unitaire pour ce contrat qui est différent du coût standard des bras robotiques de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="84af4-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
