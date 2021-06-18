---
title: Configurer les rôles de ressource
description: Procédure de configuration des rôles de ressources dans Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 59c66aa7bd6c481f8db3088bede71c1ab81a203f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999308"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="8ee07-103">Configurer des rôles de ressources (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8ee07-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8ee07-104">Les rôles jouent un rôle important dans la planification du projet, pour évaluer les besoins en ressources ou les coûts d’un projet.</span><span class="sxs-lookup"><span data-stu-id="8ee07-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="8ee07-105">Pour chaque rôle que vos projets requièrent, vous devez créer un rôle de ressource et associer des qualifications et des compétences à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="8ee07-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="8ee07-106">Par exemple, vous pouvez créer des rôles pour développeur, responsable de projet ou testeur de jeux.</span><span class="sxs-lookup"><span data-stu-id="8ee07-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="8ee07-107">Vous définirez également les qualifications et les niveaux de compétence nécessaires pour le rôle.</span><span class="sxs-lookup"><span data-stu-id="8ee07-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="8ee07-108">Configurez les rôles de ressource pour garantir une évaluation efficace du projet pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8ee07-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="8ee07-109">Assurez-vous également de définir précisément le type de facturation.</span><span class="sxs-lookup"><span data-stu-id="8ee07-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="8ee07-110">Un élément avec un type de facturation Non facturable n’apparaît pas dans le contrat ou le devis.</span><span class="sxs-lookup"><span data-stu-id="8ee07-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="8ee07-111">Une fois que vous avez configuré les rôles des ressources, vous pouvez configurer les coûts et prix de vente avec les tarifs.</span><span class="sxs-lookup"><span data-stu-id="8ee07-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="8ee07-112">Chaque fois que vous ajoutez un rôle, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ee07-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="8ee07-113">Accédez à **Project Service > Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="8ee07-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="8ee07-114">Cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="8ee07-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="8ee07-115">Dans la zone **Général**, donnez un nom au rôle dans **Nom**, puis complétez les autres champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8ee07-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="8ee07-116">Cliquez sur **Enregistrer** pour créer l’enregistrement et pouvoir continuer de le modifier.</span><span class="sxs-lookup"><span data-stu-id="8ee07-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="8ee07-117">Dans la zone **Qualifications**, cliquez sur **+** pour ajouter une qualification.</span><span class="sxs-lookup"><span data-stu-id="8ee07-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="8ee07-118">Dans le volet **Besoin en compétence du rôle**, cliquez sur le champ **Qualification**, cliquez sur le bouton **Rechercher**, puis sélectionnez une qualification.</span><span class="sxs-lookup"><span data-stu-id="8ee07-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="8ee07-119">Sélectionnez une compétence pour cette qualification, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8ee07-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="8ee07-120">Continuez d’ajouter des qualifications selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8ee07-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="8ee07-121">Lorsque vous avez fini, cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="8ee07-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="8ee07-122">Pour rendre ce rôle de ressource disponible pour des projets, cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="8ee07-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8ee07-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ee07-123">See Also</span></span>  
 [<span data-ttu-id="8ee07-124">Configurer les ressources</span><span class="sxs-lookup"><span data-stu-id="8ee07-124">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]