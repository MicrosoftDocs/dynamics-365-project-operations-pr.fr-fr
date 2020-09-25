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
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167966"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Activer des fonctionnalités de l'application Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vos ressources peuvent utiliser l'application Project Finder Mobile sur leur téléphone avec le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour rechercher de nouveaux projets sur lesquels travailler et pour mettre à jour leurs compétences.  
  
 L'application est disponibles pour les téléphones [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] et [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Vous devez définir des options dans les paramètres définissant de votre unité d'organisation pour permettre aux utilisateurs de consulter les exigences ressources et mettre à jour leurs compétences.  
  
> [!NOTE]
>  L'application mobile Project Finder Mobile fonctionne uniquement avec [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], pas sur les installations sur site.  
  
1. Accédez à **Project Service > Paramètres**.  
  
2. Cliquez sur la configuration des paramètres que vous souhaitez utiliser pour autoriser les fonctionnalités de l'application Project Finder Mobile.  
  
3. Dans la zone **Général**, définissez **Besoins en ressources visibles pour les ressources** sur **Oui**.  
  
4. Définissez **Autoriser la mise à jour des qualifications par ressource** sur **Oui**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Il s'agit d'un paramètre global. Les responsables de projet peuvent définir les projets qui apparaissent sur la page **Équipe projet** de ce projet.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notifications par courrier électronique  
 Le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envoie les messages électroniques concernant les demandes de ressources aux destinataires suivants aux heures suivantes :  
  
|Destinataire|Événement|  
|---------------|-----------|  
|Gestionnaire de projet|-   Lorsqu'une ressource s'abonne à un projet avec l'application Project Finder Mobile.|  
|Ressource|-   Lorsque la tâche de projet à laquelle la ressource s'est abonnée a déjà été réalisée par une autre ressource.<br />-   Lorsque leur demande d'approbation de qualification a été approuvée ou rejetée.<br />-   Lorsque leur demande d'inscription au projet a été approuvée ou rejetée.|  
  
## <a name="privacy-notice"></a>Avis de confidentialité  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Voir aussi  
 [Configurer les ressources](../project-service/set-up-resources.md)