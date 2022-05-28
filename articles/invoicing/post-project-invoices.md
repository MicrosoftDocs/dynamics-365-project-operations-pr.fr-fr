---
title: Vue d’ensemble du processus de facturation
description: Cette rubrique fournit une vue d’ensemble de la facturation dans Project Operations pour les scénarios basés sur les ressources/non stockés.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582707"
---
# <a name="invoicing-process-overview"></a>Vue d’ensemble du processus de facturation

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations pour les scénarios basés sur les ressources/non stockés offrent des capacités complètes adaptées aux besoins du chef de projet et du commis aux comptes clients/comptable de projet. Pour le processus de facturation, le chef de projet gère l’arriéré de facturation du projet et le commis à la Comptabilité client/comptable de projet crée un document de facture conforme et précis destiné au client.

![Diagramme du flux de facturation.](./media/invoicing-flow.png)

La ligne de contrat de projet définit le mode de facturation pour les transactions de projet associées. Lorsque le chef de projet approuve les transactions de temps et de dépenses, le système les enregistre dans l’entité **Chiffres réels du projet**, puis transmet les informations au module **Gestion et comptabilité de projet** de Dynamics 365 Finance. Le comptable du projet examine et publie ensuite les enregistrements à l’aide du [Journal d’intégration Project Operations](../project-accounting/project-operations-integration-journal.md). Ce journal comprend des détails comptables importants pour les chiffres réels du projet, tels que la facturation, le groupe de taxes, le groupe de taxes d’article de facturation et les dimensions financières.

Le chef de projet peut consulter les transactions de vente non facturées à l’aide de la méthode de facturation du temps et des matières dans la [réplication de facturation du temps et du matériel](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) et facturation forfaitaire dans [Jalons de prix fixe](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ces vues vous permettent de filtrer et sélectionner les transactions à intégrer au prochain cycle de facturation, puis de leur affecter le statut **Prêt pour la facturation**.

Vous pouvez [créer manuellement une facture pro forma](../proforma-invoicing/create-manual-proforma-invoice.md) ou utilisez un [processus périodique](../proforma-invoicing/configure-automated-invoice-creation.md). Le chef de projet peut [ajuster un brouillon de facture pro forma](../proforma-invoicing/manage-proforma-invoice.md) au besoin, puis confirmez-le.

La facture pro forma confirmée est envoyée au module **Gestion de projet et comptabilité** dans Finance. Le comptable du projet met en forme et met à jour la proposition de facture du projet, puis valide et imprime le document. Les factures de projet validées sont enregistrées dans la comptabilité, ainsi que dans les comptabilités auxiliaires client et de projet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]