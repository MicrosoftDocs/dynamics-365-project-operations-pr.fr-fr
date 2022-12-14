---
title: Gestion des unités complexes telles que par utilisateur, par mois pour les lignes de devis selon les produits
description: Cet article fournit des informations sur la gestion d’unités complexes pour les lignes de devis basées sur un produit.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50151e9a34e8608c98e406a30131c1efc4bf2f11
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825468"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Gestion des unités complexes telles que par utilisateur, par mois pour les lignes de devis selon les produits

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations utilise des facteurs de quantité pour prendre en charge la vente de produits basés sur un abonnement. Pour les produits basés sur abonnement, la quantité sur le devis ou la ligne de contrat du projet est exprimée sous la forme du nombre de mois d’utilisateur.

En règle générale, le prix des logiciels sur abonnement est stocké dans le catalogue comme prix par utilisateur par mois. Durant le processus de vente, le prix sur la ligne de devis est généralement le prix par utilisateur, par mois, négocié et avec remise, par l’agent de vente informatique. Chaque transaction a un nombre différent d’utilisateurs et un nombre différent de mois d’abonnement. La quantité utilisée pour calculer la ligne de devis est un produit du nombre d’utilisateurs et du nombre de mois d’abonnement.

Pour prendre en charge ce type de vente, Project Operations a présenté le concept de facteurs de quantité. Les facteurs de quantité reposent sur les attributs du produit dans Dynamics 365. Lorsque vous configurez des propriétés spécifiques pour un produit, Project Operations vous permet de marquer un sous-ensemble ou toutes les propriétés, comme des facteurs de la quantité.

Project Operations valide que seules les propriétés numériques ou les propriétés de produit ayant un type de données numérique sont marquées comme facteurs de la quantité. Lorsque vous ajoutez un produit avec des facteurs de quantité à une ligne de devis, le champ **Quantité** devient en lecture seule. Après avoir entré des valeurs pour les propriétés du produit qui sont des facteurs de quantité, Project Operations calcule la quantité de la ligne de devis.

Par exemple, Dynamics 365 Sales peut contenir les propriétés suivantes :

- **Nombre d’utilisateurs** : Le nombre d’utilisateurs
- **Nombre de mois** : Le nombre de mois d’abonnement
- **SKU produit**

Vous pouvez marquer les propriétés **Nombre d’utilisateurs** et **Nombre de mois** comme facteurs de quantité en modifiant les propriétés de la ligne de produit.

Pour créer des facteurs de quantité à partir des propriétés du produit, procédez comme suit :

1. Dans le volet de navigation de gauche Project Operations, accédez à **Ventes** > **Produits**.
2. Ouvrez le produit pour lequel vous devez configurer des facteurs de quantité. Assurez-vous que le produit possède des propriétés déjà configurées.
3. Sur la page **Renseignements sur le projet** pour le produit, sélectionnez l’onglet **Facteurs de quantité**.
4. Dans la sous-grille, sélectionnez **+ Nouveau calcul de champ**.
5. Entrez le nom du facteur Quantité et sélectionnez la valeur de propriété qui correspond au calcul du champ.
6. Enregistrer et fermer le formulaire. Répétez ces étapes pour toutes les propriétés à utiliser pour calculer la quantité pour la ligne de devis basée sur le produit.

Lorsque vous créez une ligne de devis basée sur un produit pour un produit, la quantité de la ligne de devis est verrouillée. La quantité sera calculée comme un produit des valeurs de propriété que vous saisissez pour cette ligne de devis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
