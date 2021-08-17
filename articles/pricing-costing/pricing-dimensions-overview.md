---
title: Vue d’ensemble des dimensions de tarification
description: Cette rubrique donne des informations sur les dimensions de tarification dans Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001968"
---
# <a name="pricing-dimensions-overview"></a>Vue d’ensemble des dimensions de tarification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les dimensions qui sont utilisées dans les ressources humaines pour définir la tarification et les coûts ont deux catégories :

- Personnes
- Travail planifié

Pour cette raison, deux types de valeurs de dimension de tarification sont disponibles :

- **Jeux d’options** : Dimensions qui sont des énumérations fixes d’un ensemble de valeurs.
- **Valeurs basées sur une entité** : Dimensions qui peuvent être un ensemble de valeurs varié.

## <a name="pricing-dimensions"></a>Dimensions de tarification

Dynamics 365 Project Operations est fourni avec un ensemble par défaut de dimensions de tarification. Vous pouvez les consulter en accédant à **Project Operations** > **Paramètres**. Dans l’enregistrement du paramètre, dans l’onglet **Dimensions de tarification basées sur un montant**, vérifiez que le rôle, **msdyn_resourcecategory** et l’unité d’organisation d’allocation des ressources, **msdyn_organizationalunit**, contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**. Si ces champs sont activés, vous pouvez alors configurer le prix et le coût de chaque combinaison de rôle et d’unité d’organisation.

![Capture d’écran des paramètres de Project Service avec « Applicable aux ventes » en surbrillance.](media/PS-OOB-parameters.png)

Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés. Pour plus d’informations, voir les rubriques suivantes. 
  
  > [!NOTE]
  > Les procédures doivent être exécutées dans l’ordre dans lequel elles sont répertoriées.

1. [Créer une solution personnalisée pour les dimensions Tarification](../sales/create-solution-custompd.md)
2. [Créer des champs et des entités personnalisés](create-custom-fields-entities-pricing-dimensions.md)
3. [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurer des champs personnalisés comme dimensions de tarification ](set-up-custom-fields-pricing-dimensions.md)
5. [Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Tarification du temps des ressources humaines
Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l’organisation. Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.

D’autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation. Les champs, tels que **Catégorie de transaction** (**msdyn_transactioncategory**) et **Ressource pouvant être réservée** (**bookableresource**) sont des exemples des dimensions possibles. 

Choisissez si votre dimension de tarification doit être une table ou un jeu d’options. Si vous prévoyez de changer des valeurs d’une dimension qui dépasseront 10 ou 12 et que vous avez besoin d’autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d’options. Tenir à jour un jeu d’options, tel qu’ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu’ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs.

L’exemple suivant présente des taux de factures configurés en fonction du rôle et de l’unité d’organisation d’allocation des ressources à laquelle la ressource appartient. Les taux de coûts sont généralement basés sur la bande du salaire de l’employé et l’unité d’organisation à laquelle il appartient. Dans cet exemple, les tables de taux de factures et de taux de coûts ressemblent au suivant.

**Exemple de taux de factures**

| Rôle        | Unité d’organisation    |Unité      |Prix      |Devise  |
| ------------|-------------|----------|----------:|----------|
| Développeur   | Contoso US  |heure | 200|USD     |
| Développeur   | Contoso Inde |heure|   112|USD     |


**Exemple de taux de coûts**

| Bande de salaire     | Unité d’organisation    |Unité      |Prix      |Devise  |
| ----------------|-------------|----------|----------:|----------|
| Ma société_Band1 | Contoso US  |heure | 145|USD     |
| Ma société_Band2 | Contoso Inde |heure|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]