---
title: Suivre le statut d'un projet
description: Procédure de suivi du statut d'un projet dans Project Service
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075826"
---
# <a name="track-a-projects-status-project-service"></a>Suivre le statut d'un projet (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilisez le [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] pour suivre la progression du projet d'un client.  

À mesure que l'engagement progresse, les phases du projet sont mises à jour pour refléter la phase de l'engagement :  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nouveau**    | Lorsque vous créez un projet, la phase est définie sur **Nouveau**. Si vous créez le projet à partir d'un modèle, à cette phase le projet peut avoir un calendrier, des estimations et les données d'équipe. Sinon, celui-ci sera le plan du projet et vous devez entrer manuellement le reste des composants du projet. |
|  **devis**   |      Lorsque vous associez un projet à un devis ou le créez depuis un devis, la phase de projet est définie sur **Devis** , et les dates de début et de fin estimée sont également mises à jour. Lorsque le projet est dans la phase de devis, les informations sur le devis s'affichent sous l'onglet **Sales** dans la page **Projet**.      |
|   **Planifier**   |                                     Lorsque vous ayez conclu un devis associé à un projet, et lorsque l'engagement progresse vers la phase de contrat, la phase de projet est mise à jour sur **Planifier**. Les détails de contrat s'affichent sous l'onglet **Sales** dans la page **Projet**.                                      |
| **Fin** |                    Lorsque la tâche de projet est terminée, vous pouvez revenir vers la phase **Terminé**. Lorsque la phase de projet est définie sur terminée, la tâche est terminée à 100 % mais le projet est maintenu ouvert en attendant l'enregistrement du temps ou des dépenses.                     |
|  **Fermer**   |           Lorsque toutes les transactions ont été enregistrées sur le projet et que vous ne prévoyez plus de saisir de données, vous pouvez manuellement définir la phase sur **Fermer**. Lorsque le contrat est défini sur **Fermer** , vous ne pouvez plus enregistrer de transactions sur le projet et le projet est en lecture seule.           |

## <a name="to-track-a-projects-status"></a>Pour suivre le statut d'un projet  

1.  Accédez à **Project Service > Projets**.  

2.  Cliquez sur le projet sur lequel vous souhaitez travailler.  

3.  Dans la barre dans toute la partie supérieure de l'écran, sélectionnez la flèche vers le bas en regard du nom de projet, puis cliquez sur **Suivi du projet**.  

4.  Sélectionnez **Suivi de l'effort** ou **Suivi du coût** dans la liste déroulante au-dessus de la liste des tâches.  

5.  Double-cliquez sur une tâche pour la modifier. Vous pouvez également déplacer ou redimensionner les barres dans le diagramme de Gantt pour modifier le temps et la progression d'une tâche.  

### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../psa/project-manager-guide.md)
