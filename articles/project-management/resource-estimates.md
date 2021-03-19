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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286515"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]