---
title: Estimations des ventes et projets
description: Cette rubrique indique comment tirer parti de la planification et des estimations dans le processus de vente.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168025"
---
# <a name="sales-estimates-and-projects"></a>Estimations des ventes et projets

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durant le processus de vente, vous pouvez créer des estimations de vente en liant un projet à un devis. De cette façon, l'estimation déterministe peut se produire pendant le processus de vente, pour bénéficier des fonctionnalités de planification et d'estimation du projet. Si la vente est réalisée, la planification utilisée pour l'estimation de ventes peut être utilisée comme base affiner davantage le plan du projet.

## <a name="linking-a-project-to-a-quote-line"></a>Lien d'un projet à une ligne de devis

Lorsque vous créez une ligne de devis basée sur un projet, vous pouvez créer un projet ou associer un projet existant sur la page **Ligne de devis**. 

> ![Formulaire Ligne de devis](media/project-8.png)
 
Lorsque vous créez un projet à partir des détails de la ligne de devis, vous pouvez bénéficier des modèles de projets. Les modèles de projet sont des projets modèles qui représentent des plans de projet standard et des estimations financières qui sont courantes dans une organisation. Ils peuvent également représenter des copies de plans et d'estimations de projets pour des projets passés.

> ![Détails de la ligne de devis](media/project-9.png)
  
Lors de la création de votre projet depuis le devis, le projet est automatiquement associé à la ligne de devis.

## <a name="components-of-estimates-in-a-project"></a>Composants des estimations dans un projet

Une planification vous permet de diviser le travail en tâches, de gérer une hiérarchie des tâches, de déterminer les ressources nécessaires pour effectuer une tâche, et d'attribuer une estimation de l'effort requis pour effectuer une tâche.

Vous pouvez définir des estimations des efforts et de la planification de travail à l'aide de champs sur l'onglet **Planification** de la page **Projet**. Étant donné que les tarifs sont associées au projet, des estimations financières sont calculées en utilisant le coût et les prix de vente définis dans les tarifs.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importation d'estimations depuis un projet dans un devis

Après avoir défini des estimations de projet, vous pouvez les importer dans la ligne de devis. Dans la page **Détails de la ligne de devis**, sélectionnez **Importer à partir des estimations** sur le ruban pour synthétiser les estimations du projet selon le type de transaction, le rôle ou le niveau de tâche.