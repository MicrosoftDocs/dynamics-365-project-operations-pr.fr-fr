---
title: Notes de développeur pour les approbations
description: Cet article fournit des informations de développeur supplémentaires sur l’utilisation des approbations.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924749"
---
# <a name="developer-notes-for-approvals"></a>Notes de développeur pour les approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation. Les transitions d’enregistrement correctes garantissent : 

  - Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.
  - L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]