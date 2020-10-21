---
title: Configurer des workflows pour la gestion des dépenses
description: Vous pouvez configurer un processus de flux de travail utilisé pour examiner et approuver les documents de déplacement et de dépenses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896548"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurer des workflows pour la gestion des dépenses

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez configurer un processus de workflow pour examiner et approuver les documents de voyage et de dépenses. Vous pouvez définir des workflows pour les notes de frais, les demandes de déplacement et les demandes d'avance de fonds.

Un workflow représente un processus métier et définit la manière dont un document circule dans le système. Le workflow indique également qui doit terminer une tâche ou approuver un document. Il y a plusieurs avantages à utiliser le système de workflow dans votre organisation :

- **Processus cohérents** : Vous pouvez définir le processus d'approbation pour des documents spécifiques, tels que les demandes d'achat et les notes de frais. Le système de workflow permet de garantir que les documents sont traités et approuvés de manière cohérente et efficace.
- **Visibilité des processus** : Vous pouvez suivre le statut, l'historique et les indicateurs de performance d'une instance de workflow spécifique. Cette approche vous aide à déterminer si des modifications doivent être apportées au workflow pour améliorer l'efficacité.
- **Liste de travail centralisée** : Les utilisateurs peuvent afficher une liste de travail centralisée pour afficher les tâches de workflow et les approbations qui leur sont affectées. 

## <a name="workflow-types"></a>Types de workflow

Le tableau ci-dessous répertorie les types de workflows que vous pouvez créer dans **Gestion des dépenses**.


|              <strong>Type</strong>              |                   <strong>Utilisez ce type pour ce qui suit</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Approbation automatique des notes de frais</strong> |            Créez des workflows d'approbation pour les notes de frais.             |
|  <strong>Validation automatique des notes de frais</strong>   |        Créez des workflows de validation automatique pour les notes de frais.        |
|       <strong>Article de ligne de dépense</strong>        |     Créez des workflows d'approbation pour les articles de ligne sur les notes de frais.      |
| <strong>Validation automatique des lignes de dépense</strong> | Créez des workflows de validation automatique pour les articles de ligne sur les notes de frais. |
|       <strong>Demande de trajet</strong>       |          Créez des workflows d'approbation pour les demandes de voyage.           |
|      <strong>Demande d'avance de disponibilités</strong>      |         Créez des workflows d'approbation pour les demandes d'avance de fonds.          |
|        <strong>Recouvrement fiscal de la TVA</strong>        | Créez des workflows d'approbation pour la récupération de la taxe sur la valeur ajoutée (TVA).  |
