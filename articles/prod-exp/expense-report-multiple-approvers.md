---
title: Plusieurs approbateurs sur une note de frais
description: Cet article fournit des informations sur les états de dépenses qui nécessitent l’approbation par plusieurs personnes.
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
ms.openlocfilehash: ae72ae578455a626c069c01552b3edf60df706a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933949"
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