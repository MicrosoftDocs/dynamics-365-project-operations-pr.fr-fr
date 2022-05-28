---
title: Résolution des problèmes lors de l’utilisation de la grille des tâches
description: Cette rubrique fournit les informations de dépannage nécessaires lorsque vous travaillez dans la grille des tâches.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: ee80363cf6f9a65a91be43a84434d37f02511f26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596415"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Résolution des problèmes lors de l’utilisation de la grille des tâches 


_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés, déploiement simplifié : traiter la facturation pro forma, Project for the Web_

La grille de tâches exploitée par Dynamics 365 Project Operations est un iFrame hébergé dans Microsoft Dataverse. Ainsi, des exigences spécifiques doivent être remplies pour garantir le bon fonctionnement de l’authentification et de l’autorisation. Cette rubrique décrit les problèmes courants qui peuvent avoir un impact sur l’affichage de la grille ou la gestion des tâches dans la structure de répartition du travail (WBS).

Les problèmes courants sont les suivants :

- L’onglet **Tâche** sur la grille des tâches est vide.
- Lors de l’ouverture du projet, ce dernier ne se charge pas et l’interface utilisateur (IU) est bloquée sur le compteur.
- Administration des privilèges pour **Projet for the Web**.
- Les modifications ne sont pas enregistrées si vous créez, mettez à jour ou supprimez une tâche.

## <a name="issue-the-task-tab-is-empty"></a>Problème : l’onglet Tâche est vide

### <a name="mitigation-1-enable-cookies"></a>Atténuation 1 : activer les cookies

Project Operations exige que les cookies tiers soient activés pour afficher la structure de répartition du travail. Lorsque les cookies tiers ne sont pas activés, au lieu de voir les tâches, vous verrez une page vierge lorsque vous sélectionnez l’onglet **Tâches** sur la page **Projet**.

Pour Microsoft Edge ou les navigateurs Google Chrome, les procédures suivantes décrivent comment mettre à jour les paramètres de votre navigateur pour activer les cookies tiers.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Ouvrez votre navigateur Edge.
2. Dans l’angle supérieur droit, sélectionnez les **points de suspension** (...), puis **Paramètres**.
3. En dessous de **Cookies et autorisations du site**, sélectionnez **Cookies et données de site**.
4. Désactivez **Bloquer les cookies tiers**.
5. Actualisez votre navigateur. 

#### <a name="google-chrome"></a>Google Chrome

1. Ouvrez votre navigateur Chrome.
2. Dans l’angle supérieur droit, sélectionnez les trois points verticaux, puis sélectionnez **Paramètres**.
3. En dessous de **Confidentialité et sécurité**, sélectionnez **Cookies et autres données de site**.
4. Sélectionnez **Autoriser tous les cookies**.
5. Actualisez votre navigateur. 

> [!NOTE]
> Si vous bloquez les cookies tiers, tous les cookies et données de site d’autres sites seront bloqués, même si le site est autorisé sur votre liste d’exceptions.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Atténuation 2 : vérifier que le point de terminaison PEX est correctement configuré

Project Operations requiert qu’un paramètre de projet fasse référence au point de terminaison PEX. Ce point de terminaison est requis pour communiquer avec le service utilisé pour afficher la structure de répartition du travail. Si le paramètre n’est pas activé, vous recevrez l’erreur "Le paramètre de projet n’est pas valide". Pour mettre à jour le point de terminaison PEX, procédez comme suit.

1. Ajoutez le champ **Point de terminaison PEX** à la page **Paramètres du projet**.
2. Identifiez le type de produit que vous utilisez. Cette valeur est utilisée lorsque le point de terminaison PEX est défini. Lors de la récupération, le type de produit est déjà défini dans le point de terminaison PEX. Conservez cette valeur.
3. Mettez à jour le champ avec la valeur suivante : `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Le tableau suivant fournit le paramètre de type à utiliser selon le type de produit.

      | **Type de produit**                     | **Paramètre de type** |
      |--------------------------------------|--------------------|
      | Project for the Web sur l’organisation par défaut   | type=0             |
      | Project for the Web sur l’organisation nommée CDS | type=1             |
      | Project Operations                   | type=2             |

4. Supprimez le champ de la page **Paramètres du projet**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Atténuation 3 : Se connecter à project.microsoft.com
Dans votre navigateur Microsoft Edge, ouvrez un nouvel onglet, accédez à project.microsoft.com et connectez-vous en utilisant le rôle d’utilisateur que vous utilisez pour accéder à Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problème : le projet ne se charge pas et l’interface utilisateur est bloquée sur le compteur

Pour l’authentification, les fenêtres contextuelles doivent être activées pour que la grille de tâches se charge. Si les fenêtres contextuelles ne sont pas activées, l’écran est bloqué sur le compteur en chargement. L’illustration suivante montre l’URL avec une étiquette contextuelle bloquée dans la barre d’adresse, ce qui a pour conséquence de bloquer le compteur lorsqu’il essaie de charger la page. 

   ![Compteur coincé et blocage des fenêtres contextuelles.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Atténuation 1 : activer les fenêtres contextuelles

Si le projet est bloqué sur le compteur, il est possible que les fenêtres contextuelles ne soient pas activées.

#### <a name="microsoft-edge"></a>Microsoft Edge

Il existe deux façons d’activer les fenêtres contextuelles dans le navigateur Edge.

1. Dans le navigateur Edge, sélectionnez la notification dans le coin supérieur droit du navigateur.
2. Sélectionnez **Toujours autoriser les fenêtres contextuelles et les redirections depuis** l’environnement Dataverse donné.
 
     ![Fenêtre des fenêtres contextuelles bloquée.](media/enablepopups.png)

Sinon, vous pouvez terminer les étapes suivantes.

1. Ouvrez votre navigateur Edge.
2. Dans le coin supérieur droit, sélectionnez l’**ellipse** (...), puis sélectionnez **Paramètres** > **Autorisations du site** > **Fenêtres contextuelles et redirections**.
3. Désactivez **Fenêtres contextuelles et redirections** pour les fenêtres contextuelles de blocage ou activez cette option pour autoriser les fenêtres contextuelles sur votre appareil.
4. Une fois les fenêtres contextuelles activées, actualisez le navigateur. 

#### <a name="google-chrome"></a>Google Chrome
1. Ouvrez votre navigateur Chrome.
2. Accédez à une page qui contient des fenêtres contextuelles bloquées.
3. Dans la barre d’adresse, sélectionnez **Fenêtre contextuelle bloquée**.
4. Sélectionnez le lien de la fenêtre contextuelle que vous souhaitez voir.
5. Une fois les fenêtres contextuelles activées, actualisez le navigateur. 

> [!NOTE]
> Pour toujours afficher les fenêtres contextuelles, sélectionnez **Toujours autoriser les fenêtres contextuelles et les redirections depuis [site]**, puis cliquez sur **Terminé**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problème 3 : administration des privilèges pour Projet for the Web

Project Operations s’appuie sur un service de planification externe. Le service exige qu’un utilisateur soit associé à plusieurs rôles qui lui permettent de lire et d’écrire dans des entités liées à WBS. Ces entités incluent les tâches de projet, les affectations de ressources et les dépendances de tâches. Si un utilisateur ne peut pas afficher WBS lorsqu’il accède à l’onglet **Tâches**, il est probable que **Project** pour **Project Operations** ne soit pas activé. Un utilisateur peut recevoir soit une erreur rôle de sécurité, soit une erreur liée à un refus d’accès.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Atténuation 1 : valider l’utilisation de l’application et les rôles de sécurité de l’utilisateur final

1. Accédez à **Paramètres** > **Sécurité** > **Utilisateurs** > **Utilisateurs de l’application**.  

   ![Lecteur d’application.](media/applicationuser.jpg)
   
2. Cliquez deux fois sur l’enregistrement de l’utilisateur de l’application pour vérifier les points suivants :

     - L’utilisateur a accès au projet. Vous pouvez le faire en vérifiant que l’utilisateur a le rôle de sécurité **Chef de projet**.
     - L’utilisateur de l’application Microsoft Project existe et est configuré correctement.
 
3. Si cet utilisateur n’existe pas, créez un enregistrement d’utilisateur. 
4. Sélectionnez **Nouveaux utilisateurs**, passez le formulaire de saisie sur **Utilisateur de l’application**, puis ajoutez l’**ID application**.

   ![Détails de l’utilisateur de l’application.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problème 4 : les modifications ne sont pas enregistrées si vous créez, mettez à jour ou supprimez une tâche

Si vous effectuez une ou plusieurs mises à jour de WBS, les modifications échouent et ne sont pas enregistrées. Une erreur se produit dans la grille de planification avec un message indiquant : « La modification récemment apportée n’a pas pu être enregistrée ».

### <a name="mitigation-1-validate-the-license-assignment"></a>Atténuation 1 : valider l’attribution de licence

1. Vérifiez que l’utilisateur a reçu la licence correcte et que le service est activé dans les détails des plans de service de la licence.  
2. Vérifiez que l’utilisateur peut ouvrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Atténuation 2 : Validation de la configuration de l’utilisateur de l’application Project
1. Vérifiez que l’utilisateur de l’application Project est bien créé.
2. Appliquez les rôles de sécurité suivants à l’utilisateur :
  
  - Utilisateur ou utilisateur de base Dataverse
  - Système de Project Operations
  - Système de projet
  - Systèmes de double écriture de Project Operations. Ce rôle est exigé pour le scénario de déploiement basé sur les ressources/produits non stockés de Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
