---
title: Importer et gérer les transactions par carte de crédit
description: Cette rubrique explique comment importer et gérer les transactions par carte de crédit liées aux dépenses. Ces transactions peuvent être configurées de manière à être automatiquement importées selon un calendrier récurrent, ou elles peuvent être importées manuellement si nécessaire.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960424"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importer et gérer les transactions par carte de crédit

Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d'être automatiquement importées selon un calendrier récurrent. Les transactions peuvent également être importées manuellement selon les besoins. Les transactions par carte de crédit sont importées via l'entité de données Transactions par carte de crédit.

Pour plus d'informations sur les entités de données, voir [Entités de données](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importer des transactions par carte de crédit

1. Sur la page **Transactions par carte de crédit**, sélectionnez **Importer des transactions**. Si vous ouvrez la gestion des données pour la première fois, le système doit mettre à jour la liste des entités de données avant de pouvoir continuer.
2. Dans le champ **Nom**, entrez une description unique de la tâche d’importation.
3. Dans le champ **Format des données source**, sélectionnez le format du fichier contenant les transactions par carte de crédit à importer.
4. Sélectionnez **Télécharger**, puis recherchez et sélectionnez le fichier à importer.
5. Une fois le fichier téléchargé, validez le mappage du fichier de transaction par carte de crédit et les colonnes de l’entité de données Transactions par carte de crédit en sélectionnant le lien **Afficher la mise en correspondance** sur la vignette. S’il y a des erreurs de mappage ou si vous devez modifier le mappage, effectuez les changements de mappage à partir de l’onglet **Visualisation cartographique** ou de l’onglet **Détails de la mise en correspondance**.
6. Pour automatiser les transactions par carte de crédit, sélectionnez **Créer une tâche de données répétitive**. Vous pouvez ensuite définir la récurrence qui définit la fréquence à laquelle les transactions par carte de crédit doivent être importées. Lorsque vous avez terminé, cliquez sur **OK**.
7. Pour importer le fichier sélectionné à présent, sélectionnez **Importer**.
8. Si des erreurs se produisent lors de l’importation, vous pouvez afficher le journal d’exécution ou les données de préparation pour voir les erreurs que vous devez corriger pour garantir la réussite de l’importation.

> [!NOTE]
> Si vous devez importer plusieurs formats de fichier, vous devez créer des travaux d’importation distincts pour chaque type de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Réaffecter les transactions par carte de crédit pour les employés licenciés

Lorsqu’un employé est licencié, son compte Services de domaine Active Directory (AD DS) est désactivé. Cependant, il peut y avoir des transactions par carte de crédit actives qui doivent encore être passées en charges et remboursées. À partir de la page **Transactions par carte de crédit**, vous pouvez réaffecter l’employé pour toute transaction par carte de crédit associée à l’employé qui a été licencié.

Sélectionnez une ou plusieurs transactions par carte de crédit, puis sélectionnez **Réaffecter les transactions**. Vous pouvez ensuite sélectionner un autre employé auquel affecter les transactions par carte de crédit. Une fois que les transactions par carte de crédit ont été réaffectées, elles peuvent être sélectionnées pour une note de frais et payées selon le processus habituel de remboursement des notes de frais.
