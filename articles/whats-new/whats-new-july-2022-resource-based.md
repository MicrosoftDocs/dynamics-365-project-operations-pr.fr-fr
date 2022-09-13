---
title: Nouveautés de juillet 2022 – Project Operations pour les scénarios basés sur les ressources/hors stock
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de juillet 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403948"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de juillet 2022 – Project Operations pour les scénarios basés sur les ressources/hors stock

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.44.0.22
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Déploiement et configuration | 2761472 | Une erreur d'installation de Project Operations est gérée. |
| Facturation et tarification | 2746940 | Le nom de la ligne de sous-traitance doit avoir une longueur maximale de 100 caractères. |
| Facturation et tarification | 2739162 | Les clients doivent pouvoir voir les boutons du ruban dans la vue de la grille des chiffres réels. |
| Planification et suivi de projets | 2730318 | Validation mise à jour pour les caractères non pris en charge dans le sujet du projet. |
| Facturation et tarification | 2705361 | Les chiffres réels des ventes facturées par étape doivent être inclus dans les champs de suivi de projet. |
| Facturation et tarification | 2675880 | Empêcher qu'un projet soit lié à une ligne de contrat qui n'est pas basée sur le travail. |
| Facturation et tarification | 2664396 | Si une liste de prix de devis est enregistrée sans devis, il doit y avoir une erreur indiquant que le devis ne peut pas être vide. |
| Facturation et tarification | 2184019 | L'onglet **Facturation à la tâche** ne doit pas être affiché pour les projets qui n'ont ni contrat ni devis. |
| Temps et dépenses | 2754459 | Lorsque le flux cloud de planification récurrente est inactif, affichez la bannière et contournez le traitement asynchrone. |
| Facturation et tarification | 2724391 | Une exception erronée est levée lorsqu’il manque une valeur client à la règle de facturation fractionnée du contrat de projet. |
| Facturation et tarification | 2708638 | L’enregistrement n’a pas été trouvé lors de la recherche à l’aide de la grille de recherche dans les utilisations de matériaux et les approbations pour les utilisations de matériaux.|
| Facturation et tarification | 2686977 | Empêchez la validation de la ligne de facture lors de la création de la facture. |
| Facturation et tarification | 2683032 | La copie des rôles et catégories facturables ne dépasse pas 5 000 enregistrements.|
| Facturation et tarification | 2673363 | Le pourcentage de consommation des coûts sur le projet est corrompu lorsqu’il existe à la fois des estimations d’effort et de dépenses et des valeurs réelles pour un projet. |

### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services (LCS) et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fonctionnalités activées par défaut dans la prochaine version

Le tableau suivant répertorie les fonctionnalités qui sont activées par défaut dans la version 10.0.29. La plupart des fonctionnalités qui ont été activées automatiquement peuvent être désactivées dans [Gestion des fonctionnalités](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). À l'avenir, certaines fonctionnalités qui ont été automatiquement activées pourraient être supprimées de la gestion des fonctionnalités et devenir obligatoires. Cette modification garantit que les clients utilisent les fonctionnalités actuelles, de sorte que les améliorations peuvent s'appuyer sur les fonctionnalités actuelles au fur et à mesure de leur ajout. Les fonctionnalités ne seront jamais automatiquement activées en moins d'un an, à moins qu'elles ne soient jugées essentielles.

| Nom de la fonction | Date d’activation | Fonction ajoutée le | État de la fonctionnalité | Module |
| --- | --- | --- |--- |--- |
| Activer l'ajustement de la transaction horaire en fonction de la modification de l'allocation des règles de financement | 16 septembre 2022 | 7 octobre 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Fonctionnalité de contrepassation de facture d'acompte de bon de commande de projet | 16 septembre 2022 | 6 octobre 2021 | Activé par défaut | Gestion et comptabilité des projets |
| Supprimer les lignes de proposition de facture lors de l'utilisation de Project Operations pour les scénarios basés sur les ressources/non stockés | 16 septembre 2022 | 6 octobre 2021 | Activé par défaut | Gestion et comptabilité des projets |
| Ajuster la comptabilité d'une transaction de projet publiée | 16 septembre 2022 | 10 mai 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Activer la configuration comptable par défaut pour le projet | 16 septembre 2022 | 19 février 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Activer plusieurs lignes de contrat pour un projet | 16 septembre 2022 | 29 juin 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Faire passer les journaux des heures du projet en lecture seule si le statut d'approbation actuel ne permet pas la modification | 16 septembre 2022 | 6 octobre 2021 | Activé par défaut | Gestion et comptabilité des projets |
| Activer la synchronisation des lignes de vente à partir des lignes d'achat lorsque les lignes d'achat sont mises à jour et que le paramètre de gestion des modifications de bon de commande est activé | 16 septembre 2022 | 7 octobre 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Activer Project Operations sur Dynamics 365 Customer Engagement | 16 septembre 2022 | 29 juin 2020 | Activé par défaut | Gestion et comptabilité des projets |
| Fonction de correction d'annulation de transaction de projet | 16 septembre 2022 | 13 juillet 2020 | Activé par défaut | Gestion et comptabilité des projets |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Fonctionnalités qui deviendront obligatoires dans la prochaine version

Le tableau suivant répertorie les fonctionnalités qui sont obligatoires à partir de la version 10.0.29.

| Nom de la fonction | Date d’activation | Fonction ajoutée le | État de la fonctionnalité | Module |
| --- | --- | --- | --- | --- |
| Calculer la valeur engagée sur la source de financement sans arrondir le taux de change | 16 septembre 2022 | 14 juin 2020 | Obligatoire | Gestion et comptabilité des projets |
| Activer la validation des ajustements de projet avec le même compte général que la transaction d'origine | 16 septembre 2022 | 14 juin 2020 | Obligatoire | Gestion et comptabilité des projets |
| Détail du montant engagé du contrat de projet | 16 septembre 2022 | 31 août 2019 | Obligatoire | Gestion et comptabilité des projets |
| Activer le tri par ressource lors de la création d'une proposition de facture de projet | 16 septembre 2022 | 31 août 2019 | Obligatoire | Gestion et comptabilité des projets |
