---
title: Page d'accueil Dimensions de tarification et des coûts
description: Cette rubrique présente les dimensions de tarification.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 137fee27dd2302d47ae12faccde1682cff43db93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284130"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Page d'accueil Dimensions de tarification et des coûts

[!include [banner](../includes/psa-now-project-operations.md)]

Les dimensions utilisées pour définir la tarification et le coût de la main-d’œuvre dans les organisations basées sur des projets sont influencées par les attributs suivants :

- Personnes effectuant un travail similaire à leur expérience, leur rôle ou leur géographie
- Travail à effectuer similaire en termes de complexité ou d’heure de la journée

Étant donné la nature classique de ces attributs du travail et des personnes nécessaires pour effectuer le travail, deux types de valeurs de dimension Tarification sont disponibles dans Project Service Automation : 

- **Jeux d’options** : attributs qui sont des énumérations fixes d’un ensemble de valeurs.
- **Valeurs basées sur l’entité** : attributs qui peuvent avoir un ensemble varié de valeurs qui sont finies, mais qui peuvent changer avec le temps.

## <a name="pricing-dimensions"></a>Dimensions de tarification

Expéditions PSA avec un ensemble par défaut de dimensions de tarification. Vous pouvez consulter ces derniers en accédant à **Project Service** > **Paramètres**. Dans l'enregistrement du paramètre, dans l'onglet **Dimensions de tarification basées sur un montant**, vérifiez que le rôle, **msdyn_resourcecategory** et l'unité d'organisation d'allocation des ressources, **msdyn_organizationalunit**, contiennent les champs **Applicable aux ventes** et **Applicable aux coûts** définis sur **Oui**. Vous pourrez ainsi configurer le prix et le coût de chaque combinaison de rôle et d'unité d'organisation.

![Capture d'écran des paramètres de Project Service avec « Applicable aux ventes » en surbrillance](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Si vous avez utilisé les champs prédéfinis du rôle et de l'unité d'organisation comme dimensions de tarification avant la version 3 de PSA, il n'existera pas de modification observable. Vous pouvez continuer à utiliser Project Service comme d'habitude. 

Si vous devez évaluer un prix ou un coût pour vos ressources en utilisant des attributs supplémentaires, vous pouvez créer des champs, des entités, et des dimensions personnalisés. Pour plus d'informations, consultez les rubriques suivantes, toutefois notez que vous devez exécuter les procédures dans l'ordre indiqué ci-dessous :

- [Créer des champs et des entités personnalisés](create-custom-fields-entities.md)
- [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md)
- [Configurer des champs personnalisés comme dimensions de tarification ](set-up-pricing-dimensions.md)
- [Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Tarification du temps des ressources humaines
Comment une organisation évalue le temps des ressources humaines est souvent un facteur stratégique important qui affecte directement la rentabilité de l'organisation. Utilisez les équipes des finances et les responsables des recommandations lorsque votre organisation est prête à identifier comment elle souhaite configurer les taux de facture et de coût du temps des ressources humaines.

D’autres points pour la tarification comprennent si réutiliser des champs ou des entités qui ne sont pas des dimensions de tarification actuellement, mais appliquer comme dimension de tarification pour votre organisation. Les champs, tels que **Catégorie de transaction** (**msdyn_transactioncategory**) et **Ressource pouvant être réservée** (**bookableresource**) sont des exemples des dimensions possibles. 

Choisissez si votre dimension de tarification doit être une table ou un jeu d’options. Si vous prévoyez de changer des valeurs d’une dimension qui dépasseront 10 ou 12 et si vous avez besoin d’autres attributs sur ces valeurs, vous pouvez créer une entité et non un jeu d’options. Tenir à jour un jeu d’options, tel qu’ajouter ou supprimer des valeurs, nécessite un administrateur ou un développeur alors qu’ajouter de nouvelles lignes à une table peut être effectué par la plupart des utilisateurs professionnels.

L'exemple suivant présente des taux de factures configurés en fonction du rôle et de l'unité d'organisation d'allocation des ressources à laquelle la ressource appartient. Les taux de coûts sont généralement basés sur la bande du salaire de l’employé et l’unité d’organisation à laquelle il appartient. Dans cet exemple, les tables de taux de factures et de taux de coûts ressemblent au suivant.

**Exemple de taux de factures**

| Rôle        | Unité d’organisation    |Unité      |Prix      |Devise  |
| ------------|-------------|----------|----------:|----------|
| Développeur   | Contoso US  |Hour | 200|USD     |
| Développeur   | Contoso Inde |Hour|   112|USD     |


**Exemple de taux de coûts**

| Bande de salaire     | Unité d’organisation    |Unité      |Prix      |Devise  |
| ----------------|-------------|----------|----------:|----------|
| Ma société_Band1 | Contoso US  |Hour | 145|USD     |
| Ma société_Band2 | Contoso Inde |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]