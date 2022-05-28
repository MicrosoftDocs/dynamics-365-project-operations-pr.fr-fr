---
title: Nouveautés d’avril 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version d’avril 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613255"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés d’avril 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.41.0.45
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.26

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les catégories d’approvisionnement peuvent être utilisées avec les bons de commande de projet et les factures fournisseur en attente. Pour en savoir plus, voir [Utiliser les catégories d’approvisionnement avec les bons de commande de projet et les factures fournisseur en attente](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Le tableau suivant présente les cartes en double écriture qui ont été modifiées ou ajoutées dans la version de mars 2022 de Project Operations.

| Mappage d’entité | Version mise à jour | Commentaires |
| -------------- | ------------------- | ------------|
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Cette carte prend en charge l’utilisation des catégories d’approvisionnement avec les bons de commande et les factures fournisseur en attente. |

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| ------------ | ---------------- | -------------- |
| Temps et dépenses | 2573900 | La fonctionnalité **Approbation moderne** doit être activée par défaut. |
| Facturation et tarification | 2603313 | Correction d’une erreur d’enregistrement en double qui empêchait l’ajout de lignes de devis et de contrat contenant un produit. |
| Déploiement et configuration | 2611368 | Les clients doivent pouvoir ajouter jusqu’à cinq entités personnalisées à la solution à l’aide du concepteur d’application moderne. |
| Temps et dépenses | 2628285 | Correction d’un problème qui affectait la possibilité de définir la bonne catégorie de ressources lors de l’importation des entrées de temps. |
| Gestion des opportunités| 2628815 | Mettez à jour la limite de caractères de la description détaillée de la ligne de devis pour qu’elle corresponde à la limite de caractères de l’objet de la tâche, afin que l’importation réussisse pour les tâches dont l’objet comporte plus de 100 caractères. |
| Temps et dépenses| 2629547 | Le champ **Soumis par** des approbations de projet doit pointer vers l’utilisateur qui a soumis l’enregistrement. |
| Temps et dépenses| 2629865 | Le champ **Copier la catégorie** sur les tâches lorsque les projets sont copiés. |
| Temps et dépenses| 2636463 | Correction des filtres sur les approbations dans les formulaires d’approbation modernes. |
| Planification et de suivi de projets | 2648300 | Correction d’un problème qui empêchait le propriétaire du projet d’être changé. |
| Facturation et tarification | 2563000 | Les lignes de journal pour une vente non facturée dont la devise diffère de la devise du contrat ne doivent pas être autorisées. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services (LCS) et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
