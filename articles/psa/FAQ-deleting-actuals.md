---
title: Pourquoi ne parviens-je pas à supprimer d'enregistrements de l'entité Chiffres réels ?
description: Cette rubrique fournit des informations sur la raison pour laquelle vous ne pouvez pas supprimer des enregistrements de l'entité Chiffres réels.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075866"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="7ddcd-103">Pourquoi ne parviens-je pas à supprimer d'enregistrements de l'entité Chiffres réels ?</span><span class="sxs-lookup"><span data-stu-id="7ddcd-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7ddcd-104">Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="7ddcd-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="7ddcd-105">Si les chiffres réels pouvaient être supprimés, l'intégrité des transactions de génération de rapports financiers pourrait être remise en cause.</span><span class="sxs-lookup"><span data-stu-id="7ddcd-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="7ddcd-106">Pour établir un journal d'audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.</span><span class="sxs-lookup"><span data-stu-id="7ddcd-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

