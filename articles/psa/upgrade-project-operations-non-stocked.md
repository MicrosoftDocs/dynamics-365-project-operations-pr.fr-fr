---
title: Effectuer une mise à niveau de Project Service Automation vers Project Operations
description: Cet article fournit une vue d’ensemble du processus de mise à niveau de Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c7958c1474820361269f19ea8c9279b96f087d7a
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230226"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Effectuer une mise à niveau de Project Service Automation vers Project Operations

Nous sommes ravis d’annoncer la première des trois phases de mise à niveau de Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Project Operations. Cet article fournit une vue d’ensemble du processus aux clients qui se lancent dans ce voyage passionnant. Les prochains articles aborderont les éléments à prendre en compte par les développeurs, ainsi que des détails sur les améliorations des fonctionnalités. Elles vous fourniront non seulement des conseils pour vous aider à préparer votre mise à niveau vers Project Operations, mais vous expliqueront également à quoi vous pouvez vous attendre après la mise à niveau.

Le programme de livraison de la mise à niveau sera divisé en trois phases.

| Livraison de la mise à niveau | Phase 1 (janvier 2022) | Phase 2 (Vague d’avril 2022) | Phase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Aucune dépendance vis-à-vis de la structure de répartition du travail (WBS) pour les projets | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La WBS dans les limites actuellement prises en charge par Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS en dehors des limites actuellement prises en charge par Project Operations, y compris la prise en charge de Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Fonctions du processus de mise à niveau 

Dans le cadre du processus de mise à niveau, nous avons ajouté des journaux de mise à niveau au plan du site, afin que les administrateurs puissent diagnostiquer plus facilement les échecs. En plus de la nouvelle interface, de nouvelles règles de validation seront ajoutées pour garantir l’intégrité des données après une mise à niveau. Les validations suivantes seront ajoutées au processus de mise à niveau.

| Contrôles | Phase 1 (janvier 2022) | Phase 2 (Vague d’avril 2022) | Phase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| La WBS sera validée par rapport aux violations courantes de l’intégrité des données (par exemple, les affectations de ressources associées à la même tâche parent mais ayant des projets parents différents). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS sera validée par rapport aux [limites connues de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS sera validée par rapport aux limites connues de Project Desktop Client. | |  | :heavy_check_mark: |
| Les ressources réservables et les calendriers de projet seront évalués par rapport aux exceptions communes aux règles de calendrier incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

Au cours de la phase 2, les clients qui passent à Project Operations verront leurs projets existants mis à niveau vers une expérience en lecture seule pour la planification de projet. Dans cette expérience en lecture seule, la WBS complète sera visible dans la grille de suivi. Pour modifier la WBS, les chefs de projet peuvent sélectionner **Convertir** sur la page principale **Projets**. Un processus d’arrière-plan mettra ensuite à jour le projet afin qu’il prenne en charge la nouvelle expérience de planification de projet à partir de Project for the Web. Cette phase est destinée aux clients qui ont des projets qui s’inscrivent dans les [limites connues de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Dans la phase 3, la prise en charge de Project Desktop Client sera ajoutée, au profit des clients qui souhaitent continuer à éditer leurs projets à partir de cette application. Cependant, si des projets existants sont convertis vers la nouvelle expérience Project for the Web, l’accès au complément sera désactivé pour chaque projet converti.

## <a name="prerequisites"></a>Conditions préalables

Pour être éligible à la phase 1 de la mise à niveau, un client doit répondre aux critères suivants :

- L’environnement cible ne doit contenir aucun enregistrement dans l’entité **msdyn_projecttask**.
- Des licences Project Operations valides doivent être attribuées à tous les utilisateurs actifs du client. 
- Le client doit valider le processus de mise à niveau dans au moins un environnement hors production avec un jeu de données représentatif des données de production.
- L’environnement cible doit être mis à jour à la version 41 ou ultérieure de Project Service Automation (3.10.62.162).

Les conditions requises pour les phases 2 et 3 actualisées à l’approche des dates de la disponibilité générale.

## <a name="licensing"></a>Gestion des licences

Si vous disposez de licences actives pour Project Service Automation, vous pouvez installer et utiliser Project Operations, qui inclut toutes les fonctionnalités de Project Service Automation et plus encore. De cette façon, vous pouvez tester les capacités de Project Operations tout en continuant à utiliser Project Service Automation en production. Après l’expiration de vos licences Project Service Automation, vous devrez passer à Project Operations. Lorsque vous planifiez cette transition, vous devez tenir compte du fait que la licence Project Operations n’inclut pas de licence Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Tester et refactoriser les personnalisations

Pour commencer, importez toutes les personnalisations dans un environnement Project Operations (simplifié) propre pour vérifier que l’importation est réussie et que les opérations de l’entreprise se comportent comme prévu.

Voici quelques points à surveiller :

- L’importation peut échouer en raison de dépendances manquantes. En d’autres termes, les personnalisations font référence à des champs ou à d’autres composants qui ont été supprimés dans Project Operations. Dans ce cas, supprimez ces dépendances de l’environnement de développement.
- Si vos solutions non gérées et gérées incluent des composants qui ne sont pas personnalisés, supprimez ces composants de la solution. Par exemple, lorsque vous personnalisez l’entité **Projet**, ajoutez uniquement l’en-tête d’entité à votre solution. N’ajoutez pas tous les champs. Si vous avez déjà ajouté tous les sous-composants, vous devrez peut-être créer manuellement une nouvelle solution et y ajouter les composants pertinents.
- Les formulaires et les vues peuvent ne pas s’afficher comme prévu. Dans certaines circonstances, si vous avez personnalisé l’un des formulaires ou vues prêts à l’emploi, les personnalisations peuvent empêcher l’entrée en vigueur de nouvelles mises à jour dans Project Operations. Pour identifier ces problèmes, nous vous recommandons d’effectuer une révision côte à côte d’une installation neuve de Project Operations et d’une installation de Project Operations qui inclut vos personnalisations. Comparez les formulaires les plus couramment utilisés dans votre entreprise pour vérifier que votre version du formulaire a toujours du sens et qu’il ne manque rien dans la version propre du formulaire. Effectuez le même type de révision côte à côte pour toutes les vues que vous avez personnalisées.
- La logique métier peut échouer au moment de l’exécution. Étant donné que les références à des champs dans vos plug-ins ne sont pas validées au moment de l’importation, la logique métier peut échouer en raison de références à des champs qui n’existent plus, et vous pouvez recevoir un message d’erreur qui ressemble à l’exemple suivant : « L’entité "Projet" ne contient pas d’attribut avec Name = ’msdyn_plannedhours’ et NameMapping = ’Logical’. » Dans ce cas, modifiez vos personnalisations pour qu’elles utilisent les nouveaux champs. Si vous utilisez des classes de proxy générées automatiquement et des références de type fort dans la logique de votre plug-in, envisagez de régénérer ces proxys à partir d’une nouvelle installation. De cette façon, vous pourrez facilement identifier tous les endroits où vos plug-ins dépendent de champs obsolètes.

Après avoir mis à jour vos personnalisations pour importer proprement Project Operations, passez aux étapes suivantes.

## <a name="end-to-end-testing-in-development-environments"></a>Tests de bout en bout dans les environnements de développement

### <a name="initiate-upgrade"></a>Lancer la mise à niveau 

1. Dans le centre d’administration de Power Platform, recherchez et sélectionnez votre environnement. Ensuite, dans les applications, recherchez et sélectionnez **Dynamics 365 Project Operations**.
2. Sélectionnez **Installer** démarrer la mise à niveau. Le centre d’administration de Power Platform présentera cette installation comme une nouvelle installation. Cependant, la présence d’une version antérieure de Project Service Automation sera détectée et l’installation existante sera mise à niveau.

    Une fois la mise à niveau terminée, l’environnement doit indiquer que Project Operations est installé et que Project Service Automation n’est pas installé.

    > [!NOTE]
    > Selon la quantité de données dans l’environnement, la mise à niveau peut prendre plusieurs heures. L’équipe principale qui gère la mise à niveau doit planifier en conséquence et exécuter la mise à niveau en dehors des heures ouvrables. Dans certains cas, si le volume de données est important, la mise à niveau doit être exécutée pendant le week-end. La décision concernant la planification doit être basée sur les résultats des tests dans des environnements inférieurs.

3. Mettez à niveau les solutions personnalisées, le cas échéant. À ce stade, déployez toutes les modifications que vous avez apportées à vos personnalisations dans la section [Tester et refactoriser les personnalisations](#testing-and-refactoring-customizations) du présent article.
4. Accédez à **Paramètres** \> **Solutions**, et sélectionnez pour désinstaller la solution **Composants obsolètes de Project Operations**.

    Cette solution est une solution temporaire qui contient le modèle de données existant et les composants présents lors de la mise à niveau. En supprimant cette solution, vous supprimez tous les champs et composants qui ne sont plus utilisés. De cette façon, vous contribuez à simplifier l’interface et à faciliter l’intégration et l’extension.
    
### <a name="validate-common-scenarios"></a>Valider les scénarios courants

Lorsque vous validez vos personnalisations spécifiques, nous vous recommandons d’examiner également les processus métier pris en charge dans les applications. Ces processus métier incluent, mais sans s’y limiter, la création d’entités de vente telles que des devis et des contrats, et la création de projets qui incluent des WBS et l’approbation des chiffres réels.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Changements majeurs entre Project Service Automation et Project Operations

Cette section fournit un résumé des changements majeurs auxquels vous pouvez vous attendre entre Project Service Automation et Project Operations.

### <a name="project-planning"></a>Planification de projet

Les fonctionnalités de planification de projet dans Project Operations ne reposent plus sur une combinaison de la logique côté client et de la logique côté serveur. AU lieu de cela, Project Operations utilise Project for the Web comme moteur de planification. Ce changement dans les capacités de planification rend possibles plusieurs nouvelles fonctionnalités, telles que les vues Tableau et Gantt, la planification axée sur les ressources, les [éléments de liste de contrôle des tâches](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) et les modes de planification de projet. Les nouvelles fonctionnalités de planification sont également appuyées sur un riche ensemble de nouvelles [interfaces de programmation d’applications (API)](../project-management/schedule-api-preview.md). Ces API sont destinées à garantir qu’aucune opération de programmation destinée à créer, mettre à jour ou supprimer une entité dans la WBS ne corrompra les champs calculés dans la planification.

## <a name="billing-and-pricing"></a>Facturation et tarification

Dans le cadre de l’investissement continu dans Project Operations, plusieurs nouvelles fonctionnalités sont disponibles dans la facturation et la tarification. En voici quelques exemples :

- [Enregistrer l’utilisation du matériel sur les projets et les tâches du projet](../material/material-usage-log.md)
- [Gestion des sous-traitants](../pro/subcontracting/managing-subcontracts-overview.md)
- [Paiements anticipés et contrats basés sur un acompte](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statut et validations des limites à ne pas dépasser des contrats](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturation à la tâche

## <a name="frequently-asked-questions"></a>Questions fréquentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quels types de déploiement sont actuellement pris en charge pour la mise à niveau ?

| Valeur                                                 | Cible                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automatisation de la gestion de projets                             | Déploiement simplifié de Project Operations                        | Prise en charge               |
| Gestion et comptabilité des projets dans Dynamics 365 Finance | Déploiement simplifié de Project Operations                        | Actuellement non pris en charge |
| Gestion et comptabilité des projets dans Finance              | Project Operations pour les scénarios basés sur les ressources/produits non stockés     | Actuellement non pris en charge |
| Project Service Automation 3.x                         | Project Operations pour les scénarios basés sur les ressources/produits non stockés     | Actuellement non pris en charge |
| Project for the Web (environnement dédié)            | Déploiement simplifié de Project Operations                        | Actuellement non pris en charge |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Comment puis-je installer Project Operations avant que l’outil de mise à niveau ne soit disponible ?

Il existe deux options pour installer Project Operations avant que l’outil de mise à niveau ne soit disponible :

- Approvisionner un nouvel environnement.
- Déployer Project Operations séparément sur n’importe quelle organisation commerciale où Project Service Automation n’est pas présent.

> [!NOTE]
> Si Project Service Automation est installé dans une organisation mais qu’il n’a pas été utilisé, il peut être désinstallé. Une fois que vous avez complètement supprimé Project Service Automation, Project Operations peut être installé dans la même organisation.
