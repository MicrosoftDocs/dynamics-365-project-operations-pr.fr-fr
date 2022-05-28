---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581281"
---
# <a name="actuals"></a>Chiffres réels

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les chiffres réels représentent l’état d’avancement des finances et du calendrier révisé et approuvé d’un projet. Ils sont créés lorsque les entrées de temps, de dépense et d’utilisation de matériel, les écritures de journal et les factures sont approuvées.

> [!IMPORTANT]
> Les chiffres réels ne doivent pas être modifiés ou supprimés du système. À défaut, l’intégrité financière et toute intégration avec d’autres systèmes financiers et comptables pourraient être affectées négativement. Microsoft Dynamics 365 Project Operations vous permet de contrepasser et de remplacer les chiffres réels pour mettre à jour les valeurs réelles à différents stades du cycle de vie des processus métier de vos projets.

## <a name="recording-actuals-based-on-project-events"></a>Enregistrement des chiffres réels en fonction des événements du projet

Project Operations enregistre les transactions financières qui se produisent pendant le cycle de vie d’un engagement de projet en tant que chiffres réels. La création de chiffres réels à divers événements du cycle de vie varie selon que l’engagement de projet utilise le modèle de facturation pour le temps et les matériaux ou le modèle de facturation à prix fixe, et s’il s’agit d’une phase de prévente ou d’un projet interne.

Les rubriques suivantes expliquent l’impact sur le tableau des chiffres réels lors de divers événements pour différentes variantes :

- [Impact des chiffres réels dans un engagement pour le temps et les matériaux](ActualsonTM.md)
- [Impact des chiffres réels dans un engagement à prix fixe](ActualonFP.md)
- [Impact des chiffres réels pendant la phase de prévente d’un engagement](ActualonPreSales.md)
- [Impact des chiffres réels pour un projet interne](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
