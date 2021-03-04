---
title: Fournir des estimations de travail pour un projet pendant le processus de vente
description: Procédure de fourniture des estimations de travail pour un projet pendant le processus de vente dans Project Service
author: ruhercul
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
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147965"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="99750-103">Fournir des estimations de travail pour un projet pendant le processus de vente (Project Service)</span><span class="sxs-lookup"><span data-stu-id="99750-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="99750-104">Durant le processus de vente, vous pouvez créer des estimations de vente à partir du début jusqu’aux lignes de devis.</span><span class="sxs-lookup"><span data-stu-id="99750-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="99750-105">Les fonctionnalités du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dans [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] offrent un moyen plus scientifique et plus déterministe de proposer des estimations de vente en décomposant des éléments de travail et en associant les attributs adéquats qui peuvent contribuer aux estimations du projet dans la structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="99750-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="99750-106">Une fois que vous ayez conclu la vente, vous pouvez utiliser la structure de répartition du travail associée dans votre plan de projet, l’affinant selon les besoins pour achever votre projet avec succès.</span><span class="sxs-lookup"><span data-stu-id="99750-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="99750-107">Lier un projet à une ligne de devis</span><span class="sxs-lookup"><span data-stu-id="99750-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="99750-108">Lorsque vous créez une ligne de devis basée sur un projet, vous pouvez créer un nouveau projet depuis la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="99750-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="99750-109">Vous pouvez ensuite utiliser les modèles de projet, qui sont des plans de projet standard préconfigurés et des estimations financières courantes à votre organisation, ou une copie d’un plan de projet et des estimations d’un projet précédent.</span><span class="sxs-lookup"><span data-stu-id="99750-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="99750-110">Lorsque vous créez un projet, choisir un modèle de projet constitue une base pour affiner le plan de projet, les estimations, et les besoins relatifs aux rôles.</span><span class="sxs-lookup"><span data-stu-id="99750-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="99750-111">En créant votre projet depuis le devis, le projet est automatiquement associé à la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="99750-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="99750-112">Composants d’évaluation de projet</span><span class="sxs-lookup"><span data-stu-id="99750-112">Project estimate components</span></span>  
 <span data-ttu-id="99750-113">La structure de répartition du travail dans un projet permet de décomposer le travail en tâches, de conserver une hiérarchie des tâches, et d’attribuer une évaluation de l’effort nécessaire pour effectuer chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="99750-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="99750-114">Vous pouvez également associer des rôles à une tâche pour indiquer une évaluation du type de ressources requises pour effectuer une tâche et un programme.</span><span class="sxs-lookup"><span data-stu-id="99750-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="99750-115">La structure de répartition du travail vous permet de déterminer l’effort de travail et de planifier des estimations.</span><span class="sxs-lookup"><span data-stu-id="99750-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="99750-116">Par défaut, le projet utilise les tarifs par défaut que vous avez définis auparavant.</span><span class="sxs-lookup"><span data-stu-id="99750-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="99750-117">Les coûts et les prix de vente définis dans les tarifs aident à déterminer les estimations financières pour la répartition du travail du projet.</span><span class="sxs-lookup"><span data-stu-id="99750-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="99750-118">Si votre projet est associé à un devis, et le devis a des tarifs différent des valeurs par défaut, les tarifs du devis sont utilisés pour les estimations financières.</span><span class="sxs-lookup"><span data-stu-id="99750-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="99750-119">Importer des estimations depuis un projet dans un devis</span><span class="sxs-lookup"><span data-stu-id="99750-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="99750-120">Une fois que vous avez des estimations de projet dans le projet, vous pouvez importer ces estimations dans la ligne de devis :</span><span class="sxs-lookup"><span data-stu-id="99750-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="99750-121">Dans **Détails de la ligne de devis**, cliquez sur **Importer à partir des estimations**.</span><span class="sxs-lookup"><span data-stu-id="99750-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="99750-122">Choisissez d’importer ou non des estimations de projet synthétisées par type de transaction, rôle, ou niveau de nœud de structure de répartition du travail.</span><span class="sxs-lookup"><span data-stu-id="99750-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="99750-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99750-123">See Also</span></span>  
 [<span data-ttu-id="99750-124">Guide du responsable de projet</span><span class="sxs-lookup"><span data-stu-id="99750-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
