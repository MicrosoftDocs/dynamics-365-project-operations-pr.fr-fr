---
title: Notes de développeur pour les approbations
description: Cette rubrique fournit des informations supplémentaires aux développeurs sur l’utilisation des approbations.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991663"
---
# <a name="developer-notes-for-approvals"></a>Notes de développeur pour les approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation. Les transitions d’enregistrement correctes garantissent : 

  - Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.
  - L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]