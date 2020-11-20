---
title: Planifier des ressources pour un projet
description: Procédure de planification de ressources pour un projet dans Project Service
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132131"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planifier des ressources pour un projet (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vous pouvez afficher la disponibilité des ressources afin d’avoir une vue globale de la façon dont les ressources sont réservées, ou vous pouvez filtrer la vue par compétences, équipe, emplacement, et d’autres options.  
  
Le tableau de planification affiche la liste des ressources et leurs disponibilités. Sélectionnez un mode d’affichage pour afficher la disponibilité par **Heure**, **Jour**, **Semaine** ou **Mois**.  
  
Avant d’utiliser le tableau de planification, il est important de le configurer. Pour plus d’informations, consultez [Configurer le tableau de planification (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Si vous utilisez une nouvelle version, pour la disponibilité des ressources, consultez [Afficher la disponibilité des ressources](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Pour utiliser la fonctionnalité de réservation du tableau de planification, le géocodage et les services d’emplacement, vous devez activer des cartes.  
> 
> 1. Dans le menu principal, sélectionnez **Planification des ressources** > **Administration**.  
> 2. Cliquez sur **Paramètres de planification**.  
> 3. Ouvrez l’enregistrement et faites défiler la liste jusqu’à la section **Resource Scheduling Optimization**.  
> 4. Dans le champ **Se connecter aux cartes**, choisissez **Oui**.  
> 5. Acceptez les conditions et enregistrez l’enregistrement.  
> 6. Dans le menu principal, sélectionnez **Project Service** > **Tableau de planification**. À ce stade, il existe plusieurs méthodes permettant de planifier manuellement un besoin en réservation. Choisissez la méthode qui fonctionne pour vous.
  
## <a name="find-available-resources"></a>Trouver des ressources disponibles

1.  Dans la liste **Besoins en réservations**, cliquez avec le bouton droit sur une réservation non planifiée et choisissez l’une des options suivantes :  
  
- Choisissez **Recherche de disponibilité - Ressources actuelles** pour rechercher une ressource disponible dans la liste du tableau de planification.  
- Choisissez **Recherche de disponibilité - Toutes les ressources** pour rechercher une ressource disponible dans les ressources du système.  
   > [!NOTE]
   >  Une fois cette opération effectuée, les filtres affichent les options pour les besoins en réservation sélectionnés.  
  
2. Lorsqu’une plage horaire disponible s’affiche, cliquez avec le bouton droit sur la plage horaire dans le tableau de planification et choisissez **Réserver ici**. Ou, glissez-déplacez les besoins en réservation vers la plage horaire disponible.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Réserver une ressource à l’aide de la vue quotidienne et rechercher les ressources sous-réservées
  
1.  Dans le tableau de planification, sélectionnez **Mode d’affichage** et sélectionnez **Jours**.  
  
    Une vue de grille s’affiche avec le nombre d’heures pendant lesquelles une ressource est réservée par jour et les jours de disponibilité.  
  
2.  Cliquez sur le nom de la ressource que vous souhaitez réserver, puis sélectionnez **Réserver**.  
  
3.  Dans la boîte de dialogue **Réservation de ressource (créer)**, choisissez le projet pour lequel vous souhaitez réserver la ressource ainsi que la méthode de réservation et les dates de début et de fin.  
  
4.  Une fois que vous avez terminé, sélectionnez **Réserver**.  
  
## <a name="view-to-the-schedule-board"></a>Afficher le tableau de planification
  
1.  Sélectionnez un besoin en réservation non planifié dans la liste en bas.  
  
2.  Déplacez le besoin en réservation vers une ressource/plage horaire disponible dans le tableau de planification.  
  
3.  Une fois que vous avez terminé, sélectionnez **Réserver**.  
  
### <a name="additional-resources"></a>Ressources complémentaires  
 [Guide du gestionnaire de ressources](../psa/resource-manager-guide.md)
