---
title: Modèles de projet
description: Cette rubrique fournit des informations sur l'utilisation des modèles de projet pour un paramétrage rapide de projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168020"
---
# <a name="project-templates"></a>Modèles de projet 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un modèle de projet est un cadre prédéfini qui vous permet de démarrer rapidement et facilement un projet. Vous pouvez utiliser un modèle prédéfini pour créer un projet avec un simple clic. Quant aux projets, vous devez définir les conditions préalables pour les modèles de projet. Vous devez définir un calendrier de projet pour chaque modèle de projet, et des rôles et des tarifs doivent être prédéfinis dans l'organisation, afin que les composants du modèle aient des informations utiles.

Un modèle de projet est composé de trois composants : une planification, des estimations de projet, et des membres de l'équipe de projet.

## <a name="schedule"></a>Planifier

Une planification dans un modèle de projet possède le même ensemble d'éléments qu'une planification dans un projet. Vous pouvez créer une hiérarchie de tâches, associer des rôles aux tâches, définir des attributs de planification et définir des dépendances. Une planification dans un modèle de projet prend également en charge les modes de tâches de chaque tâche. Par conséquent, il prend en charge le moteur de planification. Vous devez associer un calendrier de projet au projet. Lors de la création d'une planification des tâches, il n'y a aucune différence entre un modèle de projet et un projet.

## <a name="project-estimates"></a>Estimations de projets

Les estimations de projet dans un modèle de projet fonctionnent de la même manière que des estimations de projet dans un projet. Toutefois, le coût et les prix de vente sont extraits des listes de coût et des tarifs de vente par défaut qui sont définis dans les paramètres.

## <a name="creating-a-project-from-a-template"></a>Création d'un projet à partir d'un modèle
 
Il existe plusieurs manières de créer un projet à partir d'un modèle de projet :

- Lorsque vous créez un projet à partir d'un devis, vous pouvez sélectionner un modèle de projet dans la boîte de dialogue **Création rapide : Projet**.

> ![Boîte de dialogue Création rapide : Projet](media/project-11.png)

- Lorsque vous créez un projet en sélectionnant **Nouveau projet**, la page **Projet** s'affiche avant l'enregistrement. Dans le champ **Choisir un modèle**, sélectionnez l'un des modèles de projet prédéfinis dans l'organisation.
- Utilisez **Créer un projet à partir d'un modèle** sur la page **Entité Modèle**.

## <a name="copying-components-of-template-to-project"></a>Copie de composants de modèle dans un projet

Lorsque vous copiez les composants d'un modèle de projet dans un projet, certains chevauchement peuvent se produire, selon les paramètres du projet.

### <a name="copying-the-schedule"></a>Copie de la planification

Lorsque vous copiez la planification d'un modèle de projet, si le projet a un calendrier de projet différent du modèle, les heures de travail du calendrier du projet sont appliquées au programme des tâches. Ainsi, la planification est ajustée au calendrier du projet de sauvegarde. De même, la première tâche de la planification prend la date de début du projet, la planification du reste de la hiérarchie est mise à jour selon la durée et les dépendances spécifiées dans le modèle. 

### <a name="copying-project-estimates"></a>Copie d'estimations de projets 

Lorsque vous copiez dans les lignes d'estimation du projet, les tarifs sont mis à jour. Pour la liste de prix de revient, ces mises à jour sont basées sur l'unité propriétaire du projet. Pour les tarifs de vente, ils sont basés sur le client. Pour les projets associés à une entité commerciale, le prix unitaire et les prix de vente sont déterminés sur la base de ces tarifs.

### <a name="copying-a-project-team"></a>Copie d'une équipe de projet

Lorsque vous copiez une équipe de projet à partir du modèle d'un projet, les ressources génériques sont copiées, avec toutes les aptitudes et compétences définies dans le modèle. Les affectations de ressources génériques sont également gérées comme elles l'étaient dans le modèle du projet. Les ressources nommées ne sont pas prises en charge dans les modèles de projet.
