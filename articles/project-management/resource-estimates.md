---
title: Estimations basées sur la ressource
description: Cette rubrique fournit des informations sur le calcul des estimations des ressources dans Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127354"
---
# <a name="resource-estimates"></a>Estimations basées sur la ressource

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les estimations des ressources proviennent d’efforts échelonnés dans le temps qui sont définis dans la structure de répartition du travail avec les dimensions de tarification applicables. En règle générale, le calcul est **taux/h pour chaque rôle x heures.** L’effort échelonné pour chaque ressource est stocké dans l’enregistrement d’affectation de ressource. La tarification est stockée dans un tarif prédéfini. La conversion des unités est appliquée en fonction du tarif applicable.

![Estimations des ressources](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prix de revient et devise du prix de revient par défaut

Les prix de revient proviennent par défaut de l’unité d’organisation.

## <a name="default-bill-rate-and-sales-currency"></a>Taux de facturation et devise des ventes par défaut

Les prix de vente sont appliqués une fois par transaction. La hiérarchie des tarifs de vente par défaut est la suivante :

1. Organisation
2. Client
3. Devis/contrat
