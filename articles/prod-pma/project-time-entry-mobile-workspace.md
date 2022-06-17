---
title: Espace de travail mobile de saisie des heures de projet
description: Cet article fournit des informations sur l’espace de travail mobile Saisie des heures du projet. Cet espace de travail permet aux utilisateurs de saisir et de gagner du temps sur un projet en utilisant leur appareil mobile.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: a163e32dae0231b5d71d1de2dbb473593b989164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919535"
---
# <a name="project-time-entry-mobile-workspace"></a>Espace de travail mobile de saisie des heures de projet

[!include [banner](../includes/banner.md)]

Cet article fournit des informations sur l’espace de travail mobile **Saisie des heures du projet**. Cet espace de travail permet aux utilisateurs de saisir et de gagner du temps sur un projet en utilisant leur appareil mobile.

Cet espace de travail mobile est destiné à être utilisé avec l’application mobile Dynamics 365 Unified Ops. 

## <a name="overview"></a>Vue d’ensemble
Dans le cadre de leur travail quotidien, les ressources du projet sont souvent sur place ou en déplacement. L’espace de travail mobile **Entrée d’heure du projet** permet aux utilisateurs d’entrer leur temps facturable ou non facturable par rapport à un projet sur l’appareil mobile de leur choix. Par conséquent, les ressources du projet peuvent enregistrer des entrées des temps à tout moment et n’importe où. Elles peuvent également afficher les entrées des temps qui ont déjà été enregistrées. 

Plus précisément, dans l’espace de travail mobile **Entrée d’heure du projet**, les utilisateurs peuvent effectuer les tâches suivantes :

-   Pour n’importe quelle date sélectionnée, entrer le nombre d’heures passé sur une tâche spécifique.
-   Effectuer une recherche par nom de projet ou par client pour trouver le projet pour lequel entrer des heures.
-   Spécifier la catégorie et l’activité pour les heures passées.
-   Enregistrez le temps comme facturable ou non facturable pour le projet.
-   Facultatif : saisissez des commentaires externes et internes.

## <a name="prerequisites"></a>Conditions préalables
Les conditions préalables varient en fonction de la version de Microsoft Dynamics 365 qui a été déployée pour votre organisation.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Conditions préalables si vous utilisez Dynamics 365 Finance
Si Finance a été déployé pour votre organisation, l’administrateur système doit publier l’espace de travail mobile **Saisies des heures de projet**. Pour obtenir des instructions, consultez [Publier un espace de travail mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Conditions préalables si vous utilisez la version 1611 avec Platform update 3 ou version ultérieure
Si la version 1611 avec Platform update 3 ou version ultérieure a été déployée pour votre organisation, l’administrateur système doit remplir les conditions préalables suivantes. 

<table>
<thead>
<tr class="header">
<th>Éléments requis</th>
<th>Rôle</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implémentez KB 4018050.</td>
<td>Administrateur système</td>
<td>KB 4018050 est une mise à jour X++ ou un correctif de métadonnées qui contient l’espace de travail mobile <strong>Saisie des heures de projet</strong>. Pour implémenter KB 4018050, votre administrateur système doit procéder comme suit.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Téléchargez le correctif des métadonnées à partir de Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installez le correctif des métadonnées</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Créez un package déployable</a> qui contient les modèles <strong>ApplicationSuite</strong> et <strong>ProjectMobile</strong>, puis téléchargez le package déployable sur LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Appliquez le package déployable</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiez l’espace de travail mobile de <strong>Saisie des heures de projet</strong>.</td>
<td>Administrateur système</td>
<td>Voir <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publier un espace de travail mobile</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Télécharger et installer l’application mobile

Télécharger et installer l’application mobile Finance and Operations :

-   [Pour les téléphones Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pour les iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Se connecter à l’application mobile
1.  Démarrez l’application sur votre appareil mobile.
2.  Tapez votre URL Dynamics 365.
3.  La première fois que vous vous connectez, vous êtes invité à saisir votre nom d’utilisateur et votre mot de passe. Entrez vos informations d’identification.
4.  Une fois connecté, les espaces de travail disponibles pour votre entreprise s’affichent. Notez que si votre administrateur système publie un nouvel espace de travail ultérieurement, vous devez actualiser la liste des espaces de travail mobiles.

[![Balayer pour actualiser.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Saisir les heures à l’aide de l’espace de travail mobile de saisie des heures de projet
1.  Sur votre appareil mobile, sélectionnez l’espace de travail **Saisie des heures de projet**.
2.  Sélectionnez **Saisie des heures**. Les dates du calendrier de la semaine en cours sont affichées.
3.  Pour une date sélectionnée, sélectionnez **Actions** &gt; **Nouvelle entrée**.
4.  Entrez le nombre d’heures à enregistrer.
5.  Sélectionnez le projet pour la saisie des heures. Une liste affiche les projets chargés dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Si votre projet ne figure pas dans la liste, sélectionnez **Rechercher**. Recherchez par nom ou passez à une recherche par nom de projet ou client.
7.  Sélectionnez une catégorie. Une liste affiche les catégories chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher**. Recherchez par catégorie ou passez à la recherche par nom de catégorie.
9.  Sélectionnez une activité. Une liste affiche les activités chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, consultez [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Si votre activité ne figure pas dans la liste, sélectionnez **Rechercher**. Recherchez par numéro d’activité ou passez à la recherche par objectif.

11. Sélectionnez la propriété de ligne.
12. Facultatif : saisissez des commentaires externes et internes.
13. Cliquez sur **Terminé**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]