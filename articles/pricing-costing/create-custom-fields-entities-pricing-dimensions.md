---
title: Créer des champs et des entités personnalisés comme dimensions de tarification
description: Cette rubrique fournit des informations sur la création de groupes d’options ou d’entités personnalisé(es).
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130890"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Créer des champs et des entités personnalisés comme dimensions de tarification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Effectuez les étapes suivantes chaque fois que vous voulez créer un groupe d’options ou une entité personnalisé(e).

> [!IMPORTANT]
> Il est recommandé d’apporter toutes les modifications de dimension de tarification personnalisées dans une solution distincte. Cette meilleure pratique importante procure la flexibilité nécessaire à l’avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance. Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d’autres instances pour réutiliser votre configuration de tarification.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Créer une solution personnalisée pour les dimensions Tarification
1. Allez dans **Paramètres** > **Solutions**, puis cliquez sur **Nouveau** pour créer une solution. 
2. Nommez la solution, **\<your organization name> dimensions tarification**, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Créer des champs et des jeux d’options personnalisés dans la solution de dimension Tarification

Une dimension Tarification peut être un jeu d’options ou une entité. Tous deux doivent être créés dans votre solution de tarification. Les étapes de cette procédure expliquent comment créer des dimensions basées sur une entité et des dimensions basées sur un jeu d’options.

### <a name="entity-based-dimensions"></a>Dimensions basées sur une entité

1. Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités**.
3. Cliquez sur **Nouveau** pour créer une entité intitulée **Titre standard**. 
4. Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.


### <a name="option-set-based-dimensions"></a>Dimensions basées sur un jeu d’options 
Vous pouvez créer deux dimensions basées sur un jeu d’options. Utilisez **Emplacement de travail des ressources** pour suivre le prix du travail d’emplacement **Accueil** et du travail **Sur le site** et utilisez **Heures de travail des ressources** avec les valeurs **Régulier** et **Heures supplémentaires** pour appliquer une majoration lorsque le travail est terminé.


1. Allez dans **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Jeux d’options**. 
3. Cliquez sur **Nouveau** pour créer un groupe d’options, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

## <a name="create-data-for-entity-based-dimensions"></a>Créer des données pour les dimensions basées sur une entité

Vous pouvez créer des données pour les dimensions basées sur une entité manuellement, ou en utilisation l’importation Microsoft Excel ou les appels de service. Suivez les étapes de cette procédure pour créer deux titres standard, **Ingénieur système** et **Ingénieur système principal** de la dimension basée sur une entité, **Titre standard**. Si les données que vous voulez créer sont petites, comme dans l’exemple suivant, vous pouvez utiliser un formulaire standard.

1. Sélectionnez **Recherche avancée**, sélectionnez l’entité **Titre standard**, puis sélectionnez **Résultats**. Toutes les lignes de l’entité **Titre standard** s’afficheront.
2. Sélectionnez **Nouveau**, dans le champ **Nom**, entrez « Ingénieur système », puis cliquez sur **Enregistrer**.
3. Fermer le formulaire. 
4. Répétez les étapes 1 à 3 pour créer un autre titre standard pour « Ingénieur système principal ».

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Ajouter tous les entités requises et les composants associés à la solution Dimension de tarification
Vous devrez ajouter les entités suivantes à votre solution de tarification. Utilisez la procédure ci-dessous pour apporter quelques modifications importantes au schéma dans la solution de tarification de sorte que les entités soient informées des nouvelles dimensions de tarification.

1. Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.
3. Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :

  - Chiffre réel
  - Ressource pouvant être réservée
  - Ligne d’estimation
  - Détail de la ligne de facture
  - Ligne de journal
  - Détail de la ligne de contrat du projet
  - Membre de l’équipe du projet
  - Détail de la ligne de devis
  - Majoration du prix du rôle
  - Prix du rôle 
  - Entrée de temps 


> [!NOTE]
> Veillez à inclure tous les formulaires et vues pour chacune des entités sélectionnées.

4. Lorsque vous êtes invité à inclure toutes les entités dépendantes des entités sélectionnées ci-dessus, cliquez sur **Non**.

