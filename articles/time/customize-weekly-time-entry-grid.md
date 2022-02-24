---
title: Développement des entrées de temps
description: Cette rubrique fournit des informations sur la façon dont les développeurs peuvent étendre le contrôle de saisie de l’heure.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d9c14f0550d4429ac794607a3fb61717566207e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124635"
---
# <a name="extending-time-entries"></a>Développement des entrées de temps

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend un contrôle personnalisé d’entrée de temps extensible. Ce contrôle comprend les fonctionnalités suivantes :

- Saisir l’heure horizontalement sur une semaine
- Totaux par jour, ligne ou semaine
- Copier des lignes ou des semaines
- Saisie de l’heure au format HH:mm ou HH.hh (convertit automatiquement en HH.hh)
- Importer à partir d’affectations, de réservations ou de rendez-vous

L’extension des entrées de temps est possible dans deux domaines :
- [Ajouter des entrées de temps personnalisées pour votre propre usage](#add)
- [Personnaliser le contrôle des entrées de temps hebdomadaires](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Ajouter des entrées de temps personnalisées pour votre propre usage

Les entrées de temps sont une entité principale utilisée dans plusieurs scénarios. En avril Wave 1 2020, la solution principale TESA a été introduite. TESA fournit une entité **Paramètres** et un nouveau rôle de sécurité **Utilisateur de saisie de temps**. Les nouveaux domaines, **msdyn_start** et **msdyn_end**, qui ont une relation directe avec **msdyn_duration**, ont également été inclus. Les nouveaux entité, rôle de sécurité et champs permettent une approche plus unifiée du temps pour plusieurs produits.


### <a name="time-source-entity"></a>Entité source de temps
| Champ | Description | 
|-------|------------|
| Nom   | Nom de l’entrée de source de temps utilisée comme valeur de sélection lors de la création des entrées de temps. |
| Source de temps par défaut [Source de temps : isdefault] | Par défaut, une seule source de temps peut être marquée par défaut. Cela permet aux entrées de se définir par défaut sur une source de temps si aucune n’est spécifiée. |
|Type de source de temps [Source de temps : sourcetype] | Le type de source est une option (Type de source d’entrée de temps) qui permet l’association de la source de temps à une application. Microsoft réserve des valeurs supérieures à 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entrées de temps et entité de source de temps
Chaque entrée de temps est associée à un enregistrement de source de temps. Cet enregistrement détermine comment et quelles applications doivent traiter l’entrée de temps.

Les entrées de temps sont toujours un bloc de temps contigu avec le début, la fin et la durée liés.

La logique mettra automatiquement à jour l’enregistrement de saisie de temps dans les situations suivantes :

- Si deux des trois champs suivants sont fournis, le troisième est calculé automatiquement : 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Les champs **msdyn_start** et **msdyn_end** sont dépendants du fuseau horaire.
- Les entrées de temps créées avec seulement **msdyn_date** et **msdyn_duration** spécifiés commenceront à minuit. Les champs **msdyn_start** et **msdyn_end** se mettront à jour en conséquence.

#### <a name="time-entry-types"></a>Types d’entrées de temps

Les enregistrements de saisie de temps ont un type associé qui définit le comportement dans le flux d’envoi pour l’application associée.

|Étiquette | valeur|
|-----|-----|
|En pause   |192,355,000|
|Déplacement | 192,355,001|
|Heures supplémentaires   | 192,354,320|
|Emploi   | 192,350,000|
|Absence    | 192,350,001|
|Vacances   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personnaliser le contrôle des entrées de temps hebdomadaire
Les développeurs peuvent ajouter des champs et des recherches supplémentaires à d’autres entités et implémenter des règles métier personnalisées pour prendre en charge leurs scénarios métier.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Ajouter des champs personnalisés avec des recherche à d’autres entités
Il existe trois grandes étapes pour ajouter un champ personnalisé à la grille d’entrée de temps hebdomadaire.

1. Ajouter le champ personnalisé à la boîte de dialogue de création rapide.
2. Configurer la grille pour afficher le champ personnalisé.
3. Ajouter le champ personnalisé au flux de tâches de modification de ligne ou au flux de tâches de modification de cellule.

Assurez-vous que le nouveau champ a les validations requises dans le flux de modification de ligne ou de cellule. Dans le cadre de cette étape, verrouillez le champ, selon le statut de l’entrée de temps.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Ajouter le champ personnalisé à la boîte de dialogue de création rapide
Ajoutez le champ personnalisé à la boîte de dialogue **Création rapide d’une entrée de temps**. Ensuite, lorsque les entrées de temps sont ajoutées, une valeur peut être saisie en sélectionnant **Nouveau**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurer la grille pour afficher le champ personnalisé
Vous pouvez ajouter un champ personnalisé à la grille d’entrée de temps hebdomadaire de deux façons :

  - Personnaliser une vue et ajouter un champ personnalisé
  - Créer une entrée de temps personnalisée par défaut 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Personnaliser une vue et ajouter un champ personnalisé

Personnaliser la vue **Mes entrées de temps hebdomadaires** et ajoutez-y le champ personnalisé. Vous pouvez choisir la position et la taille du champ personnalisé dans la grille en modifiant les propriétés dans la vue.

#### <a name="create-a-new-default-custom-time-entry"></a>Créer une entrée de temps personnalisée par défaut

Cette vue doit contenir les champs **Description** et **Commentaires externes**, en plus des colonnes que la grille doit contenir. 

1. Choisissez la position, la taille et l’ordre de tri par défaut de la grille en modifiant ces propriétés dans la vue. 
2. Configurez le contrôle personnalisé pour cette vue de manière à ce qu’il devienne un contrôle **Grille d’entrée de temps**. 
3. Ajoutez ce contrôle à la vue, puis sélectionnez-le pour le Web, le téléphone et la tablette. 
4. Configurez les paramètres de la grille d’entrée de temps hebdomadaire. 
5. Définissez le champ **Date de début** sur **msdyn_date**, définissez le champ **Durée** sur **msdyn_duration** et définissez le champ **Statut** sur **msdyn_entrystatus**. 
6. Pour la vue par défaut, le champ **Liste des statuts en lecture seule** est défini sur **192350002,192350003,192350004**. Le champ **Flux de tâches de modification de ligne** est défini sur **msdyn_timeentryrowedit**. Le champ **Flux de tâches de modification de cellule** est défini sur **msdyn_timeentryedit**. 
7. Vous pouvez personnaliser ces champs pour ajouter ou supprimer un statut en lecture seule, ou pour utiliser une autre expérience basée sur les tâches pour la modification de ligne ou de cellule. Ces champs sont désormais associés à une valeur statique.


> [!NOTE] 
> Les deux options suppriment certaines options de filtrage prédéfinies sur les entités **Projet** et **Tâche du projet**, afin que toutes les vues de recherche des entités soient visibles. Par défaut, seules les vues de recherche pertinentes sont visibles.

Déterminez le flux de tâches approprié pour le champ personnalisé. Si vous avez ajouté le champ à la grille, il doit apparaître dans le flux de tâches de modification de ligne qui est utilisé pour les champs s’appliquant à la ligne entière d’entrées du temps. Si le champ personnalisé a une valeur unique chaque jour, comme un champ personnalisé pour **Heure de fin**, il doit apparaître dans le flux de tâches de modification de cellule.

Pour ajouter le champ personnalisé à un flux de tâches, faites glisser un élément **Champ** vers la position appropriée sur la page, puis définissez les propriétés de champs. Définissez la propriété **Source** sur **Entrée de temps**, et définissez la propriété **Champ de données** sur le champ personnalisé. La propriété **Champ** spécifie le nom complet sur la page TBX. Sélectionnez **Appliquer** pour enregistrer vos modifications dans le champ, puis sélectionnez **Mettre à jour** pour enregistrer vos modifications sur la page.

Pour utiliser une nouvelle page TBX personnalisée, créez un nouveau processus. Définissez la catégorie sur **Flux des processus d’entreprise**, définissez l’entité sur **Entrée de temps** et définissez le type de processus d’entreprise sur **Exécuter le processus en tant que flux de tâches**. Sous **Propriétés**, la propriété **Nom de la page** doit être définie sur le nom complet de la page. Ajoutez tous les champs pertinents à la page TBX. Enregistrez et activez le processus. Mettez à jour la propriété de contrôle personnalisée pour le flux de tâches approprié sur la valeur **Nom** du processus.

### <a name="add-new-option-set-values"></a>Ajouter de nouvelles valeurs de groupe d’options
Pour ajouter des valeurs de groupe d’options à un champ prédéfini, ouvrez la page de modification du champ, et sous **Type**, sélectionnez **Modifier** en regard du groupe d’options. Ajoutez une nouvelle option qui a une étiquette et une couleur personnalisées. Pour ajouter un nouveau statut d’entrée de temps, le champ prédéfini est nommé **Statut de l’entrée**, et non **Statut**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Désigner un nouveau statut d’entrée de temps en lecture seule
Pour désigner un nouveau statut d’entrée de temps en lecture seule, ajoutez la nouvelle valeur d’entrée de temps à la propriété **Liste des statuts en lecture seule**. La partie modifiable de la grille d’entrée de temps est verrouillée pour les lignes présentant le nouveau statut.
Ensuite, ajoutez des règles métier pour verrouiller tous les champs des pages TBX **Modification de ligne d’entrée de temps** et **Modification d’entrée de temps**. Vous pouvez accéder aux règles métier de ces pages en ouvrant l’éditeur de flux des processus d’entreprise pour la page et en sélectionnant **Règles métier**. Vous pouvez ajouter le nouveau statut à la condition dans les règles métier existantes, ou vous pouvez ajouter une nouvelle règle métier pour le nouveau statut.

### <a name="add-custom-validation-rules"></a>Ajouter des règles de validation personnalisées
Il existe deux types de règles de validation que vous pouvez ajouter pour l’expérience de la grille d’entrée de temps hebdomadaire :

- Règles métier côté client qui fonctionnent dans les boîtes de dialogue de création rapide et sur les pages TBX.
- Validations de plug-in côté serveur qui s’appliquent à toutes les mises à jour des entrées de temps.

#### <a name="business-rules"></a>Règles d’entreprise
Utilisez les règles métier pour verrouiller et déverrouiller des champs, entrer des valeurs par défaut dans les champs et définir des validations qui nécessitent des informations uniquement de l’enregistrement d’entrée de temps en cours. Vous pouvez accéder aux règles métier d’une page TBX en ouvrant l’éditeur de flux des processus d’entreprise pour la page et en sélectionnant **Règles métier**. Vous pouvez ensuite modifier les règles métier existantes ou ajouter une nouvelle règle métier. Pour des validations encore plus personnalisées, vous pouvez utiliser une règle métier pour exécuter JavaScript.

#### <a name="plug-in-validations"></a>Validations de plug-in
Utilisez les validations de plug-in pour les validations nécessitant plus de contexte que celui disponible dans un enregistrement d’entrée de temps unique, ou pour les validations que vous souhaitez exécuter sur les mises à jour en ligne de la grille. Pour exécuter la validation, créez un plug-in personnalisé sur l’entité **Entrée de temps**.

### <a name="copying-time-entries"></a>Copie des entrées des temps
Utilisez la vue **Copier les colonnes de saisie de l’heure** pour définir la liste des champs à copier lors de la saisie de l’heure. **Date** et **Durée** sont des champs obligatoires et ne doivent pas être supprimés de la vue.
