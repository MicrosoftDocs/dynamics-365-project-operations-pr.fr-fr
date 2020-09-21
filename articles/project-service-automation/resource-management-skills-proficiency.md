---
title: Modèles de qualifications et de compétences
description: Cette rubrique donne des informations sur l'utilisation des modèles de qualifications et de compétences.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168129"
---
# <a name="skills-and-proficiency-models"></a>Modèles de qualifications et de compétences

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les compétences sont des caractéristiques de ressource partagées entre Dynamics 365 Project Service Automation et, le cas échéant Dynamics 365 Field Service. 

Pour maintenir le référentiel de compétences de Project Service Automation, accédez à **Ressources** \> **Qualifications de la ressource**. 

> ![Qualifications de la ressource](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Utilisez les modèles de compétences pour estimer des ressources

Les compétences des ressources sont estimées selon des modèles de compétences. Les évaluations individuelles sont dans un modèle de compétences. 

1. Pour créer un modèle de compétences, accédez à **Ressources** \> **Modèles de compétences**, puis sélectionnez **Nouveau**.
2. Dans le nouveau modèle d'évaluation, spécifiez la valeur d'évaluation minimale, la valeur d'évaluation maximale et l'entité qui est estimée.
3. Dans la sous-grille dans **Valeurs d'évaluation**, vous pouvez définir des valeurs d'évaluation différentes, du minimum au maximum.

> ![Évaluations minimale et maximale définies](media/Resource-Management-image85.png)

Ces valeurs d'évaluation sont affichées dans les filtres **Besoins en ressources**, **Tableau de planification** et **Assistant Planifier**.
