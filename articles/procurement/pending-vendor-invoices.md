---
title: Acheter du matériel non stocké ou des catégories d’approvisionnement avec une facture fournisseur en attente
description: Cette rubrique explique comment enregistrer les factures fournisseur en attente.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612654"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Acheter du matériel non stocké ou des catégories d’approvisionnement avec une facture fournisseur en attente

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Lorsqu’une entreprise achète des matériaux non stockés ou des catégories d’approvisionnement pour un projet, les coûts peuvent être immédiatement enregistrés par rapport au projet. 

Par exemple, Contoso Robotics US réalise un projet de renouvellement de ses équipements et a besoin de licences logicielles. Ces licences sont obtenues auprès d’un fournisseur tiers.  À l’aide de Dynamics 365 Finance, le commis à la comptabilité fournisseur enregistre un document de facture fournisseur en attente et attribue les coûts de licence directement au projet de renouvellement de l’équipement. 

> [!IMPORTANT]
> Avant d’utiliser la fonctionnalité décrite dans cette rubrique, passez en revue et appliquez les configurations requises. Pour plus d’informations, voir [Activer les matériaux non stockés et les factures fournisseur en attente](configure-materials-nonstocked.md) et [Utiliser les catégories d’approvisionnement avec les bons de commande de projet et les factures fournisseur en attente](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publier une facture fournisseur en attente liée au projet 

Les factures fournisseur en attente peuvent être enregistrées sur la page **Factures fournisseur en attente** (**Comptabilité fournisseur** > **Factures** > **Factures fournisseur en attente**). Procédez comme suit pour valider une facture fournisseur en attente liée au projet :

1. Accédez à **Comptabilité fournisseur** > **Factures** et sélectionnez **Nouveau**. 
1. Dans le champ **Compte de facturation**, sélectionnez un fournisseur, puis, dans le champ **Numéro**, entrez l’identification de la facture du fournisseur.
1. Ajoutez une ligne à la facture fournisseur, puis, dans le champ **Numéro d’article**, sélectionnez l’article non stocké qui a été acheté auprès du fournisseur. Sinon, dans le champ **Catégorie d’approvisionnement**, sélectionnez la catégorie d’approvisionnement qui a été achetée auprès du fournisseur.   
1. Ajoutez la quantité achetée. Le système renseigne le prix unitaire, en fonction de la configuration du prix de l’article non stocké. 
1. Vérifiez le montant total et les autres détails requis sur la ligne.
1. Dans les détails de la ligne, sur l’onglet **Projet**, sélectionnez l’ID du projet dans lequel cet élément sera enregistré.
1. Facultatif : sélectionnez le numéro de l’activité et mettez à jour la catégorie de projet et la propriété de la ligne.
1. Valider la facture fournisseur en cours. Lorsque la facture est comptabilisée, le système enregistre les informations suivantes :
    
    - Le montant du solde fournisseur.
    - Le montant de la taxe de vente.
    - Le coût par rapport au projet est enregistré dans le compte d’intégration d’approvisionnement.
    - La transaction de coût réel du projet dans Dataverse.  La transaction est traitée davantage à l’aide de la [feuille intégration Project Operations](../project-accounting/project-operations-integration-journal.md). La validation de cette feuille déplace le montant du compte d’intégration d’approvisionnement vers le compte de coûts du projet. 
    - Les achats facturés au client du projet en utilisant la méthode de facturation des matériaux et du temps. De plus, les transactions commerciales non facturées sont créées pour les achats dans Dataverse. La liste des prix des produits dans Dataverse est utilisée pour les prix de vente et les montants des transactions commerciales non facturées.
