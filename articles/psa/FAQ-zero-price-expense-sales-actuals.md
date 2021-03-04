---
title: Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de vente de la dépense ?
description: Les trois vérifications suivantes vous aideront à résoudre la définition de la valeur par défaut du prix sur 0 sur les chiffres réels de vente de la dépense.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146300"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Pourquoi le tarif prend la valeur par défaut de zéro sur les chiffres réels de vente de la dépense ?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cette FAQ s’applique aux chiffres réels des dépenses où la classe de transaction est définie sur Dépenses et le type de transaction est Ventes non facturées. Les trois vérifications suivantes vous aideront à résoudre la définition de la valeur par défaut du prix (taux de facture) sur 0 sur les chiffres réels de vente de la dépense.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Vérification : 1 Identifier les tarifs de vente pour le projet

Rechercher le projet dans le champ de projet du chiffre réel et accédez à la page de projet. Accédez ensuite à l’onglet Ventes. Dans la grille des lignes Contrat du projet, cliquez sur le lien dans le champ Contrat du projet. La page Contrat du projet s’ouvre. Dans la page Contrat du projet, accédez à l’onglet Tarifs du projet. Vérifiez qu’il existe au moins un tarif joint ici.

Si aucun tarif n’est joint dans la grille Tarifs du projet du Contrat du projet :

- Joignez un tarif à la grille Tarifs du projet. Les tarifs autorisés à être joints ici doivent avoir le champ de contexte défini sur Ventes et le champ Devise sur les tarifs doit correspondre au champ Devise dans le Contrat du projet. Une fois que vous avez fait les corrections nécessaires, recréez l’entrée de dépenses, approuvez- la, et vérifiez que les chiffres réels des ventes non facturées affichent un prix valide.
- Si vous avec un ou plusieurs tarifs joints dans la grille Tarifs du projet du Contrat du projet, allez vérifier le point 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Vérification 2 : L’un des tarifs identifiés ci-dessus sont-ils valides à la date spécifique du chiffre réel des dépenses ?

Pour que Project Service prenne en compte un tarif pour le prix par défaut, ce tarif doit être applicable à la date du chiffre réel des ventes de dépenses. Vérifiez les points suivants pour voir si les tarifs identifiés ci-dessus s’appliquent :

- Commencez par vérifier si les dates de début et de fin sur l’onglet général des tarifs joints ne sont pas vides. Si les dates de début et de fin sur les tarifs identifiés ci-dessus sont vides, vous avez isolé le problème. 
- Prenez note du champ de date de début sur votre chiffre réel de ventes de dépenses et vérifiez si l’un des tarifs identifiés s’applique à cette date. Par exemple, la date du chiffre réel des dépenses doit se situer entre la date de début et la date de fin sur les tarifs. 
    - Si aucun tarif ne couvre cette date dans le chiffre réel des ventes de dépenses, vous avez le isolé problème. Modifiez les dates de début et de fin des tarifs pour vous assurer que les tarifs couvrent la date du chiffre réel des dépenses. 
    - Si plusieurs tarifs couvrent la date dans le chiffre réel des ventes de dépenses, vous avez le isolé problème. Modifiez les dates de début et de fin des tarifs afin qu’il ne reste qu’un seul tarif qui s’appliquent à la date du chiffre réel des dépenses. 
    - S’il n’existe qu’un tarif qui s’appliquent à cette date du chiffre réel des dépenses, passez à la Vérification 3.
Une fois que vous avez terminé les corrections nécessaires, recréez l’entrée de dépenses, approuvez- la, et vérifiez que les chiffres réels des ventes non facturées affichent un prix valide.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Vérification 3 : Existe -t-il un prix valide pour la catégorie de dépenses dans le tarif du projet applicable ? 

Si vous avez terminé la Vérification 1 et la Vérification 2, vous devez maintenant avoir un seul tarif de projet qui s’applique à la date du chiffre réel de la vente des dépenses. Ouvrez ce tarif du projet et accédez l’onglet Prix de la catégorie. Vérifiez qu’il existe une ligne dans la grille pour la catégorie de dépenses spécifique sur le chiffre réel des dépenses.
 
- S’il n’y a aucune ligne, vous avez isolé le problème. Créez une ligne dans la grille Prix de la catégorie pour la catégorie sur votre chiffre réel des dépenses. Ensuite, recréez l’entrée de dépenses, approuvez- la, et vérifiez que les chiffres réels des ventes non facturées affichent un prix valide. 
- S’il existe une ligne correspondant à la catégorie de dépenses dans la grille des prix de la catégorie, vérifiez si elle a un prix valide.

Pour comprendre ce qu’est un prix valide, utilisez ces méthodes suivantes :

- Si le champ Mode de tarification dans la ligne Prix de la catégorie est défini sur À prix coûtant, le taux unitaire sur votre chiffre réel des ventes des dépenses est défini par défaut sur la valeur dans l’entrée Dépenses.
- Si le champ Mode de tarification dans la ligne Prix de la catégorie est défini sur Pourcentage de la majoration, alors vérifiez si le champ Pourcentage est défini sur une valeur valide. Le taux unitaire sur votre chiffre réel de ventes de dépenses est défini par défaut en appliquant ce pourcentage de majoration au tarif dans l’entrée Dépenses.
- Si le champ Mode de tarification dans la ligne Prix de la catégorie est défini sur Prix unitaire, alors vérifiez si le champ Prix est défini sur une valeur valide. Le taux unitaire et votre chiffre réel de ventes de dépenses est défini par défaut sur le montant en devise spécifié dans le champ Prix.

Si la configuration du prix pour la catégorie de dépenses n’est pas valide, vous avez isolé le problème. La solution consiste à modifier la ligne du prix de la catégorie avec un prix valide de la catégorie de dépenses conformément aux règles ci-dessus. Une fois cette opération terminée, recréez l’entrée de dépenses, approuvez- la, puis vérifiez que les chiffres réels des ventes non facturées obtient un prix valide.

Si vous ne voyez toujours pas de prix valide sur votre chiffre réel des ventes de dépenses après avoir effectué les trois vérifications ci-dessus, entrez un ticket du support technique.


