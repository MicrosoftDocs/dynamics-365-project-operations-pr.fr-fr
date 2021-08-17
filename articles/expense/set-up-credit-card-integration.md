---
title: Configurer l’intégration des cartes de crédit
description: Cette rubrique explique comment utiliser les transactions par carte de crédit liées aux dépenses.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996208"
---
# <a name="set-up-credit-card-integration"></a>Configurer l’intégration des cartes de crédit

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les transactions par carte de crédit liées aux dépenses peuvent être configurées afin d’être automatiquement importées selon un calendrier récurrent. Les transactions peuvent également être importées manuellement selon les besoins. Les transactions par carte de crédit sont importées via l’entité de données des transactions par carte de crédit.

## <a name="import-credit-card-transactions"></a>Importer des transactions par carte de crédit

Pour importer des transactions par carte de crédit, procédez comme suit :

1. Sur la page **Transactions par carte de crédit**, sélectionnez **Importer des transactions**. Si vous ouvrez la gestion des données pour la première fois, le système doit mettre à jour la liste des entités de données avant de pouvoir continuer.
2. Dans le champ **Nom**, entrez une description unique pour la tâche d’importation.
3. Dans le champ **Format des données source**, sélectionnez le format du fichier contenant les transactions par carte de crédit à importer.
4. Cliquez sur **Charger**, puis recherchez et sélectionnez le fichier à importer.
5. Une fois le fichier téléchargé, validez le mappage du fichier de transaction par carte de crédit et les colonnes de l’entité de données de transactions par carte de crédit en sélectionnant le lien **Afficher la mise en correspondance** sur la vignette. S’il existe des erreurs de mappage ou si vous devez modifier le mappage, apportez les changements nécessaires à partir de l’onglet **Visualisation du mappage** ou **Détails du mappage**.
6. Pour automatiser l’importation des transactions par carte de crédit, cliquez sur **Créer une tâche de données répétitive**. Vous pouvez ensuite définir la périodicité correspondante, à savoir la fréquence d’importation des transactions par carte de crédit. Ensuite, cliquez sur **OK**.
7. Pour importer le fichier sélectionné maintenant, cliquez sur **Importer**.
8. Si des erreurs se produisent lors de l’importation, vous pouvez afficher le journal d’exécution ou les données intermédiaires pour voir les erreurs que vous devez corriger pour garantir une importation réussie.

> [!NOTE]
> Si vous devez importer plusieurs formats de fichier, vous devez créer des tâches d’importation distinctes pour chaque type de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Réaffecter les transactions par carte de crédit pour les employés licenciés

Lorsqu’un employé est licencié, son compte Services de domaine Active Directory (AD DS) est désactivé. Cependant, il peut y avoir des transactions par carte de crédit actives qui doivent encore être passées en charges et remboursées. Sur la page **Transactions par carte de crédit**, vous pouvez réaffecter l’employé pour toute transaction par carte de crédit pour laquelle l’employé associé ne fait plus partie de la société.

Sélectionnez une ou plusieurs transactions par carte de crédit, puis sélectionnez **Réaffecter les transactions**. Vous pouvez ensuite sélectionner un autre employé auquel affecter les transactions par carte de crédit. Une fois que les transactions par carte de crédit ont été réaffectées, elles peuvent être sélectionnées pour une note de frais et payées selon le processus habituel de remboursement des notes de frais.

## <a name="delete-credit-card-transactions"></a>Supprimer les transactions par carte de crédit 

Parfois, après l’importation de transactions par carte de crédit, certaines transactions peuvent devoir être supprimées. Cela peut être dû au fait que des transactions sont en double ou que les données peuvent ne pas être exactes. Les administrateurs peuvent utiliser la fonctionnalité **Supprimer les transactions par carte de crédit** pour sélectionner et supprimer les transactions par carte de crédit **qui ne sont pas attachées** à une note de frais. 

1. Accédez à **Tâches périodiques** > **Supprimer les transactions par carte de crédit**.
2. Sélectionnez **Filtrer** et fournissez des informations pour identifier les enregistrements à inclure.
3. Sélectionnez **OK** pour supprimer les enregistrements. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
