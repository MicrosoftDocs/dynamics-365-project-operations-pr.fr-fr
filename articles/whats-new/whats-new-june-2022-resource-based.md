---
title: Nouveautés de juin 2022 – Project Operations pour les scénarios basés sur les ressources/hors stock
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de juin 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959418"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de juin 2022 – Project Operations pour les scénarios basés sur les ressources/hors stock

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.43.0.77
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Le tableau suivant présente les cartes en double écriture qui ont été modifiées ou ajoutées dans la version de juin 2022 de Project Operations.

| Mappage d’entité | Version mise à jour | Commentaires |
| --- | --- | --- |
| Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | L’ancien champ est déconseillé et mappé au nouveau champ pour le suivi de l’état de la facture fournisseur. |

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Sous-traitance | 2708885 | Correction du message d’erreur qui s’affiche quand un utilisateur crée un enregistrement d’en-tête de réservation de ressource réservable dans lequel aucune ressource réservable n’est renseignée. |
| Planification et de suivi de projets | 2629441 | Correction de la logique de déclenchement du workflow pour éviter une boucle infinie à la mise à jour des tâches du projet. |
| Temps et dépenses | 2641209 | Les importations d’entrées de temps à partir d’affectations/réservations doivent conserver une référence de ressource réservable. |
| Planification et de suivi de projets | 2651148 | L’en-tête du document de projet doit être protégé.|
| Planification et de suivi de projets | 2653145 | Ajout de validations pour garantir qu’un enregistrement de projet ne peut pas être créé avec des caractères non valides dans son nom. |
| Temps et dépenses | 2654710 | Correction du filtrage sur la page **Approbations**. |
| Facturation et tarification | 2667805 | Ajout de validations pour empêcher la création de chiffres réels des ventes facturées si les chiffres réels des ventes non facturées n’existent pas. |
| Facturation et tarification | 2668378 | Ajout de validations pour empêcher l’ajout d’une dimension de tarification personnalisée à moins qu’un nom logique et un nom de champ ne soient renseignés. |
| Sous-traitance | 2677485 | Mise à jour de la version cible de la carte à double écriture des lignes de facture fournisseur. |
| Temps et dépenses | 2700428 | Amélioration de la logique des approbations pour garantir que d’autres ensembles d’approbations pour le projet peuvent être traités même si l’un des ensembles d’approbations est bloqué dans des tâches système. |

### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services (LCS) et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
