---
title: Nouveautés d’octobre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version d’octobre 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806605"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés d’octobre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.57.0.176
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.30

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

| Fonctionnalités | Nom de la fonction | Plus d’informations |
| --- | --- | --- |
| Planification et suivi de projets | **Planification externe Project Operations**<br>Le mode de planification externe permet aux clients de créer, mettre à jour et supprimer de manière native des entités liées aux structures de répartition du travail (WBS) à l’aide des API Dataverse natives, mais sans les limites actuelles appliquées par Microsoft Project for the Web. | [Planification externe](/dynamics365/project-operations/project-management/external-scheduling) |
| Déploiement et configuration | <p>**Autoriser les clients à choisir le type de déploiement**<br>Les mises à jour pilotées par les produits (PDU) de Project Operations sont utilisées pour installer automatiquement la solution à double écriture de Project Operations lorsque les solutions de base à double écriture et d’orchestration sont installées dans l’environnement.</p><p>Cette fonctionnalité introduit un nouveau paramètre **Comportement de mise à niveau de la solution** dans les paramètres du projet. Lorsque ce paramètre est défini sur **Simplifié uniquement**, les mises à jour pilotées par les produits (PDU) de Project Operations n’installent plus automatiquement la solution à double écriture de Project Operations même si les solutions de base à double écriture et d’orchestration sont installées dans l’environnement. Ce comportement profitera aux clients qui prévoient d’utiliser des solutions à double écriture pour intégrer les commandes clients dans les applications de finances et d’opérations, mais qui souhaitent utiliser Project Operations en mode Simplifié (c’est-à-dire sans intégration dans les applications de finances et d’opérations).</p> | |
| Facturation et tarification | <p>**Conversion de devises pour les transactions de vente non facturées dans les environnements intégrés**<br>Pour les clients qui utilisent Project Operations intégré aux applications de finances et d’opérations (c’est-à-dire dans le type de déploiement ressource/non stocké), les taux de change sont généralement maîtrisés dans les applications de finances et d’opérations. Cependant, si une catégorie de dépenses doit être tarifée à l’aide de la méthode de calcul du prix « au prix coûtant » ou « majoration du coût » lorsque le client est facturé, le taux de change utilisé pour calculé le montant de vente utilise les taux de change dans Dataverse, pas les taux de change des applications de finances et d’opérations.</p><p>Cette fonctionnalité introduit un nouveau paramètre **Comportement de conversion monétaire** dans les paramètres du projet. Lorsque ce paramètre est défini sur **Étendu avec retour vers la valeur**, les montants des ventes non facturées sur les transactions de dépenses sont calculés à l’aide des taux de change des applications de finances et d’opérations.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2316317 | Le système permet de créer des factures sans transactions facturables. |
| Facturation et tarification | 2737300 | Validez la disponibilité du champ **Client** avant d’accéder au formulaire. |
| Facturation et tarification | 2744948 | Ajoutez une vérification nulle pour la méthode de facturation. |
| Facturation et tarification | 2763515 | Traitement des erreurs de référence nulle lorsque le contrat de vente de la facture est manquant. |
| Facturation et tarification | 2844301 | La création de factures par lots échoue en raison d’une erreur. |
| Facturation et tarification | 2845869 | Stockage incorrect du service d’organisation. |
| Facturation et tarification | 2853729 | Les détails du rôle et du prix sont mis à jour lorsque le type de facturation est modifié. |
| Facturation et tarification | 2940350 | Lorsque les prix réels sont tarifés, seules les listes de prix actives doivent être saisies automatiquement. |
| Déploiement et configuration | 3001206 | L’entité msdyn\_replaylogheader empêche les mises à niveau des organisations clientes. |
| Gestion des opportunités | 2755582 | Traitement des exceptions de référence nulle dans l’assistant de règle de facturation fractionnée. |
| Gestion des opportunités | 2761477 | Lorsque la facturation fractionnée est utilisée, la suppression d’un jalon (en-tête) laisse des jalons orphelins. |
| Gestion des opportunités | 2767595 | Lorsqu’un enregistrement d’utilisation de matériel est ouvert dans le formulaire principal, la ressource réservable de l’enregistrement est remplacée par l’utilisateur actuellement connecté. |
| Planification et suivi de projets | 2790384 | Le délai d’attente OperationSet en attente est trop court. |
| Planification et suivi de projets | 2957840 | Les tâches ne peuvent pas être enregistrées et les colonnes ne peuvent pas être ajoutées à la page **Tâches** dans Project Operations intégré. |
| Gestion des ressources | 2751560 | Unités organisationnelles préférées incohérentes dans les besoins en ressources. |
| Sous-traitance | 2853245 | La mise en correspondance des chiffres réels de la ligne de facture fournisseur ne met pas à jour le statut de vérification si une ligne de contrat est déjà liée à la ligne de facture fournisseur. |
| Sous-traitance | 2907231 | L’étape de traitement des factures fournisseur ne peut pas avancer. |
| Temps et dépenses | 2867363 | Les enregistrements ne sortent pas de la vue Absences/Vacances pour approbation lorsqu’ils sont mis en file d’attente pour approbation. |
| Temps et dépenses | 2894405 | TESA : le répertoire POC inutilisé pose des problèmes de conformité. |

### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
