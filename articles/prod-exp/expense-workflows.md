---
title: Configurer des workflows pour la gestion des dépenses
description: Vous pouvez configurer un processus de workflow pour examiner et approuver les documents de voyage et de dépenses.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005113"
---
# <a name="set-up-expense-management-workflows"></a>Configurer des workflows pour la gestion des dépenses

Vous pouvez configurer un processus de flux de travail utilisé pour examiner et approuver les documents de déplacement et de dépenses. Les documents pour lesquels les workflows peuvent être définis incluent les notes de frais, les demandes de déplacement et les demandes d’avance de fonds.

Un flux de travail représente un processus métier. Il définit le transfert d’un document dans le système et indique qui doit traiter une tâche ou approuver un document. Il y a plusieurs avantages à utiliser le système de workflow dans votre organisation :

-   **Processus cohérents** — Vous pouvez définir le processus d’approbation pour des documents spécifiques, tels que des demandes d’achat ou des états de dépenses. Le système de workflow permet de s’assurer que les documents sont traités et approuvés de manière cohérente et efficace.

-   Visibilité de processus — Vous pouvez suivre le statut, l’historique et les mesures de performance d’une instance de workflow spécifique. Cette approche vous aide à déterminer si des modifications doivent être apportées au workflow pour améliorer l’efficacité.

-   Liste de travail centralisée — Les utilisateurs peuvent afficher une liste de travail centralisée pour afficher les tâches de workflow et les approbations qui leur sont affectées. 

**Types de workflows qu’il est possible de créer**

Le tableau ci-dessous répertorie les types de workflows que vous pouvez créer dans **Dépense**.


|              <strong>Type</strong>              |                   <strong>Utilisez ce type pour ce qui suit</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Rapport de dépenses</strong>         |            Créez des workflows d’approbation pour les notes de frais.             |
|  <strong>Validation automatique des notes de frais</strong>   |        Créez des workflows de validation automatique pour les notes de frais.        |
|       <strong>Article de ligne de dépense</strong>        |     Créez des workflows d’approbation pour les articles de ligne sur les notes de frais.      |
| <strong>Validation automatique des lignes de dépense</strong> | Créez des workflows de validation automatique pour les articles de ligne sur les notes de frais. |
|       <strong>Demande de trajet</strong>       |          Créez des workflows d’approbation pour les demandes de voyage.           |
|      <strong>Demande d’avance de disponibilités</strong>      |         Créez des workflows d’approbation pour les demandes d’avance de fonds.          |
|        <strong>Recouvrement fiscal de la TVA</strong>        | Créez des workflows d’approbation pour la récupération de la taxe sur la valeur ajoutée (TVA).  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]