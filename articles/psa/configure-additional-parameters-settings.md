---
title: Configurer des paramètres supplémentaires
description: Procédure de configuration de paramètres supplémentaires dans Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290761"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="f98a6-103">Configurer des paramètres supplémentaires (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f98a6-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f98a6-104">Une fois que vous avez configuré les éléments des rubriques précédentes, vous devez définir des paramètres de projet supplémentaires à utiliser pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="f98a6-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="f98a6-105">Quand vous avez installé le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour la première fois, vous avez créé les paramètres pour créer d’abord tous les enregistrements requis pour que [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fonctionne.</span><span class="sxs-lookup"><span data-stu-id="f98a6-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="f98a6-106">Maintenant il est temps de revenir en arrière et de configurer des champs supplémentaires pour ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="f98a6-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="f98a6-107">Vous devez avoir configuré les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f98a6-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="f98a6-108">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="f98a6-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="f98a6-109">Fréquence de facture</span><span class="sxs-lookup"><span data-stu-id="f98a6-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="f98a6-110">Modèle d’heures de travail</span><span class="sxs-lookup"><span data-stu-id="f98a6-110">Work hours template</span></span>  
  
-   <span data-ttu-id="f98a6-111">Tarifs</span><span class="sxs-lookup"><span data-stu-id="f98a6-111">Price list</span></span>  
 
<span data-ttu-id="f98a6-112">Dans cette étape, vous allez indiquer le type d’allocation de ressources que vous souhaitez :</span><span class="sxs-lookup"><span data-stu-id="f98a6-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="f98a6-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="f98a6-113">**Central**.</span></span> <span data-ttu-id="f98a6-114">Seuls les gestionnaires de ressources peuvent allouer des ressources à des projets.</span><span class="sxs-lookup"><span data-stu-id="f98a6-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="f98a6-115">**Hybride**.</span><span class="sxs-lookup"><span data-stu-id="f98a6-115">**Hybrid**.</span></span> <span data-ttu-id="f98a6-116">Les gestionnaires de ressources, les responsables de projet et les responsables de compte peuvent allouer des ressources à des projets.</span><span class="sxs-lookup"><span data-stu-id="f98a6-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="f98a6-117">Pour définir les paramètres de projet :</span><span class="sxs-lookup"><span data-stu-id="f98a6-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="f98a6-118">Accédez à **Project Service > Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="f98a6-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="f98a6-119">Cliquez sur le paramètre que vous souhaitez configurer (celui créé lors de la première installation du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ou cliquez sur **Nouveau** pour en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="f98a6-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="f98a6-120">Dans la zone **Général**, définissez toutes les options de vos paramètres du projet.</span><span class="sxs-lookup"><span data-stu-id="f98a6-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="f98a6-121">Dans la zone **Tarifs**, cliquez sur **+** pour ajouter des tarifs, sélectionnez des tarifs dans la liste déroulante **Tarifs du paramètre du projet**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f98a6-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="f98a6-122">Cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="f98a6-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="f98a6-123">L’enregistrement des paramètres du projet doit être conservé pour que Project Service fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="f98a6-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="f98a6-124">Cet enregistrement ne doit pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="f98a6-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="f98a6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f98a6-125">See Also</span></span>  
 [<span data-ttu-id="f98a6-126">Configurer les ressources</span><span class="sxs-lookup"><span data-stu-id="f98a6-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]