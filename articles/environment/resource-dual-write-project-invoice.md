---
title: Intégration des factures de projet
description: Cet article fournit des informations sur l’intégration en double écriture Project Operations de la facturation client.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912099"
---
# <a name="project-invoice-integration"></a>Intégration des factures de projet

Cet article fournit des informations sur l’intégration en double écriture Project Operations de la facturation client.

Dans Project Operations, le gestionnaire de projet gère la réplication de facturation pour les projets et crée une facture pro forma pour le client dans Microsoft Dataverse. À partir de cette facture pro forma, le commis à la comptabilité clients ou le comptable de projet crée une facture destinée au client. L’intégration en double écriture garantit que les détails de la facture pro forma sont synchronisés avec les applications de finances et d’opérations. Une fois la facture adressée au client validée, le système met à jour les données réelles et pertinentes du projet dans Dataverse avec les détails comptables. Le graphique suivant fournit un aperçu conceptuel de haut niveau de cette intégration.

   ![Intégration des factures de projet.](./media/DW5Invoicing.png)

Une fois que le chef de projet a confirmé la facture proforma dans Dataverse, les informations d’en-tête de facture pro forma sont synchronisées avec les applications de finances et d’opérations via le mappage de table en double écriture, **Proposition de facture de projet V2 (factures)**. Il s’agit d’une intégration à sens unique à partir de Dataverse vers les applications de finances et d’opérations. La création ou la suppression de propositions de facture de projet directement dans les applications de finances et d’opérations n’est pas prise en charge.

La confirmation d’une facture dans Dataverse déclenche également la logique métier pour créer des enregistrements liés à la facturation dans l’entité **Chiffres réels**. Ces enregistrements sont synchronisés avec Finance and Operations à l’aide du mappage de table en double écriture **Chiffres réels d’intégration de Project Operations (msdyn\_actuals).** Pour plus d’informations, voir [Estimations de projet et chiffres réels](resource-dual-write-estimates-actuals.md). 

Les lignes de propositions de facture de projet sont créées par le processus périodique, **Importer depuis la table intermédiaire**. Ce processus est basé sur les chiffres réels des ventes facturées dans la table **intermédiaire des chiffres réels**. Pour plus d’informations, voir [Gérer des propositions de facture pour un projet](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
