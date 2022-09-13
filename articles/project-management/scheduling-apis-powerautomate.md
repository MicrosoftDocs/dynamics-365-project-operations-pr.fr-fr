---
title: Utiliser les API de planification de projets avec Power Automate
description: Cet article fournit un exemple de flux qui utilise les interfaces de programmation d’application (API) de planification de projet.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404397"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Utiliser les API de planification de projets avec Power Automate

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Cet article décrit un exemple de flux qui montre comment créer un plan de projet complet en utilisant Microsoft Power Automate, comment créer un jeu d’opérations et comment mettre à jour une entité. L’exemple montre comment créer un projet, un membre d’équipe de projet, des groupes d’opérations, des tâches de projet et des affectations de ressources. Cet article explique également comment mettre à jour une entité et exécuter un groupe d’opérations.

Voici une liste complète des étapes documentées dans l’exemple de flux dans cet article :

1. [Créer un déclencheur PowerApps](#1)
2. [Créer un projet](#2)
3. [Initialiser une variable pour le membre de l’équipe](#3)
4. [Créer un membre de l’équipe générique](#4)
5. [Créer un groupe d’opérations](#5)
6. [Créer un compartiment de projet](#6)
7. [Initialiser une variable pour le statut du lien](#7)
8. [Initialiser une variable pour le nombre de tâches](#8)
9. [Initialiser une variable pour l’ID de tâches de projet](#9)
10. [Exécuter jusqu’à](#10)
11. [Définir une tâche de projet](#11)
12. [Créer une tâche de projet](#12)
13. [Créer une attribution de ressource](#13)
14. [Décrémenter une variable](#14)
15. [Renommer une tâche de projet](#15)
16. [Exécuter un groupe d’opérations](#16)

## <a name="assumptions"></a>Hypothèses

Cet article suppose que vous avez une connaissance de base de la plateforme Dataverse, des flux de cloud et de l’interface de programmation d’application (API) de planification de projet. Pour plus d’informations, voir la section [Références](#references) plus loin dans cet article.

## <a name="create-a-flow"></a>Créer un flux

### <a name="select-an-environment"></a>Sélectionner un environnement

Vous pouvez créer le flux Power Automate dans votre environnement.

1. Accédez à <https://flow.microsoft.com> et utilisez vos identifiants d’administrateur pour vous connecter.
2. Dans l’angle supérieur droit, sélectionnez **Environnements**.
3. Dans la liste, sélectionnez l’environnement dans lequel Dynamics 365 Project Operations est installé.

### <a name="create-a-solution"></a>Créer une solution

Effectuez les étapes suivantes pour créer un [flux basé sur une solution](/power-automate/overview-solution-flows). En créant un flux prenant en charge la solution, vous pouvez plus facilement exporter le flux pour l’utiliser ultérieurement.

1. Dans le volet de navigation de gauche, sélectionnez **Solutions**.
2. Sur la page **Solutions**, sélectionnez **Nouvelle solution**.
3. Dans la boîte de dialogue **Nouvelle solution**, définissez les champs obligatoires, puis les sélectionnez **Créer**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Étape 1 : créer un déclencheur PowerApps

1. Sur la page **Solutions**, choisissez la solution Mon automatisation que vous avez créée, puis sélectionnez **Nouveau**.
2. Dans le volet de gauche, sélectionnez **Flux de cloud** \> **Automatisation** \> **Flux de cloud** \> **Instantané**.
3. Dans le champ **Nom du flux**, entrez **Planifier le flux de démonstration de l’API**.
4. Dans la liste **Choisir comment déclencher ce flux**, sélectionnez **Power Apps**. Lorsque vous créez un déclencheur Power Apps, la logique dépend de vous en tant qu’auteur. Dans cet article, laissez les paramètres d’entrée vides à des fins de test.
5. Cliquez sur **Créer**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Étape 2 : Créer un projet

Procédez comme suit pour créer un exemple de projet.

1. Dans le flux que vous avez créé, sélectionnez **Nouvelle étape**.

    ![Ajout d’une nouvelle étape.](media/newstep.png)

2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.

    ![Sélection d’une opération.](media/chooseactiontab.png)

3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.

![Renommer une étape.](media/renamestep.png)

4. Renommer l’étape **Créer un projet**.
5. Dans le champ **Nom d’action**, sélectionnez **msdyn\_CreateProjectV1**.
6. Sous le champ **msdyn\_subject**, sélectionnez **Ajouter un contenu dynamique**.
7. Sur l’onglet **Expression**, dans le champ de fonction, entrez **Nom du projet - utcNow()**.
8. Cliquez sur **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Étape 3 : Initialiser une variable pour le membre de l’équipe

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **initialiser une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Membre de l’équipe Init**.
5. Dans le champ **Nom**, saisissez **TeamMemberAction**.
6. Dans le champ **Type**, sélectionnez **Chaîne**.
7. Dans le champ **Valeur**, saisissez **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Étape 4 : Créer un membre de l’équipe générique

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Créer un membre de l’équipe**.
5. Pour le champ **Nom de l’action**, sélectionnez **TeamMemberAction** dans la boîte de dialogue **Contenu dynamique**.
6. Dans le champ **Paramètres d’action**, entrez les informations de paramètre suivantes.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Voici une explication des paramètres :

    - **\@\@odata.type** – Nom de l’entité. Par exemple, saisissez **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – La clé primaire de l’ID de l’équipe du projet. La valeur est une expression d’identificateur global unique (GUID).   L’ID est généré à partir de l’onglet d’expression.

    - **msdyn\_project\@odata.bind** – L’ID de projet du projet propriétaire. La valeur a un contenu dynamique provenant de la réponse de l’étape « Créer un projet ». Assurez-vous de saisir le chemin d’accès complet et d’ajouter du contenu dynamique entre parenthèses. Les guillemets sont obligatoires. Par exemple, saisissez **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Nom du membre de l’équipe. Par exemple, saisissez **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Étape 5 : Créer un groupe d’opérations

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Créer un groupe d’opérations**.
5. Dans le champ **Nom de l’action**, sélectionnez l’action personnalisée **msdyn\_CreateOperationSetV1** Dataverse.
6. Dans le champ **Description**, saisissez **ScheduleAPIDemoOperationSet**.
7. Dans le champ **Projet**, saisissez **/msdyn\_projects(**.
8. Dans la boîte de dialogue **Contenu dynamique**, sélectionnez **msdyn\_CreateProjectV1Response ProjectId**.
9. Dans le champ **Projet**, saisissez  **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Étape 6 : Créer un compartiment de projet

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **ajouter une nouvelle ligne**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommer l’étape **Créer un compartiment**.
5. Dans le champ **Nom de table**, sélectionnez **Compartiments de projet**.
6. Dans le champ **Nom**, entrez **ScheduleAPIDemoBucket1**.
7. Pour le champ **Projet**, sélectionnez **msdyn\_CreateProjectV1Response ProjectId** dans la boîte de dialogue **Contenu dynamique**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Étape 7 : Initialiser une variable pour le statut du lien

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **initialiser une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommer l’étape **Init linkstatus**.
5. Dans le champ **Nom**, entrez **linkstatus**.
6. Dans le champ **Type**, sélectionnez **Entier**.
7. Dans le champ **Valeur**, saisissez **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Étape 8 : Initialiser une variable pour le nombre de tâches

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **initialiser une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommer l’étape **Init Nombre de tâches**.
5. Dans le champ **Nom**, saisissez **nombre de tâches**.
6. Dans le champ **Type**, sélectionnez **Entier**.
7. Dans le champ **Valeur**, saisissez **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Étape 9 : Initialiser une variable pour l’ID de tâches de projet

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **initialiser une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Init ProjectTaskID**.
5. Dans le champ **Nom**, saisissez **nombre de tâches**.
6. Dans le champ **Type**, sélectionnez **Chaîne**.
7. Pour le champ **Valeur**, entrez **guid()** dans le générateur d’expressions.

## <a name="step-10-do-until"></a><a id="10"></a>Étape 10 : Exécuter jusqu’à

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **exécuter jusqu’à**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Définissez la première valeur de l’instruction conditionnelle sur la variable **nombre de tâches** depuis la boîte de dialogue **Contenu dynamique**.
4. Définissez la condition sur **valeur inférieure ou égale à**.
5. Définissez la deuxième valeur de l’instruction conditionnelle sur **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Étape 11 : Définir une tâche de projet

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **définir une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans la nouvelle étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Définir la tâche de projet**.
5. Dans le champ **Nom**, sélectionnez **msdyn\_projectaskid**.
6. Pour le champ **Valeur**, entrez **guid()** dans le générateur d’expressions.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Étape 12 : Créer une tâche de projet

Suivez ces étapes pour créer une tâche de projet dotée d’un ID unique appartenant au projet actuel et au compartiment de projet que vous avez créé.

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans l’étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Créer une tâche de projet**.
5. Dans le champ **Nom d’action**, sélectionnez **msdyn\_PssCreateV1**.
6. Dans le champ **Entité**, entrez les informations de paramètre suivantes.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Voici une explication des paramètres :

    - **\@\@odata.type** – Nom de l’entité. Par exemple, saisissez **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID unique de la tâche. La valeur doit être définie sur une variable dynamique à partir de **msdyn\_proejcttaskid**.
    - **msdyn\_project\@odata.bind** – L’ID de projet du projet propriétaire. La valeur a un contenu dynamique provenant de la réponse de l’étape « Créer un projet ». Assurez-vous de saisir le chemin d’accès complet et d’ajouter du contenu dynamique entre parenthèses. Les guillemets sont obligatoires. Par exemple, saisissez **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – N’importe quel nom de tâche.
    - **msdyn\_ projectbucket\@odata.bind** – Compartiment du projet qui contient les tâches. La valeur a un contenu dynamique provenant de la réponse de l’étape « Créer un compartiment ». Assurez-vous de saisir le chemin d’accès complet et d’ajouter du contenu dynamique entre parenthèses. Les guillemets sont obligatoires. Par exemple, saisissez **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Contenu dynamique pour la date de début. Par exemple, demain sera représenté comme **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Date de début prévue. Par exemple, demain sera représenté comme **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Date de fin prévue. Sélectionnez une date à l’avenir. Par exemple, spécifiez **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Statut du lien. Par exemple, entrez **"192350000"**.

7. Pour le champ **OperationSetId**, sélectionnez **msdyn\_CreateOperationSetV1Response** dans la boîte de dialogue **Contenu dynamique**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Étape 13 : Créer une affectation de ressources

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans l’étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommer l’étape **Créer une affectation**.
5. Dans le champ **Nom d’action**, sélectionnez **msdyn\_PssCreateV1**.
6. Dans le champ **Entité**, entrez les informations de paramètre suivantes.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Pour le champ **OperationSetId**, sélectionnez **msdyn\_CreateOperationSetV1Response** dans la boîte de dialogue **Contenu dynamique**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Étape 14 : Décrémenter une variable

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **décrémenter une variable**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans le champ **Nom**, sélectionnez **nombre de tâches**.
4. Dans le champ **Valeur**, saisissez **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Étape 15 : Renommer une tâche de projet

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans l’étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Renommer une tâche de projet**.
5. Dans le champ **Nom d’action**, sélectionnez **msdyn\_PssUpdateV1**.
6. Dans le champ **Entité**, entrez les informations de paramètre suivantes.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pour le champ **OperationSetId**, sélectionnez **msdyn\_CreateOperationSetV1Response** dans la boîte de dialogue **Contenu dynamique**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Étape 16 : Exécuter un groupe d’opérations

1. Dans le flux, sélectionnez **Nouvelle étape**.
2. Dans la boîte de dialogue **Choisir une opération**, dans le champ de recherche, saisissez **effectuer une action non liée**. Ensuite, sur l’onglet **Actions**, sélectionnez l’opération dans la liste des résultats.
3. Dans l’étape, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.
4. Renommez l’étape **Exécuter un groupe d’opérations**.
5. Dans le champ **Nom d’action**, sélectionnez **msdyn\_ExecuteOperationSetV1**.
6. Pour le champ **OperationSetId**, sélectionnez **msdyn\_CreateOperationSetV1Response OperationSetId** dans la boîte de dialogue **Contenu dynamique**.

## <a name="references"></a>Références

- [Présentation de la façon d’intégrer les flux avec Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification](schedule-api-preview.md)
- [Vue d’ensemble des flux de cloud - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Présentation des flux prenant en charge une solution - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
