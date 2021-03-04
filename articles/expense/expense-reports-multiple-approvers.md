---
title: Notes de frais et approbateurs multiples
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l’approbation de plusieurs personnes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120990"
---
# <a name="expense-reports-and-multiple-approvers"></a>Notes de frais et approbateurs multiples

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

En fonction des politiques d’approbation des dépenses de votre organisation, il est possible que l’approbation de plusieurs personnes soit nécessaire lors de la soumission d’une note de frais. Lorsque vous configurez le processus de workflow pour l’approbation des notes de frais, vous pouvez ajouter des éléments de workflow qui incluent des tâches ou des étapes pour un ou plusieurs approbateurs de notes de frais. Par exemple, vous pouvez exiger que toutes les notes de frais soient approuvées par deux personnes distinctes, le responsable de l’employé qui a soumis la note et le coordinateur de la comptabilité fournisseur.

Si vous décidez d’exiger plusieurs approbateurs de notes de frais, vous pouvez ajouter les éléments de workflow de l’une des manières suivantes :

- Ajoutez un élément d’approbation qui comporte une étape. Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par 50 % des membres du groupe d’utilisateurs.
- Ajoutez un élément d’approbation qui comporte plusieurs étapes. Par exemple, l’élément d’approbation peut comporter les étapes suivantes :

    1. Le responsable de l’employé qui a soumis la note de frais l’approuve.
    2. Le commis à la comptabilité fournisseur vérifie les reçus et les articles des notes de frais.
    3. Le responsable du budget approuve la note de frais.

- Ajoutez plusieurs éléments d’approbation, chacun comportant une étape. Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :

    1. Le responsable de l’employé approuve la note de frais.
    2. Le responsable du budget approuve la note de frais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]