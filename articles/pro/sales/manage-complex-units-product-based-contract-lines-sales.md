---
title: Gérer des unités complexes pour les lignes de contrat basées sur les produits – Simplifié
description: Cet article fournit des informations sur la prise en charge de la vente de produits par abonnement.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f48ac31778e34ace79dbce74cff752343484e5a5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919919"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Gérer des unités complexes pour les lignes de contrat basées sur les produits – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations utilise des facteurs de quantité pour prendre en charge la vente de produits basés sur un abonnement. Pour les produits basés sur abonnement, la quantité sur le contrat ou la ligne de contrat du projet est exprimée sous la forme du nombre de mois d’utilisateur.

Le prix des logiciels sur abonnement est stocké dans le catalogue comme prix par utilisateur et par mois. Durant le processus de vente, le prix sur la ligne de contrat est généralement le prix par utilisateur, par mois, négocié et avec remise, par l’agent de vente. Chaque transaction a un nombre différent d’utilisateurs et un nombre différent de mois d’abonnement. La quantité utilisée pour calculer le montant de la ligne de contrat est un produit du nombre d’utilisateurs et du nombre de mois d’abonnement.

Pour prendre en charge ce type de vente, Project Operation prend en charge le concept de *facteurs de quantité*. Les facteurs de quantité reposent sur les attributs du produit. Lorsque vous configurez des propriétés spécifiques pour un produit, vous pouvez marquer un sous-ensemble de ces propriétés, ou toutes les propriétés, comme des facteurs de la quantité.

Project Operations valide que seules les propriétés numériques ou les propriétés de produit ayant un type de données numérique sont marquées comme facteurs de la quantité. Lorsqu’un produit avec des facteurs de quantité configurés est ajouté à une ligne de contrat, le champ **Quantité** passe en lecture seule. Après avoir saisi des valeurs pour les propriétés du produit qui sont des facteurs de quantité, Project Operations calcule la quantité de la ligne de contrat.

Par exemple, Dynamics 365 Sales peut contenir les propriétés suivantes :

- **Nombre d’utilisateurs** : le nombre d’utilisateurs.
- **Nombre de mois** : le nombre de mois d’abonnement.
- **SKU du produit** : l’unité de gestion des stocks (SKU) du produit.

Les propriétés **Nombre d’utilisateurs** et **Nombre de mois** peuvent être marquées comme facteurs de quantité en modifiant les propriétés de la ligne de produit.

Pour créer des facteurs de quantité à partir des propriétés du produit, procédez comme suit.

1. Sur **Project Operations**, sélectionnez **Ventes-Produits**.
2. Ouvrez le produit pour lequel vous devez configurer des facteurs de quantité. Assurez-vous que le produit possède des propriétés déjà configurées.
3. Sur la page **Informations sur le projet**, sélectionnez l’onglet **Facteurs de quantité**.
4. Dans la sous-grille, sélectionnez **+ Nouveau calcul de champ**.
5. Entrez le nom du facteur **Facteur de quantité** et sélectionnez la valeur de propriété qui correspond au calcul du champ.
6. Enregistrer et fermer le formulaire.
7. Répétez les étapes 2 à 6 pour toutes les propriétés qui, ensemble, constitueront la quantité de la ligne de contrat basée sur les produits.

Avec la configuration des facteurs de quantité, lorsque l’utilisateur crée une ligne de contrat pour ce produit, la quantité de la ligne de contrat est verrouillée. La quantité est ensuite calculée comme un produit des valeurs de propriété pour cette ligne de contrat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]