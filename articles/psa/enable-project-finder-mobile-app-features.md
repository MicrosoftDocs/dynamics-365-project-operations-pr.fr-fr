---
title: Activer des fonctionnalités de l’application Project Finder Mobile
description: Procédure d’activation des fonctionnalités de l’application Project Finder Mobile pour Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007723"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Activer des fonctionnalités de l’application Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vos ressources peuvent utiliser l’application Project Finder Mobile sur leur téléphone avec le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour rechercher de nouveaux projets sur lesquels travailler et pour mettre à jour leurs compétences.  
  
 L’application est disponibles pour les téléphones [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] et [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Pour permettre aux utilisateurs de consulter les exigences ressources et mettre à jour leurs compétences, des options doivent être sélectionnées dans les paramètres définissant votre unité d’organisation.
  
> [!NOTE]
>  L’application mobile Project Finder Mobile fonctionne uniquement avec [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], pas sur les installations sur site.  
  
1. Accédez à **Project Service > Paramètres**.  
  
2. Cliquez sur la configuration des paramètres que vous souhaitez utiliser pour autoriser les fonctionnalités de l’application Project Finder Mobile.  
  
3. Dans la zone **Général**, définissez **Besoins en ressources visibles pour les ressources** sur **Oui**.  
  
4. Définissez **Autoriser la mise à jour des qualifications par ressource** sur **Oui**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Il s’agit d’un paramètre global. Les responsables de projet peuvent définir les projets qui apparaissent sur la page **Équipe projet** de ce projet.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notifications par courrier électronique  
 Le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envoie les messages électroniques concernant les demandes de ressources aux destinataires suivants aux heures suivantes :  
  
|Destinataire|Événement|  
|---------------|-----------|  
|Chef de projet|- Une ressource s’abonne à un projet avec l’application Project Finder Mobile.|  
|Ressource|- La tâche de projet à laquelle la ressource s’est abonnée a déjà été réalisée par une autre ressource.<br />- La demande d’approbation d’inclusion a été approuvée ou rejetée.<br />- La demande d’inscription d’inclusion a été approuvée ou rejetée.|  
  
## <a name="privacy-notice"></a>Avis de confidentialité  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Voir aussi  
 [Configurer les ressources](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]