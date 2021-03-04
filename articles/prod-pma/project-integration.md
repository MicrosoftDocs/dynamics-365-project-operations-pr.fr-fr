---
title: Intégration de Microsoft Project Client
description: La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche. L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075801"
---
# <a name="microsoft-project-client-integration"></a>Intégration de Microsoft Project Client

[!include [banner](../includes/banner.md)]

La planification et la gestion d’un calendrier de projet peuvent être complexes, les chefs de projet doivent donc utiliser des outils qui les aident à gérer cette tâche. L’intégration à Microsoft Project Client permet d’ouvrir et de gérer une structure de répartition du travail de projet. Le chef de projet peut publier tout changement dans la structure de répartition du travail du projet Dynamics 365 Finance.

> [!NOTE]
> Si vous utilisez la mise à jour de juillet (version 10.0.4), vous devez installer KB 4054797 et 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurer le complément Microsoft Project Client
Pour activer l’intégration avec Microsoft Project Client, un complément Microsoft Dynamics 365 doit être installé dans l’application client Microsoft Project de l’utilisateur. Cela se fait en ouvrant l’ **Espace de travail de gestion de projet**.

• Cliquez sur **Configurer le complément client du projet** depuis la section **Liens** > **Configurer** de l’espace de travail.

• Cliquez sur **Ouvrir** , puis cliquez sur **Exécuter** à l’invite.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Ouvrir et modifier un brouillon de structure de répartition du travail existant dans Microsoft Project Client
Si un projet dans Dynamics 365 Finance a déjà créé une structure de répartition du travail, la structure de répartition du travail peut être ouverte dans l’application Microsoft Project Client si la structure de répartition du travail est à l’état de brouillon. Pour ouvrir depuis la page **Projet** , cliquez sur le lien **Ouvrir dans Microsoft Project** depuis l’onglet **Plan**. Cette page peut également être ouverte à partir de l’application Microsoft Project Client en cliquant sur **Ouvrir** dans l’onglet **Microsoft Dynamics 365**. Sélectionnez l’ **Entité juridique** et **Projet** depuis la liste.

> [!NOTE]
> Si vous utilisez Internet Explorer comme navigateur, vous devrez cliquer sur **Enregistrer** pour ouvrir manuellement à partir de l’emplacement de téléchargement du fichier. Ou cliquez sur **Enregistrer et ouvrir** pour ouvrir le fichier dans Microsoft Project Client. Ne renommez pas le nom du fichier lors de l’enregistrement.

Avant d’apporter des modifications au fichier à l’aide de Microsoft Project Client, vous devez l’extraire. Cliquez sur **Extraire** dans l’onglet **Microsoft Dynamics 365**. Cela empêchera les autres utilisateurs de modifier la structure de répartition du travail à partir de Finance en même temps. Pour publier la structure de répartition du travail après avoir effectué les modifications, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.

Si une équipe de projet a déjà été ajoutée au projet dans Finance, la liste des ressources sera remplie avec les membres de l’équipe. Si une équipe de projet n’a pas encore été ajoutée au projet, vous pouvez sélectionner des ressources et créer l’équipe dans Microsoft Project Client en cliquant sur le bouton **Ressources** sur l’onglet **Microsoft Dynamics 365**. 

Les données suivantes seront synchronisées avec Finance dans le cadre du processus d’archivage :

•   Nom de tâche

•   Date de début

•   Date de fin

•   Prédécesseurs

•   Noms de ressource

•   Catégorie

•   Catégorie de ressources

•   Heures de travail

•   Remarques

•   Priorité

> [!NOTE]
> Si vous ajoutez d’autres colonnes à votre fichier Microsoft Project Client, elles ne seront pas enregistrées dans le fichier et ne seront pas affichées lorsque le fichier sera à nouveau ouvert.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Créer la structure de répartition du travail pour un projet existant à l’aide de Microsoft Project Client
Pour créer une structure de répartition du travail à l’aide de Microsoft Project Client, procédez comme suit :


1.  Ouvrez Microsoft Project Client.

2.  Sous l’onglet **Microsoft Dynamics 365** , cliquez sur **Ouvrir**.

3.  Sélectionnez l’ **Entité juridique** pour le projet.

4.  Sélectionnez le **Projet**.

5.  Cliquez sur **Extraire** sur l’onglet **Microsoft Dynamics 365**.

6.  Lorsque vous êtes prêt à publier dans Finance, cliquez sur **Archiver** sur l’onglet **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Remplacer la structure de répartition du travail existante pour un projet existant à l’aide de Microsoft Project Client
Pour créer une nouvelle structure de répartition du travail à l’aide de Microsoft Project Client et remplacer une structure de répartition du travail existante pour un projet existant, procédez comme suit :

1.  Ouvrez Microsoft Project Client.

2.  Créez le programme dans Microsoft Project Client.

3.  Sur l’onglet **Microsoft Dynamics 365** , cliquez sur **Enregistrer les modifications** > **Remplacer le projet existant**.

4.  Sélectionnez l’ **Entité juridique** pour le projet.

5.  Sélectionnez le **Projet**.

6.  Cliquez sur **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Créer un nouveau projet à partir de Microsoft Project Client


1.  Ouvrez Microsoft Project Client.

2.  Créez le programme dans Microsoft Project Client.

3.  Sur l’onglet **Microsoft Dynamics 365** , cliquez sur **Enregistrer les modifications** > **Enregistrer dans un nouveau projet**.

4.  Sélectionnez l’ **Entité juridique** pour le projet.

5.  Entrez l’ **ID de projet** , si nécessaire.

6.  Entrez le **Nom du produit**.

7.  Sélectionnez le **Type de projet** , **Groupe de projet** et l’ **ID de contrat de projet**. Vous pouvez également créer un contrat de projet en cliquant sur **Nouveau**.

8.  Sélectionnez le **Calendrier** à utiliser pour l’allocation des ressources.

11. Cliquez sur **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]