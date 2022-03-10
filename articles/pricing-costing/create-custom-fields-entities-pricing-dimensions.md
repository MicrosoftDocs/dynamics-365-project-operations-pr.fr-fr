---
title: Créer des champs et des entités personnalisés comme dimensions de tarification
description: Cette rubrique fournit des informations sur la création de groupes d’options ou d’entités personnalisé(es).
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 40a6a4173cb0e4d7ea5bcf24c8954fe9d7e079d1e9ecf4aac252b5133f12d3ff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003633"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Créer des champs et des entités personnalisés comme dimensions de tarification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Effectuez les étapes suivantes lorsque vous voulez créer un jeu d’options ou une entité personnalisés à utiliser comme dimension de tarification. Pour plus d’informations, voir [Vue d’ensemble des dimensions de tarification](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Il est recommandé d’apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte. Cette bonne pratique importante offre une flexibilité à l’avenir pour mettre à jour ou supprimer les modifications selon les besoins. Cela vous aidera également à réutiliser votre travail et facilitera le portage de ces modifications vers une autre instance. Après avoir effectué toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d’autres instances pour réutiliser votre configuration de tarification.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Créer des champs et des jeux d’options personnalisés dans la solution de dimension Tarification

Une dimension Tarification peut être un jeu d’options ou une entité. Tous deux doivent être créés dans votre solution de tarification. Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d’options.

### <a name="entity-based-dimensions"></a>Dimensions basées sur une entité
Pour créer des dimensions basées sur une entité, procédez comme suit :

1. Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.
2. Dans l’Explorateur de solutions, dans le volet de navigation de gauche, sélectionnez **Entités**.
3. Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**. 
4. Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

> ![Définition de l’entité Titre standard.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensions basées sur un jeu d’options 
Vous pouvez créer deux dimensions basées sur un jeu d’options. 

- Utilisez **Emplacement de travail des ressources** pour suivre le prix de l’emplacement de travail **Accueil** et le travail **Sur site**. 
- Utilisez **Heures de travail des ressources** avec les valeurs **Régulières** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.

Le graphique suivant fournit une vue de la dimension **Emplacement de travail des ressources**. 

> ![Dimension Tarification basée sur un jeu d’options appelé Emplacement de travail de la ressource.](media/Option-set-PD-called-Resource-Work-Location.png)

Le graphique suivant fournit une vue de la dimension **Heures de travail des ressources**. 

> ![Dimension Tarification basée sur un jeu d’options appelé Heures de travail de la ressource.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, dans le volet de navigation de gauche, sélectionnez **Jeux d’options**. 
3. Cliquez sur **Nouveau** pour créer un groupe d’options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

## <a name="create-data-for-entity-based-dimensions"></a>Créer des données pour les dimensions basées sur une entité

Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l’importation Microsoft Excel ou les appels de service. Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**. Si les données que vous voulez créer sont petites, comme dans l’exemple suivant, vous pouvez utiliser un formulaire standard.

1. Sélectionnez **Recherche avancée**.
2. Sélectionnez l’entité **Titre standard**, puis cliquez sur **Résultats**. Toutes les lignes de l’entité **Titre standard** s’afficheront.
3. Sélectionnez **Nouveau**, dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.
4. Fermez la page. 
5. Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».

> ![Exemple de données pour l’entité Titre standard.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]