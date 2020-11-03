---
title: Activer des fonctionnalités de l'application Project Finder Mobile
description: Procédure d'activation des fonctionnalités de l'application Project Finder Mobile pour Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075747"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="994fc-103">Activer des fonctionnalités de l'application Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="994fc-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="994fc-104">Vos ressources peuvent utiliser l'application Project Finder Mobile sur leur téléphone avec le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour rechercher de nouveaux projets sur lesquels travailler et pour mettre à jour leurs compétences.</span><span class="sxs-lookup"><span data-stu-id="994fc-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="994fc-105">L'application est disponibles pour les téléphones [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] et [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="994fc-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="994fc-106">Vous devez définir des options dans les paramètres définissant de votre unité d'organisation pour permettre aux utilisateurs de consulter les exigences ressources et mettre à jour leurs compétences.</span><span class="sxs-lookup"><span data-stu-id="994fc-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="994fc-107">L'application mobile Project Finder Mobile fonctionne uniquement avec [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], pas sur les installations sur site.</span><span class="sxs-lookup"><span data-stu-id="994fc-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="994fc-108">Accédez à **Project Service > Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="994fc-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="994fc-109">Cliquez sur la configuration des paramètres que vous souhaitez utiliser pour autoriser les fonctionnalités de l'application Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="994fc-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="994fc-110">Dans la zone **Général** , définissez **Besoins en ressources visibles pour les ressources** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="994fc-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="994fc-111">Définissez **Autoriser la mise à jour des qualifications par ressource** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="994fc-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="994fc-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="994fc-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="994fc-113">Il s'agit d'un paramètre global.</span><span class="sxs-lookup"><span data-stu-id="994fc-113">This is a global setting.</span></span> <span data-ttu-id="994fc-114">Les responsables de projet peuvent définir les projets qui apparaissent sur la page **Équipe projet** de ce projet.</span><span class="sxs-lookup"><span data-stu-id="994fc-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="994fc-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="994fc-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="994fc-116">Notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="994fc-116">Email notifications</span></span>  
 <span data-ttu-id="994fc-117">Le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envoie les messages électroniques concernant les demandes de ressources aux destinataires suivants aux heures suivantes :</span><span class="sxs-lookup"><span data-stu-id="994fc-117">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="994fc-118">Destinataire</span><span class="sxs-lookup"><span data-stu-id="994fc-118">Recipient</span></span>|<span data-ttu-id="994fc-119">Événement</span><span class="sxs-lookup"><span data-stu-id="994fc-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="994fc-120">Gestionnaire de projet</span><span class="sxs-lookup"><span data-stu-id="994fc-120">Project manager</span></span>|<span data-ttu-id="994fc-121">-   Lorsqu'une ressource s'abonne à un projet avec l'application Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="994fc-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="994fc-122">Ressource</span><span class="sxs-lookup"><span data-stu-id="994fc-122">Resource</span></span>|<span data-ttu-id="994fc-123">-   Lorsque la tâche de projet à laquelle la ressource s'est abonnée a déjà été réalisée par une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="994fc-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="994fc-124">-   Lorsque leur demande d'approbation de qualification a été approuvée ou rejetée.</span><span class="sxs-lookup"><span data-stu-id="994fc-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="994fc-125">-   Lorsque leur demande d'inscription au projet a été approuvée ou rejetée.</span><span class="sxs-lookup"><span data-stu-id="994fc-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="994fc-126">Avis de confidentialité</span><span class="sxs-lookup"><span data-stu-id="994fc-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="994fc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="994fc-127">See Also</span></span>  
 [<span data-ttu-id="994fc-128">Configurer les ressources</span><span class="sxs-lookup"><span data-stu-id="994fc-128">Set up resources</span></span>](../psa/set-up-resources.md)
