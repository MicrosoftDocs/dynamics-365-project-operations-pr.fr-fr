---
title: Configurer une création de facture automatisée
description: Cette rubrique fournit des informations sur la façon de configurer le système pour générer automatiquement des factures.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005338"
---
# <a name="configure-automatic-invoice-creation"></a>Configurer une création de facture automatisée

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Effectuez les étapes suivantes pour configurer une exécution de facture automatisée dans Dynamics 365 Project operations.

1. Accédez à **Paramètres** > **Traitements par lots**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure les mots « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les options **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Cliquez sur **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, les trois flux de travail suivants s’affichent :

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis cliquez sur **Ajouter**.
6. Dans la boîte de dialogue suivante, cliquez sur **OK**. Un flux de travail **Sleep** est suivi d’un flux de travail **Process**.

  > [!NOTE]
  > Vous pouvez également sélectionner **ProcessRunner** à l’étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d’un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée en fait les factures. Il traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée des factures pour ces lignes. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, le traitement par lots examine les dates d’exécution des factures pour les lignes de contrat. Si des lignes de contrat appartenant à un contrat sont associées à la même date d’exécution de la facture, les transactions sont combinées en une seule facture comportant deux lignes de facture. Si aucune transaction ne nécessite la création d’une facture, le traitement par lots ne procède à aucune création.

Une fois **ProcessRunner** exécuté, il appelle **ProcessRunCaller**, fournit l’heure de fin, puis est fermé. **ProcessRunCaller** démarre alors un minuteur qui s’exécute pendant 24 heures à compter de l’heure de fin spécifiée. À la fin du minuteur, **ProcessRunCaller** est fermé.

Le processus de traitement par lots pour la création de factures est une tâche récurrente. Si ce processus de traitement par lots est exécuté plusieurs fois, plusieurs instances de la tâche sont créées et provoquent des erreurs. Par conséquent, vous devez démarrer le traitement par lots une seule fois, et vous devez le redémarrer uniquement s’il cesse de s’exécuter.

> [!NOTE]
> La facturation par lots ne s’exécute que pour les lignes de contrat de projet qui sont configurées par des calendriers de facturation. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d’un calendrier de facturation basé sur la date. Il en va de même pour une ligne de contrat basée sur un projet.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]