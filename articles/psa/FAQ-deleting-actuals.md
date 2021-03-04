---
title: Pourquoi ne parviens-je pas à supprimer d’enregistrements de l’entité Chiffres réels ?
description: Cette rubrique fournit des informations sur la raison pour laquelle vous ne pouvez pas supprimer des enregistrements de l’entité Chiffres réels.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148955"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="bee32-103">Pourquoi ne parviens-je pas à supprimer d’enregistrements de l’entité Chiffres réels ?</span><span class="sxs-lookup"><span data-stu-id="bee32-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bee32-104">Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="bee32-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="bee32-105">Si les chiffres réels pouvaient être supprimés, l’intégrité des transactions de génération de rapports financiers pourrait être remise en cause.</span><span class="sxs-lookup"><span data-stu-id="bee32-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="bee32-106">Pour établir un journal d’audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.</span><span class="sxs-lookup"><span data-stu-id="bee32-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

