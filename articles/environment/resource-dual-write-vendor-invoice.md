---
title: Intégration des factures fournisseur
description: Cette rubrique fournit des informations sur l’intégration des factures fournisseur dans Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002259"
---
# <a name="vendor-invoice-integration"></a>Intégration des factures fournisseur

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les approvisionnements liés au projet dans Dynamics 365 Project Operations peuvent être enregistrés en accédant à **Comptabilité fournisseur** > **Factures** > **Factures fournisseur en attente** et en utilisant un document de facture fournisseur en attente. Pour plus d’informations, voir [Acheter du matériel non stocké à l’aide d’une facture fournisseur en attente](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Avant d’utiliser la fonctionnalité décrite dans cette rubrique, passez en revue et appliquez les configurations requises. Pour plus d’informations, voir [Activer le matériel non stocké et les factures fournisseur en attente](../procurement/configure-materials-nonstocked.md).

Dans Project Operations, les factures fournisseur liées au projet sont validées à l’aide de règles de validation spéciales :

- Le coût lié au projet (y compris la taxe non récupérable) n’est pas immédiatement imputé au compte de coût du projet dans la comptabilité. Au lieu de cela, le coût est imputé au **Compte d’intégration d’approvisionnement**. Ce compte est configuré dans **Gestion et comptabilité des projets** > **Configurer** > **Paramètres de gestion et comptabilité des projets** dans l’onglet **Project Operations sur Dynamics 365 Customer engagement**.
- La double écriture synchronise les détails des factures fournisseur avec Microsoft Dataverse à l’aide des mappages de table suivants :

     - **Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoices)**  : Ce mappage de table synchronise les informations d’en-tête des factures fournisseur. Seules les factures fournisseur avec au moins une ligne contenant un ID de projet sont synchronisées avec Dataverse.
     - **Entité d’exportation des lignes de factures fournisseur de projet d’intégration de Project Operations (msdyn_projectvendorinvoicelines)**  : Ce mappage de table synchronise les informations des lignes des factures fournisseur. Seules les lignes contenant un ID de projet sont synchronisées avec Dataverse.

     > [!NOTE]
     > Les détails des factures fournisseur dans Dataverse ne sont pas modifiables.

Le livre auxiliaire fiscal, le livre auxiliaire fournisseur et les autres écritures financières sont enregistrés, en fonction de la situation, dans Dynamics 365 Finance au moment de la validation de la facture fournisseur.

![Intégration des factures fournisseur](media/DW7VendorInvoice.png)

Lorsque les enregistrements sont écrits sur une entité **Facture fournisseur** dans Dataverse, un processus d’approbation automatisé des enregistrements commence. Si nécessaire, le statut du processus d’approbation automatisé peut être révisé dans Dataverse en accédant à **Réglages avancés** > **Système** > **Tâches système**. Une fois l’approbation terminée, le système crée les enregistrements de classe de transaction de matériel dans l’entité **Chiffres réels**.

Les chiffres réels liés au matériel sont ensuite traités à l’aide du mappage de table à double écriture **Chiffres réels d’intégration Project Operations (msdyn_actuals)**. Pour plus d’informations, voir [Estimations de projet et chiffres réels](resource-dual-write-estimates-actuals.md).

Le processus périodique **Importer depuis la table intermédiaire** crée des lignes de journal d’intégration Project Operations liées aux factures fournisseur. Le compte de contrepartie est par défaut le compte d’intégration d’approvisionnement. Lorsque le journal d’intégration est validé, le solde de compte est effacé pour la transaction de facture fournisseur et le montant de la ligne est transféré vers le compte de coûts du projet. Des transactions de livre auxiliaire de projet sont également créées à des fins de facturation en aval et de comptabilisation des produits.
