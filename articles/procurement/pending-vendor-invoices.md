---
title: Acheter du matériel non stocké à l’aide d’une facture fournisseur en attente
description: Cette rubrique explique comment enregistrer les factures fournisseur en attente.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547286"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Acheter du matériel non stocké à l’aide d’une facture fournisseur en attente

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Lorsqu’une entreprise achète du matériel non stocké pour un projet, les coûts peuvent être immédiatement comptabilisés dans le projet. 

Par exemple, Contoso Robotics US réalise un projet de renouvellement de ses équipements et a besoin de licences logicielles. Ces licences sont obtenues auprès d’un fournisseur tiers.  À l’aide de Dynamics 365 Finance, le commis à la comptabilité fournisseur enregistre une facture fournisseur en attente et attribue les coûts de licence directement au projet de renouvellement de l’équipement. 

> [!IMPORTANT]
> Avant d’utiliser la fonctionnalité décrite dans cette rubrique, passez en revue et appliquez les configurations requises. Pour plus d’informations, consultez [Activer le matériel non stocké et les factures fournisseur en attente](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publier une facture fournisseur en attente liée au projet 

Les factures fournisseur en attente peuvent être enregistrées sur la page **Factures fournisseur en attente** (**Comptabilité fournisseur** > **Factures** > **Factures fournisseur en attente**). Procédez comme suit pour valider une facture fournisseur en attente liée au projet :

1. Accédez à **Comptabilité fournisseur** > **Factures** et sélectionnez **Nouveau**. 
2. Dans le champ **Compte de facturation**, sélectionnez un fournisseur et dans le champ **Nombre**, saisissez l’identification de la facture fournisseur.
3. Ajoutez une ligne à la facture fournisseur et dans le champ **Numéro d’article**, sélectionnez l’article non stocké acheté auprès du fournisseur. 

    > [!NOTE]
    > Les lignes de facture fournisseur basées sur une catégorie d’approvisionnement ne peuvent pas être comptabilisées dans le projet. 
    
5. Ajoutez la quantité achetée. Le système renseignera le prix unitaire en fonction de la configuration du prix de l’article non stocké. 
6. Vérifiez le montant total et les autres détails requis sur la ligne.
7. Sur les détails de la ligne, sur l’onglet **Projet**, sélectionnez l’ID du projet dans lequel cet élément sera enregistré.
8. Si vous le souhaitez, sélectionnez le numéro d’activité et mettez à jour la catégorie de projet et la propriété de ligne.
9. Validez la facture fournisseur en attente. Lorsque la facture est validée, le système enregistre :
    
    - Le montant du solde fournisseur.
    - Le montant de la taxe de vente.
    - Le coût par rapport au projet est enregistré dans le compte d’intégration d’approvisionnement.
    - La transaction de coût réel du projet dans Dataverse.  La transaction est traitée davantage à l’aide de la [feuille intégration Project Operations](../project-accounting/project-operations-integration-journal.md). La validation de cette feuille déplace le montant du compte d’intégration d’approvisionnement vers le compte de coûts du projet. 
    - Les achats facturés au client du projet en utilisant la méthode de facturation des matériaux et du temps. De plus, les transactions commerciales non facturées sont créées pour les achats dans Dataverse. La liste des prix des produits dans Dataverse est utilisée pour les prix de vente et les montants des transactions commerciales non facturées.