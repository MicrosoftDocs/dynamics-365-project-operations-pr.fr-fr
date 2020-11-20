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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="d7444-103">Notes de développeur pour les approbations</span><span class="sxs-lookup"><span data-stu-id="d7444-103">Developer notes for Approvals</span></span>

<span data-ttu-id="d7444-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="d7444-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d7444-105">Dynamics 365 Project Operations comprend une logique de validation qui garantit une transition d’enregistrement correcte tout au long des étapes d’approbation.</span><span class="sxs-lookup"><span data-stu-id="d7444-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="d7444-106">Les transitions d’enregistrement correctes garantissent :</span><span class="sxs-lookup"><span data-stu-id="d7444-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="d7444-107">Toutes les lignes associées sont créées dans des tables connexes, telles que les journaux et les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="d7444-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="d7444-108">L’approbateur est marqué comme **Approbateur du projet** dans le projet avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="d7444-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
