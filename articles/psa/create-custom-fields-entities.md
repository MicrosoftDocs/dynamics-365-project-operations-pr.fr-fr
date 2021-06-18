---
title: Créer des champs et des entités personnalisés
description: Cette rubrique explique comment créer des jeux d’options et des entités dans votre propre solution dans la plateforme Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998948"
---
# <a name="create-custom-fields-and-entities"></a>Créer des champs et des entités personnalisés 

[!include [banner](../includes/psa-now-project-operations.md)]

Effectuez les étapes suivantes chaque fois que vous voulez créer un jeu d’options ou une entité personnalisés sur la plateforme Power Apps.  
Les procédures dans cette rubrique doivent être effectuées à l’aide de l’interface web Project Service Automation (PSA).

> [!IMPORTANT]
> Il est recommandé d’apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte. Cette meilleure pratique importante procure la flexibilité nécessaire à l’avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance. Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d’autres instances pour réutiliser votre configuration de tarification.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Créer des champs et des jeux d’options personnalisés dans la solution de dimension Tarification

Une dimension Tarification peut être un jeu d’options ou une entité. Tous deux doivent être créés dans votre solution de tarification. Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d’options.

### <a name="entity-based-dimensions"></a>Dimensions basées sur une entité

1. Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis double-cliquez sur **Dimensions Tarification \<your organization name>**.
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités**.
3. Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**. Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

> ![Définition de l’entité Titre standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensions basées sur un jeu d’options 
Vous pouvez créer deux dimensions basées sur un jeu d’options. Utilisez **Emplacement de travail des ressources** pour suivre le prix du travail d’emplacement **Accueil** et du travail **Sur le site** et utilisez **Heures de travail des ressources** avec les valeurs **Régulier** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.


1. Dans PSA, cliquez sur **Paramètres** > **Solutions**, puis double-cliquez sur **Dimensions Tarification \<your organization name>**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Jeux d’options**. 
3. Cliquez sur **Nouveau** pour créer un jeu d’options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

> ![Dimension Tarification basée sur un jeu d’options appelé Emplacement de travail de la ressource ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimension Tarification basée sur un jeu d’options appelé Heures de travail de la ressource ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Créer des données pour les dimensions basées sur une entité

Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l’importation Microsoft Excel ou les appels de service. Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**. Si les données que vous voulez créer sont petites, comme dans l’exemple suivant, vous pouvez utiliser un formulaire standard.

1. Dans PSA, cliquez sur **Recherche avancée**. Sélectionnez l’entité **Titre standard**, puis cliquez sur **Résultats**. Toutes les lignes de l’entité **Titre standard** s’afficheront.
2. Cliquez sur **Nouveau**. Dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.
3. Fermez le formulaire. 
4. Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».

> ![Exemple de données pour l’entité Titre standard ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]