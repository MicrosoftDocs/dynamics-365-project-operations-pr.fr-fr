---
title: Vue d’ensemble des dépenses
description: Cette rubrique offre des informations sur la fonctionnalité Dépenses dans Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2a26b321e15080cc6a4a6a3ed410be175e790a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995393"
---
# <a name="expense-home-page"></a><span data-ttu-id="015f8-103">Page d’accueil des dépenses</span><span class="sxs-lookup"><span data-stu-id="015f8-103">Expense home page</span></span>

<span data-ttu-id="015f8-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="015f8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="015f8-105">Dynamics 365 Project Operations prend en charge la possibilité de traiter les dépenses.</span><span class="sxs-lookup"><span data-stu-id="015f8-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="015f8-106">Le traitement des dépenses se déroule avec ou sans projets à l’aide d’un flux de travail personnalisable de stratégies, de catégories de transactions et d’approbations.</span><span class="sxs-lookup"><span data-stu-id="015f8-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="015f8-107">Dans Project Operations, il existe deux modèles de déploiement pris en charge pour les dépenses :</span><span class="sxs-lookup"><span data-stu-id="015f8-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="015f8-108">**Complet** : Le déploiement complet est disponible pour **Project Operations pour les scénarios basés sur les ressources/non stockés** ou **Project Operations pour les scénarios basés sur les ordres de fabrication**.</span><span class="sxs-lookup"><span data-stu-id="015f8-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="015f8-109">**De base** : Le déploiement de base est disponible pour **Project Operations pour les scénarios basés sur les ressources/non stockés** et **Déploiement simplifié – Traiter la facturation pro forma**.</span><span class="sxs-lookup"><span data-stu-id="015f8-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="015f8-110">Complet</span><span class="sxs-lookup"><span data-stu-id="015f8-110">Full</span></span> 
<span data-ttu-id="015f8-111">Le déploiement des dépenses complet fournit une application de stratégie complète qui inclut la possibilité de créer des stratégies, telles que :</span><span class="sxs-lookup"><span data-stu-id="015f8-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="015f8-112">Limites de catégorie de dépenses</span><span class="sxs-lookup"><span data-stu-id="015f8-112">Expense category limits</span></span>
  - <span data-ttu-id="015f8-113">Voyages et déplacements</span><span class="sxs-lookup"><span data-stu-id="015f8-113">Travel</span></span>
  - <span data-ttu-id="015f8-114">Indemnités journalières</span><span class="sxs-lookup"><span data-stu-id="015f8-114">Per diem</span></span>
  - <span data-ttu-id="015f8-115">Importations d’une carte de crédit</span><span class="sxs-lookup"><span data-stu-id="015f8-115">Credit card imports</span></span>
  - <span data-ttu-id="015f8-116">Reconnaissance optique des caractères du reçu</span><span class="sxs-lookup"><span data-stu-id="015f8-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="015f8-117">De base</span><span class="sxs-lookup"><span data-stu-id="015f8-117">Basic</span></span> 
<span data-ttu-id="015f8-118">Le scénario de déploiement des dépenses de base vous permet uniquement d’enregistrer les dépenses de base par rapport à un projet.</span><span class="sxs-lookup"><span data-stu-id="015f8-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="015f8-119">Pour plus d’informations, consultez [Saisie des dépenses (simplifiée)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="015f8-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="015f8-120">Déterminer votre déploiement de dépenses</span><span class="sxs-lookup"><span data-stu-id="015f8-120">Determine your Expense deployment</span></span>
<span data-ttu-id="015f8-121">Pour déterminer si vous exécutez le déploiement de la gestion des dépenses de base, vérifiez que l’URL de l’adresse se termine par **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="015f8-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]