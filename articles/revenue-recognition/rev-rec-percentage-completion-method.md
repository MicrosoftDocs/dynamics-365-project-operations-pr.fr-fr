---
title: Projets d’estimation de revenus à prix fixe
description: Cette rubrique fournit des informations sur les projets d’estimation de revenus à prix fixe.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531420"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="8aa66-103">Projets d’estimation de revenus à prix fixe</span><span class="sxs-lookup"><span data-stu-id="8aa66-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="8aa66-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="8aa66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8aa66-105">Lorsque vous créez une ligne de contrat de projet avec les attributs suivants dans Dynamics 365 Project Operations sur Microsoft Dataverse, le système crée automatiquement un projet d'estimation des revenus à prix fixe.</span><span class="sxs-lookup"><span data-stu-id="8aa66-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="8aa66-106">Les informations de ce projet reposent sur les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8aa66-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="8aa66-107">Une méthode de facturation à prix fixe.</span><span class="sxs-lookup"><span data-stu-id="8aa66-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="8aa66-108">Un projet associé.</span><span class="sxs-lookup"><span data-stu-id="8aa66-108">An associated project.</span></span>
  - <span data-ttu-id="8aa66-109">Au moins un jalon défini sur l'onglet **Calendrier de facturation** de la page **Ligne de contrat de projet**.</span><span class="sxs-lookup"><span data-stu-id="8aa66-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="8aa66-110">Réviser des projets d’estimation de revenus à prix fixe</span><span class="sxs-lookup"><span data-stu-id="8aa66-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="8aa66-111">Pour réviser des projets d'estimation des revenus à prix fixe, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8aa66-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="8aa66-112">Dans l'environnement Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Projets** > **Projets d'estimation de revenus à prix fixe**.</span><span class="sxs-lookup"><span data-stu-id="8aa66-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="8aa66-113">Sélectionnez le projet que vous souhaitez afficher et double-cliquez sur **ID projet d'estimation** pour ouvrir l'enregistrement et revoir les détails du projet.</span><span class="sxs-lookup"><span data-stu-id="8aa66-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="8aa66-114">Développez l'onglet **Projet**. Vous verrez un projet dans la grille **Projets sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="8aa66-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="8aa66-115">Le système l'utilise comme projet par défaut car il s'agit du projet associé à la ligne de contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="8aa66-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="8aa66-116">Pour modifier l'association, sélectionnez des projets supplémentaires et ajoutez-les à la grille **Projets sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="8aa66-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="8aa66-117">Si plusieurs projets sont sélectionnés dans cette grille, le pourcentage d'achèvement du projet et les estimations de revenus sont calculés ensemble pour tous les projets sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="8aa66-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="8aa66-118">Le coût du projet, le profil de revenu, le modèle de coût et le code de période peuvent être définis manuellement.</span><span class="sxs-lookup"><span data-stu-id="8aa66-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="8aa66-119">S'ils ne sont pas définis manuellement, les valeurs sont définies par défaut lors du premier calcul d'estimation du projet à l'aide des règles configurées pour les profils de coût et de revenu du projet.</span><span class="sxs-lookup"><span data-stu-id="8aa66-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

