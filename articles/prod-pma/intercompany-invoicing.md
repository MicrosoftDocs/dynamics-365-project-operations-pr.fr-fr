---
title: Facturation intersociétés
description: Cet article offre des informations et des exemples sur la facturation intersociétés pour les projets.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075766"
---
# <a name="intercompany-invoicing"></a>Facturation intersociétés

[!include [banner](../includes/banner.md)]

Cet article offre des informations et des exemples sur la facturation intersociétés pour les projets.

Votre organisation peut avoir plusieurs divisions, filiales et autres entités juridiques qui se transfèrent des produits et des services pour des projets. L’entité juridique qui fournit le service ou le produit est appelée *entité juridique prêteuse* , et l’entité juridique qui reçoit le service ou le produit est appelée *entité juridique emprunteuse*. 

L’illustration suivante présente un scénario type où deux entités juridiques, SI FR (l’entité juridique emprunteuse) et SI USA (l’entité juridique prêteuse) partagent des ressources pour livrer un projet au client A. Dans le cadre de ce scénario, SI FR est engagée pour fournir le travail au client A. 

[![Exemple de facturation intersociétés](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

L’objectif consiste à rendre le contrôle des coûts, la reconnaissance des revenus, les taxes et le prix de transfert pour les transactions de projet intersociétés plus flexibles et plus puissants. De plus, les fonctionnalités suivantes sont fournies :

-   Créer des factures client pour un projet dans une entité juridique emprunteuse en utilisant des feuilles de temps, des dépenses et des factures fournisseur intersociétés dans une entité juridique prêteuse.
-   Soutenir les calculs fiscaux et les coûts indirects.
-   Différer la constatation du produit dans une entité juridique prêteuse et lorsqu’une entité juridique emprunteuse doit reconnaître le coût.
-   Provisionner le produit en cours dans l’entité juridique prêteuse.
-   Définir les prix du transfert qui peuvent être basés sur différents modèles de tarification. En voici quelques exemples :
    -   **Quantité**  : le montant que vous saisissez dans le champ **Tarification** est le coût réel par quantité ou unité.
    -   **Montant des frais**  : le prix/coût par transaction plus le montant des frais que vous saisissez dans le champ **Tarification**.
    -   **Pourcentage des frais**  : le prix du transfert correspond au prix/coût par transaction multiplié par le pourcentage de frais que vous saisissez dans le champ **Tarification**.
    -   **Pourcentage du prix de vente**  : le pourcentage du prix de vente qui est transféré à l’entité juridique prêteuse.
    -   **Montant inférieur au prix de vente**  : le montant que l’entité juridique emprunteuse retient des prix de vente avant transfert à l’entité juridique prêteuse.
    -   **Taux de contribution**  : le numéro que vous entrez dans le champ **Tarification** correspond au taux de contribution, exprimé en pourcentage du prix de vente.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemple 1 : Paramétrer la facturation intersociétés
Dans cet exemple, USSI désigne une entité juridique prêteuse, et ses ressources dressent des rapports de temps vis-à-vis de l’entité juridique emprunteuse, FRSI, qui détient le contrat avec le client final. Les heures et les dépenses déclarées par les employés d’USSI peuvent être incluses dans la facture de projet générée par FRSI. En outre, une troisième source de transactions peut provenir de l’entité juridique prêteuse (USSI dans cet exemple) lorsqu’elle fournit des services de fournisseurs partagés aux filiales (telles que FRSI), puis répercute ces coûts sur les projets au sein de ces filiales. Tous les documents de facturation et calculs de taxe correspondants sont effectués par Finance. 

Pour cet exemple, FRSI doit être un client de l’entité juridique USSI et USSI doit être un fournisseur de l’entité juridique FRSI. Vous pouvez ensuite configurer une relation intersociétés entre les deux entités juridiques. La procédure suivante montre comment configurer les paramètres afin que les deux entités juridiques puissent participer à la facturation intersociétés.

1. Configurez FRSI en tant que client dans l’entité juridique USSI et configurez USSI en tant que fournisseur dans l’entité juridique FRSI. Trois points d’entrée pour les étapes sont requis pour cette tâche.

   | Étape |                                                       Point d’entrée                                                        |                                                                                                                                                                                               Description                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Dans USSI, cliquez sur <strong>Comptabilité client</strong> &gt; <strong>Clients</strong> &gt; <strong>Tous les clients</strong>. |                                                                                                                                                                  Créez un enregistrement de client pour FRSI et sélectionnez le groupe de clients.                                                                                                                                                                  |
   |  G   |    Dans FRSI, cliquez sur <strong>Comptabilité fournisseur</strong> &gt; <strong>Fournisseurs</strong> &gt; <strong>Tous les fournisseurs</strong>.     |                                                                                                                                                                    Créez un enregistrement fournisseur pour USSI et sélectionnez le groupe de fournisseurs.                                                                                                                                                                    |
   |  C   |                                  Dans FRSI, ouvrez l’enregistrement de fournisseur que vous venez de créer.                                  | Dans le volet Actions, sous l’onglet <strong>Général</strong>, dans le groupe <strong>Configurer</strong>, cliquez sur <strong>Intersociétés</strong>. Sur la page <strong>Intersociétés</strong>, sous l’onglet <strong>Relation commerciale</strong>, définissez le curseur <strong>Actif</strong> sur <strong>Oui</strong>. Dans le champ <strong>Société du client</strong>, sélectionnez l’enregistrement de client que vous avez créé à l’étape A. |


2. Cliquez sur **Gestion de projets et comptabilité**&gt; **Configurer**&gt;**Paramètres de gestion de projets et de comptabilité** , puis cliquez sur l’onglet **Intersociétés**. La façon dont vous configurez les paramètres dépend du fait que vous soyez l’entité juridique emprunteuse ou l’entité juridique prêteuse.
   -   Si vous êtes l’entité juridique emprunteuse, sélectionnez la catégorie d’approvisionnement à utiliser pour faire correspondre les factures fournisseur, qui sont automatiquement générées.
   -   Si vous êtes l’entité juridique prêteuse, pour chaque entité emprunteuse, sélectionnez une catégorie de projet par défaut pour chaque type de transaction. Les catégories de projet sont utilisées pour la configuration fiscale lorsque la catégorie facturée dans les transactions intersociétés existe uniquement dans l’entité juridique emprunteuse. Vous pouvez choisir de provisionner un produit pour les transactions intersociétés. Cette provision est effectuée lorsque les transactions sont validées, puis contrepassée lorsque la facture intersociétés est validée.

3. Cliquez sur **Gestion de projets et comptabilité** &gt;**Configurer** &gt; **Prix** &gt; **Prix du transfert**.
4. Sélectionnez une devise, un type de transaction et un modèle de prix de transfert. La devise utilisée sur la facture est la devise configurée dans l’enregistrement de client pour l’entité juridique emprunteuse dans l’entité juridique prêteuse. La devise est utilisée pour faire correspondre les entrées dans le tableau des prix du transfert.
5. Cliquez sur **Comptabilité** &gt; **Paramétrage de la validation** &gt; **Comptabilité intersociétés** , et configurez une relation pour USSI et FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemple 2 : Créer et valider une feuille de temps intersociétés
L’USSI, l’entité juridique prêteuse, doit créer et valider la feuille de temps pour un projet de FRSI, l’entité juridique emprunteuse. Il existe deux points d’entrée pour les étapes requises pour cette tâche.

| Étape | Point d’entrée                                                                       | Description                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestion de projets et comptabilité** &gt; **Feuilles de temps** &gt; **Toutes les feuilles de temps** | Créez une feuille de temps. Sur une ligne de la feuille de temps, dans le champ **Entité juridique** , sélectionnez **FRSI**. Dans le champ **ID de projet** , sélectionnez le projet dans FRSI. Entrez les heures pour chaque jour de la semaine. |
| G    | Page **Feuille de temps**                                                                | Une fois le workflow exécuté, validez la feuille de temps et notez le numéro du coupon.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemple 3 : Créer et valider une facture fournisseur intersociétés
L’USSI, l’entité juridique prêteuse, doit créer et valider la facteur fournisseur intersociétés pour un projet de FRSI, l’entité juridique emprunteuse. Cette facture fournisseur représente la main-d’œuvre externalisée et les dépenses effectuées par les fournisseurs et payées par USSI. Il existe deux points d’entrée pour les étapes requises pour cette tâche.

| Étape | Point d’entrée                                                                                      | Description                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Comptabilité fournisseur** &gt; **Factures** &gt; **Factures fournisseur en cours** &gt; **Nouvelle facture fournisseur** | Créez une facture fournisseur et saisissez les services qui ont été achetés pour le compte du projet de FRSI.                                                                                                                                                                                  |
| G    | La page **Facture fournisseur**                                                                      | Saisissez les lignes qui représentent les services externalisés pour le compte de FRSI. Sur le raccourci **Détails de la ligne** , sur l’onglet **Projet** pour la ligne de facture, dans le champ **Société de projet** , saisissez **FRSI**. Saisissez le projet et les informations correspondantes. Puis validez la facture fournisseur. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemple 4 : Créer et valider la facture intersociétés
USSI, l’entité juridique prêteuse, doit créer et valider la facture intersociétés. Il existe deux points d’entrée pour les étapes requises pour cette tâche.

| Étape | Point d’entrée                                                                                             | Description                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestion de projets et comptabilité** &gt; **Factures de projet** &gt; **Facture client intersociétés**  | Cliquez sur **Nouveau** pour ouvrir la page **Créer une facture intersociétés**.                                                                                  |
| G    | **Gestion de projets et comptabilité** &gt; **Factures de projet** &gt; **Factures client intersociétés** | Sur la page **Créer une facture intersociétés** , saisissez l’entité juridique, spécifiez la transaction à inclure, puis cliquez sur **Rechercher**. |
| C    | **Gestion de projets et comptabilité** &gt; **Factures de projet** &gt; **Factures client intersociétés** | Sélectionnez les transactions à facturer ou cliquez sur **Tout sélectionner** pour facturer toutes les transactions de la liste, puis cliquez sur **OK**.                  |
| D    | La page **Facture intersociétés**                                                                       | La proposition de facture client intersociétés s’affiche.                                                                                             |
| E    | La page **Facture intersociétés**                                                                       | Cliquez sur **Valider**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemple 5 : Valider la facture fournisseur et facturer le client
Lorsque l’entité juridique prêteuse, USSI, enregistre la facture client intersociétés, une facture fournisseur en attente correspondante est créée dans l’entité juridique emprunteuse, FRSI. Une fois cette facture fournisseur validée, FRSI facture également le client du projet pour les heures saisies par USSI. Trois points d’entrée pour les étapes sont requis pour cette tâche.

| Étape | Point d’entrée                                                                                        | Description                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Comptabilité fournisseur** &gt; **Factures** &gt; **Factures fournisseur en cours**                            | Vérifiez la facture pour valider que les valeurs de feuille de temps sont incluses, puis validez la facture fournisseur.                  |
| G    | **Gestion de projets et comptabilité** &gt; **Factures de projet** &gt; **Propositions de facture du projet** | Créez une facture de projet pour le projet et vérifiez que les transactions d’heures qui ont été validées apparaissent.            |
| C    | La page **Facture projet**                                                                       | Sélectionnez la facture du projet, puis cliquez sur **Afficher les détails** pour vérifier le coût et le montant des ventes. Puis validez la facture. |


Pour plus d’informations, consultez [Configurer la facturation des projets intersociétés](tasks/configure-intercompany-project-invoicing.md).


