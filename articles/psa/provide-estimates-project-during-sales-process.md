---
title: Fournir des estimations de travail pour un projet pendant le processus de vente
description: Procédure de fourniture des estimations de travail pour un projet pendant le processus de vente dans Project Service
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: da638e5ab1f75033e5a42e51d5f35307f88c5174
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594483"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Fournir des estimations de travail pour un projet pendant le processus de vente (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durant le processus de vente, vous pouvez créer des estimations de vente à partir du début jusqu’aux lignes de devis. Les fonctionnalités du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dans [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] offrent un moyen plus scientifique et plus déterministe de proposer des estimations de vente en décomposant des éléments de travail et en associant les attributs adéquats qui peuvent contribuer aux estimations du projet dans la structure de répartition du travail.  
  
 Une fois que vous ayez conclu la vente, vous pouvez utiliser la structure de répartition du travail associée dans votre plan de projet, l’affinant selon les besoins pour achever votre projet avec succès.  
  
## <a name="link-a-project-to-a-quote-line"></a>Lier un projet à une ligne de devis  
 Lorsque vous créez une ligne de devis basée sur un projet, vous pouvez créer un nouveau projet depuis la ligne de devis. Vous pouvez ensuite utiliser les modèles de projet, qui sont des plans de projet standard préconfigurés et des estimations financières courantes à votre organisation, ou une copie d’un plan de projet et des estimations d’un projet précédent. Lorsque vous créez un projet, choisir un modèle de projet constitue une base pour affiner le plan de projet, les estimations, et les besoins relatifs aux rôles. En créant votre projet depuis le devis, le projet est automatiquement associé à la ligne de devis.  
  
## <a name="project-estimate-components"></a>Composants d’évaluation de projet  
 La structure de répartition du travail dans un projet permet de décomposer le travail en tâches, de conserver une hiérarchie des tâches, et d’attribuer une évaluation de l’effort nécessaire pour effectuer chaque tâche. Vous pouvez également associer des rôles à une tâche pour indiquer une évaluation du type de ressources requises pour effectuer une tâche et un programme.  
  
 La structure de répartition du travail vous permet de déterminer l’effort de travail et de planifier des estimations. Par défaut, le projet utilise les tarifs par défaut que vous avez définis auparavant. Les coûts et les prix de vente définis dans les tarifs aident à déterminer les estimations financières pour la répartition du travail du projet.  
  
 Si votre projet est associé à un devis, et le devis a des tarifs différent des valeurs par défaut, les tarifs du devis sont utilisés pour les estimations financières.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importer des estimations depuis un projet dans un devis  
 Une fois que vous avez des estimations de projet dans le projet, vous pouvez importer ces estimations dans la ligne de devis :  
  
-   Dans **Détails de la ligne de devis**, cliquez sur **Importer à partir des estimations**. 

-   Choisissez d’importer ou non des estimations de projet synthétisées par type de transaction, rôle, ou niveau de nœud de structure de répartition du travail.  
  
### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
