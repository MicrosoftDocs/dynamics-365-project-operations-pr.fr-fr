---
title: Créer un projet
description: Cet article fournit des informations sur la manière de créer un projet.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbe7ea7d6ee57b3494494a2758dbcb7ded735dc1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919689"
---
# <a name="create-a-new-project"></a>Créer un projet

[!include [banner](../includes/banner.md)]

Procédez comme suit pour créer un projet.

1. Sur la page **Gestion de projet**, sélectionnez **Nouveau projet**, et saisissez les valeurs suivantes :

    - **Type de projet :** Temps et matériel
    - **Nom du projet :** Mise à niveau XYZ Phase 2
    - **Groupe de projets :** TM\_TEC
    - **ID de contrat du projet :** 00000002

2. Sélectionnez **Créer un projet**.

## <a name="assign-a-resource-to-a-project"></a>Attribuer une ressource à un projet

1. Sur la page **Employés**, dans la liste **Employés**, sélectionnez l’enregistrement pour l’employé pour lequel vous avez précédemment configuré des compétences, et ouvrez l’enregistrement de l’employé.
2. Dans le volet Actions, sur l’onglet **Projet**, dans le groupe **Configuration**, sélectionnez **Attribuer les projets**.
3. Sur la page **Affectations de projets de validation de ressources**, sur l’onglet **Projets**, dans le champ **Ajouter le projet aux projets sélectionnés**, filtrez sur le projet **Mise à niveau XYZ Phase 2**.
4. Dans le volet **Projets restants**, sélectionnez un projet, puis sélectionnez le bouton fléché pour l’ajouter au volet **Projets sélectionnés**.

Vous pouvez également attribuer des catégories à une ressource selon vos besoins. Le type de catégorie est soit **Coût** soit **Revenu**. Le type de catégorie est déterminé par votre organisation. Si aucune catégorie n’est affectée à une ressource, Finance recherche la catégorie par défaut sur les prix horaires pour le coût et le revenu.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurer les caractéristiques des ressources et des rôles du projet

Un chef de projet peut utiliser la fonctionnalité de ressources de projet pour créer les rôles requis pour le projet. Les rôles peuvent être utilisés si les ressources confirmées sont toujours inconnues lorsque les ressources sont réservées. Les rôles peuvent être temporairement réservés en tant que ressources planifiées, afin que vous puissiez poursuivre les étapes de planification du projet.

[![Exemple de rôle.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

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

## <a name="assign-a-project-resource-to-a-project"></a>Attribuer une ressource de projet à un projet

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

## <a name="assign-a-resource-to-a-default-role"></a>Attribuer une ressource à un rôle par défaut

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]