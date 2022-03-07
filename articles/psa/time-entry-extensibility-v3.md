---
title: Personnaliser une entrée de temps hebdomadaire
description: Cette rubrique donne des informations sur la mise en œuvre de règles métier personnalisées qui prennent en charge les pratiques d’une organisation.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa2ef927e0234919ee4777f24c60569fb33a8570f6d48be6aef356df4f08a6e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002283"
---
# <a name="customize-weekly-time-entry"></a>Personnaliser une entrée de temps hebdomadaire 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dans Microsoft Dynamics 365 Project Service Automation version 3.3, Microsoft a introduit une grille moderne qui permet aux ressources du projet d’entrer rapidement le temps jusqu’à une semaine à la fois. La nouvelle grille d’entrée de temps hebdomadaire peut afficher les totaux des entrées par date, par ligne ou par semaine. Les ressources peuvent effectuer des copies des entrées de temps hebdomadaires et aussi effectuer une copie en bloc des semaines précédentes. Les personnalisateurs de système peuvent personnaliser la vue en ajoutant des champs, en ajoutant des champs de recherche à d’autres entités et en mettant en œuvre des règles métier personnalisées pour prendre en charge les pratiques de leur organisation.

La fonction d’entrée de temps et la nouvelle grille d’entrée de temps hebdomadaire sont accessibles par le biais du plan de site. L’expérience d’entrée de temps personnalisée non extensible qui faisait partie des versions PSA précédentes a été remplacée par la grille d’entrée de temps hebdomadaire extensible, ainsi que par une expérience alternative dans la grille et le calendrier en lecture seule. En raison de ce changement, les utilisateurs peuvent entrer le temps en quantités hebdomadaires.

## <a name="page-layout"></a>Mise en page
La nouvelle grille d’entrée de temps hebdomadaire est un contrôle personnalisé qui comporte une barre d’outils et deux sections principales, **Dimensions** et **Durée**. La barre d’outils comprend un bouton qui s’applique uniquement à ce contrôle personnalisé pour la grille d’entrée de temps. En revanche, les boutons du volet Actions en haut de la page s’appliquent aux trois types de contrôles pris en charge pour l’entrée de temps : le contrôle d’entrée de temps hebdomadaire, le contrôle en lecture seule et le contrôle Calendrier.

### <a name="dimensions"></a>Dimensions
La section **Dimensions** affiche, sous forme d’en-têtes de colonne, toutes les dimensions pour lesquelles le temps peut être entré. Les dimensions suivantes sont prises en charge par défaut :

- Projet
- Tâche du projet
- Rôle
- Type
- Statut de l’entrée

La section **Dimensions** n’autorise pas la modification intraligne. Cette section est étayée par une vue qui permet d’ajouter des champs personnalisés à la grille d’entrée de temps hebdomadaire. Pour plus d’informations sur l’ajout de champs personnalisés, consultez la section « Extensibilité » plus loin dans cette rubrique.

### <a name="duration"></a>Durée
La section Durée affiche les jours de la semaine sous forme d’en-têtes de colonne. Cette section autorise la modification intraligne. Une fois qu’une ligne d’entrée de temps avec les dimensions appropriées est créée, les utilisateurs peuvent rapidement entrer, en ligne, le temps qu’ils ont consacré à ces dimensions.

## <a name="create-a-new-time-entry"></a>Créer une entrée de temps
Pour créer une entrée de temps dans la grille d’entrée de temps, sélectionnez **Nouveau**. La boîte de dialogue **Création rapide d’une entrée de temps** s’affiche. Dans cette boîte de dialogue, les utilisateurs peuvent sélectionner la date d’entrée de temps, puis entrer des données pour les dimensions **Projet**, **Tâche du projet**, **Rôle** et **Durée** en minutes, heures ou jours en saisissant **h**, **m** ou **j**, ainsi que le nombre. Les utilisateurs peuvent également entrer une description et des commentaires qui peuvent être partagés en externe pour l’entrée de temps. Lorsque les utilisateurs enregistrent leurs modifications, les valeurs qu’ils ont entrées pour les dimensions s’affichent dans la section **Dimensions**. Les informations de durée qu’ils ont entrées dans le champ **Durée** s’affichent à la date pour laquelle l’entrée de temps a été créée.

Les champs de recherche sont soutenus par des vues système. Par exemple, après qu’un utilisateur a saisi un projet, le champ **Tâche du projet** est défini sur la vue **Copie** par défaut. Pour créer des entrées de temps pour les tâches qui ne sont pas affectées à un utilisateur, sélectionnez **Modifier la vue** dans la boîte de dialogue de recherche, puis sélectionnez la vue **Toutes les tâches du projet actives**.

## <a name="edit-a-time-entry"></a>Modifier une entrée de temps
Les détails de certains champs de la page d’entrée de temps, comme **Description** et **Commentaires externes**, ne sont pas affichés dans la grille d’entrée de temps hebdomadaire. À la place, un petit indicateur triangulaire apparaît dans les cellules de durée contenant ces détails supplémentaires. Sélectionnez la cellule, puis sélectionnez **Modifier les détails** pour afficher les données dans le volet **Modification rapide**. Pour modifier ou mettre à jour les détails d’une entrée de temps spécifique qui ne fait pas partie de la grille d’entrée de temps hebdomadaire, les utilisateurs doivent ouvrir le volet **Modification rapide**.

## <a name="copy-a-time-entry-row"></a>Copier une ligne d’entrée de temps
Une fois qu’une ligne d’entrée a été créée pour la première fois, les utilisateurs peuvent sélectionner **Copier la ligne** pour copier la ligne entière dans une nouvelle ligne. Lorsqu’une ligne est ainsi copiée, les dimensions et les durées sont également copiées. Les utilisateurs peuvent également sélectionner **Modifier la ligne** pour mettre à jour les valeurs de dimension et les durées en ligne dans la section **Durée**.

## <a name="open-a-time-entry"></a>Ouvrir une entrée de temps
Pour permettre une saisie optimale et rapide dans les champs les plus importants, la grille d’entrée de temps hebdomadaire affiche un sous-ensemble des dimensions et des durées sélectionnées. Pour afficher tous les détails d’une entrée de temps unique, sous **Modifier l’entrée**, sélectionnez **Ouvrir**.

## <a name="submit-a-time-entry"></a>Envoyer une entrée de temps
Les utilisateurs peuvent envoyer une entrée de temps unique ou un groupe d’entrées de temps en sélectionnant un bloc de cellules ou une ligne entière d’entrées de temps, puis en sélectionnant **Envoyer**. Les entrées de temps envoyées s’affichent en tant qu’entrées en attente d’approbation sur la page **Approbation** des approbateurs. Une fois que les entrées de temps sont envoyées avec succès, elles ne peuvent pas être modifiées.

## <a name="recall-a-time-entry"></a>Rappeler une entrée de temps
Vous pouvez rappeler les entrées de temps que vous avez envoyées. Vous pouvez rappeler une entrée de temps unique, un bloc d’entrées du temps ou une ligne entière d’entrées du temps. Les entrées de temps rappelées peuvent être modifiées par les ressources.

## <a name="time-entry-status"></a>Statut de l’entrée de temps
Le statut **Brouillon** est automatiquement affecté aux nouvelles entrées de temps. Lorsqu’une entrée de temps est envoyée, le statut est mis à jour sur **Envoyé**. Lorsqu’une entrée de temps envoyée est approuvée, le statut est mis à jour sur **Approuvé**. Si une entrée de temps est rejetée, le statut est mis à jour sur **Renvoyé**, et l’entrée devient disponible pour correction et renvoi. Seules les entrées de temps avec le statut **Brouillon** peuvent être supprimées.

## <a name="view-rejection-comments"></a>Afficher les commentaires de rejet
Lorsqu’une entrée de temps est rejetée par un approbateur, celui-ci peut ajouter des commentaires de rejet pour aider la ressource à comprendre la raison du rejet. Pour afficher les commentaires de rejet pour une entrée de temps, sélectionnez **Ouvrir l’entrée**. Les commentaires de rejet s’affichent dans la chronologie. Dans la chronologie, la ressource peut répondre aux commentaires de rejet avant de renvoyer l’entrée.

## <a name="copy-week"></a>Copier la semaine
Après avoir créé quelques entrées de temps, les utilisateurs peuvent sélectionner **Copier la semaine** pour créer des entrées de temps supplémentaires en bloc. La boîte de dialogue **Copier** s’affiche. Dans la section **À partir de la période**, utilisez les champs **Date de début** et **Date de fin** pour définir la plage de dates à partir de laquelle copier les entrées de temps. Dans la section **Vers la période**, dans le champ **Date de début**, spécifiez la date pour laquelle créer des entrées de temps. Sélectionnez ensuite **Copier**. Pour la date spécifiée dans la période de fin, une copie des entrées de temps pour le jour correspondant de la semaine dans la période de début est créée. Par exemple, l’entrée de temps du lundi de la semaine dernière est copiée dans le lundi de la semaine spécifiée comme période de fin.

## <a name="import"></a>Importer
Le même processus de base est utilisé pour importer des réservations, des affectations et des échanges. Les utilisateurs peuvent spécifier la plage de dates à partir de laquelle les réservations sont importées. Ils doivent ensuite explicitement sélectionner les réservations qui doivent être copiées dans les entrées de temps brouillon. Dans la version précédente, les entrées de temps suggérées s’affichaient dans la grille et le calendrier, et étaient perdues au moment de l’actualisation de la session.

## <a name="extensibility"></a>Extensibilité
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Ajouter des champs personnalisés comportant des champs de recherche à d’autres entités
Il existe trois grandes étapes pour ajouter un champ personnalisé à la grille d’entrée de temps hebdomadaire.

1.  Ajouter le champ personnalisé à la boîte de dialogue de création rapide.
2.  Configurer la grille pour afficher le champ personnalisé.
3.  Ajouter le champ personnalisé au flux de tâches de modification de ligne ou au flux de tâches de modification de cellule, si nécessaire.

Vous devez également vous assurer que le nouveau champ a les validations requises dans le flux de modification de ligne ou de cellule. Dans le cadre de cette étape, vous devez verrouiller le champ, selon le statut de l’entrée de temps.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Ajouter le champ personnalisé à la boîte de dialogue de création rapide
Vous devez ajouter le champ personnalisé à la boîte de dialogue Création rapide d’une entrée de temps afin que les utilisateurs puissent entrer une valeur lorsqu’ils ajoutent des entrées de temps à l’aide du bouton **Nouveau**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurer la grille pour afficher le champ personnalisé
Vous pouvez ajouter un champ personnalisé à la grille d’entrée de temps hebdomadaire de deux façons. La première option consiste à personnaliser la vue **Mes entrées de temps hebdomadaires** et à y ajouter le champ personnalisé. Vous pouvez choisir la position et la taille du champ personnalisé dans la grille en modifiant ces propriétés dans la vue.

La seconde option consiste à créer une nouvelle vue d’entrée de temps personnalisée et à la définir comme vue par défaut. Cette vue doit contenir les champs **Description** et **Commentaires externes**, en plus des colonnes que la grille doit contenir. Vous pouvez choisir la position, la taille et l’ordre de tri par défaut de la grille en modifiant ces propriétés dans la vue. Ensuite, configurez le contrôle personnalisé pour cette vue de manière à ce qu’il devienne un contrôle **Grille d’entrée de temps**. Ajoutez ce contrôle à la vue, puis sélectionnez-le pour le Web, le téléphone et la tablette. Ensuite, configurez les paramètres de la grille d’entrée de temps hebdomadaire. Définissez le champ **Date de début** sur **msdyn_date**, définissez le champ **Durée** sur **msdyn_duration** et définissez le champ **Statut** sur **msdyn_entrystatus**. Pour la vue par défaut, le champ **Liste des statuts en lecture seule** est défini sur **192350002,192350003,192350004**, le champ **Flux de tâches de modification de ligne** est défini sur **msdyn_timeentryrowedit** et le champ **Flux de tâches de modification de cellule** est défini sur **msdyn_timeentryedit**. Vous pouvez personnaliser ces champs pour ajouter ou supprimer un statut en lecture seule, ou pour utiliser une autre expérience basée sur les tâches pour la modification de ligne ou de cellule. Ces champs doivent être associés à une valeur statique.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Ajouter un champ personnalisé au flux de tâches de modification approprié
Les pages TBX utilisées pour la modification se trouvent sous **Processus**. Les pages par défaut sont **Project Service - Modification de ligne d’entrée de temps** et **Project Service - Modification d’entrée de temps**. Vous pouvez modifier ces pages par défaut ou créer des pages TBX personnalisées.

> [!NOTE] 
> Les deux options suppriment certaines options de filtrage prédéfinies sur les entités **Projet** et **Tâche du projet**, afin que toutes les vues de recherche des entités soient visibles. Par défaut, seules les vues de recherche pertinentes sont visibles.

Vous devez déterminer le flux de tâches approprié pour le champ personnalisé. Très probablement, si vous avez ajouté le champ à la grille, il doit apparaître dans le flux de tâches de modification de ligne qui est utilisé pour les champs s’appliquant à la ligne entière d’entrées du temps. Si le champ personnalisé a une valeur unique chaque jour, comme un champ personnalisé pour **Heure de fin**, il doit apparaître dans le flux de tâches de modification de cellule.

Pour ajouter le champ personnalisé à un flux de tâches, faites glisser un élément **Champ** vers la position appropriée sur la page, puis définissez ses propriétés. Définissez la propriété **Source** sur **Entrée de temps**, et définissez la propriété **Champ de données** sur le champ personnalisé. La propriété **Champ** spécifie le nom complet sur la page TBX. Sélectionnez **Appliquer** pour enregistrer vos modifications du champ. Sélectionnez ensuite **Mettre à jour** pour enregistrer vos modifications de la page.

Pour utiliser une nouvelle page TBX personnalisée, créez un nouveau processus. Définissez la catégorie sur **Flux des processus d’entreprise**, définissez l’entité sur **Entrée de temps** et définissez le type de processus d’entreprise sur **Exécuter le processus en tant que flux de tâches**. Sous **Propriétés**, la propriété **Nom de la page** doit être définie sur le nom complet de la page. Ajoutez tous les champs pertinents à la page TBX. Enregistrez et activez le processus, puis mettez à jour la propriété de contrôle personnalisée pour le flux de tâches approprié sur la valeur **Nom** du processus.

### <a name="add-new-option-set-values"></a>Ajouter de nouvelles valeurs de groupe d’options
Pour ajouter des valeurs de groupe d’options à un champ prédéfini, ouvrez la page de modification du champ, puis, sous **Type**, sélectionnez **Modifier** en regard du groupe d’options. Ensuite, ajoutez une nouvelle option qui a une étiquette et une couleur personnalisées. Pour ajouter un nouveau statut d’entrée de temps, le champ prédéfini est nommé **Statut de l’entrée**, et non **Statut**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Désigner un nouveau statut d’entrée de temps en lecture seule
Pour désigner un nouveau statut d’entrée de temps en lecture seule, ajoutez la nouvelle valeur d’entrée de temps (le nombre, et non le libellé) à la propriété **Liste des statuts en lecture seule**. La partie modifiable de la grille d’entrée de temps est verrouillée pour les lignes présentant le nouveau statut.
Ensuite, ajoutez des règles métier pour verrouiller tous les champs des pages TBX **Modification de ligne d’entrée de temps** et **Modification d’entrée de temps**. Vous pouvez accéder aux règles métier de ces pages en ouvrant l’éditeur de flux des processus d’entreprise pour la page et en sélectionnant **Règles métier**. Vous pouvez ajouter le nouveau statut à la condition dans les règles métier existantes, ou vous pouvez ajouter une nouvelle règle métier pour le nouveau statut.

### <a name="add-custom-validation-rules"></a>Ajouter des règles de validation personnalisées
Deux types de règles de validation peuvent être ajoutées pour l’expérience de grille d’entrée de temps hebdomadaire : •   Règles métier côté client qui fonctionnent dans les boîtes de dialogue de création rapide et dans les pages TBX •   Validations de plug-in côté serveur qui s’appliquent à toutes les mises à jour d’entrée de temps

#### <a name="business-rules"></a>Règles métier
Utilisez les règles métier pour verrouiller et déverrouiller des champs, entrer des valeurs par défaut dans les champs et définir des validations qui nécessitent des informations uniquement de l’enregistrement d’entrée de temps en cours. Vous pouvez accéder aux règles métier d’une page TBX en ouvrant l’éditeur de flux des processus d’entreprise pour la page et en sélectionnant **Règles métier**. Vous pouvez ensuite modifier les règles métier existantes ou ajouter une nouvelle règle métier. Pour des validations encore plus personnalisées, vous pouvez utiliser une règle métier pour exécuter JavaScript.

#### <a name="plug-in-validations"></a>Validations de plug-in
Vous devez utiliser les validations de plug-in pour les validations nécessitant plus de contexte que celui disponible dans un enregistrement d’entrée de temps unique, ou pour les validations que vous souhaitez exécuter sur les mises à jour en ligne de la grille. Pour exécuter la validation, créez un plug-in personnalisé sur l’entité **Entrée de temps**.

> [!IMPORTANT] 
> Actuellement, un problème connu sur les pages de TBX empêche les utilisateurs de corriger les informations et de resélectionner Terminé en cas d’échec de la mise à jour d’une validation de plug-in. Une solution de contournement consiste à configurer les validations de règle métier pour éviter cette situation autant que possible.


[!INCLUDE[footer-include](../includes/footer-banner.md)]