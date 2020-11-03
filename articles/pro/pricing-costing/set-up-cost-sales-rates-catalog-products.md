---
title: Configurer les taux de coûts et de vente pour les produits du catalogue
description: Cette rubrique fournit des informations sur la configuration des taux de coûts et de vente pour les articles d'un catalogue de produits.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075807"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Configurer les taux de coûts et de vente pour les produits du catalogue

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


La configuration de la tarification des éléments d'un catalogue de produits dans Dynamics 365 Project Operations est la même que dans Dynamics 365 Sales.

Étant donné que les produits ne peuvent pas être estimés ou utilisés sur des projets dans Project Operations, il n'est pas nécessaire de configurer les prix du catalogue de produits sur les tarifs de projet pour les devis et les contrats.

Les prix du catalogue de produits doivent être configurés dans le champ **Prix du produit** d'un devis, d'un contrat ou d'un compte. Ne configurez pas les prix du catalogue de produits dans les tarifs du projet pour ces entités. Les tarifs de projet sont exclusifs à Project Operations. Il existe une logique métier spécifique à l'application qui copie les tarifs d'un devis vers un contrat. Il en résulte un tarif spécifique au contrat. L'opération de copie peut retarder le processus d'obtention d'un devis si le tarif du projet sur le devis devient trop volumineux. Les tarifs des produits ne sont pas copiés pour créer des tarifs personnalisés sur les contrats. Cela signifie que les tarifs des produits n'ont pas d'impact sur les performances du processus d'obtention d'un devis.
