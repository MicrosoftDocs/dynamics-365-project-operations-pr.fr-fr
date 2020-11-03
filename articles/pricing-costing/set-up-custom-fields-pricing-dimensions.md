---
title: Configurer des champs personnalisés comme dimensions de tarification
description: Cette rubrique donne des informations sur la configuration de dimensions de tarification à l'aide de champs personnalisés.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 087950c9639a95868a20d71286dfad4437555108
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075735"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Configurer des champs personnalisés comme dimensions de tarification

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Avant de commencer, cette rubrique suppose que vous avez effectué les procédures décrites dans les rubriques, [Créer des champs et des entités personnalisés](create-custom-fields-entities-pricing-dimensions.md) et [Ajouter des champs personnalisés obligatoires au paramétrage de tarifs et aux entités transactionnelles](add-custom-fields-price-setup-transactional-entities.md). Si vous n'avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cette rubrique. 

Cette rubrique donne des informations sur la configuration de dimensions de tarification personnalisées. Dans la page **Paramètres** , l'onglet **Dimensions de tarification basées sur le montant** affiche les enregistrements des entités Dimension de tarification. Par défaut, il y a deux lignes dans la grille sur cet onglet :

- **msdyn_resourcecategory** (rôle)
- **msdyn_OrganizationalUnit** (unité d'organisation)

> [!IMPORTANT]
> Ne supprimez pas ces lignes. Toutefois, si vous n'en avez pas besoin, vous pouvez les rendre non applicables dans un contexte spécifique en définissant **Applicable aux coûts** , **Applicable aux ventes** et **Applicable aux achats** sur **Non**. Définir ces valeurs d'attribut sur **Non** revient au même que de ne pas définir un champ comme dimension de tarification.

Pour qu'un champ devienne une dimension de tarification, il doit être :

- Créé en tant que champ dans les entités **Prix du rôle** et **Majoration du prix du rôle**. Pour plus d'informations sur cette procédure, consultez [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](add-custom-fields-price-setup-transactional-entities.md).
- Créé en tant que ligne dans la table **Dimension de tarification**. Par exemple, ajoutez des lignes de dimension de tarification, comme illustré dans le graphique suivant. 

Les heures de travail de la ressource ( **msdyn_resourceworkhours** ) ont été ajoutée comme dimension basée sur la majoration et ajoutée à la grille de l'onglet **Dimension de tarification basée sur la majoration**.

> [!IMPORTANT]
> Toute modification des données de dimension de tarification contenues dans ce tableau, existantes ou nouvelles, est propagée à la logique métier de tarification uniquement après actualisation du cache. L'actualisation du cache peut prendre jusqu'à 10 minutes. En attendant, vous pouvez voir les modifications de la logique de prix par défaut qui doivent résulter des modifications des données de dimension de tarification.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributs de la table Dimensions de tarification
Les sections suivantes donnent des informations sur les différents attributs de la table **Dimensions de tarification**.

### <a name="pricing-dimension-name"></a>Nom de la dimension de tarification
Cette valeur doit être exactement la même que le nom de schéma du champ ajouté à la table **Prix du rôle** pour les dimensions de tarification personnalisées. Pour plus d'informations sur l'ajout de champs à la table **Prix du rôle** , consultez [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Type de dimension
Il existe deux types de dimensions de tarification :
  
  - **Dimensions basées sur le montant**  : les valeurs de dimension dans le contexte d'entrée sont mises en correspondance avec les valeurs de dimension de la ligne **Prix du rôle** et le prix/coût est défini par défaut directement à partir de la table **Prix du rôle**.
  - **Dimensions basées sur la majoration**  : Ce sont des dimensions pour lesquelles le processus en 3 étapes ci-après pour obtenir le prix/coût est utilisé :
 
    1. Les valeurs de dimension qui ne sont pas basées sur la majoration dans le contexte d'entrée sont mises en correspondance avec la ligne Prix du rôle pour obtenir le taux de base.
    2. Les valeurs de dimension dans le contexte d'entrée sont mises en correspondance avec la ligne **Majoration du prix du rôle** pour obtenir un pourcentage de majoration.
    3. Le pourcentage de majoration dans la seconde étape est appliqué au taux de base obtenu à partir de la table **Prix du rôle** dans la première étape pour arriver au prix/coût final.
   
   Le tableau suivant illustre le calcul des majorations de prix.
  
| Rôle        | Unité d'organisation    |Emplacement de travail      |Titre standard      |Heures de travail de la ressource      |  Majoration|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Inde|Sur site            |                    |Heures supplémentaires                 |15     |
|             | Contoso Inde|Local             |                    |Heures supplémentaires                 |10     |
|             | Contoso US   |Local             |                    |Heures supplémentaires                 |20     |


Si une ressource de Contoso Inde dont le taux de base est 100 USD travaille sur site, et si elle consigne 8 heures de travail normales et 2 heures supplémentaires dans l'entrée de temps, le moteur de tarification utilise le taux de base de 100 USD pour les 8 heures pour obtenir 800 USD. Pour les 2 heures supplémentaires, une majoration de 15 % est appliquée au taux de base de 100 USD pour obtenir un prix unitaire de 115 USD et un coût total de 230 USD.

### <a name="applicable-to-cost"></a>Applicable aux coûts 
Si ce paramètre est défini sur **Oui** , cela indique que la valeur de dimension dans le contexte d'entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération des taux de coût et de majoration.

### <a name="applicable-to-sales"></a>Applicable aux ventes
Si ce paramètre est défini sur **Oui** , cela indique que la valeur de dimension dans le contexte d'entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération des taux de facturation et de majoration.

### <a name="applicable-to-purchase"></a>Applicable aux achats
Si ce paramètre est défini sur **Oui** , cela indique que la valeur de dimension dans le contexte d'entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération du prix d'achat. Les scénarios de sous-traitance ne sont pas pris en charge, ce champ n'est donc pas utilisé. 

### <a name="priority"></a>Priorité
La définition de la priorité de la dimension aide à produire un prix même lorsqu'elle ne trouve pas de correspondance exacte entre les valeurs de dimension d'entrée et les valeurs des tables **Prix du rôle** ou **Majoration du prix du rôle**. Dans ce cas, des valeurs nulles sont utilisées pour les valeurs de dimension sans correspondance en pondérant les dimensions dans leur ordre de priorité.

- **Priorité des coûts**  : la valeur de la priorité des coûts d'une dimension indique le poids de cette dimension lors de la mise en correspondance avec la configuration des prix de revient. La valeur de **Priorité des coûts** doit être unique dans les dimensions **applicables aux coûts**.
- **Priorité des ventes**  : la valeur de la priorité des ventes d'une dimension indique le poids de cette dimension lors de la mise en correspondance avec la configuration des prix de vente ou des taux de facturation. La valeur de **Priorité des ventes** doit être unique dans les dimensions **applicables aux ventes**.
