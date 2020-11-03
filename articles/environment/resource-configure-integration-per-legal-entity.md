---
title: Configurer l’intégration de Project Operations par entité juridique
description: Cette rubrique fournit des informations sur la configuration de l'intégration par entité juridique dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096749"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="13f07-103">Configurer l’intégration de Project Operations par entité juridique</span><span class="sxs-lookup"><span data-stu-id="13f07-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="13f07-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="13f07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="13f07-105">Cette rubrique vous explique comment configurer Dynamics 365 Project Operations par entité juridique.</span><span class="sxs-lookup"><span data-stu-id="13f07-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="13f07-106">Activer les clés de fonctionnalités dans Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="13f07-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="13f07-107">Effectuez les étapes suivantes pour activer les fonctionnalités requises.</span><span class="sxs-lookup"><span data-stu-id="13f07-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="13f07-108">Dans Dynamics 365 Finance, accédez à l'espace de travail **Gestion des données**.</span><span class="sxs-lookup"><span data-stu-id="13f07-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="13f07-109">Dans **Liste des fonctionnalités** , recherchez et activez les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="13f07-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="13f07-110">**Activer plusieurs lignes de contrat pour un projet**</span><span class="sxs-lookup"><span data-stu-id="13f07-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="13f07-111">**Activer Project Operations sur Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="13f07-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="13f07-112">Si vous ne voyez pas **Clés de fonctionnalités** dans la liste, assurez-vous que vous disposez de la version minimale requise pour Finance (version de l'application 10.0.13 avec toutes les mises à jour de qualité appliquées, ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="13f07-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="13f07-113">Sélectionnez **Rechercher les mises à jour** pour actualiser la liste des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="13f07-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="13f07-114">Définir le scénario de déploiement Project Operations pour une entité juridique</span><span class="sxs-lookup"><span data-stu-id="13f07-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="13f07-115">Vous pouvez activer Project Operations sur Dynamics 365 Customer Engagement au niveau d'une entité juridique.</span><span class="sxs-lookup"><span data-stu-id="13f07-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="13f07-116">Vous pouvez avoir une entité juridique utilisant Project Operations sur Dynamics 365 Customer Engagement pour les scénarios d'ordre non stocké / basé sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="13f07-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="13f07-117">Dans le même environnement, vous pouvez avoir une autre entité juridique utilisant Project Operations pour les scénarios d'ordre stocké / de fabrication.</span><span class="sxs-lookup"><span data-stu-id="13f07-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="13f07-118">Dans Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres globaux de gestion et comptabilité des projets**.</span><span class="sxs-lookup"><span data-stu-id="13f07-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="13f07-119">Dans la liste des entités juridiques disponibles, sélectionnez les entités pour lesquelles plusieurs lignes de contrat et les fonctionnalités Project Operations sur Dynamics 365 Customer Engagement seront activées.</span><span class="sxs-lookup"><span data-stu-id="13f07-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="13f07-120">Laissez non sélectionnées les entités juridiques qui utiliseront Project Operations pour les scénarios d'ordre stocké / de fabrication.</span><span class="sxs-lookup"><span data-stu-id="13f07-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="13f07-121">Une entité juridique ne peut être sélectionnée que si elle n'a aucun projet existant.</span><span class="sxs-lookup"><span data-stu-id="13f07-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="13f07-122">Configurer Paramètres de gestion et comptabilité des projets</span><span class="sxs-lookup"><span data-stu-id="13f07-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="13f07-123">Chaque entité juridique utilisant Project Operations sur Dynamics 365 Customer Engagement nécessite un ensemble de paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="13f07-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="13f07-124">Ces paramètres sont configurés sur l'onglet **Project Operations** sur la page **Paramètres de gestion et comptabilité des projets**.</span><span class="sxs-lookup"><span data-stu-id="13f07-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="13f07-125">Les paramètres sont :</span><span class="sxs-lookup"><span data-stu-id="13f07-125">The parameters are:</span></span>

  - <span data-ttu-id="13f07-126">**Valeurs par défaut du type de facturation**  : Project Operations utilise un ensemble fixe de valeurs par défaut du type de facturation qui doivent être mappées aux propriétés de ligne Finance.</span><span class="sxs-lookup"><span data-stu-id="13f07-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="13f07-127">Créez un enregistrement pour chaque type de facturation : **Non spécifié** , **Facturable** , **Non facturable** , **Gratuit** et **Non disponible**.</span><span class="sxs-lookup"><span data-stu-id="13f07-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="13f07-128">**Valeurs par défaut de la catégorie de projet**  : sélectionnez les catégories de projet par défaut à utiliser pour chaque type de transaction.</span><span class="sxs-lookup"><span data-stu-id="13f07-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="13f07-129">Ces valeurs par défaut seront utilisées dans le **Journal d’intégration de Project Operations** et dans les estimations où aucune catégorie de transaction n'est spécifiée pour les chiffres réels du projet.</span><span class="sxs-lookup"><span data-stu-id="13f07-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="13f07-130">**Prévisions**  : sélectionnez le modèle de prévision à utiliser pour les estimations de temps et de dépenses.</span><span class="sxs-lookup"><span data-stu-id="13f07-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
