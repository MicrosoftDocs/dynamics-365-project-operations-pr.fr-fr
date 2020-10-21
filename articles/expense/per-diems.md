---
title: Indemnités quotidiennes
description: Cette rubrique fournit des informations sur les règles d’indemnités journalières utilisées dans la gestion des dépenses.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908102"
---
# <a name="per-diems"></a>Indemnités quotidiennes

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Une indemnité journalière est une allocation versée à un travailleur qui se déplace pour son travail. Dans Gestion des dépenses, vous pouvez créer des règles d’indemnités journalières pour diverses situations de voyage. Les tarifs journaliers peuvent être basés sur la période de l’année, le lieu de voyage ou les deux. Lorsque vous créez une règle d’indemnité journalière, vous pouvez spécifier qu’un pourcentage du tarif journalier sera retenu si un travailleur reçoit des repas ou des services gratuits. Vous pouvez également définir un nombre d’heures minimal et maximal que le taux journalier peut appliquer aux déplacements d’un travailleur.

## <a name="configuration"></a>configuration 

1. Pour ajouter des emplacements d’indemnités journalières, accédez à **Configurer** > **Calculs et codes** > **Emplacements des indemnités journalières**.
2. Pour chacun des emplacements ajoutés ci-dessus, sélectionnez un taux journalier et une devise valables entre une date de début et une date de fin spécifiques pour l’hôtel, les repas et d’autres dépenses. Les taux journaliers et les devises sont configurés sous **Configurer** > **Calculs et codes** > **Indemnités journalières**.
3. Sur la page **Emplacements des indemnités journalières**, configurez les niveaux de taux journalier. Les niveaux de taux journaliers vous permettent de définir le pourcentage de répartition d’une indemnité journalière pour les frais d’hôtel, de repas et autres. 
4. Pour spécifier le pourcentage de réduction de repas pour le petit-déjeuner, le déjeuner ou le dîner, mettez à jour les champs de la page **Paramètres de gestion des dépenses** sur l’onglet **Indemnités journalières**. 
    
## <a name="submit-expenses-using-per-diem"></a>Soumettre les dépenses en utilisant les indemnités journalières
Pour soumettre des dépenses utilisant des indemnités journalières, utilisez la catégorie de dépenses **Indemnités journalières** lorsque vous créez une note de frais. Entrer **Indemnités journalières à partir de la date**, **Indemnités journalières à ce jour** et **Emplacement des indemnités journalières**. Le montant sera calculé en fonction des taux journaliers pour l’emplacement sélectionné et la réduction de repas sera calculée en fonction des niveaux de taux journaliers.
