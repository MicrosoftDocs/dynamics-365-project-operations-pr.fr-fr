---
title: Intégration des factures de projet
description: Cette rubrique fournit des informations sur l’intégration à double écriture Project Operations pour la facturation des clients.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955743"
---
# <a name="project-invoice-integration"></a>Intégration des factures de projet

Cette rubrique fournit des informations sur l’intégration à double écriture Project Operations pour la facturation des clients.

Dans Project Operations, le gestionnaire de projet gère la réplication de facturation pour les projets et crée une facture pro forma pour le client dans Microsoft Dataverse. À partir de cette facture pro forma, le commis à la comptabilité clients ou le comptable de projet crée une facture destinée au client. L’intégration en double écriture garantit que les détails de la facture pro forma sont synchronisés avec les applications Finance and Operations. Une fois la facture adressée au client validée, le système met à jour les données réelles et pertinentes du projet dans Dataverse avec les détails comptables. Le graphique suivant fournit un aperçu conceptuel de haut niveau de cette intégration.

   ![Intégration des factures de projet](./media/DW5Invoicing.png)

Une fois que le gestionnaire de projet confirme la facture pro forma dans Dataverse, les informations d’en-tête de la facture pro forma sont synchronisées avec les applications Finance and Operations à l’aide du mappage de table à double écriture, **Propositions de facture de projet V2 (factures)**. Il s’agit d’une intégration unidirectionnelle de Dataverse vers les applications Finance and Operations. La création ou la suppression des propositions de facture de projet directement dans les applications Finance and Operations n’est pas prise en charge.

La confirmation d’une facture dans Dataverse déclenche également la logique métier pour créer des enregistrements liés à la facturation dans l’entité **Chiffres réels**. Ces enregistrements sont synchronisés avec les applications Finance and Operations à l’aide du mappage de table à double écriture, **Chiffres réels d’intégration de Project Operations (msdyn\_actuals)**. Pour plus d’informations, voir [Estimations de projet et chiffres réels](resource-dual-write-estimates-actuals.md). 

Les lignes de propositions de facture de projet sont créées par le processus périodique, **Importer depuis la table intermédiaire**. Ce processus est basé sur les chiffres réels des ventes facturées dans la table **intermédiaire des chiffres réels**. Pour plus d’informations, voir [Gérer des propositions de facture pour un projet](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
