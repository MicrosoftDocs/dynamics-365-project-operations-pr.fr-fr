---
title: Configurer le kilométrage à l’aide de barèmes de kilométrage
description: Cette rubrique fournit des informations sur les taux de kilométrage et les niveaux de taux de kilométrage.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 030c6abca169b712312ad70ed2ac8262f3d0777bcf93dcccfd956f2f9e0ea77c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993058"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurer le kilométrage à l’aide de barèmes de kilométrage

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Lorsqu’une dépense est déclarée et que la catégorie de dépenses sélectionnée est **Kilométrage**, le montant de cette ligne de dépense est calculé selon le montant du *tarif au kilométrage*. Ce montant est déterminé en utilisant des niveaux de kilométrage définis ou, si aucun niveau de taux de kilométrage n’est configuré, en suivant un taux de kilométrage standard. 

Les niveaux de taux de kilométrage peuvent être configurés en accédant à **Gestion des dépenses** > **Configuration** > **Général** > **Catégories de dépenses** > **Kilométrage** > **Configuration de la catégorie**.

Après la mise à niveau vers la version 10.0.18, si votre organisation utilise la catégorie de dépense de kilométrage, envisagez d’activer la fonction kilométrage après avoir examiné les modifications de conception ci-dessous. 

La nouvelle conception des niveaux de taux de kilométrage influe sur le traitement de la valeur du champ **Quantité**. Avant la parution de la version 10.0.18, la valeur du champ **Quantité** était considérée comme la limite inférieure. Lorsque le cumul dépassait cette valeur, le taux correspondant était utilisé.  Depuis la version 10.0.18, la valeur du champ **Quantité** est considérée comme la limite supérieure. Le taux correspondant est utilisé lorsque le kilométrage cumulé est inférieur à la valeur du champ **Quantité**.  Le nouveau modèle des niveaux de kilométrage renforce la cohérence entre les niveaux de kilométrage et facilite leur utilisation.   

Toutes les notes de frais approuvées seront recalculées lors de la validation conformément à la nouvelle conception.

## <a name="example"></a>Exemple
 
### <a name="before-version-10018"></a>Avant la version 10.0.18
Avec deux niveaux de taux de kilométrage, le champ **Quantité** dans chaque niveau représente la limite inférieure du kilométrage. Actuellement, le niveau un a une valeur de zéro (0) et un taux de 0,45, et le niveau deux a une valeur de 1000 et un taux de 0,25. Si les miles ou kilomètres cumulés croisent la valeur du champ, le taux correspondant est utilisé. S’il n’existe aucune ligne avec une quantité nulle, le système utilise le taux de kilométrage défini dans la Gestion des dépenses. 
 
Si un employé soumet une note de frais avec 1 500 miles, les deux lignes de kilométrage de la note de frais validées sont : 1 000 (taux 0,45) + 500 (taux 0,25) = 575.

### <a name="after-version-10018"></a>Après la version 10.0.18
Dans la version 10.0.18, le champ **Quantité** dans chaque niveau représente la limite supérieure du niveau. Actuellement, le niveau un a une valeur de 999 et un taux de 0,45, et le niveau deux a une valeur de 999 999 999,00 et un taux de 0,25. Si les miles ou kilomètres cumulés croisent la valeur du champ **Quantité**, le taux correspondant est utilisé. Si toutes les limites supérieures sont dépassées, le système utilise le taux de kilométrage défini dans la Gestion des dépenses. 
 
Pour calculer correctement le même scénario, il convient de modifier la configuration du niveau. Le champ **Quantité** du niveau un a une valeur de 999,00 et une valeur de 999 999 999,00 au niveau deux. Si un employé dépasse la quantité totale de miles ou de kilomètres dans le niveau un, le système utilise le taux de kilométrage défini dans la Gestion des dépenses. 
  
Si un employé soumet une note de frais avec 1 500 miles, les deux lignes de kilométrage de la note de frais validées sont : 1 000 (taux 0,45) + 500 (taux 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Activer le calcul du montant du kilométrage pour plusieurs niveaux de kilométrage avec le même taux

La fonctionnalité **Calcul du montant du kilométrage pour plusieurs niveaux de kilométrage avec le même taux** améliore le calcul du taux de kilométrage. Procédez de la manière suivante pour activer cette fonctionnalité.

1. Accédez à **Espaces de travail** > **Gestion des fonctionnalités**. 
2. Dans la liste, recherchez et sélectionnez **Calcul du montant du kilométrage pour plusieurs niveaux de kilométrage avec le même taux**, puis sélectionnez **Activer maintenant**.

Après avoir activé la fonctionnalité, réinitialisez les niveaux de kilométrage pour refléter correctement la valeur du champ **Quantité**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
