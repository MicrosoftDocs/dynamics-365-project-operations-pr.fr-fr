---
title: Comportement de l’interface utilisateur de saisie de temps
description: Cette rubrique donne des informations sur le comportement de l’interface utilisateur de saisie de temps.
author: stsporen
manager: AnnBe
ms.date: 03/03/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b552266eddc4efc1b41fc500d157239388ad219b
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499611"
---
# <a name="time-entry-ui-behavior"></a>Comportement de l’interface utilisateur de saisie de temps

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


La grille **Entrée de temps hebdomadaire** est un contrôle personnalisé qui comporte deux sections principales, **Dimensions** et **Durée**.

## <a name="keyboard-shortcuts"></a>Raccourcis clavier
| Pour        | Raccourci                  |
|------------   |------------------------   |
| Nouveau           | Alt + Maj + n           |
| Copier la ligne      | Alt + Maj + c           |
| Modifier l’entrée    | Alt + Maj + e           |
| Modifier la ligne      | Alt + Maj + Ctrl + e    |
| Ouvrir l’entrée    | Alt + Maj + o           |
| Envoyer        | Alt + Maj + s           |
| Rappeler        | Alt + Maj + r           |
| Suppr        | Alt + Maj + d           |
| Copier la semaine     | Alt + Maj + w           |

## <a name="dimensions"></a>Dimensions
La section **Dimensions** affiche toutes les dimensions pour lesquelles le temps peut être entré. Les dimensions suivantes sont prises en charge par défaut :

  - Project
  - Tâche du projet
  - Rôle
  - Type
  - Statut de l’entrée

La section **Dimensions** n’autorise pas la modification intraligne. Cette section est étayée par une vue qui permet d’ajouter des champs personnalisés à la grille d’entrée de temps hebdomadaire.

## <a name="duration"></a>Durée
La section Durée affiche les jours de la semaine sous forme d’en-têtes de colonne. Cette section autorise la modification intraligne. Une fois qu’une ligne d’entrée de temps avec les dimensions appropriées est créée, les utilisateurs peuvent rapidement entrer le temps qu’ils ont consacré à ces dimensions.

## <a name="create-a-new-time-entry"></a>Créer une entrée de temps

1. Dans la grille des entrées de temps, sélectionnez **Nouveau**. 
2. Dans la boîte de dialogue **Création rapide de saisie de temps**, sélectionnez la date d’entrée de l’heure.
3. Entrez les données pour les dimensions **Projet**, **Tâche de projet**, **Rôle**, et **Durée**. Ces informations doivent être ajoutées en minutes, heures ou jours en tapant **h**, **m** ou **j** avec le nombre. 
4. Entrez une description pour la saisie et des commentaires qui peuvent être partagés en externe concernant l’entrée de temps. 

Lorsque vous enregistrez l’entrée, les valeurs saisies apparaissent dans la section **Dimensions**. Les informations entrées dans le champ **Durée** s’affichent à la date pour laquelle l’entrée de temps a été créée.

Les champs de recherche sont étayées par des vues système. Par exemple, une fois qu’un utilisateur active un projet, le champ **Tâche du projet** est défini sur la vue **Copier** par défaut. Pour créer des entrées de temps pour les tâches qui ne sont pas affectées à un utilisateur, sélectionnez **Modifier la vue** dans la boîte de dialogue de recherche, puis sélectionnez la vue **Toutes les tâches du projet actives**.

## <a name="edit-a-time-entry"></a>Modifier une entrée de temps 
Les détails de certains champs de la page d’entrée de temps, comme **Description** et **Commentaires externes**, ne sont pas affichés dans la grille d’entrée de temps hebdomadaire. À la place, un petit indicateur triangulaire apparaît dans les cellules **Durée** contenant ces détails supplémentaires. 

1. Pour modifier une entrée d’heure, sélectionnez la cellule que vous souhaitez mettre à jour dans l’entrée d’heure.
2. Sélectionnez **Modifier les détails** pour mettre à jour les données dans le volet **Formulaire principal de saisie de l’heure**. 

## <a name="copy-a-time-entry-row"></a>Copier une ligne d’entrée de temps
Une fois une ligne créée, sélectionnez **Copier la ligne** pour copier la ligne entière dans une nouvelle ligne. Lorsqu’une ligne est ainsi copiée, les dimensions et les durées sont également copiées. Sélectionnez également **Modifier la ligne** pour mettre à jour les valeurs de dimension et les durées dans la section **Durée**.

## <a name="open-a-time-entry-behavior"></a>Comportement Ouvrir une entrée de temps
Pour permettre une saisie optimale et rapide dans les champs les plus importants, la grille d’entrée de temps hebdomadaire affiche un sous-ensemble des dimensions et des durées sélectionnées. Pour afficher tous les détails d’une entrée de temps unique, sous **Modifier l’entrée**, sélectionnez **Ouvrir**.

## <a name="submit-a-time-entry"></a>Envoyer une entrée de temps
Envoyez une entrée de temps unique ou un groupe d’entrées de temps en sélectionnant un bloc de cellules ou une ligne entière d’entrées de temps, puis en sélectionnant **Envoyer**. Les entrées de temps envoyées s’affichent en tant qu’entrées en attente d’approbation sur la page **Approbation** des approbateurs. Une fois que les entrées de temps sont envoyées avec succès, elles ne peuvent pas être modifiées.

## <a name="recall-a-time-entry"></a>Rappeler une entrée de temps
Vous pouvez rappeler les entrées de temps que vous avez envoyées. Vous pouvez rappeler une entrée de temps unique, un bloc d’entrées du temps ou une ligne entière d’entrées du temps. Les entrées d’heure rappelées peuvent être modifiées.

## <a name="time-entry-status"></a>Statut de l’entrée de temps

- **Brouillon** : Le statut **Brouillon** est automatiquement affecté aux nouvelles entrées de temps. Seules les entrées de temps avec le statut **Brouillon** peuvent être supprimées.
- **Envoyé** : Lorsqu’une entrée de temps est envoyée, le statut est mis à jour sur **Envoyé**. 
- **Approuvé** : Lorsqu’une entrée de temps envoyée est approuvée, le statut est mis à jour sur **Approuvé**. 
- **Renvoyé** : Si une entrée de temps est rejetée, le statut est mis à jour sur **Renvoyé**, et l’entrée devient disponible pour correction et renvoi. 

## <a name="view-rejection-comments"></a>Afficher les commentaires de rejet
Lorsqu’une entrée de temps est rejetée par un approbateur, celui-ci peut ajouter des commentaires pour aider la ressource à comprendre la raison du rejet. Pour afficher les commentaires de rejet pour une entrée de temps, sélectionnez **Ouvrir l’entrée**. Les commentaires de rejet s’affichent dans la chronologie. L’utilisateur peut répondre aux commentaires de rejet avant de soumettre à nouveau l’entrée.

## <a name="copy-week"></a>Copier la semaine
Une fois que quelques entrées de temps ont été créées, les utilisateurs peuvent créer plusieurs entrées de temps en même temps.

1. Dans le formulaire **Entrées de temps**, sélectionnez **Copier la semaine** pour créer en bloc des entrées de temps supplémentaires. 
2. Dans la boîte de dialogue **Copier**, dans la section **À partir de la période**, utilisez les champs **Date de début** et **Date de fin** pour définir la plage de dates à partir de laquelle copier les entrées de temps. 
3. Dans la section **Vers la période**, dans le champ **Date de début**, spécifiez la date pour laquelle créer des entrées de temps. 
4. Cliquez sur **Copier**. Pour la date spécifiée dans la **période de fin**, une copie des entrées de temps pour le jour correspondant de la semaine dans la **période de début** est créée. Par exemple, l’entrée de temps du lundi de la semaine dernière est copiée dans le lundi de la semaine spécifiée comme **période de fin**.

## <a name="import"></a>Importation
Le même processus de base est utilisé pour importer des réservations, des affectations et des échanges. Vous pouvez spécifier la plage de dates des réservations à importer, puis sélectionner explicitement les réservations devant être copiées comme entrées de temps Brouillon. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
