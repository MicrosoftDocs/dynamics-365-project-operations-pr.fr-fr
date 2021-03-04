---
title: Plusieurs approbateurs sur une note de frais
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l'approbation de plusieurs personnes.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960604"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Plusieurs approbateurs sur une note de frais

En fonction des politiques d'approbation des dépenses de votre organisation, il est possible que l'approbation d'une note de frais qui est envoyée à un employé. Lorsque vous configurez le processus de workflow pour l'approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais. Par exemple, vous pouvez exiger que toutes les notes de frais soient d'abord approuvées par le responsable de l'employé qui a soumis la note, puis par le coordinateur de la comptabilité fournisseur.

Si vous décidez d'exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l'une des manières suivantes :

- Ajoutez un élément d’approbation qui comporte une étape. Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par 50 % des membres du groupe d’utilisateurs.
- Ajoutez un élément d’approbation qui comporte plusieurs étapes. Par exemple, l’élément d’approbation peut comporter les étapes suivantes :

    1. Le responsable de l’employé qui a soumis la note de frais l’approuve.
    2. Le commis à la comptabilité fournisseur vérifie les reçus et les articles des notes de frais.
    3. Le responsable du budget approuve la note de frais.

- Ajoutez plusieurs éléments d’approbation, chacun comportant une étape. Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :

    1. Le responsable de l’employé approuve la note de frais.
    2. Le responsable du budget approuve la note de frais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]