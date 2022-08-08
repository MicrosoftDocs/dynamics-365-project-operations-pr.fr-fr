---
title: Application mobile Project Timesheet
description: Cet article fournit des informations sur l’application mobile Microsoft Dynamics 365 Project Timesheet. L’application mobile Project Timesheet permet aux utilisateurs d’envoyer et d’approuver les feuilles de temps pour les projets sur leur appareil mobile.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110972"
---
# <a name="project-timesheet-mobile-application"></a>Application mobile Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Résumé

L’application mobile Microsoft Dynamics 365 Project Timesheet permet aux utilisateurs d’envoyer et d’approuver les feuilles de temps pour les projets sur leur appareil mobile (iPhone ou Android). Cette application mobile permet d’exploiter la fonctionnalité de feuille de temps qui réside dans la zone Gestion de projet et comptabilité de Dynamics 365 Finance. Elle contribue à améliorer la productivité et l’efficacité des utilisateurs, mais également à la saisie et à l’approbation en temps opportun des feuilles de temps des projets.

## <a name="download-and-install-the-mobile-app"></a>Télécharger et installer l’application mobile

Téléchargez et installez l’application mobile Microsoft Dynamics 365 Project Timesheet pour Android ou iPhone depuis la plateforme mobile de votre appareil.

## <a name="enable-the-app"></a>Activer l’application 

Dans Finance, l’application mobile Project Timesheet doit être activée. Pour activer la fonctionnalité, accédez à **Gestion de projet et comptabilité \> Feuille de temps** et sélectionnez le paramètre **Activer Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Résoudre les problèmes de connexion

**Problème :** Lors de la connexion à l'application mobile Project Timesheet, les utilisateurs reçoivent un message d'erreur indiquant qu'ils « ne peuvent pas accéder à l'application 2bc50526-cdc3-4e36-a970-c284c34cbd6e dans ce client. »

**Publier :** Lors de la connexion à l'application mobile Project Timesheet, les utilisateurs reçoivent une erreur qui ressemble à l'un des exemples suivants :

- « AADSTS50020 : le compte d'utilisateur [nom d'utilisateur] du fournisseur d'identité https://sts.windows.net/ [app id]' n'existe pas dans le client [tenant id] et ne peut pas accéder à l'application [app id] dans ce client. »
- « Le compte d’utilisateur sélectionné n’existe pas dans le client [tenant id] et ne peut pas accéder à l’application [app id] dans ce client »

**Explication :** Ces problèmes sont dus à une modification apportée à Azure Active Directory (Azure AD) en mai 2022 et qui concerne les utilisateurs externes. Étant donné que cette modification n'a pas été apportée aux applications de finances et d’opérations, elle peut affecter les clients sur n'importe quelle version de la plateforme ou de l'application.

**Solution :** Tous les utilisateurs externes doivent être invités dans le client via Azure AD. Pour plus d'informations, voir [Inviter des utilisateurs avec Azure Active Directory B2B collaboration](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Se connecter à l’application

1.  Démarrez l’application sur votre appareil mobile.

2.  Entrez votre URL Finance.

3.  La première fois que vous vous connectez, vous êtes invité à saisir votre nom d’utilisateur et votre mot de passe. Entrez vos informations d’identification.

4. Vous serez connecté à votre entreprise par défaut.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
