---
title: Vue d’ensemble du processus de facturation
description: Cette rubrique fournit une vue d'ensemble de la facturation dans Project Operations pour les scénarios basés sur les ressources/non stockés.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089235"
---
# <a name="invoicing-process-overview"></a>Vue d’ensemble du processus de facturation

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations pour les scénarios basés sur les ressources/non stockés offrent des capacités complètes adaptées aux besoins du chef de projet et du commis aux comptes clients/comptable de projet. Pour le processus de facturation, le chef de projet gère l'arriéré de facturation du projet et le commis à la Comptabilité client/comptable de projet crée un document de facture conforme et précis destiné au client.

![Diagramme de flux de facturation](./media/invoicing-flow.png)

La ligne de contrat de projet définit la méthode de facturation pour les transactions de projet associées. Lorsque le chef de projet approuve les transactions de temps et de dépenses, le système enregistre les transactions dans l'entité **Rapports réels du projet** et envoie les informations au module **Gestion de projet et comptabilité** dans Dynamics 365 Finance. Le comptable du projet examine et publie ensuite les enregistrements à l'aide du [Journal d'intégration Project Operations](../project-accounting/project-operations-integration-journal.md). Ce journal comprend des détails comptables importants pour les chiffres réels du projet, tels que la facturation, le groupe de taxes, le groupe de taxes d'article de facturation et les dimensions financières.

Le chef de projet peut consulter les transactions de vente non facturées à l'aide de la méthode de facturation du temps et des matières dans la [réplication de facturation du temps et du matériel](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) et facturation forfaitaire dans [Jalons de prix fixe](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ces vues vous permettent de filtrer et de sélectionner les transactions qui doivent être incluses dans le prochain cycle de facturation, puis de les marquer comme **Prêt à facturer**.

Vous pouvez [créer manuellement une facture pro forma](../proforma-invoicing/create-manual-proforma-invoice.md) ou utilisez un [processus périodique](../proforma-invoicing/configure-automated-invoice-creation.md). Le chef de projet peut [ajuster un brouillon de facture pro forma](../proforma-invoicing/manage-proforma-invoice.md) au besoin, puis confirmez-le.

La facture pro forma confirmée est envoyée au module **Gestion de projet et comptabilité** dans Finance. Le comptable du projet met en forme et met à jour la proposition de facture du projet, puis valide et imprime le document. Les factures de projet validées sont enregistrées dans la comptabilité, ainsi que dans les registres auxiliaires du client et du projet.
