---
title: 'Considérations relatives à la mise à niveau : Microsoft Dynamics 365 Project Service Automation version 2.x ou 1.x vers la version 3'
description: Cette rubrique donne des informations sur les considérations que vous devez prendre en compte lors de la mise à niveau de Project Service Automation version 2.x ou 1.x vers la version 3.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ff0777705c6d0e2c0d8aa4ed191f4ae6b1786100
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281655"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Considérations relatives à la mise à niveau - PSA version 2.x ou 1.x vers la version 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation et Field Service
Dynamics 365 Project Service Automation et Dynamics 365 Field Service utilisent la solution Universal Resourcing Scheduling (URS) pour la planification des ressources. Si vous disposez de Project Service Automation et Field Service dans votre instance, mettez-les à niveau vers la version la plus récente. Pour Project Service Automation c'est la version 3.x. Pour Field Service, il s'agit de la version 8.x. La mise à niveau de Project Service Automation ou Field Service installera la dernière version d'URS. Si les solutions Project Service Automation et Field Service de la même instance ne sont pas mises à niveau vers la dernière version, il peut y avoir un comportement incohérent.

## <a name="resource-assignments"></a>Attributions de ressources
Dans Project Service Automation version 2 et version 1, les affectations de tâches étaient stockées en tant que tâches enfants (également appelées tâches de ligne) dans l’entité **Tâche**, et indirectement associées à l’entité **Affectation de ressource**. La tâche de ligne était visible dans la fenêtre contextuelle d’affectation de la structure de répartition du travail (WBS).

![Tâches de ligne de WBS dans Project Service Automation version 2 et version 1](media/upgrade-line-task-01.png)

Dans la version 3 de Project Service Automation, le schéma sous-jacent d’affectation de ressources réservables aux tâches a été modifié. La tâche de ligne a été déconseillée et il existe une relation directe de type 1:1 entre la tâche dans l’entité **Tâche** et le membre de l’équipe dans l’entité **Affectation de ressource**. Les tâches qui sont affectées à un membre de l’équipe du projet sont maintenant stockées directement dans l’entité Affectation de ressource.  

Ces modifications ont une incidence sur la mise à niveau des projets existants qui ont des affectations de ressources pour les ressources réservables nommées et les ressources génériques d’une équipe du projet. Cette rubrique décrit les considérations vous devrez prendre en compte pour vos projets lors de la mise à niveau vers la version 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tâches affectées aux ressources nommées
À l’aide de l’entité Tâche sous-jacente, les tâches dans la version 2 et la version 1 autorisaient les membres de l’équipe à utiliser un rôle autre que leur rôle défini par défaut. Par exemple, Charline Gauthier, à qui est affectée par défaut le rôle de Gestionnaire de programmes, pouvait être affectée à une tâche avec le rôle de Développeur. Dans la version 3, le rôle d’un membre de l’équipe nommé est toujours la valeur par défaut. Ainsi, toute tâche affectée à Charline Gauthier utilise son rôle par défaut de Gestionnaire de programmes.

Si vous avez affecté une ressource à une tâche en dehors de son rôle par défaut dans la version 2 et la version 1, lorsque vous effectuez une mise à niveau, le rôle par défaut est affecté à la ressource nommée pour toutes les affectations de tâches, quelle que soit l’affectation de rôle dans la version 2. Cette affectation entraînera des différences dans les estimations calculées de la version 2 ou version 1 vers la version 3, car les estimations sont calculées en fonction du rôle de la ressource au lieu de l’affectation de tâches de ligne. Par exemple, dans la version 2, deux tâches ont été affectées à Astrid Lang. Le rôle sur la tâche de ligne pour la tâche 1 est Développeur et pour la tâche 2, Gestionnaire de programmes. Astrid Lang a le rôle par défaut de Gestionnaire de programmes.

![Rôles multiples affectés à une ressource](media/upgrade-multiple-roles-02.png)

Étant donné que les rôles de Développeur et de Gestionnaire de programmes diffèrent, les estimations de coût et de vente se présentent comme suit :

![Estimations de coût pour les rôles de ressource](media/upggrade-cost-estimates-03.png)

![Estimations de vente pour les rôles de ressource](media/upgrade-sales-estimates-04.png)

Lorsque vous effectuez une mise à niveau vers la version 3, les tâches de ligne sont remplacées par des affectations de ressources sur la tâche du membre de l’équipe pour la ressource réservable. L’affectation utilise le rôle par défaut de la ressource réservable. Dans le graphique suivant, Astrid Lang qui a le rôle de Gestionnaire de programmes, est la ressource.

![Affectations de ressources](media/resource-assignment-v2-05.png)

Comme les estimations sont basées sur le rôle par défaut de la ressource, les estimations de vente et de coût peuvent changer. Dans le graphique suivant, le rôle **Développeur** ne s’affiche plus, car il est maintenant extrait du rôle par défaut de la ressource réservable.

![Estimations de coût pour les rôles par défaut](media/resource-assignment-cost-estimate-06.png)
![Estimations de vente pour les rôles par défaut](media/resource-assignment-sales-estimate-07.png)

Une fois la mise à niveau terminée, vous pouvez modifier le rôle d’un membre de l’équipe en un rôle autre que celui affecté par défaut. Toutefois, si vous modifiez le rôle d’un membre de l’équipe, cette modification est appliquée à toutes les tâches qui lui sont affectées, car les membres de l’équipe ne peuvent plus avoir plusieurs rôles dans la version 3.

![Mise à jour du rôle d’une ressource](media/resource-role-assignment-08.png)

Cette procédure s’applique également aux tâches de ligne qui ont été affectées aux ressources nommées lorsque vous modifiez l’unité d’organisation par défaut de la ressource en une autre unité d’organisation. Une fois la mise à niveau vers la version 3 terminée, l’affectation utilise l’unité d’organisation par défaut de la ressource au lieu de celle définie sur la tâche de ligne.

### <a name="tasks-assigned-to-generic-resources"></a>Tâches affectées aux ressources génériques
Dans la version 2 et la version 1, vous pouvez définir le rôle et l’unité d’organisation d’une tâche puis utiliser la fonctionnalité **Générer l’équipe** pour générer les ressources génériques en fonction des attributs définis sur la tâche. Dans la version 3, vous créez les membres de l’équipe générique avec un rôle et une unité d’organisation, puis affectez les membres de l’équipe à des tâches.

Dans la version 2 et la version 1, les projets avec des ressources génériques peuvent avoir deux états, ou une combinaison des deux au niveau de la tâche. Par exemple, les scénarios suivants sont possibles :

- Des tâches avec des rôles et des unités d’organisation définis, mais aucune affectation de ressource affiliée n’a été générée.
- Des tâches avec des affectations de ressources aux membres de l’équipe qui ont été générées en créant une ressource générique à l’aide de la fonctionnalité **Générer l’équipe**.

Avant de commencer la mise à niveau, il est recommandé de régénérer l’équipe pour chaque projet contenant des tâches affectées aux ressources génériques ou d’exécuter le processus Générer l’équipe sur celles-ci.

Pour les tâches affectées aux membres de l’équipe générique qui ont été générées avec l’option **Générer l’équipe**, la mise à niveau conserve la ressource générique de l’équipe ainsi que l’affectation à ce membre de l’équipe générique. Il est recommandé de générer les ressources requises pour le membre de l’équipe générique après la mise à niveau mais avant de réserver ou d’envoyer une demande de ressources. Cela préserve les affectations d’unité d’organisation des membres de l’équipe générique qui sont différentes de l’unité d’organisation contractuelle du projet.

Par exemple, dans le projet Project Z, l’unité d’organisation contractuelle est Contoso US. Dans le plan du projet, les tâches de test dans la phase de mise en œuvre ont été affectées au rôle Consultant technique et l’unité d’organisation affectée est Contoso Inde.

![Affectation d’organisation dans la phase de mise en œuvre](media/org-unit-assignment-09.png)

Après la phase de mise en œuvre, la tâche de test de l’intégration est affectée au rôle Consultant technique, mais l’organisation est définie sur Contoso US.  

![Affectation d’organisation pour la tâche de test de l’intégration](media/org-unit-generate-team-10.png)

Lorsque vous générez une équipe pour le projet, deux membres de l’équipe générique sont créés en raison des différentes unités d’organisation des tâches. Les tâches de Contoso Inde sont affectées au consultant technique 1 et les tâches de Contoso US au consultant technique 2.  

![Membres de l’équipe générique générés](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Dans Project Service Automation version 2 et version 1, le membre de l’équipe ne détient pas l’unité d’organisation, qui est conservée sur la tâche de ligne.

![Tâches de ligne dans la version 2 et la version 1 de Project Service Automation](media/line-tasks-12.png)

L’unité d’organisation est visible sur la vue des estimations. 

![Estimations de l’unité d’organisation](media/org-unit-estimates-view-13.png)
 
Lorsque la mise à niveau est terminée, l’unité d’organisation sur la tâche de ligne correspondant au membre de l’équipe générique est ajoutée au membre de l’équipe générique et la tâche de ligne est supprimée. C’est pourquoi il est recommandé, avant la mise à niveau, de générer ou de régénérer l’équipe sur chaque projet contenant des ressources génériques.

Pour les tâches qui sont affectées à un rôle avec une unité d’organisation différente de celle du projet contractuel, et une équipe n’a pas été générée, la mise à niveau crée un membre de l’équipe générique pour le rôle, mais utilise l’unité contractuelle du projet pour l’unité d’organisation du membre de l’équipe. Si l’on reprend l’exemple avec le projet Project Z, l’unité d’organisation contractuelle Contoso US et les tâches de test du plan du projet dans la phase de mise en œuvre ont été affectées au rôle Consultant technique avec l’unité d’organisation affectée à Contoso Inde. La tâche de test de l’intégration qui est effectuée après la phase de mise en œuvre a été affectée au rôle Consultant technique. L’unité d’organisation est Contoso US et une équipe n’a pas été générée. La mise à niveau crée un membre de l’équipe générique, un consultant technique avec les heures affectées des trois tâches et une unité d’organisation Contoso US, qui est l’unité d’organisation contractuelle du projet.   
 
La modification de la valeur par défaut des différentes unités d’organisation des membres de l’équipe non générés est la raison pour laquelle il est recommandé de générer ou de régénérer l’équipe sur chaque projet contenant des ressources génériques avant la mise à niveau afin que les affectations d’unité d’organisation ne soient pas perdues.



[!INCLUDE[footer-include](../includes/footer-banner.md)]