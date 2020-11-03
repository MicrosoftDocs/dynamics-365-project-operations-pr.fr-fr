---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des heures ?
description: Résolution de pourquoi un pris prend la valeur par défaut de 0 sur les chiffres réels de coût des heures.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075759"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de coût des heures ?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cette FAQ s'applique aux chiffres réels où la classe de transaction est définie sur Heures et le type de transaction est Coût. Les trois vérifications suivantes vous aideront à résoudre la définition de la valeur par défaut du prix sur 0 sur les chiffres réels de coût des heures.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Vérification 1 : Identifier les prix de revient du projet

Rechercher le projet dans le champ de projet du chiffre réel puis accédez à la page de projet. Cliquez sur le lien de l'unité contractuelle dans le champ. Dans la page Unité contractuelle, vérifiez si l'unité contractuelle possède un tarif dans la grille des prix de revient.

S'il existe plusieurs tarifs, vous avez isolé le problème. Project Service prend en charge un seul tarif par unité d'organisation. Supprimez tous les tarifs de cette entité jusqu'à ce qu'il n'en reste qu'un joint dans la grille des Prix de revient de l'unité d'organisation.

En l'absence de tarifs joints à l'unité d'organisation, prenez note de la devise de l'unité d'organisation. Accédez à Project Service puis à Paramètres et ouvrez l'onglet Tarifs. Vérifiez s'il existe des tarifs avec le contexte défini sur Coût et une devise correspondant à la devise de l'unité d'organisation.
 
Si aucun tarif ne correspond à ces critères, vous avez isolé le problème. Veillez à disposer d'au moins un tarif dont le contexte est défini sur Coût et dont la devise correspond à la devise de l'unité d'organisation.

Si plusieurs tarifs correspondent à ces critères, continuez de lire ce document pour effectuer d'autres contrôles.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Vérification 2 : L'un des tarifs identifiés ci-dessus sont-ils valides à la date spécifique du chiffre réel du coût des heures ?

Pour que Project Service prenne en compte un tarif pour le prix par défaut, ce tarif doit être applicable à la date du chiffre réel coût des heures. Vérifiez les points suivants pour voir si les tarifs identifiés ci-dessus s'appliquent :

- Vérifiez si les dates de début et de fin sur l'onglet général des tarifs joints ne sont pas vides. Si les dates de début et de fin sur les tarifs identifiés ci-dessus sont vides, vous avez isolé le problème. 
- Prenez note du champ de date de début sur votre chiffre réel de coût des heures et vérifiez si l'un des tarifs identifiés s'applique à cette date. Par exemple, la date du chiffre réel du coût des heures doit se situer entre la date de début et la date de fin sur les tarifs. 
    - Si aucun tarif ne couvre cette date dans le chiffre réel du coût des heures, vous avez le isolé problème. Modifiez les dates de début et de fin des tarifs pour vous assurer que les tarifs couvrent la date du chiffre réel du coût des heures. 
    - Si plusieurs tarifs couvrent la date dans le chiffre réel du coût des heures, vous avez le isolé problème. Vous pouvez résoudre ce problème en modifiant les dates de début et de fin des tarifs afin qu'il ne reste qu'un seul tarif qui s'appliquent à la date du chiffre réel du coût des heures. 
    - S'il n'existe qu'un tarif qui s'applique à cette date du chiffre réel du coût des heures, passez à la vérification suivante dans ce document.
Une fois que vous avez terminé les corrections nécessaires, recréez l'entrée de l'heure, approuvez- la, et vérifiez que les chiffres réels du coût des heures affichent un prix valide.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Vérification 3 : Existe-t-il un prix dans les tarifs pour les dimensions de tarification du chiffre réel du coût des heures ?

Si vous avez terminé la Vérification 1 et la Vérification 2, vous devez maintenant avoir un seul tarif qui s'applique à la date du chiffre réel du coût des heures. Ouvrez ce tarif et accédez l'onglet Prix du rôle. Vérifiez qu'il existe une ligne dans la grille pour les dimensions de tarification sur le chiffre réel du coût des heures.

S'il n'y a aucune ligne dans la grille des prix de rôle pour les dimensions de tarification dans le chiffre réel du coût des heures, cela signifie que vous avez isolé le problème. Créez une ligne dans la grille Prix du rôle pour les dimensions de tarification dans votre chiffre réel du coût des heures. Une fois cette opération terminée, recréez l'entrée de l'heure, approuvez-la, et vérifiez que les chiffres réels du coût des heures affichent un prix valide.
 
Si vous ne voyez toujours pas de prix valide sur votre chiffre réel du coût des heures après avoir terminé les trois vérifications ci-dessus, entrez un ticket du support technique.



