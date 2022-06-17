---
title: Vue d’ensemble de la rétention de fournisseurs
description: Cet article offre une vue d’ensemble des capacités de rétention de fournisseurs.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916837"
---
# <a name="vendor-retention-overview"></a>Vue d’ensemble de la rétention de fournisseurs

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Votre organisation peut souhaiter conserver une partie des paiements aux fournisseurs qui travaillent sur des projets pour votre organisation. Par exemple, avant de payer un fournisseur, vous souhaitez peut-être vous assurer de la qualité des articles et services fournis.

Lorsque vous négociez des achats pour des projets avec des fournisseurs, vous pouvez spécifier les conditions de rétention de fournisseurs qui incluent le pourcentage ou le montant à retenir. Au fur et à mesure que le fournisseur livre des articles et des services, vous déduisez le pourcentage ou le montant de rétention spécifié du paiement à ce fournisseur. Une fois le projet terminé ou s’il atteint une étape intermédiaire spécifiée dans le contrat, vous libérez le montant retenu et créez un paiement au fournisseur.

## <a name="vendor-retention-example"></a>Exemple de rétention de fournisseurs

L’exemple suivant montre comment un pourcentage du montant d’une facture fournisseur est conservé en fonction du pourcentage d’achèvement d’un projet.

Contoso Robotics USA a passé un contrat avec le fournisseur Fabrikam pour dispenser 100 heures de formation pour le projet de renouvellement des équipements. La valeur totale du contrat est de 30 000 USD, avec un prix d’achat convenu de 300 USD par heure.

La formation se déroulera en trois phases selon le calendrier suivant :

- Phase 1 : 50 heures, soit 50 % du projet
- Phase 2 : 30 heures, soit 80 % du total du projet
- Phase 3 : 20 heures, soit 100 % du projet

Le tableau suivant répertorie les conditions de rétention.

| **Pourcentage d’unités livrées** | **Pourcentage à retenir** | **Pourcentage à libérer** |
| --- | --- | --- |
| 50 %% | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Les transactions donnent les montants suivants :

- Phase 1 :
  - Le montant à payer est de 50 x 300, soit 15 000.
  - 20 % du montant, soit 3 000, sont retenus et seront libérés à un stade ultérieur.
  - Le montant payé au fournisseur s’élève à 12 000.
- Phase 2 :
  - Le montant à payer est de 30 x 300, soit 9 000.
  - 10 % du montant, soit 900, est retenu.
  - 10 % des 3 000 retenus en phase 1, soit 300, sont libérés.
  - Le montant payé au fournisseur s’élève à 8 400. Ce montant est de 9 000, moins la rétention de 900, plus les 300 libérés de la rétention en phase 1.
- Phase 3 :
  - Le montant à payer est de 20 x 300, soit 6 000.
  - Aucun montant n’est retenu.
  - Le montant libéré est de 3 600. Ce montant se compose des 3 000 retenus en phase 1, moins les 300 de la phase 1 libérés en phase 2, plus les 900 retenus en phase 2.
  - Le montant payé au fournisseur s’élève à 9 600. Ce montant se compose du montant retenu de 3 600, plus les 6 000 pour l’achèvement de la phase 3.

Le montant total payé au vendeur une fois les trois phases terminées est de 30 000, ce qui correspond au montant total du bon de commande (15 000 + 9 000 + 6 000).
