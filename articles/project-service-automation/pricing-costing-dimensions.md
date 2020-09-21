---
title: Page d'accueil Dimensions de tarification et des coûts
description: Cette rubrique présente les dimensions de tarification.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168028"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Page d'accueil Dimensions de tarification et des coûts

Les dimensions qui sont utilisées dans les ressources humaines pour définir la tarification et les coûts ont deux catégories :

- Personnes
- Travail planifié

Ainsi, il existe deux types de valeurs de dimension de tarification disponibles dans Project Service Automation (PSA) : 

- **Jeux d'options** - Dimensions qui sont des énumérations fixes d'un ensemble de valeurs.
- **Valeurs basées sur une entité** - Dimensions qui peuvent être un ensemble de valeurs varié.

## <a name="pricing-dimensions"></a>Dimensions de tarification

Expéditions PSA avec un ensemble par défaut de dimensions de tarification. Vous pouvez consulter ces derniers en accédant à **Project Service** > **Paramètres**. Dans l'enregistrement du paramètre, dans l'onglet **Dimensions de tarification basées sur un montant**, vérifiez que le rôle, **msdyn_resourcecategory** et l'unité d'organisation d'allocation des ressources, **msdyn_organizationalunit**, contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**. Vous pourrez ainsi configurer le prix et le coût de chaque combinaison de rôle et d'unité d'organisation.

![Capture d'écran des paramètres de Project Service avec « Applicable aux ventes » en surbrillance](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Si vous avez utilisé les champs prédéfinis du rôle et de l'unité d'organisation comme dimensions de tarification avant la version 3 de PSA, il n'existera pas de modification observable. Vous pouvez continuer à utiliser Project Service comme d'habitude. 

Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés. Pour plus d'informations, consultez les rubriques suivantes, toutefois notez que vous devez exécuter les procédures dans l'ordre indiqué ci-dessous :

- [Créer des champs et des entités personnalisés](create-custom-fields-entities.md)
- [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md)
- [Configurer des champs personnalisés comme dimensions de tarification](set-up-pricing-dimensions.md)
- [Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Tarification du temps des ressources humaines
Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l'organisation. Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.

D'autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation. Les champs, tels que **Catégorie de transaction** (**msdyn_transactioncategory**) et **Ressource pouvant être réservée** (**bookableresource**) sont des exemples des dimensions possibles. 

Vous devez également envisager si votre dimension de tarification doit être une table ou un jeu d'options. Si vous prévoyez de changer des valeurs d'une dimension qui dépasseront 10 ou 12 et que vous avez besoin d'autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d'options. Tenir à jour un jeu d'options, tel qu'ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu'ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs.

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
