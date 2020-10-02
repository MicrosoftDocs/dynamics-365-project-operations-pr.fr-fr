---
title: Définir des calendriers de projet
description: Cette rubrique fournit des informations sur l'utilisation d'un calendrier pour suivre l'avancée d'un projet.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897988"
---
# <a name="define-project-calendars"></a>Définir des calendriers de projet

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Pour créer une planification de projet, créez un modèle de calendrier de projet qui définit le nombre d'heures de travail par jour et les heures de fermeture. Pour créer un modèle de calendrier de projet, vous associez un modèle de travail au champ **Modèle de calendrier** du projet. Pour créer un modèle de travail, procédez comme suit.

1. Sélectionnez **Ressources** dans le volet de navigation de gauche. 
2. Sur la page de liste **Ressources**, ouvrez enregistrement utilisateur, puis sélectionnez **Afficher les heures de travail**.

  > [!NOTE]
  > Vérifiez que vous autorisez les fenêtres contextuelles sur la page de navigateur. Cela vous permet de voir les heures de travail définies pour la ressource.
  
3. Dans l'onglet **Vue mensuelle**, cliquez sur **Configuration**. Une liste de trois options apparaît : 

  - Nouvelle planification hebdomadaire
  - Planification des tâches sur un jour
  - Absence

4. Sélectionnez **Nouvelle planification hebdomadaire**, puis définissez les options de cette planification de ressource. Vous pouvez définir une planification hebdomadaire récurrente, des paramètres d'heure quotidiens, des fermetures de bureaux, et plus encore.
5. Définissez la plage de dates, la sélectionnez **Enregistrer**, puis cliquez sur **Fermer**. 
6. Revenez à la page de liste **Ressources**, puis sélectionnez la ressource pour laquelle vous avez défini les heures de travail. 
7. Sélectionnez **Définir le calendrier comme** pour définir le modèle de travail. 
8. Dans la boîte de dialogue **Modèle de travail**, entrez le nom pour le modèle de travail, puis sélectionnez **Appliquer**. 

Vous pouvez désormais associer le modèle de travail à un modèle de calendrier de projet.
