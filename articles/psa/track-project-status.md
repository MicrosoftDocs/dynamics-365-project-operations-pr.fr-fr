---
title: Suivre le statut d’un projet
description: Procédure de suivi du statut d’un projet dans Project Service
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281925"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="d6803-103">Suivre le statut d’un projet (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d6803-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d6803-104">Utilisez le [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] pour suivre la progression du projet d’un client.</span><span class="sxs-lookup"><span data-stu-id="d6803-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="d6803-105">À mesure que l’engagement progresse, les phases du projet sont mises à jour pour refléter la phase de l’engagement :</span><span class="sxs-lookup"><span data-stu-id="d6803-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="d6803-106">**Nouveau**</span><span class="sxs-lookup"><span data-stu-id="d6803-106">**New**</span></span>    | <span data-ttu-id="d6803-107">Lorsque vous créez un projet, la phase est définie sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="d6803-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="d6803-108">Si vous créez le projet à partir d’un modèle, à cette phase le projet peut avoir un calendrier, des estimations et les données d’équipe.</span><span class="sxs-lookup"><span data-stu-id="d6803-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="d6803-109">Sinon, celui-ci sera le plan du projet et vous devez entrer manuellement le reste des composants du projet.</span><span class="sxs-lookup"><span data-stu-id="d6803-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="d6803-110">**devis**</span><span class="sxs-lookup"><span data-stu-id="d6803-110">**Quote**</span></span>   |      <span data-ttu-id="d6803-111">Lorsque vous associez un projet à un devis ou le créez depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimée sont également mises à jour.</span><span class="sxs-lookup"><span data-stu-id="d6803-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="d6803-112">Lorsque le projet est dans la phase de devis, les informations sur le devis s’affichent sous l’onglet **Sales** dans la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="d6803-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="d6803-113">**Planifier**</span><span class="sxs-lookup"><span data-stu-id="d6803-113">**Plan**</span></span>   |                                     <span data-ttu-id="d6803-114">Lorsque vous ayez conclu un devis associé à un projet, et lorsque l’engagement progresse vers la phase de contrat, la phase de projet est mise à jour sur **Planifier**.</span><span class="sxs-lookup"><span data-stu-id="d6803-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="d6803-115">Les détails de contrat s’affichent sous l’onglet **Sales** dans la page **Projet**.</span><span class="sxs-lookup"><span data-stu-id="d6803-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="d6803-116">**Fin**</span><span class="sxs-lookup"><span data-stu-id="d6803-116">**Complete**</span></span> |                    <span data-ttu-id="d6803-117">Lorsque la tâche de projet est terminée, vous pouvez revenir vers la phase **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="d6803-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="d6803-118">Lorsque la phase de projet est définie sur terminée, la tâche est terminée à 100 % mais le projet est maintenu ouvert en attendant l’enregistrement du temps ou des dépenses.</span><span class="sxs-lookup"><span data-stu-id="d6803-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="d6803-119">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="d6803-119">**Close**</span></span>   |           <span data-ttu-id="d6803-120">Lorsque toutes les transactions ont été enregistrées sur le projet et que vous ne prévoyez plus de saisir de données, vous pouvez manuellement définir la phase sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d6803-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="d6803-121">Lorsque le contrat est défini sur **Fermer**, vous ne pouvez plus enregistrer de transactions sur le projet et le projet est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d6803-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="d6803-122">Pour suivre le statut d’un projet</span><span class="sxs-lookup"><span data-stu-id="d6803-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="d6803-123">Accédez à **Project Service > Projets**.</span><span class="sxs-lookup"><span data-stu-id="d6803-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="d6803-124">Cliquez sur le projet sur lequel vous souhaitez travailler.</span><span class="sxs-lookup"><span data-stu-id="d6803-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="d6803-125">Dans la barre dans toute la partie supérieure de l’écran, sélectionnez la flèche vers le bas en regard du nom de projet, puis cliquez sur **Suivi du projet**.</span><span class="sxs-lookup"><span data-stu-id="d6803-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="d6803-126">Sélectionnez **Suivi de l’effort** ou **Suivi du coût** dans la liste déroulante au-dessus de la liste des tâches.</span><span class="sxs-lookup"><span data-stu-id="d6803-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="d6803-127">Double-cliquez sur une tâche pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="d6803-127">Double-click any task to edit it.</span></span> <span data-ttu-id="d6803-128">Vous pouvez également déplacer ou redimensionner les barres dans le diagramme de Gantt pour modifier le temps et la progression d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d6803-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="d6803-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6803-129">See Also</span></span>  
 [<span data-ttu-id="d6803-130">Guide du responsable de projet</span><span class="sxs-lookup"><span data-stu-id="d6803-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]