---
title: Nouveautés de novembre 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de novembre 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827323"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de novembre 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.26.0.145, 4.26.0.148 ou 4.26.0.150
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.22

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Les interfaces de programmation d’applications (API) de la Planification de projets prennent désormais en charge la possibilité de créer et de supprimer des compartiments de projet.

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-in-dataverse"></a>Project Operations dans Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2240080 | Le champ **Conditions de paiement** ne doit pas être dupliqué sur la facture pro forma. |
| Facturation et tarification | 2358236 | La correction de facture doit permettre des corrections qui ont des lignes à prix zéro. |
| Gestion des ressources | 2410072 | Autoriser la configuration d’une ressource affectée à la tâche en tant que chef de projet. |
| Facturation et tarification | 2430234 | Correction d’un problème de calcul des performances de coût. |
| Temps et dépenses | 2436978 | Permettre à l’heure d’être saisie au format hh:mm. |
| Facturation et tarification | 2448623 | Autoriser la mise à jour des tarifs après leur association à une unité d’organisation. |
| Temps et dépenses | 2460396 | Autoriser la suppression d’une entrée de temps en effaçant la cellule. |
| Facturation et tarification | 2467386 | Autoriser la suppression d’un projet comportant une tâche, même lorsque la tâche est associée à un devis remporté. |
| Temps et dépenses | 2461744 | La vue **Mes approbations ayant échoué** ne contient que les approbations de projet à la phase **Envoyé**. |
| Temps et dépenses | 2464082 | Supprimer le lien entre les approbations de projet et l’ensemble d’approbations lorsqu’un statut cible correspond. |
| Temps et dépenses | 2468108 | Le travail de planification ne doit pas définir de statut **Traitement en cours** pour l’ensemble d’approbations. |
| Temps et dépenses | 2471503 | Supprimer les ensembles d’approbation datant de sept jours. |
| Facturation et tarification | 2480687 | La référence de ligne de devis ne doit pas être supprimée lorsqu’un jalon de ligne de devis est créé. |

### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion et comptabilité des projets | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Les montants fournisseurs retenus dans les transactions de dépenses de projet ne sont pas affichés dans la liste des transactions. |
| Gestion et comptabilité des projets | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La facture fournisseur intersociétés est interrompue lorsque l’intégration de la facture fournisseur est activée. |
| Gestion et comptabilité des projets | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les conditions de paiement sur les factures de projet ne fonctionnent pas comme prévu. |
| Gestion et comptabilité des projets | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Lorsque la rétention du fournisseur est libérée, la validation du numéro document comporte des lignes supplémentaires qui sont incorrectes. |
| Gestion et comptabilité des projets | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Lorsque le journal d’intégration Project Operations est validé, il échoue en raison de dimensions manquantes pour un compte qui n’est pas celui de la validation. |
| Gestion et comptabilité des projets | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | L’onglet **Projet** n’est pas modifiable sur une facture fournisseur en attente lorsque la catégorie d’approvisionnement est affectée à l’article. |
| Gestion et comptabilité des projets | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Le volet de navigation est absent si vous n’êtes pas connecté au Dataverse de Project Operations. |
| Gestion et comptabilité des projets | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Lorsque vous validez le produit à partir d’une facture de projet dans le cas de d’application d’une provision, une erreur se produit parce que les transactions ne sont pas équilibrées sur la pièce justificative. |
| Gestion et comptabilité des projets | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La création d’un devis après validation d’une proposition de facture empêche l’importation des lignes de correction. |
| Gestion et comptabilité des projets | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | La modification d’un enregistrement de jalon entièrement facturé ne devrait pas être possible. |
| Déplacement et dépenses | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Toutes les notes de frais sont visibles lorsque vous recherchez une catégorie dans l’application mobile Gestion des dépenses. |
| Déplacement et dépenses | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Des montants incorrects sur les transactions fournisseur et les transactions de taxe de vente sont validés à partir d’une dépense créée à partir d’une transaction par carte de crédit. |
| Déplacement et dépenses | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un message d’avertissement non pertinent apparaît lorsque vous actualisez la page **Note de frais**. |
| Déplacement et dépenses | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Le mauvais approbateur provisoire est utilisé lorsque vous supprimez un approbateur provisoire, puis soumettez à nouveau la note de frais via le workflow. |
| Déplacement et dépenses | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Une erreur de validation se produit, qui est liée à la configuration du kilométrage. |
