---
title: Application mobile Project Timesheet
description: Cette rubrique offre des informations sur l’application mobile Microsoft Dynamics 365 Project Timesheet. L’application mobile Project Timesheet permet aux utilisateurs d’envoyer et d’approuver les feuilles de temps pour les projets sur leur appareil mobile.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075913"
---
# <a name="project-timesheet-mobile-application"></a>Application mobile Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Vue d’ensemble

L’application mobile Microsoft Dynamics 365 Project Timesheet permet aux utilisateurs d’envoyer et d’approuver les feuilles de temps pour les projets sur leur appareil mobile (iPhone ou Android). Cette application mobile affiche la fonctionnalité de feuille de temps qui réside dans la zone Gestion de projet et comptabilité de Dynamics 365 Finance, améliorant la productivité et l’efficacité des utilisateurs, ainsi que la saisie et l’approbation rapides des feuilles de temps des projets.

## <a name="download-and-install-the-mobile-app"></a>Télécharger et installer l'application mobile

Téléchargez et installez l’application mobile Microsoft Dynamics 365 Project Timesheet pour Android ou iPhone depuis la plateforme mobile de votre appareil.

## <a name="enable-the-app"></a>Activer l’application 

Dans Finance, l’application mobile Project Timesheet doit être activée. Pour activer la fonctionnalité, accédez à **Gestion de projet et comptabilité \> Feuille de temps** et sélectionnez le paramètre **Activer Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Se connecter à l’application

1.  Démarrez l'application sur votre appareil mobile.

2.  Entrez votre URL Finance.

3.  La première fois que vous vous connectez, vous êtes invité à saisir votre nom d’utilisateur et votre mot de passe. Entrez vos informations d'identification.

4.  Vous serez connecté à votre entreprise par défaut.

## <a name="submit-a-project-timesheet"></a>Soumettre une feuille de temps de projet

Vous pouvez créer et soumettre une feuille de temps de projet dans l’application. Vous pouvez baser une nouvelle feuille de temps sur les informations d’une feuille de temps précédente, des lignes enregistrées ou des affectations de projet. Si vous êtes désigné comme délégué, vous pouvez également saisir une feuille de temps pour un autre employé. Pour créer une feuille de temps en tant que délégué, sélectionnez le bouton **Menu**, puis sélectionnez un nom de ressource.

La page de feuille de temps créera une nouvelle feuille de temps pour la période de feuille de temps, basée sur la date actuelle. La semaine ouvrée apparaît. Si la période de feuille de temps couvre plusieurs semaines, vous pouvez sélectionner une autre semaine ouvrée depuis les onglets de semaine ouvrée.
Si une feuille de temps existe pour la date actuelle, elle s’affiche. Si vous devez créer une nouvelle feuille de temps dans une période de feuille de temps différente, sélectionnez le bouton **Menu**, puis sélectionnez **Nouvelle feuille de temps**.

Vous pouvez saisir des informations sur le projet en cliquant sur l’action **Ajouter du temps** ou **Copier le temps depuis**. L’action **Copier le temps depuis** copie les informations de ligne de projet, mais pas les heures. Le menu **Copier le temps depuis** comprend les options suivantes :

- **Copier à partir de la feuille de temps existante** : copiez les lignes de la feuille de temps à partir d’une feuille de temps existante.

- **Copier depuis le favori** : créez de nouvelles lignes de feuille de temps en utilisant les paramètres de feuille de temps que vous avez sélectionnés comme favoris.

- **Copier depuis l’affectation** : créez de nouvelles lignes de feuille de temps à partir des projets assignés.

Les informations de projet affichées dépendent des paramètres mobiles que vous avez définis sur la page **Gestion de projet et comptabilité**.

Dans le champ **Entité juridique**, sélectionnez l’entité juridique pour laquelle vous avez effectué le travail de projet. Le champ **Entité juridique** n’est disponible que si la prise en charge des feuilles de temps intersociétés a été activée pour votre entité juridique.

Sélectionnez le client associé au projet pour la feuille de temps. Pour la version initiale sur Android, la saisie par le client n’est pas prise en charge, car vous devez d’abord sélectionner le projet. Si vous avez d’abord sélectionné le projet, le champ **Client** est rempli automatiquement.

Dans le champ **Projet**, sélectionnez le projet pour lequel vous entrez l’heure. Le champ **Client** est renseigné automatiquement.

Les recherches de clients et de projets permettent de rechercher à la fois les clients et les projets.

Sélectionnez les informations dans les champs **Catégorie**, **Activité**, **Propriété de ligne**, **Groupe de taxe de vente**, et **Groupe de taxe de vente d’article**, le cas échéant. Ces champs peuvent être remplacés.

Le champ **Propriété de ligne** sera défini sur une valeur par défaut, en fonction des paramètres de gestion de projet et de comptabilité. Lorsque les paramètres projet/catégorie et catégorie/ressource sont activés, la valeur **Propriété de ligne** sera définie sur la valeur par défaut que vous avez définie pour cette validation. Lorsque les paramètres projet/catégorie et catégorie/ressource ne sont pas activés, la valeur **Propriété de ligne** est définie par défaut en fonction du champ **Activer la propriété de ligne par défaut** sur la page **Gestion de projet et comptabilité**. La valeur **Propriété de ligne** peut être remplacée.

Sélectionnez un jour pour ajouter du temps. Entrez le nombre d’heures que vous avez travaillé chaque jour.

Pour ajouter des commentaires sur les heures que vous entrez, cliquez sur **Ajouter des commentaires**, puis entrez des commentaires pour un audience interne, un client audience ou les deux.
Les commentaires internes peuvent être consultés par les chefs de projet. Les commentaires des clients sont inclus sur les factures.

Pour enregistrer la ligne comme favori, cochez la case, puis cliquez sur **Enregistrer comme favori**.

La dimension financière et la prise en charge des pièces jointes ne sont pas fournies dans l’application mobile.

Continuez à ajouter des lignes de projet au besoin pour compléter votre feuille de temps.

Cliquez sur **Soumettre** pour envoyer la feuille de temps au workflow d’approbation.

## <a name="review-timesheets"></a>Consulter les feuilles de temps

Une liste des feuilles de temps à consulter est disponible dans le menu. Cette option n’est disponible que si vous avez été désigné comme approbateur de workflow. Les approbations d’en-tête et de ligne sont prises en charge. L’approbation au niveau de la ligne offre la possibilité de marquer une ou plusieurs lignes pour approbation. Après avoir examiné les informations de la feuille de temps, cliquez sur **Approuver**, **Déléguer** ou **Retour** pour continuer le workflow.
