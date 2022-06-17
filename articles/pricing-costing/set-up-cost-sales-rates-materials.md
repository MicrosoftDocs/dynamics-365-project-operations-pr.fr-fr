---
title: Configurer les taux de coûts et de vente pour le matériel
description: Cet article fournit des informations sur la configuration des taux de coût et de vente pour les matériaux utilisés sur les projets.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911777"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Configurer les taux de coûts et de vente pour le matériel

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez configurer les prix de revient et les prix de vente dans Dynamics 365 Project Operations. Les prix de revient et les prix de vente des produits ne peuvent être répertoriés que dans une seule devise, qui doit être la devise de l’en-tête du tarif.

Pour configurer les taux de coûts et de vente des produits, procédez comme suit. 

1. Accédez à **Ventes** > **Clients** > **Tarifs** et sélectionnez **Nouveau** pour créer un nouveau tarif. 
2. Sur **Éléments tarifaires**, dans le menu de la sous-grille, sélectionnez **Nouvel élément tarifaire**. 
3. Sur la page **Création rapide**, entrez le produit et l’unité pour lesquels vous créez le nouveau prix.

Pour plus d’informations sur la définition des prix des articles du catalogue, voir [Définir la tarification des produits avec des listes de prix et des éléments de liste de prix](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) et [Précision décimale dans la devise et les prix](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations ne prend pas en charge tous les modes de tarification pour les produits comme Dynamics 365 Sales. Le seul mode de tarification pris en charge pour les produits à utiliser sur des projets est *Montant en devise*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
