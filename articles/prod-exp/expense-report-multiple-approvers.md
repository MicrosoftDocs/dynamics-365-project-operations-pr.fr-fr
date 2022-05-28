---
title: Plusieurs approbateurs sur une note de frais
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l’approbation de plusieurs personnes.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 383ce9eda6d0604ce0dd090e27a5c6fd569bd9e5
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685283"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Plusieurs approbateurs sur une note de frais

En fonction des politiques d’approbation des dépenses de votre organisation, il est possible que l’approbation d’une note de frais qui est envoyée à un employé. Lorsque vous configurez le processus de workflow pour l’approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais. Par exemple, vous pouvez exiger que toutes les notes de frais soient d’abord approuvées par le responsable de l’employé qui a soumis la note, puis par le coordinateur de la comptabilité fournisseur.

Si vous décidez d’exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l’une des manières suivantes :

- Ajoutez un élément d’approbation comportant une étape. Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par la moitié des membres de ce groupe.
- Ajoutez un élément d’approbation comportant plusieurs étapes. Par exemple, l’élément d’approbation peut comporter les étapes suivantes :

    1. Le responsable du collaborateur ayant envoyé la note de frais l’approuve.
    2. Le commis à la comptabilité fournisseur vérifie les reçus et les éléments de la note de frais.
    3. Le responsable du budget approuve la note de frais.

- Ajoutez plusieurs éléments d’approbation comportant chacun une étape. Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :

    1. Le responsable de l’employé approuve la note de frais.
    2. Le responsable du budget approuve la note de frais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]