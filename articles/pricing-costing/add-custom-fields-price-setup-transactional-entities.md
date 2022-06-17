---
title: Ajouter des champs personnalisés obligatoires au paramétrage de tarifs et aux entités transactionnelles
description: Cet article fournit des informations sur la façon d’ajouter des références de champs personnalisés obligatoires aux entités, aux formulaires et aux vues.
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
ms.openlocfilehash: a984dc9e04857e101fa012734fd822440899aced
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926037"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Ajouter des champs personnalisés obligatoires au paramétrage de tarifs et aux entités transactionnelles

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Cet article suppose que vous avez effectué les procédures de l’article [Création de champs et entités personnalisés à utiliser comme dimensions de tarification](create-custom-fields-entities-pricing-dimensions.md). Si vous n’avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cet article. 

Dans cet article, les procédures vous afficheront comment ajouter des références de champ aux entités personnalisées requises et aux éléments de l’interface utilisateur (IU), tels que les formulaires et les vues.

## <a name="add-custom-pricing-dimension-fields"></a>Ajouter des champs de dimension de tarification personnalisée 
Une fois les champs et entités personnalisés créés, l’étape suivante consiste à configurer les prix et informer les entités transactionnelles de toutes les entités ou jeux d’options personnalisés en créant des champs de référence. Selon que votre liste de dimensions de tarification comprend les dimensions de jeu d’options ou les dimensions d’entité, ou les deux, suivez uniquement les étapes de **Dimensions de tarification personnalisées basées sur un jeu d’options** ou **Dimensions de tarification personnalisées basées sur une entité**, ou les deux, respectivement.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensions de tarification personnalisées basées sur un jeu d’options
Lorsqu’une dimension de tarification option personnalisée est basée sur un jeu d’options, ajoutez-la en tant que champ dans les entités principales. Dans la procédure suivante, **Emplacement de travail des ressources** et **Heures de travail des ressources** sont utilisées comme dimensions de tarification basées sur un jeu d’options. Elles doivent être préalablement ajoutées en tant que champs dans les entités de tarification, **Prix du rôle** et **Majoration du prix de rôle**.

1. Dans Project Operations, sélectionnez **Paramètres** > **Solutions** et double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Prix du rôle**.
3. Développez l’entité **Prix du rôle** et sélectionnez **Champs**.
4. Cliquez sur **Nouveau** pour créer un champ nommé **Emplacement de travail des ressources** et sélectionnez **Jeu d’options** comme type de champ. 
5. Sélectionnez **Utiliser un jeu d’options existant**, sélectionnez le jeu d’options **Emplacement de travail des ressources**, puis cliquez sur **Enregistrer**.
6. Répétez les étapes 1 à 5 pour ajouter ce champ à l’entité **Majoration du prix du rôle**. 
7. Répétez les étapes 1 à 5 du jeu d’options **Heures de travail des ressources**.

> [!IMPORTANT]
> Lorsque vous ajoutez un champ à plusieurs entités, utilisez le même nom de champ dans toutes les entités. 

> ![Ajout de l’emplacement de travail des ressources à Prix du rôle.](media/RWL-Field.png)

Dans les phases de ventes et d’estimation d’un projet, les estimations de l’effort de travail sont requises pour effectuer le travail **Local** et **Sur le site**, et les **Heures régulières** et **Heures supplémentaires**, sont utilisées pour évaluer la valeur du devis/projet. Les champs **Emplacement de travail des ressources** et **Heures de travail des ressources** sont ajoutés aux entités d’estimation, **Détail de la ligne de devis**, **Détails de la ligne de contrat**, **Membre de l’équipe du projet**, puis **Ligne d’estimation**.

1. Dans Project Operations, sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Détail de la ligne de devis**.
3. Développez l’entité **Détail de la ligne de devis**, et sélectionnez **Champs**.
4. Cliquez sur **Nouveau** pour créer un champ nommé **Emplacement de travail des ressources** et sélectionnez **Jeu d’options** comme type de champ. 
5. Sélectionnez **Utiliser un jeu d’options existant** et **Emplacement de travail des ressources**, puis cliquez sur **Enregistrer**.
6. Répétez les étapes 1 à 5 pour ajouter ce champ aux entités **Détails de la ligne de contrat de projet**, **Membre de l’équipe de projet**, et **Ligne d’estimation**.
7. Répétez les étapes 1 à 6 du jeu d’options **Heures de travail des ressources**. 

> ![Ajout de l’emplacement de travail des ressources à Ligne d’estimation.](media/RWL-Default-Value.png)

Pour la livraison et la facturation, le travail effectué doit avoir le prix exact pour sélectionner si c’était **Local** ou **Sur le site**, et si effectué pendant les **Heures régulières** ou en **Heures supplémentaires** par rapport aux chiffres réels du projet. Les champs **Emplacement de travail des ressources** et **Heures de travail des ressources** doivent être ajoutés aux entités **Entrée de temps**, **Chiffre réel**, **Détail de la ligne de facture**, et **Ligne de journal**.

1. Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**.
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Entrée de temps**.
3. Développez l’entité **Détail de la ligne de devis**, puis sélectionnez **Champs**.
4. Cliquez sur **Nouveau** pour créer un champ nommé **Emplacement de travail des ressources** et sélectionnez **Jeu d’options** comme type de champ. 
5. Sélectionnez **Utiliser un jeu d’options existant**, sélectionnez le jeu d’options **Emplacement de travail des ressources**, puis cliquez sur **Enregistrer**.
6. Répétez les étapes 1 à 5 pour ajouter ce champ aux entités **Chiffre réel**, **Détail de la ligne de facture**, et **Ligne de journal**.
7. Répétez les étapes 1 à 6 du jeu d’options **Heures de travail des ressources**. 

> ![Ajout de l’emplacement de travail des ressources à Entrée de temps.](media/RWL-time-entry.png)

Cela termine les modifications de schéma requises pour les dimensions personnalisées basées sur un jeu d’options.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensions de tarification personnalisées basées sur une entité

Lorsque la dimension personnalisée de tarification est une entité, vous ajoutez une relation 1 à N entre l’entité de dimension et les entités principales. Avec l’exemple de titre standard ci-dessus, il est logique de prévoir que chaque employé se voit attribuer un titre standard. Par conséquent, vous devez disposer d’une relation 1 à N entre le Titre standard et la Ressource réservable, ou une relation N à 1, si elle a été créée entre la Ressource réservable et le Titre standard.

1. Dans Project Operations, sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Titre standard**.
3. Développez l’entité **Titre standard** et sélectionnez **Relation 1 à N**.
4. Cliquez sur **Nouveau** pour créer une Relation 1 à N appelée **Titre standard à Ressource réservable**. Entrez les informations requises, puis cliquez sur **Enregistrer**.

> ![Ajout de Titre standard en tant que champ de référence à Ressource réservable.](media/ST-BR.png)

Le Titre standard devra également être ajouté aux entités Tarification, **Prix du rôle** et **Majoration les prix de rôle**. Cette opération s’effectue également à l’aide de Relations 1 à N entre les entités **Titre standard** et **Prix du rôle** et les entités **Titre standard** et **Majoration du prix de rôle**.

1. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Titre standard**.
2. Développez l’entité **Titre standard** et sélectionnez **Relation 1 à N**.
3. Cliquez sur **Nouveau** pour créer une Relation 1 à N appelée **Titre standard à Prix du rôle**. Entrez les informations requises, puis cliquez sur **Enregistrer**.
4. Répétez les étapes 1 à 4 pour créer des relations 1 à N entre les entités **Titre standard** et **Majoration les prix de rôle**,

Dans les phases de ventes et d’estimation du projet, pour évaluer le devis/projet, des estimations de l’effort de travail sont requises pour chaque titre standard. Cela signifie que les relations 1 à N entre le Titre standard et chacune de ces entités d’estimation sont nécessaires : 

- **Détail de la ligne de devis**
- **Détail de la ligne de contrat du projet**
- **Membre de l’équipe du projet**
- **Ligne d’estimation**

5. Répétez les étapes 1 à 5 pour créer des relations 1 à N entre **Titre standard** et **Détail de la ligne de devis**, **Détail de la ligne de contrat du projet**, **Membre de l’équipe du projet**, et **Ligne d’estimation**.

> ![Ajout de Titre standard en tant que champ de référence à Ligne de devis.](media/ST-Estimate-Line.png)

  Au cours des phases de livraison et de facturation, le travail effectué par chaque titre standard doit être tarifé exactement dans les chiffres réels du projet. Cela signifie qu’il faut des relations 1 à N entre **Titre standard** et **Entrée de temps**, **Chiffre réel**, **Détail de la ligne de facture**, et **Entités de ligne du journal**.

6. Répétez les étapes 1 à 6 pour créer des relations 1 à N entre **Titre standard** et **Entrée de temps**, **Chiffre réel**, **Détail de la ligne de facture**, et **Entités de ligne du journal**.

> ![Ajout de Titre standard en tant que champ de référence dans Entrée de temps.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configuration de la valeur par défaut de Dimension à l’aide des fonctionnalités de mappages de la plateforme
Pour Entrée de temps, il est utile d’avoir la valeur système par défaut du titre standard sur l’Entrée de temps à partir de la Ressource réservable qui enregistre l’entrée de temps. Suivez les étapes ci-dessous pour ajouter des mappages de champs sur la relation 1 à N entre **Ressource pouvant être réservée** et **Entrée de temps**.

1. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Entités > Titre standard**.
2. Développez l’entité **Titre standard** et sélectionnez **Relation 1 à N**.
3. Double-cliquez sur **Ressource pouvant être réservée à Entrée de temps**. Dans la page **Relation**, cliquez sur **Utiliser les mappages de champs**. 
4. Cliquez sur **Nouveau** pour créer un mappage de champs entre le champ **Titre standard** sur l’entité **Ressource pouvant être réservée** et le champ de référence **Titre standard** sur l’entité **Entrée de temps**. 

> ![Configurer les mappages de champs pour permettre d’utiliser Titre standard comme valeur par défaut entre Ressource réservable et Entrée de temps.](media/ST-Mapping2.png)

Cela termine les modifications de schéma requises pour les dimensions personnalisées basées sur une entité.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Ajouter des champs personnalisés aux formulaires, aux vues et aux règles métier

Après avoir apporté toutes les modifications requises au schéma, l’étape suivante consiste à rendre les champs visibles dans l’interface utilisateur en ajoutant les champs aux formulaires et aux vues.

1. Ouvrez le formulaire ou la vue. Dans le volet de navigation droit, sélectionnez le champ et faites-le glisser sur le canevas de formulaire. 
2. Si vous modifiez une vue, utilisez le volet de navigation droit, cliquez sur **Ajouter des champs**, puis dans la boîte de dialogue **Liste des champs**, sélectionnez les champs dont vous avez besoin et cliquez sur **OK**.

Le tableau suivant fournit une liste complète des formulaires et vues prédéfinis, par entité, qui doivent être mis à jour avec les nouveaux champs. Si vous disposez de vues ou formulaires supplémentaires dans vos personnalisations de ces entités, ajoutez-y également les nouveaux champs.

| Entity        | Formulaires qui nécessitent le nouveau champ   |Vues qui nécessitent le nouveau champ      |
| ------------------------------|---------------------------------|----------------------------------|
|  Prix du rôle|• Informations |• Prix de la catégorie de ressource actifs<br> • Vue associée Prix de la catégorie de ressource|
|  Majoration du prix du rôle|• Informations|• Majorations du prix du rôle actives<br>• Vue associée Majoration du prix du rôle|
|  Détail de la ligne de devis|• Informations sur le projet<br>• Création rapide de projets|• Détail de la ligne de devis active<br>• Détails de la ligne de devis combinée<br>• Vue associée Détail de la ligne de devis|
|  Détail de la ligne de contrat du projet|• Informations sur le projet<br>• Création rapide de projets|• Détails de la ligne de contrat combinée<br>• Détails de la ligne de contrat active<br>• Vue associée aux détails de la ligne de contrat|
|  Membre de l’équipe du projet|• Informations<br>• Nouveau formulaire|• Membres de l’équipe du projet actifs<br>• Membres de l’équipe du projet<br>• Vue associée Membres de l’équipe du projet|
|  Entrée de temps|• Informations<br>• Créer une entrée de temps|• Mes entrées de temps par date<br>• Mes entrées de temps pour cette semaine<br>• Entrées des temps pour approbation|
|  Ligne de journal|• Informations<br>• Création rapide|• Lignes de journal actives<br>• Vue associée Ligne de journal|
|  Détail de la ligne de facture|• Informations<br>• Création rapide|• Détails de la ligne de facture active<br>• Transactions facturables<br>• Transactions gratuites<br>• Vue associée Détails de la ligne de facture<br>• Transactions non facturables|
|  Chiffre réel|• Informations<br>• Chiffres réels actifs|• Vue associée Chiffre réel|

Les champs personnalisés peuvent également être ajoutés aux règles métier selon ce que vous avez défini. Un exemple prêt à l’emploi concerne le **Caractère modifiable de l’entrée de temps basé sur le statut** de la règle métier. Cette règle définit les champs devant être verrouillés lorsque l’entrée de temps a un statut non modifiable, comme **Approuvé**. Ajoutez des champs à cette règle métier de sorte que les champs soient verrouillés en modification lorsque l’entrée de temps a un état autre que **Brouillon** ou **Renvoyé**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]