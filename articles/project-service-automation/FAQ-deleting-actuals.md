---
title: Pourquoi ne parviens-je pas à supprimer d'enregistrements de l'entité Chiffres réels ?
description: Cette rubrique fournit des informations sur la raison pour laquelle vous ne pouvez pas supprimer des enregistrements de l'entité Chiffres réels.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167993"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="7f07e-103">Pourquoi ne parviens-je pas à supprimer d'enregistrements de l'entité Chiffres réels ?</span><span class="sxs-lookup"><span data-stu-id="7f07e-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7f07e-104">Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="7f07e-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="7f07e-105">Si les chiffres réels pouvaient être supprimés, l'intégrité des transactions de génération de rapports financiers pourrait être remise en cause.</span><span class="sxs-lookup"><span data-stu-id="7f07e-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="7f07e-106">Pour établir un journal d'audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.</span><span class="sxs-lookup"><span data-stu-id="7f07e-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

