---
title: Configuration des champs personnalisés comme dimensions de tarification
description: Cette rubrique donne des informations sur la configuration de dimensions de tarification personnalisées.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cce3a3fe6aef247380f6284f58d49337f969c38c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008308"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Configuration des champs personnalisés comme dimensions de tarification 

[!include [banner](../includes/psa-now-project-operations.md)]

Avant de commencer, cette rubrique suppose que vous avez effectué les procédures décrites dans les rubriques, [Créer des champs et des entités personnalisés](create-custom-fields-entities.md) et [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md). Si vous n’avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cette rubrique. 

Cette rubrique donne des informations sur la configuration de dimensions de tarification personnalisées. Dans l’interface Web de Project Service, dans la page **Paramètres**, l’onglet **Dimensions de tarification basées sur le montant** affiche les enregistrements des entités Dimension de tarification. Par défaut, l’installation de Project Service crée 2 lignes dans la grille de cet onglet :

- **msdyn_resourcecategory** (rôle)
- **msdyn_OrganizationalUnit** (unité d’organisation)

> [!IMPORTANT]
> Ne supprimez pas ces lignes. Toutefois, si vous n’en avez pas besoin, vous pouvez les rendre non applicables dans un contexte spécifique en définissant **Applicable aux coûts**, **Applicable aux ventes** et **Applicable aux achats** sur **Non**. Définir ces valeurs d’attribut sur **Non** revient au même que de ne pas définir un champ comme dimension de tarification.

Pour qu’un champ devienne une dimension de tarification, il doit être :

- Créé en tant que champ dans les entités **Prix du rôle** et **Majoration du prix du rôle**. Pour plus d’informations sur cette procédure, consultez [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md).
- Créé en tant que ligne dans la table **Dimension de tarification**. Par exemple, ajoutez des lignes de dimension de tarification, comme illustré dans le graphique suivant. 

![Lignes de dimension de tarification basées sur le montant](media/Amt-based-PD.png)

Notez que la ligne Heures de travail de la ressource (**msdyn_resourceworkhours**) a été ajoutée comme dimension basée sur la majoration et ajoutée à la grille de l’onglet **Dimension de tarification basée sur la majoration**.

![Lignes de dimension de tarification basées sur la majoration](media/Markup-based-PD.png)

> [!IMPORTANT]
> Toute modification des données de dimension de tarification contenues dans ce tableau, existantes ou nouvelles, est propagée à la logique métier de tarification de Project Service uniquement après actualisation du cache. L’actualisation du cache peut prendre jusqu’à 10 minutes. En attendant, vous pouvez voir les modifications de la logique de prix par défaut qui doivent résulter des modifications des données de dimension de tarification.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributs de la table Dimensions de tarification
Les sections suivantes donnent des informations sur les différents attributs de la table **Dimensions de tarification**.

### <a name="pricing-dimension-name"></a>Nom de la dimension de tarification
Cette valeur doit être exactement la même que le nom de schéma du champ ajouté à la table **Prix du rôle** pour les dimensions de tarification personnalisées. Pour plus d’informations sur l’ajout de champs à la table **Prix du rôle**, consultez [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md).

### <a name="type-of-dimension"></a>Type de dimension
Il existe deux types de dimensions de tarification :
  
  - **Dimensions basées sur le montant** : les valeurs de dimension dans le contexte d’entrée sont mises en correspondance avec les valeurs de dimension de la ligne **Prix du rôle** et le prix/coût est défini par défaut directement à partir de la table **Prix du rôle**.
  - **Dimensions basées sur la majoration** : ce sont des dimensions pour lesquelles Project Service adopte le processus en 3 étapes ci-après pour obtenir le prix/coût
 
    1. Project Service met en correspondance les valeurs de dimension qui ne sont pas basées sur la majoration dans le contexte d’entrée avec la ligne Prix du rôle pour obtenir le taux de base.
    2. Project Service met en correspondance toutes les valeurs de dimension dans le contexte d’entrée avec la ligne **Majoration du prix du rôle** pour obtenir un pourcentage de majoration.
    3. Project Service applique le pourcentage de majoration dans la seconde étape au taux de base obtenu à partir de la table **Prix du rôle** dans la première étape pour arriver au prix/coût final.
   
   Le tableau suivant illustre le calcul des majorations de prix.
  
| Rôle        | Unité d’organisation    |Emplacement de travail      |Titre standard      |Heures de travail de la ressource      |  Majoration|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Inde|Sur site            |                    |Heures supplémentaires                 |15     |
|             | Contoso Inde|Local             |                    |Heures supplémentaires                 |10     |
|             | Contoso US   |Local             |                    |Heures supplémentaires                 |20     |


Si une ressource de Contoso Inde dont le taux de base est 100 USD travaille sur site, et elle consigne 8 heures de travail normales et 2 heures supplémentaires dans l’entrée de temps, le moteur de tarification de Project Service utilise le taux de base de 100 USD pour les 8 heures pour obtenir 800 USD. Pour les 2 heures supplémentaires, une majoration de 15 %% est appliquée au taux de base de 100 USD pour obtenir un prix unitaire de 115 USD et un coût total de 230 USD.

### <a name="applicable-to-cost"></a>Applicable aux coûts 
Si ce paramètre est défini sur **Oui**, cela indique que la valeur de dimension dans le contexte d’entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération des taux de coût et de majoration.

### <a name="applicable-to-sales"></a>Applicable aux ventes
Si ce paramètre est défini sur **Oui**, cela indique que la valeur de dimension dans le contexte d’entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération des taux de facturation et de majoration.

### <a name="applicable-to-purchase"></a>Applicable aux achats
Si ce paramètre est défini sur **Oui**, cela indique que la valeur de dimension dans le contexte d’entrée doit être utilisée pour la mise en correspondance avec les champs **Prix du rôle** et **Majoration du prix du rôle** lors de la récupération du prix d’achat. Actuellement, Project Service ne prend pas en charge les scénarios de sous-traitance, ce champ n’est donc pas utilisé. 

### <a name="priority"></a>Priorité
La définition de la priorité de la dimension aide Project Service à produire un prix même lorsqu’elle ne trouve pas de correspondance exacte entre les valeurs de dimension d’entrée et les valeurs des tables **Prix du rôle** ou **Majoration du prix du rôle**. Dans ce cas, Project Service utilise des valeurs nulles pour les valeurs de dimension sans correspondance en pondérant les dimensions dans leur ordre de priorité.

- **Priorité des coûts** : la valeur de la priorité des coûts d’une dimension indique le poids de cette dimension lors de la mise en correspondance avec la configuration des prix de revient. La valeur de **Priorité des coûts** doit être unique dans les dimensions **applicables aux coûts**.
- **Priorité des ventes** : la valeur de la priorité des ventes d’une dimension indique le poids de cette dimension lors de la mise en correspondance avec la configuration des prix de vente ou des taux de facturation. La valeur de **Priorité des ventes** doit être unique dans les dimensions **applicables aux ventes**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]