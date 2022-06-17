---
title: Planifiez votre travail dans Microsoft Project avec le module complémentaire Project Service
description: Cet article fournit des informations à suivre pour utiliser le module complémentaire Microsoft Project pour Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 779d83a896dd7d92c6584e6f1c57b1ea567e9051
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910995"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planifiez votre travail dans Microsoft Project avec le module complémentaire Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vous facilite la planification de vos projets, y compris les estimations. Vous pouvez définir le travail afin que les coûts, l’effort, et la valeur de ventes soient clairs lorsque la proposition finale est envoyée.  

Vous pouvez installer [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] et effectuer vos tâches de planification dans l’environnement familier de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilisez les robustes fonctionnalités de planification et de gestion de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et mettez à jour votre plan de projet dans Project Service Automation.  

> [!IMPORTANT]
> - Pour utiliser la fonctionnalité de gestion de documents SharePoint pour stocker vos fichiers [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pour des projets [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], votre administrateur [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] doit activer la fonctionnalité de gestion de documents. 
> - Le [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] est uniquement compatible avec [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Télécharger et installer le module complémentaire  
 Munissez-vous de vos informations de connexion à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Vous devez disposer de ces informations pour vous connecter de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Dans le centre de téléchargement, téléchargez le complément pour votre version prise en charge de Project Service, soit [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x), soit [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Cliquez sur le lien de téléchargement.  

3.  Une fois le téléchargement terminé, cliquez sur **Oui** pour installer le module complémentaire.  

## <a name="configure-the-add-in"></a>Configurer le module complémentaire  

1. Ouvrez [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et cliquez sur l’onglet **Project Service**.  

2. Cliquez sur **Se connecter**.  

3. Entrez vos informations de connexion, puis cliquez sur **Se connecter**.  

   Vous pouvez à présent commencer à utiliser le module complémentaire.  

## <a name="read-from-a-template"></a>Lire à partir d’un modèle  
 Lisez depuis un modèle que vous avez créé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] et copié dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pour commencer la planification de votre projet. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Créer un modèle de projet (Project Service Automation)](../psa/create-project-template.md)  

1.  Sous l’onglet **Project Service**, cliquez sur **Lire** > **Modèle de projet Project Service Automation**.  

2.  Choisissez un modèle de projet dans la liste, puis cliquez sur **Ouvrir**.  

    > [!NOTE]
    >  Par défaut, les tâches qui sont copiées depuis le modèle dans le projet sont définies comme manuellement planifiées.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Attribuer des rôles [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] aux ressources de projet  

1.  Ouvrez un projet et cliquez sur le ruban **Tâche**.  

2. Cliquez sur le menu **Diagramme de Gantt**, puis choisissez **Feuille de ressource**.  

3. Dans la feuille de la ressource, cliquez sur le menu déroulant **Rôle de ressource Project Service** et choisissez un rôle Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Doter votre projet en ressources  

1.  Sous l’onglet Project Service, sélectionnez une ligne et cliquez sur **Rechercher des ressources**.  

2.  Sur l’écran **Réserver la ressource**, sélectionnez la ressource que vous souhaitez utiliser pour le projet.  

3.  Sélectionnez **Réserver**, puis **OK**.  

## <a name="publish-your-project"></a>Publier votre projet  
Lorsque votre planification de projet terminée, l’étape suivante consiste à importer et à publier le projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Le projet est importé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Le processus de génération de tarification et d’équipe est appliqué. Ouvrez le projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour vérifier que l’équipe, les estimations de projet, et la structure de répartition du travail ont été générées. Le tableau suivant indique où trouver les résultats.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramme de Gantt**   | Importations dans l’écran **Structure de répartition du travail** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Feuille de ressource** |   Importations dans l’écran **Project Team Members** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] - **Utilisation**    |    Importe dans l’écran **Estimations de projets** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Pour importer et publier votre projet**  
1. Sous l’onglet **Project Service**, accédez à **Publier** > **Nouveau projet Project Service Automation**.  

2. Dans la boîte de dialogue **Publier dans un nouveau projet Project Service**, entrez le **Nom du projet** et sélectionnez **Client**.  

3. Cliquez sur **Lier le plan de projet à Project Service Automation** pour lier le fichier du projet de plan à Project Service Automation.  

4. Cliquez sur **Publier**.  

   L’association du fichier de projet à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fait du fichier de projet le maître et définit la structure de répartition du travail sur [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en lecture seule.  Afin d’apporter des modifications au plan de projet, vous devez les faire dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et les publier sous forme de mises à jour dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Modifier un projet qui a été importé  
 Pour apporter des modifications à un projet qui a été importé dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], vous avez deux options :  

- Ouvrez le fichier maître et modifiez-le dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Supprimez le lien du fichier et modifiez-le directement dans Project Service. Par défaut, un projet qui a été téléchargé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] est verrouillé et peut être modifié uniquement dans Project. Pour modifier le fichier dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], le fichier doit être dissocié.  

### <a name="edit-in-pn_microsoft_project"></a>Modifier dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Dans le menu principal, accédez à **Project Service** > **Projets**.  

2. Dans la liste des projet, ouvrez celui que vous avez créé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Cliquez sur **Ouvrir dans MS Project** sur le ruban. Cela ouvrira le fichier maître associé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Supprimer le lien au fichier et le modifier dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Dans le menu principal, accédez à **Project Service** > **Projets**.  

2. Dans la liste des projet, ouvrez celui que vous avez créé dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Cliquez sur **Supprimer le lien de MS Project** sur le ruban.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Télécharger un fichier Project dans des groupes SharePoint ou Office  
 Vous pouvez télécharger votre fichier Project dans SharePoint et le trouver sous Documents associés dans votre projet [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Votre administrateur doit configurer la fonctionnalité de gestion de documents SharePoint et l’activer pour l’entité Project. 

 Vous pouvez également télécharger votre fichier Project dans [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si vous avez paramétré des groupes Office.

### <a name="upload-a-file-for-sharepoint"></a>Charger un fichier pour SharePoint  

1. Dans le menu principal, accédez à **Project Service** > **Charger**.  

2. Sélectionnez **Vers les documets du projet Project Service Automation**.  

3. Dans la boîte de dialogue **Activer l’ouverture de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sélectionnez **Oui** ou **Non**.  

   - Si vous cliquez sur **Oui**, vous pourrez sélectionner **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dans Project Service Automation et lancer [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et charger le fichier Project depuis la bibliothèque de documents SharePoint.  

   - Si vous sélectionnez **Non**, le lien pour **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne fonctionnera pas.  

4. Le fichier [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se trouve dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sous **Documents** pour le projet spécifique [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Télécharger un fichier pour les groupes Office  

1. Dans le menu principal, accédez à **Project Service** > **Charger**.  

2. Sélectionnez **Vers les documets du projet Project Service Automation**.  

3. Dans la boîte de dialogue **Activer l’ouverture de [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sélectionnez **Oui** ou **Non**.  

   - Si vous cliquez sur **Oui**, vous pourrez sélectionner **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dans Project Service Automation et lancer [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et charger le fichier Project depuis la bibliothèque de documents SharePoint.  

   - Si vous sélectionnez **Non**, le lien pour **Ouvrir dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne fonctionnera pas.  

4. Le fichier [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se trouve dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sous **Documents** pour le projet spécifique [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publier votre projet comme modèle  
 Vous pouvez enregistrer votre projet et le réutiliser en l’enregistrant comme modèle de projet dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Les modèles de projet sont des plans de projet réutilisables dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Pour plus d’informations, voir [Créer un modèle de projet (Project Service Automation)](../psa/create-project-template.md). 

1. Sous l’onglet **Project Service**, accédez à **Publier** > **Nouveau modèle de projet Project Service Automation**.  

2. Dans la boîte de dialogue **Publier dans un nouveau modèle de projet Project Service**, entrez le **Nom de modèle du projet**.  

3. Cochez éventuellement **Lier le plan de projet à Project Service Automation** pour lier le fichier du projet à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Cliquez sur **Publier**.  

L’association du fichier de projet à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fait du fichier Project le maître et définit la structure de répartition du travail dans le modèle [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sur lecture seule.  Afin d’apporter des modifications au plan de projet, vous devez les faire dans [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] et les publier sous forme de mises à jour dans [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Lire une planification chargée avec des ressources

Lors de la lecture d’un projet à partir de Project Service Automation, le calendrier de la ressource n’est pas synchronisé avec le client de bureau. S’il existe des différences dans la durée, l’effort ou la fin des tâches, c’est probablement parce que les ressources et le client de bureau n’ont pas le même calendrier de modèle d’heures de travail appliqué au projet.


## <a name="data-synchronization"></a>Synchronisation des données
Les tableaux de cette section fournissent des informations sur la synchronisation des données d’entité entre Project Service Automation et le complément de bureau Microsoft Project.

### <a name="project-task-entity-table"></a>Table d’entité de tâche de projet
Le tableau suivant décrit comment les données de l’entité Tâche de projet sont synchronisées entre Project Service Automation et le complément de bureau Microsoft Project.

| **Entité** | **Champ** | **Microsoft Project à Project Service Automation** | **Project Service Automation à Microsoft Project** |
| --- | --- | --- | --- |
| Tâche du projet | Date d’échéance | Synchronisé | Non synchronisé |
| Tâche du projet | Effort estimé | Synchronisé | Non synchronisé |
| Tâche du projet | ID du client MS Project | Synchronisé | Non synchronisé |
| Tâche du projet | Tâche parente | Synchronisé | Non synchronisé |
| Tâche du projet | Project | Synchronisé | Non synchronisé |
| Tâche du projet | Tâche du projet | Synchronisé | Non synchronisé |
| Tâche du projet | Nom de la tâche du projet | Synchronisé | Non synchronisé |
| Tâche du projet | Unité d’allocation des ressources (obsolète dans la version 3.0) | Synchronisé | Non synchronisé |
| Tâche du projet | Durée planifiée | Synchronisé | Non synchronisé |
| Tâche du projet | Date de début | Synchronisé | Non synchronisé |
| Tâche du projet | ID WBS | Synchronisé | Non synchronisé |

### <a name="team-member-entity-table"></a>Table d’entité Membre de l’équipe
Le tableau suivant décrit comment les données de l’entité Membre de l’équipe sont synchronisées entre Project Service Automation et le Micros

| **Entité** | **Champ** | **Microsoft Project à Project Service Automation** | **Project Service Automation à Microsoft Project** |
| --- | --- | --- | --- |
| Membre d’équipe | ID du client MS Project | Synchronisé | Non synchronisé |
| Membre d’équipe | Nom du poste | Synchronisé | Non synchronisé |
| Membre d’équipe | projet | Synchronisé | Synchronisé |
| Membre d’équipe | Équipe du projet | Synchronisé | Synchronisé |
| Membre d’équipe | Unité d’allocation des ressources | Non synchronisé | Synchronisé |
| Membre d’équipe | Rôle | Non synchronisé | Synchronisé |
| Membre d’équipe | Heures de travail | Non synchronisé | Non synchronisé |

### <a name="resource-assignment-entity-table"></a>Table d’entité Affectation de ressources
Le tableau suivant décrit comment les données de l’entité Affectation des ressources sont synchronisées entre Project Service Automation et le Micros

| **Entité** | **Champ** | **Microsoft Project à Project Service Automation** | **Project Service Automation à Microsoft Project** |
| --- | --- | --- | --- |
| Attribution de ressource | Date de début | Synchronisé | Non synchronisé |
| Attribution de ressource | heures | Synchronisé | Non synchronisé |
| Attribution de ressource | ID du client MS Project | Synchronisé | Non synchronisé |
| Attribution de ressource | Travail planifié | Synchronisé | Non synchronisé |
| Attribution de ressource | Project | Synchronisé | Non synchronisé |
| Attribution de ressource | Équipe du projet | Synchronisé | Non synchronisé |
| Attribution de ressource | Attribution de ressource | Synchronisé | Non synchronisé |
| Attribution de ressource | Tâche | Synchronisé | Non synchronisé |
| Attribution de ressource | Date de fin | Synchronisé | Non synchronisé |

### <a name="project-task-dependencies-entity-table"></a>Table d’entité Dépendances de tâche de projet
Le tableau suivant décrit comment les données de l’entité Dépendances de tâche de projet sont synchronisées entre Project Service Automation et le Micros

| **Entité** | **Champ** | **Microsoft Project à Project Service Automation** | **Project Service Automation à Microsoft Project** |
| --- | --- | --- | --- |
| Dépendances de la tâche du projet | Dépendance de la tâche du projet | Synchronisé | Non synchronisé |
| Dépendances de la tâche du projet | Type de lien | Synchronisé | Non synchronisé |
| Dépendances de la tâche du projet | Tâche précédente | Synchronisé | Non synchronisé |
| Dépendances de la tâche du projet | Project | Synchronisé | Non synchronisé |
| Dépendances de la tâche du projet | Tâche suivante | Synchronisé | Non synchronisé |

### <a name="additional-resources"></a>Ressources complémentaires
 [Guide du responsable de projet](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
