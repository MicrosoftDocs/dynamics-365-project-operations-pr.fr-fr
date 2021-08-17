---
title: Éliminer une estimation de projet
description: Cette rubrique fournit des informations sur l’élimination d’une estimation de projet une fois qu’elle est terminée.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a7c9f5a03e3b5e9ad43e23c6174a820088025dc8419ae4f80d247d69e80c8038
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994093"
---
# <a name="eliminate-a-project-estimate"></a>Éliminer une estimation de projet

[!include [banner](../includes/banner.md)]

Les estimations du projet fournissent une vue financière de la tâche qui est prévue et planifiée pour un projet. Pour travailler avec des devis pour un projet, vous devez attacher le projet à un projet d’estimation. Un projet d’estimation est toujours basé sur un projet existant, cependant plusieurs projets peuvent faire référence à un seul projet d’estimation. Seuls les projets à prix fixe et d’investissement peuvent être associés à des projets d’estimation, et ces projets doivent appartenir au même groupe de projets que le projet d’estimation.

Pour éliminer un projet d’estimation, il doit être complet. Les étapes suivantes expliquent comment éliminer une estimation.

1. Accédez à **Gestion de projets et comptabilité** > **Tous les projets** et ouvrez le projet. 
2. Dans l’onglet **Gérer**, sélectionnez **Estimations** et sur la page **Estimation**, sélectionnez **Éliminer**.
3. Sur la page **Éliminer l’estimation** de l’onglet **Général**, définissez les options suivantes :

   - **Code de période** : Sélectionnez le code de période pour choisir les projets d’estimation appropriés. 
   - **Date estimée** : Sélectionnez la date d’estimation appropriée pour l’élimination.
   - **Éliminer avec les avertissements WIP** : Activez cette option pour fournir une notification lorsqu’une estimation associée à un travail en cours (WIP) sera éliminée. Lorsque cette option n’est pas activée, l’élimination ne peut pas continuer s’il existe des transactions non estimées. 
   > [!NOTE]
   > Cette option n’est disponible que lorsque l’élimination est appliquée à un projet d’estimation. Il n’est pas disponible si vous utilisez des écritures périodiques. Ce paramètre fonctionne avec les paramètres de l’onglet **Estimation** dans la page **Paramètres du projet**, dans le groupe de champs **Autoriser l’élimination lorsqu’il existe des transactions non estimées**.
   - **Définir l’étape sur Terminé** : Activez cette option pour définir l’étape du projet d’estimation sur **Terminé** après avoir exécuté l’élimination.
   - **Imprimer la liste des devis** : Sélectionnez les informations à inclure lors de l’impression de la liste d’estimations.
   - **Afficher l’infolog** : Activez cette option pour afficher l’infolog.
   - **Date de validation** : Choisissez la date de validation comptable de l’estimation.

4.  Cliquez sur **OK**.
5. Une fois le processus d’élimination terminé, le projet d’estimation éliminé est affiché avec une valeur négative. 

Si vous n’aviez pas l’intention d’éliminer une estimation, vous pouvez sélectionner l’estimation éliminée, puis **Élimination inverse**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]