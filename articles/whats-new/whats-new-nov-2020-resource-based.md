---
title: Nouveautés de novembre 2020 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de novembre 2020 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 75a7b63c12b0ad3c6808785b6cbe6f22bd65f126
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029527"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de novembre 2020 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

- Version 4.4.0.70 de Project Operations dans l’environnement CDS
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Mises à jour vers Project Operations pour les scénarios basés sur les ressources/produits non stockés

### <a name="project-operations-on-cds"></a>Project Operations dans CDS

| Fonctionnalités                 | Numéro de référence | Mise à jour qualité                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestion des opportunités       | 2036993          | La ligne d’estimation et les lignes de contrat d’affectation de ressources sont mises à jour sur les devis gagnants lorsque le type de ligne de devis est **Toutes les tâches**.                                                 |
| Facturation et tarification          | 2070392          | Les lignes de contrat de projet sur la facture augmentent à chaque fois que **Actualiser les transactions de facture** est sélectionné.                                                                         |
| Planification de projet             | 2043336          | Impossible de supprimer un enregistrement de membre de l’équipe de projet.                                                                                                                                  |
| Planification de projet             | 2046013          | Comportement incohérent des colonnes d’indicateur Estimations pendant le chargement par rapport au changement de type de phase de temps.                                                                                   |
| Planification de projet             | 2046647          | Les heures de début et de fin sont décalées d’une heure lorsque les besoins en ressources sont générés par les membres de l’équipe de projet.                                                                      |
| Planification de projet             | 2053879          | (À compter du prochain déploiement de CDS) PublishUnassignedAssignments interrompt une tentative d’enregistrement d’une tâche lorsque l’erreur « La valeur transmise pour ConditionOperator.In est vide ».                       |
| Planification de projet             | 2055501          | Laisser la **Date de début du projet** vide provoque un échec de la planification.                                                                                                      |
| Planification de projet             | 2066817          | Impossible de créer une ressource générique à l’aide du sélecteur de personnes dans l’onglet **Tâches**.                                                                                                   |
| Planification de projet             | 2067034          | Le bouton **Afficher les détails** n’est pas disponible sur la page **Détails de la tâche**.                                                                                                       |
| Gestion des ressources          | 2046667          | Les membres génériques de l’équipe ne sont pas supprimés même une fois que toutes les ressources sont satisfaites.                                                                                                    |
| Temps et entrée rapide de dépenses | 2047499          | Le bouton **Nouveau** sur la page Saisie de l’heure ouvre la page **Nouvelle signature de courrier électronique**.                                                                                               |
| Temps et entrée rapide de dépenses | 2059859          | Une fenêtre contextuelle inattendue s’ouvre lors de la création d’une entrée de dépense.                                                                                                                         |
| Autres                        | 2044181          | (Désinstallation du bon de commande) Lorsque vous essayez de désinstaller msdyn_ProjectServiceCore_Patch et les solutions principales du service de projet msdyn, l’erreur « Enregistrement non disponible » se produit.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

| Fonctionnalités        | Numéro de référence | Mise à jour qualité                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constatation du produit | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Le pourcentage d’estimation de projet complété est erroné lorsque le contrat utilise une devise étrangère et le pourcentage d’avancement des travaux comme méthode d’achèvement.                     |
| Constatation du produit | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Impossible de publier des estimations avec la méthode d’achèvement du **Coût réel**.                                                                                                    |
| Constatation du produit | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | L’élimination échoue en raison d’une erreur de déséquilibre des documents lorsque la devise de la société et la devise de transaction sont différentes.                                              |
| Gestion des dépenses  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Pour les utilisateurs non administrateurs, les valeurs de recherche pour les colonnes de ligne de dépense telles que **ID du projet** et **Catégorie de dépenses** ne s’affichent pas correctement dans le cadre du connecteur de données. |
| Gestion des dépenses  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | La propriété de ligne par défaut ne s’affiche pas pour les catégories de dépenses.                                                                                                         |
| Gestion des dépenses  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | L’intégration des dépenses doit inclure la propriété de ligne de la note de frais.                                                                                             |
| Facturation           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Impossible de publier des propositions de facture de projet en raison d’un message d’erreur indiquant que la combinaison FD n’a pas été validée.                                                    |
| Facturation           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Impossible d’afficher les transactions à partir de la page de détails **Facture**.                                                                                                              |
| Facturation           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Les lignes de proposition de facture peuvent être supprimées.                                                                                                                                  |
| Comptabilité de projet  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Les éléments du menu **Prévision** ne sont pas visibles sur la page de liste **Projets**.                                                                                                   |
| Comptabilité de projet  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Impossible d’ouvrir **Instruction de projet**   > **Transactions et prévisions**.                                                                                                       |
| Comptabilité de projet  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajuster la comptabilité** n’est pas activé pour les transactions de projet facturées.                                                                                                  |
| Comptabilité de projet  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Les détails comptables ne sont pas inclus dans le tableau **ProjCDSActualsImport** lorsque le journal d’**intégration** est publié.                                                  |
| Comptabilité de projet  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | L’entrée Prévision de projet est dupliquée lorsque vous supprimez puis ajoutez à nouveau une affectation de ressource.                                                                            |
| Comptabilité de projet  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Sélectionner un lien d’ID du projet n’ouvre pas l’URL du lien ciblé CDS.                                                                                                         |
| Comptabilité de projet  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Impossible de mettre à jour la date de début d’une tâche dans CDS.                                                                                                                           |
| Comptabilité de projet  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Activer la fonctionnalité Plusieurs lignes de contrat n’est pas possible sans intégration CDS.                                                                                   |

### <a name="regulatory-updates"></a>Mises à jour réglementaires
Pour plus d’informations sur les mises à jour réglementaires pour les applications de finances et d’opérations, voir [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à LCS et afficher les mises à jour réglementaires planifiées à l’aide de l’outil de recherche d’incidents. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../includes/footer-banner.md)]