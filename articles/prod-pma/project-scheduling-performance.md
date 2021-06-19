---
title: Performances de la planification de ressources projet
description: Cette rubrique fournit des informations sur la manière d’améliorer les performances de la planification des ressources pour un grand nombre de projets.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010018"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="a802a-103">Performances de la planification de ressources projet</span><span class="sxs-lookup"><span data-stu-id="a802a-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="a802a-104">Des problèmes de performances liés à la planification des ressources peuvent survenir lorsque le nombre de projets atteint des milliers.</span><span class="sxs-lookup"><span data-stu-id="a802a-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="a802a-105">Pour améliorer les performances de planification des ressources, une fonctionnalité est disponible qui permet aux utilisateurs de réduire le temps nécessaire pour lancer le formulaire de disponibilité des ressources.</span><span class="sxs-lookup"><span data-stu-id="a802a-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="a802a-106">Plus précisément, cela supprime le processus de synchronisation de cumul de capacité des ressources et utilise la table **ResProjectResource** pour accélérer la recherche de ressources.</span><span class="sxs-lookup"><span data-stu-id="a802a-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="a802a-107">Notez que la table **ResRollup** ne sera plus utilisée.</span><span class="sxs-lookup"><span data-stu-id="a802a-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a802a-108">S’il existe une dépendance sur le processus de synchronisation de cumul de capacité des ressources ou sur la table **ResProjectResource**, n’utilisez pas cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a802a-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a802a-109">Activer l’amélioration des performances de planification des ressources</span><span class="sxs-lookup"><span data-stu-id="a802a-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="a802a-110">Pour activer l’amélioration des performances de planification des ressources, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a802a-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="a802a-111">Aller à **Gestion des fonctionnalités** > **Tout**, et dans la liste des fonctionnalités, recherchez **Activer la fonctionnalité d’amélioration des performances de planification des ressources de projet**.</span><span class="sxs-lookup"><span data-stu-id="a802a-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a802a-112">Sélectionnez **Activer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="a802a-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="a802a-113">Si vous ne trouvez pas la fonction dans la liste, sélectionnez **Rechercher des mises à jour** pour actualiser la liste.</span><span class="sxs-lookup"><span data-stu-id="a802a-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="a802a-114">Actualisez votre navigateur, puis accédez à **Gestion de projet et comptabilité** > **Périodique** > **Ressources du projet** > **Synchroniser la capacité des calendriers de ressources dans toutes les entreprises**.</span><span class="sxs-lookup"><span data-stu-id="a802a-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="a802a-115">Définissez **Supprimer les enregistrements de capacité existants** sur **Oui** pour supprimer les données précédentes.</span><span class="sxs-lookup"><span data-stu-id="a802a-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a802a-116">Si vous souhaitez générer des données incrémentielles, définissez-le sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="a802a-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="a802a-117">Dans le champ **Code de période**, sélectionnez la période pendant laquelle les données doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="a802a-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a802a-118">Si vous sélectionnez un code de période, il n’est pas nécessaire de définir une date de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="a802a-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="a802a-119">Si vous laissez le champ **Code de période** vide, sélectionnez des dates de début et de fin spécifiques pour générer des données.</span><span class="sxs-lookup"><span data-stu-id="a802a-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="a802a-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a802a-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a802a-121">Cela distribuera des données générales à la table **ResCalendarCapacity** dans toutes les entreprises de votre environnement, de sorte que le traitement par lots ne doive être exécuté que dans une seule entité juridique.</span><span class="sxs-lookup"><span data-stu-id="a802a-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a802a-122">Les données de ce traitement par lots sont nécessaires pour calculer la capacité des ressources par le biais du calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="a802a-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="a802a-123">Aller à **Gestion de projet et comptabilité** > **Périodique** > **Ressources du projet** > **Remplir les ressources de projet dans toutes les entreprises**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="a802a-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="a802a-124">Il s’agit du script de mise à niveau des données pour les données générales dans les tables **ResProjectResource**, **ResCalendarDateTimeRange** et **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="a802a-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="a802a-125">Les valeurs du champ **PSAPRojSchedRole.RootActivity** sont également mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a802a-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="a802a-126">Si ce n’est pas exécuté, vous recevrez un avertissement lorsque vous essayez d’exécuter des opérations de planification des ressources.</span><span class="sxs-lookup"><span data-stu-id="a802a-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a802a-127">Désactiver l’amélioration des performances de planification des ressources</span><span class="sxs-lookup"><span data-stu-id="a802a-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="a802a-128">Aller à **Gestion des fonctionnalités** > **Tout** et recherchez **Activer la fonctionnalité d’amélioration des performances de planification des ressources de projet**.</span><span class="sxs-lookup"><span data-stu-id="a802a-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a802a-129">Sélectionnez la fonctionnalité, puis cliquez sur le bouton **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="a802a-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="a802a-130">Actualisez votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="a802a-130">Refresh your browser.</span></span>
4. <span data-ttu-id="a802a-131">Accédez à **Gestion de projets et comptabilité** > **Périodique** > **Synchronisation des capacités** > **Synchroniser les reports de capacité des ressources**.</span><span class="sxs-lookup"><span data-stu-id="a802a-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="a802a-132">Sur la page **Synchronisation de cumul de capacité**, définissez **Supprimer les enregistrements de capacité existants** sur **Oui** pour supprimer les données précédentes.</span><span class="sxs-lookup"><span data-stu-id="a802a-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a802a-133">Si vous souhaitez générer des données incrémentielles, définissez-le sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="a802a-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="a802a-134">Dans le champ **Code de période**, sélectionnez la période pendant laquelle les données doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="a802a-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a802a-135">Si vous sélectionnez un code de période, il n’est pas nécessaire de définir une date de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="a802a-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="a802a-136">Si vous laissez le champ **Code de période** vide, sélectionnez des dates de début et de fin spécifiques pour générer des données.</span><span class="sxs-lookup"><span data-stu-id="a802a-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="a802a-137">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a802a-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a802a-138">Cela distribuera des données générales à la table **ResRollup** dans toutes les entreprises de votre environnement, de sorte que le traitement par lots ne doive être exécuté que dans une seule entité juridique.</span><span class="sxs-lookup"><span data-stu-id="a802a-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a802a-139">Ce traitement par lots est nécessaire pour toutes les vues **Disponibilité des ressources**.</span><span class="sxs-lookup"><span data-stu-id="a802a-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="a802a-140">Si ce traitement par lots n’est pas exécuté, les données **ResRollup** seront générées à la volée, ce qui peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="a802a-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]