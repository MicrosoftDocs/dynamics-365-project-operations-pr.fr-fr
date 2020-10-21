---
title: Notes de frais réinventées
description: Cette rubrique fournit des informations sur l’expérience remodelée et repensée pour la saisie des notes de frais.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d415b9cc85bac91de8fb9427da290ae0c6108
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897133"
---
# <a name="expense-reports-reimagined"></a>Notes de frais réinventées

La saisie des notes de frais a été repensée pour simplifier le processus et réduire le temps nécessaire pour remplir une note. Voici les principaux éléments de la nouvelle expérience de dépenses :

- Un nouvel espace de travail de gestion des dépenses qui vous permet d’accéder aux dépenses de votre délégué.
- Une nouvelle expérience de rapprochement des reçus pour mieux afficher les reçus au niveau de l’en-tête et simplifier le processus de jonction des reçus aux lignes de dépenses.
- Une nouvelle grille en lecture seule qui vous permet d’afficher beaucoup plus de lignes de dépenses et de colonnes de données supplémentaires. Vous pouvez maintenant voir toutes les lignes détaillées et fractionnées, ainsi que leurs dépenses parents.
- Un volet simplifié pour la modification des dépenses.
- Messages d’erreur, d’avertissement et de stratégie repensés pour fournir le contexte et la compréhension appropriés du problème et comment le résoudre. Nous avons supprimé plusieurs des messages qui apparaissaient avant que les utilisateurs puissent terminer leurs tâches et résoudre les problèmes.
- Une nouvelle page pour spécifier les champs obligatoires, les champs facultatifs et les champs à ne pas inclure. Cette page permet de réduire le nombre de champs à définir.
- Un nouvel aspect pour les notes de frais, de sorte que celles-ci ne semblent plus avoir été conçues pour des comptables.

Pour activer la nouvelle expérience, utilisez l’espace de travail **Gestion des fonctionnalités** pour activer la fonctionnalité **Notes de frais réinventées**. Lorsque vous activez cette fonctionnalité, les actions suivantes se produisent :

- L’espace de travail des dépenses existant est remplacé par le nouvel espace de travail.
- Un nouvel élément de menu pour la visibilité des champs de dépenses est ajouté.
- Aucun élément de menu existant pour les notes de frais (la page existante) ou les champs de note de frais n’est supprimé.
- Les workflows et toutes les approbations vous dirigent toujours vers la page des notes de frais existantes.

## <a name="getting-started-video-for-new-users"></a>Vidéo de mise en route pour les nouveaux utilisateurs

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

La vidéo [Expérience de dépenses dans Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (ci-dessus) est incluse dans la [playlist Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) disponible sur YouTube.

## <a name="new-features"></a>Nouvelles fonctionnalités

| Nouvelle fonctionnalité | Description |
|---|----|
| Visibilité du champ Dépenses | Une nouvelle page de configuration vous permet de spécifier quels champs doivent être désactivés pour une organisation, quels champs doivent être obligatoires et quels champs sont recommandés. |
| Champs obligatoires | La nouvelle configuration simple vous permet de rendre certains champs obligatoires sans avoir à utiliser le cadre stratégique. |
| Champs facultatifs | Une deuxième page pour les champs facultatifs est ajoutée. De cette façon, les employés n’auront pas l’impression de devoir définir les champs, mais les champs sont toujours facilement accessibles. |
| Ajouter des reçus non joints | La possibilité d’ajouter des reçus non joints à la note de frais est plus visible depuis l’espace de travail et sur la note de frais. |
| Messagerie améliorée | Il y a une meilleure visibilité sur les lignes de dépenses qui contiennent des avertissements ou des erreurs. |
| Réduction des messages dans la barre de messages| Le nombre de messages Infolog a été réduit et un effort a été fait pour empêcher l’apparition de messages en double dans de nombreux cas. |
| Actions communes regroupées | L’interface a été nettoyée avec l’ajout d’un nouveau bouton d’actions pour la plupart des actions courantes au niveau de la ligne et l’ajout d’un bouton de sélection (...) pour l’en-tête et d’autres actions moins fréquentes. |
| Nouvel espace de travail pour augmenter la visibilité | Un nouvel espace de travail unifie les fonctionnalités et les liens qui permettent aux utilisateurs de se déplacer vers différentes zones. |
| Ajouter des dépenses et des reçus existants lors de la création des dépenses | Lorsque vous créez des notes de frais, vous pouvez ajouter la totalité ou une sélection de dépenses et de reçus. |
| Calculatrice de taux de change | Une calculatrice de taux de change est ajoutée qui vous permet de calculer le taux de change pour les transactions multidevises personnelles. |
| Enregistrer et ajouter de nouvelles lignes de dépenses | Les boutons **Enregistrer** et **Nouveau** sont disponibles lorsque de nouvelles dépenses sont saisies, pour vous aider à saisir rapidement des lignes de dépenses. |
| Meilleure visibilité sur les lignes fractionnées et détaillées | Des lignes détaillées et fractionnées sont ajoutées directement à la liste des dépenses pour augmenter la visibilité et vous aider à déterminer facilement s’il y a des erreurs. |
| Afficher les reçus lors de la répartition | Les reçus peuvent être affichés lors de la répartition. |

La version initiale se concentre sur les scénarios de saisie des dépenses. Tout scénario de vérification ou d’approbation des notes de frais continuera d’utiliser la page de saisie des dépenses existante.

Les fonctionnalités suivantes sont présentes sur la page existante mais ne sont pas encore présentes sur la nouvelle page. Ces fonctionnalités seront réintroduites au cours des prochaines versions :

- Approbations
- Approbations des comptes fournisseurs et possibilité de modifier la comptabilité
- Plusieurs points de saisie
- Intégration de la demande de déplacement
- Entité de données pour la visibilité des champs de dépenses
- Inscription pour les dépenses journalières
- Workflow au niveau de la ligne
- Prise en charge provisoire des approbateurs
- Répartition avancée
