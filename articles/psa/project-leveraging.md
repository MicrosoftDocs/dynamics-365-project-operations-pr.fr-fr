---
title: Estimations des ventes et projets
description: Cette rubrique indique comment tirer parti de la planification et des estimations dans le processus de vente.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148370"
---
# <a name="sales-estimates-and-projects"></a>Estimations des ventes et projets

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durant le processus de vente, vous pouvez créer des estimations de vente en liant un projet à un devis. De cette façon, l’estimation déterministe peut se produire pendant le processus de vente, pour bénéficier des fonctionnalités de planification et d’estimation du projet. Si la vente est réalisée, la planification utilisée pour l’estimation de ventes peut être utilisée comme base affiner davantage le plan du projet.

## <a name="linking-a-project-to-a-quote-line"></a>Lien d’un projet à une ligne de devis

Lorsque vous créez une ligne de devis basée sur un projet, vous pouvez créer un projet ou associer un projet existant sur la page **Ligne de devis**. 

> ![Formulaire Ligne de devis](media/project-8.png)
 
Lorsque vous créez un projet à partir des détails de la ligne de devis, vous pouvez bénéficier des modèles de projets. Les modèles de projet sont des projets modèles qui représentent des plans de projet standard et des estimations financières qui sont courantes dans une organisation. Ils peuvent également représenter des copies de plans et d’estimations de projets pour des projets passés.

> ![Détails de la ligne de devis](media/project-9.png)
  
Lors de la création de votre projet depuis le devis, le projet est automatiquement associé à la ligne de devis.

## <a name="components-of-estimates-in-a-project"></a>Composants des estimations dans un projet

Une planification vous permet de diviser le travail en tâches, de gérer une hiérarchie des tâches, de déterminer les ressources nécessaires pour effectuer une tâche, et d’attribuer une estimation de l’effort requis pour effectuer une tâche.

Vous pouvez définir des estimations des efforts et de la planification de travail à l’aide de champs sur l’onglet **Planification** de la page **Projet**. Étant donné que les tarifs sont associées au projet, des estimations financières sont calculées en utilisant le coût et les prix de vente définis dans les tarifs.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importation d’estimations depuis un projet dans un devis

Après avoir défini des estimations de projet, vous pouvez les importer dans la ligne de devis. Dans la page **Détails de la ligne de devis**, sélectionnez **Importer à partir des estimations** sur le ruban pour synthétiser les estimations du projet selon le type de transaction, le rôle ou le niveau de tâche.
