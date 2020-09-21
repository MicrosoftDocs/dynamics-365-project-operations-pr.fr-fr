---
title: Utiliser le module complémentaire Project Service pour planifier votre travail dans Microsoft Project | MicrosoftDocs
description: Cette rubrique fournit des informations à suivre pour ajouter, configurer et utiliser le module complémentaire Microsoft Project pour Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168007"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Utiliser le module complémentaire Project Service Automation pour planifier votre travail dans Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vous facilite la planification de vos projets, y compris les estimations. Vous pouvez définir le travail afin que les coûts, l'effort, et la valeur de ventes soient clairs lorsque la proposition finale est envoyée.  

 Vous pouvez installer [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] et effectuer vos tâches de planification dans l'environnement familier de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilisez les robustes fonctionnalités de planification et de gestion de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et mettez à jour votre plan de projet dans Project Service Automation.  

> [!IMPORTANT]
> - Pour utiliser la fonctionnalité de gestion de documents SharePoint pour stocker vos fichiers [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pour des projets [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], votre administrateur [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] doit activer la fonctionnalité de gestion de documents. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Activation de la gestion de documents SharePoint pour des entités spécifiques](../admin/enable-sharepoint-document-management-specific-entities.md)  
> - Le [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] est uniquement compatible avec [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Télécharger et installer le module complémentaire  
 Munissez-vous de vos informations de connexion à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Vous devez disposer de ces informations pour vous connecter de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Dans le centre de téléchargement, téléchargez le complément pour votre version prise en charge de Project Service, soit [V2.X](https://go.microsoft.com/fwlink/?linkid=828268), soit [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Cliquez sur le lien de téléchargement.  

3.  Une fois le téléchargement terminé, cliquez sur **Oui** pour installer le module complémentaire.  

## <a name="configure-the-add-in"></a>Configurer le module complémentaire  

1. Ouvrez [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et cliquez sur l'onglet **Project Service**.  

2. Cliquez sur **Connexion**.  

3. Entrez vos informations de connexion puis cliquez sur **Se connecter**.  

   Vous pouvez à présent commencer à utiliser le module complémentaire.  

## <a name="read-from-a-template"></a>Lire à partir d'un modèle  
 Lisez depuis un modèle que vous avez créé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] et copié dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pour commencer la planification de votre projet. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Créer un modèle de projet (Project Service Automation)](../project-service/create-project-template.md)  

1.  Sous l'onglet **Project Service**, cliquez sur **Lire** > **Modèle de projet Project Service Automation**.  

2.  Choisissez un modèle de projet dans la liste puis cliquez sur **Ouvrir**.  

    > [!NOTE]
    >  Par défaut, les tâches qui sont copiées depuis le modèle dans le projet sont définies comme manuellement planifiées.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Attribuer des rôles [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] aux ressources de projet  

1.  Ouvrez un projet et cliquez sur le ruban **Tâche**.  

2.  Cliquez sur le menu **Diagramme de Gantt** puis choisissez **Feuille de ressource**.  

3.  Dans la feuille de la ressource, cliquez sur le menu déroulant **Rôle de ressource Project Service** et choisissez un rôle Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Doter votre projet en ressources  

1.  Sous l'onglet Project Service, sélectionnez une ligne et cliquez sur **Rechercher des ressources**.  

2.  Sur l'écran **Réserver la ressource**, sélectionnez la ressource que vous souhaitez utiliser pour le projet.  

3.  Cliquez sur **Réserver**, puis sur **OK**.  

## <a name="publish-your-project"></a>Publier votre projet  
Lorsque votre planification de projet terminée, l'étape suivante consiste à importer et à publier le projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Le projet est importé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Le processus de génération de tarification et d'équipe est appliqué. Ouvrez le projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour vérifier que l'équipe, les estimations de projet, et la structure de répartition du travail ont été générées. Le tableau suivant indique où trouver les résultats :


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramme de Gantt**   | Importations dans l'écran **Structure de répartition du travail** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Feuille de ressource** |   Importations dans l'écran **Project Team Members** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] - **Utilisation**    |    Importations dans l'écran **Estimations de projets** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] .     |

**Pour importer et publier votre projet**  
1. Sous l'onglet **Project Service**, cliquez sur **Publier** > **Nouveau projet Project Service Automation**.  

2. Dans la boîte de dialogue **Publier dans un nouveau projet Project Service**, entrez le **Nom du projet** et sélectionnez **Client**.  

3. Cochez éventuellement **Lier le plan de projet à Project Service Automation** pour lier le fichier du projet de plan à Project Service Automation.  

4. Cliquez sur **Publier**.  

   L'association du fichier de projet à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fait du fichier de projet le maître et définit la structure de répartition du travail sur [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en lecture seule.  Afin d'apporter des modifications au plan de projet, vous devez les faire dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et les publier sous forme de mises à jour dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Modifier un projet qui a été importé  
 Pour apporter des modifications à un projet qui a été importé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], vous avez deux options :  

- Ouvrez le fichier maître et modifiez-le dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Supprimez le lien du fichier et modifiez-le directement dans Project Service. Par défaut, un projet qui a été téléchargé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] est verrouillé et peut être modifié uniquement dans Project. Pour modifier le fichier dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], le fichier doit être dissocié.  

### <a name="edit-in-pn_microsoft_project"></a>Procéder à la modification dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Dans le menu principal, cliquez sur **Project Service** > **Projets**.  

2. Dans la liste des projet, ouvrez celui que vous avez créé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Cliquez sur **Ouvrir dans MS Project** sur le ruban. Cela ouvrira le fichier maître associé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Supprimer le lien au fichier et le modifier dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Dans le menu principal, cliquez sur **Project Service** > **Projets**.  

2. Dans la liste des projet, ouvrez celui que vous avez créé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Cliquez sur **Supprimer le lien de MS Project** sur le ruban.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Télécharger un fichier Project dans des groupes SharePoint ou Office  
 Vous pouvez télécharger votre fichier Project dans SharePoint et le trouver sous Documents associés dans votre projet [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Votre administrateur doit configurer la fonctionnalité de gestion de documents SharePoint et l'activer pour l'entité Project. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configuration de l'intégration SharePoint](../admin/set-up-sharepoint-integration.md)  

 Vous pouvez également télécharger votre fichier Project dans [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si vous avez paramétré des groupes Office. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Collaborer avec vos collègues à l'aide de Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)  

### <a name="upload-a-file-for-sharepoint"></a>Charger un fichier pour SharePoint  

1. Dans le menu principal, cliquez sur **Project Service** > **Télécharger**.  

2. Sélectionnez **Vers les documets du projet Project Service Automation**.  

3. Dans la boîte de dialogue **Activer l'ouverture dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, sélectionnez **Oui** ou **Non**.  

   - Si vous cliquez sur **Oui**, vous pourrez cliquer sur le bouton **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dans Project Service Automation, lancer [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et charger le fichier Project depuis la bibliothèque de documents SharePoint.  

   - Si vous cliquez sur **Non**, le lien vers le bouton **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne fonctionnera pas.  

4. Le fichier [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se trouve dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sous **Documents** pour le projet spécifique [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Télécharger un fichier pour les groupes Office  

1. Dans le menu principal, cliquez sur **Project Service** > **Télécharger**.  

2. Sélectionnez **Vers les documets du projet Project Service Automation**.  

3. Dans la boîte de dialogue **Activer l'ouverture dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, sélectionnez **Oui** ou **Non**.  

   - Si vous cliquez sur **Oui**, vous pourrez cliquer sur le bouton **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dans Project Service Automation, lancer [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et charger le fichier Project depuis la bibliothèque de documents SharePoint.  

   - Si vous cliquez sur **Non**, le lien vers le bouton **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne fonctionnera pas.  

4. Le fichier [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se trouve dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sous **Documents** pour le projet spécifique [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publier votre projet comme modèle  
 Vous pouvez enregistrer votre projet et le réutiliser en l'enregistrant comme modèle de projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Les modèles de projet sont des plans de projet réutilisables dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Créer un modèle de projet (Project Service Automation)](../project-service/create-project-template.md)  

1. Sous l'onglet **Project Service**, cliquez sur **Publier** > **Nouveau modèle de projet Project Service Automation**.  

2. Dans la boîte de dialogue **Publier dans un nouveau modèle de projet Project Service**, entrez le **Nom de modèle du projet**.  

3. Cochez éventuellement **Lier le plan de projet à Project Service Automation** pour lier le fichier Project à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Cliquez sur **Publier**.  

L'association du fichier de projet à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fait du fichier Project le maître et définit la structure de répartition du travail dans le modèle [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sur lecture seule.  Afin d'apporter des modifications au plan de projet, vous devez les faire dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et les publier sous forme de mises à jour dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../project-service/project-manager-guide.md)
