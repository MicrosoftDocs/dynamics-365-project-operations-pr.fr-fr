---
title: Notes de développeur pour les approbations
description: Cette rubrique fournit des informations supplémentaires aux développeurs sur l’utilisation des approbations.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483945"
---
# <a name="developer-notes-for-approvals"></a>Notes de développeur pour les approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation. Les transitions d’enregistrement correctes garantissent : 

  - Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.
  - L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]