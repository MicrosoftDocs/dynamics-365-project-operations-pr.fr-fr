---
title: Nouveautés de janvier 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de janvier 2021 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958907"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de janvier 2021 – Project Operations pour les scénarios selon les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Cette rubrique s'applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.6.0.154 de Project Operations dans l’environnement Dataverse
  - Version 10.0.16 de gestion de projet et comptabilité dans l’environnement de Dynamics 365 Finance

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Zone Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| **Déploiement et configuration** | 2106818 | Correction du changement de nom de la ressource web qui causait des problèmes liés à la personnalisation d'une page. |
| **Facturation et tarification** | 2091908 | Correction de la visibilité des options **Tarification de verrouillage** et **Utiliser la tarification actuelle** sur la page **Facture** lorsque Project Operations est installé avec Dynamics 365 Field Service. |
| **Facturation et tarification** | 2103058 | Actualisation des **Totaux du projet** pour gérer les valeurs nulles pour le coût réel d'une tâche. |
| **Facturation et tarification** | 2116100 | Amélioration des messages d'erreur utilisés avec la fonctionnalité, **Corriger les entrées sur les chiffres réels**. |
| **Facturation et tarification** | 2116129 | Amélioration de la visibilité des estimations de dépenses sur l'onglet **Estimations** de la page **Projets**. |
| **Facturation et tarification** | 2119112 | Agrégation fixe des ventes réelles et du coût réel lorsque différents taux de change sont utilisés. |
| **Facturation et tarification** | 2134705 | Correction de l'erreur "Impossible de lire la propriété **getResourceString** de non défini" lorsque la page **Facture** est ouverte et que Field Service est installé. |
| **Gestion des opportunités** | 2022195 | La grille de facturation basée sur les tâches sur la page **Projet** comprend une icône indiquant qu'un contrat ou une ligne de devis est lié à cette tâche. |
| **Gestion des opportunités** | 2029135 | Correction de l'erreur de processus d'entreprise qui se produit lorsqu'un utilisateur tente d'ouvrir une ligne de facture sur une facture confirmée avec un montant d'avance facturé. |
| **Gestion des opportunités** | 2040713 | Correction de l'erreur de script qui se produit lors de la création d'une facture à partir d'un contrat et de l'installation de Field Service. |
| **Planification et suivi de projets** | 2090202 | Les règles métier marquées qui ne sont plus utilisées comme **Obsolètes**. |
| **Temps et dépenses** | 2091249 | Des contrôles renforcés afin que les utilisateurs ne puissent pas modifier la tâche sur une entrée de temps approuvée ou soumise. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestion du projet et comptabilité dans Dynamics 365 Finance

| **Zone Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| **Gestion et comptabilité des projets** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Montant du contrat incorrect sur la page **Sur compte** pour un projet à prix fixe avec plusieurs sources de financement. |
| **Gestion et comptabilité des projets** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | L'espace réservé **Invoiceproposal.PSAnfRefProjId** n'affiche pas l'ID de projet pour le workflow, **Examiner les propositions de facture de projet**. |
| **Gestion et comptabilité des projets** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | La mauvaise date d'escompte est utilisée lors de la validation des propositions de facture de projet. |
| **Gestion et comptabilité des projets** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | La suppression et l'affectation de ressource dans Project Operations double les entrées de prévision de projet dans Finance. |
| **Gestion et comptabilité des projets** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Dans Project Operations, vous ne pouvez pas créer d'estimations de projet dans Dataverse sans avoir une ligne de contrat sur le projet. |
| **Gestion et comptabilité des projets** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | La dimension financière d'une transaction de dépenses de projet n'est pas synchronisée avec le document associé et la répartition comptable de la note de frais lorsque les coûts sont imputés au solde. |
| **Gestion et comptabilité des projets** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Le filtre **Statut de la facture** dans les transactions de projet validées pour les projets à prix fixe ne fonctionne pas. |
| **Gestion et comptabilité des projets** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L'élimination des estimations inversées ne fonctionne pas dans la section **Périodique**. |
| **Gestion et comptabilité des projets** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Les lignes de proposition de facture peuvent être supprimées dans Project Operations s'il est intégré à Dataverse. |
| **Gestion et comptabilité des projets** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Éviter d'activer la fonctionnalité Plusieurs lignes de contrat sans intégration Dataverse. |
| **Gestion et comptabilité des projets** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Lorsque la facturation en compte est égale aux bénéfices et aux pertes, les revenus facturés sont indiqués comme zéro sur la page Estimations. |
| **Gestion et comptabilité des projets** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Les corrections de facture ne fonctionnent pas dans des environnements intégrés. |
| **Gestion et comptabilité des projets** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Lors de la validation d'une valeur de vente – TEC dans la facturation de projets intersociétés, le compte incorrect est sélectionné. |
| **Gestion et comptabilité des projets** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Dans Project Operations, les dépendances sur les tâches d'estimation dans Dataverse ne peuvent pas être mises à jour. |
| **Gestion et comptabilité des projets** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | La suppression répétée des journaux d'intégration Project Operations dans Finance entraîne une perte de données. |
| **Gestion et comptabilité des projets** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | L'erreur suivante se produit lorsque la validation d'une proposition de facture de projet "une transaction n'est pas équilibrée dans la devise de rapport lorsque la facture anticipée déduite est ajoutée". |
| **Gestion et comptabilité des projets** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Un ID de projet incorrect est inclus dans les déductions après la mise à jour du contrat de projet par défaut dans Project Operations. |
| **Gestion et comptabilité des projets** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | L'estimation et la comptabilisation des revenus ne peuvent pas être terminées lorsque Project Operations est activé. |
| **Gestion et comptabilité des projets** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Dans Project Operations, la suppression d'un projet d'un contrat ne réinitialise pas le projet par défaut sur le contrat. |
| **Gestion et comptabilité des projets** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Dans Project Operations, sur une facture intersociétés, les mauvaises lignes de dépenses apparaissent dans la liste **Ajouter une ligne**. |
| **Déplacement et dépenses** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Les lignes de dépenses ne peuvent pas être validées car la configuration de l'heure est manquante sur la ligne du contrat. |
| **Déplacement et dépenses** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Lorsque la validation de projet/catégorie est obligatoire, les catégories de dépenses associées au projet ne sont pas visibles dans la note de frais. |
| **Déplacement et dépenses** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Le solde de l'avance de trésorerie n'est pas mis à jour lorsqu'une note de frais est validée par ligne. |
| **Déplacement et dépenses** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | La tâche **Mettre à jour les informations de paiement** échoue après l'annulation des règlements lorsqu'une facture a été réglée avec au moins deux opérations de paiement. |
| **Déplacement et dépenses** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Un problème est survenu avec le calcul de la réduction du repas du dernier jour pour la catégorie de dépenses journalières. |
| **Déplacement et dépenses** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Le rapport **type de dépense par employé** n'indique pas les dépenses détaillées si la première connexion d'un utilisateur était dans la langue es-MX. |
| **Déplacement et dépenses** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Le paiement fournisseur pour une facture de note de frais utilise le mauvais compte de synthèse pour la comptabilisation du règlement. |
| **Déplacement et dépenses** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Lorsqu'une note de frais est validée avec **Autoriser le regroupement des transactions en fonction du compte de paiement compensé** et **Correction de la date comptable lors de la comptabilisation** activés indique que les dates comptables ne sont pas regroupées dans la table **Répartition comptable**, ce qui a une incidence sur les enregistrements de taxe. |
| **Déplacement et dépenses** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Le mappage de sous-catégorie de dépenses est supprimé lorsque la case Utiliser dans les dépenses est décochée, puis cochée à nouveau. |
| **Déplacement et dépenses** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Une note de frais intersociétés ne peut pas être créée si l'ID de projet est ajouté au niveau de l'en-tête. |
| **Déplacement et dépenses** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Un problème avec les paiements des dépenses survient lorsque le montant des dépenses est supérieur au montant de l'avance de fonds. |
| **Déplacement et dépenses** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Le champ **ID de projet** sur une note de frais intersociétés sont vides si le rôle d'utilisateur est attribué à une organisation spécifique. |
| **Déplacement et dépenses** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | La catégorie de dépense est verrouillée lors de l'ajout d'une nouvelle ligne de dépense. |
| **Déplacement et dépenses** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Le détail des lignes de note de frais qui sont déjà fractionnées entraîne un document comptable incomplet des comptes fournisseurs\comptabilité. En raison de la duplication de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, l'Explorateur de sources de comptabilité est également endommagé. |
| **Déplacement et dépenses** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | L'index ajouté sur la table **TRVREQUISITIONLINE** pour laquelle le client a des doublons, entraîne une erreur lors de la mise à niveau. |
| **Déplacement et dépenses** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Dans Project Operations, le temps passé avec les tâches intersociétés dans Dataverse ne peut pas être créé ou approuvé. |

## <a name="regulatory-updates"></a>Mises à jour réglementaires

Pour plus d’informations sur les mises à jour réglementaires pour les applications Finance and Operations, consultez [Mises à jour réglementaires](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à LCS et afficher les mises à jour réglementaires planifiées à l’aide de l’outil de recherche d’incidents. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../includes/footer-banner.md)]