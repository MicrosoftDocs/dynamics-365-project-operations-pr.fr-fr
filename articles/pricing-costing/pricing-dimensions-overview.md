---
title: Vue d’ensemble des dimensions de tarification
description: Cette rubrique fournit des informations sur les dimensions de tarification dans Dynamics 365 Project Operations.
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075847"
---
# <a name="pricing-dimensions-overview"></a>Vue d’ensemble des dimensions de tarification

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les dimensions qui sont utilisées dans les ressources humaines pour définir la tarification et les coûts ont deux catégories :

- Personnes
- Travail planifié

Pour cette raison, deux types de valeurs de dimension de tarification sont disponibles :

- **Jeux d'options**  : Dimensions qui sont des énumérations fixes d'un ensemble de valeurs.
- **Valeurs basées sur une entité**  : Dimensions qui peuvent être un ensemble de valeurs varié.

## <a name="pricing-dimensions"></a>Dimensions de tarification

Dynamics 365 Project Operations est livré avec un ensemble par défaut de dimensions de tarification. Vous pouvez les consulter en accédant à **Project Operations** > **Paramètres**. Dans l'enregistrement du paramètre, dans l'onglet **Dimensions de tarification basées sur un montant** , vérifiez que le rôle, **msdyn_resourcecategory** et l'unité d'organisation d'allocation des ressources, **msdyn_organizationalunit** , contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**. Si ces champs sont activés, vous pouvez alors configurer le prix et le coût de chaque combinaison de rôle et d'unité d'organisation.

Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés.

## <a name="pricing-human-resource-time"></a>Tarification du temps des ressources humaines
Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l'organisation. Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.

D'autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation. Les champs, tels que **Catégorie de transaction** ( **msdyn_transactioncategory** ) et **Ressource pouvant être réservée** ( **bookableresource** ) sont des exemples des dimensions possibles. 

Choisissez si votre dimension de tarification doit être une table ou un jeu d'options. Si vous prévoyez de changer des valeurs d'une dimension qui dépasseront 10 ou 12 et que vous avez besoin d'autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d'options. Tenir à jour un jeu d'options, tel qu'ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu'ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs.

L'exemple suivant présente des taux de factures configurés en fonction du rôle et de l'unité d'organisation d'allocation des ressources à laquelle la ressource appartient. Les taux de coûts sont généralement basés sur la bande du salaire de l'employé et l'unité d'organisation à laquelle il appartient. Dans cet exemple, les tables de taux de factures et de taux de coûts ressemblent au suivant.

**Exemple de taux de factures**

| Rôle        | Unité d'organisation    |Unité      |Prix      |Devise  |
| ------------|-------------|----------|----------:|----------|
| Développeur   | Contoso US  |Hour | 200|USD     |
| Développeur   | Contoso Inde |Hour|   112|USD     |


**Exemple de taux de coûts**

| Bande de salaire     | Unité d'organisation    |Unité      |Prix      |Devise  |
| ----------------|-------------|----------|----------:|----------|
| Ma société_Band1 | Contoso US  |Hour | 145|USD     |
| Ma société_Band2 | Contoso Inde |Hour|   67|USD     |
