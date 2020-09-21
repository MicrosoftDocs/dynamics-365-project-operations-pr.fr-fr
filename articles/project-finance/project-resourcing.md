---
title: Ressources de projet
description: Cette rubrique fournit des informations sur les ressources de projet.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167973"
---
# <a name="project-resourcing"></a>Ressources de projet

[!include [banner](../includes/banner.md)]

Cette rubrique fournit des informations sur les ressources de projet.

Un défi auquel sont confrontés les chefs de projet et les responsables des ressources au cours de la phase de planification de projet n’est autre que l’allocation des ressources, au cours de laquelle ils doivent déterminer et réserver la bonne ressource pour travailler sur un projet. Dans Dynamics 365 Finance, les capacités de ressources pour les projets vous permettent de définir des rôles qui sont traités comme des ressources temporaires pouvant être réservées pour un engagement spécifique ou une partie d’un engagement. Ce type de ressources permet aux chefs de projet et aux responsables des ressources d’effectuer les tâches suivantes :

- Définissez un rôle qui possède les compétences requises, afin qu’il soit facile de faire correspondre les ressources.
- Utilisez les rôles pour définir un calendrier d’engagement initial basé sur des ressources réservées.
- Estimez les coûts et déterminez un budget initial, en fonction des rôles et des ressources attribués à un projet.
- Utilisez les rôles pour estimer le nombre de réservations de ressources requises pour chaque engagement.
- Estimez le nombre de ressources nécessaires pour tout le cycle de vie d’un projet.
- Rédigez une structure de répartition du travail en utilisant les affectations de ressources initiales.

[![Cycle de vie d’un projet](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Au fur et à mesure de la planification du projet, les ressources planifiées peuvent être remplacées par des ressources en personnel. Le chef de projet peut également revenir en arrière et mettre à jour les réservations de ressources à n’importe quelle étape du projet.

## <a name="set-up-project-resources"></a>Configurer les ressources de projet
Vous devez configurer un calendrier et l’associer à un employé ou à un employé. Le calendrier permet de planifier le projet et le temps de travail des ressources réservées au projet. Lors de la configuration du calendrier, les chefs de projet peuvent effectuer un nivellement des ressources dans le cadre de l’optimisation des ressources. En fonction du calendrier du calendrier, des restrictions peuvent être appliquées aux ressources. Vous pouvez configurer un calendrier sur la page **Calendriers**.

Lorsque vous configurez un employé en tant que ressource de projet, vous pouvez choisir parmi les employés qui travaillent dans l’entreprise pour laquelle vous configurez des ressources. Vous pouvez également sélectionner des employés d’autres sociétés de votre organisation. Ces employés sont appelés ressources intersociétés.

Les procédures suivantes expliquent comment configurer un employé en tant que ressource de projet dans votre entreprise et comment configurer une ressource de projet intersociétés.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurer un employé en tant que ressource de projet

1. Sur la page **Employés**, dans la liste **Employés**, sélectionnez l’employé que vous ajoutez en tant que ressource de projet et ouvrez l’enregistrement de l’employé.
2. Dans le volet Actions, sélectionnez **Projet** &gt;**Configurer** &gt; **Configuration du projet**.
3. Sélectionnez un calendrier, puis fermez la page.

Vous pouvez également spécifier des projets par défaut pour une ressource en tant que type de pré-affectation. Les pré-affectations peuvent être utilisées lorsque le responsable de ressources ou le chef de projet sait à l’avance sur quels projets la ressource travaillera. Les pré-affectations peuvent être également basées sur la demande d’un commanditaire ou d’un client. Pour pré-attribuer un projet, sur la page **Attribuer des projets**, sur l’onglet **Projets**, dans la liste **Projets restants**, sélectionnez le projet approprié.

### <a name="set-up-an-intercompany-resource"></a>Configurer une ressource intersociétés

Lorsque vous configurez un employé en tant que ressource intersociétés, vous devez terminer la configuration à la fois dans la société prêteuse et dans la société emprunteuse.

**Dans la société de prêt**

1. Dans Finance, vérifiez que la société de prêt est sélectionnée, puis suivez la procédure de la section précédente, « Configurer un employé en tant que ressource de projet ».
2. Sur la page **Comptabilité intersociétés**, sélectionnez **Nouveau**.
3. Dans le champ **ID d’entité juridique**, sélectionnez la société prêteuse. Complétez les champs restants, le cas échéant, puis cliquez sur **Enregistrer**.
4. Sur la page **Prix du transfert**, sélectionnez **Nouveau**.
5. Dans le champ **Entité juridique emprunteuse**, sélectionnez la société appropriée.
6. Pour prêter à la société emprunteuse uniquement la ressource que vous avez créée au début de cette section, dans le champ **Ressource**, sélectionnez le nom de la ressource que vous avez créée. Pour mettre toutes les ressources de la société prêteuse à disposition de la société emprunteuse, laissez le champ **Ressource** vide.
7. Sur la page **Gestion de projet et comptabilité**, sur l’onglet **Intersociétés**, définissez l’option **Activer la planification des ressources et les feuilles de temps intersociétés** sur **Oui**.

**Dans la société emprunteuse**

- Sur la page **Liste des ressources**, dans le filtre de recherche, saisissez le nom de la ressource que vous avez créée pour la société prêteuse, afin de vérifier que le nom est inclus dans la liste des ressources de la société emprunteuse.

## <a name="manage-resource-competencies"></a>Gérer les compétences de ressources
Les compétences des ressources sont un élément essentiel de la gestion des ressources. Les compétences peuvent être utilisées comme base de référence pour déterminer les ressources qui présentent le juste équilibre entre compétences, formation, certification et expérience de projet. Vous devez configurer ces informations pour chaque ressource et les mettre à jour régulièrement. De cette manière, vous pouvez maximiser les capacités lorsque des compétences de ressources spécifiques sont mises en correspondance lors de l’affectation des ressources du projet.

[![Exemples de compétences, certifications, formation et expérience de projet](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Les procédures suivantes expliquent comment configurer certaines des compétences pour une ressource.

Pour configurer les compétences d’un employé, vous pouvez utiliser la liste **Employés** dans les ressources humaines ou la liste **Ressources** dans Gestion de projet et comptabilité. Pour les procédures suivantes, la liste **Employés** dans les ressources humaines est utilisée.

### <a name="set-up-competencies-certificates"></a>Configurer les compétences : Certificats

1. Sur la liste **Employés**, sélectionnez la ligne pour laquelle l’employé doit ajouter des informations de certificat.
2. Dans le volet Actions, sur l’onglet **Employé**, dans le groupe **Compétences**, sélectionnez **Certificats**.
3. Sélectionnez **Nouveau**, puis dans le champ **Type de certificat**, sélectionnez **PMP**.
4. Dans le champ **Date de début**, sélectionnez **01/10/2015**, puis **Enregistrer**.

### <a name="set-up-competencies-skills"></a>Configurer les compétences : Compétences

1. Sur la liste **Employés**, veillez à ce que l’employé que vous avez utilisé dans la procédure précédente est toujours sélectionné. Dans le volet Actions, sur l’onglet **Employé**, dans le groupe **Compétences**, sélectionnez **Certificats**.
2. Cliquez sur **Nouveau**.
3. Dans le champ **Compétence**, sélectionnez **Gestion de projet**.
4. Dans le champ **Niveau**, sélectionnez **Expert 5**
5. Dans le champ **Date du niveau**, sélectionnez **14/01/2014**.
6. Dans le champ **Années d’expérience**, saisissez **10**.
7. Cliquez sur **Enregistrer** puis fermez la page.

## <a name="create-a-new-project"></a>Créer un projet
1. Sur la page **Gestion de projet**, sélectionnez **Nouveau projet**, et saisissez les valeurs suivantes :

    - **Type de projet :** Temps et matériel
    - **Nom du projet :** Mise à niveau XYZ Phase 2
    - **Groupe de projets :** TM\_TEC
    - **ID de contrat du projet :** 00000002

2. Sélectionnez **Créer un projet**.

### <a name="assign-a-resource-to-a-project"></a>Attribuer une ressource à un projet

1. Sur la page **Employés**, dans la liste **Employés**, sélectionnez l’enregistrement pour l’employé pour lequel vous avez précédemment configuré des compétences, et ouvrez l’enregistrement de l’employé.
2. Dans le volet Actions, sur l’onglet **Projet**, dans le groupe **Configuration**, sélectionnez **Attribuer les projets**.
3. Sur la page **Affectations de projets de validation de ressources**, sur l’onglet **Projets**, dans le champ **Ajouter le projet aux projets sélectionnés**, filtrez sur le projet **Mise à niveau XYZ Phase 2**.
4. Dans le volet **Projets restants**, sélectionnez un projet, puis sélectionnez le bouton fléché pour l’ajouter au volet **Projets sélectionnés**.

Vous pouvez également attribuer des catégories à une ressource selon vos besoins. Le type de catégorie est soit **Coût** soit **Revenu**. Le type de catégorie est déterminé par votre organisation. Si aucune catégorie n’est affectée à une ressource, Finance recherche la catégorie par défaut sur les prix horaires pour le coût et le revenu.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurer les caractéristiques des ressources et des rôles du projet

Un chef de projet peut utiliser la fonctionnalité de ressources de projet pour créer les rôles requis pour le projet. Les rôles peuvent être utilisés si les ressources confirmées sont toujours inconnues lorsque les ressources sont réservées. Les rôles peuvent être temporairement réservés en tant que ressources planifiées, afin que vous puissiez poursuivre les étapes de planification du projet.

[![Exemple de rôle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénario :** Contoso a été recruté pour mener à bien un projet Temps et matériel avec une charte de projet approuvée. Le chef de projet junior est toujours en train de compléter la portée du projet. Le responsable des ressources identifie actuellement des ressources spécifiques qui seront réservées pour travailler sur le nouveau projet. En raison de la nature critique du projet, le commanditaire a demandé le chef de projet senior comme l’un des rôles. Le responsable des ressources doit acquérir la nouvelle ressource et définir le rôle dans le système au cas où le chef de projet junior aurait besoin des informations sur la ressource lors de la planification du projet.

Les étapes suivantes montrent comment le responsable des ressources peut configurer le rôle de chef de projet principal et y associer des caractéristiques de ressource. Plus tard, le rôle peut être utilisé pour rechercher des ressources disponibles qui correspondent aux compétences de ressources requises.

1. Sur la page **Configurer les rôles**, sélectionnez **Nouveau**, et saisissez les valeurs suivantes :

    - **ID de rôle :** chef de projet senior
    - **Description :** chef de projet senior

2. Sélectionnez **Créer**.
3. Sélectionnez le rôle **Chef de projet senior**, puis **Configurer les caractéristiques**.
4. Dans le champ **Type de caractéristique**, sélectionnez **Compétence**.
5. Dans le champ **Caractéristiques disponibles**, entrez la compétence à rechercher.
6. Dans le champ **Type de caractéristique**, sélectionnez **Certificat**.
7. Dans le champ **Caractéristiques disponibles**, entrez le type de certificat à rechercher.

### <a name="assign-a-project-resource-to-a-project"></a>Attribuer une ressource de projet à un projet

1. Sur la page **Tous les projets**, sélectionnez le projet **Mise à niveau XYZ Phase 2**.
2. Sur l’onglet **Équipe de projet et planification**, sélectionnez **Ajouter**.
3. Dans le champ **Rôle**, sélectionnez **Membre de l’équipe**.
4. Sélectionnez **Réserver depuis le calendrier**.
5. Sur la page **Disponibilité des ressources**, sélectionnez **Paramètres d’affichage**.
6. Sur la page **Ajuster les paramètres d’affichage**, entrez les valeurs suivantes :

    - **Format d’affichage de la plage de dates :** Journée
    - **Afficher les descriptions de disponibilité :** Oui
    - **Afficher la capacité restante :** Oui

7. Dans la liste des ressources, sélectionnez une ressource.
8. Sélectionnez **Réservation ferme** et **Capacité maximale**.


### <a name="assign-a-resource-to-a-default-role"></a>Attribuer une ressource à un rôle par défaut

Pour aider les responsables de ressources ou les chefs de projets à explorer davantage les ressources qui peuvent être réservées pour un projet. Vous pouvez associer un rôle par défaut à une ressource existante ou à une ressource nouvellement acquise. Par exemple, lorsque Daniel a été embauché, il avait l’expérience et les compétences nécessaires pour remplir le rôle d’analyste d’affaires. Le responsable de ressources a attribué ce rôle comme rôle par défaut de Daniel. Par conséquent, le responsable des ressources a ajouté Daniel à un groupe d’analystes d’affaires disponibles pour travailler sur des projets.

Lors de la réservation de ressources, les chefs de projet peuvent filtrer les ressources de rôle disponibles pour travailler sur des projets. Ils peuvent utiliser ces informations comme un critère lorsqu’ils effectuent une analyse de décision multicritères pendant l’exécution des ressources. Ils peuvent également ajouter d’autres caractéristiques de ressources au filtre pour rechercher des ressources qui ont des compétences, une formation et une expérience spécifiques pour un projet donné.

**Scénario :** Un projet approuvé a démarré et le rôle de chef de projet principal a été réservé en tant que ressource planifiée pendant la phase de planification du projet. Le responsable des ressources a maintenant acquis une ressource pour remplir le rôle de chef de projet senior.

1. Sur la page **Liste des ressources**, sélectionnez **Daniel Goldschmidt**.
2. Sur la page **Rôle de la ressource**, sélectionnez **Nouveau**, et saisissez les valeurs suivantes :

    - **Efficace :** saisissez la date actuelle.
    - **Expiration :** saisissez **Jamais**.
    - **Rôle** : saisissez **Chef de projet senior**.

3. Cliquez sur **Enregistrer** puis fermez la page.
4. Sur l’onglet **Compétences**, ajoutez la compétence **ProjectMgmt** et le certificat **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurer la tarification basée sur les rôles
Tous les prix de coût, de vente et de transfert peuvent être définis pour les rôles.

1. Sur la page **Prix de vente (heure)**, sélectionnez **Nouveau** et saisissez une date de validité.
2. Dans la colonne **Rôle**, sélectionnez un rôle.
3. Dans la colonne **Tarification**, entrez un prix pour le rôle de ressource sélectionné.

## <a name="form-a-project-team"></a>Former une équipe de projet
Pour utiliser les rôles précédemment définis dans un projet, un chef de projet doit associer les rôles au projet. Plusieurs rôles peuvent être attribués à un projet. Pour éviter toute confusion, ces rôles sont automatiquement étiquetés lors de la réservation. Par exemple, si le chef de projet a besoin de trois ingénieurs en logiciel, trois rôles d’ingénieur en logiciel **ingénieur logiciel 1**, **ingénieur logiciel 2** et **ingénieur logiciel 3**, car leurs étiquettes sont automatiquement générées. Si des caractéristiques de rôle ont été précédemment définies pour le rôle, elles sont appliquées en tant que filtre lors des recherches d’une ressource. Des caractéristiques supplémentaires peuvent être ajoutées si nécessaire pour affiner davantage la recherche.

Les paramètres d’affichage peuvent également être personnalisés pour offrir une meilleure vue de la disponibilité des ressources. Il existe des options pour afficher la disponibilité horaire, quotidienne, hebdomadaire, mensuelle, trimestrielle et annuelle. Il existe également une option pour afficher la capacité disponible et restante sur les ressources. Cette option est utile pour la gestion du temps, lorsque vous estimez le temps disponible pour les activités ou la disponibilité des ressources.

Le chef de projet peut sélectionner un rôle sur la page, puis, s’il existe une ressource disponible qui répond à l’exigence, choisir de réserver une ressource pour remplir le rôle. Notez que les ressources ne doivent pas être réservées à ce stade de la phase de planification. Lorsque vous créez une structure de répartition du travail, vous pouvez remplacer les rôles par des ressources en personnel pour le projet. Si les rôles sont remplacés par des ressources dotées de personnel dans la structure de répartition du travail, la configuration des ressources met automatiquement à jour la liste et la planification de l’équipe de projet.

[![Liste des équipes de projet qui comprend à la fois les rôles et les ressources réelles](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Le chef de projet dispose de différentes options pour réserver une ressource pour un projet, telles que **Capacité restante**, **Capacité complète**, **Pourcentage de capacité** et **Préciser les heures**. Ces options de réservation peuvent être annulées à tout moment si les affectations de ressources changent. Deux types de réservation sont pris en charge :

- **Réservation ferme** : la réservation de ressources a été approuvée et confirmée pour travailler sur l’engagement pour la durée spécifiée.
- **Réservation temporaire** : les réservations de ressources était provisoirement défini pour travailler sur l’engagement pour la durée spécifiée.

La procédure suivante explique comment créer une équipe de projet.

### <a name="create-a-project-team"></a>Créer une équipe de projet

1. Sur la liste **Tous les projets**, sélectionnez un projet, puis **Modifier**.
2. Sur l’onglet **Équipe de projet et planification**, dans le champ **Date de fin de planification**, entrez la date de début de planification plus un mois. Par exemple, si la date de début de la planification est le 24 juin 2017 (24/06/2017), entrez **24/07/2017**.
3. Cliquez sur **Ajouter**.
4. Dans le volet **Ajouter des rôles au projet**, dans le champ **Rôle**, sélectionnez **Chef de projet senior**.
5. Sélectionnez **Compétences requises**.
6. Sur la page **Choisir les caractéristiques**, les caractéristiques que vous avez précédemment définies pour le rôle de chef de projet senior sont sélectionnées par défaut. Cliquez sur **OK**.
7. Sur la page **Ajouter des rôles au projet**, dans le champ **Nombre de ressources**, entrez **1**.
8. Dans le champ **Ressource**, la recherche affiche toutes les ressources possédant les compétences requises. Sélectionnez **Daniel Goldschmidt**, puis sélectionnez **Créer**.
9. Sélectionnez **Ajouter** sur la page **Projet**.
10. Dans le volet **Ajouter des rôles au projet**, dans le champ **Rôle**, sélectionnez **Membre de l’équipe**. Tapez **5** dans le champ **Nombre de ressources**.
11. Sélectionnez **Créer**.
12. Sur la page **Projets**, sélectionnez **Répondre à la ressource**.

## <a name="resource-capacity-synchronization"></a>Synchronisation de la capacité d’une ressource
Les processus de synchronisation des ressources permettent de garantir que les informations du calendrier et du calendrier de base se retrouvent dans la planification des ressources du projet. Si le calendrier est modifié, les processus apportent les mises à jour nécessaires à la planification des ressources du projet. Les processus contribuent également à améliorer les performances, car les informations sur les ressources du calendrier sont synchronisées à l’avance. Par conséquent, les mises à jour des informations de planification des ressources se produisent plus rapidement. Nous vous recommandons de planifier les processus comme un lot au lieu d’un à la fois. Sinon, il y a un risque que quelqu’un oublie les dates incluses lors de la dernière synchronisation des informations. Si les dates inclusives ne sont pas utilisées, des intervalles peuvent se produire lors de la synchronisation des dates.

![Synchronisation du calendrier](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchroniser les reports de la capacité d’une ressource

Le processus de synchronisation est conçu pour synchroniser toutes les informations du calendrier des ressources. Ces informations incluent des informations de calendrier de base sur les modifications apportées à la table de capacité du calendrier des ressources du projet. Si de nouvelles ressources sont ajoutées dans le projet, la synchronisation permet de garantir que les informations de calendrier mises à jour sont disponibles. Cette synchronisation peut être effectuée à tout moment.

Nous vous recommandons d’utiliser un lot. Les options sont disponibles lors de la synchronisation des réservations de capacité.

1. Sélectionnez **Gestion de projet et comptabilité** &gt; **Périodique** &gt; **Synchronisation de la capacité** &gt; **Synchroniser les cumuls de capacité des ressources**.
2. Définissez les options dans le tableau suivant.

    | Option      | Description |
    |-------------|-------------|
    | Code de période | Sélectionnez éventuellement le code d’intervalle de dates du grand livre général pour définir les dates de début et de fin du processus de synchronisation pour les cumuls de capacité de ressources. |
    | Date de début  | Entrez la date de début du processus de synchronisation pour les cumuls de capacité des ressources. |
    | Date de fin    | Entrez la date de fin du processus de synchronisation pour les cumuls de capacité des ressources. |

[![Processus de la synchronisation](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurer des rôles sur des modèles de structure de répartition du travail
Les chefs de projet peuvent configurer des modèles de structure de répartition du travail qu’ils peuvent appliquer lorsqu’ils créent une structure de répartition du travail pour de nouveaux projets. Les chefs de projet peuvent ajouter des rôles lorsqu’ils créent un modèle. Utilisez la procédure suivante pour attribuer un rôle à un modèle de structure de répartition du travail.

1. Sélectionnez **Gestion de projet et comptabilité** &gt; **Configurer**&gt; **Projets** &gt; **Modèles de structure de répartition du travail**.
2. Sélectionnez **Détails** pour un modèle de structure de répartition du travail sélectionné.
3. Sélectionnez une tâche dans la liste, puis, dans le champ **Rôle**, sélectionnez un rôle à attribuer à la tâche.

### <a name="work-with-a-wbs"></a>Utiliser une structure de répartition du travail

Vous pouvez créer une nouvelle structure de répartition du travail ou copier une structure de répartition du travail à partir d’un modèle de structure de répartition du travail existant. Un chef de projet peut facilement gérer les ressources en attribuant des rôles à de nouvelles tâches sur la structure de répartition du travail. Les rôles peuvent être remplacés après l’acquisition d’une ressource ou après l’identification d’une ressource confirmée pour travailler sur la tâche. Cette flexibilité permet aux chefs de projet d’effectuer les tâches suivantes :

- Identifiez le nombre de ressources requises pour les lots de travail de la structure de répartition du travail.
- Estimez les coûts de projet.
- Déterminez un budget préliminaire.
- Estimez la durée de l’activité en fonction des rôles et des ressources.
- Développez des plans de gestion de projet, basés sur les informations disponibles sur le projet.

Des options supplémentaires ont été ajoutées dans la structure de répartition du travail pour mieux utiliser la fonctionnalité des ressources.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Attributions de ressources</td>
<td>Affichez les ressources affectées, les dates, le nombre d’heures et le type de réservation pour les tâches sur la structure de répartition du travail.</td>
</tr>
<tr class="even">
<td>Générer automatiquement l’équipe</td>
<td>Ajoutez automatiquement des ressources planifiées à l’aide de rôles associés à une tâche. Finance suggère automatiquement des ressources planifiées à l’aide d’une analyse de décision multicritères basée sur les rôles. Une fois que les rôles et l’effort (heures) ont été définis pour les tâches dans une structure de répartition du travail et une fois la structure validée, sélectionnez <strong>Générer automatiquement une équipe</strong>. Le nombre requis de ressources planifiées est ajouté à la structure de répartition du travail et à l’onglet <strong>Planification des projets et des équipes</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (liste déroulante)</td>
<td>Sur la page <strong>Lancer l’affectation des ressources</strong>, vous pouvez sélectionner des ressources pour réservation ferme ou provisoire, selon la durée spécifiée. Vous pouvez ajuster les paramètres d’affichage pour voir et définir la durée des activités de ressources. Vous pouvez sélectionner et affecter des ressources au niveau du lot de travail à l’aide des options suivantes :
<ul>
<li><strong>Accepter</strong> : confirmez les modifications apportées à la ressource affectée à une tâche.</li>
<li><strong>Annuler</strong> : annulez les modifications apportées à la ressource affectée à une tâche.</li>
<li><strong>Attribuer automatiquement</strong> : une ressource disponible ayant un rôle correspondant est automatiquement sélectionnée et affectée à la tâche sélectionnée.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Sur la page **Tous les projets**, sélectionnez le projet **Mise à niveau XYZ Phase 2**.
2. Sélectionnez **Plan** &gt; **Activités** &gt; **Structure de répartition du travail**.
3. Sélectionnez **Nouveau** pour ajouter les activités de niveau un suivantes à la structure de répartition du travail :

    - Initiation
    - Planification
    - Exécution en cours
    - Surveillance et contrôle
    - Fermer

4. Réglez les dates et les efforts (heures), comme indiqué dans l’illustration suivante.

    [![Fixer les dates et les efforts](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Sélectionnez la ligne de tâche **Initier**, puis, dans le champ **Rôle**, sélectionnez **Chef de projet senior**.
6. Cliquez sur **Publier**.
7. Sur la même ligne, dans le champ **Ressource**, sélectionnez **Daniel Goldschmidt**, puis **Accepter**.
8. Sélectionnez la ligne de tâche **Planification**, puis, dans le champ **Rôle**, sélectionnez **Analyste d’affaires**.
9. Sélectionnez **Publier**, puis **Générer automatiquement une équipe**.
10. Dans la zone de message qui s’affiche, sélectionnez **Oui**.
11. Dans le champ **Ressource**, vérifiez que la valeur est **Analyste d’affaires 1**.
12. Pour la ressource **Analyste d’affaires 1**, ouvrez la recherche et sélectionnez **Lancer les affectations de ressources**. Sélectionnez ensuite un employeur pour la tâche.
13. Sélectionnez **Affectation provisoire** &gt; **Capacité complète**.

    > [!NOTE] 
    > Vous ne recevez pas d’avertissement indiquant que la ressource spécifiée est désormais 2, car le nombre de ressources reste 1.

14. Sur la page **Structure de répartition du travail**, validez l’affectation de ressource sur la structure de répartition du travail, puis sélectionnez **Enregistrer**.

## <a name="resource-fulfillment-for-planned-resources"></a>Exécution des ressources pour les ressources planifiées
Un chef de projet peut planifier les rôles de ressources requis pour un projet. Le responsable des ressources verra ces ressources planifiées comme des demandes sur la page **Exécution des ressources** et peut affecter des ressources réelles.

1. Sur la page **Tous les projets**, sélectionnez le projet **Mise à niveau XYZ Phase 2**.
2. Sélectionnez **Projet**, puis **Modifier**.
3. Sur l’onglet **Équipe de projet et planification**, sélectionnez **Ajouter**.
4. Dans la boîte de dialogue **Ajouter des rôles**, sélectionnez le rôle **Développeur de logiciels**.
5. Cliquez sur **Créer** puis fermez la page du projet.
6. Sur la page **Exécution des ressources**, sélectionnez **Développeur logiciel 1** pour le **Projet de mise à niveau XYZ Phase 2**.
7. Sélectionnez un employé, puis **Attribuer**.
8. Vérifiez que la ligne pour **Développeur logiciel 1** a été supprimée pour le projet **Projet de mise à niveau XYZ Phase 2**.
9. Sur l’onglet **Équipe de projet et planification**, pour le projet **Mise à niveau XYZ Phase 2**, vérifiez que l’employé que vous avez sélectionné à l’étape précédente a été ajouté en tant que **Développeur de logiciels**.

## <a name="requests-for-project-resources"></a>Demandes de ressources de projet
La fonctionnalité de planification des ressources de projet permet uniquement aux responsables des ressources de distribuer les ressources en personnel sur les engagements ou les projets. Pour activer cette fonctionnalité, effectuez les tâches suivantes ou vérifiez qu’elles ont été effectuées :

- Configurez des séquences de numéros.
- Configurer les workflows de gestion et de comptabilité des projets
- Activez les workflows de demande de ressources.

Une fois les tâches précédentes terminées, vous pouvez effectuer les tâches suivantes selon vos besoins :

- Créez une demande de ressource à partir d’une ressource à réservation souple.
- Surveillez les demandes de ressources.
- Répondez aux demandes de ressources.
- Demandez une ressource en personnel à une structure de répartition du travail.
- Réservez des ressources pour un projet sans avoir de demande de ressource en personnel.

## <a name="monitor-project-teams"></a>Surveiller les équipes de projet
1. Sur la page **Tous les projets**, sélectionnez l’**ID de projet** pour le projet **Mise à niveau XYZ Phase 2**.
2. Sur le raccourci **Équipe de projet et planification**, vérifiez que les ressources de projet répertoriées sont correctes.
