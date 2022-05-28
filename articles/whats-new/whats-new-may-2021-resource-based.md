---
title: Nouveautés de mai 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de mai 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723765"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de mai 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

- Project Operations sous environnement Dynamics 365 Dataverse version 4.10.0.186
- Gestion de projet et comptabilité dans les environnements d’applications de finances et d’opérations version 10.0.18

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- [Modes de planification](../project-management/scheduling-modes.md) : les chefs de projet peuvent définir si un projet doit être géré en suivant le mode de planification à durée fixe, travail fixe ou unités fixes.
- [Configurer le kilométrage à l’aide de barèmes de kilométrage](../expense/set-up-mileage.md) : permet de mettre à jour les niveaux de taux de kilométrage pour les notes de frais des employés.

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages à double écriture Project Operations

La liste suivante répertorie les mappages à double écriture qui ont été modifiés ou ajoutés dans la version de mai 2021 de Project Operations.

| Mappage d’entité | Version mise à jour | Commentaires |
| --- | --- | --- |
| Source de financement de projet (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synchronisation des conditions de paiement des clients du contrat de projet. |
| Proposition de facture de projet V2 (factures) | 1.0.0.3 | Synchronisation des conditions de paiement des factures pro forma. |
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Mises à jour qualité |
| Projets V2 (msdyn\_projects) | 1.0.0.2 | Mises à jour qualité |

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution des applications de finances et d’opérations. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les mappages](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage consacré à la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2227635 | Les valeurs des champs **Groupe d’unités** et **Unité** prennent les valeurs par défaut provenant du produit dans la grille **Estimations du matériel**. |
| Facturation et tarification | 2234127 | Le champ **ID de tâche** s’intègre désormais correctement aux chiffres du projet Dataverse lorsqu’une facture fournisseur est validée. |
| Facturation et tarification | 2235564 | L’enregistrement de la ligne de journal garantit que la devise affichée dans l’écriture comptable correspond à la devise par défaut de la ligne après l’enregistrement. |
| Facturation et tarification | 2246671 | Rendre une transaction non facturable lors de la facturation annule l’enregistrement des ventes non facturées d’origine et crée un nouvel enregistrement des ventes non facturées comme non facturables. |
| Facturation et tarification | 2264042 | Une correction de facture valide ne doit pas être bloquée si un détail de correction de facture n’est pas valide dans l’environnement. |
| Facturation et tarification | 2146367 | Le mappage en double écriture de l’en-tête de facture du projet est étendu pour inclure les conditions de paiement. |
| Gestion des opportunités | 2086888 | N’ajoutez pas de rôles et de catégories désactivés avant de copier un devis dans les rôles et catégories facturables d’un devis nouvellement copié. |
| Gestion des opportunités | 2234376 | Les champs en lecture seule sont grisés dans la grille **Estimations du matériel**. |
| Gestion des opportunités | 2238337 | Un devis basé sur un contact peut être enregistré même s’il n’est pas associé à une liste de prix de projet. |
| Gestion des opportunités | 2239810 | La clôture d’un devis comme perdu ferme également le projet associé et annule toute réservation. |
| Planification et suivi de projets | 2099559 | Ajout de validations supplémentaires de l’intégrité du système avant l’ouverture de la grille **Tâches du projet**. |
| Planification et suivi de projets | 2178987 | Correction d’une erreur transitoire qui se produisait lors de la sélection de **Étape suivante** sur la page **Projet**. |
| Gestion des ressources | 2224817 | La fonctionnalité d’extension des réservations utilise par défaut le statut de réservation correct. |
| Saisie de l’heure | 2202476 | La page **Entrée de temps** utilise désormais le contrôle de grille réactif et corrige des problèmes tels que le mauvais alignement de la grille. |
| Saisie de l’heure | 2223377 | La saisie du temps est masquée dans la section **Connexe** de la page **Ressource réservable** pour éviter toute confusion avec l’utilisation. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion et comptabilité des projets | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations, pour les scénarios basés sur les ressources : impossible d’attribuer le statut « Conclu » à un devis en raison d’une une erreur d’intégration. |
| Gestion et comptabilité des projets | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations : un message d’erreur s’affiche lorsque vous essayez d’associer une ligne de contrat à un ID de projet en raison de la vérification de chevauchement des lignes de contrat et des types de transaction. |
| Gestion et comptabilité des projets | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** définit l’adresse de facturation de la source de financement d’un autre client. |
| Déplacement et dépenses | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Une erreur de validation liée à la configuration du kilométrage peut se produire. |
| Déplacement et dépenses | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | La fonctionnalité **Fractionner en personnel** ne fonctionne pas pour les transactions de dépenses en devises étrangères. |
| Déplacement et dépenses | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Les valeurs déroulantes des catégories de dépenses affichent des catégories incorrectes pour les délégués, qu’il s’agisse ou non d’une ressource. |
| Déplacement et dépenses | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Vous ne pouvez pas enregistrer une note de frais intersociétés en raison d’une erreur de **Validation de ressource/catégorie**. |
| Déplacement et dépenses | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Le mauvais calcul des indemnités kilométriques dans la comptabilisation des notes de frais comporte des lignes fractionnées. |
| Déplacement et dépenses | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Vous ne pouvez pas valider une note de frais intersociétés lorsque la taxe de vente est incluse et que le type de compte de contrepartie sur le mode de paiement est **Employé**. |
| Déplacement et dépenses | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | L’annulation de l’entité de données **TrvRequisitionLine** et l’index unique sont associés. |
| Déplacement et dépenses | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | La note de frais prend en charge la création et la mise à jour de la ligne du document source. |
| Déplacement et dépenses | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un journal de la comptabilité auxiliaire incorrect s’affiche dans un scénario intersociétés si la taxe de vente est validée pour l’entité juridique de destination. |
| Déplacement et dépenses | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations : l’estimation de dépenses n’est pas supprimée de Finance lorsqu’elle est supprimée de Dataverse. |
| Déplacement et dépenses | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Lorsque la catégorie de dépense est une catégorie non liée au projet, les dimensions financières sélectionnées sur la page **Dépenses** ne sont pas copiées dans la note de frais. |
