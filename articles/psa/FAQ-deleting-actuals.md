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
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Pourquoi ne parviens-je pas à supprimer d'enregistrements de l'entité Chiffres réels ?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité. Si les chiffres réels pouvaient être supprimés, l'intégrité des transactions de génération de rapports financiers pourrait être remise en cause. Pour établir un journal d'audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.

