---
title: Produits
description: Cette rubrique fournit des informations sur le catalogue de produits que vous pouvez utiliser pour fournir des informations aux clients sur les produits et les prix proposés par votre organisation.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121260"
---
# <a name="products"></a>Produits

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les produits sont la colonne vertébrale de votre entreprise. Le catalogue de produits dans Dynamics 365 Sales Professional est un ensemble de produits avec des informations de tarification. Aidez vos agents des ventes à augmenter leurs ventes en créant un catalogue de produits rapidement.

## <a name="add-a-product"></a>Ajouter un produit

1.  Assurez-vous de disposer du rôle de gestionnaire de Sales Professional ou d’Administrateur système pour pouvoir ajouter des produits à Dynamics 365 Sales Professional.
2.  Sur le plan de site, sous **Configuration**, sélectionnez **Produits**.
3.  Sélectionnez **Ajouter un produit** et renseignez les informations suivantes :

    -  **Nom**
    -  **ID produit**
    -  **Parent** : Sélectionnez une famille de produits parente pour le produit. Si vous créez un produit enfant dans une famille de produits, le nom de la famille de produits parente est renseignée ici. Elle ne peut pas être modifiée une fois l’enregistrement validé.
    -  **Valide à partir du**/**Valide jusqu’au** : Définissez la période pendant laquelle le produit est valide en sélectionnant une date **Valide à partir du** et **Valide jusqu’au**.
    -  **Groupe d’unités** : sélectionnez un groupe d’unités. Un groupe d’unités est un ensemble d’unités diverses dans lesquelles un produit est vendu. Il définit comment des éléments individuels sont regroupés en de plus grandes quantités. Par exemple, si vous ajoutez des graines en tant que produit, vous pouvez avoir créé un groupe d’unités appelé « Graines » et défini son unité principale en tant que « paquet ».
    -  **Unité par défaut** : sélectionnez l’unité dans laquelle le produit est le plus souvent vendu. Les unités sont les quantités ou les unités de mesure dans lesquelles vous vendez vos produits. Par exemple, si vous ajoutez des graines en tant que produit, vous pouvez les vendre par paquets, boîtes ou palettes. Chacun de ces éléments devient une unité du produit. Si les graines sont principalement vendues en paquets, sélectionnez cette unité.
    -  **Tarifs par défaut** : S’il s’agit d’un nouveau produit, les données de ce champ sont accessibles en lecture seule. Avant de pouvoir sélectionner un tarif par défaut, vous devez compléter les champs obligatoires, puis enregistrer l’enregistrement. Bien que le tarif par défaut ne soit pas nécessaire, après avoir enregistré le produit, il est bon de définir un tarif par défaut pour chaque produit. Ainsi, si un enregistrement de client ne contient pas de tarif, Sales peut utiliser celui par défaut pour générer des devis, des commandes et des factures.
    -  **Décimales prises en charge** : Entrez un nombre entier compris entre 0 et 5. Si le produit ne peut pas être fractionné, entrez 0. La précision du champ **Quantité** dans l’enregistrement produit du devis, de la commande ou de la facture est validée par rapport à la valeur dans ce champ si le produit ne comprend pas de tarif associé.
    -  **Objet** : Associer ce produit à un sujet. Vous pouvez utiliser des sujets pour classer vos produits et appliquer des filtres sur les rapports.

4.  Sélectionnez **Enregistrer**.
5.  Dans l’onglet **Détails supplémentaires**, dans la section **Éléments tarifaires**, sélectionnez **Plus de commandes**, puis sélectionnez **Ajouter un nouvel élément tarifaire**.
7.  Dans l’onglet **Détails supplémentaires**, dans la section **Relation de produit**, sélectionnez l’icône **Plus de commandes**, puis sélectionnez **Ajouter une nouvelle la relation de produit.**
8.  Dans le formulaire **Nouvelle relation de produit**, entrez les détails suivants, et dans la barre de commandes, sélectionnez **Enregistrer et fermer** :

    -   **Produit lié** : Sélectionnez un produit à ajouter en tant que produit associé à l’enregistrement de produit existant sur lequel vous travaillez.
    -   **Type de relation des ventes** : Indiquez si vous souhaitez ajouter le produit en tant que produit de vente incitative, vente croisée, substitut ou accessoire.
    -   **Direction** : Indiquez si les relations entre les produits sont unidirectionnelles ou bidirectionnelles. Lorsque vous sélectionnez Unidirectionnel, le produit que vous sélectionnez dans **Produit lié** sera indiqué comme recommandation pour le produit existant, mais pas inversement.

9.  Dans le formulaire Produit, sélectionnez **Enregistrer**.

## <a name="import-products"></a>Importer des produits

Vous pouvez utiliser des modèles pour transférer des données de produit en bloc dans Dynamics 365 Sales.

## <a name="revise-a-product"></a>Réviser un produit

Conservez l’inventaire de produits à jour en révisant rapidement les propriétés des produits en fonction des besoins et en republiant les informations de sorte que vos agents de vente puissent voir les dernières modifications apportées à l’inventaire.

1.  Assurez-vous de disposer de l’un des rôles de sécurité suivants ou des autorisations équivalentes : Administrateur système, Personnalisateur de système, Directeur commercial, Directeur de division, Vice-président du marketing ou Directeur général/Dirigeant d’entreprise.
2.  Sur le plan de site, sélectionnez **Produits**.
3.  Ouvrez un produit actif à modifier, puis, dans la barre de commandes, sélectionnez **Réviser**.
4.  Dans la boîte de dialogue **Confirmer la révision**, sélectionnez **Confirmer**. Le statut du produit devient **En cours de révision**.
5.  Une fois que vous avez terminé les modifications, dans la barre de commandes, sélectionnez **Publier**.

    > [!TIP]
    > Pour annuler les modifications et continuer avec la dernière version active du produit, sélectionnez **Rétablir**. Cette opération rétablit le statut du produit sur **Actif**.

## <a name="clone-a-product"></a>Clonage d’un produit 

Lorsque vous créez un produit, gagnez du temps en clonant un élément existant. Vous créez ainsi une copie de l’enregistrement d’origine avec tous les détails à l’exception du nom et de l’ID.

1.  Assurez-vous de disposer de l’un des rôles de sécurité suivants ou des autorisations équivalentes : Administrateur système, Personnalisateur de système, Directeur commercial, Directeur de division, Vice-président du marketing ou Directeur général/Dirigeant d’entreprise.
2.  Sur le plan de site, sélectionnez **Produits**.
3.  Sélectionnez un enregistrement de produit à cloner, puis, dans la barre de commandes, sélectionnez **Cloner**. Une boîte de dialogue de confirmation s’affiche.
4.  Cliquez sur **Confirmer**.

Un nouvel enregistrement de produit s’ouvre, avec les mêmes informations que celui d’origine, à l’exception du nom et de l’ID.

## <a name="retire-a-product"></a>Mettre un produit hors service 

Si votre organisation ne vend plus un produit, mettez-le hors service afin qu’il ne soit plus disponible à vos agents de vente.

1.  Assurez-vous de disposer du rôle d’Administrateur système ou de gestionnaire de Sales Professional ou d’autorisations équivalentes.
2.  Sur le plan de site, sélectionnez **Produits**.
3.  Ouvrez un produit actif à mettre hors service, puis, dans la barre de commandes, sélectionnez **Mettre hors service**.
4.  Dans la boîte de dialogue **Confirmer la mise hors service**, sélectionnez **Confirmer**.


## <a name="delete-a-product"></a>Supprimer un produit

Pour arrêter de vendre un produit, supprimez-le.

> [!IMPORTANT]
> Vous ne pouvez pas restaurer un enregistrement supprimé.

1.  Assurez-vous de disposer du rôle d’Administrateur système ou de gestionnaire de Sales Professional ou d’autorisations équivalentes.
2.  Sur le plan de site, sélectionnez **Produits**.
3.  Sélectionnez un enregistrement de produit à supprimer, puis, dans la barre de commandes, sélectionnez **Supprimer**.
4.  Dans la boîte de dialogue **Confirmer la suppression**, cliquez sur **Continuer**.
 
 ## <a name="quantity-factors-for-products"></a>Facteurs de quantité pour les produits

Les facteurs de quantité prennent en charge la vente des produits basés sur un abonnement. Pour les produits basés sur abonnement, la quantité sur le devis ou la ligne de contrat du projet est exprimée sous la forme du nombre de mois d’utilisateur.

En règle générale, le prix des logiciels sur abonnement est stocké dans le catalogue comme prix par utilisateur par mois. Cependant, vous pouvez utiliser d’autres descriptions de temps à la place. Durant le processus de vente, le prix sur la ligne de devis est généralement le prix par utilisateur, par mois, négocié et avec remise, par l’agent de vente informatique. Chaque transaction a un nombre différent d’utilisateurs et un nombre différent de mois d’abonnement. La quantité utilisée pour calculer le montant de la ligne de devis est un produit du nombre d’utilisateurs et du nombre de mois d’abonnement.

Les facteurs de quantité reposent sur les attributs du produit. Lorsque vous configurez des propriétés spécifiques pour un produit, vous pouvez marquer un sous-ensemble de ces propriétés, ou toutes les propriétés, comme des facteurs de la quantité.

Le système valide que seules les propriétés numériques ou les propriétés de produit ayant un type de données numérique sont marquées comme facteurs de la quantité. Lorsqu’un produit pour lequel des facteurs de quantité sont configurés est ajouté à une ligne de devis, le champ **Quantité** de la ligne de devis devient un champ en lecture seule. Après avoir entré des valeurs pour les propriétés du produit qui sont des facteurs de quantité, la quantité de la ligne de devis est calculée.

Par exemple, s’il existe les propriétés suivantes : 

- **Nombre d’utilisateurs** : Le nombre d’utilisateurs 
- **Nombre de mois** : Le nombre de mois d’abonnement
- **SKU produit** 

Les propriétés **Nombre d’utilisateurs** et **Nombre de mois** peuvent être marquées comme facteurs de quantité en modifiant les propriétés de la ligne de produit. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]