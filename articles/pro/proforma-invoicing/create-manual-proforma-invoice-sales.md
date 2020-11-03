---
title: Création d’une facture pro forma manuelle
description: Cette rubrique fournit des informations sur la création d'une facture pro forma manuelle dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075969"
---
# <a name="creating-a-manual-proforma-invoice"></a>Création d’une facture pro forma manuelle

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, les factures pro forma peuvent être créées manuellement si nécessaire. Vous pouvez créer manuellement une facture pro forma à partir de la page de liste **Contrats de projet** ou depuis la page de détails **Contrat de projet**.

##  <a name="project-contracts-list-page"></a>Page de liste Contrats du projet

Dans la page de liste **Contrats du projet** , sélectionnez un ou plusieurs contrats de projet et créez des factures pour tous les enregistrements sélectionnés.

Le système vérifie lequel des contrats de projet sélectionnés a un arriéré **Prêt à facturer** daté avant la date d'aujourd'hui. À partir de ces contrats, le système crée des projets de factures pro forma. Si un contrat de projet a plusieurs clients, il peut y avoir une facture créée par client et plusieurs factures par contrat de projet.

Toutes les factures de projet créées sont disponibles sur la page **Facture** dans la section **Facturation** de la zone **Ventes**.

## <a name="project-contract-details-page"></a>Page Détails du contrat de projet

Une facture pro forma peut également être créée à partir de la page de détails **Contrat de projet** , qui crée la facture pour ce contrat de projet spécifique. Le système vérifie que le contrat de projet a un arriéré **Prêt à facturer** qui est daté avant la date d'aujourd'hui. À partir de ces contrats, le système crée des projets de factures pro forma en fonction du nombre de clients sur chaque ligne de contrat.

Lorsqu'une seule facture pro forma est créée, la page **Facture** s'ouvre. S'il y a plusieurs factures créées pour ce contrat de projet, la page de liste **Factures** s'ouvre pour afficher toutes les factures créées.
