---
title: Unités et groupes d’unités
description: Cette rubrique fournit des informations sur la création d'unités et de groupes d'unités dans Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075863"
---
# <a name="units-and-unit-groups"></a>Unités et groupes d’unités

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les unités sont les quantités ou les mesures selon lesquelles vous vendez vos produits ou services. Par exemple, si vous vendez des fournitures de jardinage, vous pouvez vendre des graines par unités de paquets, de cartons et de palettes. Un groupe d'unités est une combinaison de ces différentes unités.

Pour effectuer les étapes de cette rubrique, assurez-vous de disposer du rôle d'Administrateur système ou de gestionnaire de Sales Professional ou d'autorisations équivalentes..

## <a name="create-a-unit-group"></a>Créer un groupe d'unités

1. Sur le plan de site, sélectionnez **Unités**.
2. Sélectionnez **Nouveau** , et tapez le nom de l'unité dans la boîte de dialogue **Créer Unité de vente**.
3. Dans le champ **Unité principale** , entrez la plus petite unité de mesure courante dans laquelle le produit doit être vendu. Par exemple, vous pouvez entrer « pièce » ou « once ».
4. Cliquez sur **OK**.

## <a name="add-units-to-a-unit-group"></a>Ajouter des unités à un groupe d'unités

1. Ouvrez un groupe d'unités et sur l'onglet **Association** , sélectionnez **Unités**. Vous verrez que l'unité principale est déjà ajoutée.
2. Sélectionnez **Ajouter une nouvelle unité** , et sur la page **Création rapide : Unité** , entrez le nom de l'unité dans le champ **Nom**.
3. Dans le champ **Quantité** , entrez la quantité que cette unité représentera. Par exemple, si une boîte contient deux pièces, entrez « 2 ». 
4. Dans le champ **Unité de base** , sélectionnez une unité de base pour établir la plus petite unité de mesure pour l'unité. Par exemple, vous pouvez sélectionner « Pièce ».
5. Sélectionnez **Enregistrer**  :
