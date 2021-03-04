---
title: Gérer le statut et les validations Ne pas dépasser
description: Cette rubrique fournit des informations sur les vérifications de limite à ne pas dépasser effectués dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129990"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Gérer le statut et les validations Ne pas dépasser 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

## <a name="not-to-exceed-on-approvals"></a>« Ne pas dépasser » et approbations

Lorsqu’une entrée de temps ou de dépense est envoyée, un enregistrement d’approbation est créé. Si l’approbation est facturable et correspond à une ligne de contrat de temps et de matériel, le système effectue une vérification de validation Ne pas dépasser aux niveaux suivants :

  - Vérification par rapport à la limite définie pour le client sur la ligne du contrat de projet
  - Vérification par rapport à la limite définie sur la ligne du contrat
  - Vérification par rapport à la limite définie pour le client
  - Vérification par rapport à la limite définie sur le contrat

Les vérifications à chaque niveau consistent à s’assurer que le montant de la valeur des vente sur cette approbation ne violera pas la limite à ne pas dépasser à ce niveau après avoir comptabilisé le montant de la réplication de facturation déjà enregistré et le montant facturé à ce jour à ce niveau.

Si la vérification est un succès, l’approbation se voit attribuer un statut de validation de **Réussite**.

Si la vérification échoue, l’approbation se voit attribuer un statut de validation de **Échec**. Le détail de la validation Ne pas dépasser indiquera à l’utilisateur à quel niveau la validation a échoué.

Lorsque l’entrée de temps ou de dépense envoyée est considérée comme non facturable, le statut de validation Ne pas dépasser est défini sur **Non applicable** et le détail de la validation indique **Non applicable**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>« Ne pas dépasser » et chiffres réels de vente non facturés

Lorsqu’une entrée de temps ou de dépenses est approuvée, des enregistrements de coûts et de chiffres réels de vente non facturés sont créés. Si les chiffres réels de vente non facturables créés sont facturables et correspondent à une ligne de contrat de temps et de matériel, l’application effectue une vérification de validation Ne pas dépasser aux niveaux suivants :

  - Vérification par rapport à la limite définie pour le client de la ligne du contrat de projet
  - Vérification par rapport à la limite définie sur la ligne du contrat
  - Vérification par rapport à la limite définie pour le client
  - Vérification par rapport à la limite définie sur le contrat

Les vérifications à chaque niveau garantissent que le montant de la valeur des vente sur ce chiffre réel ne violera pas la limite à ne pas dépasser à ce niveau après avoir comptabilisé le montant de la réplication de facturation déjà enregistré et le montant facturé à ce jour à ce niveau.

Si la vérification est un succès, les chiffres réels de vente non facturés se voit attribuer le statut Ne pas dépasser de **Validé**.

Si la vérification échoue, les chiffres réels de vente non facturés se voit attribuer le statut Ne pas dépasser de **Échec**. Le détail de la validation indique à l’utilisateur à quel niveau la validation a échoué.

Lorsque les chiffres réels de vente non facturés sont considérées comme non facturables ou complémentaires, la limite à ne pas dépasser n’a pas été configurée à aucun des quatre niveaux, ou si le chiffre réel créé est un coût, une provision, une unité d’allocation des ressources ou les ventes inter-organisations, les champs **Statut Ne pas dépasser** et **Détails de la validation Ne pas dépasser** doivent être définis sur **Non applicable**.

## <a name="reset-the-not-to-exceed-status"></a>Rétablir le statut Ne pas dépasser

Vous pouvez effectuer une réinitialisation en bloc du statut Ne pas dépasser. Cela permet aux chefs de projet d’ajuster la validation Ne pas dépasser afin de hiérarchiser la facturation d’une partie donnée du travail, du temps ou des dépenses par rapport à d’autres qui sont déjà engagés à partir du montant disponible à ne pas dépasser.

Une fois que le statut Ne pas dépasser est réinitialisé sur les chiffres réels de vente non facturés, le montant engagé est réduit. Le chef de projet peut sélectionner une autre partie de travail, de temps ou des dépenses ayant échoué lors de la validation Ne pas dépasser précédente et les réévaluer. Grâce à la réduction du montant engagé, ces chiffres réels passeront désormais la validation avec succès. Cela permet au chef de projet d’exercer une plus grande influence et un meilleur contrôle sur les transactions facturables pour cette période.

Pour réinitialiser le statut Ne pas dépasser, sélectionnez un ou plusieurs chiffres réels dans la vue **Réplication de facturation pour le temps et le matériel** ou **Chiffres réels**, puis sélectionnez **Rétablir le statut Ne pas dépasser**.

Le statut Ne pas dépasser est réinitialisé sur **Non évalué** sur tous les chiffres réels sélectionnés pertinents. Les chiffres réels dont le statut Ne pas dépasser est réinitialisé sont des chiffres réels de vente non facturés qui n’ont pas déjà été facturés, qui ne figurent pas sur une facture en mode brouillon et qui sont marqués comme facturables. Tous les autres chiffres réels sélectionnés sont ignorés.

## <a name="reevaluate-not-to-exceed-status"></a>Réévaluer le statut Ne pas dépasser

Vous pouvez effectuer une réévaluation en bloc du statut Ne pas dépasser. La réévaluation du statut Ne pas dépasser est utile lorsque :

  - Une renégociation des limites à ne pas dépasser a eu lieu avec le client et les chiffres réels devront être réévalués.
  - Le chef de projet souhaite affiner la facturation de la réplication des ventes non facturées en privilégiant une partie du travail par rapport à une autre.

Pour réévaluer le statut Ne pas dépasser, sélectionnez un ou plusieurs chiffres réels dans la vue **Réplication de facturation pour le temps et le matériel** ou **Chiffres réels**, puis sélectionnez **Réévaluer le statut Ne pas dépasser**.

Tous les chiffres réels sélectionnés pertinents avec une limite à ne pas dépasser seront évalués par rapport à la limite à ne pas dépasser définie. Les chiffres réels pertinents pour une réévaluation du statut Ne pas dépasser sont des chiffres réels de vente non facturés qui ne sont pas facturés, ne figurent pas sur une facture en mode brouillon et sont marqués comme facturables. Tout autre chiffre réel sélectionné est sélectionné.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]