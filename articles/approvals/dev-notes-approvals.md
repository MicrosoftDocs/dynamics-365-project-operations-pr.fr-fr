---
title: Notes de développeur pour les approbations
description: Cette rubrique fournit des informations supplémentaires aux développeurs sur l’utilisation des approbations.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579717"
---
# <a name="developer-notes-for-approvals"></a>Notes de développeur pour les approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation. Les transitions d’enregistrement correctes garantissent : 

  - Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.
  - L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]