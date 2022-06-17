---
title: Configurer le matériel non stocké et les factures fournisseur en attente
description: Cet article explique comment activer les matériaux non stockés et les factures fournisseur en attente.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913755"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurer le matériel non stocké et les factures fournisseur en attente

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

## <a name="minimum-version-requirement"></a>Exigence minimale de version

L’utilisation de matériel non stocké et de factures fournisseur en attente pour les scénarios basés sur les ressources/produits non stockés Dynamics 365 Project Operations nécessite les versions suivantes :

Solutions Dynamics 365 Dataverse :

- Project Operations – 4.9.0.221 ou version ultérieure
- Solution d’orchestration d’application à double écriture - 2.2.2.23 ou version ultérieure

Dynamics 365 Finance :
- 10.0.18 (10.0.793.52) ou version ultérieure. Assurez-vous que votre environnement Finance est à jour et que toutes les mises à jour de qualité sont appliquées pour répondre aux exigences minimales de version.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Exécuter des mappages à double écriture pour le matériel non stocké et l’intégration des factures fournisseur

Cette section fournit des informations sur les mappages spécifiques requis pour le matériel non stocké et les factures fournisseur. Vérifiez que les cartes prérequises répertoriées dans l’article [Approvisionner un nouvel environnement](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) sont en cours d’exécution sur votre environnement.

1. Accédez à Lifecycle Services (LCS), accédez à votre projet LCS et accédez à la page **Détails de l’environnement**.
2. Dans la section **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**. Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.
3. Assurez-vous que les mappages suivants s’exécutent. Si ce n’est pas le cas, démarrez-les et assurez-vous d’inclure tous les mappages de table associés.

    - Produits distincts lancés par CDS (produits)
    - Fournisseurs v2 (msdyn_vendors)
    - Table Project Operations pour les estimations de matériel (msdyn_estimatelines)
    - Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoices)
    - Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoicelines)
    - Chiffres réels d’intégration Project Operations (msdyn_actuals). Assurez-vous que vous exécutez la version de mappage 1.0.0.14 ou ultérieure. Vous pouvez voir la version active du mappage dans la colonne **Version** de la page **Double écriture**. Vous pouvez activer une nouvelle version du mappage en sélectionnant **Version du mappage de table**, puis en enregistrant la version sélectionnée.

Si vous utilisez des données de démonstration standard, vous devrez peut-être également arrêter et redémarrer les mappages d’entités suivants avec la synchronisation initiale :
  - CDS jours de paiement V2 (msdyn_paymentdays)
  - Échéancier de paiement (msdyn_paymentschedules)
  - Conditions de paiement (msdyn_paymentterms)
  - Groupes de fournisseurs (msdyn_vendorgroups)
  - Unités (uom)

> [!NOTE]
> La synchronisation initiale des groupes et des unités de fournisseurs peut échouer pour quelques enregistrements du jeu de données de la démo existante. Vous pouvez ignorer les échecs car ils ne vous empêcheront pas d’utiliser les données de démonstration avec Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurer les conditions préalables dans Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Activer le flux de travail pour créer des comptes basés sur l’entité du fournisseur

La solution d’orchestration à double écriture fournit l’[intégration principale des fournisseurs ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Comme condition préalable à cette fonctionnalité, les données fournisseur doivent être créées dans l’entité **Comptes**. Activez un modèle de processus de flux de travail pour créer des fournisseurs dans la table **Comptes**, comme décrit dans [Basculer entre les conceptions des fournisseurs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Définir les produits à créer comme actifs

Le matériel non stocké doit être configuré comme **Produits lancés** dans Finance. La solution d’orchestration à double écriture fournit une solution prête à l’emploi [Intégration des produits lancés dans le catalogue des produits Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Par défaut, les produits de Finance sont synchronisés avec Dataverse à l’état de brouillon. Pour synchroniser le produit à un état actif afin qu’il puisse être directement utilisé dans les documents d’utilisation du matériel ou les factures fournisseur en attente, accédez à **Système** > **Administration** > **Administration système** > **Paramètres du système**, puis, sur l’onglet **Ventes**, définissez **Créer des produits à l’état actif** sur **Oui**.

## <a name="configure-prerequisites-in-finance"></a>Configurer les conditions préalables dans Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Activer la clé de fonction pour les factures fournisseur en attente

Procédez comme suit pour activer la fonctionnalité permettant d’ajouter des détails de projet sur les lignes de facture fournisseur en attente.

1. Dans Finance, accédez à l’espace de travail **Gestion des fonctionnalités**.
2. Dans la liste des fonctionnalités, recherchez la fonctionnalité **Activer les factures fournisseur en attente sur Project Operations pour les scénarios basés sur les ressources/produits non stockés** et sélectionnez **Activer**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Définir des groupes de catégories et des catégories de projet pour les éléments

Configurez au moins un groupe de catégories pour le type de transaction **Article** et au moins une catégorie de projet utilisant ce groupe. Pour plus d’informations, voir [Configurer les catégories de projets](../project-accounting/configure-project-categories.md#category-groups).

Passez en revue les profils de coût et de revenu du projet, et configurez les paramètres de validation dans la comptabilité pour les transactions d’article. Pour plus d’informations, consultez [Configurer la comptabilité des projets facturables](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurer un produit hors catalogue

Dans Project Operations, vous pouvez enregistrer les estimations et l’utilisation du matériel pour les produits du catalogue configurés dans le catalogue de produits lancé et pour les produits hors catalogue. L’utilisation de produits hors catalogue nécessite un seul produit lancé configuré dans Finance à cette fin. Procédez de la manière suivante pour configurer un produit hors catalogue. Répétez ces étapes dans chaque entité juridique qui utilise Project Operations pour les scénarios basés sur les ressources/produits non stockés.

1. Dans Finance, accédez à **Gestion des informations sur les produits** > **Produits** > **Produits lancés** et sélectionnez **Nouveau**.
2. Dans le champ **Type de produit**, sélectionnez **Article** et dans le champ **Sous-type de produit**, sélectionnez **Produit**.
3. Entrez le numéro de produit (WRITEIN) et le nom de produit (produit hors catalogue).
4. Sélectionnez le groupe de modèles d’article. Assurez-vous que le champ **Stratégie de stock Produit stocké** du groupe de modèles d’article que vous sélectionnez est défini sur **Faux**.
5. Sélectionnez des valeurs dans les champs **Groupe d’articles**, **Groupe de dimensions de stockage** et **Groupe de dimensions de suivi**. Utilisez la **Dimensions de stockage** pour **Site** uniquement et, dans le champ **Dimensions de suivi**, sélectionnez **Aucun**.
6. Sélectionnez des valeurs dans les champs **Unité de stock**, **Unité d’achat** et **Unité de vente**, puis enregistrez vos modifications.
7. Dans l’onglet **Planifier**, définissez les paramètres de commande par défaut et sur l’onglet **Stock**, définissez le site et l’entrepôt par défaut.
8. Accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets** et ouvrez **Project Operations sur Dynamics 365 Dataverse**. 
9. Sur l’onglet **Matériel**, dans le champ **Produit hors catalogue**, sélectionnez le produit que vous avez créé.
10. Dans votre environnement Dataverse, dans le plan de site, ouvrez l’entité **Produits** et recherchez l’enregistrement de produit hors catalogue. 
11. Ouvrez les détails de l’enregistrement et définissez l’état du produit sur **Mis hors service**. Cet état du produit empêche quiconque d’utiliser accidentellement cet enregistrement directement dans les document d’estimation et d’utilisation du matériel.

### <a name="set-up-a-procurement-integration-account"></a>Configurer un compte d’intégration d’approvisionnement

Le compte d’intégration d’approvisionnement est utilisé comme compte de compensation lors de la validation d’une facture fournisseur en attente avec des lignes attribuées à un projet.

Lorsque le système enregistre une facture fournisseur en attente, ce compte est utilisé pour le montant du coût du projet. Les détails de la facture fournisseur sont traités dans Dataverse et les chiffres réels d’un projet correspondant sont créés. Les informations des chiffres réels du projet sont ajoutées à la feuille intégration de Project Operations. Lorsque vous validez la feuille intégration, le montant est effacé du compte d’intégration d’approvisionnement et enregistré dans le coût du projet.

1. Pour configurer le compte d’intégration d’approvisionnement, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets** et ouvrez **Project Operations sur Dynamics 365 Dataverse**. 
2. Sélectionnez l’onglet **Matériel** et sélectionnez une valeur dans le champ **Compte d’intégration d’approvisionnement**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configurer les valeurs par défaut de la catégorie de projet pour un article

1. Dans Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets** et ouvrez **Project Operations sur Dynamics 365 Dataverse**. 
2. Dans l’onglet **Valeurs par défaut de la catégorie de projet**, dans le champ **Article** champ, sélectionnez une valeur. Cette catégorie de projet est utilisée pour les transactions de matériel si la catégorie de projet n’a pas été définie dans l’enregistrement des chiffres réels du projet.
