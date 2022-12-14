---
title: Configurer la conversion de devises pour calculer les prix de vente à partir des taux de coût
description: Cet article explique comment configurer le comportement de conversion de devise utilisé dans Microsoft Dynamics 365 Project Operations lorsque des transactions de vente sont générées à partir de transactions de coût.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816665"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configurer la conversion de devises pour calculer les prix de vente à partir des taux de coût

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Dans Microsoft Dynamics 365 Project Operations, les prix de vente des catégories de dépenses peuvent être configurés en tant que valeurs numériques, ou ils peuvent être configurés de manière à être calculés en fonction du coût encouru.

Lorsqu’ils sont configurés pour être calculés en fonction du coût engagé, les options suivantes sont disponibles :

- À prix coûtant
- Pourcentage de majoration par rapport au coût

Dans les scénarios où le coût des dépenses est engagé dans une devise différente de la devise de vente du contrat de projet, la conversion de devise est nécessaire pour calculer le prix de vente en fonction du coût.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportement de conversion de devise qui utilise les taux de change Dataverse natifs

Par défaut, Project Operations utilise les taux de change stockés dans la table Devise dans Dataverse. Pour configurer Project Operations afin d’utiliser les taux de change natifs pour calculer les prix de vente à partir du coût, procédez comme suit.

1. Accédez à **Project Operations \> Réglages \> Paramètres**.
1. Ouvrez la page de détails **Paramètres du projet** .
1. Définissez le champ **Logique de conversion monétaire** sur une valeur vierge.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportement de conversion monétaire qui utilise les taux de change des applications de finances et d’opérations

Les taux de change dans la table Devise qui est nativement disponible dans Dataverse n’ont pas de date d’effet. Par conséquent, ils peuvent ne pas toujours être mis à l’échelle en fonction des exigences que vous avez pour le calcul des prix de vente à partir des taux de coût.

Vous pouvez utiliser les taux de change de l’environnement de finances et d’opérations pour calculer le prix de vente dans la devise de vente à partir d’un taux de coût dans la devise de coût. Pour configurer ce comportement de conversion monétaire, procédez comme suit.

1. Sur la page **Paramètres du projet**, ajoutez le champ **Logique de conversion monétaire**. Puis enregistrez et publiez la personnalisation.
1. Accédez à **Project Operations \> Réglages \> Paramètres**.
1. Ouvrez la page de détails **Paramètres du projet** . 
1. Définissez le champ **Comportement de conversion monétaire** sur **Étendu avec retour vers la valeur par défaut**.
1. Donnez au rôle de sécurité **Utilisateur d’application à double écriture** l’autorisation **Lecture globale** pour les tables suivantes :

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Dans votre environnement de finances et d’opérations, exécutez les mappages en double écriture suivants avec la synchronisation initiale :

    - Type de taux de change (msdyn\_exchangeratetypes)
    - Taux de change entre les deux devises (msdyn\_currencyexchangeratepairs)
    - Taux de change CDS (msdyn\_currencyexchangerates)

Une fois ces changements terminés, la double écriture rend les taux de change de l’environnement de finances et d’opérations disponibles dans Dataverse. Project Operations utilise ensuite ces taux de change pour convertir les taux de coût dans la devise de vente du contrat.

> [!NOTE]
> Ce comportement de conversion monétaire s’applique uniquement au calcul des prix de vente à partir des taux de coût. Il n’est pas utilisé pour calculer de manière générique les valeurs de la devise de base. Les valeurs de la devise de base utilisent toujours les taux de change Dataverse natifs, que vous suiviez ou non cette procédure.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
