---
title: Chiffres réels
description: Cet article fournit des informations sur la façon d’utiliser les chiffres réels dans Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924795"
---
# <a name="actuals"></a>Chiffres réels

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les chiffres réels représentent l’état d’avancement des finances et du calendrier révisé et approuvé d’un projet. Ils sont créés lorsque les entrées de temps, de dépense et d’utilisation de matériel, les écritures de journal et les factures sont approuvées.

> [!IMPORTANT]
> Les chiffres réels ne doivent pas être modifiés ou supprimés du système. À défaut, l’intégrité financière et toute intégration avec d’autres systèmes financiers et comptables pourraient être affectées négativement. Microsoft Dynamics 365 Project Operations vous permet de contrepasser et de remplacer les chiffres réels pour mettre à jour les valeurs réelles à différents stades du cycle de vie des processus métier de vos projets.

## <a name="recording-actuals-based-on-project-events"></a>Enregistrement des chiffres réels en fonction des événements du projet

Project Operations enregistre les transactions financières qui se produisent pendant le cycle de vie d’un engagement de projet en tant que chiffres réels. La création de chiffres réels à divers événements du cycle de vie varie selon que l’engagement de projet utilise le modèle de facturation pour le temps et les matériaux ou le modèle de facturation à prix fixe, et s’il s’agit d’une phase de prévente ou d’un projet interne.

Les articles suivants expliquent l’impact sur le tableau des chiffres réels lors de divers événements pour différentes variantes :

- [Impact des chiffres réels dans un engagement pour le temps et les matériaux](ActualsonTM.md)
- [Impact des chiffres réels dans un engagement à prix fixe](ActualonFP.md)
- [Impact des chiffres réels pendant la phase de prévente d’un engagement](ActualonPreSales.md)
- [Impact des chiffres réels pour un projet interne](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
