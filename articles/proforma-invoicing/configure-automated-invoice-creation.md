---
title: Configurer une création de facture automatisée
description: Cette rubrique fournit des informations sur la façon de configurer le système pour générer automatiquement des factures.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898123"
---
# <a name="configure-automated-invoice-creation"></a>Configurer une création de facture automatisée

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Effectuez les étapes suivantes pour configurer une exécution de facture automatisée dans Project Operations.

1. Accédez à **Paramètres** \> **Traitements par lots**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure le terme « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les options **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Sélectionnez **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, vous verrez trois workflows :

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis **Ajouter**.
6. Dans la boîte de dialogue suivante, sélectionnez **OK**. Un workflow **Veille** est suivi d'un workflow **Processus**.

    Vous pouvez également sélectionner **ProcessRunner** à l'étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d'un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée en fait les factures. Il traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée des factures pour ces lignes. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, la tâche recherche les dates d'exécution de factures des lignes de contrat. Si des lignes de contrat qui appartiennent à un contrat disposent de la même date d'exécution de factures, les transactions sont combinées en une seule facture avec deux lignes de facture. S'il n'existe pas de transaction pour créer des factures, la tâche ignore la création de facture.

Une fois que **ProcessRunner** a fini de s'exécuter, il appelle **ProcessRunCaller**, fournit l'heure de fin, et est fermé. **ProcessRunCaller** lance alors une minuterie qui s'exécute pendant 24 heures à partir de l'heure de fin spécifiée. À la fin de la minuterie, **ProcessRunCaller** est fermé.

La tâche de traitement par lots pour la création de factures est une tâche périodique. Si ce traitement par lots est exécuté de nombreuses fois, plusieurs instances de la tâche sont créées et entraînent des erreurs. Par conséquent, vous devez démarrer le traitement par lots une seule fois, et vous devez le redémarrer uniquement s'il cesse de s'exécuter.

> [!NOTE]
> La facturation par lots ne s'exécute que pour les lignes de contrat de projet qui sont configurées par des calendriers de facturation. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d'un calendrier de facturation basé sur la date. Il en va de même pour une ligne de contrat basée sur un projet.     
