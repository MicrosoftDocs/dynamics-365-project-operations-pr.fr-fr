---
title: Configurer des paramètres supplémentaires
description: Procédure de configuration de paramètres supplémentaires dans Project Service
author: JohnPBurrows
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
ms.openlocfilehash: fb23569db5136cd1b8b7d2f5735de8a91b441b76ab7e027d27087b3785f4636e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000438"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Configurer des paramètres supplémentaires (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Une fois que vous avez configuré les éléments des rubriques précédentes, vous devez définir des paramètres de projet supplémentaires à utiliser pour vos projets. Quand vous avez installé le [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pour la première fois, vous avez créé les paramètres pour créer d’abord tous les enregistrements requis pour que [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fonctionne. Maintenant il est temps de revenir en arrière et de configurer des champs supplémentaires pour ces paramètres.  
  
 Vous devez avoir configuré les paramètres suivants :  
  
-   Unité d’organisation  
  
-   Fréquence de facture  
  
-   Modèle d’heures de travail  
  
-   Tarifs  
 
Dans cette étape, vous allez indiquer le type d’allocation de ressources que vous souhaitez :  
  
- **Central**. Seuls les gestionnaires de ressources peuvent allouer des ressources à des projets.  
  
- **Hybride**. Les gestionnaires de ressources, les responsables de projet et les responsables de compte peuvent allouer des ressources à des projets.  
  
 
Pour définir les paramètres de projet :  
  
1. Accédez à **Project Service > Paramètres**.  
  
2. Cliquez sur le paramètre que vous souhaitez configurer (celui créé lors de la première installation du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ou cliquez sur **Nouveau** pour en créer un nouveau.  
  
3. Dans la zone **Général**, définissez toutes les options de vos paramètres du projet.  
  
4. Dans la zone **Tarifs**, cliquez sur **+** pour ajouter des tarifs, sélectionnez des tarifs dans la liste déroulante **Tarifs du paramètre du projet**, puis cliquez sur **Enregistrer**.  
  
5. Cliquez sur le bouton **Enregistrer** dans le coin inférieur droit de l’écran.  

> [!NOTE]
> L’enregistrement des paramètres du projet doit être conservé pour que Project Service fonctionne correctement. Cet enregistrement ne doit pas être supprimé.

### <a name="see-also"></a>Voir aussi  
 [Configurer les ressources](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]