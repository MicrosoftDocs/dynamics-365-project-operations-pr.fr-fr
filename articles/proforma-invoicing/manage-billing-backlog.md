---
title: Gérer la réplication de facturation
description: Cette rubrique fournit des informations sur la façon d'afficher et d'utiliser la réplication de facturation dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087903"
---
# <a name="manage-the-billing-backlog"></a><span data-ttu-id="2a886-103">Gérer la réplication de facturation</span><span class="sxs-lookup"><span data-stu-id="2a886-103">Manage the billing backlog</span></span>

<span data-ttu-id="2a886-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="2a886-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2a886-105">Dynamics 365 Project Operations dispose de deux vues dédiées pour vous aider à utiliser et gérer la réplication de facturation.</span><span class="sxs-lookup"><span data-stu-id="2a886-105">Dynamics 365 Project Operations has two dedicated views to help you work with and manage the billing backlog.</span></span> <span data-ttu-id="2a886-106">Il s'agit de **Jalons de prix fixe** et **Réplication de facturation pour le temps et le matériel** Pour sélectionner une vue, dans la zone **Ventes** de Project Operations, sur la page de navigation de gauche, sélectionnez **Facturation**.</span><span class="sxs-lookup"><span data-stu-id="2a886-106">They are **Fixed Price Milestones** and **Time and Material Billing Backlog** To select a view, in the **Sales** area of Project Operations, on the left navigation page, select **Billing**.</span></span> <span data-ttu-id="2a886-107">Les liens de réplication de facturation y sont stockés.</span><span class="sxs-lookup"><span data-stu-id="2a886-107">The billing backlog links are stored there.</span></span>

## <a name="fixed-price-milestones"></a><span data-ttu-id="2a886-108">Jalons de prix fixe</span><span class="sxs-lookup"><span data-stu-id="2a886-108">Fixed Price Milestones</span></span>

<span data-ttu-id="2a886-109">Cette vue répertorie tous les jalons de prix fixe sur toutes les lignes de contrat de projet du système.</span><span class="sxs-lookup"><span data-stu-id="2a886-109">This view lists all fixed price milestones across all of the project contract lines in the system.</span></span> <span data-ttu-id="2a886-110">Un ou plusieurs jalons peuvent être marqués comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="2a886-110">Single or multiple milestones can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="2a886-111">Lorsque vous marquez un jalon comme **Prêt pour la facturation** , le jalon devient disponible pour une facture provisoire.</span><span class="sxs-lookup"><span data-stu-id="2a886-111">When you mark a milestone as **Ready to Invoice** , the milestone becomes available for a draft invoice.</span></span>

<span data-ttu-id="2a886-112">Lorsque les lignes de contrat avec plusieurs clients ont une méthode de facturation à prix fixe, un jalon est créé pour chaque client de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="2a886-112">When multi-customer contract lines have a fixed price billing method, one milestone is created for each customer on the contract line.</span></span> <span data-ttu-id="2a886-113">L'utilisateur crée un jalon et ce jalon est fractionné en enregistrements de jalons spécifiques au client en interne, selon le pourcentage de facturation fractionné défini pour chaque client sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="2a886-113">The user creates a milestone and that milestone is split into customer=specific milestone records internally, according to the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="2a886-114">Dans la vue **Jalons de prix fixes** , vous verrez des enregistrements de jalons spécifiques au client.</span><span class="sxs-lookup"><span data-stu-id="2a886-114">In the **Fixed Price Milestones** view, you will see individual customer-specific milestone records.</span></span> <span data-ttu-id="2a886-115">Chacun de ces enregistrements de jalons peut être marqué comme **Prêt pour la facturation** séparément dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="2a886-115">Each of these milestone records can be marked as **Ready to Invoice** separately from this view.</span></span> <span data-ttu-id="2a886-116">Lorsqu'un ou plusieurs fractionnements de jalons associés sont marqués comme **Prêt pour la facturation** , l'en-tête passe de l'état **Non démarré** à **En cours**.</span><span class="sxs-lookup"><span data-stu-id="2a886-116">When one or more of the related milestone splits are marked as **Ready to Invoice** , the header moves to a status of **In Progress** from **Not Started**.</span></span> <span data-ttu-id="2a886-117">Lorsque tous les fractionnements de jalons ont été facturés, le statut du jalon de l'en-tête devient **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="2a886-117">When all of the milestone splits have been invoiced, the header milestone status becomes **Completed**.</span></span>

<span data-ttu-id="2a886-118">Un jalon sur une facture provisoire est affiché dans cette vue avec le statut de facturation **Facture client créée**.</span><span class="sxs-lookup"><span data-stu-id="2a886-118">A milestone on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="2a886-119">Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture publiée**.</span><span class="sxs-lookup"><span data-stu-id="2a886-119">When the draft invoice is confirmed, the billing status on this record is updated to **Invoice Posted**.</span></span> <span data-ttu-id="2a886-120">Il n'est pas recommandé de mettre à jour cette valeur de statut à l'aide d'un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2a886-120">Updating this status value by using custom code isn't recommended.</span></span> <span data-ttu-id="2a886-121">Project Operations ne fonctionnera pas correctement si ces valeurs de statut sont mises à jour avec un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2a886-121">Project Operations won't function correctly if these status values are updated with custom code.</span></span>

## <a name="time-and-material-billing-backlog"></a><span data-ttu-id="2a886-122">Réplication de facturation pour le temps et le matériel</span><span class="sxs-lookup"><span data-stu-id="2a886-122">Time and Material Billing Backlog</span></span>

<span data-ttu-id="2a886-123">Cette vue répertorie toutes les ventes réelles non facturées qui n'ont pas été facturées pour l'ensemble des contrats de projet dans le système.</span><span class="sxs-lookup"><span data-stu-id="2a886-123">This view lists all unbilled sales actuals that haven't been invoiced across all project contracts in the system.</span></span> <span data-ttu-id="2a886-124">Une ou plusieurs ventes réelles non facturées peuvent être marquées comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="2a886-124">Single or multiple unbilled sales actuals can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="2a886-125">Marquer une vente réelle non facturée comme étant **Prêt pour la facturation** la rend disponible afin qu'elle figure sur une facture provisoire.</span><span class="sxs-lookup"><span data-stu-id="2a886-125">Marking an unbilled sales actual as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="2a886-126">Les ventes réelles non facturées dont le statut **Ne pas dépasser** est **Échec** ne peuvent pas être marquées comme **Prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="2a886-126">Unbilled sales actuals that have a **Not-to-Exceed** status of **Failed** can't be marked as **Ready to Invoice**.</span></span> <span data-ttu-id="2a886-127">Si ces ventes réelles doivent être marquées comme telles, réinitialisez le statut des autres ventes réelles de la ligne de contrat qui sont validées, puis évaluez le statut **Ne pas dépasser**.</span><span class="sxs-lookup"><span data-stu-id="2a886-127">If these actuals need to be marked as such, reset the status on other actuals on the contract line that are committed, and then evaluate the **Not-to-Exceed** status.</span></span>

<span data-ttu-id="2a886-128">Dans le cas de lignes de contrat avec plusieurs clients ayant une méthode de facturation du temps et du matériel, lorsque le temps et les dépenses sont approuvés, une vente réelle non facturée est créée pour chaque client sur la ligne de contrat, selon le pourcentage de facturation défini pour chaque client sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="2a886-128">In the case of multi-customer contract lines that have a time and material billing method, when time and expenses are approved, an unbilled sales actual is created for each customer on the contract line according to the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="2a886-129">Dans la vue **Réplication de facturation pour le temps et le matériel** , vous verrez ces ventes réelles non facturées spécifiques au client.</span><span class="sxs-lookup"><span data-stu-id="2a886-129">In the **Time and Material Billing Backlog** view, you'll see these individual customer-specific unbilled sales actuals.</span></span> <span data-ttu-id="2a886-130">Chacun de ces enregistrements de vente réelle non facturée peut être marqué comme **Prêt pour la facturation** séparément dans cette vue.</span><span class="sxs-lookup"><span data-stu-id="2a886-130">Each of these unbilled sales actual records can be marked as **Ready to Invoice** separately from this view.</span></span>

<span data-ttu-id="2a886-131">Une vente réelle non facturée sur une facture provisoire est affichée dans cette vue avec le **Statut de facturation** **Facture client créée**.</span><span class="sxs-lookup"><span data-stu-id="2a886-131">An unbilled sales actual on a draft invoice is shown in this view with a **Billing Status** of **Customer Invoice Created**.</span></span> <span data-ttu-id="2a886-132">Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture client publiée**.</span><span class="sxs-lookup"><span data-stu-id="2a886-132">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> <span data-ttu-id="2a886-133">Lorsque ce statut est en vigueur, il n'est pas recommandé de mettre à jour cette valeur de statut à l'aide d'un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2a886-133">Updating this status value when it is in this state by using custom code isn't recommended.</span></span> <span data-ttu-id="2a886-134">Project Operations ne fonctionnera pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2a886-134">Project Operations won't function correctly when these status values are updated with custom code.</span></span>