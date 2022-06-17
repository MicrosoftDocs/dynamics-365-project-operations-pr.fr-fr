---
title: Unités et groupes d’unités
description: Cet article fournit des informations sur la création d’unités et de groupes d’unités dans Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a46b7d182d3d7fc77c1275c108f5dc569ffebff1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921437"
---
# <a name="units-and-unit-groups"></a>Unités et groupes d’unités

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les unités sont les quantités ou les mesures selon lesquelles vous vendez vos produits ou services. Par exemple, si vous vendez des fournitures de jardinage, vous pouvez vendre des graines par unités de paquets, de cartons et de palettes. Un groupe d’unités est un ensemble de ces différentes unités.

Pour suivre les étapes de cet article, assurez-vous que vous avez été affecté au rôle administrateur système ou responsable Sales Professional ou que vous disposez d’autorisations équivalentes.

## <a name="create-a-unit-group"></a>Créer un groupe d’unités

1. Sur le plan de site, sélectionnez **Unités**.
2. Sélectionnez **Nouveau**, et tapez le nom de l’unité dans la boîte de dialogue **Créer Unité de vente**.
3. Dans le champ **Unité principale**, entrez la plus petite unité de mesure courante dans laquelle le produit doit être vendu. Par exemple, vous pouvez entrer « pièce » ou « once ».
4. Cliquez sur **OK**.

## <a name="add-units-to-a-unit-group"></a>Ajouter des unités à un groupe d’unités

1. Ouvrez un groupe d’unités et sur l’onglet **Association**, sélectionnez **Unités**. Vous verrez que l’unité principale est déjà ajoutée.
2. Sélectionnez **Ajouter une nouvelle unité**, et sur la page **Création rapide : Unité**, entrez le nom de l’unité dans le champ **Nom**.
3. Dans le champ **Quantité**, entrez la quantité que cette unité représentera. Par exemple, si une boîte contient deux pièces, entrez « 2 ». 
4. Dans le champ **Unité de base**, sélectionnez une unité de base pour établir la plus petite unité de mesure pour l’unité. Par exemple, vous pouvez sélectionner « Pièce ».
5. Sélectionnez **Enregistrer** :


[!INCLUDE[footer-include](../includes/footer-banner.md)]