---
title: Nouveautés de septembre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour qualité disponibles dans la version de septembre 2022 de Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634802"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de septembre 2022 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.46.0.60
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.29

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

| Fonctionnalités | Nom de la fonction | Plus d’informations |
| --- | --- | --- |
| Gestion des opportunités | **Révision et activation de devis**<br>Project Operations assure la prise en charge complète du processus de vente. Les devis de projet peuvent être activés pour représenter un état dans lequel le devis est en lecture seule et en cours de révision. Les devis activés peuvent être révisés pour créer de nouveaux devis qui ont un numéro de révision incrémenté. Les devis de projet ou les révisions de devis activés peuvent être fermés comme conclus ou perdus. | [Activer et réviser un devis de projet](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturation et tarification | **Prix par défaut indépendant du fuseau horaire**<br>Project Operations a introduit le concept d’une date indépendante du fuseau horaire pour tous les chiffres réels du projet. Un nouveau champ, **Date de la transaction**, est maintenant disponible sur les lignes de journal et les chiffres réels, et sera utilisé pour stocker la date à laquelle la transaction s’est produite, mais sans convertir cette date en temps universel coordonné. Cette date sera utilisée pour les processus en aval tels que les prix par défaut et la création de factures. | <p>[Déterminer les taux de coût pour les estimations et les réels du projet](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Déterminer les prix de vente pour les estimations et les chiffres réels du projet](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturation et tarification | **Remplacements de prix à la date d’effet dans Project Operations**<br>Les Remplacements de prix à la date d’effet fournissent un moyen de remplacer ou de modifier des prix spécifiques dans la liste de prix. | [Remplacements de prix avec date d’effet](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Sous-traitance | **Rapprochement des factures de sous-traitance et fournisseur**<br>Cette fonctionnalité permet aux clients de créer des contrats de sous-traitance pour acheter du temps de ressource, des catégories de dépenses et du matérial qui sont utilisés pour le travail du projet. Elle permet également aux clients d’enregistrer, dans les applications de finances et d’opérations, les factures fournisseur qui seront mises à la disposition des chefs de projet dans Dataverse pour vérification. | <p>[Gestion des sous-traitants](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Créer des factures fournisseur](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Temps et dépenses | **Approbateur global**<br>Cette fonctionnalité active les éditeurs de logiciels indépendants (ISV) et l’approbation centralisée, quel que soit le projet ou le statut des membres de l’équipe dans le projet. | [Sécurité et approbations](/dynamics365/project-operations/approvals/approvals-security) |
| Gestion des dépenses | **Possibilité de publier le passif des dépenses dans la devise du fournisseur**<br>Cette fonctionnalité active les rapports de dépenses qui seront publiés dans une devise du fournisseur pour le mode de paiement en espèces. | [Possibilité de publier le passif des dépenses dans la devise du fournisseur](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Approvisionnement du projet | **Payer quand les paiements des fournisseurs sont payés**<br>Cette fonctionnalité permet d’utiliser la fonction Payer au moment du paiement (PWP) avec les environnements hors stock de Project Operations. Elle permet de bloquer/conserver les paiements fournisseur, en fonction des conditions de rétention, jusqu’à ce que le paiement soit reçu du client. | [Payer quand les paiements des fournisseurs sont payés](/dynamics365/project-operations/procurement/pay-when-paid) |
| Approvisionnement du projet | **Demandes d’achat du projet**<br>Cette fonctionnalité permet aux utilisateurs de créer des commandes fournisseur liées à un projet dans les entités juridiques où l’intégration de Project Operations sur Dynamics 365 Customer Engagement est activée. Les commandes fournisseur du projet peuvent être utilisées pour enregistrer l’approvisionnement en matériel hors stock par rapport au projet par la personne du département Approvisionnement. Les commandes fournisseur du projet ne seront pas synchronisés avec Dataverse. Cependant, vous pouvez utiliser une entité virtuelle pour afficher les lignes de commande fournisseur du projet dans Dataverse pour les informations du chef de projet. Le coût de la facture fournisseur liée au projet est intégré à l’entité Chiffres réels du projet dans Dataverse. Le coût du projet est enregistré dans la comptabilité auxilliaire du projet à l’aide du journal Intégration de Project Operations. | |
|Planification et suivi de projets|**Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification** </br> </br>L’API de modification des contours d’affectation des ressources permet aux développeurs de spécifier par programme l’effort d’une personne affectée à une tâche sur n’importe quelle plage de dates prise en charge pour une planification d’effort échelonnée dans le temps plus granulaire.|[Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Le tableau suivant présente les cartes en double écriture qui ont été modifiées ou ajoutées dans la version de septembre 2022 de Project Operations.

| Mappage d’entité | Version mise à jour | Commentaires |
| -------------- | ------------------- | ------------|
| Chiffres réels d’intégration Project Operations (msdyn_actuals) | 1.0.0.15 | Cette carte prend en charge le traitement des chiffres réels de sous-traitance avec Project Operations pour les scénarios basés sur les ressources. |
| Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Cette carte prend en charge le traitement des chiffres réels de sous-traitance avec Project Operations pour les scénarios basés sur les ressources. |
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Cette carte prend en charge le traitement des chiffres réels de sous-traitance avec Project Operations pour les scénarios basés sur les ressources. |

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2754422 | Les estimations de matériel et de dépense ne sont pas envoyées à Finance lorsque les projets sont copiés dans Dataverse. |
| Temps et dépenses | 2787409 | Un approbateur non valide peut approuver une entrée de temps hors projet. |
| Gestion des opportunités | 2788907 | Message d’erreur mis à jour sur la validation de l’unicité pour les lignes de commande incluant des balises. |
| Temps et dépenses | 2842253 | Gestion des exceptions nulles pour l’approbation du temps. |
| Facturation et tarification | 2844181 | L’impossibilité d’obtenir l’ID de corrélation bloque la création de la facture. |
| Facturation et tarification | 2876628 | QLD, CLD - La résolution de la liste de prix de l’estimation doit utiliser les champs de plage de dates hérités de la liste de prix. |
| Sous-traitance | 2893222 | Si aucun rôle n’est spécifié pour une ligne de sous-traitance, il devrait être possible de sélectionner cette ligne d’un membre de l’équipe pour n’importe quel rôle. |

### <a name="project-management-and-accounting-in-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Finance

Pour plus d’informations sur les correctifs de bogues inclus dans cette mise à jour, connectez-vous à Microsoft Dynamics Lifecycle Services et consultez l’[Article de la base de connaissances](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fonctionnalités activées par défaut dans la prochaine version

Le tableau suivant répertorie les fonctionnalités qui sont activées par défaut dans la version 10.0.30. La plupart des fonctionnalités qui ont été activées automatiquement peuvent être désactivées dans [Gestion des fonctionnalités](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). À l'avenir, certaines fonctionnalités qui ont été automatiquement activées pourraient être supprimées de la gestion des fonctionnalités et devenir obligatoires. Cette modification garantit que les clients utilisent les fonctionnalités actuelles, de sorte que les améliorations peuvent s'appuyer sur les fonctionnalités actuelles au fur et à mesure de leur ajout. Les fonctionnalités ne seront jamais automatiquement activées en moins d'un an, à moins qu'elles ne soient jugées essentielles.

| Nom de la fonction | Date d’activation | Fonction ajoutée le | État de la fonctionnalité | Module |
| --- | --- | --- |--- |--- |
| Activer l’opération asynchrone lorsque l’utilisateur doit permuter entre les opérations synchrones et asynchrones | 21 octobre 2022 | 9 avril 2021 | Activé par défaut | Gestion des dépenses |
| Évaluation de la stratégie de dépense pour les reçus requise | 21 octobre 2022 | 20 décembre 2021 | Activé par défaut | Gestion des dépenses |
| Vue de liste des notes de frais créées par les travailleurs délégués | 21 octobre 2022 | 19 février 2020 | Activé par défaut | Gestion des dépenses |
| Calcul du kilométrage total par exercice | 21 octobre 2022 | 10 mai 2022 | Activé par défaut | Gestion des dépenses |
