---
title: Notes de frais et approbateurs multiples
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l'approbation de plusieurs personnes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897088"
---
# <a name="expense-reports-and-multiple-approvers"></a>Notes de frais et approbateurs multiples

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

En fonction des politiques d'approbation des dépenses de votre organisation, il est possible que l'approbation de plusieurs personnes soit nécessaire lors de la soumission d'une note de frais. Lorsque vous configurez le processus de workflow pour l'approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais. Par exemple, vous pouvez exiger que toutes les notes de frais soient approuvées par deux personnes distinctes, le responsable de l'employé qui a soumis la note et le coordinateur de la comptabilité fournisseur.

Si vous décidez d'exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l'une des manières suivantes :

- Ajoutez un élément d'approbation qui comporte une étape. Par exemple, l'étape peut exiger qu'une note de frais soit affectée à un groupe d'utilisateurs et qu'elle soit approuvée par 50 % des membres du groupe d'utilisateurs.
- Ajoutez un élément d'approbation qui comporte plusieurs étapes. Par exemple, l'élément d'approbation peut comporter les étapes suivantes :

    1. Le responsable de l'employé qui a soumis la note de frais l'approuve.
    2. Le commis à la comptabilité fournisseur vérifie les reçus et les articles des notes de frais.
    3. Le responsable du budget approuve la note de frais.

- Ajoutez plusieurs éléments d'approbation, chacun comportant une étape. Par exemple, vous pouvez ajouter un élément d'approbation distinct pour chacune des étapes suivantes :

    1. Le responsable de l'employé approuve la note de frais.
    2. Le responsable du budget approuve la note de frais.
