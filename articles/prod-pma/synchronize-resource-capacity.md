---
title: Synchroniser une capacité de ressource
description: Cette rubrique fournit des informations sur la synchronisation de la capacité d’une ressource entre les calendriers et les projets.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f2e9b8e189be0594569e14ebc41c6ed452afd10aba34ea1397b3e3f66cd2e96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005613"
---
# <a name="synchronize-resource-capacity"></a>Synchroniser une capacité de ressource

[!include [banner](../includes/banner.md)]

Les processus de synchronisation des ressources permettent de garantir que les informations du calendrier et du calendrier de base se retrouvent dans la planification des ressources du projet. Si le calendrier est modifié, les processus apportent les mises à jour nécessaires à la planification des ressources du projet. Les processus contribuent également à améliorer les performances, car les informations sur les ressources du calendrier sont synchronisées à l’avance. Par conséquent, les mises à jour des informations de planification des ressources se produisent plus rapidement. Nous vous recommandons de planifier les processus comme un lot au lieu d’un à la fois. Sinon, il y a un risque que quelqu’un oublie les dates incluses lors de la dernière synchronisation des informations. Si les dates inclusives ne sont pas utilisées, des intervalles peuvent se produire lors de la synchronisation des dates.

![Synchronisation du calendrier.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchroniser les reports de la capacité d’une ressource

Le processus de synchronisation est conçu pour synchroniser toutes les informations du calendrier des ressources. Ces informations incluent des informations de calendrier de base sur les modifications apportées à la table de capacité du calendrier des ressources du projet. Si de nouvelles ressources sont ajoutées dans le projet, la synchronisation permet de garantir que les informations de calendrier mises à jour sont disponibles. Cette synchronisation peut être effectuée à tout moment.

Nous vous recommandons d’utiliser un lot. Les options sont disponibles lors de la synchronisation des réservations de capacité.

1. Sélectionnez **Gestion de projet et comptabilité** &gt; **Périodique** &gt; **Synchronisation de la capacité** &gt; **Synchroniser les cumuls de capacité des ressources**.
2. Définissez les options dans le tableau suivant.

    | Option      | Description |
    |-------------|-------------|
    | Code de période | Sélectionnez éventuellement le code d’intervalle de dates du grand livre général pour définir les dates de début et de fin du processus de synchronisation pour les cumuls de capacité de ressources. |
    | Date de début  | Entrez la date de début du processus de synchronisation pour les cumuls de capacité des ressources. |
    | Date de fin    | Entrez la date de fin du processus de synchronisation pour les cumuls de capacité des ressources. |

[![Processus de synchronisation.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]