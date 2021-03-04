---
title: Créer un modèle de projet
description: Procédure de création d’un modèle de projet dans Project Service
author: ruhercul
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149360"
---
# <a name="create-a-project-template-project-service"></a>Créer un modèle de projet (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Les modèles de projet vous font gagner du temps si votre société fait régulièrement des offres sur des types de projet similaires. Ils fournissent un jeu standard de rôles et d’heures estimés pour un type du projet. Les responsables de compte et les responsables de projet peuvent créer des projets basés sur un modèle de projet, ou ils peuvent copier le modèle et réaliser leur propre projet.  
  
## <a name="components-of-project-template"></a>Composants du modèle de projet
 Un modèle de projet est composé de trois composants :  
  
- **Structure de répartition du travail** : une structure de répartition du travail dans un modèle de projet se compose du même ensemble d’éléments que le projet. Vous pouvez créer une hiérarchie de tâches, associer des rôles à la tâche, définir des attributs de planification, définir des dépendances et afficher toutes les données dans le diagramme de Gantt. La structure de répartition du travail dans les modèles de projet prend également en charge les modes de tâche de chaque tâche. Il n’y a aucune différence entre un modèle de projet et un projet lors de la création de la planification des tâches.  
  
- **Estimations du projet** : les estimations de projet dans les modèles fonctionnent de la même manière que dans les projets, excepté les tarifs permettant le calcul des tarifs de vente et de prix de revient par défaut qui sont toujours les tarifs de vente et de prix de revient par défaut définis dans les paramètres du [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Le reste des fonctionnalités est le même que dans un projet.  
  
- **Formation de l’équipe du projet** : lors de la formation d’une équipe de projet pour un modèle de projet, vous ne pouvez pas inscrire une ressource nommée dans un modèle. Vous pouvez **Générez l’équipe du projet** dans la structure de répartition du travail pour générer un ensemble de ressources génériques. Vous pouvez également spécifier les aptitudes et les compétences requises pour les ressources génériques. Vous ne pouvez pas substituer une ressource générique avec une ressource pouvant être réservée dans les modèles de projet.  
  
## <a name="create-a-project-from-a-template"></a>Créer un projet à partir d’un modèle  
 Vous pouvez créer un projet à partir d’un modèle de ces méthodes suivantes :  
  
-   En créant un projet à partir d’un devis, vous pouvez choisir un modèle de projet dans le formulaire de création rapide de projet.  
  
-   Lors de la création d’un projet en cliquant sur **Nouveau projet**, le formulaire du projet s’affiche avant d’enregistrer l’enregistrement. De là, vous pouvez cliquer sur le champ **Choisir un modèle** pour choisir dans la liste de modèles de projet prédéfinis de votre organisation.  
  
-   Cliquez sur **Créer un projet à partir d’un modèle** sur la page **Modèle du projet** pour créer un projet à partir du modèle.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copie de composants d’un modèle dans un projet  
 Lorsque vous copiez les composants d’un modèle dans un projet, il y a quelques précautions à prendre.  
  
 **Copie d’une structure de distribution de travail** : lorsque vous copiez la structure de répartition du travail d’un modèle de projet, si le projet a un calendrier de projet différent du modèle, les heures de travail du calendrier du projet sont appliquées au programme des tâches. Cela ajuste la planification au calendrier du projet de sauvegarde. De même, la première tâche de la structure de répartition du travail prend la date de début du projet, par conséquent le reste de la planification de la hiérarchie des tâches est mis à jour selon la durée et les dépendances spécifiées dans la structure de répartition du travail du modèle.  
  
 **Copie des estimations du projet** : lorsque vous copiez dans les lignes d’évaluation de projet, les tarifs sont mis à jour selon l’unité propriétaire du projet pour les prix de revient et selon le client pour les tarifs de vente. Le prix unitaire et les prix de vente sont déterminés à partir de ces tarifs dans les projets associés à une entité commerciale.  
  
 **Copie d’une équipe du projet** : lorsque vous copiez l’équipe du projet à partir du modèle d’un projet, les ressources génériques y sont copiées, avec toutes les aptitudes et compétences définies dans le modèle. Les affectations de ressources génériques sont également gérées comme dans le modèle du projet.  
  
### <a name="see-also"></a>Voir aussi  
 [Guide du responsable de projet](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]