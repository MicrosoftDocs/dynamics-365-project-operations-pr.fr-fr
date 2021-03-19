---
title: Configurer l’intégration des cartes de crédit
description: Cette rubrique explique comment importer et gérer les transactions par carte de crédit liées aux dépenses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276165"
---
# <a name="set-up-credit-card-integration"></a>Configurer l’intégration des cartes de crédit

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d’être automatiquement importées selon un calendrier récurrent. Les transactions peuvent également être importées manuellement selon les besoins. Les transactions par carte de crédit sont importées via l’entité de données Transactions par carte de crédit.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]