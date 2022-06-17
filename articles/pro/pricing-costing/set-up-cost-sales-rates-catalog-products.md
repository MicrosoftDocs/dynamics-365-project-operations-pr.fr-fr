---
title: Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié
description: Cet article fournit des informations sur la configuration des taux de coût et de vente pour les articles d’un catalogue de produits.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917389"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


La configuration de la tarification des articles du catalogue de produits dans Dynamics 365 Project Operations est la même que dans Dynamics 365 Sales.

Dans Project Operations, les produits ne peuvent pas être estimés ou utilisés sur des projets, de sorte que les prix du catalogue de produits n’ont pas besoin d’être définis sur les tarifs de projet pour les devis et les contrats.

Utilisez le champ **Prix du produit** d’un devis, d’un contrat ou d’un compte pour configurer les prix du catalogue de produits. Ne configurez pas les prix du catalogue de produits dans les tarifs du projet. Les tarifs de projet sont exclusifs à Project Operations. La logique métier spécifique à l’application copie les tarifs d’un devis vers un contrat. Il en résulte un tarif spécifique au contrat. L’opération de copie peut retarder le processus d’obtention d’un devis si le tarif du projet sur le devis devient trop volumineux. Les tarifs des produits ne sont pas copiés pour créer des tarifs personnalisés sur les contrats. Comme aucune copie n’est impliquée, les performances du processus de devis ne sont pas affectées.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]