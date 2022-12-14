---
title: Ajustements de projet
description: Cet article fournit des informations sur les ajustements de projet.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788297"
---
# <a name="project-adjustments"></a>Ajustements de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication_

## <a name="adjustments-overview"></a>Vue d’ensemble des ajustements

Vous pouvez configurer Microsoft Dynamics 365 Project Operations afin que les utilisateurs puissent apporter des modifications aux transactions publiées. Vous pouvez ajuster les transactions de projet une à une ou faire votre sélection de plusieurs transactions à partir d’une liste de toutes les transactions de projet. Les ajustements de projet sont utilisés, par exemple, pour mettre à jour en masse le statut facturable, recalculer le coût après un changement de configuration ou mettre à jour les sources de financement.

Les utilisateurs peuvent accéder à la fonctionnalité d’ajustement de projet de plusieurs manières :

- Avec la page **Ajuster les transactions** accessible depuis **Gestion de projet et comptabilité** \> **Configuration**.
- Avec le bouton **Ajustement** sur la page **Transactions de projet publiées** accessible depuis **Gestion de projet et comptabilité** \> **Transactions**.
- Avec le bouton **Ajustement** sur la page **Transactions de projet publiées** dans le contexte d’un projet. Cette page est accessible depuis **Gestion de projet et comptabilité** \> **Tous les projets**.

Pour permettre des ajustements, vous devez activer un ou plusieurs statuts de transaction depuis **Gestion de projet et comptabilité** \> **Paramètres de gestion de projet et de comptabilité** sur l’onglet **Général** sous la section **Autoriser l’ajustement du statut de la transaction**. Les exemples de statuts de transaction incluent les transactions validées, les transactions facturées ou les transactions éliminées. Tout statut de transaction défini sur **Non** indique des transactions qui n’apparaissent pas dans le processus d’ajustement comme sélectionnables pour l’ajustement.

Une option de configuration nommée **Toujours créer une transaction d’ajustement** est actuellement disponible dans les paramètres de gestion de projet et de comptabilité. Vous pouvez désactiver cette option pour mettre à jour la transaction d’origine au lieu de créer des transactions lors de l’ajustement dans un sous-ensemble de scénarios. Il a été annoncé que ce paramètre sera obsolète d’ici le 1er mars 2023. Après le 1er mars 2023, le système se comportera toujours comme si l’option était activée.

## <a name="adjustments-process-flow"></a>Flux de processus d’ajustements

Les étapes suivantes montrent le flux typique de traitement des ajustements.

1. Ouvrez la page **Ajustements du projet**.
2. Choisissez **Sélectionner** pour rechercher les transactions qui répondent aux critères d’ajustement attendus.
3. Dans la liste des transactions, sélectionnez toutes les transactions ou un sous-ensemble de transactions à ajuster.
4. Sélectionnez **Ajuster** et modifiez les attributs sur la ligne. À défaut, si les valeurs ont été spécifiées manuellement lors de la saisie de la transaction, vous pouvez choisir d’entrer les valeurs système par défaut.
5. La liste des transactions est renvoyée et une coche apparaît dans la colonne **Ajustement en attente** pour indiquer où les modifications ont été apportées. Tous les ajustements qui ont des modifications en attente sont affichés dans la moitié inférieure de la page. Là, vous pouvez apporter des modifications détaillées supplémentaires au-delà de ce qui a été affiché sur la page précédente.
6. Sélectionnez **Valider** pour valider les transactions d’ajustement.

Selon la configuration, de nouvelles transactions sont généralement créées pour l’ajustement.

- Le champ **Statut de la facture** de la transaction d’origine est défini sur **Ajusté**.
- Une transaction d’annulation est créée pour annuler la transaction d’origine, et le champ **Statut** est défini sur **Ajusté**.
- Une transaction est créée avec les modifications apportées au cours du processus d’ajustement.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Sélection de plusieurs transactions de projet publiées à la fois pour les ajustements et les notes de crédit

Une nouvelle fonctionnalité introduite dans la version 10.0.30 permet la sélection simultanée de plusieurs transactions à ajuster à partir de la page **Transactions de projet publiées**.

Avant de pouvoir utiliser cette fonctionnalité, vous devez l’activer dans votre système. Les administrateurs peuvent utiliser l’espace de travail **Gestion des fonctionnalités** pour vérifier le statut de la fonctionnalité et l’activer si nécessaire. Dans l’espace de travail **Gestion des fonctionnalités** , recherchez et sélectionnez **Sélection de plusieurs transactions de projet publiées à la fois pour les ajustements et les notes de crédit**, puis sélectionnez **Activer maintenant**.

Cette fonction active la fonctionnalité suivante :

- Elle est accessible à partir de la page de transaction publiée dans un projet en utilisant le bouton **Ajustement** existant.
- Elle active un contrôle de sélection multiligne sur la page **Transactions de projet publiées** . Vous pouvez appliquer des filtres à la page de liste et sélectionner vos enregistrements avant de commencer les ajustements.
- Elle désactive le bouton **Ajustement** si une seule transaction ne peut être ajustée, ou si vous sélectionnez une combinaison de notes de crédit et de journaux ensemble plutôt qu’individuellement.
- En raison de l’ajout du contrôle de sélection multi-lignes, le lien **Coût engagé** dans le ruban n’est plus désactivé si plusieurs lignes sont sélectionnées.
- Elle ajoute le message d’avertissement suivant : « Vous avez sélectionné plus de (nombre sélectionné) enregistrements à ajuster. Poursuivre cette action peut prendre un certain temps. Voulez-vous vraiment poursuivre cette action ? »

Cette fonctionnalité supprime également l’étape 2 du flux de processus décrit précédemment dans cet article. Par conséquent, toutes les transactions qui ont été sélectionnées avant l’ouverture de la page **Ajuster les transactions** seront incluses dans la liste des transactions à ajuster. Vous n’avez pas besoin d’utiliser le bouton **Sélectionner** pour les rechercher.

> [!NOTE] 
> Même si cette fonctionnalité est désactivée, vous pouvez toujours sélectionner plusieurs enregistrements à ajuster. Cependant, un seul enregistrement *reste sélectionné*, et la boîte de dialogue **Sélectionner les transactions** apparaît immédiatement après la sélection pour ouvrir les ajustements.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Statuts des transactions d’ajustement qui peuvent être activés ou désactivés pour les ajustements

Les statuts suivants peuvent être activés ou désactivés sur l’onglet **Général** de la page **Gestion de projet et paramètres comptables** :

- Publié
- Proposition de facture
- Facturé
- Estimation
- Éliminé
- Solde de début (heure)

## <a name="adjustment-parameters"></a>Paramètres d’ajustement

Ces paramètres sont répertoriés sur la page **Paramètres de gestion de projet et de comptabilité** sur l’onglet **Général** sous le groupe **Ajustement** et modifient le comportement du traitement des ajustements. 

| Nom du paramètre |  Description |
|----------------|-------------
| Toujours créer une transaction d’ajustement | Si ce paramètre est activé, le processus d’ajustement crée toujours une transaction d’annulation et une nouvelle transaction ajustée en cas d’impact financier ou de reporting. Si le paramètre est désactivé, le processus d’ajustement met à jour la transaction d’origine au lieu de créer une annulation et une transaction pour un scénario tel qu’une mise à jour du texte de la transaction. |
| Champ Mise à jour automatique | Si ce paramètre est activé, le système recalculera le prix de revient et le prix de vente. |
| Utiliser la date d’ajustement comme nouveau projet | Ce paramètre est utilisé pour déplacer les transactions dans un futur période fiscale avant que le système ne prenne en charge cette fonction. Nous vous déconseillons de l’utiliser, car il modifie la date ouvrable de la transaction et sera obsolète dans une prochaine version. |
| Autoriser les activités fermées | En règle générale, les transactions ne peuvent pas être créées pour les activités clôturées. Si ce paramètre est activé, ce comportement est remplacé. Par conséquent, des ajustements peuvent être créés pour les activités fermées. |
