---
title: Configurer la facturation intersociétés
description: Cette rubrique fournit des informations et des exemples sur la configuration de la facturation intersociétés pour les projets.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595466"
---
# <a name="configure-intercompany-invoicing"></a>Configurer la facturation intersociétés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Effectuez les étapes suivantes pour configurer la facturation intersociétés pour les projets dans Dynamics 365 Project Operations. Les transactions intersociétés sont des transactions de temps et de dépenses d'un contrat de projet qui appartiennent à une société ou une unité d'organisation, tandis que les ressources du contrat de projet font partie d'une société ou d'une unité d'organisation différente.

## <a name="example-configure-intercompany-invoicing"></a>Exemple : Configurer la facturation intersociétés

Dans l'exemple suivant, Contoso Robotics USA (USPM) est l'entité juridique emprunteuse et Contoso Robotics UK (GBPM) est l'entité juridique prêteuse. 

1. **Configurer la comptabilité intersociétés entre des entités juridiques**. Chaque paire d'entités juridiques emprunteuses et prêteuses doit être configurée dans la page Comptabilité [Comptabilité intersociétés](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Dans Dynamics 365 Finance, accédez à **Comptabilité** > **Paramétrage de la validation** > **Comptabilité intersociétés**. Créez un enregistrement contenant les informations suivantes :

        - **Société d’origine** = **GBPM**
        - **Société de destination** = **USPM**

2. **Configurez la relation commerciale entre des entités juridiques**. L'enregistrement client représentant l'entité juridique emprunteuse doit être créé dans l'entité juridique prêteuse. L'enregistrement fournisseur représentant l'entité juridique prêteuse doit être créé dans l'entité juridique emprunteuse.

     1. Dans Finance, sélectionnez l'entité juridique **GBPM**.
     2. Accédez à **Comptabilité client** > **Client** > **Tous les clients**. Créez un nouvel enregistrement pour l'entité juridiques, **USPM**.
     3. Développez **Nom**, filtrez les enregistrements par **Type** et sélectionnez **Entités juridiques**. 
     4. Recherchez et sélectionnez l'enregistrement client pour **Contoso Robotics USA (USPM)**.
     5. Cliquez sur **Utiliser une correspondance**. 
     6. Sélectionnez le groupe de clients, puis enregistrez l'enregistrement.
     7. Sélectionnez l’entité juridique **USPM**.
     8. Accédez à **Comptabilité fournisseur** > **Fournisseurs** > **Tous les fournisseurs**. Créez un nouvel enregistrement pour l'entité juridique, **GBPM**.
     9. Développez **Nom**, filtrez les enregistrements par **Type** et sélectionnez **Entités juridiques**. 
     10. Recherchez et sélectionnez l'enregistrement client pour **Contoso Robotics UK (GBPM)**.
     11. Sélectionnez **Utiliser une correspondance**, sélectionnez le groupe de fournisseurs, puis enregistrez l'enregistrement.
     12. Dans l'enregistrement du fournisseur, sélectionnez **Général** > **Installer** > **Intersociétés**.
     13. Sur l'onglet **Relation commerciale**, définissez **Actif** sur **Oui**.
     14. Sélectionnez la société du fournisseur **GBPM** et dans **Mon enregistrement de compte**, sélectionnez l'enregistrement client que vous avez créé plus tôt dans la procédure.

3. **Configurez les paramètres intersociétés dans la gestion de projet et les paramètres de comptabilité**. 

    1. Sélectionnez l'entité juridique **USPM** et accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets**.
    2. Sur l'onglet **Intersociétés**, sélectionnez la catégorie d'approvisionnement correspondant aux factures fournisseurs générées automatiquement.
    3. Dans **Catégorie par défaut**, sélectionnez **Ressources intersociétés**.
    4. Sélectionnez l'entité juridique **GBPM** et accédez à **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets**.
    5. Sur l'onglet **Intersociétés**, sélectionnez une catégorie de projet par défaut pour chaque type de transaction. Les catégories de projet sont utilisées pour la configuration fiscale lorsque la catégorie facturée dans les transactions intersociétés existe uniquement dans l’entité juridique emprunteuse. Vous pouvez choisir de provisionner un produit pour les transactions intersociétés. Une régularisation a lieu lorsque les transactions sont validées via le journal d’intégration de Project Operations dans l'entité juridique prêteuse. Le journal est inversé lorsque la facture intersociétés est validée.
    6. Dans le groupe **Lors du prêt de ressources**, sélectionnez **...** > **Nouveau**. 
    7. Dans la grille, sélectionnez les informations suivantes :

          - **Entité juridique emprunteuse** = **GBPM**
          - **Régulariser revenus** = **Oui**
          - **Catégorie de feuille de temps par défaut** = **Par défaut - Heure**
          - **Catégorie de dépense par défaut** = **Défaut - dépense**

4. **Définissez les comptes de coûts et de revenus intersociétés dans le paramétrage de la validation dans la comptabilité**. Le compte de revenus intersociétés est crédité lorsque la facture client intersociétés est validée dans l'entité juridique prêteuse. Le compte de coûts intersociétés est débité lorsque la facture fournisseur en attente correspondante est validée dans l'entité juridique emprunteuse. Ces comptes sont configurés dans les entités juridiques correspondantes. 
      
     1. Dans Finance, sélectionnez l'entité juridique emprunteuse **USPM**. 
     2. Accédezr à **Gestion et comptabilité des projets** > **Configurer** > **Validation** > **Paramétrage de la validation dans la comptabilité**. 
     3. Sur l'onglet **Comptes de coûts**, dans **Type de compte général**, sélectionnez **Coût intersociétés**. Créez un nouvel enregistrement contenant les informations suivantes :
      
        - **Entité juridique prêteuse** = **GBPM**
        - **Compte principal** = Sélectionnez le compte principal pour le coût intersociétés
        
     4. Sélectionnez l’entité juridique prêteuse **GBPM**. 
     5. Accédezr à **Gestion et comptabilité des projets** > **Configurer** > **Validation** > **Paramétrage de la validation dans la comptabilité**. 
     6. Sur l'onglet **Comptes de revenus**, dans **Type de compte général**, sélectionnez **Revenu intersociétés**. Créez un nouvel enregistrement contenant les informations suivantes :

        - **Entité juridique emprunteuse** = **USPM**
        - **Compte principal** = Sélectionnez le compte principal pour le revenu intersociétés 

5. **Configurez la tarification de transfert pour la main-d'œuvre**. La tarification de transfert intersociétés est configurée dans Project Operations sur Dataverse. Configurez les [taux de coûts de la main-d’œuvre](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) et les [taux de facturation de la main-d’œuvre](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) pour la facturation intersociétés. La tarification de transfert n'est pas prise en charge pour les transactions de dépenses intersociétés. Le prix de vente unitaire inter-organisationnel sera toujours fixé à la même valeur que le prix de revient unitaire de ressourcement.

      Le coût des ressources de développeur dans Contoso Robotics UK est de 88 GBP par heure. Contoso Robotics UK facturera Contoso Robotics USA 120 USD pour chaque heure de travail de cette ressource sur des projets américains. Contoso Robotics USA facturera le client Adventure Works 200 USD pour le travail effectué par la ressource développeur de Contoso Robotics UK.

      1. Dans Project Operations sur Dataverse, accédez à **Vente** > **Listes de prix**. Créez une nouvelle liste de prix de revient appelée **Tarifs de Contoso Robotics UK.** 
      2. Dans la liste des prix de revient, créez un enregistrement avec les informations suivantes :
         - **Rôle** = **Développeur**
         - **Coût** = **88 GBP**
      3. Accédez à **Paramètres** > **Unités d'organisation** et joignez cette liste de prix de revient à l'unité d’organisation **Contoso Robotics UK**.
      4. Accédez à **Ventes** > **Listes de prix**. Créez une liste de prix de revient appelée **Tarifs de Contoso Robotics USA**. 
      5. Dans la liste des prix de revient, créez un enregistrement avec les informations suivantes :
          - **Rôle** = **Développeur**
          - **Société d’allocation de ressources** = **Contoso Robotics UK**
          - **Coût** = **120 USD**
      6. Accédez à **Paramètres** > **Unités d'organisation** et joignez cette liste de prix de revient **Tarifs de Contoso Robotics USA** à l'unité d’organisation **Contoso Robotics USA**.
      7. Accédez à **Ventes** > **Listes de prix**. Créez une liste de prix de vente appelée **Taux de facturation Adventure Works**. 
      8. Dans la liste des prix de vente, créez un enregistrement avec les informations suivantes :
          - **Rôle** = **Développeur**
          - **Société d’allocation de ressources** = **Contoso Robotics UK**
          - **Taux de facturation** = **200 USD**
      9. Accédez à **Ventes** > **Contrats de projet** et joignez la liste de prix **Taux de facturation Adventure Works** à la liste de prix du projet Adventure Works du contrat de projet.
