---
title: Notes de frais et approbateurs multiples
description: Cette rubrique fournit des informations sur les notes de frais qui nécessitent l’approbation de plusieurs personnes.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002053"
---
# <a name="expense-reports-and-multiple-approvers"></a>Notes de frais et approbateurs multiples

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

En fonction des politiques d’approbation des dépenses de votre organisation, il est possible que l’approbation de plusieurs personnes soit nécessaire lors de la soumission d’une note de frais. Lorsque vous configurez le processus de flux de travail pour l’approbation des notes de frais, vous pouvez ajouter des éléments de flux de travail comprenant des tâches ou des étapes pour un ou plusieurs approbateurs de note de frais. Par exemple, vous pouvez exiger que toutes les notes de frais soient approuvés par deux personnes distinctes : le responsable du collaborateur ayant envoyé la note de frais et le coordinateur de la comptabilité fournisseur.

Si vous décidez d’exiger plusieurs approbateurs de note de frais, vous pouvez ajouter les éléments de flux de travail de l’une des manières suivantes :

- Ajoutez un élément d’approbation comportant une étape. Par exemple, l’étape peut exiger qu’une note de frais soit affectée à un groupe d’utilisateurs et qu’elle soit approuvée par la moitié des membres de ce groupe.
- Ajoutez un élément d’approbation comportant plusieurs étapes. Par exemple, l’élément d’approbation peut comporter les étapes suivantes :

    1. Le responsable du collaborateur ayant envoyé la note de frais l’approuve.
    2. Le commis à la comptabilité fournisseur vérifie les reçus et les éléments de la note de frais.
    3. Le responsable du budget approuve la note de frais.

- Ajoutez plusieurs éléments d’approbation comportant chacun une étape. Par exemple, vous pouvez ajouter un élément d’approbation distinct pour chacune des étapes suivantes :

    1. Le responsable de l’employé approuve la note de frais.
    2. Le responsable du budget approuve la note de frais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]