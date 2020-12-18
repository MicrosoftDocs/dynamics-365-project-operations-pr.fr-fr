---
title: Remplacer les tarifs de vente des projets
description: Cette rubrique fournit des informations sur la création de listes de prix de vente personnalisées.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672228"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="f8487-103">Remplacer les tarifs de vente des projets</span><span class="sxs-lookup"><span data-stu-id="f8487-103">Override project sales price lists</span></span>

<span data-ttu-id="f8487-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f8487-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="f8487-105">Tarifs de projet spécifique pour un client</span><span class="sxs-lookup"><span data-stu-id="f8487-105">Customer-specific project price lists</span></span>

<span data-ttu-id="f8487-106">Dans Dynamics 365 Project Operations, les accords de prix spécifiques à un client peuvent être configurés sous la forme de tarifs de projet sur un enregistrement de compte.</span><span class="sxs-lookup"><span data-stu-id="f8487-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="f8487-107">Pour configurer un tarif de projet spécifique pour un client, dans la zone **Ventes**, accédez à l’enregistrement de compte.</span><span class="sxs-lookup"><span data-stu-id="f8487-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="f8487-108">Ouvrer la page de liste **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="f8487-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="f8487-109">Recherchez et double-cliquez sur un enregistrement de client pour ouvrir la page de détails **Compte**.</span><span class="sxs-lookup"><span data-stu-id="f8487-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="f8487-110">Sur l’onglet **Tarifs de projet**, sélectionnez **+ Nouveau tarif de projet**.</span><span class="sxs-lookup"><span data-stu-id="f8487-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="f8487-111">Dans la page **Nouveau tarif de projet**, sélectionnez un tarif dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f8487-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="f8487-112">Seuls les tarifs dont le contexte est défini sur **Ventes** et dont la devise correspond à la devise du compte sont inclus.</span><span class="sxs-lookup"><span data-stu-id="f8487-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="f8487-113">Nommez l’association et sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f8487-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="f8487-114">Un tarif de projet spécifique pour un client est créé.</span><span class="sxs-lookup"><span data-stu-id="f8487-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="f8487-115">Ce tarif sera utilisé pour créer les prix de projet par défaut sur les devis de projet ou les contrats créés pour ce client, si la date de création du devis ou du contrat de projet est conforme à la date d’entrée en vigueur du tarif.</span><span class="sxs-lookup"><span data-stu-id="f8487-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="f8487-116">Tarification personnalisée sur les devis de projet</span><span class="sxs-lookup"><span data-stu-id="f8487-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="f8487-117">Sur les devis de projet, vous pouvez avoir une tarification de projet qui commence par un tarif standard par défaut qui est défini par défaut selon le client ou selon les paramètres du projet.</span><span class="sxs-lookup"><span data-stu-id="f8487-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="f8487-118">Lorsque vous avez besoin d’une tarification personnalisée pour un travail lié à un projet sur un devis particulier, vous pouvez l’obtenir à partir de l’entité associée des tarifs du projet.</span><span class="sxs-lookup"><span data-stu-id="f8487-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="f8487-119">Effectuez les étapes suivantes pour configurer une tarification de projet spécifique à un devis.</span><span class="sxs-lookup"><span data-stu-id="f8487-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="f8487-120">Ouvrez le devis du projet et sélectionnez l’onglet **Tarifs du projet**.</span><span class="sxs-lookup"><span data-stu-id="f8487-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="f8487-121">Dans la sous-grille, sélectionnez **Créer une tarification personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="f8487-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="f8487-122">Tous les tarifs du projet joints au devis sont copiés dans les nouveaux tarifs.</span><span class="sxs-lookup"><span data-stu-id="f8487-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="f8487-123">Les noms des nouveaux tarifs reflètent le nom du devis avec un horodatage pour la création de ces tarifs.</span><span class="sxs-lookup"><span data-stu-id="f8487-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="f8487-124">Vous pouvez utiliser chacun de ces tarifs et faire des mises à jour des prix de la main-d’œuvre (prix du rôle) et des dépenses (prix de la catégorie).</span><span class="sxs-lookup"><span data-stu-id="f8487-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="f8487-125">Ces prix s’appliqueront uniquement à ce devis de projet.</span><span class="sxs-lookup"><span data-stu-id="f8487-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="f8487-126">Tarifs sur un contrat de projet</span><span class="sxs-lookup"><span data-stu-id="f8487-126">Price lists on a project contract</span></span>

<span data-ttu-id="f8487-127">Dans un contrat de projet, la tarification du projet est toujours définie par défaut comme un tarif personnalisé avec le nom du contrat et la date et l’heure de création ajoutées au nom.</span><span class="sxs-lookup"><span data-stu-id="f8487-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="f8487-128">Cela est vrai, que le contrat ait été créé lorsque le devis a été remporté ou que le contrat ait été créé à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="f8487-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="f8487-129">Si nécessaire, vous pouvez supprimer cette association au tarif personnalisé et associer un tarif standard au contrat de projet à la place.</span><span class="sxs-lookup"><span data-stu-id="f8487-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="f8487-130">Lorsque vous associez un tarif standard à des tarifs du projet sur un devis ou un contrat, toute modification apportée aux prix dans le tarif aura un impact sur tous les devis et contrats qui utilisent le tarif.</span><span class="sxs-lookup"><span data-stu-id="f8487-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
