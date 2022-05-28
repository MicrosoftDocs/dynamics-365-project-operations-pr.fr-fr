---
title: Nouveautés de mars 2022 – Project Operations pour les scénarios selon les ressources/produits non stockés
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de mars 2022 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600739"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de mars 2022 – Project Operations pour les scénarios selon les ressources/produits non stockés

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.30.0.99
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.25

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les indemnités journalières sont désormais prises en charge dans le nouvel espace de travail des dépenses moderne revisité. Les entreprises qui utilisent des indemnités journalières peuvent activer cette fonctionnalité pour offrir aux utilisateurs un moyen simple de soumettre et d’être remboursés pour leurs dépenses d’indemnités journalières. Pour plus d’informations, consultez [Dépenses d’indemnités journalières](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

La liste suivante présente les cartes en double écriture qui ont été modifiées ou ajoutées dans la version de mars 2022 de Project Operations.

| **Mappage d’entité** | **Version mise à jour** | **Commentaires** |
| --- | --- | --- |
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mappages mis à jour pour s’aligner sur l’entité de ligne de facture fournisseur dans Dataverse. <br>N’activez pas la version de mappage 1.0.0.4. Elle sera prête à être utilisée en combinaison avec la version 10.0.26 de l’environnement Finance dans la prochaine mise à jour mensuelle. |

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Temps et dépenses | 2388011 | Afficher les commentaires de rejet aux auteurs de saisie de temps lors de l’approbation groupée. |
| Planification et de suivi de projets | 2495294 | Les détails du projet ne doivent pas être modifiables sur la page **Détails de la tâche**. |
| Facturation et tarification | 2499605 | Les jalons de contrat créés à partir de jalons de devis sont marqués à tort en lecture seule. |
| Planification et de suivi de projets | 2506050 | L’ensemble d’opérations reste en attente pendant une heure s’il n’y a pas de modification à enregistrer. L’ensemble est alors faussement marqué comme **Échec**, alors qu’il devrait être achevé immédiatement. |
| Facturation et tarification | 2507401 | Les unités de contrat par défaut sont saisies de manière incorrecte sur les projets en raison d’une mise en cache incorrecte. |
| Facturation et tarification | 2541660 | **Validation de la création de la commande client** en double écriture ne doit concerner que les commandes basées sur un projet. |
| Facturation et tarification | 2552745 | La taxe n’est pas répartie entre les clients qui ont configuré des règles de facturation fractionnée. |
| Facturation et tarification | 2558859 | Messages d’erreur améliorés lors de la configuration des dimensions de tarification. |
| Facturation et tarification | 2558933 | **Importer à partir des estimations de projet** échoue lorsque **msdyn\_project** est ajouté en tant que dimension de tarification. |
| Facturation et tarification | 2559101 | La suppression des paramètres du projet n’est pas bloquée et pose des problèmes. |
| Gestion des opportunités | 2570390 | Le plug-in en double écriture force le type de compte sur les devis, les commandes et les opportunités à être défini sur **Client**, même lorsque ce type de compte n’est pas correct. |
| Facturation et tarification | 2586097 | Les chiffres réels du coût facturés fractionnés ne sont pas annulés lorsqu’un projet est supprimé d’une ligne de contrat de projet. |
| Facturation et tarification | 2589619 | La taxe sur le matériel hors catalogue est propagée aux ventes réelles non facturées et à la facture. |
| Gestion des opportunités | 2594015 | Un devis ne peut pas être clôturé comme gagné pour les clients qui ont des modalités de paiement **Net60**. |
| Planification et de suivi de projets | 2595841 | Dans Project for the Web, les utilisateurs reçoivent un message d’erreur concernant un **msdyn\_actualstart** manquant lorsqu’ils créent une nouvelle demande de ressources. |
| Temps et dépenses | 2602511 | Le champ **Rejeté par** pour les entrées de temps montre **Système** au lieu d’un utilisateur nommé comme rejeteur. |
| Temps et dépenses | 2602528 | Un approbateur de projet peut approuver du temps sur des projets pour lesquels il n’est pas répertorié en tant qu’approbateur. |
| Facturation et tarification | 2608550 | Une facture de correction peut être confirmée même s’il n’y a aucun changement par rapport à l’original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets sur Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion et comptabilité des projets | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Il y a un décalage entre Finance et Project Operations dans la durée autorisée du champ **ID de catégorie**. |
| Gestion et comptabilité des projets | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Les projets à prix fixe ne peuvent pas être éliminés lorsque le champ **Facturation en compte** est défini sur **Profit et perte** et le principe **Pourcentage terminé** est utilisé. |
| Gestion et comptabilité des projets | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Un groupe de taxe de vente par défaut incorrect est entré à partir de la configuration du projet sur les lignes de dépense dans le journal d’intégration de Project Operations. |
| Gestion et comptabilité des projets | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Vous ne pouvez pas modifier les dimensions d’en-tête de proposition de facture de projet dans un déploiement intégré avec Project Operations. |
| Gestion et comptabilité des projets | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Les factures fournisseur intersociétés ne doivent pas être intégrées à Dataverse. |
| Gestion et comptabilité des projets | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Il y a une incohérence entre la devise des soldes des clients et la devise de déclaration. |
| Gestion et comptabilité des projets | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Vous pouvez valider une facture de projet même si le client est en attente pour toutes les factures. |
| Gestion et comptabilité des projets | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Le bouton **Supprimer toutes les lignes** est absent des propositions de facture de projet qui ont les vues **En-tête** et **Lignes**. |
| Gestion et comptabilité des projets | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Lorsque vous validez une facture fournisseur, l’erreur suivante se produit : « La date comptable de la facture doit être dans le même exercice comptable que la commande fournisseur associée. Exécutez le processus de fin d’exercice du bon de commande ou remplacez la date par l’exercice comptable en cours. » |
| Déplacement et dépenses | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Le coût engagé d’un projet n’est pas débloqué une fois que le coût engagé de la demande de déplacement est débloqué. |
| Déplacement et dépenses | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | L’erreur suivante se produit lorsque vous soumettez une note de frais : « Arborescence des appels de procédure : l’entreprise n’existe pas. » |
| Déplacement et dépenses | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | La valeur par défaut **ID de projet** n’est pas inscrite sur les notes de frais lorsque le paramètre **Exiger une activité pour le journal** est sélectionné sur le projet. |
| Déplacement et dépenses | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Le bouton **Publier les dépenses** ne fonctionne pas correctement dans Project Operations pour les scénarios de ressources/non stockés. |
| Déplacement et dépenses | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Il y a un problème avec **Tarif au kilomètre** pour une note de frais kilométrique incluant les passagers. |
| Déplacement et dépenses | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Les indemnités kilométriques des dépenses pour les employés ne sont pas correctement totalisées lorsque deux types de véhicules différents sont utilisés dans la catégorie de dépenses **Barème de frais kilométriques**. |
| Déplacement et dépenses | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | La recherche du champ **Projet** sur une ligne de demande de déplacement ne renvoie pas la bonne liste de projets. |
| Déplacement et dépenses | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilométrage en cours de révision** affiche un avertissement sur les notes de frais. |
| Déplacement et dépenses | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Le service de reconnaissance optique des caractères (OCR) des reçus ne fonctionne pas en raison d’un problème avec l’URL du service OCR des dépenses. |
| Déplacement et dépenses | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quand la fonctionnalité **Capacité à détailler rapidement les dépenses récurrentes** est activée, les montants sur les lignes de détail des notes de frais changent chaque fois que la page **Détailler** est ouverte. |
| Déplacement et dépenses | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Vous ne pouvez pas supprimer une note de frais lorsque la liste provisoire a plus d’un approbateur. |

## <a name="removed-and-deprecated-features"></a>Fonctionnalités supprimées et obsolètes

La rubrique [Fonctionnalités supprimées ou obsolètes dans Project Operations](removed-depreciated-features-project.md) décrit les fonctionnalités qui ont été supprimées ou obsolètes pour Dynamics 365 Project Operations.

- Une fonctionnalité supprimée n’est plus disponible dans le produit.
- Une fonction déconseillée n’est pas en développement actif et peut être supprimée dans une prochaine mise à jour.

Une annonce d’obsolescence apparaît dans la rubrique [Fonctionnalités supprimées ou obsolètes dans Project Operations](removed-depreciated-features-project.md) 12 mois avant le retrait.

Pour les dernières modifications qui n’affectent que le temps de compilation, mais qui sont compatibles d’un point de vue binaire avec les environnements sandbox et de production, le temps d’obsolescence sera inférieur à 12 mois. Ce sont généralement des mises à jour fonctionnelles qui doivent être apportées au compilateur.
