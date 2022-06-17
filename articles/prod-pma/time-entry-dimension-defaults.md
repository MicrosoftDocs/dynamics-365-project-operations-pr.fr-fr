---
title: Appliquer par défaut des dimensions financières aux entrées de temps de projet
description: Cet article donne des informations sur l’application par défaut de dimensions financières aux entrées de temps.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916561"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Appliquer par défaut des dimensions financières aux entrées de temps de projet

[!include [banner](../includes/banner.md)]

Lorsque vous utiliser les dimensions financières aux entrées de temps de projet, la valeur de dimension par défaut est évaluée dans l’ordre suivant :

1. Ressource
2. Project
3. Source de financement

Par exemple, si la dimension par défaut est spécifiée sur une ressource, la valeur par défaut est appliquée par-dessus une valeur par défaut spécifiée sur le projet. De la même manière, si la dimension par défaut est spécifiée sur un projet, la valeur par défaut est appliquée par-dessus une valeur par défaut spécifiée sur la source financement.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
