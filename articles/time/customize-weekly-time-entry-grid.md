---
title: Développement des entrées de temps
description: Cette rubrique fournit des informations sur la façon dont les développeurs peuvent étendre le contrôle de saisie de l’heure.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582983"
---
# <a name="extending-time-entries"></a>Développement des entrées de temps

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations comprend un contrôle personnalisé d’entrée de temps extensible. Ce contrôle comprend les fonctionnalités suivantes :

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
| Nom  | Nom de l’entrée de source de temps utilisée comme valeur de sélection lors de la création des entrées de temps. |
| Source de temps par défaut [Source de temps : isdefault] | Par défaut, une seule source de temps peut être marquée par défaut. Cela permet aux entrées de se définir par défaut sur une source de temps si aucune n’est spécifiée. |
|Type de source de temps [Source de temps : sourcetype] | Le type de source est une option (Type de source d’entrée de temps) qui permet l’association de la source de temps à une application. Microsoft réserve des valeurs supérieures à 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entrées de temps et entité de source de temps
Chaque entrée de temps est associée à un enregistrement de source de temps. Cet enregistrement détermine quelles applications doivent traiter l’entrée de temps et comment.

Les entrées de temps sont toujours un bloc de temps contigu avec le début, la fin et la durée liés.

La logique mettra automatiquement à jour l’enregistrement de saisie de temps dans les situations suivantes :

- Si deux des trois champs suivants sont fournis, le troisième est calculé automatiquement : 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Les champs **msdyn_start** et **msdyn_end** sont sensibles au fuseau horaire.
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

1. Ajoutez le champ personnalisé à la boîte de dialogue **Création rapide**.
2. Configurer la grille pour afficher le champ personnalisé.
3. Ajoutez le champ personnalisé à la page **Modification de la ligne** ou **Modification de l’entrée de temps**, le cas échéant.

Veillez à ce que le nouveau champ ait les validations requises sur la page **Modification de la ligne** ou **Modification de l’entrée de temps**. Dans le cadre de cette tâche, verrouillez le champ, selon le statut de l’entrée de temps.

Lorsque vous ajoutez un champ personnalisé à la grille **Entrée du temps**, puis créez des entrées de temps directement dans la grille, le champ personnalisé pour ces entrées est automatiquement défini de sorte qu’il corresponde à la ligne. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Ajouter le champ personnalisé à la boîte de dialogue de création rapide
Ajoutez le champ personnalisé à la boîte de dialogue **Création rapide : créer une entrée de temps**. Les utilisateurs peuvent ensuite entrer une valeur lorsqu’ils ajoutent des entrées de temps en sélectionnant **Nouveau**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurer la grille pour afficher le champ personnalisé
Vous pouvez ajouter un champ personnalisé à la grille **Entrée de temps hebdomadaire** de deux façons.

- Personnalisez la vue **Mes entrées de temps hebdomadaires** et ajoutez-y le champ personnalisé. Vous pouvez spécifier la position et la taille du champ personnalisé dans la grille en modifiant ces propriétés dans la vue.
- Créez une vue d’entrée de temps personnalisée et à la définir comme vue par défaut. Cette vue doit contenir les champs **Description** et **Commentaires externes**, en plus des colonnes que la grille doit contenir. Vous pouvez préciser la position, la taille et l’ordre de tri par défaut de la grille en modifiant les propriétés dans la vue. Ensuite, configurez le contrôle personnalisé pour cette vue de manière à ce qu’il devienne un contrôle **Grille d’entrée de temps**. Ajoutez le contrôle à la vue, puis sélectionnez-le pour le **Web**, **Téléphone** et **Tablette**. Ensuite, configurez les paramètres de la grille **Entrée de temps hebdomadaire**. Définissez le champ **Date de début** sur **msdyn\_date**, définissez le champ **Durée** sur **msdyn\_duration** et définissez le champ **Statut** sur **msdyn\_entrystatus**. Le champ **Liste des statuts en lecture seule** est défini sur **192350002 (Approuvé)**, **192350003 (Envoyé)** ou **192350004 (Rappel demandé)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Ajouter un champ personnalisé à la page de modification appropriée
Les pages permettant de modifier une entrée de temps ou une ligne d’entrées de temps se trouvent sous **Formes**. Le bouton **Modifier l’entrée** dans la grille ouvre la page **Modifier l’entrée**, et le bouton **Modifier la ligne** ouvre la page **Modification de la ligne**. Vous pouvez modifier ces pages afin qu’elles incluent des champs personnalisés.

Les deux options suppriment certaines options de filtrage prédéfinies sur les entités **Projet** et **Tâche du projet**, afin que toutes les vues de recherche des entités soient visibles. Par défaut, seules les vues de recherche pertinentes sont visibles.

Vous devez déterminer la page appropriée pour le champ personnalisé. Très probablement, si vous avez ajouté le champ à la grille, il doit apparaître sur la page **Modification de la ligne** qui est utilisée pour les champs s’appliquant à la ligne entière d’entrées du temps. Si le champ personnalisé a une valeur unique dans la ligne chaque jour (par exemple, s’il s’agit d’un champ personnalisé pour l’heure de fin), il doit apparaître sur la page **Modification de l’entrée de temps**.

Pour ajouter le champ personnalisé à une page, faites glisser un élément **Champ** vers la position appropriée sur la page, puis définissez ses propriétés.

### <a name="add-new-option-set-values"></a>Ajouter de nouvelles valeurs de groupe d’options
Pour ajouter des valeurs de groupe d’options à un champ prêt à l’emploi, procédez comme suit.

1. Ouvrez la page de modification du champ, puis, sous **Type**, sélectionnez **Modifier** en regard du groupe d’options.
2. Ajoutez une nouvelle option qui a une étiquette et une couleur personnalisées. Pour ajouter un nouveau statut d’entrée de temps, le champ prédéfini est nommé **Statut de l’entrée**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Désigner un nouveau statut d’entrée de temps en lecture seule
Pour désigner un nouveau statut d’entrée de temps en lecture seule, ajoutez la nouvelle valeur d’entrée de temps à la propriété **Liste des statuts en lecture seule**. Assurez-vous d’ajouter le numéro, pas l’étiquette. La partie modifiable de la grille d’entrée de temps est maintenant verrouillée pour les lignes présentant le nouveau statut. Pour définir la propriété **Liste des statuts en lecture seule** différemment pour différentes vues **Entrée de temps**, ajoutez la grille **Entrée de temps** dans une section **Contrôles personnalisés** de la vue et configurez les paramètres comme il convient.

Ensuite, ajoutez des règles métier pour verrouiller tous les champs des pages **Modification de ligne** et **Modification d’entrée de temps**. Pour accéder aux règles métier de ces pages, ouvrez l’éditeur de formulaires pour chaque page et sélectionnez **Règles métier**. Vous pouvez ajouter le nouveau statut à la condition dans les règles métier existantes, ou vous pouvez ajouter une nouvelle règle métier pour le nouveau statut.

### <a name="add-custom-validation-rules"></a>Ajouter des règles de validation personnalisées
Vous pouvez ajouter deux types de règles de validation pour l’expérience de grille **Entrée de temps hebdomadaire** :

- Règles métier côté client qui fonctionnent sur les pages
- Validations de plug-in côté serveur qui s’appliquent à toutes les mises à jour des entrées de temps

#### <a name="client-side-business-rules"></a>Règles métier côté client
Utilisez les règles métier pour verrouiller et déverrouiller des champs, entrer des valeurs par défaut dans les champs et définir des validations qui nécessitent des informations uniquement de l’enregistrement d’entrée de temps en cours. Pour accéder aux règles métier d’une page, ouvrez l’éditeur de formulaires et sélectionnez **Règles métier**. Vous pouvez ensuite modifier les règles métier existantes ou ajouter une nouvelle règle métier.

#### <a name="server-side-plug-in-validations"></a>Validations de plug-ins côté serveur
Vous devez utiliser les validations de plug-in pour les validations nécessitant plus de contexte que celui disponible dans un enregistrement d’entrée de temps unique. Vous devez également les utiliser pour toutes les validations que vous souhaitez exécuter sur les mises à jour en ligne dans la grille. Pour exécuter les validations, créez un plug-in personnalisé sur l’entité **Entrée de temps**.

### <a name="limits"></a>Limites
Actuellement, la grille **Entrée de temps** a une limite de taille de 500 lignes. S’il y a plus de 500 lignes, les lignes excédentaires ne sont pas affichées. Il n’y a aucun moyen d’augmenter cette limite de taille.

### <a name="copying-time-entries"></a>Copie des entrées des temps
Utilisez la vue **Copier les colonnes de saisie de l’heure** pour définir la liste des champs à copier lors de la saisie de l’heure. **Date** et **Durée** sont des champs obligatoires et ne doivent pas être supprimés de la vue.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
