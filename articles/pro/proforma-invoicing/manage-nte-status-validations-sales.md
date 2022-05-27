---
title: Gérer le statut et les validations Ne pas dépasser
description: Cette rubrique fournit des informations sur les vérifications de limite à ne pas dépasser effectués dans Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3444d311386ae925617c9c9be657fe012f8f867b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576129"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gérer le statut et les validations Ne pas dépasser 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

## <a name="not-to-exceed-on-approvals"></a>« Ne pas dépasser » et approbations

Lorsqu’une entrée de temps, de dépense ou d’utilisation de matériel est soumise, un enregistrement d’approbation est créé. Si l’approbation est facturable et correspond à une ligne de contrat de temps et de matériel, le système effectue une vérification de validation Ne pas dépasser aux niveaux suivants :

  - Vérification par rapport à la limite définie pour le client sur la ligne du contrat de projet
  - Vérification par rapport à la limite définie sur la ligne du contrat
  - Vérification par rapport à la limite définie pour le client
  - Vérification par rapport à la limite définie sur le contrat

Les vérifications à chaque niveau consistent à s’assurer que le montant de la valeur des vente sur cette approbation ne violera pas la limite à ne pas dépasser à ce niveau après avoir comptabilisé le montant de la réplication de facturation déjà enregistré et le montant facturé à ce jour à ce niveau.

Si la vérification est un succès, l’approbation se voit attribuer un statut de validation de **Réussite**.

Si la vérification échoue, l’approbation se voit attribuer un statut de validation de **Échec**. Le détail de la validation Ne pas dépasser indiquera à l’utilisateur à quel niveau la validation a échoué.

Lorsque l’entrée de temps, de dépense ou d’utilisation de matériel soumise est considérée comme non facturable, le statut de validation Ne pas dépasser est défini sur **Non applicable** et le détail de validation est égal à **Non applicable**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>« Ne pas dépasser » et chiffres réels de vente non facturés

Lorsqu’une entrée de temps, de dépense ou d’utilisation de matériel est approuvée, des enregistrements de chiffres réels de coûts et de ventes non facturées sont créés. Si les chiffres réels de vente non facturables créés sont facturables et correspondent à une ligne de contrat de temps et de matériel, l’application effectue une vérification de validation Ne pas dépasser aux niveaux suivants :

  - Vérification par rapport à la limite définie pour le client de la ligne du contrat de projet
  - Vérification par rapport à la limite définie sur la ligne du contrat
  - Vérification par rapport à la limite définie pour le client
  - Vérification par rapport à la limite définie sur le contrat

Les vérifications à chaque niveau garantissent que le montant de la valeur des vente sur ce chiffre réel ne violera pas la limite à ne pas dépasser à ce niveau après avoir comptabilisé le montant de la réplication de facturation déjà enregistré et le montant facturé à ce jour à ce niveau.

Si la vérification est un succès, les chiffres réels de vente non facturés se voit attribuer le statut Ne pas dépasser de **Validé**.

Si la vérification échoue, les chiffres réels de vente non facturés se voit attribuer le statut Ne pas dépasser de **Échec**. Le détail de la validation indique à l’utilisateur à quel niveau la validation a échoué.

Lorsque les chiffres réels de vente non facturés sont considérées comme non facturables ou complémentaires, la limite à ne pas dépasser n’a pas été configurée à aucun des quatre niveaux, ou si le chiffre réel créé est un coût, une provision, une unité d’allocation des ressources ou les ventes inter-organisations, les champs **Statut Ne pas dépasser** et **Détails de la validation Ne pas dépasser** doivent être définis sur **Non applicable**.

## <a name="reset-the-not-to-exceed-status"></a>Rétablir le statut Ne pas dépasser

Vous pouvez effectuer une réinitialisation en bloc du statut Ne pas dépasser. Les chefs de projet peuvent ajuster la validation Ne pas dépasser pour donner la priorité à la facturation d’un ensemble de travaux, d’un temps, d’une dépense ou d’une utilisation de matériel en particulier par rapport à d’autres qui sont déjà validés à partir du montant disponible à ne pas dépasser.

Une fois que le statut Ne pas dépasser est réinitialisé sur les chiffres réels de vente non facturés, le montant engagé est réduit. Le chef de projet peut sélectionner une autre entrée d’ensemble de travaux, de temps, de dépense ou d’utilisation de matériel qui a précédemment échoué la validation Ne pas dépasser et procéder à une nouvelle évaluation. Avec la réduction du montant engagé, ces chiffres réels réussissent désormais la validation, ce qui permet au chef de projet d’exercer une plus grande influence et un meilleur contrôle sur les transactions facturables pour cette période.

Pour réinitialiser le statut Ne pas dépasser, sélectionnez un ou plusieurs chiffres réels dans la vue **Réplication de facturation pour le temps et le matériel** ou **Chiffres réels**, puis sélectionnez **Rétablir le statut Ne pas dépasser**.

Le statut Ne pas dépasser est réinitialisé sur **Non évalué** sur tous les chiffres réels sélectionnés pertinents. Les chiffres réels dont le statut Ne pas dépasser est réinitialisé sont des chiffres réels de vente non facturés qui n’ont pas déjà été facturés, qui ne figurent pas sur une facture en mode brouillon et qui sont marqués comme facturables. Tous les autres chiffres réels sélectionnés sont ignorés.

## <a name="reevaluate-not-to-exceed-status"></a>Réévaluer le statut Ne pas dépasser

Vous pouvez effectuer une réévaluation en bloc du statut Ne pas dépasser. La réévaluation du statut Ne pas dépasser est utile lorsque :

  - Une renégociation des limites à ne pas dépasser a eu lieu avec le client et les chiffres réels devront être réévalués.
  - Le chef de projet souhaite affiner la facturation de la réplication des ventes non facturées en privilégiant une partie du travail par rapport à une autre.

Pour réévaluer le statut Ne pas dépasser, sélectionnez un ou plusieurs chiffres réels dans la vue **Réplication de facturation pour le temps et le matériel** ou **Chiffres réels**, puis sélectionnez **Réévaluer le statut Ne pas dépasser**.

Tous les chiffres réels sélectionnés pertinents avec une limite à ne pas dépasser seront évalués par rapport à la limite à ne pas dépasser définie. Les chiffres réels pertinents pour une réévaluation du statut Ne pas dépasser sont des chiffres réels de vente non facturés qui ne sont pas facturés, ne figurent pas sur une facture en mode brouillon et sont marqués comme facturables. Tout autre chiffre réel sélectionné est sélectionné.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
