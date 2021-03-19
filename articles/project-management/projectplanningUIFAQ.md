---
title: Résolution des problèmes lors de l’utilisation de la grille des tâches
description: Cette rubrique fournit les informations de dépannage nécessaires lorsque vous travaillez dans la grille des tâches.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286560"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Résolution des problèmes lors de l’utilisation de la grille des tâches 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Ce sujet décrit comment résoudre les problèmes que vous pourriez rencontrer en travaillant avec la gestion des coûts.

## <a name="enable-cookies"></a>Activer les cookies

Project Operations nécessite que les cookies tiers soient activés afin de rendre la structure de répartition du travail. Lorsque les cookies tiers ne sont pas activés, au lieu de voir les tâches, vous verrez une page vierge lorsque vous sélectionnez l'onglet **Tâches** sur la page **Projet**.

![Onglet vide lorsque les cookies tiers ne sont pas activés](media/blankschedule.png)


### <a name="workaround"></a>Solution de contournement
Pour Microsoft Edge ou les navigateurs Google Chrome, les procédures suivantes décrivent comment mettre à jour les paramètres de votre navigateur pour activer les cookies tiers.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Ouvrez votre navigateur Edge.
2. Dans l’angle supérieur droit, sélectionnez les **points de suspension** (...), puis **Paramètres**.
3. En dessous de **Cookies et autorisations du site**, sélectionnez **Cookies et données de site**.
4. Désactivez **Bloquer les cookies tiers**.

#### <a name="google-chrome"></a>Google Chrome

1. Ouvrez votre navigateur Chrome.
2. Dans l'angle supérieur droit, sélectionnez les trois points verticaux, puis sélectionnez **Paramètres**.
3. En dessous de **Confidentialité et sécurité**, sélectionnez **Cookies et autres données de site**.
4. Sélectionnez **Autoriser tous les cookies**.

> [!IMPORTANT]
> Si vous bloquez les cookies tiers, tous les cookies et données de site d'autres sites seront bloqués, même si le site est autorisé sur votre liste d'exceptions.

## <a name="pex-endpoint"></a>Point de terminaison PEX

Project Operations requiert qu'un paramètre de projet fasse référence au point de terminaison PEX. Ce point de terminaison est nécessaire pour communiquer avec le service utilisé pour rendre la structure de répartition du travail. Si le paramètre n'est pas activé, vous recevrez l'erreur "Le paramètre de projet n'est pas valide". 

### <a name="workaround"></a>Solution de contournement
 ![Champ Point de terminaison PEX sur le paramètre de projet](media/projectparameter.png)

1. Ajoutez le champ **Point de terminaison PEX** à la page **Paramètres du projet**.
2. Mettez à jour le champ avec la valeur suivante : `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Supprimez le champ de la page **Paramètres du projet**.

## <a name="privileges-for-project-for-the-web"></a>Privilèges pour Projet pour le web

Project Operations s'appuie sur un service de planification externe. Le service exige qu'un utilisateur dispose de plusieurs rôles attribués pour lire et écrire sur des entités liées à la structure de répartition du travail. Ces entités incluent les tâches de projet, les affectations de ressources et les dépendances de tâches. Si un utilisateur ne peut pas rendre la structure de répartition du travail lorsqu'il accède à l'onglet **Tâches**, c'est probablement parce que Projet pour Project Operations n'a pas été activé. Un utilisateur peut recevoir soit une erreur rôle de sécurité, soit une erreur liée à un refus d'accès.


## <a name="workaround"></a>Solution de contournement

1. Accédez à **Paramètres > Sécurité > Utilisateurs > Utilisateurs de l'application**.  

   ![Lecteur d'application](media/applicationuser.jpg)
   
2. Double-cliquez sur l'enregistrement d'utilisateur de l'application pour vérifier ce qui suit :

 - L’utilisateur a accès au projet. Cette vérification est généralement effectuée en s'assurant que l'utilisateur a un rôle de sécurité de **Chef de projet**.
 - L'utilisateur de l'application Microsoft Project existe et est configuré correctement.
 
3. Si cet utilisateur n’existe pas, vous pouvez en un enregistrement d'utilisateur. Sélectionnez **Nouveaux utilisateurs**. Remplacez le formulaire de saisie par **Utilisateur de l'application**, puis ajoutez l'**ID d'application**.

   ![Détails de l'utilisateur de l'application](media/applicationuserdetails.jpg)

4. Vérifiez que l'utilisateur a reçu la licence correcte et que le service est activé dans les détails des plans de service de la licence.
5. Vérifiez que l'utilisateur peut ouvrir project.microsoft.com.
6. Vérifiez à travers les paramètres du projet que le système pointe vers le bon point de terminaison du projet.
7. Vérifier que l'utilisateur de l'application de projet est créée.
8. Appliquez les rôles de sécurité suivants à l'utilisateur :

  - Utilisateur de Dataverse
  - Système de Project Operations
  - Système de projet

## <a name="error-when-updating-the-work-breakdown-structure"></a>Erreur lors de la mise à jour de la structure de répartition du travail

Lorsqu'une ou plusieurs mises à jour sont apportées à la structure de répartition du travail, les modifications échouent finalement et ne sont pas enregistrées. Une erreur se produit dans la grille de planification indiquant que « La modification récente que vous avez apportée n'a pas pu être enregistrée. »

### <a name="workaround"></a>Solution de contournement

1. Vérifiez que l'utilisateur a reçu la licence correcte et que le service est activé dans les détails des plans de service de la licence.
2. Vérifiez que l'utilisateur peut ouvrir project.microsoft.com.
3. Vérifiez que le système pointe vers le bon point de terminaison du projet.
4. Vérifier que l'utilisateur de l'application de projet a été créé.
5. Appliquez les rôles de sécurité suivants à l'utilisateur :
  
  - Utilisateur ou utilisateur de base Dataverse
  - Système de Project Operations
  - Système de projet
  - Système de double écriture Project Operations (ce rôle est requis si vous déployez le scénario basé sur les ressources/non stocké de Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]