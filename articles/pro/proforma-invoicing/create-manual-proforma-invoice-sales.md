---
title: Créer une facture pro forma manuelle – Simplifié
description: Cette rubrique fournit des informations sur la création d’une facture pro forma manuelle dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274185"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Créer une facture pro forma manuelle – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, les factures pro forma peuvent être créées manuellement, si nécessaire. Vous pouvez créer manuellement une facture pro forma à partir de la page de liste **Contrats de projet** ou depuis la page de détails **Contrat de projet**.

##  <a name="project-contracts-list-page"></a>Page de liste Contrats du projet

Dans la page de liste **Contrats du projet**, sélectionnez un ou plusieurs contrats de projet et créez des factures pour tous les enregistrements sélectionnés.

Le système vérifie lequel des contrats de projet sélectionnés a un arriéré **Prêt à facturer** daté avant la date d’aujourd’hui. À partir de ces contrats, le système crée des projets de factures pro forma. Si un contrat de projet a plusieurs clients, il peut y avoir une facture créée par client et plusieurs factures par contrat de projet.

Toutes les factures de projet créées sont disponibles sur la page **Facture** dans la section **Facturation** de la zone **Ventes**.

## <a name="project-contract-details-page"></a>Page Détails du contrat de projet

Une facture pro forma peut également être créée à partir de la page de détails **Contrat de projet**. Le système vérifie si le contrat de projet dispose d’un backlog **Prêt pour la facturation** daté d’avant la date du jour. À partir de ces contrats, le système crée des factures pro forma provisoires en fonction du nombre de clients sur chaque ligne de contrat.

Lorsqu’une seule facture pro forma est créée, la page **Facture** s’ouvre. Si plusieurs factures ont été créées pour le contrat de projet concerné, la page de liste **Factures** s’ouvre pour afficher toutes les factures créées.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]