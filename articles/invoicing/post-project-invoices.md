---
title: Vue d’ensemble du processus de facturation
description: Cette rubrique fournit une vue d’ensemble de la facturation dans Project Operations pour les scénarios basés sur les ressources/non stockés.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369013"
---
# <a name="invoicing-process-overview"></a>Vue d’ensemble du processus de facturation

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations pour les scénarios basés sur les ressources/non stockés offrent des capacités complètes adaptées aux besoins du chef de projet et du commis aux comptes clients/comptable de projet. Pour le processus de facturation, le chef de projet gère l’arriéré de facturation du projet et le commis à la Comptabilité client/comptable de projet crée un document de facture conforme et précis destiné au client.

![Diagramme de flux de facturation](./media/invoicing-flow.png)

La ligne de contrat de projet définit la méthode de facturation pour les transactions de projet associées. Lorsque le chef de projet approuve les transactions de temps et de dépenses, le système enregistre les transactions dans l’entité **Rapports réels du projet** et envoie les informations au module **Gestion de projet et comptabilité** dans Dynamics 365 Finance. Le comptable du projet examine et publie ensuite les enregistrements à l’aide du [Journal d’intégration Project Operations](../project-accounting/project-operations-integration-journal.md). Ce journal comprend des détails comptables importants pour les chiffres réels du projet, tels que la facturation, le groupe de taxes, le groupe de taxes d’article de facturation et les dimensions financières.

Le chef de projet peut consulter les transactions de vente non facturées à l’aide de la méthode de facturation du temps et des matières dans la [réplication de facturation du temps et du matériel](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) et facturation forfaitaire dans [Jalons de prix fixe](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ces vues vous permettent de filtrer et sélectionner les transactions à intégrer au prochain cycle de facturation, puis de leur affecter le statut **Prêt pour la facturation**.

Vous pouvez [créer manuellement une facture pro forma](../proforma-invoicing/create-manual-proforma-invoice.md) ou utilisez un [processus périodique](../proforma-invoicing/configure-automated-invoice-creation.md). Le chef de projet peut [ajuster un brouillon de facture pro forma](../proforma-invoicing/manage-proforma-invoice.md) au besoin, puis confirmez-le.

La facture pro forma confirmée est envoyée au module **Gestion de projet et comptabilité** dans Finance. Le comptable du projet met en forme et met à jour la proposition de facture du projet, puis valide et imprime le document. Les factures de projet validées sont enregistrées dans la comptabilité, ainsi que dans les comptabilités auxiliaires client et de projet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]