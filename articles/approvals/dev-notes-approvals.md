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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="2b2f0-103">Notes de développeur pour les approbations</span><span class="sxs-lookup"><span data-stu-id="2b2f0-103">Developer notes for Approvals</span></span>

<span data-ttu-id="2b2f0-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="2b2f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b2f0-105">Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation.</span><span class="sxs-lookup"><span data-stu-id="2b2f0-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="2b2f0-106">Les transitions d’enregistrement correctes garantissent :</span><span class="sxs-lookup"><span data-stu-id="2b2f0-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="2b2f0-107">Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="2b2f0-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="2b2f0-108">L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="2b2f0-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]