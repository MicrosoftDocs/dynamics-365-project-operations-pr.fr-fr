---
title: Importer et gérer les transactions par carte de crédit
description: Cette rubrique explique comment importer et gérer les transactions par carte de crédit liées aux dépenses. Ces transactions peuvent être configurées de manière à être automatiquement importées selon un calendrier récurrent, ou elles peuvent être importées manuellement si nécessaire.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995848"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importer et gérer les transactions par carte de crédit

Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d’être automatiquement importées selon un calendrier récurrent. Les transactions peuvent également être importées manuellement, le cas échéant. Les transactions par carte de crédit sont importées via l’entité de données Transactions par carte de crédit.

Pour plus d’informations sur les entités de données, voir [Entités de données](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importer des transactions par carte de crédit

1. Sur la page **Transactions par carte de crédit**, sélectionnez **Importer des transactions**. Si vous ouvrez l’espace de travail Gestion des données pour la première fois, le système doit mettre à jour la liste des entités de données avant de pouvoir continuer.
2. Dans le champ **Nom**, saisissez une description unique pour la tâche d’importation.
3. Dans le champ **Format des données source**, sélectionnez le format du fichier contenant les transactions par carte de crédit à importer.
4. Cliquez sur **Charger**, puis recherchez et sélectionnez le fichier à importer.
5. Une fois le fichier téléchargé, validez le mappage du fichier de transaction par carte de crédit et les colonnes de l’entité de données Transactions par carte de crédit en sélectionnant le lien **Afficher la mise en correspondance** sur la vignette. S’il existe des erreurs de mappage ou si vous devez modifier le mappage, apportez les changements nécessaires à partir de l’onglet **Visualisation du mappage** ou **Détails du mappage**.
6. Pour automatiser l’importation des transactions par carte de crédit, cliquez sur **Créer une tâche de données répétitive**. Vous pouvez ensuite définir la périodicité correspondante, à savoir la fréquence d’importation des transactions par carte de crédit. Ensuite, cliquez sur **OK**.
7. Pour importer le fichier sélectionné maintenant, cliquez sur **Importer**.
8. Si des erreurs se produisent lors de l’importation, vous pouvez afficher le journal d’exécution ou les données de préparation pour voir les erreurs que vous devez corriger pour garantir la réussite de l’importation.

> [!NOTE]
> Si vous devez importer plusieurs formats de fichier, vous devez créer des travaux d’importation distincts pour chaque type de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Réaffecter les transactions par carte de crédit pour les employés licenciés

Lorsqu’un employé est licencié, son compte Services de domaine Active Directory (AD DS) est désactivé. Cependant, il peut y avoir des transactions par carte de crédit actives qui doivent encore être passées en charges et remboursées. À partir de la page **Transactions par carte de crédit**, vous pouvez réaffecter l’employé pour toute transaction par carte de crédit associée à l’employé qui a été licencié.

Sélectionnez une ou plusieurs transactions par carte de crédit, puis sélectionnez **Réaffecter les transactions**. Vous pouvez ensuite sélectionner un autre employé auquel affecter les transactions par carte de crédit. Une fois que les transactions par carte de crédit ont été réaffectées, elles peuvent être sélectionnées pour une note de frais et payées selon le processus habituel de remboursement des notes de frais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]