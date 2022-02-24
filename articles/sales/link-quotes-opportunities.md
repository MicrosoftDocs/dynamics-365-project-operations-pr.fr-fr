---
title: Créer des devis de projet à partir d’opportunités
description: Cette rubrique fournit des informations sur la création d’un devis de projet à partir d’une opportunité.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d2cc35e3205332d2941bf17fb8c7d8c9d9f310c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118110"
---
# <a name="create-project-quotes-from-opportunities"></a>Créer des devis de projet à partir d’opportunités

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les devis peuvent être créés à partir d’opportunités de projet des manières suivantes :

- À partir de l’onglet **Devis** sur la page **Opportunité de projet**
- À partir du flux des processus de vente Opportunité
- En mettant à jour la référence d’opportunité sur un devis existant

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>À partir de l’onglet Devis de la page Opportunité de projet

Pour créer un devis de projet à partir d’une opportunité, procédez comme suit.

1. Ouvrez la page **Opportunité de projet** et sélectionnez l’onglet **Devis**. 
2. Dans la sous-grille **Devis**, sélectionnez le symbole **+** pour créer un devis de projet basé sur l’opportunité. Toutes les lignes d’opportunité et les tarifs de projet associés sont copiés dans le nouveau devis à partir de l’opportunité.

## <a name="from-the-opportunity-sales-process-flow"></a>À partir du flux des processus de vente Opportunité

Pour créer un devis de projet à partir du flux des processus de vente Opportunité, procédez comme suit.

1. Dans le flux des processus de vente Opportunité, ouvrez l’opportunité.
2. Sélectionnez la phase **Qualifier**. 
3. Sélectionnez **Suivant**, puis **+ Créer** pour créer un devis. La plupart des informations sur l’onglet **Résumé** pour ce nouveau devis seront par défaut à partir de l’opportunité. 
4. Entrez les informations requises manquantes ou mettez à jour les valeurs par défaut si nécessaire sur l’onglet **Résumé**,
5. Sélectionnez **Enregistrer**. Le devis est créé et associé à l’opportunité. Vous pouvez maintenant afficher les informations de devis sur l’onglet **Devis** de la page **Opportunité**. 

   Le processus de vente d’opportunité passe à l’étape suivante, **Proposer**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>En mettant à jour la référence d’opportunité sur un devis existant

Un devis existant peut être lié à une opportunité. Effectuez les étapes suivantes pour mettre à jour les informations d’opportunité sur un devis existant.

1. Ouvrez la page **Devis** et sélectionnez l’onglet **Résumé**.
2. Dans le champ **Opportunité**, sélectionnez l’opportunité que vous souhaitez lier au devis. Vous pouvez voir le devis dans la grille **Devis** de l’opportunité. 
3. À l’aide du processus de vente Opportunité, l’opportunité peut être déplacée vers l’étape suivante, **Proposer**. 

   Lorsque vous déplacez une opportunité vers cette phase, vous pouvez sélectionner ce devis dans une liste de devis associés à cette opportunité. La sélection de ce devis indique que vous poursuivez.

   Tous les autres devis associés à l’opportunité seront toujours disponibles et actifs jusqu’à ce que l’un d’eux soit remporté. Vous pouvez ramener le processus de vente à la phase précédente **Qualifier**, et choisir un autre devis pour avancer.
