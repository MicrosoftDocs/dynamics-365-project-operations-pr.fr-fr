---
title: Nouveautés de mars 2021 – Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de mars 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993863"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="42033-103">Nouveautés de mars 2021 – Déploiement simplifié de Project Operations</span><span class="sxs-lookup"><span data-stu-id="42033-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="42033-104">_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="42033-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="42033-105">Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :</span><span class="sxs-lookup"><span data-stu-id="42033-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="42033-106">Version 4.8.0.91 de Project Operations dans l’environnement Dataverse</span><span class="sxs-lookup"><span data-stu-id="42033-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="42033-107">Mises à jour qualité</span><span class="sxs-lookup"><span data-stu-id="42033-107">Quality updates</span></span>

| <span data-ttu-id="42033-108">**Fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="42033-108">**Feature area**</span></span> | <span data-ttu-id="42033-109">**Numéro de référence**</span><span class="sxs-lookup"><span data-stu-id="42033-109">**Reference number**</span></span> | <span data-ttu-id="42033-110">**Mise à jour qualité**</span><span class="sxs-lookup"><span data-stu-id="42033-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="42033-111">Facturation et tarification</span><span class="sxs-lookup"><span data-stu-id="42033-111">Billing and pricing</span></span> | <span data-ttu-id="42033-112">2133873</span><span class="sxs-lookup"><span data-stu-id="42033-112">2133873</span></span> | <span data-ttu-id="42033-113">Correction de l’affichage du symbole monétaire du **Prix de vente unitaire** dans la grille **Estimations des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="42033-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="42033-114">Facturation et tarification</span><span class="sxs-lookup"><span data-stu-id="42033-114">Billing and pricing</span></span> | <span data-ttu-id="42033-115">2174616</span><span class="sxs-lookup"><span data-stu-id="42033-115">2174616</span></span> | <span data-ttu-id="42033-116">Lorsqu’un devis est conclu, la liste de prix personnalisée du contrat est référencée dans les détails de la ligne du contrat qui sont copiés à partir du devis.</span><span class="sxs-lookup"><span data-stu-id="42033-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="42033-117">Gestion des opportunités</span><span class="sxs-lookup"><span data-stu-id="42033-117">Opportunity Management</span></span> | <span data-ttu-id="42033-118">2167475</span><span class="sxs-lookup"><span data-stu-id="42033-118">2167475</span></span> | <span data-ttu-id="42033-119">Montant de taxe fixe dans la facture de correction à l’origine d’une entrée réelle non facturée.</span><span class="sxs-lookup"><span data-stu-id="42033-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="42033-120">Gestion des opportunités</span><span class="sxs-lookup"><span data-stu-id="42033-120">Opportunity Management</span></span> | <span data-ttu-id="42033-121">2176285</span><span class="sxs-lookup"><span data-stu-id="42033-121">2176285</span></span> | <span data-ttu-id="42033-122">Le montant de la taxe ne doit pas être copié depuis les détails du contrat de vente/de la ligne de devis vers les détails du contrat de coût/de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="42033-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="42033-123">Gestion des opportunités</span><span class="sxs-lookup"><span data-stu-id="42033-123">Opportunity Management</span></span> | <span data-ttu-id="42033-124">2188079</span><span class="sxs-lookup"><span data-stu-id="42033-124">2188079</span></span> | <span data-ttu-id="42033-125">Une règle de facturation fractionnée ne doit pas être créée pour les contrats qui ne sont pas basés sur le travail.</span><span class="sxs-lookup"><span data-stu-id="42033-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="42033-126">Planification et suivi</span><span class="sxs-lookup"><span data-stu-id="42033-126">Planning and Tracking</span></span> | <span data-ttu-id="42033-127">2138853</span><span class="sxs-lookup"><span data-stu-id="42033-127">2138853</span></span> | <span data-ttu-id="42033-128">La fonction de copie du projet a été mise à jour pour s’assurer que les lignes d’estimation des dépenses faisant référence aux tâches sont copiées dans le projet de destination.</span><span class="sxs-lookup"><span data-stu-id="42033-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="42033-129">Planification et suivi</span><span class="sxs-lookup"><span data-stu-id="42033-129">Planning and Tracking</span></span> | <span data-ttu-id="42033-130">2173259</span><span class="sxs-lookup"><span data-stu-id="42033-130">2173259</span></span> | <span data-ttu-id="42033-131">La fonction de copie du projet a été mise à jour pour garantir que le message d’erreur **Copie de WBS** ne s’affiche pas dans certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="42033-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="42033-132">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="42033-132">Time and Expense</span></span> | <span data-ttu-id="42033-133">2148910</span><span class="sxs-lookup"><span data-stu-id="42033-133">2148910</span></span> | <span data-ttu-id="42033-134">Résolution du problème d’affichage de la page **Modifier l’entrée** dans la grillle **Entrée de temps**.</span><span class="sxs-lookup"><span data-stu-id="42033-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="42033-135">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="42033-135">Time and Expense</span></span> | <span data-ttu-id="42033-136">2159798</span><span class="sxs-lookup"><span data-stu-id="42033-136">2159798</span></span> | <span data-ttu-id="42033-137">Contrôles plus stricts pour garantir que les entrées de dépenses approuvées ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="42033-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


