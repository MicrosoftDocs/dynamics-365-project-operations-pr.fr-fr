---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de vente des heures ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels des ventes des heures.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011638"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de vente des heures ?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cette FAQ s’applique aux chiffres réels où la classe de transaction est définie sur Heures et le type de transaction est Ventes non facturées. Les trois vérifications suivantes vous aideront à résoudre la définition de la valeur par défaut du prix (taux de facture) sur 0 sur les chiffres réels de vente des heures.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Vérification : 1 Identifier les tarifs de vente du projet

Rechercher le projet dans le champ de projet du chiffre réel et accédez à la page de projet. Accédez ensuite à l’onglet Ventes et dans la grille des lignes Contrat du projet, cliquez sur le lien dans le champ Contrat du projet. La page Contrat du projet s’ouvre. Dans la page Contrat du projet, accédez à l’onglet Tarifs du projet. Vérifiez qu’il existe au moins un tarif joint ici. Si aucun tarif n’est joint dans la grille Tarifs du projet du Contrat du projet, vous avez isolé le problème. Joignez un tarif à la grille Tarifs du projet. Les tarifs autorisés à être joints ici doivent avoir le champ de contexte défini sur Ventes et le champ Devise sur les tarifs doit correspondre au champ Devise dans le Contrat du projet. Une fois que vous avez terminé les corrections nécessaires, recréez l’entrée de l’heure, approuvez-la, et vérifiez que les chiffres réels des ventes non facturées affichent un prix valide. 

Si vous avec un ou plusieurs tarifs joints dans la grille Tarifs du projet du Contrat du projet, passez à la prochaine vérification de ce document.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Vérification 2 : L’un des tarifs identifiés ci-dessus sont-ils valides à la date spécifique du chiffre réel de vente des heures ?

Pour que Project Service prenne en compte un tarif pour le prix par défaut, ce tarif doit être applicable à la date du chiffre réel de vente des heures. Vérifiez les points suivants pour voir si les tarifs identifiés ci-dessus s’appliquent :
- Vérifiez si les dates de début et de fin sur l’onglet général des tarifs joints ne sont pas vides. Si les dates de début et de fin sur les tarifs identifiés ci-dessus sont vides, vous avez isolé le problème. 
- Prenez note du champ de date de début sur votre chiffre réel de vente des heures et vérifiez si l’un des tarifs identifiés s’applique à cette date. Par exemple, la date du chiffre réel de vente des heures doit se situer entre la date de début et la date de fin sur les tarifs. 
    - Si aucun tarif ne couvre cette date dans le chiffre réel de vente des heures, vous avez le isolé problème. Modifiez les dates de début et de fin des tarifs pour vous assurer que les tarifs couvrent la date du chiffre réel de vente des heures. 
    - Si plusieurs tarifs couvrent la date dans le chiffre réel de vente des heures, vous avez le isolé problème. Vous pouvez résoudre ce problème en modifiant les dates de début et de fin des tarifs afin qu’il ne reste qu’un seul tarif qui s’appliquent à la date du chiffre réel de vente des heures. 
    - S’il n’existe qu’un tarif qui s’appliquent à cette date du chiffre réel de vente des heures, passez à la Vérification 3.
Une fois que vous avez terminé les corrections nécessaires, recréez l’entrée de l’heure, approuvez-la, et vérifiez que les chiffres réels de vente des heures affichent un prix valide.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Vérification 3 : Existe-t-il un prix dans les tarifs pour les dimensions de tarification du chiffre réel de vente des heures ?

Si vous avez terminé la Vérification 1 et la Vérification 2, vous devez maintenant avoir un seul tarif qui s’applique à la date du chiffre réel de vente des heures. Ouvrez ce tarif et naviguez jusqu’à l’onglet Prix du rôle. Vérifiez qu’il existe une ligne dans la grille pour les dimensions de tarification sur le chiffre réel de vente des heures.

S’il n’y a aucune ligne dans la grille des prix de rôle pour les dimensions de tarification dans le chiffre réel de vente des heures, cela signifie que vous avez isolé le problème. Créez une ligne dans la grille Prix du rôle pour les dimensions de tarification dans votre chiffre réel de vente des heures. Une fois cette opération terminée, recréez l’entrée de l’heure, approuvez-la, et vérifiez que les chiffres réels de vente des heures affichent un prix valide.

Si vous ne voyez toujours pas de prix valide sur votre chiffre réel de vente des heures après avoir effectué les trois vérifications ci-dessus, entrez un ticket du support technique. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]