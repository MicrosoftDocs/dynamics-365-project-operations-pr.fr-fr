---
title: Gérer les ressources
description: Cette rubrique fournit des informations sur la façon dont vous pouvez gérer les ressources.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 548ee7db1c8ca14f1b88d76a534d2922549eba138659e67a84cd89e6f7ee2170
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998503"
---
# <a name="manage-resources"></a>Gérer les ressources

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation contient un tableau de bord de gestionnaire des ressources qui fournit une vue d’ensemble visuelle de la demande et de l’utilisation des ressources dans toute l’organisation. Vous pouvez utiliser les graphiques de ce tableau de bord pour visualiser les informations suivantes :

- **Demande de ressource** – Le graphique **Demande de ressource active** présente les ressources qui ont été envoyés. Les ressources sont regroupées par rôle ou par projet.
- **Demande de ressource non envoyée** – Le graphique **Demande de ressource non attribuée** affiche tous les besoins en ressources qui n’ont pas été envoyés. Il permet aux gestionnaires de ressources à afficher la demande qui n’est pas ferme et peut être transmise via une demande de ressource.
- **Utilisation facturable pour la semaine dernière** – Le graphique **Utilisation par rôle** affiche le pourcentage d’utilisation facturable réelle de l’organisation par rôle par rapport à son utilisation facturable cible par rôle.

    > [!NOTE]
    > Pour rendre le graphique **Utilisation par rôle** disponibles, créez une tâche qui exécute le workflow UpdateRoleUtilization. Cette tâche périodique exécute tous les sept jours calculer l’utilisation facturable pour les sept jours précédents. Les résultats sont regroupés par rôle.

## <a name="manage-project-team-members"></a>Gérer les membres de l’équipe du projet

Les responsables de projet peuvent utiliser le tableau de bord du gde ressources pour gérer les ressources dans des projets. Par exemple, ils peuvent ajouter un membre de l’équipe directement au projet et réserver un membre de l’équipe pour combler les besoins en ressources capturés par une ressource générique.

### <a name="add-a-team-member-directly-to-a-project"></a>Ajouter un membre d’équipe directement à un projet

Pour ajouter un membre de l’équipe directement au projet, dans la page **Projets**, dans l’onglet **Équipe**, sélectionnez **Nouveau**. La boîte de dialogue **Création rapide : Membre de l’équipe du projet** apparaît. Dans cette boîte de dialogue, vous pouvez effectuer ces tâches :

- **Réserver une ressource nommée** – Dans le champ **Ressource pouvant être réservée**, sélectionnez le nom de la ressource. Sélectionnez ensuite le rôle, définissez la période et sélectionnez une méthode d’allocation. La ressource nommée sélectionnée est ajoutée au projet en utilisant la méthode sélectionnée de répartition et le calendrier de ressources.
- **Ajouter une ressource générique** – Laissez le champ **Ressource pouvant être réservée** vide, puis sélectionnez le rôle, définissez la période, puis la méthode privilégiée de répartition. Une ressource générique est ajoutée à l’équipe comme un espace réservé pour maintenir le critère de demande utilisé pour réserver des ressources nommées de l’équipe. La demande est effectuée en fonction du calendrier du projet.
- **Ajouter une ressource nommée à l’équipe sans consommer la capacité de ressource** – Dans le champ **Ressource pouvant être réservée**, sélectionnez une ressource. Puis sélectionnez la période, et sélectionnez **Aucun** comme méthode de répartition. La ressource est ajoutée à l’équipe, mais la capacité de la ressource n’est pas consommée via une réservation.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Réserver un membre de l’équipe pour satisfaire aux besoins en ressources pour une ressource générique

Dans PSA, vous pouvez réserver une ressource générique sur une équipe du projet, et spécifier le type de rôle, la capacité nécessaire, et comment la capacité distribuée. Dans le besoin en ressources, vous pouvez spécifier des attributs associés à la ressource générique. Ces attributs incluent les compétences requises, l’unité d’organisation privilégiée, et les ressources préférées.

Procédez comme suit pour spécifier les compétences requises sur une ressource générique pour un développeur.

1. Dans la page **Projets**, dans l’onglet **Équipe**, sélectionnez **Nouveau** pour réserver une ressource générique.

    ![Ressource générique réservée sur l’équipe.](media/Resource-Management-image9.png)

2. Dans la vue **Tous les membres de l’équipe**, dans la colonne **Besoin en ressources**, sélectionnez le lien pour ajouter des compétences requises pour la ressource générique.

    ![Lien Besoin.](media/Resource-Management-image10.png)

3. Dans la page **Besoin en ressources** qui s’affiche, dans la grille **Qualifications**, sélectionnez les points de suspension (**...**) puis sélectionnez **Ajouter la nouvelle caractéristique du besoin** pour ajouter les compétences requises pour votre développeur.

    ![Commande Ajouter la nouvelle caractéristique du besoin.](media/Resource-Management-image11.png)

4. Dans la boîte de dialogue **Création rapide : Caractéristique du besoin** qui s’affiche, dans le champ **Caractéristique**, sélectionnez la qualification requise. Ensuite, dans le champ **Valeur d’évaluation**, sélectionnez le niveau de qualification pour cette compétence. Enfin, dans le champ **Besoin en ressources**, définissez le besoin en ressources sources à partir des unités d’organisation ou même de ressources nommées. Lorsque vous avez terminé, cliquez sur **Enregistrer**.

    ![Boîte de dialogue Création rapide : Caractéristique du besoin.](media/Resource-Management-image12.png)

5. Dans la page **Besoin en ressources**, sélectionnez **Réserver** pour satisfaire le besoin en ressources.

    ![Bouton Réserver de la page Besoin en ressources.](media/Resource-Management-image13.png)

    Vous pouvez également sélectionner la ressource générique dans la grille **Tous les membres de l’équipe** puis sélectionner **Réserver**.

    ![Bouton Réserver au-dessus de la grille Tous les membres de l’équipe.](media/Resource-Management-image14.png)

    > [!NOTE]
    > Dans cet exemple, il y a 40 heures requises mais aucun heure réservée réellement, car les ressources génériques ne disposent pas de réservations. En outre, il n’existe aucune heure attribuée, car la ressource générique a été ajoutée directement à l’équipe. Elle n’a pas été ajoutée à l’aide de l’affectation des tâches.

    Dans la page **Assistant Planifier**, vous pouvez filtrer les ressources disponibles par les besoins spécifiés sur le besoin en ressources. Les ressources sont triées en fonction des paramètres de tri spécifiés sur le tableau de planification.

    ![Page Assistant Planifier.](media/Resource-Management-image15.png)

    Voici quelques filtres souvent utilisés :

    - **Caractéristiques avec une évaluation** – Filtrez par compétences, certifications, et autres qualités de ressource, en plus des évaluations de compétences.
    - **Rôles** – Filtrez par les rôles par défaut qui sont affectés aux ressources pouvant être réservées.
    - **Unité d’organisation** – Filtrez les ressources pouvant être réservées par les unités d’organisation auxquelles elles sont attribuées.

6. Si les résultats de la recherche de besoin d’origine ne vous conviennent pas, vous pouvez modifier les critères de filtre. Développez le volet **Vue de filtre** de gauche, puis sélectionnez **Rechercher** pour trouver des ressources supplémentaires.

    ![Volet Vue de filtre.](media/Resource-Management-image16.png)

7. Pour modifier la façon dont les résultats sont triés, sélectionnez **Trier**.

    ![Commande Trier.](media/Resource-Management-image17.png)

8. Sélectionnez les ressources en fonction de la demande spécifiée sur le besoin, comme indiqué en haut de la grille. Vous pouvez désactiver la sélection des cellules dans la grille et laisser cette capacité de ressource ouverte. Une seule ressource à la fois peut être sélectionnée comme réservée.

9. Sélectionnez **Réserver** pour réserver la ressource sélectionnée et laissez le Tableau de planification ouvert, de sorte à sélectionner des ressources supplémentaires. Par ailleurs, sélectionnez **Réserver et quitter** pour réserver la ressource sélectionnée et fermez le tableau de planification.

    ![Ressource à réserver.](media/Resource-Management-image19.png)

    Vous recevez une notification sur les heures réservées. Les indicateurs de la demande affichent la satisfaction du besoin de réservation et ce qu’il reste à satisfaire. Vous pouvez aussi voir quelle quantité de capacité de la ressource sélectionnée est utilisée. Sélectionnez **Développer** pour afficher plus de détails sur les réservations de ressources.

9. Revenez à la vue **Tous les membres de l’équipe**. Dans la grille, notez que la ressource générique a été remplacée par la ressource nommée, et 40 heures sont répertoriées comme réservées pour cette ressource.

    ![Grille Tous les membres de l’équipe mise à jour.](media/Resource-Management-image20.png)

    > [!NOTE]
    > Aucune heure affectée n’est affichée, car elles ont été réservées directement sur l’équipe. Elles n’ont pas été réservées à l’aide de l’affectation des tâches.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Attribuez des ressources génériques aux tâches et générez des besoins en ressources

Dans PSA, vous pouvez créer des tâches puis leur attribuer des ressources génériques. De cette façon, la demande de ressource peut être représentée par des espaces réservés, pendant que vous estimez votre planification et les chiffres financiers. Vous pouvez ensuite générer des besoins en ressources pour les ressources génériques et les mener à bien.

1. Dans la page **Projets**, dans l’onglet **Planification**, sélectionnez **Ajouter** pour créer une tâche.

    ![Nouvelle tâche créée.](media/Resource-Management-image21.png)

2. Dans le champ **Ressources**, sélectionnez le symbole **Sélecteur de ressources**. Le sélecteur de ressources s’affiche et affiche les membres de l’équipe existants du projet.

    ![Sélecteur de ressources.](media/Resource-Management-image22.png)

3. Entrez le nom de la ressource générique, puis sélectionnez **Créer**.

    ![Nom d’une nouvelle ressource générique entré.](media/Resource-Management-image23.png)

4. Dans la boîte de dialogue **Création rapide : Membre de l’équipe du projet** qui s’affiche, dans le champ **Rôle**, sélectionnez le rôle pour la ressource générique. Dans le champ **Unité d’allocation des ressources**, sélectionnez l’unité d’organisation pour la ressource générique. Sélectionnez ensuite **Enregistrer**.

    ![Boîte de dialogue Création rapide : Membre de l’équipe du projet.](media/Resource-Management-image24.png)

    Le membre de l’équipe générique est maintenant attribué à la tâche.

    ![Membre de l’équipe générique attribué à la tâche.](media/Resource-Management-image25.png)

    Dans l’onglet **Équipe**, vous verrez le nouveau membre de l’équipe générique. Notez qu’il a uniquement des heures affectées. Ces heures sont la somme de toutes les tâches qui sont affectées au membre de l’équipe générique. Le membre de l’équipe générique n’a pas encore d’heures requises ou de besoin en ressources.

    ![Membre de l’équipe générique dans l’onglet Équipe.](media/Resource-Management-image26.png)

5. Vous pouvez désormais affecter le membre de l’équipe générique à d’autres tâches en utilisant le Sélecteur de ressources.

    ![Membre de l’équipe générique dans le Sélecteur de ressources.](media/Resource-Management-image27.png)

    Lorsque vous avez terminé d’affecter la ressource générique aux tâches, vous pouvez générer un besoin en ressources pour la ressource générique.

5. Dans l’onglet **Équipe**, sélectionnez la ressource générique, puis sélectionnez **Générer un besoin**.

    ![Commande Générer un besoin.](media/Resource-Management-image28.png)

    Lorsque le besoin est généré, le membre de l’équipe générique aura des heures requises et un lien pour le besoin en ressources.

    ![Lien Besoin en ressources.](media/Resource-Management-image29.png)

    Une fois que vous avez réservé une ressource nommée, la ressource générique est supprimée de l’équipe et remplacée par la ressource nommée.

    ![Ressource générique remplacée par la ressource nommée.](media/Resource-Management-image30.png)

    Dans l’onglet **Planification**, les affectations des ressources génériques sont supprimées et remplacées par la ressource nommée.

    ![Les affectations de ressources génériques sont remplacées par la ressource nommée dans l’onglet Planification.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Ceci se produit uniquement lorsque la ressource nommée est entièrement réservée pour ce besoin en ressources générique. Lorsqu’une ou plusieurs ressources nommées remplacent partiellement ou entièrement, respectivement, le besoin en ressources générique, la ressource générique reste affectée à la tâche.

    Dans l’illustration qui suit, une tâche de 80 heures a été planifiée pour une durée de cinq jours (16 heures par jour pendant cinq jours) et affectée à la ressource générique nommée **Fonctionnel**.

    ![Tâche de 80 heures, cinq jours affectée à la ressource générique Fonctionnel.](media/Resource-Management-image32.png)

    Lorsque vous générez le besoin, il correspond à 80 heures pendant cinq jours.

    ![Besoin généré pour 80 heures pendant cinq jours.](media/Resource-Management-image33.png)

    Étant donné que les ressources disponibles travaillent uniquement huit heures par jour, deux ressources sont nécessaires pour exécuter ce besoin.

    ![Deuxième ressource.](media/Resource-Management-image35.png)

    Dans l’onglet **Équipe**, vous pouvez désormais voir que la ressource générique ne contient pas de temps requis, mais des heures affectées continuent de s’afficher avec les deux ressources nommées qui composent la réalisation.

    ![Deux ressources nommées dans l’onglet Équipe.](media/Resource-Management-image36.png)

    Dans l’onglet **Planification**, la ressource générique reste affectée à la tâche.

    ![Ressources génériques dans l’onglet Planification.](media/Resource-Management-image37.png)

PSA n’attribue pas les deux ressources à la tâche, car ce comportement produirait une planification moins prévisible. Dans cet exemple simple, il est facile de répartir les heures également entre deux ressources. Toutefois, dans les scénarios plus complexes qui impliquent plusieurs tâches et des ressources multiples, PSA doit faire des hypothèses sur la manière dont elle doit affecter les réservations qui sont reçues pour plusieurs ressources et plusieurs tâches.

Par conséquent, dans les scénarios suivants, le chef de projet est responsable d’analyser plusieurs réservations et de les affecter en conséquence. Pour affecter les réservations, le chef de projet attribue les tâches des ressources génériques aux ressources nommées puis utilise la vue **Rapprochement** pour s’assurer que la répartition fonctionne avec les réservations.

### <a name="edit-a-resource-requirement"></a>Modifier un besoin en ressources

Lorsqu’un besoin en ressources a été créé, un responsable de projet ou un gestionnaire des ressources peut également modifier les détails pour affiner les critères de recherche lorsque le Tableau de planification est utilisé. Pour modifier le besoin en ressources, procédez comme suit.

1. Dans la page **Projets**, dans l’onglet **Équipe**, sélectionnez le lien vers un besoin sur une ressource générique.
2. Sur la page **Besoin en ressources** qui s’affiche, vous pouvez mettre plusieurs attributs à jour. Voici quelques exemples :

    - Nom
    - Date de début
    - Date de fin
    - Durée
    - Type de ressource

Dans la page **Besoin en ressources**, le chef de projet ou le gestionnaire de ressources peut également définir les informations suivantes :

- Qualifications
- Rôles
- Préférences de ressource
- Unité d’organisation privilégiée

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Mettre à jour les réservations des ressources après leur réservations sur un projet

Après avoir ajouté une ressource générique ou nommée à une équipe de projet, vous pouvez modifier les réservations de la ressource.

1. Dans la page **Projets**, dans l’onglet **Équipe**, sélectionnez un membre de l’équipe, puis sélectionnez **Gérer les réservations**.

    ![Tableau de planification ouvert pour le membre de l’équipe sélectionné.](media/Resource-Management-image40.png)

    Le tableau de planification s’affiche et présente les réservations du membre de l’équipe de projet. Développez l’enregistrement du membre de l’équipe pour afficher les heures réservées dans ce projet et d’autres projet qui consomment la capacité du membre de l’équipe.

2. Sélectionnez et faites glisser la réservation pour l’étendre ou la réduire. Une boîte de dialogue **Créer une réservation de ressource** apparaît qui vous permet d’ajuster la réservation.

    ![Boîte de dialogue Créer une réservation de ressource.](media/Resource-Management-image41.png)

3. Cliquez avec le bouton droit sur la réservation. Vous pouvez ensuite utiliser le menu contextuel qui s’affiche pour effectuer les actions suivantes :

    - Modifier le statut de la réservation.
    - Modifier la réservation.
    - Substituer une ressource sur l’équipe du projet.

### <a name="change-the-booking-status"></a>Modifier le statut de la réservation

Vous pouvez changer tous les statuts de réservation par défaut ou personnalisés.

![Commande Modifier le statut.](media/Resource-Management-image42.png)

Les statuts suivants sont inclus dans PSA :

- **Annulé** – Ce statut annule la réservation d’une ressource et permet de libérer la capacité de la ressource.
- **Réservation ferme** – Ce statut consomme la capacité d’une ressource. Une ressource a généralement ce statut lorsque vous ouvrez **Gérer les réservations** de la grille **Tous les membres de l’équipe** sur la page **Projets**.
- **Réservation temporaire** – Ce statut ajoute une ressource à une équipe mais ne consomme pas la capacité de la ressource. Il indique que la ressource a été réservée pour le travail à faire mais a toujours de la capacité si elle est nécessaire pour d’autres tâches. Dans la vue de la disponibilité des ressources en général, les réservations temporaires disposent d’un statut différent de celui des réservations fermes.
- **Proposé** – Ce statut représente une proposition de ressource du gestionnaire de ressources ou du responsable de projet. Les propositions ne consomment pas la capacité d’une ressource, et la ressource n’est pas ajoutée à l’équipe du projet. Pour réserver fermement la ressource de l’équipe, le chef de projet doit accepter la proposition.

### <a name="submit-resource-requests"></a>Soumettre les demandes de ressources

Les demandes de ressources sont utilisées pour transmettre la demande (besoin en ressources) à exécuter par un gestionnaire des ressources. Pour une ressource générique déjà dans l’équipe, vous pouvez envoyer une demande de ressource directement. Une demande de ressource peut être exécutée de deux manières :

- Le gestionnaire de ressources exécute directement la demande. Dans ce cas, la ressource générique est remplacée par une réservation ferme avec une ressource nommée.
- Le gestionnaire de ressources propose une ressource au chef de projet, le chef de projet approuve ou rejette la ressource proposée.

#### <a name="direct-fulfillment-of-resource-requests"></a>Exécution directe des demandes de ressources

Lorsqu’un besoin en ressources est généré, un chef de projet peut envoyer une demande de ressource pour une ressource générique en sélectionnant la ressource puis en sélectionnant **Envoyer la demande**.

![Bouton Envoyer la demande.](media/Resource-Management-image45.png)

Les commentaires sur la ressource peuvent être fournis au gestionnaire des ressources qui exécute la demande. Une fois la demande envoyée, le champ **Statut** du membre de l’équipe passe à **Envoyé**.

![Saisie de commentaires facultatifs.](media/Resource-Management-image46.png)

Lorsque le gestionnaire des ressources exécute la demande, le membre de l’équipe générique est remplacé par la ressource nommée dans la grille **Tous les membres de l’équipe**.

![Membre de l’équipe générique remplacé par la ressource nommée dans la grille Tous les membres de l’équipe.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utiliser une proposition de ressource pour les demandes de ressources

Au lieu de réserver directement une ressource sur une demande de ressource, un gestionnaire des ressources peut proposer une ressource au chef de projet. Un gestionnaire des ressources peut utiliser cette option si une correspondance exacte pour les besoins n’est pas disponible. Lorsqu’un gestionnaire des ressources propose une ressource, le chef de projet voit que le champ **Statut** du membre de l’équipe générique est passé à **Révision nécessaire**.

![Statut du membre de l’équipe générique passé à Révision nécessaire.](media/Resource-Management-image48.png)

Pour afficher la ressource proposée conjointement à une visualisation des effets de la réservation de la proposition, double-cliquez sur le membre de l’équipe qui a le statut **Révision nécessaire**. Sélectionnez ensuite l’onglet **Ressources proposées**.

![Onglet Ressources proposées.](media/Resource-Management-image49.png)

Sélectionnez **Accepter toutes les propositions** pour accepter toutes les ressources ou **Rejeter toutes les propositions** pour les refuser. Si vous acceptez les ressources proposées, elles sont réservées fermement sur le projet comme membres de l’équipe et remplacent les ressources génériques.

> [!NOTE]
> Vous devez accepter ou rejeter toutes les ressources proposées. Vous ne pouvez pas les accepter ou les rejeter partiellement.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituer une ressource sur l’équipe du projet

Parfois, un chef de projet doit substituer un membre de l’équipe réservé sur un projet.

1. Dans la page **Projets**, dans l’onglet **Équipe**, sélectionnez la ressource nécessitant d’être substituée, puis sélectionnez **Gérer les réservations**.
2. Développez la ressource pour afficher les projets auxquels elle est affectée.

    ![Ressource développée pour afficher des projets affectés.](media/Resource-Management-image50.png)

3. Cliquez avec le bouton droit sur le projet, puis sélectionnez **Substituer la ressource**.
4. Si vous connaissez la ressource à substituer à la ressource actuelle, sélectionnez ou saisissez le nom, puis sélectionnez **Réattribuer**.

    ![Spécification d’une ressource de substitution.](media/Resource-Management-image51.png)

    Sinon, procédez comme suit pour rechercher une ressource :

    1. Sélectionnez **Rechercher une substitution**.

        ![Recherche d’une ressource de substitution.](media/Resource-Management-image52.png)

        L’Assistant Planifier retourne une liste des substituts disponibles. Dans l’Assistant Planifier, vous pouvez filtrer davantage les ressources disponibles pour trouver un substitut approprié.

        ![Liste des substituts disponibles.](media/Resource-Management-image53.png)

    2. Pour substituer la ressource, sélectionnez la ressource souhaitée, puis sélectionnez **Substituer**.

        ![Substituer la ressource sélectionnée.](media/Resource-Management-image54.png)

    Les réservations et attributions sont substituées avec la nouvelle ressource.

    ![Réservations et attributions substituées avec la nouvelle ressource.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Rapprocher les réservations et les attributions de membre d’équipe

Pour les membres de l’équipe, les réservations et les attributions sont légèrement couplées. En d’autres termes, les ressources peuvent avoir des attributions mais aucune réservation, ou elles peuvent avoir des réservations mais aucune attribution. Idéalement, certaines réservation et attributions doivent être alignées, de sorte que les ressources aient une capacité engagée à effectuer les affectations des tâches. Cependant, les réservations peuvent être basées sur la disponibilité et les calendriers des tâches peuvent changer à mesure que le projet se poursuit. Par conséquent, le couplage léger des réservations ou des attributions procurent de la flexibilité.

PSA a un onglet **Rapprochement** permettant aux chefs de projet de rapprocher les réservations des membres de l’équipe et leurs attributions pour les équipes de projet.

![Onglet Rapprochement.](media/Resource-Management-image56.png)

L’onglet **Rapprochement** affiche des réservations et attributions jusqu’au niveau de l’affectation de tâches individuelles à chaque membre de l’équipe. Il affiche les heures dans cellules représentant des périodes allant des mois jusqu’à des jours.

L’onglet affiche également un total net général pour le projet, conjointement à une colonne totale.

Pour chaque ressource, l’onglet calcule la distinction entre les réservations du membre de l’équipe et un report des affectations des tâches du membre de l’équipe. Idéalement, cette différence doit être de 0 (zéro). En d’autres termes, il ne doit exister aucune différence entre les réservations et les attributions. Les différences sont en couleur et grisées pour attirer l’attention sur deux conditions :

- **Pénurie de réservation** : ce phénomène se produit lorsqu’une ressource comporte plus d’affectations que de réservations. Comme cette capacité n’a pas été réservée, un chef de projet peut souhaiter corriger cet état en augmentant les réservations de la ressource pour couvrir le déficit.
- **Réservations excédentaires** : ce phénomène se produit lorsqu’une ressource a été réservée dans le projet mais n’a pas été affectée à des tâches. Cet état peut être acceptable dans les cas où la ressource a été réservée dans le projet avant l’affectation de la tâche. Cependant, dans d’autres cas, la ressource n’est pas planifiée pour être affectée à des tâches. Dans ce genre de situation, le chef de projet doit envisager d’annuler les réservations de la ressource, de sorte que la capacité puisse être utilisée pour un autre projet.

Dans certains cas, lorsque vous affichez le temps à un niveau supérieur que le niveau du jour (par exemple, le niveau de mois), vous pouvez voir une différence nette de zéro pour une ressource (en d’autres termes, réservations = attributions). Toutefois, si vous affichez le temps au niveau de la semaine, vous pouvez voir des attributions de zéro heure et des réservations de 40 heures au cours de la première semaine, mais des attributions de 40 heures et des réservations de zéro heure dans la deuxième semaine. Globalement, les réservations et attributions sont rapprochées, mais elles ne correspondent pas d’une semaine à l’autre.

Lorsque vous affichez le temps à des niveaux plus élevés, les cellules de l’onglet **Rapprochement** ont un indicateur pour vous informer qu’il existe des différences à des niveaux plus bas. En double-cliquant sur une cellule, vous pouvez faire un zoom avant pour afficher la différence. Vous pouvez ensuite cliquer avec le bouton droit pour faire un zoom arrière. En sélectionnant une ressource puis en utilisant le contrôle **Différence suivante** dans la barre d’outils de la grille, vous pouvez passer à la prochaine différence entre les réservations et les affectations d’une ressource. Vous pouvez ensuite utiliser le contrôle **Différence précédente** pour revenir. Vous pouvez également désactiver l’indicateur de différence et le comportement de navigation sous **Paramètres**.

![Indicateur de différence.](media/Resource-Management-image57.png)

Si vous avez des affectations de tâches pour une ressource mais aucune réservation, dans la page **Projets**, dans l’onglet **Rapprochement**, sélectionnez la pénurie de réservation, puis sélectionnez **Étendre la réservation**. La boîte de dialogue **Étendre la réservation** s’affiche et affiche la réservation qui est nécessaire pour compenser la pénurie de la ressource. Elle présente également les réservations existantes de la ressource dans tous les projets ou d’autres entités planifiables. Si vous sélectionnez **OK** pour créer la réservation pour la ressource, indépendamment de la disponibilité de cette ressource, vous pouvez entraîner de la surréservation.

![Boîte de dialogue Étendre la réservation.](media/Resource-Management-image58.png)

Le chef de projet ou le gestionnaire de ressources peut ensuite utiliser le Tableau de planification pour gérer tous les cas où une ressource est surréservée au-delà de sa capacité.


[!INCLUDE[footer-include](../includes/footer-banner.md)]