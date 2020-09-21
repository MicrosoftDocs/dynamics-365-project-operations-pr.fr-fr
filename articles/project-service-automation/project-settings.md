---
title: Paramètres du projet
description: Cette rubrique fournit des informations sur les paramètres de gestion du projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168022"
---
# <a name="project-settings"></a>Paramètres du projet

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utilisez les paramètres suivants pour accéder aux fonctionnalités de planification du projet.

## <a name="work-template"></a>Modèle de travail

Pour créer une planification de projet, créez un modèle de calendrier de projet qui définit le nombre d'heures de travail par jour et les heures de fermeture. Pour créer un modèle de calendrier de projet, vous associez un modèle de travail au champ **Modèle de calendrier** du projet. Pour créer un modèle de travail, procédez comme suit.

1. Dans PSA, dans le volet de navigation gauche, cliquez sur **Ressources**. 
2. Sur la page de liste **Ressources**, ouvrez enregistrement utilisateur, puis sélectionnez **Afficher les heures de travail**.

  > [!NOTE]
  > Vérifiez que vous autorisez les fenêtres contextuelles sur la page de navigateur. Cela vous permet de voir les heures de travail définies pour la ressource.
  
3. Dans l'onglet **Vue mensuelle**, cliquez sur **Configuration**. Une liste de trois options apparaît : 

  - Nouvelle planification hebdomadaire
  - Planification des tâches sur un jour
  - Absence

> ![Groupe d’options](media/project-13.png)

4. Sélectionnez **Nouvelle planification hebdomadaire**, puis définissez les options de cette planification de ressource. Vous pouvez définir une planification hebdomadaire récurrente, des paramètres d'heure quotidiens, des fermetures de bureaux, et plus encore.
5. Définissez la plage de dates, la sélectionnez **Enregistrer**, puis cliquez sur **Fermer**. 
6. Revenez à la page de liste **Ressources**, puis sélectionnez la ressource pour laquelle vous avez défini les heures de travail. 
7. Sélectionnez **Définir le calendrier comme** pour définir le modèle de travail. 
8. Dans la boîte de dialogue **Modèle de travail**, entrez le nom pour le modèle de travail, puis sélectionnez **Appliquer**. 

Vous pouvez désormais associer le modèle de travail à un modèle de calendrier de projet.

## <a name="resource-roles"></a>Rôles des ressources

Le terme *rôle de la ressource* fait référence à l'ensemble de compétences, de qualifications et de certifications qu'une personne doit avoir pour effectuer un ensemble spécifique de tâches sur un projet. PSA vous permet d'établir le coût et de facturer le temps d'une ressource en fonction du rôle auquel la ressource est associée. Chaque organisation doit configurer ces rôles à l'aide de la navigation gauche sur le menu **Project Service**.

Chaque organisation doit configurer ces rôles sur la page **Catégories de ressources actives**. Pour ouvrir cette page, dans le volet de navigation de gauche, sélectionnez **Rôles des ressources**.

## <a name="price-lists"></a>Tarifs

Les tarifs vous permettent de définir le coût et les prix de vente des rôles de ressources, des catégories de dépenses, des produits et d'autres éléments dans votre organisation. Avant de définir des estimations financières pour le travail à fournir pour un projet, vous devez créer un coût de support et des tarifs de vente. Dans la section des paramètres, vous devez configurer un coût et des tarifs de vente par défaut qui s'appliquent à tous les projets créés dans l'organisation. Dans la page **Paramètres du projet actifs**, vérifiez que vous configurez un coût et des tarifs de vente par défaut.
