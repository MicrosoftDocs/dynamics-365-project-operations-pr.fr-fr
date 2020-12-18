---
title: Types de période
description: Cette rubrique fournit des informations sur la manière de configurer des types de période pour une estimation de revenus.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531419"
---
# <a name="period-types"></a><span data-ttu-id="ae889-103">Types de période</span><span class="sxs-lookup"><span data-stu-id="ae889-103">Period types</span></span>

<span data-ttu-id="ae889-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="ae889-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae889-105">Un type de période définit la fréquence à laquelle les revenus d'un projet sont estimés.</span><span class="sxs-lookup"><span data-stu-id="ae889-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="ae889-106">Cette rubrique fournit des informations sur la manière de configurer des types de période pour une estimation de revenus.</span><span class="sxs-lookup"><span data-stu-id="ae889-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="ae889-107">Créer et utiliser des types de période</span><span class="sxs-lookup"><span data-stu-id="ae889-107">Create and work with period types</span></span>
<span data-ttu-id="ae889-108">Pour créer et utiliser des types de période, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae889-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="ae889-109">Dans votre environnement Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Estimations** > **Types de période**.</span><span class="sxs-lookup"><span data-stu-id="ae889-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="ae889-110">Sélectionnez **Nouveau** pour créer un nouveau type de période.</span><span class="sxs-lookup"><span data-stu-id="ae889-110">Select **New** to create new period type.</span></span> <span data-ttu-id="ae889-111">Entrez un nom et une description.</span><span class="sxs-lookup"><span data-stu-id="ae889-111">Enter a name and description.</span></span>
3. <span data-ttu-id="ae889-112">Dans le champ **Fréquence**, sélectionnez une valeur :</span><span class="sxs-lookup"><span data-stu-id="ae889-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="ae889-113">Si vous sélectionnez **Semaine**, **Bihebdomadaire**, **Semi-mensuelle**, **Mois**, **Jour**, **Trimestre** ou **Année**, le calendrier sera utilisé pour générer les périodes.</span><span class="sxs-lookup"><span data-stu-id="ae889-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="ae889-114">Si vous sélectionnez **Période comptable**, les périodes comptables de la configuration de comptabilité seront utilisées pour générer des périodes.</span><span class="sxs-lookup"><span data-stu-id="ae889-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="ae889-115">Si vous sélectionnez **Illimité**, vous pouvez spécifier des périodes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ae889-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="ae889-116">Sélectionnez l'enregistrement de type de période, puis sélectionnez **Générer des périodes** pour créer des périodes pour le type de période.</span><span class="sxs-lookup"><span data-stu-id="ae889-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="ae889-117">En fonction de la fréquence de période que vous avez sélectionnée, vous avez la possibilité de spécifier une date de début ou le nombre de périodes à générer.</span><span class="sxs-lookup"><span data-stu-id="ae889-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="ae889-118">Sélectionnez **Périodes** pour revoir les périodes générées.</span><span class="sxs-lookup"><span data-stu-id="ae889-118">Select **Periods** to review generated periods.</span></span>

