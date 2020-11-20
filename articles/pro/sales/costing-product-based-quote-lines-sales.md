---
title: Lignes du devis selon les produits pour l’évaluation des coûts
description: Cette rubrique fournit des informations sur l’application d’un prix de revient à une ligne de devis basée sur un produit.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118920"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="bc697-103">Lignes du devis selon les produits pour l’évaluation des coûts</span><span class="sxs-lookup"><span data-stu-id="bc697-103">Costing product-based quote lines</span></span>

<span data-ttu-id="bc697-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="bc697-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bc697-105">Les lignes de devis basées sur les produits dans Dynamics 365 Project Operations ont également un champ **Prix de revient**.</span><span class="sxs-lookup"><span data-stu-id="bc697-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="bc697-106">Ce champ est utilisé pour suivre le prix de revient du produit sur la ligne de devis et pour les calculs de rentabilité en aval.</span><span class="sxs-lookup"><span data-stu-id="bc697-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="bc697-107">Lorsqu’une ligne de devis basée sur un produit est créée pour un produit du catalogue, le coût de la ligne de devis basée sur le produit est par défaut celui du champ **Coût standard** dans le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="bc697-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="bc697-108">Le champ de coût standard dans le catalogue de produits est configuré dans la devise de base de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="bc697-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="bc697-109">Le coût unitaire par défaut de la ligne de devis basée sur le produit est converti dans la devise de vente du devis.</span><span class="sxs-lookup"><span data-stu-id="bc697-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="bc697-110">Coût unitaire sur une ligne du devis selon les produits</span><span class="sxs-lookup"><span data-stu-id="bc697-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="bc697-111">Le but d’avoir un coût unitaire sur une ligne de devis basée sur un produit est de permettre des coûts différents pour un produit pour chaque vente.</span><span class="sxs-lookup"><span data-stu-id="bc697-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="bc697-112">Ce n’est pas un scénario typique, mais parfois le coût du produit peut être réduit par le fournisseur en fonction du client de la vente finale.</span><span class="sxs-lookup"><span data-stu-id="bc697-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="bc697-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bc697-113">For example:</span></span>

<span data-ttu-id="bc697-114">Fabrikam Robotics installe des bras robotiques dans les chaînes de montage d’A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="bc697-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="bc697-115">Fabrikam fournit des services d’installation mais les bras robotiques sont fournis par Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="bc697-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="bc697-116">Si l’installation de bras robotiques chez A Datum Corporation ouvre un nouveau secteur vertical pour les bras robotiques de Trey, Trey pourrait accorder une remise spéciale pour cet accord à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="bc697-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="bc697-117">Dans ce cas, Fabrikam créera une ligne de devis basée sur le produit pour Robotic Arms et saisira un coût unitaire spécial pour ce devis.</span><span class="sxs-lookup"><span data-stu-id="bc697-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="bc697-118">Ce coût est différent du coût standard des bras robotiques Trey.</span><span class="sxs-lookup"><span data-stu-id="bc697-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
