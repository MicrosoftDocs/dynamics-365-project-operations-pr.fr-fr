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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290266"
---
# <a name="developer-notes-for-approvals"></a>Notes de développeur pour les approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation. Les transitions d’enregistrement correctes garantissent : 

  - Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.
  - L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]