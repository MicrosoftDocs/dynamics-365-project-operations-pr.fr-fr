---
title: Appliquer par défaut des dimensions financières aux entrées de temps de projet
description: Cette rubrique donne des informations sur l’application par défaut de dimensions financières aux entrées de temps.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597933"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Appliquer par défaut des dimensions financières aux entrées de temps de projet

[!include [banner](../includes/banner.md)]

Lorsque vous utiliser les dimensions financières aux entrées de temps de projet, la valeur de dimension par défaut est évaluée dans l’ordre suivant :

1. Ressource
2. Project
3. Source de financement

Par exemple, si la dimension par défaut est spécifiée sur une ressource, la valeur par défaut est appliquée par-dessus une valeur par défaut spécifiée sur le projet. De la même manière, si la dimension par défaut est spécifiée sur un projet, la valeur par défaut est appliquée par-dessus une valeur par défaut spécifiée sur la source financement.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
