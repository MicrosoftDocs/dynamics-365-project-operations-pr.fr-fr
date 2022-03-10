---
title: Nouveautés de juillet 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de juillet 2021 de Project Operations pour les scénarios basés sur les ressources/hors stock.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008043"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de juillet 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

   - Project Operations dans l’environnement Microsoft Dataverse, version 4.12.0.148 ou 4.12.0.152.
   - Gestion et comptabilité de projets dans l’environnement Dynamics 365 Finance, version 10.0.20.

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Possibilité pour les administrateurs d’afficher les journaux PSS et les journaux d’ensembles d’opérations à partir du menu des paramètres. Les journaux sont stockés pendant 90 jours.

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations.

Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la page **Double écriture** dans la colonne **Version**. Activez une nouvelle version du mappage en sélectionnant **Versions de mappage de table**, en sélectionnant la version la plus récente, puis en enregistrant la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème au démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes dans les mappages](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du Guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités**              | **Numéro de référence** | **Mise à jour qualité**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturation et tarification           | 2224046              | Le champ **Classe de transaction** est modifiable dans l’onglet **Détails de la ligne de devis**, mais est verrouillé si vous travaillez à partir de la page **Détails de la ligne de devis**.                                                                     |
| Facturation et tarification           | 2224400              | L’action **Fermer le devis comme conclu** échoue lorsqu’un devis n’a pas de jalons de date.                                                                                                                                    |
| Facturation et tarification           | 2234089              | Lorsque vous entrez manuellement une description de produit, celle-ci est effacée une fois que vous entrez une quantité pour une estimation de matériel.                                                                                                                         |
| Facturation et tarification           | 2234100              | La grille **Configuration de la facturation de tâches** n’inclut pas la colonne **Matériel** et sa valeur dans l’onglet **Facturation de tâches** du projet.                                                                                                       |
| Facturation et tarification           | 2277409              | L’ID produit n’est pas disponible dans le détail de la ligne de contrat pour une ligne de type de matériel.                                                                                                                                        |
| Facturation et tarification           | 2281728              | La création d’une ligne de contrat réévalue inutilement les chiffres réels, ce qui entraîne des augmentations significatives du volume de données et affecte les performances.                                                                                |
| Facturation et tarification           | 2298668              | Les lignes de journal associées à une dépense rappelée et supprimée ne sont pas supprimées.                                                                                                                                     |
| Facturation et tarification           | 2300192              | Lorsque plusieurs utilisateurs modifient une facture, il est possible de créer un nouveau détail de ligne de facture dans une facture confirmée.                                                                                   |
| Facturation et tarification           | 2301569              | Les factures ne peuvent pas être corrigées si une provision d’un montant de \$0 a été appliquée.                                                                                                                                        |
| Facturation et tarification           | 2307965              | Une erreur se produit si un prix de catégorie est créé avec des valeurs manquantes.                                                                                                                           |
| Facturation et tarification           | 2326870              | Une erreur se produit dans **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** si **producttypecode** a la valeur null.                                                                            |
| Facturation et tarification           | 2332732              | Une erreur se produit si un jalon de ligne de contrat est créé sans ligne de commande.                                                                                                                |
| Planification et suivi de projets | 2181094              | L’API de planification de projets prend désormais en charge les journaux PSS et les journaux d’ensembles d’opérations qui sont stockés pendant 90 jours.                                                                                                                  |
| Planification et suivi de projets | 2254201              | L’étiquette **Mode de planification** est mise à jour avec des détails qui décrivent la logique par défaut.                                                                                                                                      |
| Planification et suivi de projets | 2300252              | Le cache de réponse **openProject** est mis à jour et inclut le propriétaire du jeton dans la clé du cache, l’**URL de base** et l’**URL du segment** afin que l’**URL de demande** puisse toujours être recréée si l’**URL de base** change. |
| Planification et suivi de projets | 2301312              | **msdyn_membershipstatus** a été supprimé de la vue **Membre de l’équipe du projet**.                                                                                                                                        |
| Planification et suivi de projets | 2302759              | Les produits sont extraits inutilement dans les onglets **Affectations de ressources**, **Estimations** et **Estimations des dépenses**.                                                                                                        |
| Planification et suivi de projets | 2308050              | **CopyProject** échoue avec l’erreur, « Impossible d’obtenir le jeton pour parler au service distant ».                                                                                                                           |
| Planification et suivi de projets | 2322650              | La vue **Liste de tâches du projet** a été mise à jour pour afficher la date de la tâche par défaut.                                                                                                            |
| Planification et suivi de projets | 2327266              | **CopyProject** génère l’erreur « Clé introuvable dans le dictionnaire » lors de la copie des estimations.                                                                                                      |
| Planification et suivi de projets | 2328123              | **CopyProject** génère l’erreur, « Impossible d’obtenir le jeton pour parler au service distant ».                                                                                                                          |
| Planification et suivi de projets | 2336258              | **CopyProject** copie de manière incorrecte les noms de poste des ressources.                                                                                                                                                 |
| Facturation et tarification           | 2224476              | Le champ **Ressource réservable** n’est pas correctement défini par défaut sur l’utilisateur connecté dans la page **Utilisation de matériel**.                                                                                                            |
| Gestion des ressources           | 2277249              | Une erreur se produit lorsqu’une ressource requise qui n’est pas basée sur un projet est mise à jour.                                                                                                            |
| Gestion des ressources           | 2323869              | L’utilisation de ressources ne reconnaît pas correctement les ressources filtrées.                                                                                                                                             |
| Temps et dépenses              | 2176538              | Des opérateurs de filtre incorrects sont appliqués au contrôle **Entrée de temps**.                                                                                                                                                   |
| Temps et dépenses              | 2177462              | La suppression d’une entrée de temps dans la grille ne met pas à jour le statut des boutons **Soumettre**, **Rappeler**, **Supprimer** et **Modifier l’entrée** comme prévu.                                                                                        |
| Temps et dépenses              | 2299985              | **TimeEntriesImportFromResourceAssignment** ne maintient pas l’heure de début/fin des contours d’affectation.                                                                                                  |
| Temps et dépenses              | 2318426              | Une fois qu’une entrée de temps est envoyée, les champs verrouillés peuvent toujours être modifiés.                                                                                                                                   |
| Temps et dépenses              | 2323749              | Une erreur se produit lorsqu’une dépense est créée dans l’onglet **Associé** d’une ressource réservable.                                                                                                      |
| Temps et dépenses              | 2327678              | Lorsque vous créez une entrée de temps dans l’onglet **Associé** d’une ressource réservable, la ressource parent n’est pas transmise au contrôle d’entrée de temps.                                                                            |
| GÉNÉRAL                       | 2296857              | Suivi de la progression pour les tâches de longue durée.                                                                                                                                                                        |
| GÉNÉRAL                       | 2253682              | La solution de double écriture de Project Operations ne doit pas être installée lorsque le noyau de double écriture est installée dans un environnement sans la solution d’orchestration de la double écriture.                                                |
| GÉNÉRAL                       | 2316420              | La mise en service du noyau de Project Service échoue si la division de l’utilisateur de l’application est modifiée.                                                                                                                     |
| GÉNÉRAL                       | 2376405              | Correction d′un problème de mise à jour piloté par l′éditeur (la mise à jour de qualité est disponible dans la version 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestion de projets et comptabilité dans Dynamics 365 Finance

| Fonctionnalités                      | Numéro de référence | Mise à jour qualité                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestion et comptabilité des projets | 4620267          | Impossible de personnaliser les formulaires pour ajouter un champ **Finalité** aux pages **Transaction de projet validée**, **Création de proposition de facture** et **Proposition de facture**.                                                                                                                                                                                         |
| Gestion et comptabilité des projets | 4613449          | Lorsque vous sélectionnez un ID de contrat de projet dans Finance, l’environnement intégré Project Operations ouvre la page pour créer un nouvel enregistrement, au lieu de la page des contrats de projet déjà créés.                                                                                                                                           |
| Gestion et comptabilité des projets | 4614445          | Dans le déploiement du scénario intégré de Project Operations, vous ne pouvez pas modifier le champ **Groupe de taxe d’article** dans la proposition de facture importée depuis la table intermédiaire. Le groupe de taxe d’article doit être modifiable pour une proposition de facture ouverte de tous les types de transaction, y compris les comptes, heures, dépenses, frais et articles. |
| Gestion et comptabilité des projets |                  | Impossible de valider une proposition de facture résultant d’une correction de transaction de temps négative.                                                                                                                                                                                                                                              |
| Gestion et comptabilité des projets |                  | Les lignes de proposition de facture sont dupliquées en raison de plusieurs processus périodiques **Importer depuis la table intermédiaire** qui s’exécutent en même temps.                                                                                                                                                                                                                |

