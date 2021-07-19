---
title: Performance de la proposition de facture de projet
description: Cette rubrique fournit des informations sur les améliorations des performances des propositions de facture de projet.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269787"
---
# <a name="project-invoice-proposal-performance"></a>Performance de la proposition de facture de projet

[!include [banner](../includes/banner.md)]

Lorsque vous créez une nouvelle proposition de facture, vous pouvez rencontrer des problèmes de performances à mesure que le nombre de projets et de sous-projets augmente. Pour améliorer les performances, une fonctionnalité est disponible pour réduire le temps nécessaire à la création d’une nouvelle proposition de facture pour les transactions de projet validées.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Activer l’amélioration des performances de la proposition de facture de projet
Pour activer la fonctionnalité d’amélioration des performances de la proposition de facture de projet, procédez comme suit.

1.  Accédez à **Gestion des fonctionnalités** > **Tout**. Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.
2.  Sélectionnez **Activer maintenant**.
3.  Actualisez votre navigateur, puis créez une nouvelle proposition de facture.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Désactiver l’amélioration des performances de la proposition de facture de projet
Procédez de la manière suivante pour désactiver l’amélioration des performances de la proposition de facture de projet.

1.  Accédez à **Gestion des fonctionnalités** > **Tout**. Dans la liste des fonctionnalités, recherchez **Amélioration des performances de la proposition de facture de projet**.
2.  Sélectionnez **Désactiver**.
3.  Actualisez votre navigateur.

> [!NOTE]
> Les performances de la proposition de facture ne peuvent pas être appliquées lorsque les règles de facturation sont activées.
> 
> Pendant le traitement par lots pour créer des propositions de facture, le nombre de sous-tâches fractionnera les tâches en un nombre maximal en fonction du nombre de contrats avec des transactions facturables, indépendamment de votre saisie. Par exemple, si vous entrez **3** pour le nombre de sous-tâches pour la création de propositions de facture par lots et il n’y a que deux contrats avec des transactions facturables, seules deux sous-tâches sont créées.
