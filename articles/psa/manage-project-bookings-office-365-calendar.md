---
title: Gérer les projets et les réservations dans votre calendrier Office 365
description: Comment gérer les projets et les réservations dans votre calendrier Office 365
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: fd4119693875fb851c7bd3f34287db7d81237140
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075774"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Gérer les projets et les réservations dans votre calendrier (Project Service)

> [!Note]
> OBSOLÈTE : Cette fonctionnalité a été déconseillée et n'est plus disponible.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Afficher les rendez-vous personnels, les réservations de tâche de projet et les affectations d'ordre de travail du service après-vente à l'aide du calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Il est facile de gérer votre journée lorsque tout est centralisé. Vos réunions, rendez-vous, réservations et tâches sont tous disponibles dans votre calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Si vous utilisez [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], vous pouvez aussi entrer vos rendez-vous personnels dans la vue de saisie de l'heure de Project Service. Cela permet aux responsables de projets et de ressources de connaître votre disponibilité pour les projets. Cela vous permet également de gagner du temps, car il n'est pas nécessaire d'entrer deux fois les informations sur vos rendez-vous personnels. Vous pouvez simplement importer vos rendez-vous personnels de votre calendrier vers la vue de saisie de l'heure de Project Service.  
  
 Votre calendrier synchronise les réservations de projet et d'ordre de travail à partir du jour actuel jusqu'aux quatre prochaines semaines. Ce paramètre ne peut pas être modifié.  
  
 La synchronisation n'est prise en charge que dans un sens, de PSA vers votre calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Vous pouvez synchroniser dans l'ordre inverse. 
  
 Pour savoir comment utiliser votre calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], voir [Calendrier dans Outlook sur le Web pour les entreprises](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Configurer  
 Avant de pouvoir afficher et gérer vos réservations sur votre calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], vous devez configurer quelques éléments.  
  
- Vous devez disposer des informations d'identification de l'administrateur global ou de l'administrateur système [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- Votre administrateur doit configurer le profil du serveur de messagerie et chaque utilisateur doit configurer sa boîte aux lettres. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurer le traitement des messages électroniques via la synchronisation côté serveur](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Activer la synchronisation de votre organisation (tâche d'administrateur)  
  
1.  Dans le menu principal, cliquez sur **Paramètres** > **Administration**.  
  
2.  Cliquez sur **Paramètres système**.  
  
3.  Cliquez sur l'onglet **Synchronisation**.  
  
4.  Sous **Sélectionner s'il faut activer la synchronisation de réservations de ressource avec Outlook** , activez la case à cocher **Synchroniser les réservations de ressource avec Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Activer la synchronisation pour votre profil utilisateur (tâche d'utilisateur)  
  
1.  Cliquez sur le bouton **Paramètres** dans l'angle supérieur droit de l'écran.  
  
2.  Cliquez sur **Options**.  
  
3.  Cliquez sur l'onglet **Synchronisation**.  
  
4.  Sous **Synchronisation des réservations de ressource avec Outlook** , activez la case à cocher **Synchroniser les réservations de ressource avec Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importer vos rendez-vous personnels (tâche d'utilisateur)  
 Vous pouvez importer vos rendez-vous personnels de votre calendrier vers la vue de saisie de l'heure de Project Service Automation.  
  
1. Ouvrez le calendrier [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] et cliquez sur **Importer les données**.  
  
2. Dans l'écran Filtres, sélectionnez **Rendez-vous depuis Exchange** , puis cliquez sur **Appliquer**.  
  
3. Le système importe les rendez-vous dans la vue de saisie de l'heure en tant qu'entrées suggérées à partir de la semaine en cours. Pour ajouter des entrées pour une autre semaine, cliquez sur **Précédent** ou **Suivant**.  
  
4. Sélectionnez le rendez-vous que vous souhaitez ajouter à la vue de saisie de l'heure de Project Service Automation.  
  
5. Dans la zone contextuelle **Entrée de temps** , sélectionnez les options appropriées pour convertir le rendez-vous en une vue d'entrée de l'heure de Project Service Automation.  
  
6. Cliquez sur **Enregistrer**.  
  
### <a name="see-also"></a>Voir aussi  
 [Guide sur le temps, les dépenses et la collaboration](../psa/time-expense-collaboration-guide.md)
