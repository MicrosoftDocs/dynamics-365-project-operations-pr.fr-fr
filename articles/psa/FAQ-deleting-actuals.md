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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286065"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c1f9d-103">Pourquoi ne parviens-je pas à supprimer d’enregistrements de l’entité Chiffres réels ?</span><span class="sxs-lookup"><span data-stu-id="c1f9d-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c1f9d-104">Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="c1f9d-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c1f9d-105">Si les chiffres réels pouvaient être supprimés, l’intégrité des transactions de génération de rapports financiers pourrait être remise en cause.</span><span class="sxs-lookup"><span data-stu-id="c1f9d-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c1f9d-106">Pour établir un journal d’audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.</span><span class="sxs-lookup"><span data-stu-id="c1f9d-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]