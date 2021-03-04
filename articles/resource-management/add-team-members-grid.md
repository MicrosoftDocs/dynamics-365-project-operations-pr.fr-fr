---
title: Ajouter des membres de l’équipe depuis la grille des membres de l’équipe
description: Cette rubrique fournit des informations sur la façon dont vous pouvez gérer les ressources des membres de l’équipe.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: de73dac28046ec98ed201e129be6511f894223fd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121530"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Ajouter des membres de l’équipe depuis la grille des membres de l’équipe

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations contient un tableau de bord Resource Manager qui fournit une vue d’ensemble visuelle de la demande et de l’utilisation des ressources dans toute l’organisation. Vous pouvez utiliser les graphiques de ce tableau de bord pour visualiser les informations suivantes :

- **Demande de ressource** : Le graphique **Demande de ressource active** présente les ressources qui ont été envoyés. Les ressources sont regroupées par rôle ou par projet.
- **Demande de ressource non envoyée** : Le graphique **Demande de ressource non attribuée** affiche tous les besoins en ressources qui n’ont pas été envoyés. Ce graphique permet aux gestionnaires de ressources d’afficher la demande qui n’est pas ferme et peut être transmise via une demande de ressource.
- **Utilisation facturable pour la semaine dernière** : Le graphique **Utilisation par rôle** affiche le pourcentage d’utilisation facturable réelle de l’organisation par rôle par rapport à l’utilisation facturable cible par rôle.

    > [!NOTE]
    > Pour rendre le graphique **Utilisation par rôle** disponibles, créez une tâche qui exécute le workflow **UpdateRoleUtilization**. Cette tâche périodique exécute tous les sept jours calculer l’utilisation facturable pour les sept jours précédents. Les résultats sont regroupés par rôle.

## <a name="manage-project-team-members"></a>Gérer les membres de l’équipe du projet

Les responsables de projet peuvent utiliser le tableau de bord Resource Manager pour gérer les ressources dans des projets. Par exemple, ils peuvent ajouter un membre de l’équipe directement au projet et réserver un membre de l’équipe pour combler les besoins en ressources capturés par une ressource générique.

### <a name="add-a-team-member-directly-to-a-project"></a>Ajouter un membre d’équipe directement au projet

Pour ajouter un membre de l’équipe directement au projet, sur le formulaire **Projets**, dans l’onglet **Équipe**, sélectionnez **Nouveau**. La boîte de dialogue **Création rapide : Membre de l’équipe du projet** apparaît. Dans cette boîte de dialogue, vous pouvez effectuer ces tâches :

- **Réserver une ressource nommée** : Dans le champ **Ressource pouvant être réservée**, sélectionnez le nom de la ressource. Puis sélectionnez le rôle, définissez la période, puis sélectionnez une méthode de répartition. La ressource nommée sélectionnée est ajoutée au projet en utilisant la méthode sélectionnée de répartition et le calendrier de ressources.
- **Ajouter une ressource générique** : Laissez le champ **Ressource pouvant être réservée** vide, puis sélectionnez le rôle, définissez la période, puis la méthode privilégiée de répartition. Une ressource générique est ajoutée à l’équipe en tant qu’espace réservé. L’espace réservé contient le modèle de demande utilisé pour réserver des ressources nommées dans l’équipe. Le besoin est créé selon le calendrier de projet.
- **Ajouter une ressource nommée à l’équipe sans consommer la capacité de ressource** : Dans le champ **Ressource pouvant être réservée**, sélectionnez une ressource. Sélectionnez la période, puis **Aucun** comme méthode de répartition. La ressource est ajoutée à l’équipe, mais la capacité de la ressource n’est pas consommée via une réservation.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Réserver un membre de l’équipe pour satisfaire aux besoins en ressources pour une ressource générique

Dans Project Operations, vous pouvez réserver une ressource générique dans une équipe de projet. Vous pouvez également spécifier le rôle, la capacité requise et la manière dont cette capacité est répartie. Pour le besoin en ressources, vous pouvez spécifier des attributs associés à la ressource générique. Ces attributs incluent les compétences requises, l’unité d’organisation privilégiée, et les ressources préférées.

Effectuez les étapes suivantes pour spécifier les compétences requises sur une ressource générique pour un développeur.

1. Sur le formulaire **Projets**, dans l’onglet **Équipe**, sélectionnez **Nouveau** pour réserver une ressource générique.
2. Dans la vue **Tous les membres de l’équipe**, dans la colonne **Besoin en ressources**, sélectionnez le lien pour ajouter des compétences requises pour la ressource générique.
3. Sur le formulaire **Besoin en ressources**, dans la grille **Qualifications**, sélectionnez les points de suspension (**...**) puis sélectionnez **Ajouter la nouvelle caractéristique du besoin** pour ajouter les compétences requises pour votre développeur.
4. Sur le formulaire de la boîte de dialogue **Création rapide : Caractéristique du besoin**, dans le champ **Caractéristique**, sélectionnez la qualification requise.
5. Dans le champ **Valeur d’évaluation**, sélectionnez le niveau de qualification pour cette compétence. 
6. Dans le champ **Besoin en ressources**, définissez le besoin en ressources sources à partir des unités d’organisation ou même de ressources nommées. Lorsque vous avez terminé, sélectionnez **Enregistrer**.
7. Sur le formulaire **Besoin en ressources**, sélectionnez **Réserver** pour satisfaire le besoin en ressources. Vous pouvez également sélectionner la ressource générique dans la grille **Tous les membres de l’équipe** puis sélectionner **Réserver**.

    > [!NOTE]
    > Dans cet exemple, il y a 40 heures requises mais aucun heure réservée réellement, car les ressources génériques ne disposent pas de réservations. En outre, il n’existe aucune heure attribuée, car la ressource générique a été ajoutée directement à l’équipe, plutôt que d’être ajoutée à l’aide d’une attribution de tâche.

    Sur le formulaire **Assistant Planifier**, vous pouvez filtrer les ressources disponibles par les besoins spécifiés sur le besoin en ressources. Les ressources sont triées en fonction des paramètres de tri spécifiés sur le tableau de planification.

   Voici quelques-uns des filtres les plus couramment utilisés :

    - **Caractéristiques avec une évaluation** : Filtrez par compétences, certifications, et autres qualités de ressource, en plus des évaluations de compétences.
    - **Rôles** : Filtrez par les rôles par défaut qui sont affectés aux ressources pouvant être réservées.
    - **Unité d’organisation** : Filtrez les ressources pouvant être réservées par les unités d’organisation auxquelles elles sont attribuées.

8. Si les résultats de la recherche de besoin d’origine ne vous conviennent pas, vous pouvez modifier les critères de filtre. Développez le volet **Vue de filtre** de gauche, puis sélectionnez **Rechercher** pour trouver des ressources supplémentaires. Pour modifier la façon dont les résultats sont triés, sélectionnez **Trier**.
9. Sélectionnez les ressources en fonction de la demande spécifiée sur le besoin, comme indiqué en haut de la grille. Vous pouvez désactiver la sélection des cellules dans la grille et laisser cette capacité de ressource ouverte. Une seule ressource à la fois peut être sélectionnée comme réservée.
10. Sélectionnez **Réserver** pour réserver la ressource sélectionnée et laissez le Tableau de planification ouvert, de sorte à sélectionner des ressources supplémentaires. Par ailleurs, sélectionnez **Réserver et quitter** pour réserver la ressource sélectionnée et fermez le tableau de planification.
11. Revenez à la vue **Tous les membres de l’équipe**. Dans la grille, notez que la ressource générique a été remplacée par la ressource nommée, et 40 heures sont répertoriées comme réservées pour cette ressource.

    > [!NOTE]
    > Aucune heure affectée n’est affichée, car elles ont été réservées directement sur l’équipe. Elles n’ont pas été réservées à l’aide de l’affectation des tâches.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Attribuez des ressources génériques aux tâches et générez des besoins en ressources

Dans Project Operations, vous pouvez créer des tâches puis leur attribuer des ressources génériques. La demande de ressource peut ensuite être représentée par des espaces réservés, pendant que vous estimez votre planification et les chiffres financiers. Vous pouvez ensuite générer des besoins en ressources pour les ressources génériques et les mener à bien.

1. Sur le formulaire **Projets**, dans l’onglet **Planification**, sélectionnez **Ajouter** pour créer une tâche.
2. Dans le champ **Ressources**, sélectionnez le symbole **Sélecteur de ressources**. Le sélecteur de ressources s’affiche et affiche les membres de l’équipe existants du projet.
3. Entrez le nom de la ressource générique, puis sélectionnez **Créer**.
4. Dans la boîte de dialogue **Création rapide : Membre de l’équipe du projet** qui s’affiche, dans le champ **Rôle**, sélectionnez le rôle pour la ressource générique. 
5. Dans le champ **Unité d’allocation des ressources**, sélectionnez l’unité d’organisation pour la ressource générique. Sélectionnez ensuite **Enregistrer**. Le membre de l’équipe générique est maintenant attribué à la tâche.

   Dans l’onglet **Équipe**, vous verrez le nouveau membre de l’équipe générique. Notez qu’il a uniquement des heures affectées. Ces heures sont la somme de toutes les tâches qui sont affectées au membre de l’équipe générique. Le membre de l’équipe générique n’a pas les heures requises ou de besoin en ressources.

6. Vous pouvez désormais affecter le membre de l’équipe générique à d’autres tâches en utilisant le Sélecteur de ressources.

   Lorsque vous avez terminé d’affecter la ressource générique aux tâches, vous pouvez générer un besoin en ressources pour la ressource générique.

7. Dans l’onglet **Équipe**, sélectionnez la ressource générique, puis sélectionnez **Générer un besoin**. Lorsque le besoin est généré, le membre de l’équipe générique aura des heures requises et un lien pour le besoin en ressources.

  Une fois que vous avez réservé une ressource nommée, la ressource générique est supprimée de l’équipe et remplacée par la ressource nommée. Dans l’onglet **Planification**, les affectations des ressources génériques sont supprimées et remplacées par la ressource nommée.

  > [!NOTE]
  > Ceci se produit uniquement lorsque la ressource nommée est entièrement réservée pour ce besoin en ressources générique. Lorsqu’une ou plusieurs ressources nommées remplacent partiellement ou entièrement, respectivement, le besoin en ressources générique, la ressource générique reste affectée à la tâche.

Project Operations n’attribue pas les deux ressources à la tâche, car ce comportement produirait une planification moins prévisible. Dans cet exemple simple, il est facile de répartir les heures également entre deux ressources. Toutefois, dans les scénarios plus complexes qui impliquent plusieurs tâches et des ressources multiples, PSA doit faire des hypothèses sur la manière dont elle doit affecter les réservations qui sont reçues pour plusieurs ressources et plusieurs tâches.

Par conséquent, dans les scénarios suivants, le chef de projet est responsable d’analyser plusieurs réservations et de les affecter en conséquence. Pour affecter les réservations, le chef de projet attribue les tâches des ressources génériques aux ressources nommées puis utilise la vue **Rapprochement** pour s’assurer que la répartition fonctionne avec les réservations.

### <a name="edit-a-resource-requirement"></a>Modifier un besoin en ressources

Lorsqu’un besoin en ressources a été créé, un chef de projet ou un gestionnaire des ressources peut également modifier les détails pour affiner les critères de recherche lorsque le Tableau de planification est utilisé. Pour modifier le besoin en ressources, procédez comme suit.

1. Sur le formulaire **Projets**, dans l’onglet **Équipe**, sélectionnez le lien vers un besoin sur une ressource générique.
2. Sur le formulaire **Besoin en ressources** qui apparaît, entrez les informations de champ nécessaires

   Sur le formulaire **Besoin en ressources**, le chef de projet ou le gestionnaire de ressources peut également définir les compétences, les rôles, les préférences de ressources et l’unité organisationnelle préférée.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Mettre à jour les réservations des ressources après leur réservations sur un projet

Après avoir ajouté une ressource générique ou nommée à une équipe de projet, vous pouvez modifier les réservations de la ressource.

1. Sur le formulaire **Projets**, dans l’onglet **Équipe**, sélectionnez un membre de l’équipe, puis sélectionnez **Gérer les réservations**.
 
   Le tableau de planification s’affiche et présente les réservations du membre de l’équipe de projet. Développez l’enregistrement du membre de l’équipe pour afficher les heures réservées dans ce projet et d’autres projet qui consomment la capacité du membre de l’équipe.

2. Sélectionnez et faites glisser la réservation pour l’étendre ou la réduire. Une boîte de dialogue **Créer une réservation de ressource** apparaît qui vous permet d’ajuster la réservation.
3. Cliquez avec le bouton droit sur la réservation. Vous pouvez ensuite utiliser le menu contextuel qui s’affiche pour effectuer les actions suivantes :

    - Modifier le statut de la réservation
    - Modifier la réservation
    - Substituer une ressource sur l’équipe du projet

### <a name="change-the-booking-status"></a>Modifier le statut de la réservation

Vous pouvez changer tous les statuts de réservation par défaut ou personnalisés.

Les statuts suivants sont inclus dans Project Operations :

- **Annulé** : Annule la réservation d’une ressource et permet de libérer la capacité de la ressource.
- **Réservation ferme** : Consomme la capacité d’une ressource. Une ressource a généralement ce statut lorsque vous ouvrez **Gérer les réservations** de la grille **Tous les membres de l’équipe** sur le formulaire **Projets**.
- **Réservation temporaire** : Ajoute une ressource à une équipe mais ne consomme pas la capacité de la ressource. Ce statut indique que la ressource a été réservée pour le travail à faire mais a toujours de la capacité si elle est nécessaire pour d’autres tâches. Dans la vue de la disponibilité des ressources en général, les réservations temporaires disposent d’un statut différent de celui des réservations fermes.
- **Proposé** : Représente une proposition de ressource du gestionnaire de ressources ou du chef de projet. Les propositions ne consomment pas la capacité d’une ressource, et la ressource n’est pas ajoutée à l’équipe du projet. Pour réserver fermement la ressource de l’équipe, le chef de projet doit accepter la proposition.

### <a name="submit-resource-requests"></a>Envoyer des demandes de ressource

Les demandes de ressources sont utilisées pour transmettre la demande ou le besoin en ressources à exécuter par un gestionnaire des ressources. Pour une ressource générique déjà dans l’équipe, vous pouvez envoyer une demande de ressource directement. Une demande de ressource peut être exécutée de deux manières :

- Le gestionnaire de ressources exécute directement la demande. Dans ce cas, la ressource générique est remplacée par une réservation ferme avec une ressource nommée.
- Le gestionnaire de ressources propose une ressource au chef de projet, et celui-ci approuve ou rejette la ressource proposée.

#### <a name="direct-fulfillment-of-resource-requests"></a>Exécution directe des demandes de ressources

Lorsqu’un besoin en ressources est généré, un chef de projet peut envoyer une demande de ressource pour une ressource générique en sélectionnant la ressource puis en sélectionnant **Envoyer la demande**. Les commentaires sur la ressource peuvent être fournis au gestionnaire des ressources qui exécute la demande. Une fois la demande envoyée, le champ **Statut** du membre de l’équipe passe à **Envoyé**. Lorsque le gestionnaire des ressources exécute la demande, le membre de l’équipe générique est remplacé par la ressource nommée dans la grille **Tous les membres de l’équipe**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utiliser une proposition de ressource pour les demandes de ressources

Au lieu de réserver directement une ressource sur une demande de ressource, un gestionnaire des ressources peut proposer une ressource au chef de projet. Un gestionnaire des ressources peut utiliser cette option si une correspondance exacte pour les besoins n’est pas disponible. Lorsqu’un gestionnaire des ressources propose une ressource, le chef de projet voit que le champ **Statut** du membre de l’équipe générique est passé à **Révision nécessaire**.

Vous pouvez afficher la ressource proposée avec une visualisation de l’effet de la réservation de la proposition. 

1. Double-cliquez sur le membre de l’équipe dont le statut est **Révision nécessaire**. 
2. Sélectionnez l’onglet **Ressources proposées**.
3. Sélectionnez **Accepter toutes les propositions** pour accepter toutes les ressources ou **Rejeter toutes les propositions** pour les refuser. Si vous acceptez les ressources proposées, elles sont réservées fermement sur le projet comme membres de l’équipe et remplacent les ressources génériques.

> [!NOTE]
> Vous devez accepter ou rejeter toutes les ressources proposées. Vous ne pouvez pas les accepter ou les rejeter partiellement.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituer une ressource sur l’équipe du projet

Parfois, un chef de projet doit substituer un membre de l’équipe réservé sur un projet.

1. Sur le formulaire **Projets**, dans l’onglet **Équipe**, sélectionnez la ressource nécessitant d’être substituée, puis sélectionnez **Gérer les réservations**.
2. Développez la ressource pour afficher les projets auxquels elle est affectée.
3. Cliquez avec le bouton droit sur le projet, puis sélectionnez **Substituer la ressource**.
4. Si vous connaissez la ressource à substituer à la ressource actuelle, sélectionnez ou saisissez le nom, puis sélectionnez **Réattribuer**.

ou si vous devez rechercher une ressource, procédez comme suit.

1. Sélectionnez **Rechercher une substitution**.

   L’Assistant Planifier retourne une liste des substituts disponibles. Dans l’Assistant Planifier, vous pouvez filtrer davantage les ressources disponibles pour trouver un substitut approprié.

2. Pour substituer la ressource, sélectionnez la ressource souhaitée, puis sélectionnez **Substituer**.   

   Les réservations et attributions sont substituées avec la nouvelle ressource.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Rapprocher les réservations et les attributions de membre d’équipe

Pour les membres de l’équipe, les réservations et les attributions sont légèrement couplées. En d’autres termes, les ressources peuvent avoir des attributions mais aucune réservation, ou elles peuvent avoir des réservations mais aucune attribution. Idéalement, certaines réservation et attributions doivent être alignées, de sorte que les ressources aient une capacité engagée à effectuer les affectations des tâches. Toutefois, les réservations peuvent être basées sur la disponibilité, et les horaires des tâches peuvent changer à mesure que le projet avance. Par conséquent, le couplage léger des réservations ou des attributions procurent de la flexibilité.

Project Operations a un onglet **Rapprochement** permettant aux chefs de projet de rapprocher les réservations des membres de l’équipe et leurs attributions pour les équipes de projet.

L’onglet **Rapprochement** affiche des réservations et attributions jusqu’au niveau de l’affectation de tâches individuelles à chaque membre de l’équipe. Il affiche les heures dans cellules représentant des périodes allant des mois jusqu’à des jours.

L’onglet affiche également un total net général pour le projet, conjointement à une colonne totale.

Pour chaque ressource, l’onglet calcule la distinction entre les réservations du membre de l’équipe et un report des affectations des tâches du membre de l’équipe. Idéalement, cette différence doit être de 0 (zéro). En d’autres termes, il ne doit exister aucune différence entre les réservations et les attributions. Les différences sont en couleur et grisées pour attirer l’attention sur deux conditions :

- **Pénurie de réservation** : Se produit lorsque la ressource a plus d’attributions que de réservations. Cette capacité n’ayant pas été réservée, un chef de projet peut également corriger cette condition en étendant les réservations de la ressource pour compenser la pénurie.
- **Réservations en trop** : Se produit lorsque la ressource a été réservée pour le projet, mais n’a pas été affectée à des tâches. Cette condition peut être acceptable dans les cas où la ressource a été réservée dans le projet avant que l’affectation de tâches se soit produite. En revanche, dans d’autres cas, la ressource n’est pas planifiée pour être affectée à des tâches. Dans ce genre de situation, le chef de projet doit envisager d’annuler les réservations de la ressource, de sorte que la capacité puisse être utilisée pour un autre projet.

Dans certains cas, lorsque vous affichez le temps à un niveau supérieur que le niveau du jour, par exemple, le niveau de mois, vous pouvez voir une différence nette de zéro pour une ressource. En d’autres termes, réservations = attributions. Toutefois, si vous affichez le temps au niveau de la semaine, vous pouvez voir des attributions de zéro heure et des réservations de 40 heures au cours de la première semaine, mais des attributions de 40 heures et des réservations de zéro heure dans la deuxième semaine. Globalement, les réservations et attributions sont rapprochées, mais elles ne correspondent pas d’une semaine à l’autre.

Lorsque vous affichez le temps à des niveaux plus élevés, les cellules de l’onglet **Rapprochement** ont un indicateur pour vous informer qu’il existe des différences à des niveaux plus bas. Double-cliquez sur une cellule pour faire un zoom avant pour afficher la différence. Vous pouvez ensuite cliquer avec le bouton droit pour faire un zoom arrière. En sélectionnant une ressource puis en cliquant sur **Différence suivante** dans la barre d’outils de la grille, vous pouvez passer à la prochaine différence entre les réservations et les affectations d’une ressource. Sélectionnez **Différence précédente** pour revenir. Vous pouvez également désactiver l’indicateur de différence et le comportement de navigation sous **Paramètres**.

Si vous avez des affectations de tâches pour une ressource mais aucune réservation, sur le formulaire **Projets**, dans l’onglet **Rapprochement**, sélectionnez la pénurie de réservation, puis sélectionnez **Étendre la réservation**. La boîte de dialogue **Étendre la réservation** s’affiche et affiche la réservation qui est nécessaire pour compenser la pénurie de la ressource. La boîte de dialogue présente également les réservations existantes de la ressource dans tous les projets ou d’autres entités planifiables. Si vous sélectionnez **OK** pour créer la réservation pour la ressource, indépendamment de la disponibilité de cette ressource, vous pouvez entraîner de la surréservation.

Le chef de projet ou le gestionnaire de ressources peut ensuite utiliser le Tableau de planification pour gérer tous les cas où une ressource est réservée en trop au-delà de sa capacité.


[!INCLUDE[footer-include](../includes/footer-banner.md)]