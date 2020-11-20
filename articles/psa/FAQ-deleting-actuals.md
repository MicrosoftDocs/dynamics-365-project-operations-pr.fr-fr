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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127155"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Pourquoi ne parviens-je pas à supprimer d’enregistrements de l’entité Chiffres réels ?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne vous permet pas de supprimer des chiffres réels, car ils servent de source fiable pour les transactions qui ont des implications financières à des systèmes en aval, tels que la comptabilité. Si les chiffres réels pouvaient être supprimés, l’intégrité des transactions de génération de rapports financiers pourrait être remise en cause. Pour établir un journal d’audit, les clients doivent utiliser des journaux pour créer des transactions de compensation.

